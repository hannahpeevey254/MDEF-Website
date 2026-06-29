# ★ ★ MDEF Fabrication ★ ★

---

## ★ System Architecture[¶](#system-architecture "Permanent link")

<div style="border:2px solid black; margin:24px 0;">
  <div style="background:#c8d400; padding:8px 16px; font-weight:bold; font-size:12px; letter-spacing:0.08em;">FIND YOUR MATCH AT ELISAVA · SYSTEM ARCHITECTURE · HOW IT WAS BUILT</div>
  <div style="display:grid; grid-template-columns:1fr 1fr 1fr 1fr; border-top:2px solid black;">
    <div style="border-right:2px solid black; padding:16px;">
      <div style="font-weight:bold; font-size:11px; letter-spacing:0.08em; border-bottom:1px solid black; padding-bottom:6px; margin-bottom:12px;">USER LAYER</div>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>TALLY FORM</strong><br>tally.so/r/xXlz2E<br>20 questions total<br>Q1–Q15 scored<br>Q17–Q20 filler</p>
      <p style="font-size:12px; font-family:monospace; margin:0;"><strong>PARTICIPANT</strong><br>Name + Email<br>Instagram handle<br>Gender identity<br>Sexuality</p>
    </div>
    <div style="border-right:2px solid black; padding:16px;">
      <div style="font-weight:bold; font-size:11px; letter-spacing:0.08em; border-bottom:1px solid black; padding-bottom:6px; margin-bottom:12px;">BACKEND</div>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>WEBHOOK</strong><br>/api/webhook/route.js<br>Receives Tally POST<br>Resolves UUID → text<br>Runs scoring algo</p>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>SCORING ENGINE</strong><br>scoringConfig.js<br>15 Qs × 7 buyers<br>105 Q/A entries</p>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>MATCHING ALGO</strong><br>/api/matching<br>Hard filter: gender+sex<br>Tier 1: Q17–20 ×3<br>Tier 2: Q5–11 ×2</p>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>EMAIL ROUTE</strong><br>/api/email/route.js<br>Resend provider<br>"Your match is waiting"</p>
      <p style="font-size:12px; font-family:monospace; margin:0;"><strong>ADMIN UI</strong><br>/admin/matching<br>Runs locally only<br>Review + confirm pairs<br>Trigger email send</p>
    </div>
    <div style="border-right:2px solid black; padding:16px;">
      <div style="font-weight:bold; font-size:11px; letter-spacing:0.08em; border-bottom:1px solid black; padding-bottom:6px; margin-bottom:12px;">DATABASE</div>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>SUPABASE</strong><br>participants table<br>responses table<br>scores table<br>matching_data table</p>
      <p style="font-size:12px; font-family:monospace; margin:0;"><strong>NEXT.JS</strong><br>App Router<br>Vercel deploy<br>PowerShell / VS Code<br>GitHub: hannahpeevey254</p>
    </div>
    <div style="padding:16px;">
      <div style="font-weight:bold; font-size:11px; letter-spacing:0.08em; border-bottom:1px solid black; padding-bottom:6px; margin-bottom:12px;">DISPLAY</div>
      <p style="font-size:12px; font-family:monospace; margin:0 0 10px 0;"><strong>STOCK MARKET</strong><br>/market<br>Candlestick bars<br>7 buyer categories<br>Live participant data</p>
      <p style="font-size:12px; font-family:monospace; margin:0;"><strong>PROFILE REVEAL</strong><br>/profile/[id]<br>3-column CCTV layout<br>Buyer scores exposed<br>Data body aesthetic</p>
    </div>
  </div>
  <div style="border-top:2px solid black; padding:12px 16px;">
    <div style="font-weight:bold; font-size:11px; letter-spacing:0.08em; margin-bottom:10px;">7 DATA BUYERS · SCORING WEIGHTS</div>
    <div style="display:flex; gap:8px; flex-wrap:wrap;">
      <span style="background:#8B0000; color:white; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">PHARMA €50</span>
      <span style="background:#1a1a2e; color:white; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">GOVT €40</span>
      <span style="background:#b5e550; color:black; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">BIG TECH €30</span>
      <span style="background:#e8a020; color:black; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">INSUR. €20</span>
      <span style="background:#6abf69; color:black; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">BEHAV. €10</span>
      <span style="background:#6b6b2a; color:white; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">EMPLOY. €7</span>
      <span style="background:#1565c0; color:white; padding:6px 12px; font-size:12px; font-weight:bold; font-family:monospace;">IDENTITY €2</span>
    </div>
  </div>
