---
number: 6
title: "If It's Not in Salesforce, It Didn't Happen"
short_title: "If It's Not in Salesforce"
description: "Why logging your work matters, how to do it well, and what happens downstream when you do."
---

This module is about the most important habit you can build: logging your work.

At OpenStax, some channels do this automatically. When someone emails support@openstax.org, a Case is created and the full email thread is preserved. When a phone call comes in through Service Cloud Voice, the call is recorded and an AI-generated summary is attached to the Case. When Account Engagement sends a marketing email, the delivery and engagement data syncs back to the Campaign and the recipient's record.

But for everything that happens *between* the automated touchpoints — the conversations at conferences, the follow-up calls with instructors, the hallway chat where a colleague mentions that a school district is interested in Assignable — logging requires a human.

### What to Log

Salesforce offers several activity types:

- **Tasks** are to-do items or records of completed work. "Follow up with Dr. Chen about Assignable pilot" or "Called Central Arizona College re: spring adoption."
- **Events** are scheduled calendar items. "Meeting with Houston ISD curriculum team, March 15."
- **Log a Call** is a quick way to record a phone conversation. Who you talked to, when, and what was discussed.
- **Emails** can be logged automatically through the Outlook or Gmail sidebar integration, which captures sent and received emails directly onto the relevant Contact or Lead record.

### The Art of a Good Note

The difference between a useful activity log and a useless one is context. Compare these two:

> ❌ "Called Dr. Rivera"

> ✅ "Called Dr. Rivera at Central Arizona College. She's using A&P 2e for the third year, has 4 sections this spring. Interested in Assignable but needs to clear it with her department chair first. IT is supportive of the Canvas integration. Follow up mid-April after their curriculum committee meets."

The first version tells the next person that a call happened. The second version tells them *what to do next* and gives them the context to do it well. If Dr. Rivera calls support next week, the agent can see that she's a long-time adopter exploring Assignable. If a sales rep picks up the relationship, they know exactly where the conversation left off.

Writing good activity notes takes an extra minute. That minute saves hours of re-discovery later.

![Side-by-side comparison: a useless note that just says "Called Dr. Rivera" vs a detailed note with institution context, adoption details, interest level, and a clear follow-up action. The extra minute saves hours.]({{ '/assets/images/good-vs-bad-note.svg' | relative_url }})

### The Downstream Effect

Here's what happens when activities are logged consistently:

- **Support agents** can see the full interaction history before they pick up the phone, so the educator doesn't have to repeat themselves
- **Sales reps** can pick up relationships from colleagues without starting from scratch
- **Marketing** can see which contacts have been personally touched recently, avoiding tone-deaf outreach to someone who just had a detailed conversation with your team
- **Leadership** can see activity volume and patterns across the team, informing capacity planning and resource allocation
- **The data team** can analyze touchpoint patterns to understand which engagement sequences actually lead to adoptions

![One logged activity ripples to every team: Support sees full history, Sales picks up where you left off, Marketing avoids tone-deaf outreach, Leadership sees patterns. When activities aren't logged, everyone flies blind.]({{ '/assets/images/activity-downstream.svg' | relative_url }})

When activities *aren't* logged, all of that goes blind. The support agent walks into the call cold. The sales rep asks questions that were already answered. Marketing sends a generic email to someone who had a personal conversation yesterday. Leadership makes decisions based on incomplete information.

The hard truth: if it's not in Salesforce, it didn't happen — not because the work wasn't real, but because it's invisible to everyone else.

