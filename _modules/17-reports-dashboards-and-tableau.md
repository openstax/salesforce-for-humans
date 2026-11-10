---
number: 17
part: 5
title: "Reports, Dashboards, and Tableau — Where the Numbers Live"
short_title: "Reports & Tableau"
description: "How to read a report, find the trusted ones, use Tableau, and state a number so nobody argues about it later."
key_points:
  - "Change filters or **Save As** to answer your own question. Never edit a shared report."
  - "Look in **★ Trusted Numbers** first, then the subject folders, then **Explore**."
  - "Headline impact numbers come from **Tableau**, not from adding up Salesforce rows."
  - "Say the school year, confirmation types, rollover setting, and as-of date every time you quote a number."
redirect_from:
  - /modules/08-reading-the-numbers/
---

Almost every conversation at OpenStax eventually turns into "what's the number?" This chapter helps you find the right one, read it correctly, and describe it so the next person gets the same answer.

## Anatomy of a report

A Salesforce report is a saved question about your data. It has four parts worth knowing:

- **Filters** decide which records are included: a school year, a record type, a confirmation type.
- **Columns** are the fields shown for each record.
- **Groupings** collect rows that share a value, such as school or book.
- **Summaries** add up each group (a count, a sum, an average) and the whole report.

![A report titled Adoptions by School for school year 2026 - 27, with callouts pointing to the filter bar, the columns, the groupings by school, and the subtotal rows. The data is made-up example data.]({{ '/assets/images/report-anatomy.svg' | relative_url }})

The most useful skill is changing a filter on a report someone else built. Say a colleague's report lists all adoptions this year and you only want your territory. Add a filter, run it, and you have your answer.

<div class="callout callout-orange" markdown="1">
**Hands off:** Don't save changes to a shared report. Others rely on it exactly as it is. Click **Save As** (in the report's menu), give it a name, and put your copy in the **Explore** folder. Change the copy as much as you like.
</div>

## Where to look first

Report folders were reorganized in October 2026, and about 1,400 reports nobody had opened were removed. Start at the top of this list and work down.

| Folder | What's in it | How to use it |
|---|---|---|
| **★ Trusted Numbers** | Curated reports that follow the team's shared definitions | Open and read. Use **Save As** to change anything. |
| **Subject folders** | Adoptions and Students, Assignable, Campaigns and Marketing, Finance, Instructors and Contacts, K12, Leads, Opportunities, Schools and Accounts, Support, and more | Browse by topic. |
| **Curated Dashboards** | Dashboards built from the trusted reports | Glance, then drill down. |
| **Explore** | Anyone can save their own work here | Your sandbox. Expect it to be messy. |
| **Archive** | Retired reports, kept until mid-2027 | Check here if a favorite vanished. |

The curated reports share a few conventions. The school year runs July to June, the same as the fiscal year. Headline adoption counts include confirmed adoptions only, and leave out rollover and test accounts. Leads are counted by Signup Date. When you build your own report, follow the same rules so your numbers line up with theirs.

<div class="callout callout-green" markdown="1">
**Try it:** Open the Reports tab, search for a topic you care about, and open the first result in ★ Trusted Numbers. Inside a report, the eye icon next to a row lets you preview that record without leaving the report (new in Winter '27).
</div>

## Dashboards and drill-down

A dashboard is a page of charts and big numbers, each powered by a report. Most components are clickable: click a bar and you land in the report behind it, with every row listed. The dashboard is the summary, and the report is the evidence.

![A dashboard titled Adoption Dashboard for school year 2026 - 27 with a student total, a bar chart by market, a pie chart of confirmation types, and a table of top titles. All numbers are made-up example data. A callout explains drill-down and a sidebar lists the three parts of a report request.]({{ '/assets/images/dashboard-layout.svg' | relative_url }})

## Tableau Cloud

Tableau holds the dashboards for organization-wide questions: adoption counts, goals, Assignable, support, and pipeline. Sign in with Salesforce single sign-on at openstax.org/r/tableau. If you can't see a dashboard, ask in #data-intel; some projects are open to everyone and some are scoped to a team. The old dataviz.rice.edu site is retired, so don't send anyone there.

| If your question is... | Open this |
|---|---|
| How many adoptions, by book, school, or school year? | **Adoptions Dashboard** |
| Are we on track for our organizational goals? | The **KPI** workbook |
| How is Assignable doing? | **Assignable Dashboard** |
| How many support cases, and how fast do we resolve them? | **Service Cloud v2** |
| What does back-to-school support traffic look like? | **War Room** |
| What's in the sales pipeline? | **Weighted Sales Pipeline** |

Tableau refreshes once a day, so it runs about a day behind Salesforce. For a number that has to be current this minute, use a Salesforce report instead.

## Why two numbers can both be right

Someone will eventually show you a Tableau figure and a Salesforce report that disagree. Usually neither is wrong. The usual causes:

- **Different school year.** "This year" can mean 2026 - 27 or the calendar year.
- **Different confirmation types.** Only OpenStax Confirmed and Third Party Confirmed adoptions count as confirmed. User Behavior Informed adoptions (inferred from signals, with no student count) don't.
- **Rollover on or off.** Tableau's headline numbers assume a confirmed adoption continues until there's evidence otherwise. A raw report only sees this year's records. The published impact figures use rollover, so a raw Salesforce report will not match them, and that's expected.
- **Timing.** Tableau's daily refresh, or new Leads not yet verified.
- **Raw rows versus a modeled number.** Tableau excludes test accounts and applies the shared rules.

So when you quote a number, say how you got it:

> ✅ "2,950 students in confirmed adoptions (OpenStax or Third Party Confirmed), school year 2026 - 27, rollover off, from the Adoptions Dashboard as of November 9."

> ❌ "About 3,000 students use Anatomy and Physiology 2e."

For official impact figures, point to OpenStax's published numbers rather than repeating a total from memory. They change.

## Asking for a new report

If nothing in the folders answers your question, ask the Data Intelligence team (see [Getting Help]({{ '/modules/19-getting-help/' | relative_url }})). A good request has three parts about the data and three about you:

1. **What** you want to see: "A count of Contacts."
2. **Grouped** how: "By school and Adoption Status."
3. **Filtered** how: "For the 2026 - 27 school year, higher education only."
4. **Who** will use it: just you, your team, everyone.
5. **How often**: once, or on a regular schedule.
6. **By when**: a date, with some lead time.

<div class="callout callout-blue" markdown="1">
**Good to know:** Before asking for something new, try adding or removing one filter on an existing trusted report. Often that's all the "new report" needed.
</div>
