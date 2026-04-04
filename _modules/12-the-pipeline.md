---
number: 12
title: "The Pipeline — Tracking What Matters from Interest to Outcome"
short_title: "The Pipeline"
description: "Opportunities, Adoptions, Record Types, and how OpenStax tracks everything from interest to impact."
---

In Salesforce, an **Opportunity** represents something moving toward a meaningful outcome. In a typical sales organization, that means a deal. At OpenStax, it's broader. Because the organization operates with both free products (textbooks) and paid products (Assignable), and because the mission involves both revenue and impact, the Opportunity object wears several hats.

### The Many Lives of an OpenStax Opportunity

OpenStax uses **Record Types** to split the Opportunity object into distinct business processes:

**Book Opportunities** track faculty textbook adoptions. These don't generate revenue (the textbooks are free), but they generate *mission impact*. A Book Opp moves through stages that reflect confidence level: Unconfirmed (we think they adopted), Assumed (indirect evidence suggests they're using it), Active (confirmed in use), and Lapsed (used previously but not currently confirmed). The majority of Opportunities in the system are Book Opps, because textbook adoption tracking is the foundation of OpenStax's mission.

**Assignable Opportunities** track the paid homework platform pipeline at two levels: Instructor-level opportunities follow a traditional sales pipeline (New → Contacted → Discovery → Demo → Implementation → Closed), while Student-level opportunities track individual purchases and access code redemptions.

**Donations** track contributions to the nonprofit. These link to donor Contacts and carry detailed financial data including payment method, recognition preferences, and fiscal year attribution.

### Adoptions: The Mission Impact Layer

Connected to each Book Opportunity is a chain of **Adoption** records — one for each school year the faculty member uses the textbook. Adoptions are where OpenStax measures its impact:

- **Students** — How many students used this textbook this year?
- **Savings** — How much did those students save compared to a traditional textbook?
- **Confirmation Type** — How do we know this adoption is real? (OpenStax Confirmed, Third Party Confirmed, or User Behavior Informed)

These numbers roll up into the mission impact figures that OpenStax reports publicly: millions of students reached, billions in savings. Those headline numbers aren't abstract. They're the sum of individual Adoption records, each one representing a faculty member at a specific institution in a specific school year with a specific student count.

![The pipeline: Book Opportunity stages progress from Unconfirmed through Active (or Lapsed). Each Opportunity has child Adoption records per school year tracking students and savings. Those individual records roll up into the headline mission impact numbers.]({{ '/assets/images/opportunity-adoption-chain.svg' | relative_url }})

Most of this data flows in automatically. When an instructor fills out a re-confirmation form on openstax.org, when behavioral signals from the website indicate continued usage, or when a third-party data source validates an adoption, the automated pipelines create and update Adoption records without anyone clicking a button. The chain from form submission to headline impact number is direct and largely hands-off.

That said, sometimes you learn about an adoption through a conversation, a support call, or a campus visit. When that happens, there's a **screen flow on the Contact record** specifically designed for this. It walks you through capturing what you learned and routes it into the right pipeline. You don't need to manually create Adoption records or edit Opportunity stages. Use the flow, and the system handles the rest.

**A general rule: Adoption records and Assignable records (outside of interest-related fields) should not be edited manually.** They're maintained by automated processes that keep them accurate and consistent. If something looks wrong, flag it for your admin or the data team rather than editing it directly.

### Pipeline Stages and Why They Matter

Every Opportunity sits at a stage, and that stage tells a story about where the relationship is in its journey.

For **Book Opportunities**, stage progression is largely automated. Re-confirmation forms, behavioral data from the website, and third-party adoption sources drive stage changes from Unconfirmed through Active. Lapsed status is applied when a previously confirmed adoption doesn't get re-confirmed in a new school year. You'll see these stages on records, and understanding what they mean helps you interpret the data, but you generally don't need to change them yourself.

For **Assignable Opportunities**, the instructor-level pipeline has more human touchpoints. Sales reps working with instructors evaluating the platform may update stages as conversations progress through discovery, demo, and implementation. Student-level records are automated from purchase and access code activity.

When leadership asks "how many instructors are actively using our books this year?" or "what's the Assignable revenue forecast for Q3?", the answer comes from counting Opportunities at specific stages. The automated pipelines keep the vast majority of this data current, which is why protecting those pipelines (and not manually overriding their work) matters.

