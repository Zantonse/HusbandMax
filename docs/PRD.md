# HusbandMax — Product Requirements Document

**Status:** Draft v0.4
**Owner:** Craig
**Last updated:** 2026-10-16

---

## 1. Summary

HusbandMax is a personal coaching app that helps a husband become a more considerate partner and take on a real share of the household **mental load**: the invisible work of noticing, anticipating, planning, deciding, and following through that keeps a home and a relationship running.

Most "chore apps" split tasks. That misses the point. The hard part of mental load isn't doing the dishes when asked; it's being the person who *notices* the dishes, the dentist appointment, the birthday next week, and the fact that your partner seems stressed, without being told. HusbandMax trains that noticing-and-owning muscle through three things:

1. **A shared map of the household's invisible work**, so the load becomes visible and can be deliberately rebalanced.
2. **Ownership, not assistance**: tasks are handed over *end to end* (notice → plan → do → follow up), and the app helps him carry the whole thing.
3. **Daily micro-coaching** on consideration: small prompts, reflections, and lessons that build habits over weeks.

## 2. Problem

- In many households one partner (often the wife) carries most of the cognitive and emotional labor: remembering, scheduling, anticipating needs, and delegating. Even when the other partner "helps," she still has to manage him, which is itself load.
- Well-meaning husbands often don't see the work because it's invisible, and asking "just tell me what to do" keeps her in the manager role.
- Consideration (noticing moods, remembering what matters to her, doing small thoughtful things unprompted) is a skill, but there is no structured, low-friction way to practice it.
- Generic relationship content (books, podcasts) is inspiring but doesn't translate into daily behavior change.

## 3. Goals and non-goals

### Goals
- **G1. Make the invisible visible.** Help the couple inventory household and relational responsibilities, and see who currently owns each one.
- **G2. Shift real ownership.** Help him take over whole areas of responsibility, not one-off chores, and sustain them.
- **G3. Build consideration habits.** Through daily nudges and reflection, increase unprompted thoughtful actions.
- **G4. Measure what matters from her side.** Progress is judged by whether *she* feels the load is lighter, not by how many boxes he ticks.

### Non-goals (v1)
- Not couples therapy, and not a substitute for it. The app will point to professional help where appropriate.
- Not a general family calendar or a full replacement for existing tools (Google Calendar, Apple Reminders); integrate rather than replace.
- Not a scorekeeping or "who did more" tool. Tallies that invite conflict are deliberately avoided.
- Not built for children's accounts or multi-adult households in v1.

## 4. Users

| Persona | Description | What they need |
|---|---|---|
| **Primary: the Husband ("Learner")** | Motivated to do better, may not know where the gaps are. Busy, phone-first, responds to clear plans and progress. | A clear picture of what to own, reminders that build anticipation rather than replace it, short practical coaching, and a sense of progress. |
| **Secondary: the Wife ("Partner")** | Carries much of the load today. Has little appetite for another app to manage. | A very light way to share what matters, see ownership shift, and give feedback, without becoming his project manager. |

Design principle that follows from this: **every interaction asked of the Partner must take under a minute and be optional.** If the app creates work for her, it has failed.

## 5. Core concepts

