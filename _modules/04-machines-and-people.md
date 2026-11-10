---
number: 4
part: 1
title: "Machines and People: What Runs Itself and What Needs You"
short_title: "Machines & People"
description: "Which systems write into Salesforce, which fields to leave alone, and where your edits help most."
key_points:
  - "Automation creates and updates most records. Fields it owns get overwritten if you edit them."
  - "Leave Adoptions, Book Opp stages, formula fields, Account Engagement fields, and Assignable data alone."
  - "People improve Cases, notes, Contact and school details, duplicates, and opt-outs. Report anything odd in #data-intel."
---

Before you edit anything, it helps to know who else is writing to the record. Many systems feed Salesforce, and some fields belong to them. This module sorts the fields into three piles: what machines own, what people improve, and what to do when something looks wrong.

![Systems on the left feed Salesforce: openstax.org and Accounts, Account Engagement, Assignable nightly loads, AI assistants, and adoption automation. People on the right add Cases, activities and notes, corrections and details, and judgment calls. Tableau reads from Salesforce.]({{ '/assets/images/04-machines-and-people.svg' | relative_url }})

## What writes into Salesforce

| Created or updated by | What it touches | Your role |
|---|---|---|
| **openstax.org and OpenStax Accounts** | New instructor signups become Leads. Form submissions land on records. Changes to a school or Contact in Salesforce reach the person's OpenStax account within about an hour. | Review Leads that need a person (see the SDR Queue). Fix school and Contact details. |
| **Account Engagement** (Pardot) | Score, grade, email activity, and bounce status on Leads and Contacts. It reads opt-outs, Adoption Status, and school type from Salesforce. | Record opt-out requests. Don't edit its fields. |
| **Assignable nightly loads** | Courses, assignments, access, access codes, and payments, plus school fit fields. | Read only. Edits are overwritten. |
| **AI case classification** | Soon after an email, web, or chat Case arrives, it fills Summary, Type, Reason, and other tags, and flags spam. | Correct Product, Feature, or Issue if they're wrong. |
| **AI faculty verification (FV) review** | Writes a recommendation and summary on Leads that need a human. | The AI advises. A person decides. |
| **Adoption automation** | Creates Adoptions from forms, conversations, and Assignable student work, and sets Book Opp stages. | Log adoptions you hear about with the Build Adoption flow. Don't edit the results. |
| **Tableau** | Reads Salesforce each day for dashboards. It writes nothing back. | Report a wrong number rather than fixing it in place. |

## Hands off

<div class="callout callout-orange" markdown="1">
**Hands off:** Automation owns these. Your edit will be overwritten, or will quietly confuse a count.

- **Adoption records.** Several automations write them. Never create or edit one by hand.
- **Book Opp stages.** Set from that Opportunity's Adoptions for the current school year. People don't move them.
- **Formula fields**, such as a Contact's Adoption Status and Instructor Engagement Tier. They recalculate themselves.
- **Fields from Account Engagement**, the score, grade, activity, and bounce fields (technical names start with `pi__`).
- **Assignable objects**: Courses, Assignments, Access, Access Codes, Transactions.
- **Case Summary, Type, and Reason.** These belong to the AI.
- **AdoptionsJSON fields** on Leads and Contacts. They hold form data in transit.
</div>

Not sure whether a field is automated? Look for a pencil. If you can't edit it, there's a reason. If you can, ask in #data-intel before changing anything on the list above.

## Yours to improve

This is where people matter most. Machines fill records in volume. They can't know the story.

- **Cases.** CX works them by hand. Fix Product, Feature, and Issue tags when the AI guessed wrong, and the AI will leave your choice alone.
- **Activities and notes.** Log calls, meetings, and conversations. See [Logging Your Work]({{ '/modules/07-logging-your-work/' | relative_url }}).
- **Contact details.** Subject Interest, role at the school, and a correct school.
- **School details.** Facts like the school's LMS.
- **Duplicates.** Flag possible duplicate Contacts, Leads, and Accounts instead of working around them.
- **Adoptions you hear about.** On the instructor's Contact, use the **Build Adoption** flow. It creates the Adoption the right way.
- **Opt-outs.** When someone asks to stop getting email, record it on their Contact and on their Lead if one is open.

<div class="callout callout-green" markdown="1">
**Try it:** Open a Contact you know well and check three things: the school, the role, and the Subject Interest. If one is out of date, fix it. That small edit helps CX, Sales, and Marketing at once.
</div>

## When something looks wrong

Post in **#data-intel** on Slack. Include a link to the record (the URL works), what you expected, and what you see. Don't paste student names, emails, or Case text from a student.

The Data Intelligence team will look, and often turns a post into a ticket. If the problem is a field you can fix yourself, like a school or a role, fix it. If it's an automated field, the fix is upstream, and they'll handle it. [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}) covers the rest.

<div class="callout callout-blue" markdown="1">
**Good to know:** An "oddly empty" or "oddly full" record is often a timing issue. Some systems sync nightly or weekly, and Tableau lags about a day. Check again tomorrow before you worry.
</div>
