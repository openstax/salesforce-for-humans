---
number: 3
title: "The Map — Finding Your Way Around"
short_title: "The Map"
description: "Apps, navigation, Global Search, and the pattern that unlocks the entire interface."
---

The first time you open Salesforce, the interface can feel like walking into a building with no directory. Tabs, icons, a search bar, sidebars, related lists — it's a lot. This module is the orientation session.

### Apps: Different Views of the Same Data

Salesforce uses the concept of **Apps** to organize the interface for different roles and workflows. An App is not a separate system. It's a curated set of tabs, objects, and pages tailored for a specific type of work. The support team's Service Console shows Cases, Knowledge Articles, and Omni-Channel routing. A sales-focused app might surface Opportunities, Accounts, and pipeline views. A marketing app centers on Campaigns and Lead management.

You switch between Apps using the **App Launcher** (the grid icon in the top-left corner). Think of it as choosing which lens you want to look through. The data underneath is all the same — you're just choosing which parts of it to foreground.

![The App Launcher — click the grid icon in the top-left corner to switch between Apps like Sales Console, Service Console, and Marketing. Same data, different view for each team.]({{ '/assets/images/app-launcher.svg' | relative_url }})

### The Navigation Bar

The horizontal bar at the top of the screen is your primary navigation. It shows the tabs available in your current App. You can customize this bar by clicking the pencil icon: add tabs you use frequently, remove ones you don't, and reorder them so the things you reach for most are front and center.

This is one of the simplest and most impactful things you can do in your first week. Spend five minutes customizing your nav bar. Future you will be grateful.

![The navigation bar shows your current App's tabs. The green underline marks your active tab. Click the pencil icon on the right to add, remove, and reorder tabs to match your daily workflow.]({{ '/assets/images/navigation-bar.svg' | relative_url }})

### Global Search

The search bar at the top of every page is **Global Search**. Type a name, an email address, an institution name, or a case number and Salesforce will search across all objects you have access to.

A few things to know about search:
- **It works best with complete terms.** Searching for "Houston Community" will find Houston Community College. Searching for "Houst" might not.
- **You can scope your search** by clicking the dropdown next to the search bar and selecting a specific object. If you know you're looking for a Contact, scoping the search to Contacts gives you faster, more relevant results.
- **Recently viewed records** appear below the search bar as you click into it. Salesforce remembers what you've looked at recently, which is surprisingly useful for getting back to something you were working on.

![Global Search with a scoped search for Contacts matching "Houston Community." The dropdown on the left lets you narrow results to a single object. Recently viewed records appear as you click into the search bar.]({{ '/assets/images/global-search.svg' | relative_url }})

### Home Page

The Home tab is your landing page when you log in. It typically shows a dashboard, your open tasks, and recent records. It's configurable by your admin, so what you see may differ from what a colleague sees depending on your role.

![The Home page shows dashboard components with key metrics, your open tasks, and a list of recently viewed records for quick access. Your admin configures the layout for your role.]({{ '/assets/images/home-page.svg' | relative_url }})

### The Pattern That Unlocks Everything

Once you navigate to an object (say, Accounts), you're looking at a **List View**: a filtered table of records. Click any record and you're on the **Record Page**: a detailed view of one specific record with all its fields, related records, and activity history. Click a related record and you're on *that* record's page.

That's the whole navigation model: **List → Record → Related Record**. Every object works this way. Once the pattern clicks, you can navigate any corner of Salesforce without a map.

![The navigation pattern that works everywhere: start from a List View (a filtered table of records), click a row to open the Record Page (full detail view with fields and related lists), then click a related record to navigate deeper. List → Record → Related Record. Every object, every time.]({{ '/assets/images/list-record-related.svg' | relative_url }})
