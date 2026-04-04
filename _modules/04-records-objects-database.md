---
number: 4
title: "Records, Objects, and the Database Wearing a Nice Outfit"
short_title: "Records & Objects"
description: "Objects, records, fields, and how a database becomes something you actually want to use."
---

If you only internalize one concept from this book, make it this one.

Salesforce is a database with a user interface on top of it. Everything in Salesforce is organized into **objects** (tables), **records** (rows), and **fields** (columns). That's the entire mental model.

An **object** is a category of thing. At OpenStax, the objects you'll encounter most include:

| Object | What It Represents |
|---|---|
| **Account** | An institution — a school, university, community college, or school district |
| **Contact** | A person — usually a faculty member, but also donors, partner contacts, and staff |
| **Lead** | A prospective person who hasn't been verified yet — the front door of the funnel |
| **Opportunity** | Something moving toward an outcome — a textbook adoption, a donation, an Assignable sale |
| **Case** | A support interaction — any time someone contacts OpenStax for help |
| **Campaign** | A marketing effort — an email send, a webinar, a conference, a seasonal push |
| **Book** | An OpenStax textbook — the catalog of titles available for adoption |
| **Adoption** | A time-stamped measurement of a textbook adoption — students reached and savings generated in a specific school year |

A **record** is one specific instance of an object. "Houston Community College" is a record on the Account object. "Dr. Jane Smith" is a record on the Contact object. "Biology 2e" is a record on the Book object.

A **field** is a piece of information on a record. The Account record for Houston Community College has fields for its name, address, phone number, enrollment size, LMS system, whether it's a KIP institution, and dozens more.

### What a Record Page Looks Like

When you open a record, you'll see several distinct sections:

**Detail fields** at the top show the core information about this record: names, statuses, dates, and key identifiers. These are the fields you'll read and update most frequently.

**Related lists** in the lower portion show records on *other* objects that connect to this one. On an Account record, you'll see related Contacts (the educators at that institution), related Opportunities (adoptions and deals), related Cases (support history), and more. These related lists are the connective tissue of the whole system.

**The activity timeline** (usually on the right side or in a tab) shows the chronological history of interactions: logged calls, emails, tasks, and events. This is the "what's happened recently" view.

**Chatter feed** shows internal team conversations attached to this specific record.

### Creating and Editing Records

Creating a record is straightforward: navigate to the object, click "New," fill in the fields, and save. Editing is even simpler: click the pencil icon next to any field on a record to edit it in place.

Some fields are **required** (marked with a red asterisk). These are fields the system needs to function correctly — skipping them isn't an option. Other fields are optional, but that doesn't mean they're unimportant. When you leave optional fields blank, you're leaving gaps in the organizational picture. The next person who opens that record, whether it's a support agent on a call, a sales rep preparing for a meeting, or a data analyst building a report, will have less context to work with.

Think about it from the other direction: when *you* open a record and everything you need is right there, that's because someone before you took the time to fill it in completely. Be that person for the next person.

