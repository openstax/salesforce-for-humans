---
number: 5
title: "How Everything Connects — The Relationship Model"
short_title: "How Everything Connects"
description: "The relationship web that connects Accounts, Contacts, Opportunities, Cases, and Campaigns."
---

This is the module that separates "I know where things are in Salesforce" from "I understand how Salesforce works."

Salesforce isn't just a collection of independent records. It's a *web of relationships* between them. Every record connects to other records, and those connections tell a story that no single record can tell alone.

### The OpenStax Relationship Web

Let's trace the connections starting from a single Account record: **Central Arizona College**.

Central Arizona College is an Account. That Account has **Contacts**: the faculty members who teach there. One of those Contacts, let's call her Dr. Rivera, has an **Opportunity** of type "Book Opp" tracking her adoption of Anatomy & Physiology 2e. That Opportunity has child **Adoption** records for each school year she's used the book, tracking how many students she reached and how much money they saved.

Dr. Rivera also has **Campaign Member** records showing that she received two back-to-school emails and attended a webinar on OpenStax resources. She submitted a **Case** last September asking about instructor resource access, which was resolved the same day. Her Contact record shows a Pardot engagement score of 45 and a lifecycle stage of "Nurturing."

Meanwhile, the Account record for Central Arizona College shows that the institution uses Canvas as its LMS, has an undergraduate enrollment in the mid-thousands, and is located in a rural setting. Three other Contacts (other faculty) are also linked to this Account, each with their own adoption histories and engagement profiles.

![The OpenStax relationship web: Central Arizona College (Account) connects to Contacts like Dr. Rivera, who connects to Opportunities and Adoptions tracking her textbook usage. Cases and Campaigns also link to both the Account and Contact. Every team sees a different slice of the same connected data.]({{ '/assets/images/relationship-web.svg' | relative_url }})

That's the power of the relationship model. One pull on the thread and the whole picture emerges: who teaches where, what they've adopted, how engaged they are, what support they've needed, and what marketing they've seen. Every team at OpenStax benefits from a different slice of this picture:

- **Support** opens the Contact record during a call and instantly sees the person's institution, their adoption history, and any prior cases
- **Sales** looks at the Account and sees which books are already adopted, who the key contacts are, and whether there's Assignable pipeline activity
- **Marketing** filters Contacts by engagement score, adoption status, and institution type to build targeted campaign audiences
- **The web experience** uses data from Salesforce to personalize what an educator sees when they log into openstax.org — showing them relevant resources, renewal prompts, and Assignable options based on their actual adoption history
- **Leadership** aggregates all of it into mission impact numbers, pipeline forecasts, and strategic planning

### Parent-Child Relationships

Most relationships in Salesforce follow a parent-child pattern. An Account is the parent; its Contacts are children. An Opportunity is the parent; its Adoptions are children. A Campaign is the parent; its Campaign Members are children.

When you're on a record page and you see **related lists** at the bottom, you're looking at the children (or sometimes the parents and siblings) of that record. These aren't just decorative. They're the navigation paths through the relationship web. Clicking a related Contact on an Account takes you to that Contact's full record, where you can see *their* related records, and so on.

### Why This Matters for Your Daily Work

When you create or update a record, you're not just editing a row in a table. You're modifying a node in a connected web. If you update an email address on a Contact, that change is visible to every team that interacts with that Contact, and it syncs to Account Engagement within minutes. If you tag a Case with the right product and issue classification, that data feeds support analytics that inform product decisions. If you log an activity note with real context, the next person who opens that record walks in informed instead of blind.

The relationship model is the reason Salesforce is more than a fancy database. It's why a single update can ripple across support, sales, marketing, and strategy. And it's why accuracy matters: every connection in the web is only as good as the data at each node.

