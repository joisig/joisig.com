---
title: "The $0 Subscription Startup Stack — Part 1: Build a product"
date: 2017-07-16T12:59:09+00:00
author: joisig
layout: post
permalink: '/0-subscription-startup-stack-part-1-3/'
canonical_url: https://startupresources.io/blog/the-zero-subscription-startup-stack-part-one/
categories:
  - startups
---
> This article was originally published on the [Startup Resources blog](https://startupresources.io/blog/the-zero-subscription-startup-stack-part-one/).

<img class="progressiveMedia-image js-progressiveMedia-image" style="color: #333333; font-size: 18px; font-weight: 400;" src="https://cdn-images-1.medium.com/max/1600/0*cpjXuDdE3vj1iIMh.jpg" data-src="https://cdn-images-1.medium.com/max/1600/0*cpjXuDdE3vj1iIMh.jpg" />

I've been building a SaaS startup for a couple of years now, and one of the things I noticed after a few months of operation is that all those small subscriptions I had for various things needed for the operation of the startup really start to add up. We have enough revenue now that those subscriptions don't matter so much, but there was a time when they were a burden, particularly since we were bootstrapping.

I got to thinking whether it would be possible to build a startup stack with $0 in monthly subscriptions, and after putting together a list of the various tools we've been using, and looking for replacements for some of them where you can avoid the monthly subscription, I figured that this would be quite doable.

In this series of three articles, I'll cover the different areas most startups need some help with, and list tools and approaches all of which have no fixed cost per month. Most of these are completely free, at least up to some decent level of usage, although some of the alternatives I list are zero subscription in the sense that you pay no fixed monthly fee although you do pay a small fee per usage.

Some of the services you use early on have high switching costs. I'll try to point out tools that are like this, and give my advice on cases where I feel it may be good to invest some money early on to get you on the appropriate tool from day one, rather than having to spend a lot of time switching later.

I've spent almost 11 years doing startups (and almost 10 years leading technical projects at Google), but my recent startup experience is primarily from building a SaaS startup, so I'll be able to provide the most relevant advice on categories of tools used by such startups. Many of the same tools apply to any type of startup, and I'll also try to cover a few specialized tools other types of startups need, e.g. e-commerce startups, but I'm not an authority on those.

This first article of three will focus on tools you need to build a product and run it. The second installment will focus on how to get your product in front of your users, and how to make sales. The third and final installment will talk about all the other things you need to run a successful business: Accounting, customer support, billing, legal, financing and more.

Let's dive in, shall we?

<img src="https://cdn-images-1.medium.com/max/1600/0*OBge7EAJdff-KNgd.jpg" />

## Ideation and Validation


Startups typically start with an idea. In this section, we'll explore some tools and approaches that can help develop your idea, validate it by getting it in front of potential users, and more.

I recommend pitching your idea to potential customers very early, and very often, to avoid building the wrong product or service. Even if you think you're all for this idea and will do super early pitches to real decision makers at potential customers, take my advice: Whatever the earliest you would feel comfortable with pitching a customer would be, do it twice as early, and do it twice as often as you planned to before reading this paragraph. Here are some tools to help you.

### Mockups

Showing your potential customers a mockup of your product can be a great way to get early feedback. Having a rough design for your user interfaces ready will make it that much easier to explain your vision and get actionable feedback.

The cliché here is that your first mockup should be hand drawn on the back of a paper napkin is actually pretty close to how rough your early mockups should be before you start talking to customers.

Once you get a bit further, sketch-like mockup tools are all the rage. I use <a class="markup--anchor markup--p-anchor" href="https://balsamiq.com/" target="_blank" rel="nofollow noopener" data-href="https://balsamiq.com/">Balsamiq</a>, which is a great tool, but it doesn't have a free version except for a free trial. <a class="markup--anchor markup--p-anchor" href="https://ninjamock.com/" target="_blank" rel="nofollow noopener" data-href="https://ninjamock.com/">NinjaMock</a>, which has been featured right here on <a class="markup--anchor markup--p-anchor" href="https://startupresources.io/" target="_blank" rel="nofollow noopener" data-href="https://startupresources.io/">StartupResources.io</a> for a while, uses a similar style of sketch-like mockups and they have a free plan; the only catch is that your projects on this plan are public.

A similar tool with a different type of free plan is <a class="markup--anchor markup--p-anchor" href="https://moqups.com/" target="_blank" rel="nofollow noopener" data-href="https://moqups.com/">Moqups</a>. Their free plan lets you have just one project, with up to 300 objects.

Another type of mockup is what's called a design prototype, and looks a lot closer to a finished product although with no functionality behind anything. A very popular tool for this is <a class="markup--anchor markup--p-anchor" href="https://www.invisionapp.com/" target="_blank" rel="nofollow noopener" data-href="https://www.invisionapp.com/">InVision</a>, and they have a free plan that lets you work with a single design prototype.

I like Reddit, and I recently stumbled upon an <a class="markup--anchor markup--p-anchor" href="https://www.reddit.com/r/startups/comments/6imzrg/why_product_clickable_prototype_is_different_and/" target="_blank" rel="nofollow noopener" data-href="https://www.reddit.com/r/startups/comments/6imzrg/why_product_clickable_prototype_is_different_and/">interesting thread there on the subject of prototypes and mockups</a>, that mentions a few other tools.

Remember, don't just build your mockups and prototypes. Get feedback from your team or friends and colleagues in the same industry, iterate on your mockup, then go out there and get it in front of potential customers for more valuable feedback.

### User Testing

Your first quite-a-few go-arounds of getting user feedback should be done completely manually and by interacting with real people directly.

The way we did this manually at my startup, <a class="markup--anchor markup--p-anchor" href="https://crankwheel.com/?ref=startupresources" target="_blank" rel="nofollow noopener" data-href="https://crankwheel.com/?ref=startupresources">CrankWheel</a>, was first to pitch to potential customers, and then as our product started being closer to usable, to do hallway testing. Hallway testing is when you grab people from the hallway and ask them to try to achieve some goals with your product or service while you step out of the room, but maybe record their interactions to see what they get stuck on and why. How to do this could be the subject of a whole separate piece; if you'd be interested in a piece on that, get in touch.

Once you're slightly further advanced, you'll probably want to use some tools.

A very neat tool is <a class="markup--anchor markup--p-anchor" href="http://peek.usertesting.com/" target="_blank" rel="nofollow noopener" data-href="http://peek.usertesting.com/">Peek</a>, which lets you get a 5-minute video of a person using your website or app (along with their comments while using it), for free. If I recall correctly there are some limits on how often you can do this, but it's a very useful service nonetheless, that <a class="markup--anchor markup--p-anchor" href="https://www.usertesting.com/" target="_blank" rel="nofollow noopener" data-href="https://www.usertesting.com/">UserTesting</a> (a very useful but pretty expensive service) uses as a teaser of their full set of paid services. If you can afford them, great, they seem to be a leader in this space, but most startups starting out can get by with hallway testing instead, as briefly described above.

Another great resource is <a class="markup--anchor markup--p-anchor" href="https://usabilityhub.com/" target="_blank" rel="nofollow noopener" data-href="https://usabilityhub.com/">UsabilityHub</a>. They have a $0/month plan and as long as you invite your own testers, using their platform to run tests on that plan is completely free. Using testers from their network is a pretty reasonable $2.50 per test.

I'll also sneak in Stuart Brent's <a class="markup--anchor markup--p-anchor" href="https://userinput.io/" target="_blank" rel="nofollow noopener" data-href="https://userinput.io/">UserInput.io</a>. There is no free plan, but no subscription either — it's pay per use. This could be an alternative to UserTesting but at a much lower price point.

### Business Model Canvas

This is less of a way to validate your idea, and more a way to ensure that you're thinking about the various different angles that might need validation. The <a class="markup--anchor markup--p-anchor" href="https://en.wikipedia.org/wiki/Business_Model_Canvas" target="_blank" rel="nofollow noopener" data-href="https://en.wikipedia.org/wiki/Business_Model_Canvas">Business Model Canvas</a> is a very simple framework for putting a startup idea down on paper and understanding how it's different, how it will make money, how you will get it in front of customers, and more.

You don't really need a tool for this, there are lots of free templates you can download and fill in, but if you want a free and simple tool, you could try <a class="markup--anchor markup--p-anchor" href="https://canvanizer.com/" target="_blank" rel="nofollow noopener" data-href="https://canvanizer.com/">Canvanizer</a>.

### Validation from Investors

One good way to get often quite insightful feedback on your idea is to create a pitch deck and/or demo for it, and show it to some angel investors or VCs, and maybe apply for some accelerators. Even if you don't get funded or accepted to an accelerator, you should most often get valuable feedback.

I would only recommend doing this if you are actually open to taking in outside funding, or joining an accelerator. You don't want to burn any bridges you might want to cross in the future by making people feel like you wasted their time.

<img class="progressiveMedia-image js-progressiveMedia-image" src="https://cdn-images-1.medium.com/max/1600/0*qanyRKYUf121JieQ.jpg" data-src="https://cdn-images-1.medium.com/max/1600/0*qanyRKYUf121JieQ.jpg" />

## Product Development

This section focuses on tools you need to develop digital products. I realize not all startups are built around a digital product, but most have at least a website, which sort of qualifies.

It used to be you would need to pay lots of money for software libraries that you were going to use to build your product on. Those days are gone, with open source providing a free implementation for an incredibly wide range of things. Hooray! So what is left? Well, it turns out, quite a lot.

You may need to find and hire folks to work on developing your product. Maybe you've got this covered yourself, or through your co-founder(s) or close contacts that you can recruit, but maybe not.

You need a safe place to keep everything you're developing, track versions, keep track of bugs, and so on.

You also need to manage your development project, get your product tested, and more.

Let's start with a couple of tools to help you recruit talent, if you need it.

### Talent

If you have local talent available and vetted by yourself or somebody you trust, that is often the very best way to start. Perhaps they are willing to work for some sweat equity, or even join up to become a co-founder.

If you're not in a position to find the very best local talent, you may want to look online.

If you don't have much time to spend and are willing to pay for the value you get, I would recommend <a class="markup--anchor markup--p-anchor" href="https://www.toptal.com/#assume-first-rate-engineers" target="_blank" rel="nofollow noopener" data-href="https://www.toptal.com/#assume-first-rate-engineers">Toptal</a>. They have programmers, designers, and even finance professionals who can help you, and they hire only the top 3% of everybody who interviews with them, and they expect and enforce a high level of quality. There's a no risk trial period so if you're not happy with the person they find for you, you don't have to pay.

If you have more time and are able to take a chance on trying a few people before you find the right fit, then check out <a class="markup--anchor markup--p-anchor" href="https://www.upwork.com/" target="_blank" rel="nofollow noopener" data-href="https://www.upwork.com/">Upwork</a>. I've been able to find some good talent there at a good rate, but be advised that you may need to work with a few people before finding a strong talent and a good match in terms of ease of working with that person.

Obviously, neither Upwork nor Toptal are free, but both of them qualify for this article as there is no fixed subscription fee — rather, they are collecting a part of what you pay to the talent you hire through the platform.

### Project Management

Developing your product is a project that can sometimes get really complicated, with lots of moving parts and many people involved.

My favorite tool for the cat-herding involved in project management is <a class="markup--anchor markup--p-anchor" href="https://asana.com/" target="_blank" rel="nofollow noopener" data-href="https://asana.com/">Asana</a>. It's like a perfect to-do list that you can categorize, tag, prioritize, and the best part is that it does collaboration really well. Asana has a very generous free plan for up to 15 users in a team.

Taking a slightly different approach to project management, a lot of people really love <a class="markup--anchor markup--p-anchor" href="https://trello.com/" target="_blank" rel="nofollow noopener" data-href="https://trello.com/">Trello</a>. Instead of being based on the concept of a to-do list, the base concept feels more like boards on your wall with sticky notes where you can move sticky notes between boards. If you're doing something like <a class="markup--anchor markup--p-anchor" href="https://en.wikipedia.org/wiki/Kanban_%28development%29" target="_blank" rel="nofollow noopener" data-href="https://en.wikipedia.org/wiki/Kanban_(development)">Kanban</a> (we actually do this in my team but we use a real wall and sticky notes…), then it's a pretty perfect match. Like Asana, they have a very generous free plan with an unlimited number of users and boards, but lacking some features you may end up deciding to pay for.

###  Code Hosting

You need your code in a safe place, off-premises, and you need to be able to go back to any older version of your code. Choosing a cloud service built around a revision control system is the best way to achieve this, and these days the only revision control system I'd recommend you use is Git.

<a class="markup--anchor markup--p-anchor" href="https://bitbucket.org/" target="_blank" rel="nofollow noopener" data-href="https://bitbucket.org/">Bitbucket</a> by Atlassian fits the bill. It's built around Git and it is free for teams of up to 5 developers. I haven't used it personally but Atlassian is a solid company that's not going anywhere, and I've heard people speak well of Bitbucket. That said…

Your source code repository is one case of a system that has very high switching costs, so I would choose carefully here. My company uses <a class="markup--anchor markup--p-anchor" href="https://github.com/" target="_blank" rel="nofollow noopener" data-href="https://github.com/">GitHub</a>and we're very happy with it; if you're doing open source it's kind of the industry standard (and it's free if you only work with open source projects, no proprietary code). If you're incorporating open source projects hosted on GitHub into your product, it makes it pretty easy to work with those.

