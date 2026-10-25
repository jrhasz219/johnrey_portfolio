# Portfolio progress: John Rey S. Santos

> **Start of every new chat, say:** "Read PROGRESS.md in jrhasz219/johnrey_portfolio and continue with the next step."
> Update this file at the end of every session.

## NEXT STEP
**Section 2: About + Skills.** Content is in "Content bank" below. Add it inside `<main>` in `index.html` where the `NEXT SECTIONS GO HERE` comment is. Reuse the tokens in `styles.css` (`:root`) and the existing classes.

## Plan (one section per session)
- [x] 1. Hero / summary intro (header, name, role, summary, tool chips, CTA buttons, decorative chart card, 3-stat strip, footer)
- [ ] 2. About + Skills (grouped skills)
- [ ] 3. Experience (timeline)
- [ ] 4. Contact (+ education)
- [ ] 5. Polish: nav links to new sections, meta/OG, accessibility check, turn on GitHub Pages
- [ ] 6. Put the live URL on the resume
- [ ] Optional: sample project/dashboard showcase (needs real or anonymized examples from John Rey), Figma version

## Repo and hosting
- Repo: https://github.com/jrhasz219/johnrey_portfolio (branch `main`, plain HTML/CSS, no build step)
- Planned URL after GitHub Pages is on: https://jrhasz219.github.io/johnrey_portfolio/
- To turn on Pages: repo Settings > Pages > Source "Deploy from a branch" > `main` / `(root)` > Save. Not done yet.

## Files
- `index.html`: page markup, one `<section>` per portfolio section
- `styles.css`: design tokens at the top (`:root`), then base, then one block per section
- `assets/fonts/`: self-hosted woff2 fonts (no external requests)

## Design decisions (keep consistent)
- **Feel:** modern minimalist, tech / data-analyst, white background, lots of space
- **Colours (tokens):** white `--bg #fff`; turquoise `--turquoise #14b8a6`, `--turquoise-deep #0b8f87` (use for text); blue `--blue #2f6bff`, `--blue-deep #1d4ed8`; sky `#7dd3fc`; tiny warm accent `--sand #ffd9a8` (sparingly); ink `--ink #0c2233`, `--ink-soft #4a6275`; washes `--surface #f4fbfb`, `--surface-2 #eef4ff`; hairlines `--line #dcebec`
- **Fonts:** Cormorant Garamond *italic* 500/600 for display (name, big numbers, logo; this carries the calligraphy feel) / Inter 400-600 for body / JetBrains Mono for small labels, chips, code-style details
- **Gradient:** turquoise to blue, used on the surname, the primary button and chart only
- **Voice:** first person, plain, no invented numbers. Stats must come from the resume.
- **Motion:** gentle fade-up and chart draw-in; all wrapped in `prefers-reduced-motion`
- **Code-flavoured touches:** `// comment` eyebrow, `report.sql` card, mono chips. Repeat sparingly (e.g. `// skills`, `// experience` as section eyebrows).
- Light theme only. Mobile first-class (checked at 390px and 1280px).

## Privacy choices
- Phone number is **not** on the site (public page). Only email + LinkedIn.
- Resume PDF is **not** in the repo (contains phone). If a download button is wanted, use a version without the phone number.

## Content bank (from the resume)
**Name:** John Rey S. Santos
**Titles:** Reports Analyst | Data Analyst | Power BI & Data Visualization
**Headline tools:** SQL, Power BI, DAX, Power Query, Excel
**Location:** Quezon City, Philippines
**Email:** 19jrsantos@gmail.com
**LinkedIn:** https://linkedin.com/in/john-rey-santos-777926136

**Professional summary:** Reports and Data Analyst skilled in developing reliable dashboards, recurring and ad hoc reports, and actionable analysis to support operational decision-making. Proficient in SQL, Power BI (DAX and Power Query), Excel, Amazon QuickSight, and Looker Studio, with experience working across SQL Server, Amazon Redshift, and Google BigQuery. Brings a detail-oriented approach to data validation, reconciliation, and reporting automation, along with the ability to translate stakeholder needs into clear, dependable reporting solutions and collaborate effectively across teams.

**Technical skills**
- Data Visualization & BI: Power BI Desktop, Power BI Report Server (PBIRS), DAX, Amazon QuickSight, Looker Studio
- Databases & Querying: SQL, Microsoft SQL Server, SSMS, Amazon Redshift, Google BigQuery
- Data Preparation & Analysis: Microsoft Excel, Power Query, Data Cleaning, Data Transformation, Data Validation, Data Quality
- Reporting: Operational Reporting, Ad Hoc Reporting, Dashboard Development, Report Automation, Requirements Gathering
- Interaction Analytics: CallMiner, Vocci V-Spark, Nexidia
- Professional: Troubleshooting, Root Cause Analysis, Stakeholder Communication, Cross-functional Collaboration

**Experience (all at ResultsCX)**
- **Ops Reporting Analyst**, Feb 2021 - Present
  - Build and maintain recurring and ad hoc operational reports using SQL, Excel, Power Query, and BI tools to support informed business decisions
  - Develop and maintain dashboards in Power BI, Amazon QuickSight, and Looker Studio
  - Consolidate and analyze data from multiple systems, databases, and spreadsheets to deliver consistent reporting
  - Validate, cleanse, and reconcile data, applying quality checks to maintain accurate and reliable reports
  - Automate repetitive reporting tasks to improve efficiency and reduce manual effort
  - Gather stakeholder requirements and translate business needs into practical, actionable reporting solutions
  - Investigate data and reporting discrepancies, troubleshoot issues, and identify root causes
  - Collaborate with cross-functional teams to deliver accurate, timely reporting and analytical support
- **Interaction Analytics Analyst**, Feb 2017 - Feb 2021
  - Analyze recorded customer interactions using CallMiner, Vocci V-Spark, and Nexidia to identify trends, topics, behaviors, and opportunities for process improvement
  - Prepare analytical reports and communicate insights that support operational and customer experience initiatives
  - Develop recommendations from customer interaction data to support process improvements and customer satisfaction
  - Collaborate with stakeholders to define analytical requirements and deliver relevant insights
- **Earlier roles**, Aug 2012 - Feb 2017: Sprint Fulfillment Exception Desk Analyst (Feb 2015 - Feb 2017), Tier 3 Backoffice Analyst (Nov 2013 - Feb 2015), Customer Service Representative (Aug 2012 - Nov 2013). Progressed through customer service, back-office, Tier 3 escalation, and fulfillment operations, handling complex cases, troubleshooting, coordinating resolutions, and maintaining accurate documentation.

**Education:** Saint Louis University, Philippines. Bachelor of Science in Human Resources Development Management, 2007 - 2012

## Session log
- **Session 1:** Built Section 1 (hero/summary). Self-hosted fonts. Checked at desktop and mobile widths. Pushed to `main`. GitHub Pages not enabled yet.
