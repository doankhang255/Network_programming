# Diagrams – Design presentation (week 21/10)

Six diagrams, one folder per part of the presentation. They follow the final feature list UC1–UC17
(personal room created at login, game rooms created by the server, random / ranked / friend games,
Elo only for ranked games, disconnect = immediate loss, message log on the server).

| Part | Folder | Diagram |
|---|---|---|
| 1. Application introduction | – | slides only (no diagram) |
| 2. Architecture (client/server, P2P, hybrid) | [2_architecture](2_architecture) | `01_architecture` – client/server over TCP |
| 3. Functionality | [3_functionality](3_functionality) | `02_usecase` – UC1–UC17 |
| 4. Protocol design – message | [../../PROTOCOL.md](../../PROTOCOL.md) | message table (no diagram) |
| 4. Protocol design – state machine | [4_protocol_design/state_machine](4_protocol_design/state_machine) | `03_player_state`, `04_game_room_state` |
| 4. Protocol design – message processing | [4_protocol_design/message_processing](4_protocol_design/message_processing) | `05_seq_ranked_match`, `06_seq_move_game_over` |

PNG images are in the `png/` folder next to each `.puml` file. All diagrams share `style.iuml`.

`_old_spec/` keeps the earlier diagrams and mockups made before UC1–UC17 were fixed. They no longer
match the spec; keep them only for reference.

Re-render after editing a `.puml` file (from `docs/diagrams`):

```bash
for d in 2_architecture 3_functionality 4_protocol_design/state_machine 4_protocol_design/message_processing; do (cd $d && plantuml -tpng -o png *.puml); done
```
