---
number: 8
title: "Reading the Numbers — Reports and Dashboards"
short_title: "Reports & Dashboards"
description: "How to read a report, interpret a dashboard, and ask for the data you actually need."
---

At OpenStax, data drives decisions at every level. The adoption numbers that appear on the website come from Salesforce. The pipeline forecasts that inform staffing decisions are Salesforce reports. The support case trends that guide product improvements are built on Case data. The marketing campaign performance reviewed in team meetings comes from Campaign and engagement records.

If you interact with any of these numbers — and you almost certainly do — understanding how to read a report and interpret a dashboard makes you a more effective participant in every conversation where data comes up.

### Anatomy of a Report

A Salesforce report is a structured query of data, presented as a table with optional groupings, summaries, and charts. When you open a report, you'll see:

- **Columns** showing the fields included in the report (names, dates, statuses, amounts, etc.)
- **Groupings** that organize the rows by a shared value (grouped by institution, by book, by school year, by campaign)
- **Summary rows** that calculate totals, averages, or counts for each group
- **Filters** at the top that control which records are included (date ranges, statuses, record types)

The most useful thing you can learn is how to **modify the filters** on an existing report to answer your specific question. Your team lead built a report showing all adoptions for the current year. You want to see just your territory. Click the filter panel, add a filter for your state or territory, and run the report. You're now looking at a customized view of the same data without changing the original report for everyone else.

![Anatomy of a report: filters at the top control which records are included, columns show the fields, groupings organize rows by institution, and summary rows calculate totals for each group. Modify existing filters to answer your specific question.]({{ '/assets/images/report-anatomy.svg' | relative_url }})

### Dashboards: The Visual Layer

A dashboard is a collection of visual components — bar charts, pie charts, gauges, tables, single-number metrics — each powered by an underlying report. Dashboards are designed for quick consumption: glance at the numbers, spot anything unusual, drill into the details if something catches your eye.

**Drilling down** is key. Almost every dashboard component is clickable. If a bar chart shows that Assignable cases spiked last month, click that bar to see the underlying report with every individual case listed. Dashboards are the surface; reports are the depth.

![A dashboard with metric numbers, bar charts, pie charts, and data tables — each powered by an underlying report. Click any component to drill into the full report. The sidebar shows the three-part formula for requesting a new report.]({{ '/assets/images/dashboard-layout.svg' | relative_url }})

### How to Ask for a New Report

When you need data that doesn't exist in a current report, the quality of your request determines how quickly you get what you need.

**A well-framed request has three parts:**
1. **What you want to see:** "I need a count of Contacts"
2. **How you want it grouped:** "...grouped by institution and adoption status"
3. **How you want it filtered:** "...for the current school year, in the Higher Ed market"

That gives your admin or data team everything they need to build it in minutes. Compare that with "can you pull me some adoption data?" which requires a round of follow-up questions before anyone can start building.

