---
number: 8
part: 2
title: "Keeping Data Clean"
short_title: "Keeping Data Clean"
description: "What bad data costs, how duplicate rules actually work, and the small habits that keep records trustworthy."
key_points:
  - "Bad data rarely announces itself. It quietly skews every report, email, and support call that touches the record."
  - "Search before you create. Creating a duplicate Account is blocked, and a possible duplicate Contact or Lead triggers a warning you should read."
  - "Create a Contact only for a confirmed instructor or partner. Everyone else is a Lead."
  - "Fill in what you know, and flag what's wrong in #data-intel."
redirect_from:
  - /modules/13-data-hygiene/
---

Most records in Salesforce are created by machines, but people are the ones who notice when something is off. This module is about what bad data costs, what the system does to stop it, and the few habits that make the biggest difference.

## What bad data costs

Bad data doesn't throw an error. It just makes everything downstream a little wrong.

- **Duplicates.** Dr. Maya Rivera exists twice, once as "Dr. Maya Rivera" and once as "Maya Rivera, PhD". One record holds her adoption, the other her support Case. The agent sees half the story, and marketing emails her twice.
- **Missing fields.** If Cedar Bluff Community College has no LMS recorded, nobody filtering for Canvas schools will find it when Assignable outreach starts.
- **Stale data.** An instructor's email bounced last spring and nobody noticed. The address stays on lists and the reachable audience looks bigger than it is.
- **Misclassified Cases.** A Case tagged with the wrong Product or Issue sends support trend reports in the wrong direction, and the team may chase a problem that isn't there.

![Two duplicate Contact records for Dr. Maya Rivera, each with half the history, next to the single record they should be.]({{ '/assets/images/bad-data-ripple.svg' | relative_url }})

## How duplicate rules work

Salesforce checks for matches when a record is created. The rules differ by object.

| Object | What happens on a match |
|---|---|
| **Account** | Creating a match is **blocked**. Find and use the existing school. For a second campus, ask in #data-intel. |
| **Contact** and **Lead** | A **warning** appears with the possible match. Open it and look. Don't click past it. |
| **Opportunity** | Opportunities **can't be merged**, so check the Contact's existing Book Opps before opening a new one. |

Salesforce can merge Contacts, Leads, and Accounts. Donation records with the same email can be merged too, but records with different donor IDs can't. Ask the data team rather than merging by hand.

When a new Lead matches an existing Contact, the answer is usually to work the Contact. The person is already confirmed, and the signup process merges new details into the Contact anyway. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

## Check before you create

1. Search by **email address** first, then by name.
2. For a school, search the name and a distinctive word from it. "Cedar Bluff" beats "Cedar Bluff Community College" if someone typed it slightly differently.
3. If you find a match, open it and add to it.
4. If you find nothing and it's right to create, then create it.

### Contact or Lead?

Create a **Contact** only for a confirmed instructor or partner. A person who hasn't been confirmed, such as someone who signed up and is in verification, is a **Lead**. Making a Contact for an unverified person skips the checks that protect instructor access and your adoption counts.

## Fill in what you know

You learn things on calls that no system will. If Dr. Rivera says Cedar Bluff switched to Canvas, update the LMS on the Account. If an instructor says they teach Chemistry now, update their Subject Interest. Each small edit helps the next search, list view, and campaign.

For things you heard about adoptions, use the Build Adoption flow on the Contact instead of editing records directly (see [Machines and People]({{ '/modules/04-machines-and-people/' | relative_url }}) for the hands-off list).

## Flag what's wrong

Spot a duplicate, a dead email, a school with the wrong parent district, or a number that looks off? Post it in **#data-intel** with a link to the record. Don't just work around it. The Data Intelligence team can fix the cause as well as the record, and your flag may save the next ten people the same detour.

## If you delete something

Deleted records go to the **Recycle Bin** and can be restored for **15 days**. After that, ask the data team. If you deleted the wrong thing, say so right away. Early is easy to fix.

## The data policy in one paragraph

Salesforce keeps people, organizations, and outcomes. Detailed event logs, such as every download or every email send, live in the source systems or the data lakehouse, not here. Don't upload copies of files that live somewhere else. Link to them instead. Field history is kept for 18 months.

<div class="callout callout-green" markdown="1">
**Try it:** Open a school you work with and look for one blank field you can fill from what you know today: LMS, a subject, a website. Fill it in.
</div>

<div class="callout callout-orange" markdown="1">
**Hands off:** Adoption records, Book Opp stages, Assignable objects, and Account Engagement fields (the `pi__` ones) are written by automation. Your edits would be overwritten or would confuse the counts. [Machines and People]({{ '/modules/04-machines-and-people/' | relative_url }}) has the full list.
</div>
