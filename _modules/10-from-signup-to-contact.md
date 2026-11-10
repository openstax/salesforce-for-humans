---
number: 10
part: 3
title: "From Signup to Contact — Leads, Faculty Verification, and the SDR Queue"
short_title: "Signup to Contact"
description: "How a new openstax.org signup becomes a Lead, gets matched to a school, is verified as faculty, and becomes a Contact."
key_points:
  - "A **Lead** is a person we haven't confirmed yet. A **Contact** is a confirmed instructor or partner."
  - "Automation matches the school and runs verification. When it can't decide, an AI recommends and **a person decides**."
  - "Work the **SDR Queue** top-down by priority tier. A Merged Lead is finished: work the Contact."
---

Almost every instructor Salesforce knows about started as a signup on openstax.org. This module follows one of them from the moment they click "Create account" to the day they are a confirmed Contact, and shows where a person (maybe you) steps in. If you work in Customer Experience (CX) or the Sales Development Rep (SDR) role, this is your daily path.

## Leads and Contacts

A **Lead** is a person we haven't confirmed yet, usually a new instructor signup. A **Contact** is a confirmed person: a verified instructor, a partner contact, a donor. The rule of thumb: create a Contact only for confirmed instructors and partners. Everyone else is a Lead until someone checks.

Meet Sam Okafor (they), a biology instructor at Northgate State University. Sam signs up on openstax.org with a school email address and ticks *Biology 2e* as a book of interest.

![The path from signup to Contact: signup creates a Lead, automation matches a school, SheerID checks faculty status, and the result is either an automatic confirmation or an AI review followed by a person's decision, ending in a Contact or an Unqualified Lead.]({{ '/assets/images/10-signup-to-contact.svg' | relative_url }})

## Step 1: The signup becomes a Lead

Within moments, Salesforce has a Lead (record type Instructor Lead) holding Sam's details, the books they picked, and a **Signup Date**. When you count signups, use Signup Date, not Created Date.

## Step 2: Automation finds the school

Salesforce tries three lookups, in order, and stops at the first that works:

1. The school name returned by the verification service, SheerID.
2. The school or company Sam typed on the signup form.
3. Sam's email domain, compared with the website domains stored on school Accounts.

Personal domains like gmail.com are never used. Most Leads find a school this way. If nothing matches, the Lead gets a placeholder school called **Find Me A Home** and lands in the SDR Queue so a person can choose the right one. That placeholder is intentional, not an error.

<div class="callout callout-green" markdown="1">
**Try it:** On a Lead sitting at Find Me A Home, search for the real school by name or website domain and pick it, rather than leaving the placeholder. Capturing the email domain on any form you build helps the next person.
</div>

## Step 3: Faculty verification

SheerID checks most signups automatically, and most people never reach a human. If SheerID can't decide, the Lead needs a person. An AI assistant reads it first and writes a recommendation and summary in the fields that start with "AI FV" (AI FV Recommendation, AI FV Summary). **The AI advises. A person decides.**

The reviewer opens the Lead and uses the **Verify** action, a guided screen flow. The list views "AI says approve", "AI says reject", "AI asks for documents", "School not matched", and "Verified not converted" sort the work.

| FV Status | Meaning |
|---|---|
| Incomplete signup | The person started but didn't finish |
| Pending SheerID | Waiting on the automatic check |
| Rejected by SheerID | The automatic check said no |
| Pending faculty | A person needs to review |
| Confirmed faculty | Verified. Instructor resources unlock on openstax.org |
| Rejected faculty | A person reviewed and said no |
| SheerID expired / SheerID error | The automatic check didn't finish |

If SheerID can't verify Sam, they may email proof (a department page, a syllabus) to support. That email becomes a Case, and Salesforce links it to Sam's open Lead by email address, so the agent can decide from the Case.

## What happens when you confirm or reject

**Confirm.** The Lead converts into a Contact on the school's Account (Northgate State). If Sam already existed as a Contact, the new information merges into that Contact and the Lead is marked **Merged**. No duplicate appears. A repeat signup never downgrades someone who is already verified.

**Reject.** The Lead is closed as Unqualified, a rejection email goes out, and the person is opted out of marketing email. A Lead or account whose role is **Student** is rejected automatically.

A change to a person's school or Contact in Salesforce reaches their OpenStax account within about an hour.

## Two emails that aren't marketing

Two transactional emails come from this path: a reminder about three days after an unfinished signup, and a welcome when someone becomes confirmed faculty. They're separate from marketing email.

## The SDR Queue

The **SDR Queue** (called the CX lead queue until 2 November 2026) is one list of open instructor Leads that need a person. CX works it until the SDR role is fully in place. Every Lead carries an **SDR Priority Tier** and a plain-language **SDR Priority Reason**. Open the list view "SDR Queue: by priority" and work from the top.

| Tier | Name | Who is in it |
|---|---|---|
| 1 | Verification waiting | Blocked from instructor resources until someone decides |
| 2 | Hot intent | Asked to be contacted (for example, the Assignable interest form) |
| 3 | Finish the match | Needs a school matched or a conversion finished |
| 4 | Warm | Showing engagement or Assignable use |
| 5 | Cold list | Not urgent |
| Hold | Hold | Parked on purpose |

A **Send to SDR Queue** checkbox on a Lead keeps it in the queue. The home page "SDR Queue: work next" component shows the same list, filtered by tier.

<div class="callout callout-blue" markdown="1">
**Good to know:** To find Leads still waiting, filter on Status = Open. Older closed Leads can show a stale "pending" verification status. Lead Status values are Open, Unqualified, Lost, Merged, and Converted. A Merged Lead is finished; work the Contact, which now holds everything.
</div>

Once Sam is confirmed, their Contact is the place to read what we know. That's the next module: [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).
