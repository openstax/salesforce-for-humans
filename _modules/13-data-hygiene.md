---
number: 13
title: "Data Hygiene Is a Civic Duty"
short_title: "Data Hygiene"
description: "Duplicates, missing fields, stale data, and why keeping records clean is everyone's responsibility."
---

Duplicate records, missing fields, outdated information, contacts still listed at institutions they left years ago. Bad data is a slow poison. It doesn't announce itself with alarms or error messages. It just quietly degrades every report, every campaign, every dashboard, every support call, and every decision made from them.

### What Bad Data Actually Costs

Let's make this concrete with OpenStax examples:

**Duplicate Contacts** mean that one instructor's adoption history, support cases, and engagement data are split across two records. Neither record tells the full story. A support agent sees half the picture. A marketing campaign reaches the person twice (or misses them entirely because the filter matched one record and not the other). The adoption count for their institution is potentially wrong because it's counting from the wrong Contact.

**Missing fields** mean missed opportunities. If an Account is missing its LMS field, a sales rep evaluating Assignable prospects can't filter for schools using Canvas (where integration is smoothest). If a Contact is missing their subject interest, marketing can't include them in a targeted subject-specific campaign.

**Stale data** means false confidence. If a Contact's email address bounced six months ago but nobody updated the record, marketing continues targeting them (hurting deliverability scores), sales continues including them in outreach plans, and the "marketable audience" count is inflated.

**Misclassified records** mean bad analytics. If a Case is tagged with the wrong Product or Issue, the support trend reports show the wrong patterns, and the product team gets misleading signals about where users are struggling.

![What bad data costs: a duplicate Contact splits adoption history, support context, and engagement data across two records. Neither tells the full story. Support sees half the picture, marketing double-sends or misses entirely, and adoption counts are wrong.]({{ '/assets/images/bad-data-ripple.svg' | relative_url }})

### What You Can Do

Data quality is a shared responsibility. You don't need special permissions to make a difference:

- **Check before you create.** Before making a new Contact or Account, search for it first. Duplicates are far easier to prevent than to clean up.
- **Fill in what you know.** If you're on a call and learn that a school uses Canvas, update the LMS field on the Account. If an instructor mentions they're teaching Chemistry this fall, update their Subject Interest on the Contact. These small additions compound.
- **Flag what's wrong.** If you notice a duplicate, an outdated email, or data that doesn't look right, flag it. Tell your admin. Log a case with the data team. Don't just work around it.
- **Use the duplicate detection tools.** Salesforce flags potential duplicates when you create records. Don't dismiss these warnings without checking — they're often right.

### What NOT to Edit

Some records are maintained by automated pipelines and should generally be left alone:

- **Adoption records** are created and updated by automated processes that track re-confirmation forms, behavioral signals, and third-party data. If an Adoption looks wrong, flag it for the data team rather than editing it directly.
- **Assignable records** (access codes, transactions, student-level data) flow in from the platform's payment and provisioning systems. Outside of interest-related fields, these shouldn't be manually modified.
- **Book Opportunity stages** are managed by the same automated pipelines that process adoption data. You don't need to move a Book Opp from "Unconfirmed" to "Active" yourself.
- **Pardot/Account Engagement fields** (the `pi__` fields on Contacts) are synced from Account Engagement. Editing them in Salesforce won't stick — the next sync overwrites your change.

If you learn about an adoption or confirmed usage through a conversation or campus visit, use the **screen flow on the Contact record** to capture what you learned. The flow routes it into the right automated pipeline so the Opportunity, Adoption, and related records update correctly.

### The Multiplier Effect

Here's the thing about data quality: it's multiplicative. One clean record benefits every team that touches it. One bad record costs every team that touches it. When hundreds of people each make small improvements (an updated email here, a filled-in field there, a merged duplicate over there), the cumulative effect on organizational data quality is enormous.

OpenStax's data powers mission impact reporting to funders, personalized web experiences for educators, targeted marketing campaigns, efficient support operations, and strategic planning by leadership. All of it runs on the same data. Clean data makes all of it work better.

Data hygiene isn't someone else's job. It's a shared responsibility, and every contribution matters.