Any feedback on Bitbucket vs. GitHub from folks who have used both? I'd love to get your comments.

### Issue Tracking

I mentioned issue tracking in relation to GitHub above, so let's tackle that next.

You need a place to write down problems that are found in your product, to assign them to people, track whether they're new, fixed, have been verified as fixed, reopened, etc.

One way to do this for free is to track your issues in your project management tool, e.g. Asana or Trello, both of which I mentioned above. They're not specialized for this, but can do the job.

Both Bitbucket and GitHub have simple issue trackers integrated. This is probably the way to go to begin with, for most startups.

Switching cost caveat: If you have a fairly large and complex product, you may be better served by going with a more feature-rich issue tracker right off the bat. There are full-featured open source issue trackers available such as <a class="markup--anchor markup--p-anchor" href="https://www.mantisbt.org/" target="_blank" rel="nofollow noopener" data-href="https://www.mantisbt.org/">MantisBT</a>, <a class="markup--anchor markup--p-anchor" href="http://www.redmine.org/" target="_blank" rel="nofollow noopener" data-href="http://www.redmine.org/">Redmine</a> and the venerable <a class="markup--anchor markup--p-anchor" href="https://www.bugzilla.org/" target="_blank" rel="nofollow noopener" data-href="https://www.bugzilla.org/">Bugzilla</a>, and if you host them yourself, there is no subscription fee, although I'd recommend using a hosted version for peace of mind and simplicity. There are also products such as <a class="markup--anchor markup--p-anchor" href="https://www.fogcreek.com/fogbugz/" target="_blank" rel="nofollow noopener" data-href="https://www.fogcreek.com/fogbugz/">FogBugz</a> which some people swear by.

