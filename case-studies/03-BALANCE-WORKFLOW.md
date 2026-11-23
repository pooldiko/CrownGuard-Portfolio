# Case study: reduce the work between balance experiments

**Focus:** technical game design and QA tooling.  
**Status:** implemented workflow described by project records; time savings have not been measured.

## The bottleneck

Balance questions involved hero stats, tower roles, wave composition and resources together. Changing configuration outside the session and reconstructing what happened from memory made comparison cumbersome. Some changes could be made in the editor; code changes could also require a build. Not every balance edit required compilation.

## Tool design

The balance laboratory groups supported parameters into **Hero, Towers, Waves and Resources**. Sliders are paired with numeric input, baseline values and reset controls. Changes remain drafts until applied. Named variants allow a test configuration to be reused.

The tool also distinguishes application timing: starting gold needs a restart, enemy values affect future spawns, and hero equipment/passives are evaluated on top of changed base values. This matters because an interface that accepts a number but silently applies it at the wrong time produces misleading tests.

The documented test mode uses an isolated profile copy so experimental progression does not become normal campaign progress.

## Before and after the workflow

| Task | Earlier workflow | Supported laboratory workflow |
|---|---|---|
| Adjust a tower or wave | Locate the relevant configuration; restart or rebuild when necessary | Edit a supported value in its named category and apply at the appropriate phase |
| Repeat a candidate balance | Re-enter values and remember the setup | Save/load a named variant and repeat |
| Explain a loss | Reconstruct events from notes and screenshots | Read a recorded attempt alongside notes and video |
| Compare routes after they merge | Infer which approach caused the leak | Preserve enemy origin-route identity in recorded events |
| Control test context | Manually track upgrades and equipment | Capture the profile, equipment and applied settings with the attempt |

This removes specific manual steps. It does not establish a measured speedup.

## Attempt recording

The November 22 recorder captures a strategy name/description, initial setup and events such as spawns, kills, damage, building, repair, upgrades, losses and wave transitions. It produces HTML for reading and JSON for analysis. Game time excludes pauses.

Route identity is retained after lanes merge. Gate arrival and church arrival are distinct events. An attempt started late is marked partial; events before recording began cannot be recovered. Recording is event-based, not a full replay. A crash may lose events after the most recent intermediate save.

No completed recorded playtest is included here yet. The recorder's documented build success is not presented as a verified report from a real run.

## How to measure the benefit honestly

1. Choose one repeatable task: change a wave composition and tower interval, start a fresh attempt and recover the result.
2. Use the same build, machine, profile and scenario for both workflows; define the exact start and finish of timing.
3. Repeat each workflow several times, alternate their order, and record setup time separately from battle duration.
4. Record errors too: wrong preset, retained progression or missing context can outweigh a shorter setup.
5. Publish raw observations, sample size and median setup time before making a percentage claim.

**Measurement status: not yet collected.** See the [run comparison template](../qa/RUN-COMPARISON.md).

Sources: E06, E09. The next validation is a complete recorded victory, defeat and early exit, compared against observed events.
