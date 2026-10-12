---
name: character-bible
description: "Builds and maintains a character bible for an AI creator — the five silhouette anchors that make the character recognisable in a thumbnail, a paste-in identity block for image and video prompts, a negative block, named wardrobe looks, recurring settings, a palette, a voice with sample captions, and a hard \"never\" list. Uses Juno, the example creator that appears throughout these skills, as a fully worked bible, and includes a blank template and a distinctness test for building your own. Use when writing any prompt, caption or script that features a recurring character, when checking a generation for off-model drift, or when starting a new character from scratch."
license: MIT
metadata:
  title: "Character bible"
  category: create
  summary: "Define an AI character in one document — face, wardrobe, settings, palette, voice and limits — using a fully worked example."
  level: beginner
  tags: "character, persona, brand, identity, ai influencer, style guide, wardrobe, voice"
  time: "15 min"
  version: "3.0.0"
  updated: "2026-10-12"
---

# Character bible

A recurring AI character only works if every image, clip and caption describes the same person. The character bible is
the one document every prompt and script draws from. This skill shows the whole bible for **Juno**, the example creator
used across these skills, then walks you through writing your own.

Juno is fictional and exists only as a teaching example. Don't publish content as Juno; build your own character with
the template in step 8.

## When to use this

- Before writing an image, video, voice or avatar prompt that features a recurring character.
- Before writing captions, replies, bios, alt text or scripts in a character's voice.
- When reviewing a generation and asking "is this still them?"
- When starting a brand-new character and you want a structure that holds up over hundreds of posts.

## What you need

- Nothing to read the bible. To generate, any image or video model you already use, with your own account or API key.
- An approved reference pack of 8–12 images once the look is settled (step 2 of
  [../character-consistency/SKILL.md](../character-consistency/SKILL.md)).
- Deeper material: [references/look-constants.md](references/look-constants.md) (every visual detail with how much
  drift is acceptable), [references/voice-and-personality.md](references/voice-and-personality.md) (tone, rules and
  25 sample lines), [references/reference-set.md](references/reference-set.md) (the shots a reference pack needs).

## Steps

### 1. Fix the five silhouette anchors

Anchors are what a viewer recognises in a one-second thumbnail. Every generation keeps all five unless a shot hides one
on purpose (a back view hides the face, a close-up crops the camera strap). Juno's:

1. **Hair:** shoulder-length copper-red loose curls, usually half-up in a tortoiseshell claw clip, a few curls loose at
   the temples.
2. **Glasses:** round, thin brass wire-rim glasses. She is never without them on camera.
3. **Camera:** a small vintage half-frame film camera on a woven olive strap, worn cross-body or held in one hand.
4. **Beauty mark:** one small beauty mark just under her left eye.
5. **Face:** warm medium-brown skin, hazel-amber eyes, soft arched brows, matte terracotta lips, faint smile lines; her
   default expression is a half-smile, as if she just noticed something.

She is **a 31-year-old woman**. Put the age in every prompt. Models drift younger with curls, glasses and selfie
framing, and an explicit adult age is the cheapest fix (see [../character-consistency/SKILL.md](../character-consistency/SKILL.md)).

### 2. Paste the identity block, word for word

The identity block is versioned. When the look changes, bump the version and retire the old block.

```text
[JUNO ID v1] Juno, a 31-year-old woman (adult) with shoulder-length copper-red loose curls worn half-up in a
tortoiseshell claw clip, a few curls loose at the temples; round thin brass wire-rim glasses; a small vintage half-frame
film camera on a woven olive strap; one small beauty mark under her left eye; warm medium-brown skin with natural
texture and visible pores; hazel-amber eyes; soft arched brows; matte terracotta lips; faint smile lines; a curious
half-smile.
```

Short form, for prompt fields under about 500 characters:

```text
Juno, 31-year-old woman, copper-red shoulder-length curls half-up in a tortoiseshell claw clip, round brass wire glasses,
vintage film camera on an olive strap, beauty mark under left eye, warm brown skin, hazel eyes, curious half-smile
```

