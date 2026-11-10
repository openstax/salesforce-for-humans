---
number: 2
part: 1
title: "Records, Objects, and Fields"
short_title: "Records & Objects"
description: "The three ideas behind everything in Salesforce, the objects you'll meet, and how a record page is laid out."
key_points:
  - "An object is a table, a record is one row, and a field is one column."
  - "About a dozen objects cover almost everything you'll do. Record types sort one object into kinds."
  - "Every record page has the same parts: highlights, details, related lists, activity, and Chatter."
redirect_from:
  - /modules/04-records-objects-database/
---

If you keep one idea from this book, keep this one. Salesforce is a database with a friendly face. Once you see how it's organized, every page in it looks familiar.

## Objects, records, and fields

An **object** is a kind of thing, like a school or a person. A **record** is one specific example of it. A **field** is one piece of information on a record.

So "Account" is an object. "Cedar Bluff Community College" is a record on it. "LMS: Canvas" is a field on that record. Picture a table: the whole table is the object, each row is a record, and each column is a field.

![An Account table with columns for Name, Record Type, and LMS. Each row is a record, such as Cedar Bluff Community College, which is highlighted. The table is the object, the row is a record, and each column is a field.]({{ '/assets/images/objects-records-fields.svg' | relative_url }})

## The objects you'll meet

You'll hear about dozens of objects, but these cover nearly everything most people do.

| Object | What it is |
|---|---|
| **Account** | A school, district, partner, or other organization |
| **Contact** | A confirmed person: faculty, donor, or partner contact |
| **Lead** | A person we haven't confirmed yet, usually a new instructor signup |
| **Opportunity** | Something moving toward an outcome: an instructor's use of a book, an Assignable sale, a donation |
| **Adoption** | One instructor, one book, one school year |
| **Book** | The OpenStax catalog |
| **Case** | A support request |
| **Campaign** and **Campaign Member** | A marketing effort, and each person who took part |
| **Task** and **Event** | Activities: calls, to-dos, meetings |
| **Assignable objects** | Courses, assignments, access, and payments loaded from Assignable (read-only) |
| **Account External Data** | Yearly enrollment and classification figures for HE schools |
| **Individual** | One consent record per person, shared by their Lead and Contact |

Two more show up for specific teams: Instructor Feedback, and Contract (data agreements with districts, still being set up).

## Record types

One object can hold different kinds of records. **Record types** are how Salesforce sorts them, and they change which fields and options you see.

- **Account**: School, School District, Other Educational Institution, Partner, Vendor, General.
- **Contact**: Faculty, Donor, Partner, General.
- **Opportunity**: Book Opp, Book Dept, Assignable Instructor, Assignable Student, Institutional, Donation, Partner. Most are Book Opps.

Cedar Bluff Community College is an Account with the record type School. Willow Creek Unified School District is an Account with the record type School District. Same object, different kind.

## What a record page looks like

Open any record and you'll find the same layout, whether it's an Account, a Contact, or a Case.

1. **Highlights** at the top: the name and a few key fields, plus action buttons.
2. **Details**: the full set of fields. Click the pencil next to a field to edit it, if it's one you can edit.
3. **Related lists**: records on other objects that connect to this one. On a school, that means its Contacts, Opportunities, and Cases. Click any row to jump to that record.
4. **Activity**: the timeline of logged calls, tasks, events, and emails.
5. **Chatter**: posts and @mentions from colleagues, kept with the record.

![A record page for Cedar Bluff Community College. The header shows the highlights, followed by detail fields, then related lists for Contacts, Opportunities, Cases, and Campaigns. Callouts explain highlights and details, related lists, and activity and Chatter.]({{ '/assets/images/record-page-anatomy.svg' | relative_url }})

Learn this layout once and you can find your way around any object. The related lists matter most. They're the paths from one record to the next, which is the subject of [How Everything Connects]({{ '/modules/03-how-everything-connects/' | relative_url }}).

## Required and read-only fields

Fields marked with a red asterisk are required: Salesforce won't save the record without them. Optional fields are still worth filling in, because the next person to open the record has only what you left.

Some fields can't be edited at all. They're formulas that calculate themselves, or they're written by an automated system and would be overwritten. A field that looks greyed out is usually one of these. [Machines and People]({{ '/modules/04-machines-and-people/' | relative_url }}) lists the ones to leave alone.

<div class="callout callout-blue" markdown="1">
**Good to know:** You'll see field **labels** on screen, like "Adoption Status". Behind each label is a technical name that only matters when someone builds a report filter. This book uses labels.
</div>
