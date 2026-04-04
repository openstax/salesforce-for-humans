---
number: 9
title: "Campaigns, Attribution, and Why Marketing Keeps Asking You to Update Things"
short_title: "Campaigns & Attribution"
description: "How OpenStax tracks marketing efforts, measures attribution, and why accurate campaign data matters."
---

A **Campaign** in Salesforce represents any trackable marketing effort. At OpenStax, that includes seasonal email pushes (like the Back to School campaigns that go out twice a year), webinars (tracked with registration and attendance data from ON24), conference booths, paid media, landing pages, and ongoing newsletter programs.

### The Hierarchy

OpenStax Campaigns are organized as a hierarchy. A top-level parent Campaign like "Back to School Spring" acts as a container for an entire marketing program. Nested underneath are child campaigns for each specific effort: HE adoption emails, K-12 outreach, print channel pushes, brand awareness, subject-specific campaigns, and partner co-marketing.

This hierarchy is the marketing team's organizational structure. The parent campaign shows the aggregate reach and impact of the whole program. The child campaigns show the individual executions and their specific performance.

### Campaign Members: The People Layer

A **Campaign Member** is a junction record connecting a person (Contact or Lead) to a Campaign. Their **status** tells the engagement story: were they sent an email? Did they open it? Did they click a link? Did they register for the webinar? Did they attend live or watch the recording?

This is where things connect to you, even if you're not on the marketing team.

When OpenStax needs to understand whether a marketing effort led to textbook adoptions, the evidence trail runs through Campaign Members. An instructor was sent an email (Campaign Member status: Sent). They opened it (status: Opened). Two weeks later, they submitted an adoption form. That adoption gets attributed to the campaign. If the statuses don't get updated, or the person was never added to the campaign, that attribution trail goes cold.

If you're in a role where you interact with educators, whether through sales conversations, support calls, or event attendance, and someone asks you to "make sure these contacts are on the campaign," this is why. Campaign attribution data is how the marketing team proves that their work leads to outcomes, and how leadership decides where to invest resources next.

### Why Personalization Depends on This Data

The data captured through Campaigns and engagement tracking feeds personalization across the organization. Marketing uses engagement scores and campaign history to segment audiences, sending different messages to someone who attended a webinar versus someone who's never interacted with an email. The openstax.org web experience uses adoption and engagement data to surface relevant content and resources. Support agents see campaign history on Contact records, giving them context about what outreach the person has received.

All of this personalization runs on the same data. Clean campaign data means better targeting, better personalization, and fewer "why did I get this email?" complaints. Messy campaign data means everyone gets the same generic experience.

