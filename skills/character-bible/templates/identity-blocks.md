# Juno — identity blocks in every format

Paste the format your model expects. All of them describe the same person; only the packaging changes.

## Long (most models)

```text
[JUNO ID v1] Juno, a 31-year-old woman (adult) with shoulder-length copper-red loose curls worn half-up in a
tortoiseshell claw clip, a few curls loose at the temples; round thin brass wire-rim glasses; a small vintage half-frame
film camera on a woven olive strap; one small beauty mark under her left eye; warm medium-brown skin with natural
texture and visible pores; hazel-amber eyes; soft arched brows; matte terracotta lips; faint smile lines; a curious
half-smile.
```

## Short (fields under about 500 characters)

```text
Juno, 31-year-old woman, copper-red shoulder-length curls half-up in a tortoiseshell claw clip, round brass wire glasses,
vintage film camera on an olive strap, beauty mark under left eye, warm brown skin, hazel eyes, curious half-smile
```

## Midjourney

```text
portrait of a 31-year-old woman, copper-red shoulder-length loose curls half-up with a tortoiseshell claw clip, round thin
brass wire-rim glasses, small vintage film camera on a woven olive strap, beauty mark under left eye, warm medium-brown
skin, hazel-amber eyes, matte terracotta lips, curious half-smile, natural skin texture --style raw --no teenager,
straight hair, sunglasses, heavy makeup, text, logo
```

## JSON (models and tools that take structured prompts)

```json
{
  "subject": {
    "id": "juno-v1",
    "age": "31-year-old woman (adult)",
    "hair": "shoulder-length copper-red loose curls, half-up in a tortoiseshell claw clip, a few curls loose at the temples",
    "accessories": ["round thin brass wire-rim glasses", "small vintage half-frame film camera on a woven olive strap"],
    "face": "warm medium-brown skin with visible pores, hazel-amber eyes, soft arched brows, matte terracotta lips, faint smile lines, one small beauty mark under the left eye",
    "expression": "curious half-smile"
  },
  "avoid": ["teenager", "childlike face", "straight hair", "sunglasses", "heavy makeup", "tattoos", "text", "logos"]
}
```

## Wardrobe strings

| Look | Paste after the identity block |
|---|---|
| Signature | wearing an oversized cream linen shirt with rolled sleeves, olive wide-leg cargo trousers and worn white canvas sneakers |
| Darkroom | wearing a charcoal cotton utility jumpsuit with a rust bandana tied in her hair |
| Market | wearing a vintage brown leather jacket over a navy-and-cream striped top and straight dark jeans |
| Greenhouse | wearing a rust knit vest over a white T-shirt, wide light jeans and a canvas work apron |
| Evening | wearing a terracotta satin slip dress under a cropped faded denim jacket |
| Coast | wearing a chunky cream cardigan, loose linen trousers and a canvas bucket hat |

## Setting strings

| Setting | Paste after the wardrobe |
|---|---|
| Greenhouse studio | in a rooftop glasshouse full of potted ferns and fig trees, soft diffused daylight through whitewashed glass, a long wooden worktable with prints and a loupe |
| Darkroom | in a darkroom lit by red safelight, prints drying on a line behind her, trays and tongs, a single warm work lamp |
| Night market | at a night market under warm string lights, steam from food stalls, wet pavement reflecting colour, shallow depth of field |
| Riso print shop | in a small print shop with stacked coloured paper and two-colour prints pinned to the wall, overhead fluorescent light |
| The coast | on grassy dunes at golden hour, low sun, wind in her hair, long soft shadows |
| Her desk | at a desk with contact sheets, a loupe, a laptop showing an editing timeline and a chipped enamel mug |
