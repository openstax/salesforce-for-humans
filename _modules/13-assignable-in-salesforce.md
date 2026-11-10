---
number: 13
part: 3
title: "Assignable in Salesforce"
short_title: "Assignable"
description: "What Salesforce holds about Assignable: read-only course data, adoption status, opportunities, school fit, and instructor health."
key_points:
  - "Assignable's courses, assignments, access, codes, and payments appear in Salesforce as **read-only** data loaded by automation."
  - "A student completing Assignable work confirms the adoption. **Effective Student Count** is the larger of reported and Assignable students."
  - "Assignable opportunities start when a person opens one after real interest, not automatically from an adoption."
---

Assignable is OpenStax's paid digital homework and assignment platform. It runs inside a school's learning management system (LMS), such as Canvas. Salesforce doesn't run Assignable. It holds a copy of what happened there, plus the sales and relationship side. This module covers both, and the sales process is still evolving, so it sticks to what is settled.

## What Salesforce receives from Assignable

Automated jobs load these objects from Assignable's own systems. They're **read-only**: edits get overwritten.

| Object | What it is |
|---|---|
| Assignable Course | A course deployment (a classroom in an LMS) |
| Assignment | An assignment, with "Number of Student Completions", refreshed daily |
| Assignable Access | A student's access: Grace Period, Access Code, Direct Payment, or Free |
| Access Code and Access Code Batch | Codes a school or bookstore buys. Only redeemed codes show |
| Assignable Transaction | Payments |

Individual student records are protected student data, so you won't see them as ordinary records.

## Adoption Status and student count

Every Adoption carries an **Assignable Adoption Status** that climbs a ladder:

| Value | Meaning |
|---|---|
| 0 Book Available | The book is available in Assignable |
| 1 Integrated | The instructor's LMS is connected |
| 2 Created Assignment | An assignment exists |
| 3 Students Completed | Students did the work |

One student completion confirms the adoption as OpenStax Confirmed and credits the school year in which the students did the work. **Effective Student Count** is the larger of the reported students and Assignable's maximum student completions.

## Assignable opportunity types

| Type | What it tracks | Stages |
|---|---|---|
| Assignable Instructor | Interest in Assignable at a school | New, Working, Qualified, Committed, Closed Won, Closed Lost |
| Assignable Student | One student's payment | Closed Won or Closed Lost, set by automation |
| Institutional | A school or bookstore buying access centrally | Estimate Sent, Order Submitted, Access Codes Sent, Closed Won |

Only certain people can mark an Assignable Instructor opportunity Closed Won.

## How an opportunity starts now

Confirmed adoptions no longer create Assignable opportunities on their own. Here is the path:

1. An instructor fills in the **Assignable Interest Form**.
2. Salesforce creates a Lead in the SDR Queue at Tier 2 (Hot intent), and a **Qualify Interest** task for the school's owner.
3. A person opens the opportunity when there's real interest: the **Open an opportunity** button, the **Create Assignable Opportunity** action on a Contact, or **New Assignable Opportunity** on an Account.

Dana Brooks, an Algebra 1 teacher at Willow Creek High School, might do exactly this. Her interest form creates a Tier 2 Lead (see [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }})), and whoever owns Willow Creek gets a task to qualify it.

## What Salesforce knows about the school

Each school Account has Assignable fields, refreshed nightly:

- **Assignable Fit Tier**: A, B, C, Nurture, or Out, with a plain-language priority reason. Fit is based on how many instructors at the school have confirmed adoptions of books available in Assignable.
- **Assignable Stage**, the school's **LMS** and **LMS Install Path**.
- A qualification section (affordability programs and similar).

For Cedar Bluff Community College, which uses Canvas, you'd see Canvas as the LMS and a tier reflecting how many of its instructors already use books Assignable supports.

## Instructors, roles, and comps

**Assignable Instructor Health** is updated weekly: In regular use, Light use, At risk, or Lapsed. If an instructor stops, log why with the **Log Instructor Feedback** action on their Contact. That becomes **Instructor Feedback**.

The **Set role at this school** action on a Contact records their buying role. On an opportunity, contact roles now include **Champion** and **Technical Contact**.

A **comp** gives a course access with the student payment waived, approved through an approval flow. Students who enrolled before the comp can show Grace Period, and later ones Free.

<div class="callout callout-orange" markdown="1">
**Hands off:** Don't edit the Assignable course, assignment, access, code, or transaction records, or the nightly school fields. Automation overwrites them. If the data looks wrong, ask in #data-intel.
</div>

<div class="callout callout-blue" markdown="1">
**Good to know:** Sales Action Plan templates give you a checklist of dated tasks to start from a record. Use one when it fits.
</div>
