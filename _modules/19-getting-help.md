---
number: 19
part: 5
title: "Getting Help — Asking the Right Questions"
short_title: "Getting Help"
description: "Where to go with a Salesforce question, and how to write a request that gets a useful answer the first time."
key_points:
  - "**#data-intel** in Slack is the front door for questions, report requests, login trouble, and \"this looks wrong.\""
  - "Bigger requests go on the **DATA** board in Jira, with a due date and some lead time."
  - "Describe your goal, not your guess at the fix. That's how you avoid the XY problem."
  - "Check Trusted Numbers, list views, and the glossary first. They answer a lot."
redirect_from:
  - /modules/16-asking-the-right-questions/
---

The Data Intelligence team runs Salesforce, Account Engagement (Pardot), and Tableau. They're your partners, not a ticket counter, and how you ask shapes how fast you get an answer. This chapter covers where to go and how to ask.

## Where to go

| You need... | Go to |
|---|---|
| A quick question, a report request, access or login trouble, or "this number looks wrong" | **#data-intel** in Slack |
| Live help and demos | **Data Office Hours**, the first Wednesday of every month. They're recorded and posted in #data-intel. |
| A bigger request (a new report, a new field, a data pull) | The **DATA** board in Jira. There's a request form; give a due date. The team will often turn your #data-intel post into a ticket for you. |
| Phone or voice trouble (dial button greyed out, "Couldn't connect to telephony") | Refresh the page first. If it persists, post in #data-intel. |
| A change to openstax.org | A separate request process through Creative Services, not the data team |
| General Salesforce skills | [Trailhead](https://trailhead.salesforce.com), Salesforce's free learning site |

<div class="callout callout-green" markdown="1">
**Try it:** Join #data-intel today and skim the last few weeks. You'll see which questions get asked, how people phrase them, and what answers look like.
</div>

## The XY problem

You want to get something done (X). You decide a particular fix (Y) is the answer, and you ask for Y. If Y is the wrong tool, nobody notices, because nobody ever heard about X.

> ❌ "Can you add a field to Account called 'Priority Level' with values High, Medium, and Low?"

> ✅ "I want to know which schools to call first about Assignable next semester. Today I check adoption history, LMS, and enrollment one school at a time. Can you help?"

The second request lets the team say, "That already exists," or "A list view would do it," or "We could build a field, but here's a better one." In this case, schools already carry an Assignable Fit Tier, refreshed every night. The first request would have produced a second, hand-maintained field next to it.

![Two requests side by side. The left asks for a specific new field and hides the real need. The right describes the goal, so the team can offer an existing field, a list view, a report, or a dashboard.]({{ '/assets/images/xy-problem.svg' | relative_url }})

## How to write a good request

Include five things:

1. **Your goal.** What are you trying to get done, and why?
2. **Who needs it.** Just you, your team, or everyone?
3. **How often.** A one-time pull, or something you'll use every week?
4. **What you tried.** The report you opened, the filter you changed, the place you looked.
5. **By when.** A real date. Allow lead time: a quarter ahead is better than a few days.

A request like "Can you pull me some adoption data?" needs several rounds of follow-up before anyone can start. Compare:

> "For the board slides on October 15, I need confirmed adoptions for Cedar Bluff and Northgate State, grouped by book, school year 2026 - 27. I tried the Adoptions report in Trusted Numbers, but it doesn't group by school. One time only."

Anyone on the team can start on that one.

## Try these first

Many questions answer themselves in a minute:

- **★ Trusted Numbers** may already hold the report. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).
- **A list view filter** might get you the list you need. See [Finding Things]({{ '/modules/06-finding-things/' | relative_url }}).
- **The [glossary]({{ '/modules/21-glossary/' | relative_url }})** explains the terms in this book.
- **A teammate** probably knows the trick.

## Releases and sign-in

Salesforce ships three releases a year. Winter '27 arrived in October 2026. The team posts what changed in #data-intel, which is worth a skim, because a button may have moved.

Salesforce also requires multi-factor authentication (MFA) with an authenticator app. If your login breaks, ask in #data-intel.

<div class="callout callout-blue" markdown="1">
**Good to know:** If you're sharing a screenshot or a record in your request, check it first for student or donor details. See [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}).
</div>
