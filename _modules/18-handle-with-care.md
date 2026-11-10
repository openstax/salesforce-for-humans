---
number: 18
part: 5
title: "Handle With Care — Student, Donor, and Personal Data"
short_title: "Handle With Care"
description: "Most of what's in Salesforce is fine to use for work. This chapter covers the two kinds that need extra care, and the everyday habits that keep them safe."
key_points:
  - "Student data and donor data need extra care. Instructor, school, and adoption data is fine for normal work."
  - "Share counts and totals, not rows. For student performance on fewer than 10 students, show \"<10\"."
  - "Filter first, keep only the columns you need, and don't paste details into Slack, email, tickets, or AI tools."
  - "If something slips, tell the Data Intelligence team right away. Early is easy to fix."
---

Most of what you see in Salesforce is ordinary working information: schools, instructors, adoptions, Cases, campaigns, and totals. You can look at it, use it, and discuss it as part of your job. This chapter is about the two kinds of data that deserve a little more care, and the small habits that keep them safe.

## The two kinds that need extra care

**Student data** is protected by FERPA (the US federal law on student education records), and K-12 learners can be minors. Treat all of these as student data:

- a student's name or email
- a user ID or UUID (a long string of letters and numbers; it looks anonymous, but it isn't)
- one student's activity or scores
- anything a student wrote, including the text of a Case from a student

Students are mostly not in Salesforce at all, unless they use Assignable. If you see a student's record, look at it only when a support need requires it.

**Donor data** (Donor Contacts and the Mission Makers fields) is restricted. You can share totals and counts. You can't share names or rows.

<div class="callout callout-blue" markdown="1">
**Good to know:** Instructor and staff information is fine for business use. The care is about students and donors, and about not sending educator email lists anywhere for non-business purposes.
</div>

## Counts, not rows

A count answers most questions without exposing anyone. "How many students completed an assignment at Cedar Bluff?" is a count. "Which students?" is a list of people, and you almost never need it.

Small groups can point to one person. When you report a student performance statistic on fewer than 10 students, show "<10" instead of the number.

## Everyday rules

| Situation | ✅ Do | ❌ Don't |
|---|---|---|
| **Exporting a report** | Filter first (date, book, school), keep only the columns you need, delete the file when done | Export student or donor details, or keep copies on your laptop or a shared drive |
| **Spreadsheets** | Build a Salesforce report and use Save As for your own copy | Build a shadow spreadsheet. It has no audit trail and is one wrong share away from a leak. |
| **Slack, email, tickets, docs** | Share a link to the record, or a count | Paste student or donor details |
| **Screenshots** | Check for names, emails, Case text, access codes, payment details, and donor info before sharing | Share a screenshot of a Case or report without looking at it first |
| **AI tools** | Ask general questions, or describe a problem without identifying anyone | Paste student or donor details into an AI chat |
| **Case text** | Treat a student's message as student data | Quote it outside the Case |
| **Research requests** | Ask the Data Intelligence team in #data-intel | Pull row-level student data yourself and paste it into a ticket or chat |

Row-level student data for research needs FERPA training and approval through the Data Intelligence team. It's a short conversation, and they can usually suggest a version of the question that needs no student rows at all.

<div class="callout callout-green" markdown="1">
**Try it:** Before your next screenshot, scan it for four things: a name, an email address, a line of Case text, a code or payment detail. Crop or blur anything you find.
</div>

## If you make a mistake

It happens to careful people. You pasted the wrong report, shared a file with the wrong group, or sent a screenshot with a student's email in the corner.

1. **Stop.** Don't forward it or add to it.
2. **Tell the Data Intelligence team right away** by direct message rather than in a channel, so the details don't spread further. Say what was shared, where, and when.
3. **Leave the cleanup to the team.** They'll tell you what, if anything, you need to do. The sooner they know, the easier it is to fix.

For more on keeping the records themselves tidy, see [Keeping Data Clean]({{ '/modules/08-keeping-data-clean/' | relative_url }}). For who to contact and how, see [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}).
