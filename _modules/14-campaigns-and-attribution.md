---
number: 14
part: 4
title: "Campaigns and Attribution"
short_title: "Campaigns & Attribution"
description: "What a campaign is, how the four tiers fit together, how people land on one, and why attribution is still a work in progress."
key_points:
  - "A **Campaign** is a goal and an audience. It is not a single email or a single asset."
  - "There are four tiers. Marketers work at Tier 3 and 4; Pardot forms, sends, and webinars attach to **Tier 4**."
  - "People join campaigns mostly by themselves, and their **Campaign Member status** is the evidence trail."
  - "Attribution uses Campaign Influence. It is useful for Assignable and still thin for book adoptions."
redirect_from:
  - /modules/09-campaigns-and-attribution/
---

A **Campaign** in Salesforce is a goal and an audience: who we are trying to reach, why, and through which channel. It is not one email or one webinar. If you work with educators in sales, support, or events, you will bump into campaigns when someone asks you to "make sure these contacts are on the campaign." This module explains what that request is about.

## The four tiers

OpenStax organizes campaigns in four tiers, from permanent to very specific. Think of a filing system: the folders at the top never move, and the day-to-day work lands in the folders at the bottom.

| Tier | What it is | Example | Who creates it |
|---|---|---|---|
| **1. Program** | Permanent anchor, no year | Instructor Marketing, Mission Makers, Research, Tech Partners, Operational, Brand and Ancillary Communications | Data Intelligence team |
| **2. Initiative** | Evergreen anchor for an occasion or push | HE Semester Engagement, Giving Tuesday, K12 Algebra 1 | Data Intelligence team |
| **3. Season** | One run of an initiative | Spring 2026 HE Semester Engagement | Marketers |
| **4. Channel** | The execution: Digital, Webinar, In-Person or Event, Mail | Spring 2026 HE Semester Engagement — Webinar | Marketers |

Tier 4 is where the real work lives. Pardot forms, landing pages, emails, tracked links, members, and attribution all attach there, and results roll up the tree to the season, the initiative, and the program.

<div class="callout callout-orange" markdown="1">
**Stop and ask:** if you are about to attach a form, landing page, or tracked link to a Tier 1 or Tier 2 campaign, pause. It belongs on a Tier 4 campaign. Ask in #data-intel or the marketer who owns the effort.
</div>

![Four campaign tiers from Instructor Marketing down to a Spring 2026 webinar, with the Campaign Member status trail from Sent to Attended and a note on how Campaign Influence shares credit.]({{ '/assets/images/campaign-hierarchy.svg' | relative_url }})

## Naming and required fields

Names follow one pattern: `[Year if time-bound] [Program or Audience] — [Initiative or Channel]`. Spell everything out ("Back to School", not "B2S"), put the year first, and keep send dates out of the name. For example: `Spring 2026 HE Engagement — Email Series`.

Before a campaign can send or report cleanly, these fields need values: Record Type (the old "In-Person Campaign" type is now **Event Campaign**), Type, Audience Segment, Funnel Stage Target, Related Product, Status, Start Date, and Campaign Brief URL.

Renaming a campaign is safe, because Salesforce keeps the record behind the name. Check any report that filters on the old name text.

## Campaign Members: how people get on a campaign

A **Campaign Member** links one person (a Contact or a Lead) to one campaign, and its **status** tells you what they did. Common statuses include Sent, Opened, Clicked, Responded, Registered, Attended, Attended On-demand, Adoption Confirmed, Adopted, Donated, and Met at Booth.

Mostly, nobody adds people by hand. A Pardot form completion or email send adds the person automatically, and ON24 webinar registrations arrive in near real time. An individual email send is not a new campaign: recipients join the existing Tier 4 campaign.

Take a made-up example. Dr. Maya Rivera, an Anatomy & Physiology instructor at Cedar Bluff Community College, gets the **Spring 2026 HE Semester Engagement — Email Series** and clicks the webinar link. She registers for the **Spring 2026 HE Semester Engagement — Webinar** (status Registered), then joins the live session (status Attended). Her Contact page now shows that trail, and so does every report that counts it. Nobody typed any of it.

<div class="callout callout-blue" markdown="1">
**Good to know:** an active webinar campaign with an empty member list usually means a sync has stopped working. Tell #data-intel rather than adding people by hand.
</div>

## Attribution: what it can and can't say

OpenStax measures marketing credit with **Campaign Influence**. Instead of pinning an Opportunity to one campaign, it shares credit across the campaigns a person touched along the way. That is a fairer picture, and it works well for Assignable sales.

For book adoptions, attribution is thin today. Many instructors find OpenStax on their own, hear from a colleague, or fill out a form that no campaign claims. So treat influence numbers as one clue, never as proof that a campaign "caused" an adoption, and don't quote them as campaign revenue.

Member statuses are still the evidence trail. Someone missing from a campaign, or stuck on Sent after they plainly attended, leaves a gap that nobody can fill in later.

## UTM basics

A UTM is a small tag added to the end of a link so web analytics can tell where a visit came from. You need one in a single situation: a link from a site we do not own **to** openstax.org. That covers partner sites, ads, social posts, QR codes, and webinar descriptions.

- Never tag a link from openstax.org to openstax.org. It overwrites the visitor's original source.
- Pardot emails tag themselves.
- `utm_campaign` is the name of the owning Tier 4 campaign in kebab-case, for example `spring-2026-he-semester-engagement-webinar`.

<div class="callout callout-green" markdown="1">
**Try it:** open a Contact who attended a webinar and look at their **Campaign History**. Check that the statuses tell a sensible story. If something looks off, post it in #data-intel with the campaign name.
</div>
