# Optima Learn — AI PM Intern Assignment Submission


---

## TASK 3 — Usability Test Findings

### Methodology
From the 10 user research conversations, 5 users were selected for usability testing — covering a range of prep stages (just started → advanced) and backgrounds (working professional, fresh grad, small-town aspirant). Each user was given unguided access to optimalearn.com after completing the signup/onboarding form. No hints were given. After exploration, each was asked:

>

### User 1 — Priya Shaw (Just Started, Coaching-dependent)

**What she wrote:**
1. Practice questions for CAT
2. Some kind of AI study assistant
3. Mock tests maybe?

**Analysis:**
- ✅ Got right: Practice questions and mocks — core features
- ❌ Misunderstood: "AI study assistant" — she couldn't articulate *what* it does specifically; she associated "AI" with a chatbot she could ask questions to, which isn't the product's core offering
- ❌ Missed entirely: Personalised study plans, score prediction, the roadmap feature

**Insight:** The word "AI" on the homepage creates expectation of a chatbot/tutor, not a planning tool. There is a messaging-expectation mismatch. Users arrive expecting interaction, but find content.

---

### User 2 — Naveen (Just Started, RC-averse)

**What he wrote:**
1. Free CAT questions
2. Study material for Quant and VARC
3. Something about previous year papers

**Analysis:**
- ✅ Got right: Free PYQ access — this clearly communicated
- ❌ Misunderstood: Treated the platform like an online library/content bank (like Unacademy free content), not as a personalised prep system
- ❌ Missed entirely: AI-powered personalisation, study plans, score prediction entirely missed

**Insight:** Users with no prior structured prep treat every platform as "more content." The onboarding doesn't successfully differentiate Optima Learn's AI layer from a simple question bank. The *so what* of personalisation isn't landing.

---

### User 3 — Tushar (Practice Stage, DILR-focused)

**What he wrote:**
1. Lots of DILR and Quant sets to solve
2. Previous CAT papers (PYQs)
3. Analytics or performance tracking of some kind

**Analysis:**
- ✅ Got right: DILR/Quant content depth, PYQ access
- ✅ Partially right: Noticed performance tracking but couldn't describe it clearly
- ❌ Missed: Personalised roadmap, mock interviews, score prediction

**Insight:** More advanced users engage deeper and notice features like analytics — but even Tushar couldn't articulate *how* the platform tells him what to study next. The intelligence is there, but invisible to the user.

---

### User 4 — Aryan Mehra (Working Professional, consistency issues)

