# Selected design decisions

This is an editorial retrospective, not a complete dated changelog. Rows without exact dates preserve sequence only. The purpose is to expose the reason behind a change.

| Context | Observation / question | Decision | Tradeoff / next check |
|---|---|---|---|
| Initial Unreal scope | A broad concept needed a testable core | Fixed routes, build/defense phases, editable parameters | Less freedom initially; easier to inspect the loop |
| Early terrain iteration | Towers struggled to hit enemies below the surrounding ground | Revisit road elevation and firing constraints | Terrain appearance must not obscure attack rules |
| Larger enemy formations | Rows looked artificial; dense groups blocked one another | Revisit spacing, mixing and local avoidance | Natural appearance must retain readable movement and bounded cost |
| Long approaches | Waiting dominated parts of a wave | Shorten the map/approaches and revisit spawn pacing | Preserve preparation time without empty travel |
| November 1 gameplay package | Four archers felt restrictive and easy | More room for mixed defenses and a shared position | Shared coverage could become dominant |
| Later playtests | Junction defense could clear without the hero | Attackable towers and frontline defense | Avoid turning every strategy into mandatory hero tanking |
| Barricade test | Enemies could bypass a single barrier | Match road width and blocking footprint | Check crowd recovery and alternate approaches |
| First-map tower roles | Slow aura's value was unclear beside barricades | Defer aura on map one; emphasize other roles | Revisit later only when it solves a distinct problem |
| November 20 laboratory | Repeated tuning and setup were cumbersome | Grouped controls, variants and repeat flow | Explain when changes take effect; isolate profile progression |
| November 21 mission update | Early pressure needed a clearer progression | Five waves; armored threats introduced later | Needs fresh full-mission calibration |
| November 22 recording | Memory alone could not explain route-specific failures | Event reports with setup context and original routes | Reports are not video replays; partial runs need labeling |

See [evidence register](../EVIDENCE.md) before interpreting these as measured outcomes.
