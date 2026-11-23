# Potentially Dangerous Infrastructure Incidents: Evidence Review

## 1. Executive Summary

The request labels identify **1,127 hazard-yes requests** representing **1,122 distinct incidents**, while **126 requests remain unknown**. Eastbank has the highest population-normalized hazard request rate (**25.00 per 10,000 residents**); Old Port has the highest hazard share (**72.00%**) and the longest median hazard closure time (**75.65 hours**). Operational consistency warrants review: **812 of 1,127 (72.05%)** LLM-flagged hazards were assigned Routine or Unassigned intake priority, and the LLM safety-hazard label matched the validation reference in **152 of 200 cases (76.00%)**. These are request and association patterns, not proof of incident prevalence or causes.

## 2. Quantitative Results

**A. Citywide classification and duplicate sensitivity.** The system labels **1,127 requests yes (1,122 distinct incident IDs)**, **747 no (745 distinct incident IDs)**, and **126 unknown (125 distinct incident IDs)**. These counts come from grouping requests by LLM safety-hazard label and counting both rows and distinct `incident_id`. Counting distinct incidents reduces the hazard-yes total by **5**; Eastbank's hazard count changes from **225 requests to 222 incidents**, but it remains the top district by rate. Thus duplicates make a small difference to these headline rankings, though the request counts are not incident counts.

**B. District variation.** Rates use requests divided by district population and multiplied by 10,000; hazard share uses hazard requests divided by all requests in that district. The table reports those denominators explicitly.

| District | Population | Requests (all) | Hazard requests | Distinct hazard incidents | Hazards per 10,000 residents | Hazard share of requests |
|---|---:|---:|---:|---:|---:|---:|
| Eastbank | 90,000 | 388 | 225 | 222 | 25.00 | 57.99% |
| Old Port | 84,000 | 250 | 180 | 178 | 21.43 | 72.00% |
| West Commons | 68,000 | 200 | 119 | 119 | 17.50 | 59.50% |
| Southpoint | 95,000 | 308 | 166 | 166 | 17.47 | 53.90% |
| Riverside | 79,000 | 227 | 120 | 120 | 15.19 | 52.86% |
| North Harbor | 74,000 | 198 | 108 | 108 | 14.59 | 54.55% |
| Cedar Hills | 61,000 | 187 | 89 | 89 | 14.59 | 47.59% |
| Lakeview | 85,000 | 242 | 120 | 120 | 14.12 | 49.59% |

Eastbank's rate is the highest; its **225 / 388** hazard share is not the highest. Old Port's share is highest, based on **180 / 250** requests. The rate calculation normalizes request counts by population, while the share describes the composition of requests, not resident risk.

**C. Intake priority and urgency.** Within LLM hazard-yes requests, **750 / 1,127 (66.55%)** were intake Routine and **62 / 1,127 (5.50%)** Unassigned. Combined, **812 / 1,127 (72.05%)** were Routine or Unassigned. The hazard/urgency breakdown by intake priority is:

| Intake priority | Hazard requests | LLM urgent | LLM routine |
|---|---:|---:|---:|
| High | 315 | 244 | 71 |
| Routine | 750 | 244 | 506 |
| Unassigned | 62 | 37 | 25 |

These cells are counts from the intake-priority × safety-hazard × urgency cross-tab; no hazard-yes request had LLM urgency unknown in that query. This points to a triage review opportunity, not a conclusion that every flagged item should have been High priority.

**D. Handling time.** `hours_to_close` averages and medians exclude requests without a close time. For hazard-yes requests, **1,122 closed requests** had a mean of **59.06 hours** and median of **23.99 hours**. For no-or-unknown requests, **872 closed requests** had a mean of **33.23 hours** and median of **14.18 hours**. These are descriptive comparisons across closed requests. By intake priority within hazards: High (**315 closed**) averaged **82.11 hours**, median **54.02**; Routine (**746 closed**) averaged **49.59**, median **20.11**; Unassigned (**61 closed**) averaged **55.71**, median **36.47**.

| District | Hazard yes: closed n | Hazard median (hours) | No/unknown: closed n | No/unknown median (hours) |
|---|---:|---:|---:|---:|
| Cedar Hills | 89 | 22.10 | 98 | 16.00 |
| Eastbank | 225 | 17.72 | 163 | 10.43 |
| Lakeview | 119 | 25.72 | 122 | 15.94 |
| North Harbor | 107 | 22.03 | 90 | 13.83 |
| Old Port | 179 | 75.65 | 70 | 23.85 |
| Riverside | 119 | 21.48 | 107 | 14.95 |
| Southpoint | 165 | 18.80 | 141 | 12.92 |
| West Commons | 119 | 24.02 | 81 | 13.87 |

Old Port stands out on closure time: hazard median **75.65 hours**, compared with **23.85 hours** for its no-or-unknown requests. Its hazard mean is **99.59 hours** (179 closed hazards). District medians and means are associations; they do not adjust for work type or complexity.

**E. Time, events, and reporting channel.** Eastbank hazard counts by month were Jan **10**, Feb **11**, Mar **8**, Apr **15**, May **32**, Jun **30**, Jul **25**, Aug **27**, Sep **16**, Oct **20**, Nov **15**, and Dec **16**. This is a request count by `created_at` month; duplicates are included. In the Eastbank event records, rainstorms occurred Mar 23–26, May 12–16, Sep 5–8, and Sep 20–21; the May event description notes major rainfall and road-surface damage. The Mobile Reporting Rollout is recorded for Eastbank from **May 1 through Dec 31, 2025**.

