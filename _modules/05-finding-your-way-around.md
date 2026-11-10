---
number: 5
part: 2
title: "Finding Your Way Around"
short_title: "Finding Your Way Around"
description: "Apps, the navigation bar, the Home page, and the one pattern that works on every object."
key_points:
  - "An **app** is a set of tabs and pages for one kind of work. The data underneath is the same in every app."
  - "Customize your navigation bar once and the tabs you use are always one click away."
  - "Your Home page is built for your role, and every component ends in something to do."
  - "Every object works the same way: List View, then Record, then Related Record."
redirect_from:
  - /modules/03-the-map/
---

Opening Salesforce for the first time can feel like walking into a building with no directory. This module is the directory. By the end you'll know which app to be in, how to set up your tabs, what your Home page is trying to tell you, and how to get from any list to any record.

## Apps: the same data through different windows

An **app** is a set of tabs and pages organized for one kind of work. It is not a separate system. Switch apps and you see the same Accounts, Contacts, and Cases, arranged differently.

Open the **App Launcher** (the nine-dot grid at the top left) to see the apps your role can use.

| App | Who uses it | What it's for |
|---|---|---|
| **OpenStax** | Most staff | Schools, people, opportunities, reports. The main app. |
| **Service** | Customer Experience (CX) | Cases, phone, chat, Knowledge. The support console. |
| **Finance** | Finance | Records and reports for the Finance team |
| **Philanthropy** | Fundraising | Donors and gifts (our Mission Makers) |
| **Campaigns** | Marketing | Campaign planning and membership |
| **Partner Manager** | Partnerships | Partner organizations |

Some teams also see **Pardot** (Account Engagement, our marketing email tool) or Sales. If an app you need isn't in your launcher, ask in #data-intel.

![The App Launcher open over the OpenStax app, listing OpenStax, Service, Finance, Philanthropy, Campaigns, and Partner Manager.]({{ '/assets/images/app-launcher.svg' | relative_url }})

## The navigation bar

The bar across the top shows the tabs for your current app. Click the pencil icon at the right end to add tabs you use, remove ones you don't, and drag them into the order you want. The change belongs to you and doesn't touch anyone else's view.

Five minutes of tidying in your first week saves you clicks for as long as you work here.

![The navigation bar for the OpenStax app, with the active tab underlined in green and the pencil icon that opens tab customization.]({{ '/assets/images/navigation-bar.svg' | relative_url }})

## Your Home page

Home is the first tab. What you see depends on your role, because the page is built from components and each team gets the ones that help it. You may see some or all of these:

- **SDR Queue: work next.** The instructor Leads that need a person, ordered by priority. The Sales Development Rep (SDR) and CX work from here.
- **My opportunities.** Your open opportunities, with what to do next for each.
- **School brief.** Pick a school and get a one-screen summary of it. Handy right before a call.
- **Home Funnels.** "This school year" views of the adoption and Assignable funnels.
- **Today's tasks**, recent items, and upcoming events.

The design rule is that every component ends in an action, in plain words. If a card tells you something and gives you nowhere to go with it, tell the Data Intelligence team in #data-intel.

![A Home page with SDR Queue, My opportunities, School brief, Home Funnels, and Today's tasks components.]({{ '/assets/images/home-page.svg' | relative_url }})

## List, Record, Related Record

Click a tab such as Accounts and you land on a **list view**: a table of records, filtered. Click a row and you open the **record page**, with every field, the related lists, and the activity history for that one thing. Click something in a related list and you're on that record's page.

That is the whole navigation model, and it works the same on every object. Start at Accounts, open Cedar Bluff Community College, click Dr. Maya Rivera in its Contacts list, and you're on her page. From there her Book Opps, Cases, and Tasks are one click each. The pattern also runs in reverse: Dr. Rivera's page links back to her school through the Account Name field.

![A list of schools, the Cedar Bluff Community College record page, and the Dr. Maya Rivera Contact reached through its related list.]({{ '/assets/images/list-record-related.svg' | relative_url }})

<div class="callout callout-green" markdown="1">
**Try it:** Open the App Launcher and look at which apps you have. Then click the pencil on your navigation bar and add the one tab you wish were there.
</div>

<div class="callout callout-blue" markdown="1">
**Good to know:** Schools sit in a hierarchy. A district is the parent of its schools, and some college systems are parents of their campuses. From a school's record, the Parent Account link takes you up a level. [Power User Moves]({{ '/modules/09-power-user-moves/' | relative_url }}) covers it.
</div>
