# ODI Deep Dive Reference

## The Full ODI Framework (8 Steps)

1. **Define the market** — identify the job executor (who performs the job) and the job itself
2. **Uncover desired outcomes** — 50–150 outcome statements per job is normal at full scale
3. **Quantify the opportunity** — survey for importance and satisfaction
4. **Segment the market** — group customers by underserved outcomes, not demographics
5. **Target the segments** — decide which underserved segments to pursue
6. **Position the offering** — align messaging to the job and outcomes you serve best
7. **Conduct competitive analysis** — map competitors' features to outcomes to find gaps
8. **Define the product/service strategy** — invest where opportunity scores are highest

For most product work, steps 1–4 are the relevant core. Steps 5–8 are strategy/GTM territory.

---

## Interview Question Templates

### Switch Interview (understanding the job in context)
- "Walk me through the last time you had to [job]. What triggered it?"
- "What were you doing before you found this solution?"
- "What made that approach frustrating?"
- "What were you hoping would be different?"
- "What almost stopped you from switching?"

### Outcome Elicitation
- "When you're doing [job], what does 'done well' look like to you?"
- "What would make this faster / less risky / require less effort?"
- "What could go wrong that you're trying to avoid?"
- "How do you know when you've done this successfully?"
- "What takes the most time? What do you have to redo most often?"

### Importance vs. Satisfaction Probes
- "How important is it that [outcome]?" (1–10)
- "How satisfied are you today with how well [outcome] is achieved?" (1–10)

---

## Survey Design for Quantitative Opportunity Scoring

When running a quantitative study:

**Sample size**: 30+ for directional signal; 100+ for segmentation
**Scale**: 1–10 for both importance and satisfaction
**Question framing**:
- Importance: "When [job], how important is it to [outcome]?" (1 = not important, 10 = extremely important)
- Satisfaction: "How satisfied are you with how well existing solutions allow you to [outcome]?" (1 = not satisfied, 10 = completely satisfied)

**Opportunity score formula**: `Importance + max(Importance - Satisfaction, 0)`

**Reporting**: Sort by opportunity score descending. Flag anything ≥ 10 as a strategic priority. Group 7–9 as strong candidates. Treat < 5 as evidence of overinvestment.

---

## Qualitative Opportunity Estimation (No Survey Data)

When working from transcripts, notes, or observation:

**Proxy for importance:**
- Mentioned unprompted across multiple participants
- Associated with emotional language (frustration, anxiety, relief when resolved)
- Connected to a downstream consequence ("if this goes wrong, then...")
- Described as blocking or delaying other jobs

**Proxy for satisfaction:**
- Workarounds present → low satisfaction
- Manual steps in an otherwise automated flow → low satisfaction
- Described as "the way it works" with resignation → moderate satisfaction
- Explicit praise, described as solved → high satisfaction

Use a 1–10 scale for both even when estimating. Be transparent that scores are qualitative estimates. Mark them as QE (qualitative estimate) vs. QN (quantitative/survey-based).

---

## Outcome Statement Writing Rules

1. Start with a direction word: Minimize, Maximize, Reduce, Increase
2. Name the metric: time, likelihood, frequency, number of steps, risk, cost, effort
3. Identify the object: what is being measured
4. Add a clarifier: in what context or under what conditions

**Bad**: "Easy to schedule"
**Good**: "Minimize the number of steps required to reschedule a session after a cancellation"

**Bad**: "Improve communication with caregivers"
**Good**: "Reduce the likelihood that a caregiver misses a session due to not receiving a reminder"

Aim for 2–4 outcomes per job step in a job map. At the functional job level, 8–15 outcomes is a reasonable working set for most product contexts.