Negative block, only for models that accept negatives:

```text
teenager, childlike face, straight hair, short hair, blonde, black hair, square glasses, sunglasses, no glasses,
heavy makeup, glossy lips, airbrushed skin, plastic skin, tattoos, extra fingers, warped hands, text, watermark, logo
```

### 3. Dress the character from named looks

Named looks keep wardrobe consistent without repeating outfits exactly. Pick one per post.

| Look | Prompt wording | Where it fits |
|---|---|---|
| **Signature** | an oversized cream linen shirt with rolled sleeves, olive wide-leg cargo trousers, worn white canvas sneakers | greenhouse studio, portraits, profile images |
| **Darkroom** | a charcoal cotton utility jumpsuit, a rust bandana tied in her hair | the darkroom, process clips |
| **Market** | a vintage brown leather jacket over a navy-and-cream striped top, straight dark jeans | night market, street scenes |
| **Greenhouse** | a rust knit vest over a white T-shirt, wide light jeans, a canvas work apron | greenhouse studio, behind the scenes |
| **Evening** | a terracotta satin slip dress under a cropped faded denim jacket | rooftop at dusk, events |
| **Coast** | a chunky cream cardigan, loose linen trousers, a canvas bucket hat | the coast at golden hour |

Rules: glasses and camera in every look. Metal is brass or gold-toned. No visible tattoos. No readable brand logos.

### 4. Put the character in recurring settings

Reusing a small set of places makes a feed read as one world.

- **Greenhouse studio:** a rooftop glasshouse full of potted ferns and fig trees, soft diffused daylight through
  whitewashed glass, a long wooden worktable with prints and a loupe.
- **Darkroom:** red safelight, prints drying on a line, trays and tongs, deep shadows, a single warm work lamp.
- **Night market:** warm string lights, steam from food stalls, wet pavement reflecting colour, shallow depth of field.
- **Riso print shop:** stacked coloured paper, two-colour prints pinned to a wall, overhead fluorescent light.
- **The coast:** low golden sun, grassy dunes, wind in her hair, long soft shadows.
- **Her desk:** contact sheets, a loupe, a laptop with an editing timeline, a chipped enamel mug.

### 5. Hold the palette

| Token | Hex | Use |
|---|---|---|
| Ink | `#14161a` | backgrounds, banner gutters |
| Paper | `#f3ead8` | wordmark, text on images |
| **Lagoon (accent)** | `#2a9d8f` | the one accent: underlines, highlights, stickers |
| Terracotta | `#c8553d` | buttons and solid shapes on dark |
| In-image colour | olive `#6b7a3a`, copper `#b5562b`, brass `#b8923a`, safelight red `#b3261e` | wardrobe and light, never as UI |

Grade: warm and filmic, slightly lifted shadows, fine grain, natural skin. Night scenes keep warm highlights over teal
shadows; avoid a heavy orange-and-teal blockbuster look.

### 6. Write in the character's voice

Juno is curious, warm and observant, with dry humour. She notices small things — light on a wall, a stranger's
umbrella — and writes in short sentence-case lines. She talks about craft, not about herself as a product. She never
names the model that makes her, never claims to be human and never gives financial advice. More in
[references/voice-and-personality.md](references/voice-and-personality.md).

Sample captions (each ships with the label the platform requires — see
[../ai-disclosure-and-provenance/SKILL.md](../ai-disclosure-and-provenance/SKILL.md)):

- `the safelight makes everyone look like a secret`
- `shot 14 of 36. the good one is always 14`
- `today's lesson: the fern does not want to be photographed`
- `night market rule: buy the dumplings first, then the photo`
- `new skill up: how to make a character that isn't me`
- `contact sheets are just a diary you can hold`

### 7. Keep a "never" list

Write the hard limits before the first image, and keep them next to the identity block:

- Never depicted or described as under 18.
- Never explicit or sexualised.
- Never resembles, names or imitates a real person.
- Never claims to be human; always carries an AI label where a platform asks for one.
- Never gives financial advice, price targets or return promises.
- Never posts real people's photos as references.

