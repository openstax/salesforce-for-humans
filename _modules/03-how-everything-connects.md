---
number: 3
part: 1
title: "How Everything Connects"
short_title: "How Everything Connects"
description: "Follow one school, one instructor, and one book through the web of relationships that links every record."
key_points:
  - "Records link to each other as parents and children. Related lists are the paths between them."
  - "A school has Contacts, a Contact has Book Opps, and a Book Opp has one Adoption per school year."
  - "Districts are parents of their schools. Each team uses a different slice of the same web."
redirect_from:
  - /modules/05-how-everything-connects/
---

Records aren't isolated rows. Each one is linked to others, and those links tell a story no single record can. The quickest way to see it is to follow one school.

## One school, one instructor, one book

**Cedar Bluff Community College** is an Account, a two-year school that uses Canvas.

**Dr. Maya Rivera** teaches anatomy and physiology there. She's a Contact linked to that Account. Her Contact shows an Adoption Status of Current Adopter and an Instructor Engagement Tier of "1 - Champion".

She has a **Book Opp** (an Opportunity) for *Anatomy and Physiology 2e*. It represents her ongoing use of that book. Below it sit **Adoption** records, one for each school year she's used it: "2024 - 25", "2025 - 26", and so on. Each records how many students she reported and the estimated savings.

She also appears as a **Campaign Member** on a couple of campaigns, one for an email series and one for a webinar, with a status on each (Sent, Opened, Registered, Attended). Last fall she wrote to support about instructor resource access. That's a **Case**, linked to her Contact and her school.

![A relationship diagram. Cedar Bluff Community College (Account) has Contacts including Dr. Maya Rivera. Her Book Opp for Anatomy and Physiology 2e has Adoptions for 2024 - 25 and 2025 - 26. Cases and Campaigns link to the Contact and the Account.]({{ '/assets/images/relationship-web.svg' | relative_url }})

One click from the school shows who teaches there. One more shows what they've adopted, what they've asked us, and which emails they've seen.

## Parents and children

Most links follow a parent and child pattern.

| Parent | Children |
|---|---|
| Account | Contacts, Opportunities, Cases |
| Opportunity (Book Opp) | Adoptions |
| Campaign | Campaign Members |
| Lead (when converted) | becomes a Contact on the school's Account |

The **related lists** on a record page are the children, plus a few siblings. Click a row and you land on that record, with its own related lists. That's the whole navigation model: from a list view to a record to a related record.

A Campaign Member is a small record that joins a person to a campaign, with that person's status. A Contact in three campaigns has three Campaign Members.

## Account hierarchy

Accounts can have parents too. **Districts are parents of their schools.** Willow Creek Unified School District is the parent of Willow Creek High School, where Ms. Dana Brooks teaches Algebra 1. Some college systems are parents of their campuses in the same way. District hierarchies were cleaned up in fall 2026 and are now reliable.

To move up, use the **Parent Account** link on a school. To move down, open the district and look for its child accounts.

This matters for work that happens above the school level. A K12 conversation with a district reaches every school under it.

## Everyone sees a different slice

The web is the same for everyone. What changes is where you enter it.

- **CX** opens a Contact during a call and sees the school, adoption history, and earlier Cases.
- **Sales and the SDR** start from a school or the SDR Queue: who teaches there, what's adopted, where Assignable fits.
- **Marketing** builds audiences from Contact fields like Adoption Status, Engagement Tier, and subject interest.
- **Fundraising** works from donor Contacts and Donation opportunities.
- **Finance** looks at Opportunities, such as Assignable payments and orders.
- **Leadership** sees the totals in Tableau (see [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }})).

## Why it matters when you edit

Changing a record changes what everyone downstream sees. Fix a school on a Contact, and the instructor's OpenStax account catches up within about an hour. Tag a Case with the right product and issue, and support reporting gets better. Leave a real note, and the next person starts informed.

<div class="callout callout-green" markdown="1">
**Try it:** Open any school. Scroll to the related lists, click a Contact, then click one of that person's related records. Notice how few clicks it takes to go from a school to one instructor's history.
</div>
