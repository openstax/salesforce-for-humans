---
number: 1
part: 1
title: "The Shared Brain: Why OpenStax Keeps One Record of Everyone"
short_title: "The Shared Brain"
description: "What a CRM is, why OpenStax keeps one shared record, and why a spreadsheet can't do the job."
key_points:
  - "Salesforce is OpenStax's shared memory: one record of each school, instructor, adoption, and support request."
  - "A few dozen staff use it, and most records are created by automation. People add the context machines can't."
  - "Spreadsheets are fine for analysis. Ongoing relationships belong in the shared record."
redirect_from:
  - /modules/02-your-spreadsheet-is-not-a-strategy/
---

OpenStax works with hundreds of thousands of instructors at thousands of schools. Instructors adopt free textbooks, schools buy Assignable access, donors fund the mission, partners build on our content, and support answers questions all day. This module explains why we keep all of that in one place, who uses it, and what your part is.

## What a CRM is

Every one of those interactions teaches us something. A support agent learns that an instructor can't get their LMS (learning management system) to connect. The SDR (Sales Development Rep) hears that a department is picking homework tools for fall. Marketing notices which webinars lead to adoptions.

Knowledge like that is fragile. It lives in inboxes, notebooks, and memory. When someone changes roles or has a busy week, it goes dark, and the next person walks into the conversation blind.

A **Customer Relationship Management** system (CRM) is a shared memory. Salesforce is OpenStax's. Anyone who opens a record can see the whole relationship without asking five people in Slack.

![Salesforce sits at the center of every team at OpenStax. Customer Experience, Sales, Marketing, the website, and leadership all read from and write to the same shared system, each using the slice of data they need.]({{ '/assets/images/crm-hub.svg' | relative_url }})

## What we keep in it

As of late 2026, Salesforce holds about:

| Record | Roughly how many |
|---|---|
| Accounts (almost all are schools; about 1,600 are school districts, about 180 are partners) | 110,000 |
| Contacts (confirmed people) | 345,000 |
| Leads (people not yet confirmed) | 450,000 |
| Opportunities (an instructor's use of a book, plus Assignable and donations) | 360,000 |
| Adoptions (one instructor, one book, one school year) | 565,000 |
| Campaigns | 870 |
| Support Cases per year | 10,000 |

Those are rounded, and they move every day.

## Who uses it

A few dozen people log in: Sales (higher education (HE), K12, and the SDR), Marketing, Customer Experience (CX, our support team), Finance, Fundraising (our Mission Makers community), and the Data Intelligence team, who run the system. Each team lives in a different corner of it, covered in [Finding Your Way Around]({{ '/modules/05-finding-your-way-around/' | relative_url }}).

Many other systems write to Salesforce too, which brings up an honest point.

## Most records aren't made by people

Most records in Salesforce are created by automation: openstax.org signups and forms, the OpenStax Accounts system, Account Engagement (our marketing platform, also called Pardot), nightly Assignable data loads, and AI steps that sort incoming support requests. A person didn't type most of what you'll see.

What machines can't know is the story: the call where an instructor said they're switching books, the correction to a school's LMS, the reason a request is tricky. Your job is to add that. Cases are the big exception, since CX works them by hand every day. [Machines and People]({{ '/modules/04-machines-and-people/' | relative_url }}) sorts out what to leave alone and what to improve.

## Why not a spreadsheet?

Spreadsheets are wonderful for one-off analysis, quick math, and personal to-do lists. They are a poor home for relationships that other people depend on. Four reasons.

**Version control.** Two people track conference contacts. One adds three people on Tuesday, the other fixes two emails on Thursday. Now there are two versions of reality and no way to know which to trust. In Salesforce there is one record.

**Relational context.** A spreadsheet can tell you Sam Okafor teaches at Northgate State University. Salesforce can also tell you their faculty verification is pending, which books they're interested in, what they've asked support, and what we know about their school. A spreadsheet gives you a row. Salesforce gives you a story.

**Access control.** OpenStax handles sensitive data: donor information and student data protected by FERPA (the US student-privacy law). A shared spreadsheet is one accidental link-share from exposure and doesn't show who looked at what. Salesforce limits who can see which fields and keeps a history of changes. (See [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}).)

**Bus factor.** If the person who owns the spreadsheet leaves or goes on vacation, the data goes stale. In Salesforce, the data belongs to OpenStax.

![A spreadsheet row for Dr. Maya Rivera shows a name, school, and email. Her Salesforce record also shows her Adoption Status, Engagement Tier, related adoptions, cases, campaigns, school details, and the last conversation.]({{ '/assets/images/spreadsheet-vs-crm.svg' | relative_url }})

<div class="callout callout-green" markdown="1">
**Try it:** Next time you learn something about a school or instructor, ask "would someone else benefit from knowing this?" If yes, add a note or log the activity on their record instead of keeping it in your notebook.
</div>