### Quality Assurance / Testing

The basics of quality assurance aren't that complicated, even though the work is challenging, especially to find the most elusive bugs. For much of what you need to start, you don't need any tools aside from your issue tracker and a documentation tool such as <a class="markup--anchor markup--p-anchor" href="https://gsuite.google.com/together/" target="_blank" rel="nofollow noopener" data-href="https://gsuite.google.com/together/">Google Docs</a>:

   1. For as much of your functionality as economically feasible, create automated tests to cover this functionality. This helps a great deal to avoid bugs creeping in later, and is a key component of <a class="markup--anchor markup--li-anchor" href="https://en.wikipedia.org/wiki/Continuous_integration" target="_blank" rel="nofollow noopener" data-href="https://en.wikipedia.org/wiki/Continuous_integration">Continuous Integration</a>, which I highly recommend. I say “as much as economically feasible” because for a startup in the early stages, you may be better off spending more time on manual testing and less time on automation, until your product is a bit more mature. Early stage products tend to change a great deal, which gives you less time over which to amortize the setup costs of the automated tests, whereas manual testing has close to zero setup cost, with the downside that the per-test cost is high.

   1. Have a written description for how to test your product, i.e. steps to take to run through all the basic test cases that will cover most of what your product does. Google Docs or any other documentation system is good enough for this.

   1. Create a test matrix of the different platforms your testing should be performed on. Depending on your product this may be a set of browsers and different versions of their browsers, or it could be a set of operating systems and different versions of those. In your test matrix you can specify which

   1. When your product is tested, it should be done based on the written test description, as well as exploratory testing outside of what's in the written description to try to find new defects in corner cases. For any new or changed features, you should also ask for hints from your developers on what they think might break or need a particular emphasis in testing.

   1. Any time you find an issue, register it in your issue tracking system and decide how to prioritize it, when to tackle it, etc. Your issue tracking system can help with this, for example you can break your releases down to milestones (for example once every 2–3 weeks) and determine which bugs to fix immediately and which bugs it may be OK to defer a little bit. This depends on their severity and how many users they may impact.

   1. Any time you find an issue that you would not have detected using your written test description, take a step to make sure this or similar issues do not come back in the future. Add an automated test that would have caught the problem, or add a test case to your manual test description that would have made the problem obvious in routine testing.