</div>

---

## ★ Data Flow[¶](#data-flow "Permanent link")

<div style="border:2px solid black; margin:24px 0;">
  <div style="background:#c8d400; padding:8px 16px; font-weight:bold; font-size:12px; letter-spacing:0.08em;">DATA FLOW · FORM TO REVEAL · HOW PARTICIPANT DATA BECOMES A COMMODITY</div>
  <div style="display:grid; grid-template-columns:repeat(7,1fr); border-top:2px solid black;">
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">01</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>PARTICIPANT FILLS FORM</strong><br><br>Thinks it's a dating app</p>
    </div>
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">02</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>TALLY WEBHOOK</strong><br><br>POST to /api/webhook</p>
    </div>
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">03</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>SCORING ENGINE</strong><br><br>15 Qs × 7 buyer categories</p>
    </div>
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">04</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>SUPABASE DB WRITE</strong><br><br>participants + scores tables</p>
    </div>
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">05</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>ADMIN MATCHING</strong><br><br>3-tier weighted algorithm runs</p>
    </div>
    <div style="border-right:2px solid black; padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">06</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>EMAIL SENT</strong><br><br>Resend via /api/email</p>
    </div>
    <div style="padding:12px; text-align:center;">
      <div style="background:black; color:white; font-weight:bold; font-size:11px; padding:4px 6px; margin-bottom:8px;">07</div>
      <p style="font-size:11px; font-family:monospace; margin:0;"><strong>THE REVEAL</strong><br><br>Profile + Market shown publicly</p>
    </div>
  </div>
</div>

![](..images/)

<img src="../images/MDEF FEST PHOTO2.jpeg" style="width:80%; height:auto; border-radius:6px;">

---

## ★ The Story[¶](#the-story "Permanent link")

**What the Project Is.**

Find Your Match at Elisava is a speculative design installation disguised as a blind dating experience. It uses the social mechanics of a dating app — the curiosity, the intimacy, the desire for connection — as a delivery mechanism for a gut-punch about data surveillance. Participants believed they were submitting personal information to find a romantic match at a student festival. What they were actually doing was voluntarily handing over a biometric and behavioral dataset that got assigned a monetary value and traded publicly on a live stock market, in front of them, without them realizing it until they were already standing in the room.

The gap between what they came for and what they found is the work.

**Where It Comes From.**

This project is the middle act of a three-part research arc examining the lifecycle of personal data. The first project, Mochi, explored the relationship between data, the body, and ownership. The third, Safe Hands, will examine data as post-mortem inheritance — what happens to your data body after you die. Find Your Match sits between them at the moment of extraction: the point at which personal data leaves the body and enters the market.

The direct predecessor is the Biometric Stock Market, a live data visualization installation built in the 2024/25 academic year. That project identified six core data types collected by everyday apps — screentime, GPS location, heart rate, pedometer and movement data, calendar entries, and menstrual tracking — and mapped each one outward to four institutional buyers: tech companies, governments, insurance companies, and employers. It then traced seven feedback loops in which these data types combine and compound to produce something far more invasive than any single input: a complete digital twin of a person. Their body, their behaviour, their vulnerabilities, their economic risk profile, their emotional calendar.

The key finding from that diagram was that data types are not equal in value. Health, behavioral, and intimate data sits at the top of the hierarchy and commands the highest market rates. Basic demographic information sits at the bottom. This hierarchy became the conceptual and mathematical engine for Find Your Match. The shift from the Biometric Stock Market to this project is a shift in stakes. In the earlier piece, the shock came from seeing friends' data commodified. In this version, the shock is personal and immediate: the participant is the data point. They did not know they signed up for this. They thought they were looking for love.

**The Research Behind the Valuation System.**

