---
number: 7
title: "Finding Things — Search, List Views, and the Art of Filters"
short_title: "Finding Things"
description: "Global Search, List Views, and the daily habits that make finding data effortless."
---

You've been putting data in. Now let's talk about getting it back out efficiently.

Finding records in Salesforce is a daily activity, and there's a massive quality-of-life gap between people who know the search tools well and people who don't. This module covers the three tools that matter most: **Global Search**, **List Views**, and **Recently Viewed**.

### Global Search: When You Know What You're Looking For

Global Search (the bar at the top of every page) is your go-to when you have a specific name, email, institution, or record number in mind. Type it in, hit enter, and Salesforce searches across every object you have access to.

**Tips for better search results:**
- Use full terms rather than fragments. "Houston Community College" works better than "Houston Comm."
- Scope your search to a specific object when possible (click the dropdown). Searching for "Biology" across all objects returns books, adoptions, cases, and campaigns. Searching within Contacts returns people who teach biology.
- Email addresses are excellent search keys. If you have someone's email, search by that — it's the most unique identifier most people have.

### List Views: Your Most Powerful Daily Tool

A **List View** is a saved, filtered view of an object. Think of it as a custom window into a specific slice of the data. Instead of looking at every Account in the system, you can build a list view that shows "Accounts in My Territory with Active Adoptions" or "Contacts with Assignable Interest" or "Open Cases Created This Week."

List views are criminally underused. Most people stare at the default "Recently Viewed" or "All" views when they could have a curated set of views tailored to their daily work.

**Building a list view:**
1. Navigate to the object (e.g., Accounts)
2. Click the list view dropdown and select "New"
3. Give it a name (be descriptive — "My Texas HE Accounts" is better than "My View")
4. Add filters to narrow the records (State = TX, Type includes "College/University", etc.)
5. Choose which columns to display
6. Save — it's now one click away every time you need it

**Pro tip:** You can edit records directly from a list view using inline editing. Double-click a field in the list to edit it without opening the full record. This is a game changer for bulk updates.

![A custom list view with descriptive name, active filters narrowing to Texas HE accounts, and inline editing in action. The filter panel lets you slice the data; inline editing lets you update fields without opening each record.]({{ '/assets/images/list-view-builder.svg' | relative_url }})

### Recently Viewed: The "What Was I Just Looking At?" Safety Net

Salesforce tracks the records you've recently viewed, and surfaces them in the search bar dropdown and on each object's default list view. When you've been clicking through records and lose your place, Recently Viewed gets you back.

### Finding What You Need, Fast

The pattern for experienced users looks like this:

1. **Daily work:** Start from a custom List View tailored to your role
2. **Specific lookup:** Use Global Search with the person's name or email
3. **Following a thread:** Click through related lists on records to follow connections
4. **Lost your place:** Check Recently Viewed

Build two or three good list views in your first week. You'll use them every day.

