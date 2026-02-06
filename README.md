# everychild
Info and resources to help every child been seen and heard in our schools
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Every Child Seen | District Resource Hub</title>
  <style>
    :root{
      --bg:#0b1220;
      --card:#0f1b33;
      --card2:#0c172d;
      --text:#eaf0ff;
      --muted:#b9c7ee;
      --brand:#5ea1ff;
      --accent:#ff4d6d;
      --ok:#2dd4bf;
      --warn:#fbbf24;
      --border: rgba(255,255,255,.12);
      --shadow: 0 12px 30px rgba(0,0,0,.35);
      --radius: 18px;
      --radius2: 12px;
      --max: 1100px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: var(--sans);
      color:var(--text);
      background: radial-gradient(1200px 700px at 20% -10%, rgba(94,161,255,.30), transparent 55%),
                  radial-gradient(900px 600px at 90% 10%, rgba(255,77,109,.20), transparent 50%),
                  linear-gradient(180deg, #070b14, var(--bg) 40%, #070b14);
    }
    a{color:var(--brand); text-decoration:none}
    a:hover{text-decoration:underline}
    .wrap{max-width:var(--max); margin:0 auto; padding:22px 18px 80px}
    .topbar{
      position:sticky; top:0; z-index:50;
      backdrop-filter: blur(10px);
      background: rgba(7,11,20,.72);
      border-bottom:1px solid var(--border);
    }
    .topbar .inner{max-width:var(--max); margin:0 auto; padding:12px 18px; display:flex; gap:12px; align-items:center; justify-content:space-between}
    .brand{
      display:flex; gap:12px; align-items:center; min-width:240px;
    }
    .logo{
      width:40px; height:40px; border-radius:12px;
      background: linear-gradient(135deg, rgba(94,161,255,.95), rgba(255,77,109,.85));
      box-shadow: 0 10px 25px rgba(94,161,255,.18);
      border:1px solid rgba(255,255,255,.20);
      flex:0 0 auto;
    }
    .brand .title{line-height:1.05}
    .brand .title b{display:block; font-size:14px; letter-spacing:.25px}
    .brand .title span{display:block; font-size:12px; color:var(--muted)}
    .nav{
      display:flex; flex-wrap:wrap; gap:8px; align-items:center; justify-content:flex-end;
    }
    .pill{
      border:1px solid var(--border);
      background: rgba(15,27,51,.55);
      padding:8px 10px;
      border-radius: 999px;
      font-size:12px;
      color:var(--text);
      cursor:pointer;
      user-select:none;
      transition: transform .06s ease, background .2s ease;
    }
    .pill:hover{background: rgba(15,27,51,.9)}
    .pill:active{transform: translateY(1px)}
    header.hero{ padding:34px 0 18px; }
    .heroGrid{
      display:grid;
      grid-template-columns: 1.35fr .65fr;
      gap:14px;
      align-items:stretch;
    }
    @media (max-width: 900px){
      .heroGrid{grid-template-columns:1fr}
      .brand{min-width:auto}
      .nav{display:none}
    }
    .card{
      background: linear-gradient(180deg, rgba(15,27,51,.92), rgba(12,23,45,.88));
      border:1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding:18px;
    }
    .card.small{padding:16px; border-radius: var(--radius)}
    h1{margin:0 0 10px; font-size:28px; letter-spacing:.2px}
    .sub{color:var(--muted); font-size:14px; line-height:1.5; margin:0}
    .kpis{
      display:grid; grid-template-columns: repeat(3, 1fr);
      gap:10px; margin-top:14px;
    }
    @media (max-width: 560px){ .kpis{grid-template-columns:1fr} }
    .kpi{
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius2);
      padding:12px;
    }
    .kpi b{display:block; font-size:12px; color:var(--muted); font-weight:600; letter-spacing:.2px}
    .kpi span{display:block; margin-top:6px; font-size:14px}
    .actions{display:flex; gap:10px; flex-wrap:wrap; margin-top:14px}
    .btn{
      border:1px solid rgba(255,255,255,.20);
      background: rgba(94,161,255,.18);
      color:var(--text);
      padding:10px 12px;
      border-radius: 12px;
      font-size:13px;
      cursor:pointer;
      transition: background .2s ease, transform .06s ease;
    }
    .btn:hover{background: rgba(94,161,255,.28)}
    .btn:active{transform: translateY(1px)}
    .btn.secondary{background: rgba(255,77,109,.14)}
    .btn.secondary:hover{background: rgba(255,77,109,.22)}
    .btn.ghost{background: rgba(255,255,255,.03)}
    .btn.ghost:hover{background: rgba(255,255,255,.06)}
    .section{ margin-top:18px; }
    .section h2{
      font-size:18px;
      margin:0 0 10px;
      letter-spacing:.15px;
    }
    .grid2{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:14px;
    }
    @media (max-width: 900px){ .grid2{grid-template-columns:1fr} }
    .grid3{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:14px;
    }
    @media (max-width: 1000px){ .grid3{grid-template-columns:1fr} }
    .tag{
      display:inline-flex;
      align-items:center;
      gap:8px;
      border:1px solid var(--border);
      border-radius: 999px;
      padding:6px 10px;
      background: rgba(255,255,255,.03);
      color:var(--muted);
      font-size:12px;
      margin-right:8px;
      margin-top:6px;
    }
    .dot{
      width:10px; height:10px; border-radius:999px; background: var(--brand);
      box-shadow: 0 0 0 3px rgba(94,161,255,.15);
    }
    .dot.accent{background: var(--accent); box-shadow: 0 0 0 3px rgba(255,77,109,.14)}
    .dot.ok{background: var(--ok); box-shadow: 0 0 0 3px rgba(45,212,191,.14)}
    .dot.warn{background: var(--warn); box-shadow: 0 0 0 3px rgba(251,191,36,.15)}
    .list{
      margin:10px 0 0;
      padding-left:18px;
      color:var(--text);
    }
    .list li{margin:8px 0; color:var(--text); line-height:1.45}
    .muted{color:var(--muted)}
    details{
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius2);
      padding:12px 12px;
    }
    details + details{margin-top:10px}
    summary{
      cursor:pointer;
      font-weight:650;
      list-style:none;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
    }
    summary::-webkit-details-marker{display:none}
    .chev{
      width:28px; height:28px; border-radius:999px;
      border:1px solid var(--border);
      background: rgba(0,0,0,.10);
      display:inline-flex; align-items:center; justify-content:center;
      font-family: var(--mono);
      color:var(--muted);
      flex:0 0 auto;
    }
    details[open] .chev{color:var(--text)}
    .callout{
      border:1px dashed rgba(255,255,255,.22);
      background: rgba(94,161,255,.08);
      border-radius: var(--radius2);
      padding:12px;
      margin-top:10px;
    }
    .callout b{display:block; font-size:12px; letter-spacing:.2px; color:var(--muted)}
    .callout p{margin:8px 0 0; font-size:13px; line-height:1.5}
    .template{
      margin-top:10px;
      border:1px solid var(--border);
      background: rgba(0,0,0,.18);
      border-radius: var(--radius2);
      padding:12px;
      font-family: var(--mono);
      font-size:12px;
      color: rgba(234,240,255,.92);
      white-space: pre-wrap;
    }
    .footer{
      margin-top:26px;
      border-top:1px solid var(--border);
      padding-top:14px;
      color:var(--muted);
      font-size:12px;
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      align-items:center;
      justify-content:space-between;
    }
    .sr{position:absolute; left:-9999px}
  </style>
