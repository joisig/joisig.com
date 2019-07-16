---
id: 100
title: 'GDPR: The Quick and Dirty Guide to Getting Compliant for Startups and Small Business'
date: 2018-05-18T12:12:00+00:00
author: joisig
layout: post
guid: http://joisig.com/?p=100
permalink: /gdpr-the-quick-and-dirty-guide-to-getting-compliant-for-startups-and-small-business/
categories:
  - Uncategorized
---
A lot has been written about the European Union’s new data protection regulation, the [GDPR](https://gdpr-info.eu/), but not much of it is tailored for startups and small businesses, and a lot of it just muddies the picture of what you really need to do or gives you an incomplete picture.

In this guide, it is my intent to give you a simple set of steps you can take, **if you fit a particular profile** that will apply to many small businesses and startups, to become compliant enough to avoid fines, to treat your users fairly under the new regulation, and to work towards fuller compliance over time as the regulation gets interpreted and more best practices get established around what it means to be compliant (much of this is a bit vague at the moment). Read on for important legal disclaimers, and for details on the profile you need to fit for this guide to apply to you.[<img class="alignright size-full wp-image-101" src="http://joisig.com/wp-content/uploads/2018/05/private.jpg" alt="Private, photo by Dayne Topkin on Unsplash" width="1280" height="853" srcset="http://joisig.com/wp-content/uploads/2018/05/private.jpg 1280w, http://joisig.com/wp-content/uploads/2018/05/private-300x200.jpg 300w, http://joisig.com/wp-content/uploads/2018/05/private-768x512.jpg 768w, http://joisig.com/wp-content/uploads/2018/05/private-1024x682.jpg 1024w" sizes="(max-width: 1280px) 100vw, 1280px" />](http://joisig.com/wp-content/uploads/2018/05/private.jpg)

GDPR is in effect from May 25th, 2018, and whether you are based in the EU or not, you very likely will need to be compliant. If you have users living in the EU or [EEA](https://en.wikipedia.org/wiki/European_Economic_Area)then you need to comply. You will also need to comply if you process any personal data on users who live in the EU or EEA, even if that processing is done on behalf of a third party (i.e., the users are not directly _your_ users).

# Disclaimer

I am not a lawyer, and none of the advice in this guide should be taken as legal advice. This guide is based on my own discussions with lawyers and other experts on European data protection regulations, as well as my own research in figuring out how to make my own startup compliant, but **I strongly encourage you to seek your own legal counsel and expert advice** to ensure you do what is right in your own particular situation. I also encourage you to simply [read the regulation](https://gdpr-info.eu/), it is not so terribly long or dense.

We (I the author and StartupResources.io) make no warranties about the completeness, reliability or accuracy of this information, or its suitability to purpose. **Any action you take, or fail to take, based upon the information in this guide is strictly at your own risk**, and we will not be liable for any losses or damages in connection with the use of this guide.

# Profile you need to fit to use this guide

To keep this guide simple and concise, I’ve written it for a very specific profile that many startups and small businesses will fit. To avoid having to repeat the various criteria throughout the guide, please check whether you fit this profile:

  1. Your organization is a startup company or a small business. Not a public authority, non-profit, NGO, etc.
  2. You have fewer than 250 employees.
  3. You are not performing regular and systematic monitoring of people on a large scale.
  4. You don’t process personal information for children younger than 13.
  5. You do not process data revealing race, ethnic origin, political opinions, religious or philosophical beliefs, trade union membership, criminal history, genetic data, biometric data that can uniquely identify a natural person, health data, or data on sex life or sexual orientation.

If you don’t fit the profile, then this guide isn’t for you. You may find useful information in it, but please note that the rest of the guide will not explain which bits would be different for larger companies, or public authorities, or those processing childrens’ personal information, etc. The rest of the guide is written with the assumption that you fit the profile.

Also, to keep the guide simple, I am focusing on the changes occurring May 25th, 2018, and assuming you were already compliant with previous EU privacy regulations, for example showing an explicit notice for users to [accept cookies](https://www.cookielaw.org/the-cookie-law/) if you use them for anything other than what is necessary for your service.

# Definitions

Before we get started, it will help to get some definitions out of the way:

  * **Subject:** A natural person, i.e. an individual.
  * **Data Controller:** The entity that collects and processes data on subjects. This will normally be the company that the user feels like they are submitting their personal data to. For example, if you run a B2C SaaS business, you are almost certainly a Data Controller.
  * **Data Processor:** An entity that processes data on behalf of a data controller. A lot of B2B SaaS companies will be Data Processors, for example anyone who runs an API-based service that accepts personal data. A lot of companies, especially B2B companies, will also find that they are both a Data Controller (to their own registered users), as well as a Data Processor (for the data entered by their users). An example of a company that is definitely both a Data Controller as well as a Data Processor would be a cloud-hosted CRM system; it is a Data Controller for its own registered users’ data, and a Data Processor for all the personal information on their prospects and customers.
  * **Personal data**: Any data that relates to a Subject (i.e. an individual), that either is identified or can be identified based on that or other data. Essentially, any data you store that relates to a natural person, whether or not you know their identity or just know enough about them that they might be identified.

# Step by step

## 1. Catalog all personal data

Your first step should be to make a catalog of all the different types of personal data you store and process in your business. To jog your memory, here’s a list of different types of such data you might be collecting and processing:

  * Data on your employees (for payroll and other purposes)
  * User account data, settings, etc.
  * Usage records in your database
  * Diagnostic logs and analytics (may e.g. contain IP addresses)
  * Any data files, photos, etc. that you store on behalf of subjects
  * Details related to subscriptions, payments, etc.
  * Lead lists that you have created or purchased (e.g., lists of email addresses, names, titles) for direct sales or marketing purposes, without explicit consent from the subjects
  * Prospect and customer details in your CRM
  * Mailing lists that subjects have opted into

For each category of personal data you collect, add a row to a spreadsheet or database where you can record your answers to the following questions:

  1. What is our purpose for collecting/processing this data? If there are multiple different types of processing for one set of data, make separate entries in your spreadsheet for each different type.
  2. Where do we store the data? E.g., in a database, files (note the location), or in a 3rd party system such as Google Analytics or MailChimp?
  3. What types of personal data is collected/stored for this processing? Name? Email? Photographs of the person? Write down all the different aspects of data related to an individual that you collect and store for this particular processing.
  4. Where does the information come from? From the subjects themselves, or from 3rd party datasets, from your own online research, or it is entered or otherwise input by your users (e.g. if you run a CRM)?
  5. Do you use a Data Processor to store/process this data? For example, if it’s a flat file stored in Google Drive, then Google is your Data Processor here. List all data processors for each category of personal data.
  6. How long do you store the data? Could you store it for a shorter duration?
  7. What is your policy related to this data?
  8. What is your [justification](https://gdpr-info.eu/art-6-gdpr/) to process the data? The most common ones are that consent was given, or it is required to fulfill a contract with the Subject, or you have a legitimate interest to process the data that is not overridden by the interests or fundamental rights and freedoms of the Subject (yes, this last bit is vague – we’ll discuss this a bit more in step 7). If consent was given for the processing, what form of consent is it, and is it explicit enough? We’ll talk more about getting consent in step 3.

Again, make sure each entry in your database or spreadsheet has only a single purpose for the processing. If you use the same set of data for different types of processing, duplicate the entry and just change the purpose bit on each entry. For example, if you use your registered users’ email address both as a key to their user accounts, and also for some marketing purposes (e.g., finding and following them on LinkedIn), then those are two separate purposes.

You may find that you don’t have great answers for items 6 through 8 to begin with. Don’t worry, we’ll get to those columns in later steps of the guide.

## 2. Minimize risk and reduce work

From the document you generated in step 1, your next step is now to use those details to reduce the amount of work you need to do, and to minimize risk for you and for your users.

The more you reduce your work and minimize your risk in this step, the less work you will have in subsequent steps.

**First,** for each item, see if you can collect less information, store that information for less time, or make the information collected not personally identifiable by partially or completely scrubbing it.

One important way to do this is for example, if you collect IP addresses (and almost all HTTP server logs do!), why not strip out the last 8 bits so that they are no longer potentially traceable back to an individual? Even without those last 8 bits, they’ll still be specific enough to understand roughly where in the world they are (based on IP geolocation) and perform various other types of analytics on.

**Second,** review all the different Data Processors that you use as subprocessors. Are they all GDPR compliant, or planning to be? Do they all offer a Data Processing Agreement (DPA)? It’s easy to figure this out by doing a search like “[provider name] GDPR” and “[provider name] DPA”. If there are any Data Processors that you feel like you can stop using, at least temporarily, then consider doing so. If there are any that you critically rely on, that don’t yet have a clear statement on GDPR compliance and availability of a DPA, it’s time to start a serious discussion with them or create a fallback plan to mitigate your risk.

**Third,** note that [one of the requirements](https://gdpr-info.eu/art-32-gdpr/) of the GDPR is for data controllers and processors to “implement appropriate technical and organisational measures to ensure a level of security appropriate to the risk.” Since you fit the profile for this guide, there may not be that much you need to do beyond what you already do, but I would recommend you schedule a risk assessment meeting with your technical team, to generate a list of what the highest technical and process risks might be to the security of personal data, and suggest mitigating steps for each of these. Write down meeting minutes from this risk assessment. You don’t have to take every potential mitigating step right away, but you might want to start on one or two of the lowest-hanging fruit. For example, transmit personal data only over encrypted communication channels, or minimize the number of staff that have full access to all production data.

## 3. Get consent

Going back to the list of data generated in step 1, review the justification for processing each category of personal data.

For any category where the justification is consent, make sure you are getting that consent in the right way, and plan modifications to your product or service as quickly as possible to fix any areas where you’re not quite doing it in a compliant way.

The GDPR requires that you use explicit opt-ins or forced choices, so no more pre-checked opt-in buttons or unchecked opt-out buttons. This is the most common change a lot of websites and products need to make.

The GDPR also requires unbundling of choices, so no more “enter your email to create an account in our product and join our mailing list.” Those need to be two separate choices.

However, it does allow for unambiguous consent rather than explicit opt-in when you are not collecting sensitive data, and this is great to use where you can, as it’s a better user experience as well as creating less friction than explicit opt-in or forced choice. This is best explained by way of example:

Let’s say your account signup is based on an email address, and above the email field you have text saying something like “We will use your email to send you transactional emails”. If the user enters their email and submits your form after seeing this notice, then they are giving unambiguous consent to this use of their address (i.e., you can now send them transactional emails).

In the example above, due to the requirement of unbundling, a good next step might be to have a forced “yes/no” choice of whether to also sign up for your newsletter.

## 4. Enable subjects to exercise their rights

Under the GDPR, data subjects have a number of rights that you as a Data Controller must allow them to exercise, and that you as a Data Processor must enable a data controller to implement.

Subject rights according to the GDPR include full access to their data in a computer-readable format, the right to correct their data, to object to any part of your data processing activities, and the right to be forgotten (right to erasure). You need to be able to implement all of these, not just with data that you directly store, but with data stored by any subprocessors you use.

Implementing all of these rights in a fully-automated manner can be a daunting task, especially for small companies. Fortunately, the GDPR does not require that exercising these rights be fully automated or instant; it just states that we should do things “without undue delay”.

My recommendation is to initially implement each of the rights only through a manual process: Create an internally documented checklist and train your customer support staff on what to do for each type of request from subjects, and to ask subjects to submit requests to exercise their rights through your support ticketing system. Later, when you understand more about how frequent different types of requests are, you can see what the return on investment for fully or partially automating each task will be, and decide based on that.

Here are some recommendations on how to some of the [different rights](https://gdpr-info.eu/chapter-3/):

  1. [Right of access](https://gdpr-info.eu/art-15-gdpr/): If they ask, you need to tell them whether and how you are processing their data. You can also mostly handle this right by having a public statement about your data protection policies (see next step).
  2. [Right to data portability](https://gdpr-info.eu/art-20-gdpr/): You can handle these two rights more or less the same. Document a process whereby you gather all data on the person into a single folder, ZIP it up, and send to them. Use your list from step 1 to achieve this, and don’t forget data stored by various subprocessors. The GDPR requires that the data be machine readable but does not specify the exact format. As standards emerge around this, look to them and try to do what others are doing, but for now, who’s to say what the right format is?
  3. [Right to rectification](https://gdpr-info.eu/art-16-gdpr/): This is essentially a right to make corrections. Just accept the corrected data and update your systems.
  4. [Right to erasure](https://gdpr-info.eu/art-17-gdpr/): Part of this right requires that you “forget” subjects if you no longer need to process their data. The other part is, they can withdraw their consent or object to your processing of their data (see below) at which point you need to erase them from your data. If you only process data based on consent, then all you need to do is remove their records. If you also process personal data not submitted by the subject in question, see the next right (the right to object).
  5. [Right to object](https://gdpr-info.eu/art-21-gdpr/): If you fit the profile for this article, then this is bound to have to do with direct marketing, e.g. cold outreach or some other form of processing where they did not consent, but rather you are processing their data because of a business need you have. If they object, you stop processing their data (i.e. you unsubscribe them / add them to an exclusion list) and make sure you do not process their data again without consent. It’s unclear to me whether you are allowed to keep their email address or some other identifier on file as part of an exclusion list, but I would think that as a first step towards an implementation this should be OK; a more advanced implementation would be to keep a list of one-way cryptographic hashes of email addresses or other identifiers that have opted out.

## 5. Document your policies

Internal policy documentation is important when it comes to treating data subjects fairly, and doubly important when it comes to avoiding fines. Your internal documented policies and training of staff in dealing with the GDPR are likely to go a long way to convincing regulators you should not be fined, even if something happens to go wrong or not be 100% compliant.

Create a master document for all data protection policies and documentation internally, and link everything there.

Make sure you have a documented security policy and a documented policy on access to personal data and handling of personal data by your staff. Among other things, this policy should minimize the number of staff who have full access to everything, and should attempt to establish appropriate controls for what can be done with data and who needs to authorize which type of use of data. Refer back to your list from step 1 to create this policy.

I also recommend creating an external web page, promoted similarly as your Terms of Service and your Privacy Policy (and probably also linked to from your Privacy Policy). Call it Data Protection Statement and document as much as you can for external users – give them an insight on your policies, which subprocessors you use, how your subprocessors are compliant, and give them instructions on how to exercise their rights (see step 4). Refer to the [right of access](https://gdpr-info.eu/art-15-gdpr/) for a list of information you need to disclose and should be part of your Data Protection Statement.

## 6. Sign DPAs and consider territories

The most onerous requirement of the GDPR, for small businesses, is the need to sign a Data Processing Agreement (DPA) with any sub-processor you use, and if you are a Data Processor, to offer your customers to sign such an agreement with you.

Many well-established platforms and SaaS that you may be using will already have these well before the GDPR deadline of May 25th, 2018. For example, Amazon Web Services and MailChimp had these ready well in advance. Other providers, you may need to contact their support team and indicate to them that you will be unable to use their services after the deadline unless they sign such an agreement with you.

If you are a Data Processor, you will need to have a lawyer draft your DPA. You can look to other providers’ DPAs for inspriation.

Another potentially onerous obligation for small companies is that if you are outside the European Union (and a [handful of other countries](https://ec.europa.eu/info/law/law-topic/data-protection/data-transfers-outside-eu/adequacy-protection-personal-data-non-eu-countries_en)), you need to get explicit consent from the user, consenting to have their data processed outside of the EU (remember, explicit consent means an explicit opt-in or forced yes/no choice indicating that they agree to this; in this case an unambiguous consent is not sufficient).

There are two ways around the above, but only the former is likely to be feasible by a small company such as yours:

  1. For US businesses, you can certify to the [U.S. Privacy Shield](https://ec.europa.eu/info/law/law-topic/data-protection/data-transfers-outside-eu/eu-us-privacy-shield_en) framework.
  2. For businesses in other jurisdictions, you _could_ apply to the EU privacy regulators to have them certify so-called [Binding Corporate Rules](https://gdpr-info.eu/art-47-gdpr/). You’ll probably prefer to just ask for explicit consent from the user.

## 7. Be transparent

A fundamental principle of the GDPR, and one of the rights of data subjects, is [transparency](https://gdpr-info.eu/art-12-gdpr/). This means, it needs to be clear and easily discoverable how and why you are processing the subject’s data.

You already set up your public Data Protection Statement, which is one of the main ways to fulfill your obligation to be transparent.

Another very important obligation is to report security incidents.

If there is ever a security incident where a personal data breach is possible, i.e. where it looks like unauthorized parties may have gained access to any personal data, you have an obligation to:

  1. Notify the data subject without undue delay. You probably already know their email or phone number, so use that. If you don’t, you need to set up some kind of opt-in mailing list or similar that users can subscribe to for such notifications, or you will need to communicate publicly about data breaches. There are [certain situations](https://gdpr-info.eu/art-34-gdpr/) where you can skip notifying individual subjects.
  2. If you are a Data Processor, you must notify affected Data Controllers without undue delay.
  3. Unless the data breach is “unlikely to result in a risk to the rights and freedoms of natural persons”, you must notify the [supervisory authorities](https://broadcasting.house/eu-gpdr-lead-supervisory-authorities/) of the EU/EEA member state(s) affected, i.e. where the data subjects reside.

## 8. Consider your cold outreach practices

Recall that one of the rights of data subjects is [transparency](https://gdpr-info.eu/art-12-gdpr/). You need to let them know how and why you are processing their data. For consent-based or contract-based processing, they should already know this from the time they consented. They should know they are users of yours, and they know where to find and read your Data Protection Statement to see how to reach you, how to withdraw their consent if they wish, etc. You still need to have the typical unsubscribe links in emails you send to a mailing list, and so forth, but mostly you can do things the same as you have before, after finishing all the steps above

For direct marketing, e.g. cold email campaigns, the waters are murkier. Some have said that cold email is dead with the advent of GDPR, but I don’t think this is actually true. Important figures such as highly placed folks at Amazon have claimed that you can still cold email under the GDPR.

My reading of the regulation is that you need to still provide transparency, and let the user know how they can object to processing. I would suggest you include not only a link to unsubscribe (already required by several regulations in many countries around the world), but also a one-liner of where you got their data and why you are emailing them (i.e., what your legitimate business interest in contacting them is), and a link to your Data Protection Statement so that they have clarity on how to exercise their rights. I would also suggest that you be even more careful than before in targeting very specific market segments, departments, titles, etc. so that it is easier to make the case should the regulators start talking about fining you, that you were strongly convinced that this particular piece of email would be of interest to the particular group of people you contacted.

An alternate approach that you may wish to try instead of contacting individuals, and is certainly lower risk now that the GDPR looms large, is to prefer sending to generic email addresses such as info@ and contactus@, asking for an introduction to the right person.

Finally, we may see a return to more cold calling rather than cold emailing. While you still have an obligation to be transparent and answer truthfully if they ask why you are calling them or how you found their name and phone number, I doubt that it will be a requirement any time soon to start every call with a two-minute disclosure of this information.

The GDPR is very open to interpretation and only time will tell how strictly it gets interpreted. As long as you make your best effort to be compliant and treat your data subjects fairly, process their data lawfully, and be transparent, I think you should be fine.

# What’s missing?

This guide has been targeted at companies that fit the profile, i.e., many small businesses and startups. For companies processing sensitive data, there are lots of additional requirements including stronger consent and more strict security requirements. For companies with more than 250 employees, there are stringent record keeping requirements, essentially you need an audit log of all activities. Fortunately, as small companies, we don’t need to worry about that until we grow – and once you get big enough to have to worry about that, then you’ll be big enough to hire lawyers and other experts to help make sure you do the right things to get compliant.

# Useful resources

The two resources that helped me the most while working through GDPR compliance were:

  1. This neat [indexed version](https://gdpr-info.eu/) of the full text of the GDPR, with links to relevant additional material for each article. This is what I’ve linked to in several places in the guide.
  2. The UK Information Commisioner’s Office (ICO’s) [guide](https://ico.org.uk/for-organisations/guide-to-the-general-data-protection-regulation-gdpr/), which is the most concise and easy to understand full commentary on the GDPR. I especially recommend their checklist for [data controllers](https://ico.org.uk/for-organisations/resources-and-support/data-protection-self-assessment/controllers-checklist/) and [data processors](https://ico.org.uk/for-organisations/resources-and-support/data-protection-self-assessment/processors-checklist/).

_This article was originally published on the [StartupResources.io](http://startupresources.io/) [blog](http://startupresources.io/blog/). If you need more help getting your startup off the ground, I suggest you join the [StartupResources.io](http://startupresources.io/) mailing list where you’ll get a weekly newsletter with tools and articles to help you get your startup going._