- **Domain:** an area of household life (e.g., Kids' school, Meals, Finances, Social calendar, Home maintenance, Health appointments, Gifts & occasions, Her wellbeing).
- **Responsibility:** a recurring piece of work inside a domain (e.g., "Plan weekly meals," "Track kids' school forms," "Book annual car service"). Each has an owner and covers the full cycle: *notice, plan, execute, follow up*.
- **Handoff:** moving ownership of a responsibility from Partner to Learner, with a short context transfer ("here's how I usually do it, here's what matters").
- **Nudge:** a timely, anticipatory prompt ("Her mom's birthday is in 10 days. What's the plan?") that asks him to *think*, not just tick.
- **Lesson:** a 2–5 minute coaching unit on a consideration skill (e.g., "Noticing bids for connection," "Planning ahead vs. reacting," "Following up without being asked").
- **Check-in:** a lightweight weekly signal from the Partner on how the load feels.

## 6. Features

Priority: **P0** = MVP, **P1** = fast follow, **P2** = later.

### 6.1 Onboarding and Mental Load Audit (P0)
- Guided audit with a starter library of ~80 common responsibilities across ~10 domains; add custom ones.
- Each partner marks, separately, who currently owns each responsibility (Me / Partner / Shared / Nobody) and how much it weighs on them. The Partner's side can be done in ~5 minutes or skipped.
- Output: a **Load Map** showing the current split by domain, with mismatches highlighted (e.g., he thinks it's "Shared," she thinks it's hers).
- Single-player mode: Learner can complete the audit alone, with the app guiding him to estimate honestly, and invite his partner later.
- **Launch domains (v1 focus):** Kids, Meals, Gifts & occasions, and Home admin are seeded first and suggested for early handoffs. The Kids domain is tuned for **one toddler (age 2)**: daycare/childcare logistics, pediatrician well visits and vaccines, sleep and nap routines, clothes and diaper sizing, activities and playdates, and milestone prep (potty training, toddler-bed move). Social calendar is seeded as **Shared**, since Craig already carries part of it; the audit should split it into specific responsibilities (e.g., "RSVPs and kid birthday parties" vs. "planning our weekends with friends") to find the parts still sitting with her.

### 6.2 Ownership Plan (P0)
- App suggests 2–3 responsibilities to take over first, favoring ones that are high-weight for her, recurring, and achievable.
- **Handoff flow:** Partner can optionally add notes ("the pediatrician's office only answers before 10am"). Once handed off, she's out of the loop by default.
- Each owned responsibility gets a **playbook**: what "done well" looks like, cadence, lead times, and a checklist for the full notice → follow-up cycle.
- Gradual pacing: add a new responsibility only once current ones are stable (e.g., 3 consecutive cycles on time).

### 6.3 Anticipation Nudges (P0)
- Nudges fire *ahead* of need, with lead time appropriate to the task (gift: 2 weeks; school form: 3 days; groceries: day before).
- Nudges ask a question rather than issuing an order, to train anticipation: "Week ahead: anything she has on that you could take off her plate?"
- Daily digest (morning) plus a small number of time-sensitive pushes. User sets quiet hours and a max-per-day cap.

### 6.4 Consideration Coach (P0)
- Daily 2-minute lesson or prompt, organized in tracks (e.g., *Foundations of mental load*, *Noticing*, *Emotional labor*, *Planning ahead*, *Thoughtful gestures*, *Repair after a miss*).
- **Daily practice prompt:** one small, concrete action ("Ask her about the thing she was worried about yesterday").
- **Evening reflection** (30 seconds): Did I notice something today without being told? What did I own end to end?
- **Content approach:** an original HusbandMax curriculum, drafted with AI and reviewed and approved by Craig before it ships. Lessons draw on established ideas (e.g., Eve Rodsky's *Fair Play* split of conception/planning/execution, Gottman's "bids for connection") with attribution, but don't reproduce any book's material.

### 6.5 "Things She Cares About" Memory (P0)
- A private notebook of what matters to her: preferences, upcoming events, stressors she's mentioned, favorite things, sizes, people's names.
- Quick capture ("She mentioned her boss is giving her a hard time") with optional follow-up reminder ("Ask how it went on Thursday").
- Feeds nudges and gift/occasion planning.

### 6.6 Partner Check-in (P1)
- Weekly one-tap check-in for the Partner: "How heavy did the load feel this week?" (1–5) plus an optional note or "one thing that would help."
- Learner sees trends, not individual scores out of context, and gets coaching suggestions based on them.
- Partner can also send a **"Thank you / noticed that"** micro-acknowledgment.

### 6.7 Progress & Insights (P1)
- Load Map re-run every 4–6 weeks to show the shift over time.
- Streaks for reflections and on-time responsibilities (gentle, no shaming for breaks).
- Monthly summary: domains owned, cycles completed without prompting, Partner check-in trend.

### 6.8 AI Coach Chat (P1)
- Conversational coach (LLM-powered) for situations: "She seemed upset after dinner, what could I do?", "Help me plan a low-key anniversary," "I dropped the ball on the school form, how do I own it?"
- Has context from the Load Map, owned responsibilities, and the "Things She Cares About" notebook, with user control over what's shared.
- Safety: recognizes signs of serious conflict, abuse, or mental health crisis and points to appropriate professional resources rather than coaching through them.

### 6.9 Integrations (P1–P2)
- Calendar read/write (Google, Apple) for scheduling owned tasks and seeing her commitments (with consent). **P1**
- Shared grocery/meal planning list. **P2**
- Smart suggestions from calendar (e.g., "She has three late meetings this week. Take dinner Tuesday and Thursday?"). **P2**

## 7. Key user flows

1. **First week:** Install → short intro to mental load (2 min) → solo audit → Load Map → pick first 2 responsibilities → invite partner (optional) → first daily lesson.
2. **Daily loop:** Morning digest (owned tasks due, one anticipation nudge, one practice prompt) → do things through the day → 30-second evening reflection.
3. **Handoff:** Learner proposes taking over a responsibility → Partner gets a one-tap "Yes, and here's anything I'd want you to know" → responsibility moves to Learner with playbook.
4. **Weekly loop:** Partner check-in → Learner gets a weekly review: what went well, what slipped, one focus for next week.

## 8. Success metrics

**North star:** Partner-reported load lightness (weekly check-in score) improving over 8 weeks.

Supporting metrics:
- Responsibilities fully owned by the Learner (count, and % of high-weight ones).
- % of owned-task cycles completed on time *without* a last-minute nudge (measures true anticipation, not reminder-following).
- Reflection completion rate (habit formation).
- Partner effort: median Partner time-in-app per week (target: under 3 minutes).
- Retention: D30 and D90 for Learners.

## 9. Platform and technical approach (proposed)

- **Client:** Web and phone from day one. Proposed: React Native (Expo) with Expo Router, which builds iOS, Android, and web from one codebase. The Partner can use the web version without installing anything.
- **Built for one household, ready for many:** v1 serves Craig's household only, but the data model is multi-household (all data lives under `households/{householdId}`, enforced by Firestore security rules) so it can open to other husbands later without a rewrite.
- **Backend: Firebase** (decided). A hosted backend is needed because two people on separate devices share the same household data, and nudges must be sent on a schedule even when the app is closed. Firebase covers it with Firestore (database, live sync between both phones, offline cache), Firebase Auth (sign-in for Craig and his wife), Security Rules (keep the Learner's private notebook and reflections private), and scheduled Cloud Functions (nudges, weekly check-in prompts). Scheduled functions require the pay-as-you-go Blaze plan; at one household's usage this should stay within the free quota, but set a budget alert.
- **Notifications:** Firebase Cloud Messaging (via Expo push) triggered by scheduled Cloud Functions.
- **AI:** Claude API for the coach chat, lesson personalization, and weekly summaries.
- **Data model (initial, Firestore):** `households/{id}` with subcollections `members`, `domains`, `responsibilities` (owner, cadence, lead_time, playbook), `taskCycles`, `nudges`, `checkins`; per-user private data under `users/{uid}`: `reflections`, `partnerNotes` (the "Things She Cares About" notebook), `lessonProgress`. Lesson content lives in a top-level `lessons` collection. The Claude API key stays server-side in Cloud Functions, never in the app.

## 10. Privacy, trust, and tone

- The "Things She Cares About" notebook and reflections are **private to the Learner by default.** Nothing is shared with the Partner without an explicit action.
- Partner check-ins are visible only to the household.
- No selling or ad use of relationship data. Data export and full deletion are available.
- Tone: **earnest coach**. Warm, sincere, and direct; encouraging without jokes getting in the way; never preachy or shaming. Framing is "becoming the partner you want to be," not "you're failing."
- Avoid gamification that turns care into points-for-rewards with the Partner as judge.

## 11. Release plan

| Phase | Scope | Goal |
|---|---|---|
| **1. MVP (Craig's household)** | Web app **and** phone app (iOS + Android) from day one, one shared codebase. Learner: audit, Load Map, ownership plan, nudges, daily lesson, reflection, notebook. Partner: invite, audit, handoffs, weekly check-in. Launch domains: Kids, Meals, Gifts, Home admin, Social (shared). | Dogfood for 6–8 weeks; validate the daily loop and that Partner-reported load improves. |
| **2. Coach** | AI coach chat, calendar integration, progress insights. | Deepen engagement and personalization. |
| **3. Share with other husbands** | Multi-household onboarding, generic starter library, more content tracks, smart calendar suggestions. | Open to other couples once it works in Craig's household. |

## 12. Risks

- **The app itself becomes load for her.** Mitigation: Partner actions are optional and under a minute; single-player mode works fully.
- **Reminder dependency instead of real anticipation.** Mitigation: nudges ask questions, lead time shrinks as he gets consistent, metric tracks unprompted completions.
- **Scorekeeping and conflict.** Mitigation: no side-by-side tallies; show trends and her experience, not his effort points.
- **Content credibility and IP.** Mitigation: original content inspired by cited frameworks; review licensing before using any named system.
- **Sensitive situations.** Mitigation: AI coach safety guardrails and links to professional resources.

## 13. Decisions made

- **Audience:** Built for Craig first; designed to share with other husbands later (Phase 3).
- **Partner involvement:** Craig's wife will use the Partner side (audit, handoffs, weekly check-in). Single-player mode stays as a fallback for future users.
- **Platform:** Web and phone app in the first version.
- **Launch domains:** Kids, Meals, Gifts & occasions, Home admin, and Social calendar (partly owned by Craig already).
- **Household:** One child, age 2.
- **Lessons:** Original curriculum, drafted with AI and reviewed by Craig.
- **Tone:** Earnest coach.
- **Backend:** Firebase (Craig's free Supabase slot is already used by another app).

## 14. Open questions for Craig

None right now. Next step is to scaffold the app.
