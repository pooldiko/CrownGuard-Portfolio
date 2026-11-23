# QA approach

I separate **functional correctness** from **gameplay quality**. A tower can shoot correctly while making the level trivial; a difficult wave can still contain a movement bug.

## A repeatable issue record

Record the build and map, relevant preset/profile, reproduction steps, expected and observed behavior, evidence, severity, proposed investigation and retest result. Keep a screenshot for geometry/UI and video or event timing for movement and combat. A fix should link back to the original scenario.

## Sample regression matrix

These are planned checks, not newly executed results.

| Area | Scenario | Acceptance evidence |
|---|---|---|
| Crowd movement | Block the shared junction, then remove the obstruction | Enemies resume movement; no teleporting or escape from the intended road corridor |
| Road surface | Inspect bridge, junction and cart connection from hero height | Continuous readable surface without terrain cutting through it |
| Placement | Rotate at an edge and compare preview with the completed tower | Displayed footprint and actual validation agree with current rules |
| Session menus | Pause, open inventory and upgrade menus, return to combat | Same attempt resumes; state and controls remain correct |
| Laboratory | Save/load a variant, apply and repeat | Correct values apply at their documented time; campaign profile remains isolated |
| Recorder | Complete a victory, defeat and early exit | Separate readable reports; outcomes and route counts match observations |
| Recorder timing | Pause during a recorded attempt; begin another recording late | Paused time excluded; late recording marked partial |
| Target selection | Bring a nearer eligible enemy into range before the next shot | The next target follows the documented nearest-target rule |

## Example issue: road surface intersections

**Historical observation:** green triangles interrupted the brown road after terrain edits.  
**Reproduction:** inspect the bridge approach, junction and cart connection at third-person camera height.  
**Expected:** the visible road is continuous over its intended surface.  
**Documented response:** align road geometry with terrain triangles and use the bridge deck as its surface.  
**Recorded verification:** successful build and selected close static views on November 1.  
**Limit:** those views did not certify all positions or prove movement smoothness.

This distinction prevents a compilation result or one attractive screenshot from closing a broader gameplay issue prematurely.

## Future external feedback

Give a tester a build identifier and a short goal rather than explain the intended solution. Ask where they were confused, when they felt pressured, what they built and why. Compare their choices with the designer's familiar strategies. Owner testing is valuable, but cannot substitute for a fresh player's first experience.
