---
number: 10
title: "The Robot Behind the Curtain — Pardot, Account Engagement, and Marketing Automation"
short_title: "Pardot / Account Engagement"
description: "What Account Engagement does, how it reads and writes Salesforce data, and why it matters to you."
---

First things first: Pardot and Account Engagement are the same product. Salesforce rebranded it. The industry still uses both names interchangeably, and you'll hear both at OpenStax. Now that we've gotten that out of the way.

**Account Engagement** is the marketing automation engine that works alongside Salesforce. If Salesforce is the shared brain, Account Engagement is the nervous system that sends signals at scale. It's what makes it possible to send personalized emails to hundreds of thousands of educators, track every open and click, score prospects based on their behavior, and feed all of that intelligence back into Salesforce.

### What It Does (In Plain Terms)

**Email sends at scale.** When OpenStax sends a back-to-school email to every higher-ed biology instructor in the system, Account Engagement handles the delivery. It manages the send lists, personalizes the content (merging in first names, institution details, etc.), sends the emails, tracks delivery, and records every open, click, and unsubscribe.

**Lead scoring.** Account Engagement assigns a numerical score to every prospect based on their behavior: opening emails, clicking links, visiting web pages, submitting forms, attending webinars. A faculty member who registered for two webinars and downloaded three resource guides has a higher score than someone who hasn't opened an email in six months. These scores help prioritize who gets personal outreach.

**Scoring categories.** Beyond a single overall score, OpenStax uses category-level scoring to distinguish between different *types* of engagement. Someone might be highly engaged with adoption-related content but show no interest in the paid Assignable platform, or vice versa. Category scores let marketing and sales understand not just *how much* someone is engaging, but *what they're engaging with*.

**Forms and landing pages.** Account Engagement powers the forms on openstax.org that capture interest, adoption confirmations, and resource requests. When someone fills out a form, the data flows back into Salesforce as a Lead or Contact update, a Campaign Member record, and potentially a new Opportunity.

### Why It Matters To You

Even if you never log into Account Engagement, it touches your work:

- **The `pi__` fields on Contact and Lead records** (score, grade, last activity, hard bounced) come from Account Engagement. When you see a Pardot score of 85 on a Contact, that's Account Engagement telling you this person is actively engaged with OpenStax content.
- **When you update an email address or opt-out status on a Contact**, that change syncs to Account Engagement and immediately affects what marketing can send to that person.
- **Hard bounce data flows both directions.** If an email bounces in Account Engagement, the Contact's record in Salesforce reflects it. If roughly a quarter of your Contacts show a hard bounce, that's Account Engagement telling you the email address is dead. Continuing to send to bounced addresses hurts deliverability for everyone.
- **Marketing campaign lists are built from Salesforce data.** The Contacts and Leads that Account Engagement sends emails to are selected based on their Salesforce field values: adoption status, institution type, subject interest, engagement recency. The accuracy of those fields directly controls who receives what messages.

![The two-way data flow: Salesforce sends field values (email, opt-out status, adoption, institution type) to Account Engagement, which sends back scores, engagement data, and bounce status. The pi__ fields on your Contact records come from Account Engagement. What you update in Salesforce controls what marketing sends.]({{ '/assets/images/pardot-data-flow.svg' | relative_url }})

Understanding that this engine exists, and that it's constantly reading from and writing to the same Salesforce records you touch, makes you a more effective participant in the data ecosystem. You don't need to operate Account Engagement. You just need to know it's there, it's always watching, and the data flows in both directions.

