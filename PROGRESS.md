# Portfolio progress: John Rey S. Santos

> **Start of every new chat, say:** "Read PROGRESS.md in jrhasz219/johnrey_portfolio and continue with the next step."
> Update this file at the end of every session. Session log is newest first.

## NEXT STEP
**Step 6: put the live URL on the resume:** https://jrhasz219.github.io/johnrey_portfolio/ (the resume itself is not in the repo; John Rey updates it, or shares a copy without the phone number for help).

After that, the optional items (see Plan): the **Projects section** (on hold until John Rey has his Power BI screenshots) and a Figma version.

All four content sections, the polish step and an accessibility audit are DONE. The site is considered finished apart from the items above.

## Plan
- [x] 1. Hero / summary intro (logo + nav header, name, role, summary, tool chips, LinkedIn button, decorative chart card, 2-stat strip, footer)
- [x] 2. About + Skills (grouped skills)
- [x] 3. Experience (timeline)
- [x] 4. Contact (centred card: email as plain text + LinkedIn button; education was removed on request)
- [x] 5. Polish (header nav, canonical/og:url/twitter card, AA-contrast turquoise, axe audit clean at 1280px and 390px, heading order OK)
- [ ] 6. Put the live URL on the resume
- [ ] Optional: **Projects section** (ON HOLD until John Rey has his Power BI screenshots ready), Figma version
  - Plan agreed (session 7): new `#projects` section between Skills and Experience, eyebrow `// projects`, add "Projects" to the header nav. One card per project: screenshot, short title, one line on what it does, tools as chips (reuse `.chips` and the `.skill-card` style). `index.html` has a `FUTURE` comment marking the spot.
  - Power BI reports cannot run inside this plain HTML site. Use screenshots (or a short GIF/video). A link button only if the report is publicly viewable (Publish to web exposes it to anyone with the link).
  - Privacy: reports from ResultsCX may hold company or customer data. John Rey must anonymize (blur names/figures/branding) or use sample data, and confirm he is allowed to show them.
  - Needed from him: PNG/JPG screenshots plus 1-2 sentences per project. Do not invent descriptions or numbers.
  - Put images in `assets/projects/`, compress them, give each meaningful `alt` text.

## Repo and hosting
- Repo: https://github.com/jrhasz219/johnrey_portfolio (branch `main`, plain HTML/CSS, no build step)
- **Live URL (GitHub Pages is ON, deploys from `main` / root):** https://jrhasz219.github.io/johnrey_portfolio/
- Every push to `main` updates the live site after about a minute. The Actions "pages build and deployment" run should show Success.
- If an automated fetch (from the sandbox) shows an old page, that is a stale cache on the fetching side; ask the user to hard refresh (Ctrl+Shift+R).
- **Cache busting:** `index.html` links `styles.css?v=NN`. **Bump NN every time `styles.css` changes** (currently `v=11`) so visitors never see stale CSS.

## Files
- `index.html`: page markup, one `<section>` per portfolio section (`#top` hero, `#about`, `#skills`, `#experience`, `#contact`), plus a small inline script at the end (see Behaviour)
- `styles.css`: design tokens at the top (`:root`), then base, then one block per section. Shared pieces: `.section`, `.section-head`, `.chips`, `.btn`, `.btn-primary`
- `assets/fonts/`: self-hosted woff2 fonts (no external requests)
- `assets/deco/`: three subtle geometric line-art SVGs (`deco-a|b|c.svg`) used as section background decoration via `::after`
- `README.md`: one-paragraph description and link to this file

## Behaviour (keep)
- Page always opens at the intro: inline script sets `history.scrollRestoration = "manual"`, strips any `#hash` on load and scrolls to top. Header links smooth-scroll without writing a hash to the URL (a hash used to make a refresh jump to that section).
- Header nav: About, Skills, Experience, Contact; stays on one row down to 320px.
- Sticky header is 68px; `.section` has `scroll-margin-top: 68px`.

## Design decisions (keep consistent)
- **Feel:** modern minimalist, tech / data-analyst, white background, lots of space, subtle geometric line art in section corners. **No dot grid** (removed on request).
- **Colours (tokens):** white `--bg #fff`; turquoise `--turquoise #14b8a6`, `--turquoise-deep #0a7a73` (use for text; AA on white); blue `--blue #2f6bff`, `--blue-deep #1d4ed8`; sky `#7dd3fc`; tiny warm accent `--sand #ffd9a8` (sparingly); ink `--ink #0c2233`, `--ink-soft #4a6275`; washes `--surface #f4fbfb`, `--surface-2 #eef4ff`; hairlines `--line #dcebec`
- **Fonts:** Cormorant Garamond *italic* 500/600 for display (name, headings, big numbers, logo; this carries the calligraphy feel) / Inter 400-600 for body / JetBrains Mono for small labels, chips, code-style details
- **Gradient:** turquoise to blue, used on the surname, the accent word in each section heading, the primary button and the chart
- **Voice:** first person, plain, no invented numbers. Stats must come from the resume.
- **Experience wording:** never write "14 years" or "14+" as a number. Do not use "Since 2012" in headings or stats (removed from the intro stat and the Experience heading on request). The 2012 start year still appears in the About text and the timeline dates.
- **Buttons:** no empty or placeholder buttons. Only add a button if it links somewhere real. LinkedIn is the only button (hero and contact).
- **Motion:** gentle fade-up and chart draw-in; all wrapped in `prefers-reduced-motion`
- **Code-flavoured touches:** `// comment` eyebrow, `report.sql` card, mono chips. Repeat sparingly (`// about`, `// skills`, `// experience`, `// contact` as section eyebrows).
- Light theme only. Mobile first-class (checked at 390px, 320px for the nav, and 1280px).
- Accessibility: axe-core audit clean; headings h1 > h2 > h3; LinkedIn links labelled "opens in a new tab"; skip link; visible focus states.