Your initial testing can be done by you and your core team, but I would recommend having a separate person doing quality assurance pretty soon after the ball gets rolling. For one, it's a somewhat specialized role and folks with experience in it will find more bugs than those without, and for another, you and your development team will become blind to defects in the product, and will do less creative exploratory testing. As for development, I would recommend <a class="markup--anchor markup--p-anchor" href="https://www.toptal.com/#assume-first-rate-engineers" target="_blank" rel="nofollow noopener" data-href="https://www.toptal.com/#assume-first-rate-engineers">Toptal</a> if you want to be sure you get a great team member without having to try several times, and if you're more budget conscious and have more time, you should be able to find somebody on <a class="markup--anchor markup--p-anchor" href="https://www.upwork.com/" target="_blank" rel="nofollow noopener" data-href="https://www.upwork.com/">Upwork</a>, but you do need to be willing to take that time and may end up spending a fair bit of money to try a few freelancers before you settle on somebody for the long term.

One key tool that I always recommend for quality assurance of web-based applications is <a class="markup--anchor markup--p-anchor" href="https://www.browserstack.com/" target="_blank" rel="nofollow noopener" data-href="https://www.browserstack.com/">BrowserStack</a>. It lets you run literally hundreds of different browsers on both desktop and mobile platforms right in the comfort of your browser. They used to have some of their features free, but no more (unless you have an open source project) — so I looked around for some alternatives for the $0 Subscription Startup Stack.