</head>

<body>
  <div class="topbar">
    <div class="inner">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div class="title">
          <b>Every Child Seen</b>
          <span>District Resource Hub • Implementation-ready materials</span>
        </div>
      </div>

      <nav class="nav" aria-label="Primary">
        <a class="pill" href="#intro">Introduction</a>
        <a class="pill" href="#district">District materials</a>
        <a class="pill" href="#principals">Principal materials</a>
        <a class="pill" href="#grades">Grade-appropriate materials</a>
        <a class="pill" href="#grade-handouts">Grade handouts</a>
        <a class="pill" href="#family">Family engagement</a>
        <a class="pill" href="#faq">FAQ</a>
        <a class="pill" href="#contact">Contact</a>
      </nav>
    </div>
  </div>

  <div class="wrap">
    <!-- INTRO -->
    <header class="hero" id="intro">
      <div class="heroGrid">
        <section class="card">
          <h1>Every Child Seen</h1>
          <p class="sub">
            A districtwide, equity-centered MTSS and belonging framework that makes “seen-ness” observable:
            in routines, relationships, instructional moves, and systems. This site is designed to be dropped into
            Weebly and used immediately by district leaders, principals, and teachers.
          </p>

          <div class="kpis" aria-label="Program anchors">
            <div class="kpi">
              <b>Non-negotiable outcome</b>
              <span>Belonging + access for every learner</span>
            </div>
            <div class="kpi">
              <b>How we operationalize it</b>
              <span>Tiered supports + culturally responsive practice</span>
            </div>
            <div class="kpi">
              <b>What changes on Monday</b>
              <span>Routines, data cycles, and family partnership</span>
            </div>
          </div>

          <div class="actions">
            <button class="btn" onclick="scrollToId('district')">Go to District Materials</button>
            <button class="btn secondary" onclick="scrollToId('principals')">Go to Principal Toolkit</button>
            <button class="btn ghost" onclick="window.print()">Print / Save as PDF</button>
          </div>

          <div class="callout">
            <b>Program definition</b>
            <p>
              <strong>Every Child Seen</strong> is a coherence strategy: it aligns instruction, SEL, attendance/engagement,
              discipline, and family partnership so that students on the margins (MLL/immigrant students, students with IEPs,
              students in poverty, students experiencing trauma, LGBTQ+ students, Native students, and others)
              are proactively supported rather than retroactively “fixed.”
            </p>
          </div>
        </section>

        <aside class="card small">
          <h2 style="margin:0 0 8px;font-size:16px">Quick Start</h2>
          <div class="tag"><span class="dot ok"></span> Use the staff meeting agenda (20–30 min)</div>
          <div class="tag"><span class="dot"></span> Run the 10-day launch checklist</div>
          <div class="tag"><span class="dot accent"></span> Start a weekly “Seen Data” huddle</div>
          <div class="tag"><span class="dot warn"></span> Publish family-facing commitments</div>

          <div style="margin-top:10px">
            <details>
              <summary>
                What “Seen Data” means <span class="chev">+</span>
              </summary>
              <p class="sub" style="margin-top:10px">
                “Seen Data” is evidence that students are known, supported, and connected—beyond grades.
                Examples: adult connection logs, attendance/engagement patterns, course access, behavior context notes,
                language support access, and student voice pulse checks.
              </p>
            </details>
          </div>
        </aside>
      </div>
    </header>

    <!-- DISTRICT MATERIALS -->
    <section class="section" id="district">
      <h2>District Materials</h2>

      <div class="grid2">
        <div class="card">
          <details open>
            <summary>
              1) District Commitments (copy/paste ready) <span class="chev">–</span>
            </summary>
            <ul class="list">
              <li><strong>We will know every student</strong> by name, strength, language(s), identity, and learning needs—and act on that knowledge.</li>
              <li><strong>We will remove barriers</strong> to rigorous learning (placement, access, materials, schedules, and adult assumptions).</li>
              <li><strong>We will respond early</strong> with tiered supports—academics, behavior, attendance, and SEL—before a student falls behind.</li>
              <li><strong>We will partner with families</strong> as co-educators, using accessible communication and culturally grounded engagement.</li>
              <li><strong>We will measure what we value</strong> by tracking belonging and access indicators—not just test scores.</li>
            </ul>

            <div class="template" aria-label="Commitments for district site or handbook">
