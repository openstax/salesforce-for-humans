---
number: 2
title: "Your Spreadsheet Is Not a Strategy"
short_title: "Spreadsheet vs. Strategy"
description: "Why spreadsheets can't replace a system of record, and what you lose when you try."
---

This module is an intervention, delivered with love.

Spreadsheets are wonderful tools. They're flexible, familiar, and fast to set up. They're perfect for one-off analysis, quick calculations, personal tracking, and ad-hoc data exploration. What they are *not* good at is serving as the system of record for an organization's relationships.

Here's why this matters at OpenStax.

**The version control problem.** Two people are tracking conference contacts. Both have spreadsheets. Both are correct, as of the day they last updated theirs. But one person added three new contacts last Tuesday, and the other updated two email addresses on Thursday. Now there are two divergent versions of reality, and nobody knows which one to trust. In Salesforce, there is one record. When someone updates it, everyone sees the update.

**The relational context problem.** A spreadsheet can tell you that Dr. Smith teaches at State University. Salesforce can tell you that Dr. Smith teaches at State University, adopted Biology 2e three years ago, attended two webinars, submitted a support case about instructor resources last month, received five marketing emails this year (opened three), has a Pardot engagement score indicating active interest, and works at an institution with 42,000 undergraduates and an existing LMS integration with Canvas. That context changes how you approach every interaction with Dr. Smith. A spreadsheet gives you a row. Salesforce gives you a story.

![Side-by-side comparison: a spreadsheet row shows name, institution, and email — and that's it. The Salesforce record for the same person shows adoption history, engagement score, support cases, campaign interactions, institution details, and the last conversation. A spreadsheet gives you a row. Salesforce gives you a story.]({{ '/assets/images/spreadsheet-vs-crm.svg' | relative_url }})

**The access control problem.** OpenStax handles sensitive data: donor information, student records subject to FERPA, institutional partnership details. A spreadsheet shared via Google Drive has no field-level security, no audit trail of who viewed what, and is one accidental permission change away from exposure. Salesforce has role-based access, field-level security, record-type visibility rules, and complete audit logging.

**The "bus factor" problem.** If the person who maintains the spreadsheet leaves, gets busy, or goes on vacation, the data goes stale or becomes inaccessible. In Salesforce, the data belongs to the organization, not to any individual.

None of this means you should never use a spreadsheet. Spreadsheets are great for what they're great for. But when the data represents an ongoing organizational relationship (an institution, an educator, a partnership, a pipeline deal), it belongs in the shared system where it can be connected, secured, and maintained by the whole team.

The practical shift is this: when you have information about a person, an institution, or an interaction, ask yourself "would someone else benefit from knowing this?" If the answer is yes, it belongs in Salesforce.