The valuation system is built entirely on documented, evidence-based research into what real data types are actually worth to real institutional buyers. The hierarchy was sourced from FTC reports, investigative journalism, academic research, and documented data broker pricing. None of the numbers are speculative.

Pharma and Health Tech sits at the top of the hierarchy with an estimated rate of 50 to 500 euros per individual health record. Companies like Pfizer spend 12 million dollars per year purchasing health data. One accurate health data point informs multi-billion dollar drug pipeline decisions. In the installation, every answer that mapped to this category was worth 50 euros on the market.

Government and Law Enforcement sits second, with documented purchases of 476,000 dollars per location dataset. The NSA was confirmed in January 2024 to be buying Americans' internet browsing records directly from data brokers. No other buyer uses data to directly deprive people of their liberty. Each government-mapped answer was worth 40 euros.

Big Tech and Advertising sits third. Meta's 2023 revenue of 134.9 billion dollars was 97 percent advertising-derived. The volume is the highest of any buyer but the per-point rate is lower because the data is commoditized at scale. Each big tech answer was worth 30 euros.

Insurance Companies sit fourth at 0.08 to 50 dollars per data point. Allstate's subsidiary Arity paid mobile apps millions to install tracking software purely for insurance pricing. Each insurance-mapped answer was worth 20 euros.

Behavioral and Psychological Modeling sits fifth. Researcher Joanna Moll purchased one million online dating profiles for under 150 dollars — including sexual orientation, physical characteristics, and personality traits — to study the psychographic data embedded in relationship behavior answers. Each behavioral answer was worth 10 euros.

Employers and HR sits sixth. HireRight alone generated 722 million dollars in revenue in 2023 from employer background screening. 95 percent of US employers conduct background checks. Each employer-mapped answer was worth 7 euros.

Identity and Social Class Profiling sits at the bottom. Acxiom charges approximately 0.05 dollars per consumer profile and holds data on hundreds of millions of people globally. Each identity-mapped answer was worth 2 euros.

**How the Form Was Designed.**

The entry point was a QR code placed around the Elisava campus bearing a single line: Find your match at Elisava. No explanation, no branding. Ambiguity does the work. Curiosity is the hook.

Participants were taken to a 23-question form built in Tally that looked and felt exactly like a dating app questionnaire — warm, personal, designed to lower the guard. Four unscored baseline questions collected name, gender identity, sexuality, and course of study. Fifteen scored questions each contained seven answer options, one per institutional buyer. The question itself was entirely neutral — the data signal lived in the answer chosen, not in the question asked. Four filler questions maintained the dating app disguise and fed the matching algorithm. One multi-select exception on substance use allowed up to three simultaneous answers, each routing to a different buyer.

The form was designed so the most intimate, honest answers produced the highest market value — because those are the answers the real market pays most for.

**How the Technical System Was Built.**

The entire system was built from scratch as a Next.js web application, deployed on Vercel, with Supabase as the Postgres backend. The scoring configuration file — scoringConfig.js — is the most important file in the project: a complete map of every question, every answer, and which buyer column each routes to. Before any real participant touched the system, seven synthetic test users were injected directly into Supabase — one maximizing each buyer column — to verify the scoring engine.

When a participant submitted the form, Tally fired a webhook POST to the receiver endpoint. The handler verified the request, extracted the submission, ran the scoring engine, computed the total, identified the dominant buyer, generated a five-digit anonymous market ID, and wrote four simultaneous inserts to Supabase: participants, responses, scores, and matching_data. The participant received no confirmation. From their perspective they had submitted a form. On the backend they were now a priced data asset in a live database.

The live stock market display used a candlestick-style visualization — a format that reads immediately as financial infrastructure to anyone walking past. Seven colors, one per buyer category. The admin matching page ran a three-tier algorithm: filler questions at 3× weighting (worthless to buyers, most meaningful for human connection), personality and relationship questions at 2×, remaining scored questions at 1×. Receipts were generated by a standalone Python script using ReportLab, producing 16 thermal-printer-style PDFs for the physical folders.

**The Physical Installation.**

