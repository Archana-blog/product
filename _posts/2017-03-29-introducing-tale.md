---
layout: post
title:  "What went wrong? - A Product Manager's guide to root cause analysis and crisis management"
author: "Archana Kumari"
comments: true
tags: Analysis
excerpt_separator: <!--more-->
sticky: true
hidden: true
---

As a product manager/owner of a product, a service or a feature, when do you get to know something went wrong? <!--more-->

Is it when a mail is sent to you from your CEO asking why the numbers dropped yesterday? Or are you a prompt product manager who looks at your numbers first thing in the morning. Chances are, you could be in either of the two categories but you must always know the why.

### Why the numbers were low yesterday?
There are several ways to start the root cause analysis but it always ends with an exhaustive search of the culprit. Here is my take on how to ensure timely and more importantly precisely knowing what went wrong.

First step let's look at the mess and confirm the issue -

What numbers are we talking about? Which KPI was hit (acquisition / engagement / satisfaction)?
What time frame we are looking at. Is it a day's data or weekly or monthly?
What are you comparing the current numbers with? Make sure the dropped KPI is compared against a correct time frame. You can not be comparing weekday's data with a weekend.
Were users facing some serious issues such as login/downtime/non-responsive pages?
Once that's done, let's look into the issue -

Taking inspiration from the Cynefin Framework, almost 80% of the issues come under "Simple" contexts. When I say simple, I don't mean easy to diagnose and fix but the "The Known" issues.

![alt text](assets/Cynefin.jpeg "Cynefin Framework")

“Cynefin, pronounced ku-nev-in, is a Welsh word that signifies the multiple factors in our environment and our experience that influence us in ways we can never understand.” - Dave Snowden

## Simple Context (Knowns) -

Your end users are always the first ones to report either through app store, customer queries or service tickets. Quickly check if something was broken, understand from user queries and reviews. If the reviews / tickets did say something was broken, speak with engineering/support team.
Now, let's check if the change was expected. Maybe seasonality effect is in the picture. Compare the data with same time last week/month/year.
If the issue is because of either of above, you have the Sense –> Categorise –> Respond path to take. Quickly sense and assess the situation, categorise the issue type and respond to the issue accordingly.
If the issue is not sorted out from the above two reasons, then it is not simple anymore. We will go to next domain.
Complicated Context (Known Unknowns) -

In this knowable domain, a good product manager would need to deep dive in the issue. You would have to take the Sense –> Analyse –> Respond route. The approach it to sense and assess the situation. Analyse the issue with the help of tools and experts. Lastly, respond appropriately.

Sit with your engineering partners and understand what has changed. If any releases were live recently.
Check with other PM teams. Maybe the another team is running an A/B test.
Usually there are great monitoring tools such as Icinga, Crashlytics etc that helps you understand what went wrong.
Chances are you will be able to figure out if any releases or A/B tests might have impacted the product. An example could be, a new feature was released but it might not be correctly tested for one particular type of device/OS. For complex context, usually multiple correct solutions exist, you can choose based on your product.

## Complex Context (Unknown Unknowns) -

If you were not able to identify the issue in any of the above approaches, you have entered the Complex Zone. You would have to take the Probe –> Sense –> Respond route. You were not able to identify any potential cause and effect relationship. So instead of enforcing an action plan, be a little patient and try to understand issue. Sometimes, you can also experience changing outcomes as well. So sit with your team and do some out of box thinking.

This context is often unpredictable, now you would have to look deeply both inside and outside. Maybe competitors are doing something that is taking the attention away from your product. Also, check with Public Relations and Marketing Team if we have made any announcements that might have impacted the users.
Check your channels, time zones, demographics. Also, check if any specific user segment was impacted.
Now is the time you enter into funnel analysis. Based on your product type define your funnels. Which step in your product funnel is leaking and causing the drop. Here are few examples of funnel -

### Payment Funnels

Payment Button → Enter details → Success page

### Onboarding Funnels

Home → Social Login Option/Login Form → Submit

### Subscription Funnels

Homepage → Pricing Page → Select and Proceed / Summary Page → Purchase

### Growth Funnels

Homepage → Free Trial Sign-up → Social Login Option/Login Form → Submit

### Shopping Funnel

Home -> Category Page -> Product Details -> Add to Cart -> Purchase

If you are still not able to figure out the exact issue, you are entering the chaotic and disorder zones. These zones are unclear and you may not have enough information to answer the questions.

## Chaotic and Disorder Contexts (Unknowables) -

Now this is a very risky and incoherent zone, most of the time you would have to take a call and roll back the changes. Based on the damage done, you might have to apologise and provide incentives to your loyal users. This could have happened because of a bug or a malicious cyber attack. There are no constraints in this zone.

The best way to tackle these kind of issues is act → sense → respond. Act decisively and do damage control. Understand clearly which part of the product has the issue. Lastly, try to bring the issue to complex/complicated contexts by gathering more information.

## Final Thoughts

There is no one correct way to diagnose an issue. With increased unpredictability, ever changing customer needs, emerging new technologies, unreliable market forces and various unknowns, every system is prone to failure.

It is always a good practice if you are looking at the data daily. You will be able to notice the gradual shifts, analyse trends and catch issues early on. Talk to your dev team and setup up automatic hourly/daily/weekly reports. You can also ensure tracking of server logs. Always be in touch with infra team to know any outages or downtimes beforehand. Lastly, depending upon the size of your organisation, you can add yourself in support DLs, you can always check if the volume has suddenly increased.

All we can do as a product manager is adapt quickly, find the issues, help the team recover swiftly.
