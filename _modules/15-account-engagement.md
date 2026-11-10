---
number: 15
part: 4
title: "Account Engagement (Pardot) — The Marketing Engine"
short_title: "Account Engagement"
description: "What Account Engagement does, how it syncs with Salesforce, and which of its fields you can trust."
key_points:
  - "Pardot, Account Engagement, and MCAE are one product: it sends marketing email, tracks response, scores people, and runs forms."
  - "Data flows both ways. The `pi__` fields come from Account Engagement and are read-only."
  - "**Last Activity** ignores email opens, and **Lifecycle Stage** is a score bucket, not a sales judgment."
  - "Opt-outs and bounces decide who can be emailed. Ask marketing for list emails about two weeks ahead."
redirect_from:
  - /modules/10-the-robot-behind-the-curtain/
---

Pardot, Account Engagement, and MCAE (Marketing Cloud Account Engagement) are three names for one product. Salesforce renamed it and people kept the old name, so you will hear all three at OpenStax. You will probably never log in, but it writes to the Contact and Lead records you read every day, so it helps to know what it does.

## What it does

- **Sends marketing email at scale.** It builds the audience, merges in details like first name, delivers the message, and records opens, clicks, bounces, and unsubscribes.
- **Runs forms on openstax.org.** Interest forms, adoption and renewal forms, and resource requests are Account Engagement forms. A completed form updates the person in Salesforce and adds them to a campaign. Adoption forms create Adoptions; see [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).
- **Scores people.** Behavior earns points (clicks, form fills, visits), and a letter grade reflects how well a person fits our audience.
- **Scores by category.** Separate scores for general engagement, **Adoption Engagement**, **Assignable Engagement**, and **Algebra Interest** show *what* someone engages with, not only how much. Scores never create Opportunities.

## The two-way sync

Salesforce and Account Engagement trade information constantly. Salesforce sends email addresses, opt-outs, adoption status, school type, and subject interest. Account Engagement sends back score, grade, activity, and bounce status.

The returning values live in fields that begin with `pi__`. They are read-only: edit one and the next sync overwrites it. Syncs happen shortly after a change, not instantly, and the most recent edit wins.

![Two boxes, Salesforce and Account Engagement, with arrows showing field values, opt-outs and consent flowing one way and scores, activity and bounce status flowing back.]({{ '/assets/images/pardot-data-flow.svg' | relative_url }})

What you change in Salesforce, such as a corrected email address or subject interest, changes who gets which message. Clean fields mean fewer "why did I get this?" replies.

## Reading the fields it writes

- **Lifecycle Stage** is a bucket built from the overall score: New, Nurturing (most people), MQL (marketing-qualified lead), or SQL (sales-qualified lead). It is **not** a sales judgment. Someone can be an SQL without ever having talked to us.
- **Last Activity** moves on clicks, form submissions, and page visits, but **not on email opens**. Don't read it as "last engaged." For that, use Last Engagement Date and Instructor Engagement Tier; see [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).
- **Score and grade** show behavior and fit. A high score on its own does not make someone a good prospect.

## Bounces, opt-outs, and who can be emailed

A **hard bounce** means the address is dead. Account Engagement flags it, **Marketing Engagement Status** shows Bounced - Unmailable, and the **Unable to Email** checkbox is ticked (it is also ticked for opt-outs and for people who never gave marketing consent). A substantial share of the addresses in our system have bounced over the years, so a bounce flag is common.

Account Engagement will not email anyone with **Email Opt Out** (Do Not Email) set. Record a "please stop emailing me" request on the person's Contact, and on their Lead if one is open. Consent is stored once per person, but the Lead side is older, so check both. Signups who leave the marketing box unticked are treated as not consenting. For the full rules, see [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

<div class="callout callout-orange" markdown="1">
**Hands off:** don't edit `pi__` fields, and don't clear a bounce or opt-out to "give someone another chance." Those flags protect our ability to reach everyone else.
</div>

## Asking marketing for an email

Need a list email to go out to a group of instructors? Ask marketing and allow up to two weeks. They build the list from Salesforce fields, check consent, and attach the send to the right Tier 4 campaign ([Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }})). A sales or outreach email you send yourself from Salesforce must include a way to unsubscribe.

<div class="callout callout-blue" markdown="1">
**Good to know:** marketing email history lives in Account Engagement, not as Tasks on the Contact. Campaign History is the quickest way to see what someone received.
</div>