The installation ran on 18 June 2026 in Room 314 at Elisava, 14:30–16:30, as part of MDEF Fest. 16 real participants had been processed through the full pipeline in the weeks before the event. 12 synthetic test users were deleted before the event opened so the live market showed only real data.

The space held a table with physical folders — one per participant, face up, showing only their anonymous ID and euro value on the exterior. Inside: the Question Design Key, a thermal-style receipt showing their full buyer breakdown, and a match card with the name of the person they had been matched with.

Two screens ran simultaneously: the live candlestick stock market at /market, and the 3-column CCTV-aesthetic profile reveal cycling through participant data. Below the screens, printed on a long scroll mounted on the wall in the manner of Dima Yarovinsky's I Agree (2018), was the full Terms and Conditions document. The clause that disclosed what would happen to their data was buried in the middle of it, in the same small legal font as everything else. It was always there. They agreed to it. They just did not read it.

<img src="../images/MDEF FEST IMAGE 2 STOCK MARKET.png" style="width:80%; height:auto; border-radius:6px;">

<img src="../images/MDEF FEST IMAGE 3.jpg" style="width:80%; height:auto; border-radius:6px;">

> "You came looking for a date. We found 7 buyers for your data."

**Open Source.**

<https://github.com/hannahpeevey254/elisava-dating>

---

## ★ The Questions[¶](#the-questions "Permanent link")

Every scored question appeared as a standard dating app prompt. Every answer was pre-mapped to an institutional data buyer. Participants had no way of knowing which answer fed which category.

<div style="display:flex; gap:8px; flex-wrap:wrap; margin-bottom:20px;">
  <span style="background:#8B0000; color:white; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">PHARMA €50</span>
  <span style="background:#1a1a2e; color:white; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">GOVT €40</span>
  <span style="background:#b5e550; color:black; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">BIG TECH €30</span>
  <span style="background:#e8a020; color:black; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">INSURANCE €20</span>
  <span style="background:#6abf69; color:black; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">BEHAVIORAL €10</span>
  <span style="background:#6b6b2a; color:white; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">EMPLOYERS €7</span>
  <span style="background:#1565c0; color:white; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">IDENTITY €2</span>
  <span style="background:#555; color:white; padding:4px 10px; font-size:11px; font-weight:bold; font-family:monospace;">MATCHING DATA</span>
</div>