One alternative is <a class="markup--anchor markup--p-anchor" href="http://browsershots.org/" target="_blank" rel="nofollow noopener" data-href="http://browsershots.org/">Browsershots</a>, which is completely free and supports a range of browsers. It doesn't provide live testing though, only screenshots of your site across multiple different browsers and versions (this is the same service BrowserStack used to have for free).

Another that is now part of my toolchest is the <a class="markup--anchor markup--p-anchor" href="https://blisk.io/" target="_blank" rel="nofollow noopener" data-href="https://blisk.io/">Blisk</a> browser, available for Windows and macOS, which does emulation of multiple devices so that you can view your site for quality assurance, and in fact for development as well. Their free version includes some of the devices they support, and you can upgrade to get more.

<img class="progressiveMedia-image js-progressiveMedia-image" src="https://cdn-images-1.medium.com/max/1600/0*za4xLgA33RLBHKai.jpg" />

## Operations

Now that you've built a product, what about running it? Most digital products need to be hosted somewhere online. Many require functionality such as email, SMS, telephony, and more, that you're better off buying from a Platform as a Service rather than building and running those functions yourself. Finally, you will need to understand how your users use your products in order to be able to improve it, and for that you need product analytics. Let's explore each of these areas in turn.

### Hosting

There are several levels of hosting you could go for. The simplest and least expensive level is when you have a simple static page. The next level after that is when you need your own dynamic back-end but can make do with something like WordPress, in which case you need a shared web host. Finally, if you are running a complicated digital product, you will likely want your own custom backend that you might host in multiple geographic locations. In all cases, you may want to use a CDN in front of your site to speed it up and decrease load on your servers.

