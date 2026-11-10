---
number: 6
part: 2
title: "Finding Things: Search and List Views"
short_title: "Finding Things"
description: "Global Search for a specific record, list views for your daily work, and a routine experienced users follow."
key_points:
  - "Use **Global Search** when you know what you're looking for. An email address is the best search key."
  - "Use a **list view** when you work through a group of records. Build your own in a few minutes."
  - "Inline editing fixes a field right in the list, with no page load."
  - "**Recently Viewed** gets you back to what you had open a minute ago."
redirect_from:
  - /modules/07-finding-things/
---

With around 110,000 Accounts and hundreds of thousands of people in Salesforce, scrolling is not a plan. This module covers the two ways to find things (search and list views) and the habits that make both fast. You've already seen how to move between records in [Finding Your Way Around]({{ '/modules/05-finding-your-way-around/' | relative_url }}).

## Global Search

The search box at the top of every page looks across the objects you can see. Use it when you have something specific: a name, a school, a Case number, an email address.

- **Email is the best key.** Almost nobody shares an email address, so it finds one person and not four.
- **Use whole words.** "Cedar Bluff" finds Cedar Bluff Community College. "Ced Blu" may not.
- **Scope it.** The dropdown at the left of the box narrows the search to one object. Searching "Rivera" in Contacts returns people. Searching it everywhere also returns Cases and Campaigns that mention her.
- **Click into the box before you type.** Your recently viewed records show up right there.

![Global Search scoped to Contacts with the text "Cedar Bluff", showing recently viewed records below the box.]({{ '/assets/images/global-search.svg' | relative_url }})

Search covers records you're allowed to see, so an empty result doesn't always mean the record doesn't exist. Try the email address or the school before you create anything new (see [Keeping Data Clean]({{ '/modules/08-keeping-data-clean/' | relative_url }})).

## List views

A **list view** is a saved filter on one object, with the columns you chose. Search finds one record. A list view is for the days when you work through a group: your schools, this week's open Cases, instructors waiting on verification.

Several already exist. The SDR Queue has "SDR Queue: by priority", and CX has views for Cases. Build your own for anything you check regularly.

### Build one

1. Open the tab for the object, such as Accounts.
2. Click the list view dropdown (the name at the top left) and choose **New**.
3. Name it for what it shows: "My A/B Fit Schools", not "My View". Choose who can see it, usually just you.
4. Click **Save**, then open **Filters**. Set **Filter by Owner** to *My accounts*.
5. Add filters. For this one: **Assignable Fit Tier** is A or B. To limit it to Canvas schools, add **LMS** equals Canvas.
6. Use the gear menu, then **Select Fields to Display**, to choose columns. Add LMS and Assignable Fit Tier so you can see why each school is there.
7. Save. It's now one click from the dropdown, any day.

![A list view called My A/B Fit Schools with three active filters, three columns, and an inline edit in progress.]({{ '/assets/images/list-view-builder.svg' | relative_url }})

Other filters worth knowing: on Contacts, **Adoption Status** and **Instructor Engagement Tier** (see [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }})); on Leads, **SDR Priority Tier**. Filter text has to match exactly, so a school year is written "2026 - 27", with spaces.

### Fix things in place

Spot a blank LMS in the list? Click the pencil that appears at the right edge of the cell (or double-click the cell), type, and save. Nothing else opens. Fields the system calculates, such as a Contact's Instructor Engagement Tier, won't offer the pencil, and fields automation fills (like Assignable Fit Tier) shouldn't be edited even when they do.

## Recently Viewed

Salesforce remembers what you opened. The records appear when you click into Global Search, and the **Recently Viewed** list view is on each object's tab. When you're three records deep and lose the thread, start there.

## How experienced users find things

| You want to... | Start with |
|---|---|
| Work through your regular group of records | Your own list view |
| Find one person or school | Global Search, with an email if you have one |
| See what's connected to a record | Its related lists, then click through |
| Get back to what you just had | Recently Viewed |
| Get a number or a trend | A report, not a list view ([Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }})) |

<div class="callout callout-green" markdown="1">
**Try it:** Build one list view today for something you check at least weekly. Filter by owner, add one or two filters, choose your columns, and save it.
</div>

<div class="callout callout-blue" markdown="1">
**Good to know:** A list view isn't a report. It shows rows on one object, and it's shared only the way you choose. If you're about to export it, read [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}) first.
</div>
