---
number: 21
part: 5
title: "Glossary"
short_title: "Glossary"
description: "Plain-language definitions of the terms you will meet in Salesforce at OpenStax, with a link to the chapter that explains each."
key_points:
  - "Terms are listed A to Z. Each links to the chapter that covers it in more depth."
  - "Look for the label you see on screen, not the technical name behind it."
  - "Can't find a term? Ask in #data-intel, and we'll add it."
---

Short definitions for the terms you'll hear in meetings and see on screen. Each entry points to the chapter that covers it properly. Use your browser's find (Ctrl + F, or Cmd + F on a Mac) to jump to a term.

## A

**Account.** A school, district, partner, or other organization. Most Accounts are schools. A district is the parent of its schools. See [Records, Objects, and Fields]({{ '/modules/02-records-objects-fields/' | relative_url }}).

**Adoption.** One instructor using one book at one school in one school year. Adoption records hang below a Book Opp. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**Adoption Status.** A Contact field that says whether the person is using a book now: Current Adopter, Past Adopter, Not Adopter, or an "Assumed" version of the first two. It's calculated, not typed. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

**AI FV.** Short for the "AI Faculty Verification" fields on a Lead. An AI assistant reviews a hard-to-verify signup first and writes a recommendation and summary. The AI advises, and a person decides. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**Assignable.** OpenStax's paid homework and assignment platform, which runs inside a school's learning management system. See [Assignable in Salesforce]({{ '/modules/13-assignable-in-salesforce/' | relative_url }}).

**Assignable Fit Tier.** A school-level rating (A, B, C, Nurture, Out) of how good a match the school is for Assignable, with a plain-language reason. It refreshes every night. See [Assignable in Salesforce]({{ '/modules/13-assignable-in-salesforce/' | relative_url }}).

## B

**Book Opp.** An Opportunity of record type Book Opp: one instructor and one book, over the long term. Automation sets its stage from that year's Adoptions. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

## C

**Campaign.** A goal and an audience, such as a semester engagement push. Campaigns come in four tiers. See [Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }}).

**Campaign Influence.** Multi-touch credit across the campaigns a person interacted with. It's how marketing attribution works, and it is thin for book adoptions today. See [Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }}).

**Campaign Member.** A person (Lead or Contact) attached to a Campaign, with a status such as Sent, Opened, Clicked, or Registered. See [Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }}).

**Case.** A support request, handled in the Service app. About 10,000 arrive each year. See [Support and Cases]({{ '/modules/16-support-and-cases/' | relative_url }}).

**Champion.** The top Instructor Engagement Tier: a current adopter for three or more years who has engaged in the last 180 days. Also a role on an Opportunity. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

**Comp.** Course access with the student payment waived, approved through an approval flow. See [Assignable in Salesforce]({{ '/modules/13-assignable-in-salesforce/' | relative_url }}).

**Confirmation Type.** How we know about an adoption: OpenStax Confirmed, Third Party Confirmed, or User Behavior Informed. Only the first two count as confirmed. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**Contact.** A confirmed person, with a record type such as Faculty, Donor, Partner, or General. People we haven't confirmed are Leads. See [Records, Objects, and Fields]({{ '/modules/02-records-objects-fields/' | relative_url }}).

**Critsit.** A checkbox on a Case for a rare "critical situation" that needs cross-team attention right away. See [Support and Cases]({{ '/modules/16-support-and-cases/' | relative_url }}).

**CX.** Customer Experience, the support team. See [Support and Cases]({{ '/modules/16-support-and-cases/' | relative_url }}).

## D

**DATA board.** The Jira board where bigger data and Salesforce requests go. There's a request form. See [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}).

**Data Intelligence team.** The team that runs Salesforce, Account Engagement, and Tableau. Start with them in #data-intel. See [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}).

**Data Office Hours.** Open help sessions on the first Wednesday of each month, recorded and posted in #data-intel. See [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}).

**Do Not Email.** The opt-out setting on a person's record. Account Engagement won't email anyone who has it. Check both their Lead and their Contact. See [Account Engagement]({{ '/modules/15-account-engagement/' | relative_url }}).

## E

**Engagement Tier.** The Instructor Engagement Tier on a Contact, from 1 Champion to 8 No Signal. It summarizes how engaged someone is overall, and has nothing to do with permission to email. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

**Explore folder.** The report folder where anyone can save their own work, including copies made with Save As. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).

## F

**Find Me A Home.** The placeholder school given to a Lead when automation can't match a real one. A person in the SDR Queue picks the right school. This is by design. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**FV / FV Status.** Faculty Verification, and the field that tracks it: pending, confirmed faculty, rejected faculty, plus SheerID expired or error. Confirmed faculty get instructor resources. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

## G

**Grace Period.** An Assignable Access value for students who enrolled before a comp was approved. Later students show "Free." See [Assignable in Salesforce]({{ '/modules/13-assignable-in-salesforce/' | relative_url }}).

## H

**HE / K12.** Higher education and K-12, OpenStax's two main markets. K12 users usually say "teacher" where HE says "faculty." See [The Shared Brain]({{ '/modules/01-the-shared-brain/' | relative_url }}).

## I

**Individual.** The one consent record per person, shared by their Lead and Contact. See [Account Engagement]({{ '/modules/15-account-engagement/' | relative_url }}).

