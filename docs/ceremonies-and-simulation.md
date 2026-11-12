# Scrum planning and simulation record

Board: https://github.com/users/Kr1sKros/projects/3/views/2

This is an AI-assisted solo role-play using @Kr1sKros for all roles. These are recorded planning decisions, not minutes from a real group meeting. No customer was contacted, and no backend implementation or deployment is claimed. Module videos and the separate course sharing example were not supplied; the issue template follows the textual assignment instructions.

## Product owner and customer roles: backlog refinement

Scope: catalog CRUD, reactions, browsing/filtering, cloud hosting, automated deployment. Product details include name, description, price, currency and availability. Create ten issues in the supplied requirements order. Defer listing (#7) and subset queries (#8) to Icebox, as instructed. Prioritize the remaining stories #1, #2, #3, #4, #5, #6, #9, #10, with ranks 1–8. Preserve rank when stories move to the sprint. CRUD precedes preferences; hosting and deployment stay visible for later planning.

Refine #1–#5 using testable Gherkin happy paths and failure cases. Clarify that Dislike is a negative reaction, not removal of a Like; one current reaction per shopper/product is an assumption for later refinement. Label #1–#8 enhancement; #9–#10 technical debt as enabling infrastructure work. The latter label follows the assignment taxonomy, although these are also explicit stakeholder requirements.

## Scrum master and developer roles: sprint planning

Milestone **Sprint** covers 12–25 November 2026 inclusive (14 calendar days), ending at 26 November 00:00 UTC. The start is recorded in milestone documentation because GitHub milestones expose a due date rather than a start date. Sprint goal: establish the catalog's four basic CRUD capabilities.

| Rank | Story | Points | Estimate rationale |
|---|---|---:|---|
| 1 | #1 Create | 5 | Validation, persistence, identifier and creation response |
| 2 | #2 Retrieve | 2 | Single-ID lookup and missing-product response |
| 3 | #3 Update | 3 | Validation, persistence changes and missing-product handling |
| 4 | #4 Delete | 3 | Authorization, deletion and absence verification |

Total commitment: **13 points**. Points express relative complexity, not hours. This is an illustrative capacity assumption, not an empirical team velocity. All four stories receive milestone Sprint and move Product Backlog → Sprint Backlog. Stories #1–#3 are assigned to @Kr1sKros when started. #4 remains unassigned and unstarted.

## Developer and reviewer roles: ordered simulation

| Checkpoint | Board changes | Remaining points |
|---|---|---:|
| Planning | #1–#4 in Sprint Backlog | 13 |
| Step 1 | #1 → In Progress; assign @Kr1sKros | 13 |
| Step 2 | #1 → Review/QA; #2 → In Progress and assign | 13 |
| Step 3 | #1 → Done; #2 → Review/QA; #3 → In Progress and assign | 8 |
| Step 4 / end | #2 → Done; leave #3 In Progress and #4 Sprint Backlog | 6 |

Each transition is recorded in issue comments. #1 and #2 are closed as completed to match Done. Completion means simulated acceptance only; tests were not run against product code. Review/QA is empty at the end, as required. In real Scrum, unfinished work is re-evaluated for the Product Backlog after review; this exercise preserves the required snapshot instead.

## Burndown method and retrospective

[Burndown](burndown.svg) uses [CSV data](burndown.csv). The 14-day time axis maps the five mock checkpoints to illustrative offsets 0, 3, 6, 9 and 14. This mapping is synthetic; all GitHub operations were performed during setup, not over two elapsed weeks. Remaining = 13 minus points of Done stories. Partial progress earns no credit. The ideal line declines linearly from 13 to 0. Final remaining work is 6 points (3 + 3), completed work 7 points (5 + 2), and completion is 53.8% of planned points.

GitHub documents a native historical burn-up chart. It cannot infer the synthetic timeline above from same-day changes. Therefore the repository provides an explicitly simulated burndown instead of presenting invented daily history as native analytics. GitHub Insights may be used separately for actual recorded activity.

Challenges: separating role-play from implementation, turning vague requirements into measurable criteria, estimating without past velocity, resolving reaction semantics, and handling chart/tool differences. Lessons: make assumptions explicit, preserve priority, limit started work, and count only fully Done stories. A future sprint should reassess #3 and #4 before taking more work.

## Sources

- Assignment 12.1 instructions supplied in chat.
- [Paperflite: product catalog](https://www.paperflite.com/blogs/product-catalog).
- [GitHub: Insights](https://docs.github.com/en/issues/planning-and-tracking-with-projects/viewing-insights-from-your-project/about-insights-for-projects).
