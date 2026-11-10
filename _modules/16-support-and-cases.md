---
number: 16
part: 4
title: "Support and Cases"
short_title: "Support & Cases"
description: "How support requests arrive, how AI tags them, what the tags mean, and how to leave a Case better than you found it."
key_points:
  - "Every request, from any channel, becomes a **Case** matched to a person by email or phone."
  - "AI fills **Summary, Type, and Reason**; agents can fix **Product, Feature, and Issue**."
  - "Account access and faculty verification are the biggest support topics, and Case data shows it."
  - "Case text from a student is student data: handle it with care."
redirect_from:
  - /modules/11-when-someone-needs-help/
---

A **Case** is a support request. About 10,000 arrive each year, from a student locked out of a book, an instructor waiting on faculty verification, or a partner with an integration question. Customer Experience (CX) works Cases by hand every day, which makes them the big exception in a system where most records are created by automation. This module is for CX and for anyone else who creates or touches a Case.

## How requests arrive

| Channel | What happens |
|---|---|
| **Email** | Messages to support@openstax.org and other OpenStax help inboxes become Cases. The email thread stays on the Case. |
| **Web form** | Forms on openstax.org create a Case. |
| **Chat** | An AI chat assistant answers from help content that CX has verified. If it can't help, it hands the conversation to a person. Files uploaded in chat, such as verification proof, attach to the Case. |
| **Phone** | Calls are recorded and an AI summary lands on the Case. Not every call becomes a Case. |

Each Case records its channel as **Origin**: mostly Email, Chat, Web, and Phone, with a few Errata, Internal, and Partner. Every channel tries to match the requester by email (including alternate addresses) and by phone, and a phone number is remembered once someone is identified. That is why a Case often opens with the person's school and history already attached.

## What the AI fills in

Soon after an email, web, or chat Case arrives, an AI step reads it and fills in **Summary**, **Type**, **Reason**, **Sentiment**, **Product**, **Feature**, and **Issue**. It also flags spam, which goes to a Spam Queue.

- **Summary, Type, and Reason** belong to the AI. They are read-only for agents.
- **Product, Feature, and Issue** can be changed by agents. The AI only fills blanks, so a person's choice always wins.
- **Phone Cases** use a separate flow that works from the call transcript, and their subject starts with "[Phone]". So the tags can differ slightly from an email Case about the same problem.

![Four support channels feeding one Case record, an AI step that fills the classification fields, and example Product, Feature and Issue values.]({{ '/assets/images/case-channels-taxonomy.svg' | relative_url }})

## The taxonomy

Cases are tagged **Product, then Feature, then Issue**, alongside a **Reason** and a **User Type** (Faculty, Student, K-12 Teacher, and so on). These values show up most often:

| Level | Common values |
|---|---|
| **Reason** | Account Access, Product Question, Content Request, Technical Issue, Payment & Billing, Integration Support, Partnership Inquiry |
| **Product** | Accounts, Textbook, General, Assignable, REX, Website |
| **Feature** | Faculty Verification, Sign Up, Payment, Automated Emails, Instructor Resources, Account Profile, Errata, Accessibility |
| **Issue** | Credentials, 6 Digit Pin, How To, Access Pending, Error, Delete Account, Test Banks |

## Priority and Critsit

**Priority** is Low, Medium, or High. **Critsit** is a checkbox for a rare "critical situation" that needs immediate attention across teams. Tick it only when people from several teams need to act right now.

## What Case data tells the rest of OpenStax

Tags turn thousands of individual conversations into a picture. Account access and faculty verification dominate, and the answers to both live in OpenStax Accounts; Salesforce is where CX reaches them. Product teams use the same data to see where people get stuck, and sales can see whether a school has had trouble.

Verification Cases also feed the signup process. Proof sent to support is linked to the open Lead by email address, so the agent can decide from the Case. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

## Good habits

1. **Fix Product, Feature, and Issue when they are wrong.** It takes seconds, and every report downstream benefits.
2. **Keep the conversation on the Case.** Reply from the Case so the thread stays with the record, not in a side inbox.
3. **Check the person.** If the Case matched the wrong person, or none, correct it before replying.
4. **Mind what students write.** Case text from a student is student data. Don't paste it into Slack, tickets, or screenshots. See [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}).

<div class="callout callout-green" markdown="1">
**Try it:** open one of your recent Cases and read the Summary against the Product, Feature, and Issue. If they disagree, fix the tags.
</div>