### 8. Build your own character from the template

1. Copy [templates/character-bible-template.yaml](templates/character-bible-template.yaml).
2. **Distinctness test:** change at least four of the five anchors from any existing character you know of — hair shape
   and colour, signature accessory, second accessory, face, and home settings. Similar is not distinct.
3. Give an adult age (25+) and invent the face. Never describe, name or reference a real person ("looks like…" is
   banned) and never use a real person's photo as a reference.
4. Pick one accent colour and one grade, and write them down.
5. Write 10 sample captions and the "never" list before generating anything.
6. Generate a 12-image reference pack (see [../character-consistency/SKILL.md](../character-consistency/SKILL.md)) and
   lock it.

A second worked example, built from a blank template, is in
[examples/building-a-distinct-character.md](examples/building-a-distinct-character.md). Juno's full bible as YAML is in
[examples/juno-bible.yaml](examples/juno-bible.yaml).

### 9. Store the style with your generator

Most image tools let you save a reusable style or "brand" with a default prompt prefix and reference images. Save the
short identity block as the prefix and attach three approved references (front, three-quarter, profile). If your tool
has no saved styles, keep the block in your prompt library (see
[../prompt-library-management/SKILL.md](../prompt-library-management/SKILL.md)) and paste it every time.

## Templates

- [templates/character-bible-template.yaml](templates/character-bible-template.yaml) — blank bible for any character.
- [templates/identity-blocks.md](templates/identity-blocks.md) — Juno's identity block in long, short, Midjourney and
  JSON forms, plus per-look wardrobe strings.
- [examples/juno-bible.yaml](examples/juno-bible.yaml) — this bible as machine-readable YAML.

Fill-in caption line:

```text
[a small observation about the scene in ≤ 9 words] + [one dry twist] + [optional single emoji] + [AI label per platform]
```

## Check before you finish

- [ ] All five anchors visible, or hidden on purpose.
- [ ] Reads as an adult; the prompt states the age.
- [ ] Wardrobe is one named look; glasses and camera present.
- [ ] Setting is one of the recurring worlds, or a deliberate new one that fits.
- [ ] No real-person likeness, no readable third-party logos, nothing sexualised.
- [ ] Caption is in voice, names no model, makes no price or return claim, and carries the AI label.
- [ ] A new character passes the distinctness test (four of five anchors changed).

## Pitfalls

- **Age drift.** Curls, glasses and wide-angle selfies push models younger. State the age, add "adult", and prefer
  35–50 mm framing for portraits.
- **Glasses drift.** Models swap round wire frames for thick or square ones, or drop them. Say "round thin brass
  wire-rim glasses" every time.
- **Hair drift.** Curls straighten or go auburn-brown. Say "copper-red loose curls".
- **Camera becomes a phone.** Say "vintage half-frame film camera" and mention the strap.
- **Over-styling.** Heavy contour and glossy lips make the face generic. Keep makeup minimal: matte terracotta lips,
  bare skin texture.
- **Logo soup.** Real camera and clothing logos appear; prompt "no readable logos" and fix in the edit.

## Related skills

- [../character-consistency/SKILL.md](../character-consistency/SKILL.md) — reference packs, seeds, drift checks.
- [../photoreal-portrait-prompts/SKILL.md](../photoreal-portrait-prompts/SKILL.md) · [../lifestyle-scene-prompts/SKILL.md](../lifestyle-scene-prompts/SKILL.md)
- [../selfie-and-ugc-video-prompts/SKILL.md](../selfie-and-ugc-video-prompts/SKILL.md) · [../voice-and-lip-sync/SKILL.md](../voice-and-lip-sync/SKILL.md)
- [../captions-and-hooks/SKILL.md](../captions-and-hooks/SKILL.md) · [../ai-disclosure-and-provenance/SKILL.md](../ai-disclosure-and-provenance/SKILL.md)
- [../personal-brand-strategy/SKILL.md](../personal-brand-strategy/SKILL.md) · [../agent-persona-and-system-prompt/SKILL.md](../agent-persona-and-system-prompt/SKILL.md)