#### Static site hosting

My recommendation: If you can build your site as a static site, you should do so. Especially if you've got some coding skills. You can do this even with fairly complicated sites that accept user submissions, might have a blog, and more.

For static hosting, I would recommend <a class="markup--anchor markup--p-anchor" href="https://www.netlify.com/" target="_blank" rel="nofollow noopener" data-href="https://www.netlify.com/">Netlify</a>, which is simple to use and has a generous free plan. This is what I use for <a class="markup--anchor markup--p-anchor" href="http://startupresources.io/" target="_blank" rel="nofollow noopener" data-href="http://startupresources.io/">StartupResources.io</a>, which is a static site even though we have various forms you can submit (more on how to do that in the next installment in this series). You can either simply drop a folder on your Netlify deployment in order to upload that folder as a new version of your site, or you can integrate Netlify with GitHub to continuously publish any branch of any repository as soon as you push to that branch.

Another good alternative is <a class="markup--anchor markup--p-anchor" href="https://pages.github.com/" target="_blank" rel="nofollow noopener" data-href="https://pages.github.com/">GitHub Pages</a> which is built into GitHub, so if you're already using that it may be a very convenient alternative. I use this for the <a class="markup--anchor markup--p-anchor" href="https://crankwheel.com/?ref=startupresources" target="_blank" rel="nofollow noopener" data-href="https://crankwheel.com/?ref=startupresources">CrankWheel</a> marketing site and it works really well.

There are many free and easy static site builders that you can use to make a static site feel more like WordPress. For example, when I write a blog article for CrankWheel, I'm basically just writing a <a class="markup--anchor markup--p-anchor" href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank" rel="nofollow noopener" data-href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet">Markdown</a> file; no HTML or CSS. The static site builder that I've used and can recommend is <a class="markup--anchor markup--p-anchor" href="https://jekyllrb.com/" target="_blank" rel="nofollow noopener" data-href="https://jekyllrb.com/">Jekyll</a>, which takes a set of source and configuration files and builds the static files that get served up for your site.

For non-developers out there, you can still use static sites. Ask your web developer to set up the initial site using e.g. Jekyll, and then use a tool like <a class="markup--anchor markup--p-anchor" href="http://cloudcannon.com/" target="_blank" rel="nofollow noopener" data-href="http://cloudcannon.com/">CloudCannon</a> so that you have a visual, web-based editor for creating and editing blog posts and such.

#### Shared Hosting

Many companies offer shared hosting of WordPress and such. I need to do my research on this before creating a full comparison review, but <a class="markup--anchor markup--p-anchor" href="http://www.bluehost.com/track/startupres/" target="_blank" rel="nofollow noopener" data-href="http://www.bluehost.com/track/startupres/">Bluehost</a>comes highly recommended by many folks I've spoken to. While it's not free, you can sign up for as little as $3.95 per month <a class="markup--anchor markup--p-anchor" href="http://www.bluehost.com/track/startupres/" target="_blank" rel="nofollow noopener" data-href="http://www.bluehost.com/track/startupres/">using this link</a>, and you get more than $150 in advertising value with Google AdWords, Bing and other leading advertisers, which is more than you'll pay for the first 36 months.

