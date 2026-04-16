# Skills · DESIGN.md

How to write a well-formed DESIGN.md — the design context file
consumed by Stitch, the Anthropic design tool, and Claude Code
when generating or refining UI.

DESIGN.md is to design what CLAUDE.md is to code. It gives any
AI design tool enough context to generate UI that is coherent
with the product's intent, user, and principles — without
having to ask.

---

## Structure

```
# Design context: [product name]

## What this product is
[1 paragraph: what it does, who it's for, what job it performs]

## The user we're designing for
[Human description with emotional context — from the Design Agent.
Not a demographic. A person with a situation, motivations, and
feelings about the problem being solved.]

## How they should feel using this
[3 emotional qualities. Not visual descriptors — emotional ones.
"Confident, not overwhelmed" rather than "clean and minimal"]

## Design principles
[3–5 principles derived from the user research, not generic best practice.
Format: **Principle name:** What this means in practice for this product.]

## Visual direction
[Tone and aesthetic intent. What this should feel like.
What it should not feel like. Any specific references if helpful.]

## Key screens / surfaces
[List of the primary UI surfaces this product needs.
Each with one sentence on its purpose.]

## What to avoid
[Specific patterns or aesthetics that would be wrong for this product
and this user — with a brief reason why]
```

---

## Example (illustrative)

```
# Design context: focus-app

## What this product is
A lightweight focus timer for independent workers who struggle to
protect deep work time in unstructured days. It helps them start
focused sessions quickly and track where their time actually went.

## The user we're designing for
A freelance designer in her early 30s. She works from home and
loves the autonomy but loses hours to low-value tasks without
noticing. She feels vaguely guilty most afternoons. She has tried
every productivity app and abandoned all of them within two weeks.
She is sceptical of tools that feel like homework.

## How they should feel using this
- **In control** — not managed by the app, using it deliberately
- **Unencumbered** — starting a session should feel like clearing
  the desk, not filling out a form
- **Lightly accountable** — aware of where time went without
  being judged for it

## Design principles
- **Fast to start:** The path from "I want to focus" to "I'm focusing"
  should be two taps maximum
- **No guilt architecture:** History and data should inform, not accuse
- **Get out of the way:** During a session the UI should nearly disappear

## Visual direction
Calm, minimal, considered. Think text-first, lots of whitespace.
Not clinical — warm but unfussy. No gamification, no streaks,
no badges. Avoid dashboard-heavy layouts.

## Key screens / surfaces
- Session start: select duration, start — nothing else
- Active session: large timer, one button to end early
- End of session: brief summary, option to log what you worked on
- History: simple weekly view of where time went

## What to avoid
- Onboarding flows longer than 2 steps
- Any pattern that requires the user to "manage" the app
- Notification-heavy patterns
- Anything that feels like a Pomodoro app
```
