---
number: 7
part: 2
title: "Logging Your Work: Activities, Notes, and Chatter"
short_title: "Logging Your Work"
description: "What Salesforce records on its own, what only a person can add, and how to leave a note the next person can use."
key_points:
  - "Case emails, chats, call summaries, and marketing email history are recorded automatically. Conversations and context are not."
  - "Log calls, emails, and meetings within 24 hours, and write down what happens next."
  - "An open Task means real work you own. Use Closed, no action when it's no longer needed."
  - "Use Chatter for record-specific context, Slack for quick talk, and email for people outside OpenStax."
redirect_from:
  - /modules/06-if-its-not-in-salesforce/
  - /modules/14-collaboration/
---

Some of what happens with an instructor lands in Salesforce without anyone lifting a finger. The rest only gets there if you put it there. This module sorts out which is which, then covers how to log the second kind well and where to talk about it.

## What happens automatically

| Source | What lands in Salesforce | Where |
|---|---|---|
| Email to support | The whole thread, kept on the Case | The Case |
| Chat | The transcript, plus any file the person uploads (such as verification proof) | The Case |
| Phone | A call recording and AI call summary (not every call becomes a Case) | The Case |
| Marketing email | Sends, opens, clicks, and unsubscribes | Account Engagement, shown on the person's record |
| Website forms | Signups, adoption and renewal forms, interest forms | Leads, Adoptions, and Tasks |

Case emails stay on the Case and no longer create Tasks. Marketing email history lives in Account Engagement and doesn't show up as Tasks either.

## What needs a person

The conversation at a conference. The call where Dr. Maya Rivera mentions her department chair is looking at Assignable. A colleague's hallway comment that a district is curious. No system hears these, so they exist only if you log them.

On a Contact, Lead, or Account, the activity actions are:

- **Log a Call** for a phone conversation. Record who, when, and what was said, and set the **Call Outcome**.
- **New Task** for work someone has to do, with a due date and an owner.
- **New Event** for a scheduled meeting.
- **Send Email** to email from Salesforce.
- **Notes** for context that doesn't fit the others.

Log calls, emails, and meetings within 24 hours, while you still remember the details. For emails you send from your own inbox, use your personal **Email to Salesforce** address: BCC it, and the email attaches to the matching records. You'll find the address in your personal Settings.

## Write a note someone else can use

The test is whether a colleague could pick up the relationship from your note alone.

> ❌ "Called Dr. Rivera"

> ✅ "Dr. Maya Rivera, Cedar Bluff Community College. Using *Anatomy and Physiology 2e*, four sections this spring. Interested in Assignable but needs her department chair's OK. Cedar Bluff uses Canvas and IT is supportive. Follow up mid-April, after the curriculum committee meets. If approved, offer an Assignable walkthrough."

The first note says a call happened. The second says what was learned and what to do next. If Dr. Rivera writes to support next week, the agent knows she's a long-time adopter weighing Assignable. If a new rep inherits Cedar Bluff, they don't start from zero.

![A one-line call note next to a detailed note about Dr. Maya Rivera, with the follow-up spelled out.]({{ '/assets/images/good-vs-bad-note.svg' | relative_url }})

![A logged call flows to Support, Sales, Marketing, and leadership, each of whom sees the history.]({{ '/assets/images/activity-downstream.svg' | relative_url }})

## Tasks mean real work

Since November 2026 an **open Task means real work you own**. Thousands of stale Tasks were cleared out, and the open list is now short enough to trust. A few habits keep it that way:

- Create a Task only when someone needs to do something.
- Finish it with status **Completed** if you did the work.
- If it's no longer needed, set **Closed, no action**. Don't mark it Completed to make it go away, since that tells everyone the work happened.
- Log calls with a **Call Outcome**. Tasks and Events also have a **Topic** field that helps reports group them.

## Email from Salesforce and unsubscribing

Sales and outreach emails sent from Salesforce must give the person a way to unsubscribe (that's the US CAN-SPAM rule). If someone replies "please stop emailing me", record it on their Contact and on their Lead if they have an open one. Consent is stored once per person, but Lead handling is older, so check both. Marketing email at scale goes through marketing, not through Salesforce.

## Chatter, Slack, or email

**Chatter** is the feed on every record. Post on an Account, @mention a colleague, and the conversation stays with that record. Automated "created a..." posts were cleared, so feeds now show what people wrote.

| Use | When |
|---|---|
| **Chatter** | Internal context about one record that someone may need later: "IT confirmed Canvas support; chair wants to wait until fall." |
| **Slack** | Quick questions and live coordination. Findings in a channel get buried within days. |
| **Email** | Anyone outside OpenStax, and anything formal. BCC your Email to Salesforce address to log it. |

![Slack, email, and Chatter compared by what each is best for and how long the context lasts.]({{ '/assets/images/slack-email-chatter.svg' | relative_url }})

You can also **follow** a record. Click Follow on the Account for a school you care about and its updates and posts appear in your feed.

<div class="callout callout-green" markdown="1">
**Try it:** Think of the last call you had that isn't in Salesforce. Log it now, with an outcome and a next step. It takes about two minutes.
</div>

<div class="callout callout-orange" markdown="1">
**Hands off:** Don't paste student or donor details into notes or Chatter. If something sensitive comes up in a call, write what you need to act on and leave the rest out. See [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}).
</div>
