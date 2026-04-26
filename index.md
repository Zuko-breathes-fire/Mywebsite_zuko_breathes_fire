---
# Do not edit the text between these lines!
layout: default
---

<!DOCTYPE html>
<html lang="en">
<title>Does Prior Experience Shape How Hard COMP110 Feels? · COMP110 EX09</title>
<header>
  <p class="eyebrow fade-up">COMP 110 · EX09 · Course Improvement Analysis</p>
  <h1 class="fade-up">Does <em>Prior Experience</em> Shape<br>How Hard COMP110 Feels?</h1>
  <p class="subtitle fade-up">An analysis of anonymized COMP110 survey data · Spring 2026</p>
  <p class="subtitle fade-up" style="margin-top: 0.5rem; font-size: 0.9rem; opacity: 0.75;">
    Muhammad Khan &nbsp;&amp;&nbsp; Avi Tikoo
  </p>
</header>
<head>
<header>
  <p class="eyebrow fade-up">COMP 110 · EX09 · Course Improvement Analysis</p>
  <h1 class="fade-up">Does <em>Prior Experience</em> Shape<br>How Hard COMP110 Feels?</h1>
  <p class="subtitle fade-up">An analysis of anonymized COMP110 survey data · Spring 2026</p>
  <p class="subtitle fade-up" style="margin-top: 0.5rem; font-size: 0.9rem; opacity: 0.75;">Muhammad Khan &amp; Avi Tikoo</p>
