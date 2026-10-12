# The reference set — which shots to lock

A reference set is the small group of approved images every later generation is checked against and, where the model
supports it, fed as references. Twelve images cover almost every situation.

| # | Shot | Why it is in the set |
|---|---|---|
| 01 | Front, neutral expression, eye level, 85 mm | the master face; first reference for every model |
| 02 | Three-quarter left | most portraits and thumbnails use this angle |
| 03 | Three-quarter right | catches the side the model sees less often |
| 04 | Profile | locks nose, jaw and hair volume |
| 05 | Laughing | expressions are where faces drift most |
| 06 | Signature accessory off (for Juno: glasses in hand) | stops models drawing the accessory into the face |
| 07 | Full body, standing, signature look | proportions and wardrobe |
| 08 | Seated at the desk or worktable | the most common lifestyle pose |
| 09 | Hands visible, holding the camera | hands and the prop together |
| 10 | Night light (warm practicals) | colour of skin and hair under artificial light |
| 11 | Daylight, outdoors | skin and hair in natural light |
| 12 | Close-up, eyes and glasses | fine detail: eye colour, beauty mark, rims |

## Rules

- Generate 01 first and pick it carefully; every other image uses it as a reference.
- Reject any image that fails a **hard** check in [look-constants.md](look-constants.md).
- File names follow the number and shot, e.g. `refs/juno/02-three-quarter-left.jpg`.
- Record the model, date and settings for each file in a provenance log (see
  [../../ai-disclosure-and-provenance/SKILL.md](../../ai-disclosure-and-provenance/SKILL.md)).
- When the look changes, make a new versioned folder (`refs/juno-v2/`) rather than replacing images in place.