#### Cloud Hosting

For the most complex needs, you'll want a cloud hosting provider. There are times when you might want to set up a virtual private server (VPS) rather than do cloud hosting, but in my opinion for almost any reasonably complex product, the ability to grow without switching providers is going to be very important, so I'd recommend going with cloud hosting.

I've primarily used <a class="markup--anchor markup--p-anchor" href="https://aws.amazon.com/" target="_blank" rel="nofollow noopener" data-href="https://aws.amazon.com/">Amazon Web Services</a> (AWS), and I've had a very good experience with it. I've also heard good things about <a class="markup--anchor markup--p-anchor" href="https://azure.microsoft.com/en-us/" target="_blank" rel="nofollow noopener" data-href="https://azure.microsoft.com/en-us/">Microsoft Azure</a> (it's not just Windows — you can run Linux on it too). The most important criteria for a provider to me would be that I have to trust that they will stay in business and won't cancel any of the platform services that I'm relying on, and both of these companies qualify.

Neither of those are free for serious usage, although both offer a free tier to get you started. However, as a startup you can apply for significant credits with both of them. With <a class="markup--anchor markup--p-anchor" href="https://aws.amazon.com/activate/" target="_blank" rel="nofollow noopener" data-href="https://aws.amazon.com/activate/">Amazon's startup program</a>, you can get up to $15,000 in credits that are valid for 2 years (even more in some cases), and with <a class="markup--anchor markup--p-anchor" href="https://azure.microsoft.com/en-us/pricing/member-offers/bizspark-startups/" target="_blank" rel="nofollow noopener" data-href="https://azure.microsoft.com/en-us/pricing/member-offers/bizspark-startups/">Microsoft's BizSpark program</a> you get up to $150 of cloud services per month for free (along with many other benefits), and up to $12,000 if you qualify for BizSpark Plus.

#### Content Delivery Networks (CDNs)

A CDN is a great way to reduce the load on your servers, and in some cases can also provide redundancy and protection in case of a distributed denial of service attack (DDoS). If you haven't already heard of <a class="markup--anchor markup--p-anchor" href="https://www.cloudflare.com/" target="_blank" rel="nofollow noopener" data-href="https://www.cloudflare.com/">CloudFlare</a>, then you should check them out. Just head over to their site and click Signup, and you'll be able to add a site for free. Their free plan is quite generous and includes a basic SSL certificate for your site, caching, and various other goodies that can speed up your site. They take over as the nameserver for your DNS. Setup is really easy. I use this for multiple sites.

### Platforms as a Service (PaaS)

#### Transactional Email

Transactional emails are those emails your system may send on account creation, password reset, confirmation of orders, shipping updates — the emails your customers definitely want to receive independent of their preference in terms of marketing email.

Don't set up your own mail servers to send transactional email (and definitely not marketing email — but that's for our next installment).

Use a service like <a class="markup--anchor markup--p-anchor" href="https://aws.amazon.com/ses/" target="_blank" rel="nofollow noopener" data-href="https://aws.amazon.com/ses/">Amazon SES</a> (Simple Email Service) for sending email. They have a <a class="markup--anchor markup--p-anchor" href="https://aws.amazon.com/ses/pricing/" target="_blank" rel="nofollow noopener" data-href="https://aws.amazon.com/ses/pricing/">free tier</a> for up to 62,000 messages per month, and pricing after that is not expensive — $0.10 per 1000 messages. I use this for CrankWheel and it's rock solid, although it doesn't have all the bells and whistles of <a class="markup--anchor markup--p-anchor" href="http://www.mandrill.com/" target="_blank" rel="nofollow noopener" data-href="http://www.mandrill.com/">Mandrill</a> (now part of MailChimp), <a class="markup--anchor markup--p-anchor" href="https://www.mailjet.com/" target="_blank" rel="nofollow noopener" data-href="https://www.mailjet.com/">Mailjet</a> (free for up to 6,000 messages a month) or <a class="markup--anchor markup--p-anchor" href="https://www.mailgun.com/" target="_blank" rel="nofollow noopener" data-href="https://www.mailgun.com/">Mailgun</a> (free for up to 10,000 messages a month).

