---
number: 11
part: 3
title: "Reading a Contact at a Glance"
short_title: "Reading a Contact"
description: "A walk-through of one instructor's Contact: which fields to read, what they mean, and what to do next."
key_points:
  - "Adoption Status, Instructor Engagement Tier, and Marketing Engagement Status answer three different questions."
  - "Pardot's Last Activity doesn't move on email opens. Use Last Engagement Date and the Engagement Tier."
  - "Engagement is not permission. An opted-out Champion is still a Champion, and still must not be emailed."
---

A Contact page can look like a wall of fields. A handful of them, mostly formulas that update themselves, tell you who this person is to OpenStax in about ten seconds. This module reads one Contact top to bottom so you can do the same.

## Meet Dr. Maya Rivera

Dr. Rivera (she) teaches Anatomy & Physiology at Cedar Bluff Community College and has used *Anatomy and Physiology 2e* for years. Open her Contact and look at the highlights panel and the fields beneath it.

![A mock Contact highlights panel for Dr. Maya Rivera with labelled fields: Adoption Status Current Adopter, Instructor Engagement Tier 1 Champion, Last Engagement Date, Marketing Engagement Status, FV Status confirmed faculty, and a note beside each saying what it answers. Example data.]({{ '/assets/images/11-contact-at-a-glance.svg' | relative_url }})

## The fields that matter

You don't edit any of these. They're calculated from adoptions, support Cases, campaigns, and Account Engagement (Pardot).

| Field | What it answers | Values |
|---|---|---|
| **Adoption Status** | Are they using a book now? | Current Adopter, Current Adopter - Assumed, Past Adopter, Past Adopter - Assumed, Not Adopter. Current flips to Past each July until they re-confirm |
| **Instructor Engagement Tier** | How engaged are they overall? | 1 Champion, 2 Active Adopter, 3 New, 4 Engaged Prospect, 5 Lapsing Adopter, 6 Dormant, 7 Inactive, 8 No Signal |
| **Last Engagement Date** and **Days Since Last Engagement** | When did we last see any sign of them? | Counts marketing activity, a support Case, a confirmed adoption, a campaign response, an email open |
| **Engagement Recency** | A quick bucket | From "1 - Active (30d)" through Unreachable |
| **Marketing Engagement Status** | Can we email them, and is it worth it? | Bounced - Unmailable, Opted Out, Engaged - Recent Response (90d), Engaged - Responded This Year, Dormant - Past Responder, Scored - No Campaign Response, On List - Never Engaged |
| **Last Email Open** | When did they last open marketing email? | Includes automatic opens (Apple Mail privacy, security scanners). A click is stronger evidence |
| **Adoption Health** | Adoption status and recency combined | Segments |
| **Lifecycle Stage** | Which Pardot score bucket? | New, Nurturing (most people), MQL, SQL. A score bucket, not a sales judgment |
| **Pardot score / grade** | Behavior points / fit letter grade | Written by Account Engagement |
| **Account Engagement Hard Bounced** | Is the email address dead? | Checkbox |
| **FV Status** | Verified faculty? | See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}) |
| **Subject Interest** | What do they teach? | Multi-select |

The Champion tier means an adopter for three or more years who has engaged in the last 180 days. Adopters stay "adopter" for 400 days after an OpenStax-confirmed adoption, so last year's adopters don't all look lapsed every fall.

Dr. Rivera reads: Current Adopter, tier 1 Champion, engaged recently, faculty confirmed. She is the person you thank, not the person you pitch.

<div class="callout callout-orange" markdown="1">
**Hands off:** Pardot's "Last Activity" does not move when someone opens an email, only on clicks, form submissions, and visits. Don't read it as "last engaged". Website login, website visit, and resource download date fields aren't filled by anything yet, so don't filter on them. Fields beginning `pi__` come from Account Engagement and get overwritten if you edit them.
</div>

## Engagement is not permission

These are different questions. The Engagement Tier says how active someone is. **Marketing Engagement Status** says whether we may and should email them. A Champion who has opted out is still a Champion, and still must not get marketing email.

Account Engagement won't email anyone with **Email Opt Out** or **Do Not Email** set. When someone asks us to stop, record it on their Contact, and on their Lead too if one is open. People who leave the marketing-consent box unticked at signup are treated as not consenting. Rejected faculty are opted out at rejection.

Consent is stored once per person, on a shared **Individual** record that both their Lead and Contact point to. Lead handling is older than Contact handling, so when you process an opt-out, check both the Lead and the Contact (Merged Leads included). Email you send from Salesforce still has to give people a way to unsubscribe.

## What to do with what you read

| You see | A sensible next step |
|---|---|
| Champion, Current Adopter | Say thanks, ask for a story, check whether they'd mentor a colleague |
| Lapsing Adopter (tier 5) | They used a book recently and have gone quiet. Check for a recent Case, then a personal note before the renewal email |
| Past Adopter, Engaged Prospect | Worth a conversation about this year's course |
| Hard Bounced, or Bounced - Unmailable | Don't keep emailing. Look for a current address on the school's site, or ask the school |
| Heard about an adoption on a call | Log it with Build Adoption ([Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }})) |

<div class="callout callout-green" markdown="1">
**Try it:** Open a Contact you know well and read Adoption Status, Engagement Tier, and Marketing Engagement Status in that order. Do the three tell one story? If they don't, that's usually informative, not broken.
</div>