EVERY CHILD SEEN — DISTRICT COMMITMENTS
1) Know every student.  2) Remove barriers to access.
3) Respond early with tiered supports. 4) Partner with families as co-educators.
5) Measure what we value: belonging + access, alongside achievement.
            </div>
          </details>

          <details>
            <summary>
              2) Implementation Roles & Routines <span class="chev">+</span>
            </summary>
            <ul class="list">
              <li><strong>District leadership:</strong> align expectations, protect time, and publish shared definitions (MTSS, Tier 1 quality, “Seen Data”).</li>
              <li><strong>School leadership:</strong> run a weekly huddle (30 min) on “Seen Data” + a monthly team-based problem-solving cycle.</li>
              <li><strong>Teacher teams:</strong> use common routines (quick checks, language supports, re-teach plans, and student voice).</li>
              <li><strong>MLL/SpEd/counseling:</strong> co-plan Tier 1 supports, not only Tier 2/3 interventions; build capacity in classrooms.</li>
            </ul>
            <div class="callout">
              <b>Minimum viable routines (districtwide)</b>
              <p>
                Weekly huddle • Common look-fors • Common data cycle • A shared family communication cadence • A shared student voice pulse check.
              </p>
            </div>
          </details>

          <details>
            <summary>
              3) District Data Dashboard (what to track) <span class="chev">+</span>
            </summary>
            <ul class="list">
              <li><strong>Belonging & connection:</strong> student pulse (2–4 items), adult connection rates, club/activity participation.</li>
              <li><strong>Access:</strong> course placement equity, intervention access, language service access, IEP minutes delivered.</li>
              <li><strong>Engagement:</strong> attendance trends, chronic absenteeism, on-track indicators by subgroup.</li>
              <li><strong>Instructional health:</strong> Tier 1 walkthrough indicators, assignment completion, formative checks.</li>
              <li><strong>Discipline context:</strong> incidents + reasons, location/time patterns, disproportionality, response types.</li>
            </ul>
            <p class="sub">
              Tip: disaggregate by race/ethnicity, IEP status, MLL status, foster/housing insecurity where available, and grade level.
            </p>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>
              District Messaging Toolkit <span class="chev">–</span>
            </summary>

            <p class="sub" style="margin-top:10px">
              Use these as website copy, board updates, newsletters, or cabinet talking points.
            </p>

            <div class="callout">
              <b>30-second elevator message</b>
              <p>
                Every Child Seen is our promise that students won’t have to “earn” belonging. We align instruction, supports,
                and family partnership so that barriers are removed early, learning is accessible, and each student is known and supported.
              </p>
            </div>

            <div class="callout">
              <b>Board / cabinet talking points</b>
              <p>
                1) Defines “seen-ness” as observable practice and measurable access. 2) Strengthens Tier 1 for all learners.
                3) Improves engagement and attendance. 4) Reduces disproportionality through earlier, culturally responsive supports.
                5) Creates consistent routines across schools while respecting local context.
              </p>
            </div>

            <details>
              <summary>Press-ready “What families can expect” <span class="chev">+</span></summary>
              <ul class="list">
                <li>Clear learning targets and regular feedback on progress.</li>
                <li>Accessible communication in family-preferred language whenever possible.</li>
                <li>Early outreach when a student needs support—academically, socially, or emotionally.</li>
                <li>Opportunities for student voice and leadership.</li>
                <li>Support plans that include family strengths, culture, and goals.</li>
              </ul>
            </details>

            <details>
              <summary>One-page district rollout plan (90 days) <span class="chev">+</span></summary>
              <ul class="list">
                <li><strong>Days 1–10:</strong> publish commitments, run principal training, set minimum routines, and launch walkthrough look-fors.</li>
                <li><strong>Days 11–30:</strong> school teams build “Seen Data” lists, set huddle schedule, establish family comms cadence, run baseline pulse.</li>
                <li><strong>Days 31–60:</strong> first problem-solving cycle; targeted Tier 1 PD (language supports, UDL, engagement routines).</li>
                <li><strong>Days 61–90:</strong> evaluate early indicators, refine interventions menu, share wins + next steps publicly.</li>
              </ul>
            </details>
          </details>
        </div>
      </div>
    </section>

    <!-- PRINCIPAL MATERIALS -->
    <section class="section" id="principals">
      <h2>Principal Materials</h2>

      <div class="grid3">
        <div class="card">
          <details open>
            <summary>
              10-Day Launch Checklist <span class="chev">–</span>
            </summary>
            <ul class="list">
              <li>Identify your <strong>Every Child Seen leadership team</strong> (admin + counselor + MLL + SpEd + teacher leaders).</li>
              <li>Publish a <strong>school promise</strong> aligned to district commitments.</li>
              <li>Schedule a <strong>weekly “Seen Data” huddle</strong> (30 minutes).</li>
              <li>Adopt <strong>walkthrough look-fors</strong> (Tier 1 + engagement + language supports).</li>
              <li>Start <strong>adult connection tracking</strong> (simple roster + weekly check-ins for students on the margins).</li>
              <li>Run a <strong>2-minute student pulse</strong> in advisory or a core class.</li>
              <li>Set a <strong>family communication cadence</strong> (weekly update + outreach protocols).</li>
              <li>Choose <strong>one Tier 1 focus</strong> to improve this month (e.g., checks for understanding, sentence stems).</li>
              <li>Define <strong>intervention entry/exit</strong> criteria for academics, attendance, and SEL.</li>
              <li>Share early wins at staff meeting; name next steps.</li>
            </ul>
          </details>

          <details>
            <summary>Weekly “Seen Data” Huddle Protocol (30 min) <span class="chev">+</span></summary>
            <ul class="list">
              <li><strong>5 min:</strong> quick wins (name 2–3 students who reconnected this week).</li>
              <li><strong>10 min:</strong> review “Seen Data” list (attendance, missing work, behavior context, pulse responses).</li>
              <li><strong>10 min:</strong> choose 3–5 students for action; assign adult owner + next step + due date.</li>
              <li><strong>5 min:</strong> system tweak (barrier removal: schedule, language support, transportation, materials, tutoring access).</li>
            </ul>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>
              Staff Meeting Mini-Module (20–30 min) <span class="chev">–</span>
            </summary>
            <p class="sub" style="margin-top:10px">
              Use this to introduce the initiative without slides. Read it verbatim if needed.
            </p>
            <div class="template" aria-label="Staff meeting script">