---

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q1 — Do you smoke, drink, or use drugs?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — Never, not my thing</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — I drink socially, nothing serious</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — I smoke but I'm trying to stop</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — I smoke and am not trying to stop</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — On the weekends only</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">F — Only in social situations</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Recreational drugs occasionally, nothing I'd call a habit</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q2 — The thing you find most attractive in a person is:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — How they treat strangers and people around them</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">B — Their ambition — knowing what they want</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — The feeling I get when I'm around them</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — That they actually take care of themselves</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — That they're easy to be around — no drama</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Their vibe — music, style, how they move</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">G — That they make me laugh</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q3 — On a Sunday morning you're more likely to be:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — At church or in some kind of spiritual practice</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — Hungover and piecing together last night</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — At a market or out for brunch</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — In bed recovering from the week</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — At the gym or on a run</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Working on something personal</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">G — Scrolling or watching something</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:#555; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q4 (MATCHING DATA) — You're most yourself when:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — You're with your close friends</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">B — You're alone</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — You're creating something</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — You're travelling somewhere new</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — You're in a good conversation</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — You're in love</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — You're not trying to impress anyone</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:#555; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q5 (MATCHING DATA) — Your love language is:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Physical touch</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Words of affirmation</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Quality time</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Acts of service</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Gifts — I'm not ashamed</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">I don't believe in love languages</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">All of them when I actually like someone</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q6 — How religious are you?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — It shapes every decision I make</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">B — It's a big part of my identity</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — I was raised in it and some of it stuck</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — Spiritual but not religious</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — I respect it but it's not part of my life</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — I've actively moved away from it</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">G — Not at all — never has been</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q7 — Your biggest problem with your ex was:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">A — They were emotionally unavailable</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — We wanted different things financially</div>
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — They didn't respect my independence</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — They were too focused on work or status</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — Long distance</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — We came from different worlds</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Our lifestyles just didn't match</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q8 — Your last relationship ended because:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — I ended it</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — They ended it</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — It was mutual</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — Life got in the way — timing, distance, circumstance</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — We grew into different people</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — It got toxic</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — I don't really want to talk about it</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q9 — When you like someone you: <em style="font-size:11px; font-weight:normal;">(multi-select — up to 3 answers)</em></div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — Text them immediately, no games</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — Wait and see if they make a move first</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — Post a story and hope they see it</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — Tell all my friends and feed into the delusion</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — Play it cool even though I'm not</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Manifest it and see what happens</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Make it obvious — life is too short</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q10 — What are you like when nobody is watching?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — Pretty much the same as when people are</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — More relaxed and less put together</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — Darker and more honest</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — Lazy in ways I'd never admit</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — On my phone way more than I'd like to admit</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — More emotional than anyone would guess</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Honestly kind of a different person</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q11 — The last thing that made you genuinely angry was:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — A political leader or government decision</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — A billionaire or corporation</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — A financial situation I couldn't control</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — Someone close to me</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — Something at school or work</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — An unfair situation I witnessed</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — My own body or health</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q12 — How often do you actually prioritise your health?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — I work out, sleep well, eat well</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — I'm pretty good about it most of the time</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — Mentally yes, physically not so much</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — I do my best but it's hard with school and social life</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — I need to be better at eating healthier and working out</div>
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Only when something actually goes wrong</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — I party more than I sleep and I'm fine with that</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q13 — Have you ever attended a protest?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — Yes, regularly</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — Yes, once or twice</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — No but I would</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — No and I wouldn't</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">E — I organise them</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — It depends what for</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — I've thought about it but haven't</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q14 — You'd describe your energy as:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — High and consistent</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — Good when I'm inspired, gone when I'm not</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — Depends entirely on my sleep</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — Fuelled by deadlines and pressure</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — Scattered</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Socially I'm great, alone I crash</div>
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Running on fumes but making it work</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q15 — In your ideal relationship, who takes care of what?</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">A — We split everything equally — 50/50</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — It shifts depending on who needs what</div>
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">C — We each do what we're naturally better at</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — Whoever earns more contributes more</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — We figure it out as we go — no rules</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — One person leads, the other supports</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Honestly I haven't thought that far ahead</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q16 — Success to you right now means:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">A — Financial stability</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">B — Creative freedom / doing work that's mine</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — Getting a job I actually want and building something real</div>
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">D — Having people who matter around me</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — Just being genuinely happy</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Feeling good in my body and mind</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Travelling and seeing the world</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:black; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q17 — Money is:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#e8a020; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">A — Security</div>
    <div style="background:#1a1a2e; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">B — Freedom</div>
    <div style="background:#6b6b2a; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">C — A game</div>
    <div style="background:#6abf69; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">D — Uncomfortable to talk about but always on my mind</div>
    <div style="background:#b5e550; color:black; padding:6px 10px; font-size:12px; font-family:monospace;">E — A tool, I need it but I don't worship it</div>
    <div style="background:#1565c0; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">F — Something I watched my family stress about</div>
    <div style="background:#8B0000; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">G — Something I need to understand better</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:#555; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q18 (MATCHING DATA) — The version of you on a first date is:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Nervous but funny</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Completely yourself</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Whoever they seem to need</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Calm and curious</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Oversharing within the first ten minutes</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Quieter than usual</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Honestly a little performative — everyone is</div>
  </div>
</div>

<div style="border:2px solid black; margin:16px 0;">
  <div style="background:#555; color:white; padding:8px 16px; font-weight:bold; font-size:12px; font-family:monospace;">Q19 (MATCHING DATA) — You can tell a lot about someone by:</div>
  <div style="padding:12px 16px; display:grid; grid-template-columns:1fr 1fr; gap:6px;">
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">How they treat waiters and service staff</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Their bookshelf or playlist</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">How they act when things go wrong</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Who they are with their family</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">What they're like when they're drunk</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">How they talk about their exes</div>
    <div style="background:#555; color:white; padding:6px 10px; font-size:12px; font-family:monospace;">Whether they're a morning or night person</div>
  </div>
</div>
