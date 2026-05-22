# JTBD Worked Examples

## Example 1: Healthcare / Telehealth (Care Operations)

**Context**: Mapping features for a BCBA scheduling and credentialing product

### Functional Jobs (credentialing context)
- Ensure a new clinician is authorized to see patients before their first session
- Minimize the risk of a lapsed credential going unnoticed until it causes a compliance issue
- Reduce the time it takes to track down missing documentation from a clinician

### Desired Outcomes (for job: "ensure clinician is authorized before first session")
| Outcome Statement | Importance (QE) | Satisfaction (QE) | Opp Score |
|---|---|---|---|
| Minimize the likelihood that a session is scheduled before credentials are verified | 9 | 4 | 14 |
| Reduce the time required to chase down missing documents from a clinician | 8 | 3 | 13 |
| Minimize the number of manual steps to update a clinician's status after verification | 7 | 4 | 10 |
| Reduce the likelihood that a credential expiration is missed before it lapses | 9 | 5 | 13 |
| Minimize the effort required to understand what's blocking a clinician from being cleared | 8 | 4 | 12 |

### Feature-to-Job Mapping
| Feature / Requirement | Job It Serves | Outcome Addressed | Coverage Assessment |
|---|---|---|---|
| Automated credential expiration alerts | Ensure clinician remains authorized | Reduce likelihood of missed expiration | Strong — directly addresses opp score 13 |
| Document upload portal for clinicians | Ensure authorized before first session | Reduce time to collect missing docs | Partial — upload helps but follow-up is still manual |
| Status dashboard for credentialing ops | Ensure authorized before first session | Minimize effort to understand what's blocking | Addresses the outcome but needs clear status taxonomy |
| Medallion / Verifiable integration | Both | Multiple outcomes | High leverage — addresses 3 outcomes simultaneously |

---

## Example 2: SaaS / Marketplace

**Context**: Mapping a proposed notification feature for a talent marketplace

### Functional Job
"Stay informed about candidate pipeline status without having to manually check the platform"

### Desired Outcomes
| Outcome Statement | Importance (QE) | Satisfaction (QE) | Opp Score |
|---|---|---|---|
| Minimize time spent logging in just to check if something has changed | 8 | 3 | 13 |
| Reduce the likelihood of missing a time-sensitive candidate action | 9 | 4 | 14 |
| Minimize the number of irrelevant notifications received | 7 | 5 | 9 |
| Reduce the cognitive load of understanding what requires action vs. FYI | 8 | 4 | 12 |

### PRD Reframe
**Original problem statement in PRD**: "Users need a notification system so they know what's happening."

**Reframed as JTBD**: The job is "stay informed about pipeline status without checking manually." The highest-opportunity outcome is "reduce the likelihood of missing a time-sensitive action" (score: 14). The second-highest is "reduce cognitive load distinguishing action-required from informational" (score: 12).

**Implication**: The feature shouldn't just send more notifications — it needs to triage them. A system that sends everything equally is likely to degrade satisfaction on the "irrelevant notifications" outcome (score: 9), which will cause users to turn off notifications entirely, eliminating the benefit.

---

## Example 3: Subscription / Consumer

**Context**: Reframing a churn-reduction feature list for a subscription product

### Functional Job
"Maintain the value I'm getting from the subscription without having to think about it every month"

### Feature-to-Job Mapping
| Feature | Job Served | Assessment |
|---|---|---|
| Pause subscription option | Minimize the likelihood of canceling when life gets busy | Addresses a real outcome — reduces forced binary decisions |
| Personalization quiz at signup | Increase confidence that the subscription will be worth it | Addresses anxiety before first hire, not churn |
| Monthly "here's what you got" email | Reduce the likelihood of forgetting the value received | Addresses the job directly — counters passive churn |
| Loyalty discount at 6 months | Increase satisfaction with cost-to-value ratio | Addresses price sensitivity but not the core job |

### Gap Identified
No feature addresses: "Minimize the effort required to update preferences when my taste/needs change." Subscribers who drift away without canceling are often stuck in a fit mismatch — they don't update preferences because it's effortful, not because they want to leave. This is a high-opportunity outcome with zero coverage.