A key issue with transactional email is deliverability, a.k.a. not getting your email marked as spam. Once you've got your basic setup for transactional email, use the free tool <a class="markup--anchor markup--p-anchor" href="https://www.mail-tester.com/" target="_blank" rel="nofollow noopener" data-href="https://www.mail-tester.com/">MailTester</a> to get hints on how to optimize for deliverability.

#### Non-Internet Communications

Do you remember life before the Internet? There used to be these things called telephones, which people would use to talk to each other, and a bit later there was this thing we now call a feature phone where you could send short text messages (SMS), it was like Facebook Messenger only without the GIFs.

It turns out, for many products, the ability to integrate with the telephone network or to send text messages can be extremely useful and effective. We use this at my startup to enable sending text message links to screen sharing sessions, and it's great because it works on all phones.

The platform I recommend for both telephony and text messaging is <a class="markup--anchor markup--p-anchor" href="https://twilio.com/" target="_blank" rel="nofollow noopener" data-href="https://twilio.com/">Twilio</a>. It's been around for a while, and I've personally witnessed text message deliverability improve quarter over quarter for the last couple of years.

#### Logs Analysis

If you've ever run a webserver or a custom server, you'll know how useful it can be to view server log files to diagnose problems.

There is a really useful class of services out there that allows you store logs from all of your different servers and machines in one centralized place, visualize them, query them, and create alarms based on them. I very much recommend setting this up if you have a complex product.

The solution I've used is <a class="markup--anchor markup--p-anchor" href="https://www.loggly.com/" target="_blank" rel="nofollow noopener" data-href="https://www.loggly.com/">Loggly</a>. It's a solid product, and it has a free tier that will be suitable for many startups.

There are significant switching costs for a product like this. I sometimes wish I'd gone for a metered product like <a class="markup--anchor markup--p-anchor" href="https://logdna.com/" target="_blank" rel="nofollow noopener" data-href="https://logdna.com/">LogDNA</a>, which is priced per usage, rather than going with a plan-based product like Loggly, where I've had many months where we were on a plan that was significantly too large for us. I haven't tried them, but they promise lower rates than Loggly, and much faster queries, which is an area where Loggly doesn't exactly shine.

#### Usage Analytics

If you have a complex product, read this section. If you just have a static site or a WordPress site, wait until the next installment in this series, where I'll talk about marketing analytics — that's all you typically need for a website.

Usage analytics are important so that you can see where your users are having trouble, compare retention rates between versions, and more.

Many of you have probably heard of <a class="markup--anchor markup--p-anchor" href="https://mixpanel.com/" target="_blank" rel="nofollow noopener" data-href="https://mixpanel.com/">Mixpanel</a>, which was the pioneer in the space of usage analytics, finally making it easy for small startups to track user churn, behavior funnels and more. They have a solid free offering.

The alternative that I recommend is <a class="markup--anchor markup--p-anchor" href="https://amplitude.com/" target="_blank" rel="nofollow noopener" data-href="https://amplitude.com/">Amplitude</a>. They were first to offer a generous free plan, and although their free plan today allows fewer events than Mixpanel's free plan, I can vouch that the free version of Amplitude is very powerful and lets you visualize and analyze a ton of stuff regarding how your users are behaving.

### Summary

We've covered ideation and validation, product development, and operations in this installment of <em class="markup--em markup--p-em">The $0 Subscription Startup Stack</em>.

The next installment will cover sales and marketing — how to get your product in front of your prospective users, and how to make revenues from them.

The third and final installment will cover other stuff you need to build and run a startup — customer support, billing, legal, funding and more.

I hope you've enjoyed this installment. I'd love to hear your feedback, just get in touch.
