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

When you confirm that an instructor is still using their OpenStax textbook, that confirmation creates or updates an Adoption record. That Adoption record feeds the school year's impact numbers. Those impact numbers go into funder reports, board presentations, and the OpenStax website. The chain from your click to the headline number is direct and traceable.

### Pipeline Stages and Why They Matter

Every Opportunity sits at a stage, and that stage tells a story about where the relationship is in its journey. Moving an Opportunity from one stage to the next isn't just bookkeeping — it's how the organization understands its pipeline.

When leadership asks "how many instructors are actively using our books this year?" or "what's the Assignable revenue forecast for Q3?", the answer comes from counting Opportunities at specific stages. If stages aren't updated, the pipeline view is wrong. If a lapsed adoption isn't marked as lapsed, it inflates the active count. If a closed deal isn't moved to Closed Won, it's missing from the revenue forecast.

Stage accuracy is a team effort. The data is only as good as the updates.

