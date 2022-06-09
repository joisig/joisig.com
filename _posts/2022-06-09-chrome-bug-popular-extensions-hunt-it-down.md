---
layout: post
title: A Chrome bug affects 3-5% of users of 5+ popular extensions. Help hunt it down!
description: 
date: 2022-06-09 16:14:00 +0000
author: joisig
comments: true
categories:
  - coding
  - extensions
  - google
  - CrankWheel
---

**TL;DR:** After one of the updates for Chrome 100, my company's browser extension stopped working for a small percentage of users, and after lots of digging, it looks like the same issue occurs in several of the most popular Chrome extensions out there. We are certain it's a bug in Google Chrome itself. The bug is very elusive and remains hard to reproduce, even after 8 weeks of non-stop legwork. This post documents some of the things we've tried, and details how you can help. BTW, there are two separate US $4,000 bounties for whoever can find a reliable repro or a fix.

## Prelude

My company, [CrankWheel](https://crankwheel.com/), has an optional Chrome extension that improves the ergonomics of our telesales-oriented screen sharing web app, and which is required by a handful of features mostly used by enterprises. The Chrome web store has also been a very good distribution channel for us, so we rely quite a bit on our extension.

Around April 10th, we started getting reports from several users that clicking the CrankWheel button in their browser was not causing anything to happen. Our initial suggestion to users was to disable and re-enable our extension, and that seemed to do the trick.

Five days later, the issue randomly reproduced on my machine, and I was able to confirm that it is a Google Chrome / Chromium problem, not a problem with our extension, and I registered [an issue on the Chromium issue tracker](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588), along with screen recordings that confirm the reproduction and provide some extra detail.

How do I know it's a Chromium issue? Because I was able to inspect our extension's background page (see [comment #4](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588#c4)), see that no errors were occurring, and that events dispatched locally were firing, whereas identical events that should be dispatched to the extension based on external things happening (such as clicking our browser action button) were not firing or not getting delivered to the extension.

Timing was also a factor. Although we change our web app all the time, our extension is fairly small and simple and we hadn't made any code changes to it for a good long while, whereas version 100 of Chromium started rolling out to Google's stable channel for Chrome basically the same day as we started getting reports.

I was on the Chromium team [a long time ago](/why-i-left-google/), so although my knowledge is dated, I know a fair bit about the architecture and how to work with Chromium, which has helped. I was also fortunate enough to still have some old friends at Google, who I could ping to see if they agreed that the issue would be worthy of some attention from the extensions team. Within a week of the bug being filed, `rdevl...@`, who I believe leads the Chromium extensions development nowadays, had helpfully responded with some things to check, and has since helped move the issue along.

After the things `rdevl...@` suggested had been checked and deemed not to be culprits, we were asked if possible to provide a dump of the `chrome://extensions-internals` page, or the part of it that had details on our extension, while the issue was reproducing. Unfortunately the issue has reproduces for our team seldom and completely at random, and for a long time we didn't have this.

In this initial period, I also reached out to the [Chromium Extensions mailing list](https://groups.google.com/a/chromium.org/g/chromium-extensions) to see if this bug had affected other extensions by authors on the list. Initially there was nobody, then there was one, more on that in the next section - but trying to find other extension authors dealing with this issue remained in the back of my mind.

## MV3?

For over a year now, Google has been working towards deprecating "Manifest Version 2" (MV2) for Chrome extensions and moving to version 3 (MV3) which changes from using background event pages to service workers, removes some of the APIs commonly used by ad blockers, and improves many other APIs. The currently upcoming deprecation deadlines are that this month, you can no longer add new publicly-available MV2 extensions to the Chrome Web Store (even if they are unlisted), and in January 2023 all MV2 extensions will be removed from the Web Store.

Fairly early after we started working to understand the Chromium bug, someone pointed out to me that maybe we should switch to MV3 to see if that fixes the issue, as well as to maybe help get more attention on the problem, since Google's focus for a while has been on MV3.

We were able to convert our extension to MV3 in the span of a few working days, and then test that it was working correctly, so we thought we might be ready to update to that.

Not so fast - somebody from the Chromium Extensions mailing list commented on the issue, revealing a similar (but not quite identical) [known issue with MV3 extensions](https://github.com/GoogleChrome/developer.chrome.com/issues/2590), and then during testing we found that we were able to reproduce that issue more easily than the original MV2 issue, and then finally it turned out that this was an [already-registered issue with MV3 in the Chromium issue tracker](https://bugs.chromium.org/p/chromium/issues/detail?id=1271154) and that a fix would be included in Chrome 102 once it rolled out to stable.

So we waited, but we also start testing against Chromium 102 (beta channel at this point).

The day of the version 102 roll-out to stable comes (May 23rd) and we're getting ready, but while looking at our pre-push checklist, we note that several of our larger customers are a couple of versions behind the Google Chrome stable channel, sometimes even more than that. So we can't really roll the MV3 extension out as our main extension yet. (As a side note, there is no mechanism in the Web Store to give users different versions based on what browser version they have; you can specify a minimum supported version, but that would cause new employees of some of our largest customers not to be able to install CrankWheel until their organization updates to a supported version).

Good thing we didn't roll out MV3, though. Further testing revealed that the issue still occurs with an MV3 extension in Chrome 102, and this has since then been confirmed by a couple of other folks.

## More details, scary news from users, and some help!

We happened to get a repro case with the MV2 extension, and were able to provide the `chrome://extensions-internals` [details for the extension while the issue reproduced](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588#c25). These details show over 3000 `keepalive` entries, mostly for messages related to events the extension subscribed to like `chrome.windows.onRemoved`, that I understand to be unhandled messages that should keep the extension background process alive. My theory is that messages are not being delivered to the extension process. So far, we haven't heard back from Google whether this information is helpful.

About a week after we had to abort the roll-out of our MV3 extension, on June 2nd and 3rd, we got some scary news from 4 users: The workarounds that we had been providing (enabling/re-enabling, or uninstalling/re-installing the extension, or quitting the Chrome browser and starting it again) were all failing. One of these users even confirmed that they had also tried rebooting their machine and even tried uninstalling and re-installing Google Chrome itself.

We fortunately haven't heard from more users of a problem like that, but that doesn't mean it's not happening. We redoubled our efforts at this point.

The day after, we had some luck. User `orego...@gmail.com` added a [comment](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588#c32) that they had confirmed a rperoduction of the issue in two popular extensions, [Google Mail Checker](https://chrome.google.com/webstore/detail/google-mail-checker/mihcahmgecmbnbcchbopgniflfhgnkff) which is an extension with over 3 million users, made by Google, and [Mute Tab](https://chrome.google.com/webstore/detail/mute-tab/blljobffcekcbopmkgfhpcjmbfnelkfg), an extension with over 400 thousand users. Thank you kind stranger, this really helped!

## Two others. Could there be more?

I decided to approach the problem in two ways, given the new information about other extensions:
   1. What did CrankWheel, Google Mail Checker, and Mute Tab have in common? Could this lead to an extension that would reproduce the issue?
   2. Could we find other extensions where user feedback in reviews or support channels might indicate that their users were running into the same issues?

### Reproducing based on commonalities

Let's start with trying to reproduce the issue. Before we got the news about those two extensions, I'd written a few iterations of a simple Chrome extension, trying to get a reproduction going. This Chrome extension used most of the extension APIs that CrankWheel does, but also tried to do a bunch of things in an autoamted way to create traffic and load on the extensions system. I went through 8 different revisions of this (you can see the history in the [public GitHub repo](https://github.com/CrankWheel/chrome-ext-repro)), with no reproduction.

Once I was able to look at the three extensions together, it turned out that what they had in common was, they all modify the icon and/or badge text of the browser action button. I [updated my test extension](https://github.com/CrankWheel/chrome-ext-repro/compare/5bf534e..f5b7787) to do almost just that, but (on a hunch) to also do it on an alarm that was just long enough to allow the extension page to go to sleep in between these actions happening.

That very day I got two reproductions in a row, after leaving the test extension running for about 30 minutes each time, doing some work for a while (using the same browser) but also stepping away from the computer for maybe 10 minutes at a time. I reported that success back on the [Chromium issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1271154) and was hoping others would try the reproduction and have success with it. Perhaps you, dear reader, would try? Instructions in [this comment on the issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588#c35).

That said, it doesn't seem that the reproduction is consistent. The day after, I got no repro, even though I ran 12 different user profiles in Chrome on a Windows machine with the extension running, as well as 12 different user profiles in my debug build of Chromium on a macOS machine. However, the day after that, with still no repro on those 12 user profile setups, I did get a repro out of nowhere in my main browser. So it seems that either this is completely random, or you need to do some other stuff in your browser to tickle the bug, I'm just not sure what.

### Systematically searching for other extensions that tickle the bug

A couple of days ago, I sat down and started systematically looking for other extensions that might be causing the Chromium bug to reproduce.

My methodology was as follows, and all code I wrote for this is in the [same repo as the reproduction extension](https://github.com/CrankWheel/chrome-ext-repro):

For each of the top 100 Chrome extensions by popularity (based on the 2021 list in [this repository](https://github.com/DebugBear/chrome-extension-list)):

   1. Download the extension's CRX file, and unzip it, using a couple of Bash scripts;
   1. Fetch the most recent 20 reviews for the extension, in English;
   1. Based on grepping the source code after extracting CRXes, make a list of IDs of extensions that were calling the `chrome.browserAction.setIcon` or `chrome.browserAction.setBadgeText` APIs, then pipe that through `sort` and `uniq` to have a unique, sorted list;
   1. By grepping the reviews for keywords like "stopped working", "not working", "does nothing" and a few more, made a list of IDs for extensions that seemed like they have users complaining about issues that sound like they might be this bug;
   1. Used `diff` to diff those two lists to find the extensions they had in common (and it turns out, there was quite a lot of overlap between the two lists);  and then
   1. I manually read through the recent reviews (newer than ~March 2022) and support section (when available on the Chrome Web Store) to see if I could find comments that made it sound quite likely that it could be the same issue causing trouble.

I did the above for the top 100 extensions, and later, I ended up just doing a grep for keywords like "stopped working" for all extensions in the top 300 positions sorted by popularity.

### Several extensions found!

In the end, I found the following extensions, with my personal estimate of confidence that it's the same bug (I didn't report any extensions where I wasn't at least 70% confident):

| Name | Number of users | Example user feedback | Confidence |
| [LastPass: Free Password Manager](https://chrome.google.com/webstore/detail/lastpass-free-password-ma/hdokiejnpimakedhajhdlcegeplioahd) | 10,000,000+ | "Lastpass wont open anymore on Chrome. The icon for lastpass is there ,but when I click to open my vault, nothing happens. Please fix this. It is on my extensions, and nothing has changed. Just suddenly it wont open my vault. I can access it on you website though" | 80% |
| [Screencastify - Screen Video Recorder](https://chrome.google.com/webstore/detail/screencastify-screen-vide/mmeijimgabbpbgpdklnllpncmdofkcpn) | 10,000,000+ | "Since last three -four days Screencastify - not working on my google chrome extension, whenever i clinking on it, it never start the task. Even i remove the extension and retired it. but after than same issues i am facing." | 80% |
| [Norton Password Manager](https://chrome.google.com/webstore/detail/norton-password-manager/admmjipmmciaobhojoghlmleefbicajg) | 4,000,000+ | Review May 13th: "I used to really like this, bur recently it randomly fails to launch and has to be reinstalled.  Presents a poor impression of the whole Norton suite", and review May 5th, "The chrome extension doesn't work consistently. I have to remove and reinstall it every time I reboot. When it works it's great, but when it doesn't it just shows a blank page when trying to access the vault." | 70% |
| [Mendeley Web Importer](https://chrome.google.com/webstore/detail/mendeley-web-importer/dagcmkpagjlhakfdhnbomgmjdpkdklff) | 2,000,000+ | "Have been using for a long time and it stopped working. I uninstalled and re-installed it, and still no response when pressing the button" and "Does not work at all. Pressing the extension does nothing" (and last extension update was months before the former review). | 80% |
| [Picture in Picture Extension (by Google)](https://chrome.google.com/webstore/detail/picture-in-picture-extens/hkgfoiooedgoejojocmhlaklaeopbecg) | 2,000,000+ | "was good but recently (like in the last week), it has stopped working for me. i have needed to remove then redownload it when this happens" | 80% |
| [CrxMouse Chrome™ Gestures](https://chrome.google.com/webstore/detail/crxmouse-chrome-gestures/jlgkpaicikihijadgifklkbpdajbkhjo) | 700,000+ | Multiple recent reviews claim it stopped working from 100.0.4896.60, needs to be enabled at each run, etc. Not sure it's the same issue but the timing/version is conspicuously similar. | 70% |

Let's add to that list these three extensions; the Save to Pocket one is an MV3 extension that I found, so most likely not this exact bug but rather the related issue (which in the end may turn out to be the same underlying issue, who knows), then there's the two MV2 extensions reported by `orego...@gmail.com`, and to round out the list I've added CrankWheel:

| Name | Number of users | Example user feedback | Confidence |
| [Save to Pocket](https://chrome.google.com/webstore/detail/save-to-pocket/niloccemoadcdkdjlinkgdfekeahmflj) | 2,000,000+ users | "Randomly stops working in Chrome and does nothing until disabled and re-enabled. No longer shows if a page has been saved to Pocket already." Note also a couple of places where somebody responds to users' issues with "When it stops working, go to extension options and disable then re-enable it." | 90% |
| [Google Mail Checker](https://chrome.google.com/webstore/detail/google-mail-checker/mihcahmgecmbnbcchbopgniflfhgnkff) (by Google) | 3,000,000+ | "nothing happens when I click on the extension." and the response "Until they fix it, a work around, right click on it, select "manage extension", turn it off for a few seconds then turn it back on. Should work now, for awhile anyhow." | 100% |
| [Mute Tab](https://chrome.google.com/webstore/detail/mute-tab/blljobffcekcbopmkgfhpcjmbfnelkfg) | 400,000+ | "As others have noted it will sometimes stop working. Clicking on it does nothing, not even toggling the icon. I've found that restarting Chrome makes it work again. Unfortunately I don't have any more specifics than that." and "Chrome just updated to Version 100.0.4896.127, and the plugin (version 1.4) stopped working. It does not respond to the mouse clicks to mute the tabs." | 90% |
| [CrankWheel Screen Sharing](https://chrome.google.com/webstore/detail/crankwheel-screen-sharing/dooinopjfnhlmmdkdepajfipfhlcmjgp) | 50,000+ | Many reports through our support channel, and confirmed reproductions within our own team. | 100% |

## 2 months in, still elusive. Can you help?

At the time of writing, this bug has existed in Google Chrome's stable channel for about two months (at least since April 10th, 2022).

I would love for the community's help with this issue. It is clear that it is affecting not just CrankWheel users but users of at least several highly popular Chrome extensions out there.

Here are some ways to help:

### Star the issue

More stars on an issue helps up its priority with the Chromium team. Simply [click here](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588), log in with a Google account (top right) and click on the star icon (near the top left).

### Get other impacted extension authors tracking the issue

If you know any of the authors of the extensions listed above, please encourage them to chime in on the [Chromium issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588) where they can add any details they are able to share, or just chime in that they are seeing this issue impact them and would love to get it fixed.

### Consistent reproduction

A way the Chromium team often tracks down elusive issues is to do a [bisection](https://en.wikipedia.org/wiki/Bisection_(software_engineering)), but this is impossible without a consistent way to reproduce the issue within a reasonable amount of time, with a low occurrence of false negatives.

If you try the [simple reproduction extension](https://github.com/CrankWheel/chrome-ext-repro) that I created, and figure out a way to get the issue to consistently reproduce, either through manual steps or with some code changes to the extension, or you come up with some whole new way to consistently reproduce the issue, that would be tremendously helpful and very likely lead to solving the issue soon.

The best way to document a reproduction scenario is on the [Chromium issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588).

### Wizardry

If you are a Chromium wizard, perhaps you can figure out what is going wrong simply by looking at the code and finding a what is causing the problem? Perhaps a race condition, deadlock or other timing issue?

## Bug bounties offered

<strong>CrankWheel is offering a bounty of $4,000 US for a consistent reproduction scenario.</strong> Be first to submit (on the [issue](https://bugs.chromium.org/p/chromium/issues/detail?id=1316588)) the steps (manual and/or automated) that will consistently (90% or more) reproduce the issue in less than half an hour, we will validate the repro, and then you can send a PayPal invoice to CrankWheel's support address. PLEASE do not spam the issue with repro steps unless they are consistent or lead to a repro more frequently than the current state of knowledge on the issue.

For a Chromium wizard who manages to fix the bug, most likely, this would also let you create a consistent repro and claim the bounty above, but <strong>CrankWheel is also offering a separate bounty of $4,000 US for a confirmed fix to the issue, that is accepted as a pull request by the Chromium team.</strong> A confirmed fix would be if we also have a consistent reproduction scenario by that time and are able to verify the fix using it. If we don't, and there are one or more fixes made that show reasonable grounds for why they would fix the issue, and the issue goes away per user reports in the next stable channel update after, then we would pay a combined bounty of $4,000 US split evenly between the authors of such fixes. If you have a proposed fix that can't be confirmed, feel free to send it to CrankWheel's support channel for feedback, before submitting your pull request to Chromium.

## That's all folks!

I hope this has been an interesting read, and furthermore I truly hope you can help us and users of Chrome extensions!
