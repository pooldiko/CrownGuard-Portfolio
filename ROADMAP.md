# Roadmap to the first public demo

Agreed with the project owner on **22 November 2026**. This is the working sequence for development and portfolio updates. Changes to scope or order should be recorded explicitly rather than silently replacing earlier decisions.

**Current position (23 November 2026):** Stage 1 is complete: the initial English portfolio is published at [pooldiko/CrownGuard-Portfolio](https://github.com/pooldiko/CrownGuard-Portfolio). Stage 2 is complete with the [main systems overview](SYSTEMS.md). Stage 3, external playtesting and prioritized fixes, is next. Later stages remain planned. No completion dates have been committed.

## Demo scope

Deliver one complete forest mission with understandable onboarding, a clear ending and the ability to retry. Defer new mechanics that are not necessary for that experience. Preserve the distinction between implemented features and verified player outcomes.

## Stages and completion criteria

| Stage | Work | Completion criteria | GitHub portfolio update |
|---|---|---|---|
| 1 — Publish the initial portfolio | Publish the prepared English overview, project journey and case studies | The public repository clearly explains the project, contribution and evidence limits | Initial curated edition; no invented retrospective commits |
| 2 — Explain the main systems | Document tower roles, barricades, waves, hero progression, equipment, loot, economy, objectives, onboarding and their relationships | Readers can understand the current game as well as its development history | System overview and selected decision explanations; distinguish current and historical values |
| 3 — External playtest and fixes | Share a feedback build with acquaintances; collect observations and attempt reports; address major problems | Players can understand the tutorial and rules; no blocking issues prevent completion | Build context, anonymized findings, prioritized issues, changes and retest evidence |
| 4 — Visual presentation | Integrate models, materials, environment art, icons and effects | The map is visually coherent; enemies, towers and UI remain readable | Before/after comparisons, art integration decisions and relevant verification |
| 5 — Audio presentation | Add combat, threat, UI and environmental sounds, plus music and volume controls | Audio communicates useful information and can be adjusted through settings | Audio goals, examples and player feedback where available |
| 6 — Final optimization and quality checks | Evaluate performance, loading, graphics settings and stability across available PCs | The demo meets explicitly chosen hardware/performance targets and has no critical known defects | Hardware/build context, measured results, resolved issues and remaining limitations |
| 7 — Prepare and release the demo | Produce the final build; verify installation, saves and the full mission; prepare description, screenshots, known issues and a feedback channel | Another person can independently obtain, launch and complete the demo | Release notes, usable download when published, instructions and feedback route |

## Rules across stages

- **External testing is not final at Stage 3.** Run a short follow-up external playtest of the visually and audibly finished build before release. New presentation can change combat readability.
- **Start external testing without coaching.** Let players encounter the tutorial themselves. Afterwards ask what was unclear, boring or unfair, what they built and why. Keep ordinary runs separate from laboratory-assisted balance experiments.
- **Preserve validated level geometry during art integration.** Replacing its appearance differs from changing routes, heights or defense positions. Structural changes require another gameplay/balance check.
- **Check model integration.** Recheck scale, collision, aiming and visibility when replacing placeholders.
- **Optimize incrementally.** Check performance after substantial batches of models or effects. Stage 6 is the final consolidation, not the first performance investigation. Agree hardware and performance targets before judging success; none are assumed here.
- **Audio may overlap Stage 4.** Its final review still depends on the integrated combat and interface experience.
- **Publish evidence with context.** Use build identifiers and distinguish owner reports, external feedback, static checks, compilation and executed gameplay tests. Do not publish personal tester information without permission.

## Updating the portfolio

For each significant milestone, record **problem or goal → decision and reasoning → evidence → outcome and remaining work**. Keep the README current while retaining dated historical case studies. Combine small fixes into a milestone update; give a defect its own case study when its diagnosis or resolution demonstrates useful work.

All public portfolio material is maintained in English. Record measured improvements only when measurements exist. Update stage status when its completion criteria are met, not merely when implementation is finished.

## Progress tracker

- [x] Stage 1: Initial portfolio published on 23 November 2026.
- [x] Stage 2: Main systems overview added on 23 November 2026; documentation only, not new gameplay certification.
- [ ] Stage 3: External playtest, prioritized fixes and retests completed.
- [ ] Stage 4: Visual integration completed and checked.
- [ ] Stage 5: Audio integration completed and checked.
- [ ] Stage 6: Performance targets and final quality checks satisfied.
- [ ] Stage 7: Final external check, packaging verification and demo release completed.

Supporting documents: [project journey](journey/PROJECT_JOURNEY.md), [QA approach](qa/QA-APPROACH.md), [run comparison template](qa/RUN-COMPARISON.md), [evidence to collect](NEXT-EVIDENCE.md).
