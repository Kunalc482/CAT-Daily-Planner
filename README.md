# CAT AI Daily Study Planner
### Built by Kunal Chaudhary — Associate Product Manager

A Claude-powered daily study planner for CAT (Common Admission Test) aspirants. Built as part of an AI PM Intern Assignment for Optima Learn — directly solving the #1 pain point found across 10 user interviews: *"I don't know what to study today."*

**Live Demo:** [Coming soon — deploy via GitHub Pages]

---

## The Problem This Solves

After conducting 10 user interviews and 5 usability tests on Optima Learn (a CAT prep platform), one finding was consistent across 7 out of 10 students:

> *"I have everything — books, apps, coaching — but I still sit down every day unsure where to start."*

This isn't a content problem. Optima Learn has 20,000+ questions. The problem is **prioritisation and daily structure**. Students know what exists. They don't know what to do *right now*, given their time, weak areas, and exam date.

---

## What It Does

The student inputs:
- Their name and CAT exam date
- Prep stage (Just Started / Mid-Prep / Advanced / Revision)
- Time available today (1 hour to 4+ hours)
- Specific weak areas (RC, Algebra, DILR, Parajumbles, etc.)
- Any extra context ("mock test tomorrow", "haven't touched VARC in 2 weeks")

The AI generates:
- A **named theme for the day** (e.g. "RC Domination Day")
- **Session-by-session plan** with duration, section tag, and 3 concrete tasks per session
- A **personalised coach's note** tailored to their prep stage and context

---

## Research Behind It

This prototype emerged from a structured PM research process:

| Research Activity | Finding |
|---|---|
| 10 user interviews | 7/10 cited "don't know what to study" as top frustration |
| 5 usability tests on Optima Learn | 0/5 users identified the AI personalisation feature |
| Aggregate analysis | Score prediction, daily roadmap, mock interviews — all missed by every user |

**Root cause:** The platform's AI works — but it's invisible to the user. There is no moment where the student thinks: *"This platform actually knows me."*

This planner creates that moment.

---

## How It Integrates Into a Real Product

In a production context, this feature would sit as a **persistent "Today's Plan" card** on the Optima Learn dashboard, generated fresh each morning using:
- Diagnostic data from onboarding
- Performance on recent mock tests
- Self-reported daily time availability
- Days remaining to CAT exam date

Over time it becomes more intelligent — tracking completion, adjusting for plateaus, and escalating intensity as exam day approaches.

---

## Tech Stack

| Layer | Tool |
|---|---|
| AI Model | Claude (Anthropic API) — `claude-sonnet-4-20250514` |
| Prompt Design | Context-aware prompt with structured plan output |
| Frontend | Vanilla HTML + CSS + JavaScript |
| Backend | None — runs entirely in the browser |

---

## How to Run

1. Clone or download this repo
2. Open `cat-daily-planner.html` in any browser
3. Enter your Anthropic API key (get one at [console.anthropic.com](https://console.anthropic.com))
4. Fill in your details and click **Generate My Plan**

---

## PM Context

This project demonstrates the full PM loop:
- **Discovery:** 10 user interviews to find the real problem
- **Definition:** Usability testing to validate the gap
- **Solution design:** Identified the minimum feature that creates the "aha moment"
- **Execution:** Shipped a working Claude-powered prototype with zero backend

The goal wasn't to build a full app. It was to make the AI layer *visible and felt* — and prove the concept works before investing in infrastructure.

---

## Related Work

This prototype was submitted as part of the **Optima Learn AI PM Intern Assignment**, which included:
- Task 3: Usability test findings across 5 users
- Task 4: Problem statement, prototype, and integration roadmap

Full write-up: [`optima_learn_submission_tasks3_4.md`](./optima_learn_submission_tasks3_4.md)

---

## Author

**Kunal Chaudhary**
Associate Product Manager | B.Tech ECE (AI/ML) — NSUT Delhi
kunalc4820@gmail.com | [LinkedIn](https://linkedin.com/in/kunalchaudhary) | [Portfolio](https://kunalc482.lovable.app)