**What he wrote:**
1. CAT mock tests
2. Practice sets for Quant
3. A study planner or schedule thing (not sure if it's AI or manual)

**Analysis:**
- ✅ Got right: Mocks and Quant practice
- ❌ Misunderstood: Described the study planner as "not sure if it's AI or manual" — the AI element was unclear
- ❌ Missed: Personalisation to his specific time constraints (he has only 1 hour/day — this is a huge user need and the platform doesn't visibly address it)

**Insight:** The product's core value — *replacing generic plans with your personalised roadmap* — is not felt in the first impression. Users see content, not a system that understands them.

---

### User 5 — Narendra Sharma (Language Immersion, small-town)

**What he wrote:**
1. English practice for CAT
2. Questions and tests
3. Maybe vocabulary or reading help?

**Analysis:**
- ✅ Got right: English/VARC focus
- ❌ Missed: Everything beyond VARC content — Quant, DILR, mocks, planning, AI features
- ❌ Missed entirely: The platform's differentiation from a static study site

**Insight:** First-generation aspirants from non-metro backgrounds anchor on what they need most (English help) and don't explore further. The onboarding doesn't guide discovery — users with lower platform literacy drop off after finding one thing that matches their need.

---

### Aggregate Findings

| Feature | Users who identified it correctly | Users who missed it |
|---|---|---|
| PYQ / Practice Questions | 5/5 | 0 |
| Mock Tests | 4/5 | 1 |
| AI Personalisation / Study Plan | 1/5 | 4 |
| Score Prediction | 0/5 | 5 |
| Mock Interviews | 0/5 | 5 |
| Daily Roadmap | 0/5 | 5 |

### What This Tells Us

**Messaging problem:** "Stop Guessing What to Study" is the headline — but users still left guessing what the *platform* does beyond content. The hero message promises clarity, but the product experience doesn't deliver the *aha moment* of personalisation fast enough.

**Onboarding gap:** All 5 users completed the signup form but still couldn't articulate the AI layer. This means the onboarding captures data but doesn't visibly *use* it in a way that the user can feel. There is no moment where the user thinks: *"oh, this platform actually knows me."*

**Content vs. System perception:** Every user perceived Optima Learn as a content platform (like a question bank) rather than an intelligent prep system. This is the core positioning gap. The AI does work — but it's invisible.

**Recommendation:** Introduce a post-onboarding "Your Plan is Ready" moment — where the AI immediately generates a personalised first-day study plan based on the onboarding data. This single change would make the AI layer tangible and memorable in the first session.

---

## TASK 4 — Prototype

### Problem Statement

**"I don't know what to study today."**

Across 10 user conversations, 7 out of 10 students cited some version of this as their top frustration:
- Priya: *"Doesn't know what to study and in what order."*
- Naveen: *"No fixed study plan yet, still deciding."*
- Ishwar: *"No fixed study plan yet, still deciding."*
- Prince: *"Information overload — too many PDFs, doesn't know which to trust."*
- Aryan: *"Zero consistency — work meetings kill the schedule."*

This is not a content problem. Optima Learn has 20,000+ questions. The problem is **prioritisation and daily structure** — students know *what* exists, they don't know *what to do right now*, given their time, weak areas, and exam date.

---

### Why This Isn't Currently Solved by Optima Learn

Optima Learn offers personalised study plans and a daily roadmap — but based on usability testing, **0 out of 5 users could identify or articulate this feature** after an unguided session. The feature either:
1. Exists but isn't surfaced prominently enough post-onboarding
2. Isn't personalised dynamically to daily constraints (like "I only have 1 hour today" or "I have a mock tomorrow")

There is no tool that the student can interact with in <60 seconds to get a concrete, actionable daily schedule that accounts for their specific weak areas + the time they have *today*.

---

### The Prototype: CAT AI Daily Study Planner

**Live file:** `cat_daily_planner_prototype.html` (open in browser)

A Claude-powered AI tool where a student inputs:
- Their name and exam date
- Prep stage (just started / mid-prep / advanced / revision)
- Time available today (1–4+ hours)
- Their specific weak areas (checkboxes: RC, Algebra, DILR, etc.)
- Any additional context ("mock test tomorrow", "haven't done VARC in 2 weeks")

The AI generates a **fully personalised, session-by-session daily study plan** with:
- A named theme for the day (e.g. "RC Domination Day")
- Specific sessions with duration, section tag, and 3 concrete tasks each
- A coach's motivational note tailored to their stage

**It works. Open the HTML file in any browser.**

---

### How It Integrates Into Optima Learn

This feature would sit as a **persistent "Today's Plan" card** on the Optima Learn dashboard — generated fresh each morning using:
- The student's diagnostic data from onboarding
- Their performance on recent mocks (which sections they underperformed)
- Their self-reported time availability (a simple "how much time do you have today?" input each morning)
- Days remaining to CAT

Over time, the plan becomes more intelligent — it tracks what was completed, adjusts for where the student is plateauing, and escalates intensity as exam day approaches.

This directly solves the #1 user pain point found in research — and makes Optima Learn's AI layer *visible and felt* from day one.

---

## 200-WORD SUBMISSION NOTE

*What surprised you the most from talking to users?*

The most surprising discovery wasn't a specific pain point — it was the emotional weight behind a very simple problem: not knowing what to study today.

I expected users to talk about content gaps, difficulty of questions, or expensive coaching. Instead, almost every conversation kept returning to the same quiet frustration: they had everything they needed — books, apps, YouTube channels, coaching — and still sat down each day unsure where to start. The problem wasn't resources. It was prioritisation paralysis.

What surprised me even more was how this affected confidence. Students weren't just wasting time — they were interpreting their own indecision as evidence that they weren't serious enough, or smart enough. The lack of structure was doing psychological damage, not just logistical.

The second surprise came from usability testing. Optima Learn clearly has strong AI features — but not a single user could identify the personalised plan feature after exploring the platform on their own. The intelligence exists. The moment where the user *feels* it, doesn't.

That gap — between what the product does and what the user experiences — is the exact thing worth fixing. And it's entirely fixable.

---
*Submitted by: Kunal Chaudhary*
*Email: ashwin@optimalearn.com*
*Subject: AI PM Intern Assignment
