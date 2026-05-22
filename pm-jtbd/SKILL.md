---
name: jtbd
description: >
  Apply Jobs-to-be-Done (Ulwick/ODI) methodology to product work. Use this skill whenever the user
  wants to map features or requirements to customer jobs, write JTBD job statements, score opportunity
  areas, analyze research or transcripts through a JTBD lens, build a job map, or prioritize a roadmap
  using outcome-driven innovation. Trigger on phrases like "map this to jobs", "what job does this
  feature serve", "write a JTBD statement", "opportunity scoring", "job map", "reframe this as a job",
  "what outcome does this address", or any request to connect product decisions to customer motivations.
  Also trigger when the user shares transcripts, notes, feature lists, or PRDs and wants to extract
  or validate the underlying jobs. Do not wait for the user to say "JTBD" explicitly — if they're
  trying to understand why customers want something or whether a feature is worth building, this skill applies.
---

# Jobs-to-be-Done (Ulwick/ODI) Skill

## Framework Overview

Outcome-Driven Innovation (ODI) defines jobs at three levels:

1. **Functional job** — the core task the customer is trying to accomplish ("get from A to B")
2. **Desired outcomes** — the metrics customers use to judge how well the job is done (speed, predictability, effort, risk)
3. **Opportunity score** — a prioritization formula that reveals where outcomes are underserved

The goal is to move from "what do customers say they want" to "what job are they trying to get done and which outcomes are unmet" — then map features/investments against those gaps.

---

## Core Output Formats

### Functional Job Statement
**Structure:** [Verb] + [object of the verb] + [contextual clarifier]

Examples:
- "Minimize the time it takes to verify a clinician's credentials before their first session"
- "Ensure a caregiver receives session reminders without needing to check the app"
- "Reduce the risk of billing errors when a session length deviates from the scheduled time"

Avoid solution language. "Schedule a session via the app" is a solution. "Get a session on the calendar at a time that works" is a job.

### Desired Outcome Statement
**Structure:** [Direction] + [metric] + [object] + [contextual clarifier]

Direction is always: Minimize / Maximize / Increase / Decrease / Reduce

Examples:
- "Minimize the likelihood that a session is missed due to a scheduling conflict"
- "Reduce the time it takes to identify which caregivers haven't completed onboarding"
- "Minimize the number of manual steps required to update a clinician's availability"

### Opportunity Score
**Formula:** Importance + max(Importance − Satisfaction, 0)

Score interpretation:
- **10+**: Extreme opportunity — underserved and critical
- **7–9**: Strong opportunity — worth prioritizing
- **5–6**: Moderate — table stakes, not differentiating
- **<5**: Overserved — reduce investment

When you don't have survey data, derive importance and satisfaction qualitatively from the input (transcripts, notes, PRDs) using the signals below.

---

## Workflow by Input Type

### Input: Raw Interview Transcripts or Notes

1. **Extract job candidates** — scan for struggle language ("I have to...", "I wish...", "every time I...", "it's annoying when..."), workarounds, and emotional friction
2. **Cluster by functional job** — group related pain points under the job they serve
3. **Write desired outcome statements** for each cluster
4. **Estimate opportunity** — infer importance (how often mentioned, how strongly) and satisfaction (are they working around it? is there a manual step?)
5. **Output a job map** — ordered list of functional jobs with associated outcomes and opportunity scores

### Input: Feature List or Requirements

1. **Reframe each feature as the job it serves** — strip solution language, identify the underlying outcome
2. **Identify which job layer it addresses** — functional job, desired outcome, or job step
3. **Flag job coverage gaps** — are there high-opportunity outcomes with no feature addressing them?
4. **Flag overinvestment** — are multiple features serving the same low-opportunity outcome?
5. **Output a feature-to-job mapping table** with coverage assessment

### Input: PRD or Product Brief

1. **Extract the stated problem** and rewrite it as a functional job statement
2. **Identify implied desired outcomes** in the success metrics or user stories
3. **Challenge solution assumptions** — does this feature actually address the highest-opportunity outcome for this job, or a lower one?
4. **Write a JTBD framing section** the team can use to anchor the brief

---

## Job Map Structure

A job map breaks the functional job into sequential steps. Use this when the user needs to understand the full job landscape, not just a single outcome.

Standard job map phases (adapt to context):
1. **Define** — determine goals and plan resources
2. **Locate** — gather items and information needed
3. **Prepare** — set up the environment
4. **Confirm** — verify readiness
5. **Execute** — carry out the job
6. **Monitor** — evaluate progress
7. **Modify** — make adjustments
8. **Conclude** — finish and follow up

For each phase: identify 2–4 desired outcomes. Score each. Highlight the top opportunities.

---

## Output Guidelines

**Default output** for most requests: a prioritized list of functional jobs + desired outcomes + opportunity scores, followed by implications for the feature/roadmap in question.

**When mapping features to jobs:** use a two-column structure — feature/requirement on the left, job/outcome it serves on the right — followed by a gap/overlap analysis in prose.

**When writing statements only:** deliver clean job statements with brief rationale. Don't pad with framework explanation unless the user asks.

**Tone:** Write job statements in plain language, from the customer's point of view. Avoid internal jargon. A caregiver's job is not "complete onboarding" — it's "get my child started with a therapist as quickly as possible."

---

## Common Mistakes to Catch and Correct

- **Solution-as-job**: "Use the scheduling tool to book a session" → rewrite as the underlying job
- **Activity-as-outcome**: "Complete the intake form" is a step, not an outcome — push to the result ("Ensure nothing is missing before the first session")
- **Vague direction**: "Improve communication" is not a job statement — force specificity on what dimension of communication and in what context
- **Feature-first framing in PRDs**: if a PRD leads with the solution and buries the job, surface it explicitly before proceeding

---

## Reference Files

- `references/odi-deep-dive.md` — Ulwick's full ODI framework detail, interview question templates, and survey design for quantitative opportunity scoring
- `references/jtbd-examples.md` — Worked examples across SaaS, marketplace, and healthcare contexts

Read these when the user needs deeper methodology support or example-driven guidance.
