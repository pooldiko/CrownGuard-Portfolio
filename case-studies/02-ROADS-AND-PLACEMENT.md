# Case study: the road must agree with the game rules

**Focus:** visual readability, placement constraints and regression design.

## Player-facing symptoms

After terrain changes, green triangles appeared inside the brown road. Some road segments looked hidden, bridge connections were unclear, and the tower footprint made building near an edge frustrating. Enemy movement also appeared unstable in some reports.

These symptoms were related spatially, but were not necessarily one bug. A still screenshot could show road coverage; it could not prove smooth movement or identify the cause of motion blur.

## Response

The documented November 1 repair made the road surface follow the terrain's actual triangles with a small height offset. Bridge movement used the deck surface. Placement gained 15-degree preview rotation and a smaller horizontal footprint while keeping tower height and combat values separate.

The important design requirement was agreement between what the player sees and what the placement system accepts. Rotating the preview must also rotate the footprint used by validation and the final placed object.

## Verification was split by evidence type

| Check | What it can establish | What it cannot establish |
|---|---|---|
| Successful editor build | The changed implementation compiles | Placement feels correct in play |
| Close static views of bridge, road and junction | Visible surface coverage at those viewpoints | Every location is free of defects |
| Placement scenarios at corners and slopes | Preview, validation and final placement agree | All enemy movement is smooth |
| Moving crowd observed over time | Steering, waiting and recovery behavior | Cause of a defect without further diagnosis |

The retained repair note reports a successful build and clean close views at selected locations. It explicitly says the added regression scenarios were compiled but not run in that cycle. This portfolio preserves that limitation.

## Regression scope

Check the bridge approach, deck, straight road, junction and cart connection from hero height. Rotate a tower at an edge and on a slope; compare the ghost and completed footprint. Observe a blocked crowd until the obstacle clears and verify that movement resumes without crossing the allowed corridor.

Placement rules evolved later to allow building on roads. Historical tests that forbade road overlap must therefore be revised, not blindly reused as current acceptance criteria.

## Lesson

A top-down map review is not enough for a third-person game. Visual presentation, collision and validation must be checked together from the player's perspective. A recurring report is a reason to improve reproduction and evidence, not simply increase another parameter.

Source: E05. Earlier screenshots and repeated owner reports informed the diagnosis; no new gameplay verification was performed to prepare this portfolio.
