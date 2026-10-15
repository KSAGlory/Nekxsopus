# Verification scope

Recorded on 15 October 2026 from private development checks. This showcase does not include runnable tests, implementation source, private logs, or server configuration.

## Desktop and storage

Development verification included TypeScript checks, a production build, nine core tests, and real Electron desktop checks. Desktop tests exercised editing, custom categories, mixed forces, additional teams and participants, advanced JSON, preferences, workspace import/export, and persistence after a complete app restart.

Storage checks covered revision conflicts, corrupt-file recovery, incompatible schemas, and invalid references. Counts of 500, 50, 750, and 1200 were configuration test values; no battle with those forces was executed.

Packaged desktop checks were completed for the 0.3.0 milestone. The later source startup fix was checked in an isolated development run; it should not be described as a rebuilt and accepted public binary. No public binary is distributed here.

## MTA transport and control logic

An isolated real MTA server engine test used fresh configuration and databases with dedicated local ports. It exercised paired resource export through the desktop, telemetry, two pings, listener restart/reconnection, server shutdown detection, and authenticated observation access.

The test engine reported `1.6.0-9.24133.0`. This identifies the tested engine, not a promise of support for every MTA version.

Client actuator and duel referee checks ran in the engine's Lua VM with stubbed game primitives. They covered movement steering, arrival, command expiry, stale identity rejection, stream-loss stopping, cleanup, fixed aim, firing inputs, duel setup/countdown, winner logic, and equipment restoration. The resource applies normal damage without damage-cancellation handlers.

These checks validate transport and logic. Stubbed client primitives do not establish live GTA physics, hit detection, or complete duel behavior.

## Live movement

In a live MTA client, an NPC moved from approximately `(398, 2514)` toward `(406, 2514)`. Subsequent observations reached approximately `(405.635, 2514.006)` and reported arrival, about 0.37 metres from the requested point.

A later diagonal movement attempt was interrupted and does not count as a second completed movement test.

## Actual model decisions

A signed-in Codex runtime returned structured aim, fire, and movement decisions. A cold execution probe took about 30.7 seconds. Two persistent-runtime probes took approximately 7.7 and 4.2 seconds.

These are measured development probes. They do not represent guaranteed in-game reaction times, average performance, or a completed live duel. The tested runtime/model configuration belongs to that development environment; it is not a promise of availability for another account.

## Remaining acceptance work

| Area | What remains unverified |
| --- | --- |
| Complete MTA duel | Full human-versus-Codex round in the live client, including effective control, damage, outcome, and restoration. |
| Combat performance | Accuracy, tactical quality, reaction time under actual play, and repeated-match reliability. |
| Claude | Authentication, observations, decisions, game control, and fair comparison. |
| Warcraft III | Any Nekxsopus connector, custom-map task, campaign mission, or runtime compatibility. |
| Other games | Executable integrations for the remaining catalog entries. |
| General competition system | Automated tournaments, cross-game scoring, and reproducible multi-model benchmark results. |

The current acceptance target is the first complete MTA duel. Automated logic checks and real model responses are useful prerequisites; neither substitutes for that gameplay test.
