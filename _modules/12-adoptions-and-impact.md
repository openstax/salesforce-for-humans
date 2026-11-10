---
number: 12
part: 3
title: "Adoptions — How OpenStax Counts Its Impact"
short_title: "Adoptions & Impact"
description: "Book Opps, Adoption records, school years, and why the headline impact numbers come from Tableau instead of a Salesforce report."
key_points:
  - "A **Book Opp** is one instructor and one book. Each **Adoption** under it is one school year."
  - "Only OpenStax Confirmed and Third Party Confirmed adoptions count toward students and savings. \"Assumed\" ones never do."
  - "Headline numbers are built in Tableau with rollover and lag about a day, so a raw Salesforce report won't match them."
redirect_from:
  - /modules/12-the-pipeline/
---

Adoptions are how OpenStax measures whether the mission is working: an instructor, a book, a class of students, a school year. This module explains the records behind that, who creates them (mostly machines), what you can safely do, and why the published numbers don't come from adding up a Salesforce report.

## Opportunities come in several kinds

An Opportunity in Salesforce is something moving toward an outcome. OpenStax uses **record types** to split it into separate kinds of work, so always filter by record type in a report.

| Record type | Tracks |
|---|---|
| Book Opp | An instructor's use of one book. Most Opportunities are this |
| Book Dept | A department-level book adoption (rare) |
| Assignable Instructor | Interest in Assignable at a school ([Assignable in Salesforce]({{ '/modules/13-assignable-in-salesforce/' | relative_url }})) |
| Assignable Student | One student's payment for Assignable |
| Institutional | A school or bookstore buying Assignable access centrally |
| Donation | A gift to OpenStax (Fundraising) |
| Partner | Partner revenue (rare) |

## Book Opp and Adoption

A **Book Opp** is the long-running relationship: this instructor, this book. Under it hang **Adoption** records, one for each school year (sometimes more than one). Think of the Book Opp as who and which book, and the Adoption as when, how many students, and how much saved.

Dr. Rivera at Cedar Bluff Community College has one Book Opp for *Anatomy and Physiology 2e*, with an Adoption beneath it for each year she has taught from it.

![Dr. Rivera's Book Opp for Anatomy and Physiology 2e has five possible stages, set by automation. Beneath it sit Adoption records for 2024 - 25, 2025 - 26, and 2026 - 27 with example student counts. Confirmed adoptions feed the impact numbers built in Tableau. Example data.]({{ '/assets/images/opportunity-adoption-chain.svg' | relative_url }})

Each Adoption records its **School Year**, **Reported Students**, **Savings per Student**, **Savings**, **Confirmation Type**, Confirmation Date, and How Using. Savings is a formula, students times the book's savings rate, so it's an estimate against a traditional textbook rather than a receipt.

## School years

A school year runs July 1 to June 30, the same as OpenStax's fiscal year. In Salesforce it's written **2026 - 27**, with spaces around the hyphen, and filters need that exact text. The current school year is 2026 - 27. Instructors can report last, this, and next year on one form, so say which year you mean.

## How we know: Confirmation Types

| Confirmation Type | Where it comes from | Counts? |
|---|---|---|
| OpenStax Confirmed Adoption | The instructor told us: an adoption or renewal form, a logged conversation, or real student work in Assignable | Yes |
| Third Party Confirmed Adoption | An outside source, such as bookstore, courseware, or partner data | Yes |
| User Behavior Informed Adoption | Inferred from signals like downloads. No student count, $0 savings | No ("assumed") |

## The five Book Opp stages

Automation sets the stage from that Opportunity's Adoptions for the current school year. People don't move them.

| Stage | Meaning |
|---|---|
| Unconfirmed | Nothing confirmed, nothing current |
| Assumed - Book Likely in Use | Only behavior signals this year |
| Active - Book Currently in Use | A confirmed adoption this school year |
| Lapsed - Book Used Previously Not Currently | Confirmed in an earlier year, not yet this year. Not lost: may return |
| Inactive - Book No Longer in Use | Confirmed stopped. Automation leaves it alone |

Behavior signals alone never make a Book Opp Active. A Contact's **Adoption Status** is computed from the same records ([Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }})).

## How adoptions arrive

Almost all of them come without a person typing anything:

- An instructor submits the adoption form or the **Renewal Form** on openstax.org. Each year an automated email asks past adopters to confirm they're still using the book, and a confirmation creates a fresh Adoption for the new year.
- A third-party data source confirms one.
- Assignable records a student completing work (see the next module).
- Behavior signals create "assumed" adoptions, and nothing more.

## Logging one you heard about

Heard it from an instructor on a call or at a campus visit? Open their Contact and run the **Build Adoption** flow. Pick the book, school year, number of students, how they use it, and add a description. The flow refuses roles that can't adopt (Student, Librarian, Instructional Designer, Administrator).

<div class="callout callout-orange" markdown="1">
**Hands off:** Don't create or edit Adoption records by hand, and don't change Book Opp stages. Several automations write them and will recompute over your edit. Leave the AdoptionsJSON fields on Leads and Contacts alone too: that's form data in transit. If a record looks wrong, post in #data-intel.
</div>

## Why the headline numbers live in Tableau

Students reached, savings, and "used in N classrooms" are built in **Tableau**, not by summing a Salesforce report. They count confirmed adoptions only, exclude test accounts, and use **rollover**: a model that assumes a confirmed adoption continues until there's evidence otherwise. Tableau refreshes daily, so figures lag about a day.

A raw Salesforce report will not match the published figure, and that's expected. It's a different question with different settings. This book doesn't quote totals; for those, use OpenStax's official impact figures.

<div class="callout callout-blue" markdown="1">
**Good to know:** Several Adoption rows per instructor per year are normal, so a count of Adoption records isn't a count of instructors or schools. When you share any number, say the school year, the confirmation types, and whether rollover is on.
</div>