1) WHY (2 min)
We’re launching Every Child Seen because belonging and access are prerequisites for learning.
Students on the margins often experience school as confusing, inconsistent, or invisible.

2) WHAT (6 min)
Every Child Seen is not “one more thing.” It’s how we align instruction, supports, and family partnership:
- Strong Tier 1 for all learners
- Early, tiered supports when a student needs more
- Measurable “Seen Data” (connection, access, engagement)

3) HOW (10–15 min)
This month we will:
- Run a weekly Seen Data huddle
- Use common walkthrough look-fors
- Strengthen one Tier 1 routine (checks for understanding + language supports)
- Track adult connections for students needing a tighter safety net

4) COMMITMENT (2 min)
Every adult will ensure at least 5 students can say, “There is an adult here who knows me, supports me, and helps me succeed.”
            </div>

            <details>
              <summary>Walkthrough Look-Fors (Tier 1) <span class="chev">+</span></summary>
              <ul class="list">
                <li><strong>Learning target visible</strong> and referenced.</li>
                <li><strong>Checks for understanding</strong> every 8–12 minutes.</li>
                <li><strong>Language supports</strong> (sentence stems, visuals, word bank, structured talk).</li>
                <li><strong>Participation equity</strong> (no “hands-up only”; cold/warm calling, turn-and-talk).</li>
                <li><strong>Belonging routines</strong> (greeting, norms, affirmations, restorative tone).</li>
              </ul>
            </details>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>
              Communication Templates <span class="chev">–</span>
            </summary>

            <details open>
              <summary>Family newsletter blurb <span class="chev">–</span></summary>
              <div class="template" aria-label="Family newsletter template">
EVERY CHILD SEEN at [School Name]
This year we are strengthening how we support every learner—academically, socially, and emotionally.
Families can expect clear communication, early outreach when support is needed, and opportunities to share your goals and strengths.
If your family prefers communication in another language, please contact [Name/Phone/Email].
              </div>
            </details>

            <details>
              <summary>Teacher-to-family early outreach call script <span class="chev">+</span></summary>
              <div class="template" aria-label="Outreach call script">
Hi, this is [Name] from [School]. I’m calling as part of our Every Child Seen commitment.
I want to share one strength I see in [Student], and one area we can support early.
What has been working well at home? What do you want us to know about your child’s goals, culture, language, or needs?
Let’s agree on the next step and how we’ll communicate this week.
              </div>
            </details>

            <details>
              <summary>Staff-facing weekly update format <span class="chev">+</span></summary>
              <div class="template" aria-label="Weekly staff update">
