---
number: 11
title: "When Someone Needs Help — How Support Works in Salesforce"
short_title: "Support & Cases"
description: "How support requests become Cases, why classification matters, and how Case data informs the whole org."
---

Every time someone contacts OpenStax for help, whether it's a student who can't access their textbook, an instructor who needs faculty verification, or a partner with an integration question, that interaction becomes a **Case**.

### How Cases Arrive

At OpenStax, support requests arrive through every channel:

- **Email** to support@openstax.org, info@openstax.org, or service@openstax.org — the email thread is captured directly on the Case
- **Web forms** on openstax.org — the form submission creates the Case automatically
- **Live chat** — the full chat transcript attaches to the Case
- **Phone calls** through Service Cloud Voice — the call recording and an AI-generated summary link to the Case

Regardless of how someone reaches out, the support team sees the same unified interface. Every channel funnels into the same place: a Case record with the person's identity, their institution, the full interaction history, and (thanks to the relationship model) their adoption history, engagement profile, and any prior support cases.

![Every support channel (email, web form, chat, phone) funnels into a single unified Case record. Below, the three-level classification taxonomy: Product → Feature → Issue turns individual support conversations into organizational intelligence.]({{ '/assets/images/case-channels-taxonomy.svg' | relative_url }})

### The Classification System

What makes OpenStax's Case data particularly valuable is the three-level classification taxonomy. Every Case gets tagged with:

1. **Product** — What product is this about? (Textbook, Accounts, Assignable, Website, etc.)
2. **Feature** — What feature area? (Instructor Resources, Faculty Verification, Adoptions, Log In, Payment, etc.)
3. **Issue** — What does the person actually need? (Access Request, Credentials, How To, Error, etc.)

This taxonomy isn't bureaucratic overhead. It's what transforms individual support conversations into organizational intelligence. When the data team can run a report showing that "Instructor Resources > Access Request" is the number one support topic, and that it's grown 20% this semester, that's actionable information that can inform product decisions, content strategy, and process improvements.

Accurate tagging is one of the highest-leverage things a support agent (or anyone who creates a Case) can do. A well-tagged Case contributes to a clear picture. A vaguely tagged Case is noise.

### Escalation Levels

Most Cases are routine and resolve quickly. But OpenStax has escalation mechanisms for when things are more urgent:

- **Priority: High** means this is important and should be handled promptly
- **Critsit (Critical Situation)** is the "drop everything" flag — reserved for situations that require immediate cross-team attention

When a Case is escalated, the routing and visibility change to make sure the right people see it immediately.

### Why Accurate Case Data Matters Beyond Support

Case data doesn't just serve the support team. It feeds insights across the organization:

- **Product teams** use Case trends to identify friction points and prioritize improvements
- **The data team** analyzes Case patterns to understand which products, features, and issues generate the most support volume
- **Sales** can see whether a school they're working with has had support issues, informing their approach
- **Leadership** uses aggregate Case data to assess product health and resource allocation

When a support agent takes the extra ten seconds to tag a Case accurately, they're contributing to every one of those downstream use cases. Support data is one of the richest operational datasets in the organization — but only if it's clean.

