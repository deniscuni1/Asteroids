# Asteroids

A small Asteroids-style arcade game built in Python to practice real-time loops, collision detection, and clean multi-file project structure.

In addition to gameplay, the project includes **structured JSONL logging** (game events + state snapshots) to make behaviour easy to debug and analyze.

## Features
- Player ship movement and rotation
- Shooting projectiles
- Asteroid spawning/management via an asteroid field
- Collision detection using circular hitboxes (`CircleShape`)
- Tunable configuration via `constants.py`
- **Structured logging**:
  - `game_events.jsonl` (event stream)
  - `game_state.jsonl` (state snapshots)

## Project structure
```text
.
├── main.py              # game entry point / loop
├── constants.py         # game constants (screen size, speeds, etc.)
├── circleshape.py       # base collision shape (circle hitbox)
├── player.py            # player ship behaviour
├── shot.py              # projectile behaviour
├── asteroid.py          # asteroid entity
├── asteroidfield.py     # spawner/manager for asteroids
├── logger.py            # JSONL logging utilities
├── game_events.jsonl    # generated event logs (runtime output)
├── game_state.jsonl     # generated state logs (runtime output)
├── pyproject.toml       # project metadata/deps
└── uv.lock              # locked dependency versions