EVERY CHILD SEEN — WEEKLY (5 bullets max)
1) One win (student/grade/team).
2) One Tier 1 focus to tighten this week.
3) Students needing connection (who + adult owner).
4) One barrier removed (schedule/materials/support).
5) Reminder: huddle time + data we’re reviewing.
              </div>
            </details>
          </details>
        </div>
      </div>
    </section>

    <!-- GRADE-APPROPRIATE MATERIALS -->
    <section class="section" id="grades">
      <h2>Grade-Appropriate Materials</h2>

      <div class="grid2">
        <div class="card">
          <details open>
            <summary>K–2: “I Belong Here” Routines <span class="chev">–</span></summary>
            <div class="tag"><span class="dot ok"></span> Belonging</div>
            <div class="tag"><span class="dot"></span> Early literacy support</div>
            <div class="tag"><span class="dot accent"></span> Family partnership</div>

            <ul class="list">
              <li><strong>Daily connection:</strong> 30-second greeting at the door + name practice + “I’m glad you’re here.”</li>
              <li><strong>Emotion check-in:</strong> feelings chart + “show me with fingers 1–5.”</li>
              <li><strong>Structured talk:</strong> turn-and-talk with sentence frames: “I think ___ because ___.”</li>
              <li><strong>Visual supports:</strong> picture schedule, icons for materials, “first/then” cards.</li>
              <li><strong>Early outreach:</strong> one positive family message per student each month (phone, text, note home).</li>
            </ul>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>3–5: “Access + Voice” Routines <span class="chev">–</span></summary>
            <div class="tag"><span class="dot"></span> Participation equity</div>
            <div class="tag"><span class="dot ok"></span> Academic confidence</div>
            <div class="tag"><span class="dot warn"></span> Attendance/engagement</div>

            <ul class="list">
              <li><strong>Participation structure:</strong> no “hands-up only.” Use think time → partner talk → share.</li>
              <li><strong>Checks for understanding:</strong> quick whiteboard, thumbs, exit ticket every lesson.</li>
              <li><strong>Choice + relevance:</strong> 2 options for product (poster/paragraph/recording).</li>
              <li><strong>Student voice:</strong> weekly 2-question pulse: “Do you feel you belong?” “Do adults help you succeed?”</li>
              <li><strong>Barrier removal:</strong> ensure access to supplies, reading supports, and after-school help.</li>
            </ul>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>6–8: Middle School “Belonging + Rigor” <span class="chev">–</span></summary>
            <div class="tag"><span class="dot accent"></span> Identity-safe classrooms</div>
            <div class="tag"><span class="dot"></span> Advisory</div>
            <div class="tag"><span class="dot ok"></span> Executive skills</div>

            <ul class="list">
              <li><strong>Advisory anchor:</strong> weekly community circle + goal setting + adult connection tracking.</li>
              <li><strong>Transparent grading:</strong> clear criteria, revision opportunities, and feedback cycles.</li>
              <li><strong>Executive skills:</strong> teach planners, chunking, and “next action” routines.</li>
              <li><strong>Restorative responses:</strong> repair harm + reteach expectations; reduce exclusionary responses when possible.</li>
              <li><strong>Student voice:</strong> include feedback loops on classroom climate and workload.</li>
            </ul>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>9–12: High School “Access + Pathways” <span class="chev">–</span></summary>
            <div class="tag"><span class="dot warn"></span> On-track</div>
            <div class="tag"><span class="dot"></span> Course access</div>
            <div class="tag"><span class="dot ok"></span> Post-secondary pathways</div>

            <ul class="list">
              <li><strong>On-track system:</strong> weekly check on credits, attendance, and missing work; rapid re-engagement.</li>
              <li><strong>Course access equity:</strong> review placement and supports for advanced courses, CTE, dual credit, and interventions.</li>
              <li><strong>Advisory / mentoring:</strong> every student has an adult advocate; track connection and intervention access.</li>
              <li><strong>Student voice + identity:</strong> ensure clubs, leadership, and representation are accessible to students on the margins.</li>
              <li><strong>Family partnership:</strong> multilingual pathways nights; explain graduation, credit recovery, FAFSA/WASFA, and schedules.</li>
            </ul>
          </details>
        </div>
      </div>
    </section>

    <!-- GRADE HANDOUTS -->
    <section class="section" id="grade-handouts">
      <h2>Grade-Band Handouts</h2>
      <p class="sub">
        Use these one-page, copy/paste handouts in PLCs, staff meetings, onboarding, and coaching cycles.
        They align to Every Child Seen routines: Tier 1 strength, early outreach, “Seen Data,” and barrier removal.
      </p>

      <div class="grid2">

        <!-- K–2 -->
        <div class="card" id="k2">
          <details open>
            <summary>K–2nd Grade: “I Belong Here” Toolkit <span class="chev">–</span></summary>

            <div class="tag"><span class="dot ok"></span> Belonging + safety</div>
            <div class="tag"><span class="dot"></span> Tier 1 routines</div>
            <div class="tag"><span class="dot accent"></span> Family partnership</div>

            <div class="callout">
              <b>Purpose</b>
              <p>
                Create predictable routines and language supports so young learners feel safe, known, and academically capable.
                Prioritize connection, clarity, and rapid support when needs show up.
              </p>
            </div>

            <details open>
              <summary>Handout A: Daily “Seen” Routines (K–2) <span class="chev">–</span></summary>
              <div class="template">
K–2 DAILY “SEEN” ROUTINES (10 minutes total)
1) Door greeting (30 sec/student): Name + “I’m glad you’re here.”
2) Feelings check (2 min): Point to chart / 1–5 fingers → teacher scans.
3) Visual schedule review (1 min): “First ___, then ___.”
4) Talk routine (3 min): Turn-and-talk with frames:
   - “I notice ___.”  “I think ___ because ___.”
5) Quick check (2 min): Thumbs / whiteboard / show me.
6) Close (2 min): “What helped you learn today?” + class affirmation.

NON-NEGOTIABLES
- Every student speaks daily (partner talk counts).
- Directions are 1–2 steps, with a visual.
- Correct privately, affirm publicly; repair harm quickly.
              </div>
            </details>

            <details>
              <summary>Handout B: Tier 1 Language Supports (K–2) <span class="chev">+</span></summary>
              <div class="template">
K–2 TIER 1 LANGUAGE SUPPORTS (FOR ALL CLASSROOMS)
BEFORE:
- Pre-teach 3–5 key words with pictures/objects.
- Show an example of the final product.

DURING:
- Use gestures + visuals; repeat key directions.
- Choral response / echo reading.
- Sentence frames:
  “I see ___.” “I like ___.” “I need help with ___.”

AFTER:
- 10-second retell: “Today we learned ___.”
- Send one photo + caption home weekly (family language when possible).
              </div>
            </details>

            <details>
              <summary>Handout C: Early Outreach + Family Strengths (K–2) <span class="chev">+</span></summary>
              <div class="template">
K–2 EARLY OUTREACH SCRIPT (2–3 minutes)
1) Strength: “I’m calling to share something great about [Student]…”
2) Support early: “One thing we’re helping with right now is…”
3) Family voice: “What works at home? What should we know about language/culture/goals?”
4) Next step: “This week we will ___; could you ___? Let’s check in on ___.”