## K

**KIP.** Key Institutional Partner: a school in OpenStax's institutional partner program. The KIP checkbox and KIP Start Year sit on the school's Account. See [Records, Objects, and Fields]({{ '/modules/02-records-objects-fields/' | relative_url }}).

## L

**Lapsed.** A Book Opp stage: confirmed in an earlier school year, not yet this year. Not lost; the instructor may well return. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**Last Engagement Date.** The most recent sign of life from a person: marketing activity, a Case, a confirmed adoption, a campaign response, or an email open. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

**Lead.** A person who isn't confirmed yet, usually a new instructor who just signed up on openstax.org. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**Lifecycle Stage.** A bucket (New, Nurturing, MQL, SQL) based on the Pardot score. It's a score bucket, not a sales judgment. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

**List View.** A saved, filtered list of records on an object's tab. List View, then Record, then Related Record is how you move around. See [Finding Things]({{ '/modules/06-finding-things/' | relative_url }}).

## M

**MCAE / Pardot / Account Engagement.** Three names for one product: OpenStax's marketing email and automation tool, two-way synced with Salesforce. See [Account Engagement]({{ '/modules/15-account-engagement/' | relative_url }}).

**Merged Lead.** A Lead whose details were folded into an existing Contact, so no duplicate is created. Its status is Merged. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**Mission Makers.** OpenStax's donors and supporters. Their data is restricted: share counts and totals, never rows. See [Handle With Care]({{ '/modules/18-handle-with-care/' | relative_url }}).

**MQL.** Marketing Qualified Lead, a Lifecycle Stage reached by a higher Pardot score. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

## O

**Omni-Channel.** The Service app feature that routes incoming work (Cases, chats, calls) to available agents. See [Support and Cases]({{ '/modules/16-support-and-cases/' | relative_url }}).

**Opportunity.** A record that tracks something moving toward an outcome. At OpenStax, several record types: Book Opp, Assignable Instructor, Institutional, Donation, and others. See [Records, Objects, and Fields]({{ '/modules/02-records-objects-fields/' | relative_url }}).

## R

**Record Type.** A setting on a record that decides which fields, stages, and layouts it uses, such as Faculty versus Donor Contacts. See [Records, Objects, and Fields]({{ '/modules/02-records-objects-fields/' | relative_url }}).

**Renewal.** The yearly email that asks past adopters to confirm they're still using a book. A confirmation creates a fresh Adoption. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**Rollover.** A counting rule in Tableau that assumes a confirmed adoption continues until there's evidence otherwise. Headline impact numbers use it, and raw reports don't. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).

## S

**Save As.** The report action that makes your own copy. Use it before changing anything shared. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).

**School Year.** July 1 to June 30, matching the fiscal year. Written "2026 - 27" in Salesforce, with spaces. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**SDR.** Sales Development Rep. The role that works new instructor Leads. Until the role is filled, CX works the queue. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**SDR Priority Tier.** A rating on each Lead: 1 Verification waiting, 2 Hot intent, 3 Finish the match, 4 Warm, 5 Cold list, or Hold. It comes with a plain-language reason. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**SDR Queue.** The one queue of open instructor Leads that need a person. Work the "SDR Queue: by priority" list view top-down. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**SheerID.** The service that automatically checks whether a new signup is a real instructor. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**Signup Date.** The date someone signed up on openstax.org. Use it, not Created Date, to count signups. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

**StaxSupport.** The internal name for the AI chat assistant that answers from verified help content and hands off to a person. See [Support and Cases]({{ '/modules/16-support-and-cases/' | relative_url }}).

**Subject Interest.** A multi-select field for what a person teaches or cares about. See [Reading a Contact]({{ '/modules/11-reading-a-contact/' | relative_url }}).

## T

**Tableau.** The tool that holds OpenStax's KPI, adoption, Assignable, support, and pipeline dashboards. It refreshes daily. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).

**Third Party Confirmed Adoption.** An adoption confirmed by an outside source, such as bookstore, courseware, or partner data. It counts as confirmed. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**Tier 1-4 campaigns.** The four campaign levels: program anchor, occasion anchor, season instance, and channel execution (where forms, members, and attribution live). See [Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }}).

**Trusted Numbers.** The ★ report folder of curated reports with shared definitions. Open and read, and use Save As to change anything. See [Reports, Dashboards, and Tableau]({{ '/modules/17-reports-dashboards-and-tableau/' | relative_url }}).

## U

**User Behavior Informed Adoption.** An "assumed" adoption inferred from signals like downloads. It has no student count and $0 savings, and doesn't count as confirmed. See [Adoptions]({{ '/modules/12-adoptions-and-impact/' | relative_url }}).

**UTM.** Tags added to links from outside sites to openstax.org so analytics can tell where visitors came from. Never tag links within openstax.org. See [Campaigns and Attribution]({{ '/modules/14-campaigns-and-attribution/' | relative_url }}).

## V

**Verify.** The guided screen flow a reviewer uses to approve or reject a faculty verification. See [From Signup to Contact]({{ '/modules/10-from-signup-to-contact/' | relative_url }}).

## W

**Winter '27.** Salesforce's October 2026 release, one of three each year. See [Getting Help]({{ '/modules/19-getting-help/' | relative_url }}).