</header>
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
  <style>
    /* ── Design tokens ─────────────────────────────────────────── */
    :root {
      --ink:       #0f0e0d;
      --paper:     #f6f3ee;
      --accent:    #c94b2b;
      --accent2:   #2b6cc9;
      --muted:     #7a7269;
      --rule:      #d9d4cc;
      --card-bg:   #ffffff;
      --mono:      'DM Mono', monospace;
      --serif:     'DM Serif Display', Georgia, serif;
      --sans:      'DM Sans', sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--paper);
      color: var(--ink);
      font-family: var(--sans);
      font-size: 17px;
      line-height: 1.72;
    }

    /* ── Header ─────────────────────────────────────────────────── */
    header {
      background: var(--ink);
      color: var(--paper);
      padding: 3.5rem 2rem 2.8rem;
      text-align: center;
      border-bottom: 5px solid var(--accent);
      position: relative;
      overflow: hidden;
    }
    header::before {
      content: "";
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        -45deg,
        transparent,
        transparent 18px,
        rgba(255,255,255,0.025) 18px,
        rgba(255,255,255,0.025) 19px
      );
      pointer-events: none;
    }
    .eyebrow {
      font-family: var(--mono);
      font-size: 0.72rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.75rem;
    }
    header h1 {
      font-family: var(--serif);
      font-size: clamp(2rem, 5vw, 3.4rem);
      line-height: 1.15;
      margin-bottom: 0.6rem;
    }
    header h1 em { color: var(--accent); font-style: italic; }
    .subtitle {
      font-size: 1rem;
      color: rgba(246,243,238,0.65);
      font-weight: 300;
    }

    /* ── Nav ─────────────────────────────────────────────────────── */
    nav {
      background: var(--card-bg);
      border-bottom: 1px solid var(--rule);
      display: flex;
      justify-content: center;
      gap: 0;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    nav a {
      font-family: var(--mono);
      font-size: 0.78rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      text-decoration: none;
      color: var(--muted);
      padding: 1rem 1.6rem;
      border-bottom: 3px solid transparent;
      transition: color 0.2s, border-color 0.2s;
    }
    nav a:hover { color: var(--accent); border-bottom-color: var(--accent); }

    /* ── Layout ─────────────────────────────────────────────────── */
    main { max-width: 860px; margin: 0 auto; padding: 0 1.5rem 5rem; }

    section { padding: 3.5rem 0 2rem; border-bottom: 1px solid var(--rule); }
    section:last-child { border-bottom: none; }

    .section-label {
      font-family: var(--mono);
      font-size: 0.68rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.5rem;
    }
    h2 {
      font-family: var(--serif);
      font-size: clamp(1.5rem, 3.5vw, 2.1rem);
      line-height: 1.2;
      margin-bottom: 1.1rem;
    }
    h3 {
      font-family: var(--serif);
      font-size: 1.25rem;
      margin: 1.8rem 0 0.5rem;
      color: var(--ink);
    }
    p { margin-bottom: 1rem; color: #2d2a26; font-weight: 300; }
    p strong { font-weight: 500; color: var(--ink); }

    /* ── Idea cards ─────────────────────────────────────────────── */
    .idea-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1rem;
      margin-top: 1.2rem;
    }
    .idea-card {
      background: var(--card-bg);
      border: 1px solid var(--rule);
      border-radius: 6px;
      padding: 1.2rem 1.3rem;
      border-left: 4px solid var(--accent2);
      transition: box-shadow 0.2s;
    }
    .idea-card:hover { box-shadow: 0 4px 18px rgba(0,0,0,0.07); }
    .idea-card .idea-num {
      font-family: var(--mono);
      font-size: 0.68rem;
      letter-spacing: 0.15em;
      color: var(--accent2);
      text-transform: uppercase;
      margin-bottom: 0.3rem;
    }
    .idea-card h4 { font-size: 0.97rem; font-weight: 500; margin-bottom: 0.3rem; }
    .idea-card .stakeholder {
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--muted);
    }
    .idea-card p { font-size: 0.88rem; margin-top: 0.45rem; margin-bottom: 0; }

    /* ── Highlighted box ─────────────────────────────────────────── */
    .callout {
      background: #fff8f5;
      border: 1px solid #f2d0c5;
      border-left: 4px solid var(--accent);
      border-radius: 6px;
      padding: 1.1rem 1.4rem;
      margin: 1.4rem 0;
      font-size: 0.95rem;
    }
    .callout strong { color: var(--accent); }

    /* ── Chart placeholders / real img ──────────────────────────── */
    .chart-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 1.4rem;
      margin: 1.8rem 0;
    }
    .chart-card {
      background: var(--card-bg);
      border: 1px solid var(--rule);
      border-radius: 8px;
      overflow: hidden;
    }
    .chart-card .chart-body {
      background: #fafafa;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 220px;
      padding: 1rem;
    }
    .chart-card .chart-body img {
      width: 100%;
      height: auto;
      display: block;
    }
    /* Placeholder when no image */
    .chart-placeholder {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      color: var(--muted);
      font-family: var(--mono);
      font-size: 0.78rem;
      text-align: center;
      min-height: 220px;
      padding: 1.5rem;
      background: repeating-linear-gradient(
        45deg,
        #f5f3f0,
        #f5f3f0 6px,
        #f0ede8 6px,
        #f0ede8 12px
      );
    }
    .chart-placeholder svg { opacity: 0.35; }
    .chart-footer {
      padding: 0.75rem 1rem;
      border-top: 1px solid var(--rule);
      font-size: 0.82rem;
      font-weight: 500;
      color: var(--muted);
    }

    /* ── Conclusion list ─────────────────────────────────────────── */
    ul.findings {
      list-style: none;
      padding: 0;
      margin: 1rem 0;
    }
    ul.findings li {
      display: flex;
      gap: 0.75rem;
      align-items: flex-start;
      padding: 0.55rem 0;
      border-bottom: 1px solid var(--rule);
      font-size: 0.95rem;
      font-weight: 300;
    }
    ul.findings li:last-child { border-bottom: none; }
    ul.findings li .dot {
      width: 8px; height: 8px;
      border-radius: 50%;
      background: var(--accent);
      flex-shrink: 0;
      margin-top: 0.55rem;
    }

    /* ── Footer ─────────────────────────────────────────────────── */
    footer {
      text-align: center;
      padding: 2rem 1rem;
      font-family: var(--mono);
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      color: var(--muted);
      border-top: 1px solid var(--rule);
    }

    /* ── Animations ─────────────────────────────────────────────── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(22px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .fade-up { animation: fadeUp 0.6s ease both; }
    header h1    { animation-delay: 0.05s; }
    .subtitle    { animation-delay: 0.15s; }
  </style>
</head>
<body>

<!-- ── Header ─────────────────────────────────────────────────────────────── -->
<header>
  <p class="eyebrow fade-up">COMP 110 · EX09 · Course Improvement Analysis</p>
  <h1 class="fade-up">Does <em>Prior Experience</em> Shape<br>How Hard COMP110 Feels?</h1>
  <p class="subtitle fade-up">An analysis of anonymized COMP110 survey data · Spring 2026</p>
</header>

<!-- ── Nav ─────────────────────────────────────────────────────────────────── -->
<nav>
  <a href="#ideas">Ideas</a>
  <a href="#missing">Missing Data</a>
  <a href="#analysis">Analysis</a>
  <a href="#conclusion">Conclusion</a>
</nav>

<main>

  <!-- ── Part 1: Ideation ──────────────────────────────────────────────────── -->
  <section id="ideas">
    <p class="section-label">Part 1 · Creative Ideation</p>
    <h2>Five Ideas for Improving COMP110</h2>
    <p>
      Each idea below targets a specific stakeholder group and identifies a concrete form of value the change could create.
    </p>

    <div class="idea-grid">
      <div class="idea-card">
        <p class="idea-num">Idea 01</p>
        <h4>Pre-Lecture Videos</h4>
        <p class="stakeholder">Stakeholder → Students</p>
        <p>Short optional videos before each class introduce vocabulary so students can engage more deeply during lecture.</p>
      </div>
      <div class="idea-card">
        <p class="idea-num">Idea 02</p>
        <h4>Livestream Lectures</h4>
        <p class="stakeholder">Stakeholder → Students</p>
        <p>Live-streaming removes attendance barriers for students with disabilities, commutes, or schedule conflicts.</p>
      </div>
      <div class="idea-card">
        <p class="idea-num">Idea 03</p>
        <h4>Expand Office Hours</h4>
        <p class="stakeholder">Stakeholder → Students & Instructional Staff</p>
        <p>If OH visits correlate with higher understanding, scaling TA hours could improve outcomes across the board.</p>
      </div>
      <div class="idea-card" style="border-left-color: var(--accent);">
        <p class="idea-num" style="color:var(--accent);">Idea 04 ★ Analyzed</p>
        <h4>Pre-Semester Bootcamp for Novices</h4>
        <p class="stakeholder">Stakeholder → Students & Academic Institution</p>
        <p>A zero-to-code async module before the semester could level the playing field for students with no prior experience.</p>
      </div>
      <div class="idea-card">
        <p class="idea-num">Idea 05</p>
        <h4>Interdisciplinary Project Modules</h4>
        <p class="stakeholder">Stakeholder → Students & Societal Workforce</p>
        <p>Project themes tied to students' primary majors (Bio, Economics, etc.) could increase perceived relevance of coding.</p>
      </div>
    </div>
  </section>

  <!-- ── Part 1.1: Missing Data ────────────────────────────────────────────── -->
  <section id="missing">
    <p class="section-label">Part 1.1 · Missing Data</p>
    <h2>Which Idea Lacks Supporting Data?</h2>

    <p>
      <strong>Idea 5 – Interdisciplinary Project Modules</strong> cannot be adequately tested with the current survey.
      While we know a student's <code>primary_major</code> and their rating of
      <code>interested_connections</code>, we have no data on whether students would
      actually choose an interdisciplinary module, nor which domains they want.
    </p>

    <div class="callout">
      <strong>Proposed data collection:</strong> Add two questions to next semester's survey:
      <ol style="margin-top:0.5rem; margin-left:1.2rem; font-size:0.93rem;">
        <li style="margin-bottom:0.3rem"><em>"If COMP110 offered project modules themed around your primary major, how likely would you be to choose one?"</em> (1–7 Likert)</li>
        <li><em>"Which field would you most want a project module to focus on?"</em> (checkbox with major categories)</li>
      </ol>
    </div>
  </section>

  <!-- ── Part 1.2 + 1.3: Analysis ─────────────────────────────────────────── -->
  <section id="analysis">
    <p class="section-label">Part 1.2–1.3 · Analysis</p>
    <h2>Does Prior Experience Predict Difficulty &amp; Understanding?</h2>

    <p>
      I chose <strong>Idea 4</strong> because the survey contains three directly relevant columns —
      <code>prior_exp</code>, <code>difficulty</code>, and <code>understanding</code> — that allow me
      to measure an <em>actual gap in student experience</em> rather than just opinion about a hypothetical feature.
      If novice students demonstrably struggle more, there is a concrete, data-backed argument for investing
      in pre-semester support, creating value for both students and the institution.
    </p>

    <h3>Methodology</h3>
    <p>
      Survey responses were loaded using custom Python utility functions (<code>read_csv_rows</code>,
      <code>columnar</code>, <code>select</code>, <code>head</code>, <code>count</code>).
      Rows with missing values in any required column were dropped. Difficulty and understanding
      ratings (1–7 Likert) were averaged within each of five prior-experience groups, ordered
      from least to most experienced. Four seaborn visualizations were produced.
    </p>

    <!-- Charts ──────────────────────────────────────────────────────────────── -->
    <div class="chart-grid">

      <div class="chart-card">
        <div class="chart-body">
          <img src="chart1_difficulty_bar.png" alt="Bar chart showing average perceived difficulty by prior programming experience level">
        </div>
        <div class="chart-footer">Fig 1 · Avg Difficulty by Prior Experience (Bar)</div>
      </div>

      <div class="chart-card">
        <div class="chart-body">
          <img src="chart2_understanding_bar.png" alt="Bar chart showing average self-reported understanding by prior programming experience level">
        </div>
        <div class="chart-footer">Fig 2 · Avg Understanding by Prior Experience (Bar)</div>
      </div>

      <div class="chart-card">
        <div class="chart-body">
          <img src="chart3_difficulty_boxplot.png" alt="Box plot showing distribution of difficulty ratings by prior experience">
        </div>
        <div class="chart-footer">Fig 3 · Difficulty Distribution by Experience (Box)</div>
      </div>

      <div class="chart-card">
        <div class="chart-body">
          <img src="chart4_scatter.png" alt="Scatter plot of difficulty vs understanding colored by prior experience level">
        </div>
        <div class="chart-footer">Fig 4 · Difficulty vs Understanding, colored by Experience (Scatter)</div>
      </div>

    </div>
  </section>

  <!-- ── Part 1.4: Conclusion ──────────────────────────────────────────────── -->
  <section id="conclusion">
    <p class="section-label">Part 1.4 · Conclusion</p>
    <h2>What the Data Says — and What to Do Next</h2>

    <h3>Findings</h3>
    <ul class="findings">
      <li><span class="dot"></span>Students with no or minimal experience (<em>&lt; 1 month</em>) rated COMP110 as harder on average than peers with 1+ years of experience.</li>
      <li><span class="dot"></span>The same group reported lower self-assessed understanding, and their spread was wider — meaning outcomes within the novice group are highly variable.</li>
      <li><span class="dot"></span>The scatter plot shows novices cluster toward high-difficulty / low-understanding, supporting a real experience gap. The data provides <strong>moderate support</strong> for the bootcamp idea.</li>
    </ul>

    <h3>Costs &amp; Trade-offs</h3>
    <ul class="findings">
      <li><span class="dot"></span><strong>Staff burden:</strong> Pre-semester events require TAs/instructors outside the normal pay period.</li>
      <li><span class="dot"></span><strong>Opt-in problem:</strong> Students who most need help may be least likely to voluntarily engage with optional prep material.</li>
      <li><span class="dot"></span><strong>Equity concerns:</strong> Lower-income students may have less flexibility before the semester begins.</li>
      <li><span class="dot"></span><strong>Risk of redundancy:</strong> If novices catch up quickly on their own, the investment may be unnecessary for many.</li>
    </ul>

    <h3>Extensions &amp; Future Work</h3>
    <ul class="findings">
      <li><span class="dot"></span>Track <strong>objective outcomes</strong> (quiz scores, exercise grades) by experience group, not just self-reported perceptions.</li>
      <li><span class="dot"></span>Pilot a short <strong>async pre-semester module</strong> (3 videos + 2 exercises) and compare survey results to a control semester.</li>
      <li><span class="dot"></span>Examine whether <strong>office-hours attendance</strong> closes the novice gap — if so, expanding OH may be a cheaper alternative to a bootcamp.</li>
      <li><span class="dot"></span>Intersect experience with <strong>demographic variables</strong> to understand whether the gap has equity implications for underrepresented groups.</li>
    </ul>
  </section>

</main>

<footer>
  COMP 110 · EX09 · Course Improvement Analysis &nbsp;·&nbsp; Built with Python &amp; Seaborn
</footer>

</body>
</html>

