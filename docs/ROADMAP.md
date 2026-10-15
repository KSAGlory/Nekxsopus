# Roadmap

The order below reflects current priorities, not release dates or a promise that every candidate game can be integrated.

## 1. Desktop foundation — implemented and checked

- Editable library and challenge drafts.
- Flexible participants, teams, mixed forces, counts, and custom rules.
- Local persistence, backup recovery, and workspace import/export.
- Connection status and paired-resource export for MTA.

The current catalog is editable and can grow beyond its 21 starter games.

## 2. MTA connection and movement — established prototype

- Authenticated local desktop/server communication.
- Telemetry, round-trip ping, and connection-loss detection.
- An opt-in NPC arena and external movement commands.
- A live observation of the NPC reaching a commanded destination.

The local prototype is not a general public-server deployment or a multiplayer tournament platform.

## 3. Human versus Codex — current acceptance milestone

Complete the first live Desert Eagle duel initiated by `/nekxsopus_solo` and `/nekxsopus_cvsp`.

Check actual aim, movement, damage, round endings, cleanup, and decision latency. Record what the model does and where it fails before describing its gameplay performance. Use the existing configurable scenario rather than adding unrelated systems.

## 4. Claude and repeatable comparisons — planned

Add a separately configured Claude controller after the Codex gameplay test. Establish equivalent observation and action permissions, repeatable starting states, and explicit results before running AI-versus-AI comparisons.

Provider authentication, model availability, usage limits, and costs remain separate from the game adapter.

## 5. Warcraft III — priority integration

Two tracks are required:

| Track | First proof needed |
| --- | --- |
| Custom-map battles | Verify the installed game build, create a diagnostic map, and demonstrate bidirectional observation and orders. |
| Campaign missions | Establish a compatible integration route and validate reset, objectives, and control for a specific mission. |

Hero duels, mixed armies, asymmetric forces, abilities, and configurable objectives are desired scenarios. Counts such as 50 or 500 are inputs, not fixed modes. Practical engine and hardware limits must be measured for each integration.

Custom-map success will not automatically establish campaign compatibility. Legacy and current installations may require different profiles.

## 6. More games and categories — incremental

Expand through individually verified adapters. GTA remains a primary focus alongside Warcraft III. Racing, shooters, building, and mission-based games can share the desktop foundation while using different observation, execution, reset, and scoring logic.

Catalog entries and roadmap items do not constitute a supported-game list. Public availability and licensing decisions will be announced separately if a release is offered.