## Privacy choices
- Phone number is **not** on the site (public page).
- Location on the site is shown as "NCR, Philippines" (user's choice), not Quezon City.
- Email **is shown** as plain text, NOT a link (user's decision): 19jrsantos@gmail.com in the Contact section.
- **Education is not on the site** (removed on request). It is still in the Content bank and on the resume.
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

## Session log (newest first)
- **Session 11:** Experience heading changed from "Since 2012, in operations and reporting" to "From operations to reporting" (no year, on request). HTML only, so the stylesheet version stays `v=11`.
- **Session 10:** Review and finalize. Rewrote this file (fixed outdated details: stat count, education, old step-5 notes, dot-grid mentions; sessions now newest first; added Behaviour and cache-busting notes). Removed unused `.btn-outline` CSS, fixed two stale HTML comments, wrote `README.md`, bumped `styles.css?v=11`. Final checks run (axe, overflow at 1280/390, hash/refresh test). Nothing else outstanding.
- **Session 9:** Contact alignment pass. User's screenshot showed the OLD CSS (full-width, left-aligned card) because the browser had cached `styles.css`; added a version query on the stylesheet link. Contact section tightened (less padding, card max 640px, centred), footer text centred. Checked at 1280/390.
- **Session 8:** Removed the "Since 2012" stat from the at-a-glance strip (now 2 stats: 3 BI tools, 3 data platforms; grid is 2 columns). Removed the Education card from Contact. Contact became a single centred card. Experience heading still says "Since 2012" (user only asked to change the Intro). Checked at 1280/390.
- **Session 7b:** Removed the body dot grid at the user's request; the geometric line art per section stays.
- **Session 7 (iterations):** (1) Page always opens at the intro (see Behaviour). (2) Contact: removed the "Send an email" button; email is plain text with no mailto link anywhere. (3) Subtle tech background: a faint dot grid (later removed, see 7b) plus one geometric line-art SVG per section (`assets/deco/`), placed with `::after` at section edges, low opacity, dimmer on mobile. `.skills` / `.contact` washes were made translucent. Also agreed the Projects section plan (see Plan). Tested at 1280/390: no overflow.
- **Session 6:** Polish finished. An earlier session hit its usage limit midway through Polish and left uncommitted nav/meta/contrast edits; reviewed, tested nav at 1280/390/320px, committed (a20f87a). Ran axe-core: only issue was the Education card being an `aside` inside `main` (card since removed). LinkedIn links now have an accessible name saying they open in a new tab. Headings go h1 > h2 > h3 in order.
- **Session 5:** Built Section 4 (Contact + Education; both later reworked in sessions 7-9, so the details of that first version no longer apply). Live-site check: an automated fetch showed only the hero although `origin/main` had all sections. **Resolved:** the user confirmed Settings > Pages (main / root) and the Actions run succeeded, so the deploy was fine and the stale view was on the fetching side.
- **Session 4:** Built Section 3. `#experience`: vertical timeline (date + company column, rail with nodes, role content), three entries from the resume: Ops Reporting Analyst (Feb 2021 - Present), Interaction Analytics Analyst (Feb 2017 - Feb 2021), Earlier roles (Aug 2012 - Feb 2017, with the three earlier titles as chips with dates). Bullets are the resume bullets as written. Heading: "Since 2012, in operations and reporting". Under 760px the rail moves to the left edge and dates sit above each role. Fixed date ranges wrapping mid-date inside the earlier-role chips on mobile. Company shown as ResultsCX on all three entries per the Content bank.
- **Session 3:** Built Section 2. `#about`: heading left, two paragraphs right plus a 2x2 "how I work" grid (requirements, validation, automation, root cause), all taken from the resume. `#skills`: six grouped cards with chips, 3 columns on desktop, 2 on tablet, 1 on mobile. Added shared `.section` / `.section-head` / `.chips` styles. Fixed "know-how" splitting at the hyphen (`white-space: nowrap` on the heading accent).
- **Session 2 (iteration on Section 1):** Removed the "say hello" header button and the "Get in touch" button. LinkedIn is now the single primary (gradient) button. Location changed to "NCR, Philippines". First stat changed from "14 years" to "Since 2012". Removed the unused `.nav-link` and `.btn-ghost` CSS. Confirmed GitHub Pages is live.
- **Session 1:** Built Section 1 (hero/summary). Self-hosted fonts. Checked at desktop and mobile widths. Pushed to `main`.