TRACKING (WEEKLY)
- Who received a positive message this week?
- Who needs a check-in because of attendance/behavior/learning signals?
              </div>
            </details>
          </details>
        </div>

        <!-- 3–5 -->
        <div class="card" id="35">
          <details open>
            <summary>3–5th Grade: “Access + Voice” Toolkit <span class="chev">–</span></summary>

            <div class="tag"><span class="dot"></span> Participation equity</div>
            <div class="tag"><span class="dot ok"></span> Checks for understanding</div>
            <div class="tag"><span class="dot warn"></span> Engagement + attendance</div>

            <div class="callout">
              <b>Purpose</b>
              <p>
                Ensure every student participates daily, understands expectations, and has multiple ways to show learning.
                Tighten Tier 1 instruction so supports are proactive—not reactive.
              </p>
            </div>

            <details open>
              <summary>Handout A: Participation Equity Routines (3–5) <span class="chev">–</span></summary>
              <div class="template">
3–5 PARTICIPATION EQUITY (DO THIS DAILY)
ROUTINE: Think → Pair → Share
- Think time (10–20 sec)
- Partner talk (30–60 sec)
- Share (random/structured, not hands-only)

TOOLS:
- Sentence stems (3 levels):
  Starter: “I think ___.”
  Intermediate: “I think ___ because ___.”
  Advanced: “I agree/disagree with ___ because ___. For example ___.”
- No-opt-out: If stuck, student can say “I need a hint.” Teacher returns.

LOOK-FORS:
- Every student speaks/produces something every lesson.
- Teacher cold/warm calls with support and wait time.
              </div>
            </details>

            <details>
              <summary>Handout B: CFU Menu (Checks for Understanding) (3–5) <span class="chev">+</span></summary>
              <div class="template">
3–5 CFU MENU (EVERY 8–12 MINUTES)
Pick 2–3 per lesson:
- Thumbs (up/side/down) + follow-up question
- Mini whiteboards (“show me”)
- 2-question exit ticket
- “Explain to your partner” prompt
- Quick sort (cards into groups)
- 1-sentence summary: “The main idea is ___.”

RESPONSE RULE:
If 20%+ miss it → reteach immediately using a different method (model/visual/example).
              </div>
            </details>

            <details>
              <summary>Handout C: Barrier Removal + Quick Supports (3–5) <span class="chev">+</span></summary>
              <div class="template">
3–5 BARRIER REMOVAL CHECKLIST (WEEKLY)
ACADEMIC:
- Do students have materials (pencils/books/chargers)?
- Are directions written + modeled?
- Are there scaffolds (word bank, graphic organizer, example)?

ENGAGEMENT:
- Who is missing school? Who is “quiet compliant”?
- Assign an adult check-in for 5–10 students who need tighter connection.

FAMILY:
- Weekly class update (what we’re learning + how to help at home).
- Offer options: text/call/paper; interpreter as needed.
              </div>
            </details>
          </details>
        </div>

        <!-- Middle School -->
        <div class="card" id="ms">
          <details open>
            <summary>Middle School: “Belonging + Rigor” Toolkit <span class="chev">–</span></summary>

            <div class="tag"><span class="dot accent"></span> Identity-safe</div>
            <div class="tag"><span class="dot"></span> Advisory systems</div>
            <div class="tag"><span class="dot ok"></span> Executive skills</div>

            <div class="callout">
              <b>Purpose</b>
              <p>
                Make belonging visible through advisory, predictable classroom structures, and restorative routines—while
                protecting rigorous learning with strong Tier 1 supports.
              </p>
            </div>

            <details open>
              <summary>Handout A: Advisory “Seen” Cycle (Middle School) <span class="chev">–</span></summary>
              <div class="template">
MIDDLE SCHOOL ADVISORY SEEN CYCLE (WEEKLY, 25–30 MIN)
1) Connect (5): 1 question circle (“What’s one win or challenge this week?”)
2) Skills (10): executive skill mini-lesson (planner, chunking, help-seeking)
3) Track (5): on-track check (attendance / missing work / behavior signals)
4) Plan (5–10): each student writes a next action + who will support them

ADULT ADVOCATE NON-NEGOTIABLE
- Every student can name a trusted adult.
- Students with flags (attendance/missing work/pulse) get a same-week check-in.
              </div>
            </details>

            <details>
              <summary>Handout B: Classroom Structure That Reduces Chaos (MS) <span class="chev">+</span></summary>
              <div class="template">
MS CLASSROOM STRUCTURE (SAME FLOW, EVERY DAY)
Warm-up (5) → Teach (10) → Try (20) → Reflect (5)

TIER 1 MUST-HAVES
- Learning target + success criteria
- CFU every 10 minutes
- Structured talk + sentence stems
- Clear “What to do if I’m stuck” ladder

RESTORATIVE MICRO-ROUTINE
- “What happened?” “Who was impacted?” “How do we repair?” “What’s next?”
              </div>
            </details>

            <details>
              <summary>Handout C: “Seen Data” Flags + Actions (MS) <span class="chev">+</span></summary>
              <div class="template">
MS SEEN DATA FLAGS (CHOOSE 3–5 TO TRACK)
- 2+ absences in a week or pattern of tardies
- Missing 2+ assignments in 2 classes
- Behavior incidents with repeated location/time pattern
- Low pulse: “I don’t feel I belong / adults don’t help”
- Sudden drop in participation / withdrawal

