# Portfolio progress: John Rey S. Santos

> **Start of every new chat, say:** "Read PROGRESS.md in jrhasz219/johnrey_portfolio and continue with the next step."
> Update this file at the end of every session.

## NEXT STEP
**Step 5: Polish.** All content sections exist. Do: (a) add nav links in the header (About, Skills, Experience, Contact; the header currently has only the logo; keep it clean on mobile, e.g. hide or collapse the links under ~640px), (b) meta/OG (add `og:url`, consider an OG image only if the user supplies one), (c) accessibility check (headings order, contrast, focus states, link names, reduced motion). The live site deploys fine (Actions run for 6162bd5 succeeded, Pages set to main / root). If an automated fetch shows only the hero, that is a stale cache on the fetching side, not a deploy problem; ask the user to hard refresh instead.

## Plan (one section per session)
- [x] 1. Hero / summary intro (header with logo only, name, role, summary, tool chips, LinkedIn button, decorative chart card, 3-stat strip, footer). Iterated once after review (see session log).
- [x] 2. About + Skills (grouped skills)
- [x] 3. Experience (timeline)
- [x] 4. Contact (+ education)
- [~] 5. Polish (nav links, og:url/canonical/twitter card, darker --turquoise-deep for AA contrast DONE; accessibility pass still to do): nav links to new sections (header currently has only the logo; add links once the sections exist), meta/OG, accessibility check
- [ ] 6. Put the live URL on the resume
- [ ] Optional: sample project/dashboard showcase (needs real or anonymized examples from John Rey), Figma version

## Repo and hosting
- Repo: https://github.com/jrhasz219/johnrey_portfolio (branch `main`, plain HTML/CSS, no build step)
- **Live URL (GitHub Pages is ON, deploys from `main` / root):** https://jrhasz219.github.io/johnrey_portfolio/
- Every push to `main` updates the live site after about a minute.

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
- **Experience wording:** never write "14 years" or "14+" as a number. Imply it with "Since 2012" (user's request).
- **Buttons:** no empty or placeholder buttons. Only add a button if it links somewhere real.
- **Motion:** gentle fade-up and chart draw-in; all wrapped in `prefers-reduced-motion`
- **Code-flavoured touches:** `// comment` eyebrow, `report.sql` card, mono chips. Repeat sparingly (e.g. `// skills`, `// experience` as section eyebrows).
- Light theme only. Mobile first-class (checked at 390px and 1280px).

## Privacy choices
- Phone number is **not** on the site (public page).
- Location on the site is shown as "NCR, Philippines" (user's choice), not Quezon City.
- Email **is shown** (user's decision, session 5): 19jrsantos@gmail.com as a mailto link in the Contact section. Phone stays off the site.
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
- **Session 1:** Built Section 1 (hero/summary). Self-hosted fonts. Checked at desktop and mobile widths. Pushed to `main`.
- **Session 5:** Built Section 4. `#contact`: heading "Let's connect", a contact card (short lead, email as mono mailto link, "Send an email" primary button, LinkedIn outline button, "// NCR, Philippines") and an Education card (Saint Louis University, BS Human Resources Development Management, 2007 - 2012, Philippines). Added `.btn-outline`. Stacks to one column under 860px. Checked at 1280px and 390px: no horizontal overflow. **Live-site issue:** fetching https://jrhasz219.github.io/johnrey_portfolio/ (twice, second with a cache-busting query) returned only the hero, with no About/Skills/Experience, although `origin/main` contains them (commit b422c41 verified). The Pages build status could not be read from the sandbox (GitHub API blocked). **Resolved:** the user confirmed Settings > Pages (main / root) and the Actions run for 6162bd5 succeeded, so the deploy is fine and the stale view was on the fetching side.
- **Session 4:** Built Section 3. `#experience`: vertical timeline (date + company column, rail with nodes, role content), three entries from the resume: Ops Reporting Analyst (Feb 2021 - Present), Interaction Analytics Analyst (Feb 2017 - Feb 2021), Earlier roles (Aug 2012 - Feb 2017, with the three earlier titles as chips with dates). Bullets are the resume bullets as written. Heading: "Since 2012, in operations and reporting". Under 760px the rail moves to the left edge and dates sit above each role. Checked at 1280px and 390px: no horizontal overflow. Fixed date ranges wrapping mid-date inside the earlier-role chips on mobile (nowrap, dates on their own line). Company shown as ResultsCX on all three entries per the Content bank.
- **Session 3:** Built Section 2. `#about`: heading left, two paragraphs right (career path from 2012, interaction analytics 2017-2021, Ops Reporting since 2021) plus a 2x2 "how I work" grid (requirements, validation, automation, root cause), all taken from the resume. `#skills`: six grouped cards (the six groups in the Content bank) with chips, 3 columns on desktop, 2 on tablet, 1 on mobile. Added shared `.section` / `.section-head` / `.chips` styles to reuse. `.section` has `scroll-margin-top: 68px` for the sticky header. Checked at 1280px and 390px: no horizontal overflow. Fixed "know-how" splitting at the hyphen (`white-space: nowrap` on the heading accent). No nav links yet (Section 5).
- **Session 2 (iteration on Section 1):** Removed the "say hello" header button and the "Get in touch" button. LinkedIn is now the single primary (gradient) button. Location changed to "NCR, Philippines". First stat changed from "14 years" to "Since 2012". Removed the unused `.nav-link` and `.btn-ghost` CSS. Confirmed GitHub Pages is live.
