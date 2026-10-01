# Lab 4: VibeCoding - Centipede Repair Lab

A single-file Centipede-lite clone built with **Pygame**. The original project had one deliberate bug and three empty feature functions. I used an LLM as a pair-programming partner to fix the bug and implement the features, one task at a time, with a separate commit for each.

## Setup

Requires Python 3.10+.

```bash
pip install pygame
python game.py
```

**Controls:** Arrow keys to move, Space to fire, `R` to reset.

## Tasks Completed

| # | Task | Change |
|---|------|--------|
| 1 | Fix mushroom durability bug | In `hit_mushroom`, changed the removal check from `<= 1` to `<= 0`. Mushrooms now survive 4 hits instead of 3. |
| 2 | Implement `mushroom_color(hp)` | Returns red-orange `(255, 90, 60)` when a mushroom is on its last hit point; otherwise returns `None` (default fading color). |
| 3 | Implement `on_segment_hit(segment, score)` | Spawns a burst of 10 spark particles at the destroyed segment's position. Added a module-level `sparks` list, an `update_sparks` method, spark drawing in `draw`, and `sparks.clear()` in `reset`. |
| 4 | Implement `wave_speed_bonus(wave)` | Returns `1 + 0.15 * (wave - 1)`, so each wave moves 15% faster than the previous one. |

## Verifying the Changes

- **Task 1:** Shoot one mushroom repeatedly. It should remain after 3 hits and disappear on the 4th.
- **Task 2:** A mushroom turns red-orange after its 3rd hit.
- **Task 3:** Shooting a centipede segment produces a short spark burst.
- **Task 4:** Clear every segment. The next wave (shown in the HUD) moves faster.

## Submission Contents (`Lab-4/`)

- `game.py` - updated code
- `before.mp4` - 10-second gameplay video showing the original bug
- `after.mp4` - 10-second gameplay video showing the fix and new features
- Chat history (PDF/doc): `<add file name here>`
- LLM chat link: `<add shareable link here>`

## Git History

Each task was committed separately:

1. `Task 1: fix mushroom durability bug`
2. `Task 2: implement mushroom_color`
3. `Task 3: implement on_segment_hit`
4. `Task 4: implement wave_speed_bonus`