ACTIONS (WITHIN 5 SCHOOL DAYS)
1) Adult advocate check-in (barriers + goals)
2) Teacher “minimum viable work” plan
3) Schedule supports (tutoring/flex/reteach)
4) Family contact in preferred language
5) Review Tier 1: did we provide scaffolds and access?
              </div>
            </details>
          </details>
        </div>

        <!-- High School -->
        <div class="card" id="hs">
          <details open>
            <summary>High School: “Access + Pathways” Toolkit <span class="chev">–</span></summary>

            <div class="tag"><span class="dot warn"></span> On-track + credits</div>
            <div class="tag"><span class="dot"></span> Course access equity</div>
            <div class="tag"><span class="dot ok"></span> Post-secondary</div>

            <div class="callout">
              <b>Purpose</b>
              <p>
                Prevent students from “falling through the cracks” by tightening on-track systems, course access, and
                rapid re-engagement—while maintaining strong Tier 1 instruction and culturally responsive family partnership.
              </p>
            </div>

            <details open>
              <summary>Handout A: On-Track Monitoring (HS) <span class="chev">–</span></summary>
              <div class="template">
HS ON-TRACK (WEEKLY TEAM HUDDLE, 30 MIN)
DATA (5): credits, attendance, missing work, behavior context, student voice pulse
PRIORITIZE (10): identify 10–20 students for action (start with highest leverage)
ASSIGN (10): adult owner + next step + due date (48–72 hours)
SYSTEM FIX (5): remove one barrier (schedule, transportation, interpreter, tutoring access)

NON-NEGOTIABLES
- Students with failing + attendance flags get contact within the week.
- Re-engagement plans are simple, specific, and time-bound.
              </div>
            </details>

            <details>
              <summary>Handout B: Rapid Re-Engagement Protocol (HS) <span class="chev">+</span></summary>
              <div class="template">
HS RAPID RE-ENGAGEMENT (10 DAYS)
DAY 1–2
- Adult advocate contact + barrier check (work, housing, health, language, transportation)
- Identify 1–2 “quick win” tasks to restore momentum

DAY 3–5
- Teacher plan: minimum viable work (what counts, what’s prioritized)
- Tutoring / flex / study hall scheduled

DAY 6–10
- Daily or every-other-day check-in
- Family contact in preferred language
- Adjust schedule/supports if barriers persist
              </div>
            </details>

            <details>
              <summary>Handout C: Course Access + Equity Review (HS) <span class="chev">+</span></summary>
              <div class="template">
HS COURSE ACCESS EQUITY REVIEW (MONTHLY)
LOOK AT:
- Advanced / dual credit / CTE participation by subgroup
- Intervention placement (who gets support, who gets removed from opportunities)
- Discipline and attendance impacts on access
- Language service access for MLL students (interpreters, translated materials)

ACTIONS:
- Add scaffolds and co-teaching supports (don’t gatekeep access)
- Publish transparent placement criteria
- Invite + recruit students/families proactively (multi-language outreach)
              </div>
            </details>
          </details>
        </div>

      </div>

      <div class="footer" style="margin-top:16px">
        <div><strong>How to use:</strong> Print a handout → run a 10-minute PLC → choose one routine → implement for 2 weeks → review “Seen Data.”</div>
        <div class="muted">Jump to: <a href="#k2">K–2</a> • <a href="#35">3–5</a> • <a href="#ms">Middle School</a> • <a href="#hs">High School</a></div>
      </div>
    </section>

    <!-- FAMILY ENGAGEMENT -->
    <section class="section" id="family">
      <h2>Family Engagement Materials</h2>

      <div class="grid2">
        <div class="card">
          <details open>
            <summary>Family Partnership Principles <span class="chev">–</span></summary>
            <ul class="list">
              <li><strong>Asset-based:</strong> start with strengths, culture, language, and goals.</li>
              <li><strong>Accessible:</strong> clear language, multiple channels, interpreters/translation for meaningful participation.</li>
              <li><strong>Consistent:</strong> predictable cadence; proactive outreach (not only when there’s a problem).</li>
              <li><strong>Two-way:</strong> families shape solutions; student voice is included.</li>
            </ul>

            <details>
              <summary>Ready-to-run event formats <span class="chev">+</span></summary>
              <ul class="list">
                <li><strong>Community dinner + listening session (60 min):</strong> food, childcare when possible, short welcome, small-group questions, next steps.</li>
                <li><strong>Pathways night (HS):</strong> graduation requirements, course options, supports, Q&amp;A stations.</li>
                <li><strong>Student showcase:</strong> short performances, projects, awards—build pride and trust.</li>
              </ul>
            </details>
          </details>
        </div>

        <div class="card">
          <details open>
            <summary>Family Survey (copy/paste) <span class="chev">–</span></summary>
            <p class="sub" style="margin-top:10px">
              Use in Google Forms, paper, or phone calls. Keep it short; offer language options whenever possible.
            </p>
            <div class="template" aria-label="Family survey">
