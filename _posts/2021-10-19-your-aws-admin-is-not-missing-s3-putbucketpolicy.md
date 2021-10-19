---
layout: post
title: No, your AWS administrator account isn't missing s3:PutBucketPolicy
description: If you run into this confounding AWS error message, maybe this will help
date: 2021-10-19 15:48:00 +0000
author: joisig
comments: true
categories:
  - aws
  - coding
---

I ran into this absolutely confounding error today and figured I would document it here in case somebody else runs into it and can't find the solution.

The error was: "You don't have permissions to edit. After you or your AWS administrator have updated your permissions to allow the s3:PutBucketPolicy action, choose Save changes."

That didn't make sense - I was logged in with administrative privileges.

We recently started using AWS Organizations to federate access to different accounts with AWS, and to use AWS SSO for log-in across all those accounts, so I spent a bunch of time thinking I needed to add privileges to the IAM user I was using. Nope.

I ran down the checklist [here](https://aws.amazon.com/premiumsupport/knowledge-center/s3-access-denied-bucket-policy/). Nope.

I finally tried logging in as the root user on the account. SAME ERROR!

The reason for this error turned out to be the default setting when creating an S3 bucket, "Block all public access". Removing that and then setting the policy, I was able to proceed without any error.