Comparing Eastbank's pre-rollout period (Jan–Apr) with the rollout period (May–Dec), all requests changed from **79 total / 19.75 per month** to **309 / 38.63 per month**; hazard requests changed from **44 / 11.00 per month** to **181 / 22.63 per month**. This aligns in time with a channel change, but cannot distinguish reporting volume from underlying conditions. Channel counts further show **3 Mobile, 39 Phone, and 37 Web** requests before the rollout date versus **230 Mobile, 29 Phone, and 50 Web** during the rollout period. Mobile reports were already present before the event's stated start, so the channel and event date should be checked before using this as a clean before/after comparison. May–Aug had **114 hazards (28.50 per month)** and Sep–Dec had **67 (16.75 per month)**; the later period overlaps Eastbank's September rainstorms, so the monthly pattern is not a simple event response.

The recorded Staffing Expansion (June 16) is in Riverside, and Triage Workflow Update (September 1) is in Southpoint—not Eastbank. They should not be treated as Eastbank interventions. Event and request counts are aligned by district and dates; associations here are descriptive, not causal.

## 3. Visualizations

![LLM-flagged hazard requests per 10,000 residents by district](charts/hazard_rate_by_district.png)

This compares population-normalized hazard request counts; Eastbank is highest, while Old Port has the largest request hazard share (the latter is not what this rate measures).

![Monthly LLM-flagged hazard requests in Eastbank](charts/eastbank_monthly_hazards.png)

This shows Eastbank's monthly hazard request volume in 2025, including the increase in May and subsequent decline from the summer peak.

![Median closure time for LLM-flagged hazards by district](charts/hazard_median_close_by_district.png)

This shows the median hours to close among closed hazard-yes requests, with Old Port higher than the other districts.

## 4. Classification Analysis

**Intake versus LLM.** The priority cross-tab above shows that most LLM hazard-yes requests were intake Routine; among those, **506** were LLM routine urgency and **244** urgent. Of the **62** Unassigned hazard-yes requests, **37** were LLM urgent and **25** routine. Thus urgency and intake priority do not line up consistently, but neither label is a verified operational severity assessment.

For intake category versus LLM incident type, I used an explicit comparison crosswalk: Drainage→drainage, General Inquiry→other, Road Maintenance→road, Sanitation→sanitation, Streetlight→electrical, Traffic Signal→traffic_signal, Tree Maintenance→tree, Water Service→water, and Other→other. LLM `unknown` is counted as disagreement. By this crosswalk, General Inquiry had **134 disagreements / 274 requests (48.91%)**, Road Maintenance **121 / 632 (19.15%)**, and intake Other **110 / 126 (87.30%)**. The largest disagreement count is General Inquiry; the highest rate is Other. The “Other” crosswalk is inherently broad, so its rate should not be read as a definitive error rate. These comparisons are not ground-truth accuracy measurements.

**Validation sample.** Joining `validation_labels` to `enriched` by `request_id` produced **200** matched records. Exact-match accuracy was incident type **197 / 200 (98.50%)**, urgency **196 / 200 (98.00%)**, and safety hazard **152 / 200 (76.00%)**. The observed nonzero safety-hazard confusion cells were:

| Reference safety label | LLM no | LLM unknown | LLM yes |
|---|---:|---:|---:|
| no | 71 | 2 | 46 |
| unknown | 0 | 20 | 0 |
| yes | 0 | 0 | 61 |

There were **46** reference-no records labeled hazard yes; the validation sample therefore cautions against treating the hazard flags as verified facts. The LLM correctly retained the unknown label in **20** reference-unknown cases, while also assigning no in **2** reference-no cases.

## 5. Caveats

- `unknown` is a separate LLM output, not a synonym for no: **126 requests / 125 incidents** are unknown. Excluding or reallocating these could change comparisons.
- The safety label's validation accuracy is **76.00% on 200 matched sample records**. The validation sample may not represent all requests; in particular, the confusion table includes **46** reference-no cases labeled yes.
- There are **6 of 2,000** requests with null `closed_at` and null `hours_to_close` (5 hazard-yes and 1 no/unknown). Closure averages and medians exclude them; open requests may be unresolved rather than quickly handled.
- District populations differ (from **61,000** in Cedar Hills to **95,000** in Southpoint), so raw counts alone are not comparable. Rates here use resident population but do not account for infrastructure condition, reporting propensity, or exposure.
- There are **184** duplicate-marked requests. Distinct `incident_id` counts reduce hazard-yes from **1,127 requests to 1,122 incidents**; duplicates can inflate request volume and may be distributed unevenly.
- Reporting channel changed around the Eastbank mobile rollout, and Mobile appears in the records before the rollout's stated date. Increased reports could reflect access or channel coding as well as conditions. Events are recorded observations, not proof that they caused request changes.
- LLM and intake labels use request descriptions that may be incomplete or ambiguous; the category crosswalk is an analytical convention, especially for Other and General Inquiry. Priority labels are known to be imperfect. Closure time also reflects workload mix and process, not only hazard severity.

## 6. Recommendation

Investigate whether Eastbank's Mobile channel start date and reporting-channel coding are consistent with the May 1 rollout record, and whether increased post-May requests reflect newly accessible reporting, a change in underlying hazards, or both. In parallel, audit the Routine and Unassigned intake assignments among LLM-flagged hazards against case descriptions and field outcomes, with particular attention to urgent-tagged cases. These checks would test a plausible triage and measurement concern without assuming that the observed associations establish a cause.