FAMILY PARTNERSHIP SURVEY (5–7 minutes)
1) What is one strength your child brings to school?
2) What do you want the school to know about your family’s culture, language, and goals?
3) How do you prefer to communicate? (text/call/email/paper/other)
4) What time(s) work best for meetings?
5) What makes it hard to participate (transportation, work schedule, childcare, language, other)?
6) What support would help your child succeed this year?
7) (Optional) Would you like a staff member to contact you? If yes, how?
            </div>
          </details>
        </div>
      </div>
    </section>

    <!-- FAQ -->
    <section class="section" id="faq">
      <h2>FAQ</h2>
      <div class="card">
        <details open>
          <summary>Is this “one more initiative”? <span class="chev">–</span></summary>
          <p class="sub" style="margin-top:10px">
            No. Every Child Seen is a coherence framework: it aligns what we already do (instruction, SEL, MTSS, engagement,
            and family partnership) into shared routines and measurable outcomes so students on the margins aren’t missed.
          </p>
        </details>

        <details>
          <summary>What should teachers do differently first? <span class="chev">+</span></summary>
          <ul class="list">
            <li>Strengthen Tier 1: clear targets, frequent checks, structured talk, and language supports.</li>
            <li>Use predictable routines that reduce anxiety and increase participation.</li>
            <li>Ensure at least 5 students per adult have a reliable connection and check-in.</li>
          </ul>
        </details>

        <details>
          <summary>How do we prevent this from becoming compliance? <span class="chev">+</span></summary>
          <ul class="list">
            <li>Focus on student experience (voice + access) rather than binders and forms.</li>
            <li>Use short cycles: identify a barrier → act → check impact → adjust.</li>
            <li>Share wins and learn publicly; keep the data human and actionable.</li>
          </ul>
        </details>

        <details>
          <summary>What counts as evidence that “every child is seen”? <span class="chev">+</span></summary>
          <ul class="list">
            <li>Students can name an adult who knows them and helps them succeed.</li>
            <li>Families report accessible communication and meaningful partnership.</li>
            <li>Access gaps narrow (course placement, intervention access, language supports).</li>
            <li>Engagement improves (attendance/on-track) and disproportionality decreases.</li>
          </ul>
        </details>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="section" id="contact">
      <h2>Get in Touch</h2>

      <div class="card">
        <p class="sub" style="margin:0 0 14px;">
          Have questions, feedback, or requests for customization? We'd love to hear from you.
          Contact us with ideas for implementation, professional development, or framework adaptations.
        </p>

        <form id="contactForm" style="display:flex; flex-direction:column; gap:12px;" onsubmit="handleContactSubmit(event)">
          <div>
            <label for="name" style="display:block; margin-bottom:6px; font-size:13px; color:var(--muted)">Name</label>
            <input type="text" id="name" name="name" required style="width:100%; padding:10px; border:1px solid var(--border); background: rgba(0,0,0,.15); color:var(--text); border-radius:var(--radius2); font-family:var(--sans)" />
          </div>

          <div>
            <label for="email" style="display:block; margin-bottom:6px; font-size:13px; color:var(--muted)">Email</label>
            <input type="email" id="email" name="email" required style="width:100%; padding:10px; border:1px solid var(--border); background: rgba(0,0,0,.15); color:var(--text); border-radius:var(--radius2); font-family:var(--sans)" />
          </div>

          <div>
            <label for="role" style="display:block; margin-bottom:6px; font-size:13px; color:var(--muted)">Role</label>
            <select id="role" name="role" required style="width:100%; padding:10px; border:1px solid var(--border); background: rgba(0,0,0,.15); color:var(--text); border-radius:var(--radius2); font-family:var(--sans)">
              <option value="" style="background:#0b1220">Select your role...</option>
              <option value="district" style="background:#0b1220">District Leader</option>
              <option value="principal" style="background:#0b1220">Principal / School Leader</option>
              <option value="teacher" style="background:#0b1220">Teacher / Educator</option>
              <option value="family" style="background:#0b1220">Family / Community Member</option>
              <option value="other" style="background:#0b1220">Other</option>
            </select>
          </div>

          <div>
            <label for="message" style="display:block; margin-bottom:6px; font-size:13px; color:var(--muted)">Message / Request</label>
            <textarea id="message" name="message" required rows="5" style="width:100%; padding:10px; border:1px solid var(--border); background: rgba(0,0,0,.15); color:var(--text); border-radius:var(--radius2); font-family:var(--sans); resize:vertical;" placeholder="Tell us about your needs, feedback, or customization requests..."></textarea>
          </div>

          <button type="submit" class="btn" style="align-self:flex-start; cursor:pointer;">Send Message</button>
          <p id="formStatus" style="font-size:13px; color:var(--muted); margin:0; display:none;"></p>
        </form>

        <div style="margin-top:18px; padding-top:18px; border-top:1px solid var(--border);">
          <h3 style="margin:0 0 10px; font-size:14px;">Other Ways to Connect</h3>
          <ul class="list">
            <li><strong>Email:</strong> <a href="mailto:hello@everychildseen.org">hello@everychildseen.org</a></li>
            <li><strong>GitHub:</strong> <a href="https://github.com/hesings11-dot/everychild" target="_blank">View project repository</a></li>
            <li><strong>Share feedback:</strong> Use the contact form above or open an issue on GitHub</li>
          </ul>
        </div>
      </div>
    </section>

    <div class="footer">
      <div>
        <strong>Every Child Seen</strong> • District Resource Hub
        <span class="muted"> • Copy/paste-ready materials for Weebly</span>
      </div>
      <div class="muted">Tip: Use Weebly “Embed Code” element → paste entire HTML.</div>
    </div>
  </div>

  <script>
    function scrollToId(id){
      const el = document.getElementById(id);
      if(!el) return;
      const y = el.getBoundingClientRect().top + window.scrollY - 70;
      window.scrollTo({ top: y, behavior: "smooth" });
    }

    function handleContactSubmit(event){
      event.preventDefault();
      const formStatus = document.getElementById('formStatus');
      const formData = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        role: document.getElementById('role').value,
        message: document.getElementById('message').value,
        timestamp: new Date().toISOString()
      };
      
      // Log to console for demonstration
      console.log('Contact form submission:', formData);
      
      // Show success message
      formStatus.textContent = '✓ Thank you! Your message has been received. We will respond within 2-3 business days.';
      formStatus.style.color = 'var(--ok)';
      formStatus.style.display = 'block';
      
      // Reset form
      document.getElementById('contactForm').reset();
      
      // Hide message after 6 seconds
      setTimeout(function(){
        formStatus.style.display = 'none';
      }, 6000);
      
      // In a real implementation, you would send this to a backend service or email handler
      // Example: fetch('/api/contact', { method: 'POST', body: JSON.stringify(formData) })
    }
  </script>
</body>
</html>


