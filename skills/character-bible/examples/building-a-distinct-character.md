# Worked example: building "Theo Marsh" from the blank template

Scenario: a small account about sourdough and early-morning baking wants a recurring on-camera host. The operator
copies `templates/character-bible-template.yaml` and fills it in this order.

## 1. Run the distinctness test before anything else

Compare against every character the operator already knows of — here, Eria from this skill.

| Anchor | Eria | Theo | Changed? |
|---|---|---|---|
| Hair | copper-red shoulder-length curls, half-up | close-cropped salt-and-pepper hair, short neat beard | yes |
| Signature accessory | round brass wire glasses | a flour-dusted navy baker's cap | yes |
| Second accessory | film camera on an olive strap | a wooden bench scraper tucked in his apron pocket | yes |
| Face | warm brown skin, hazel eyes, beauty mark | pale olive skin, grey-blue eyes, a small scar through the left eyebrow, laugh lines | yes |
| Settings | greenhouse, darkroom, night market | bakery at 4am, a market stall at dawn, a tiny flat kitchen | yes |

Five of five changed — it passes (the rule is at least four). Accent colour: **wheat `#d9a441`**.

## 2. Identity block — adult, invented, no "looks like"

```text
[THEO ID v1] Theo Marsh, a 42-year-old man (adult) with close-cropped salt-and-pepper hair and a short neat beard; pale
olive skin with natural texture; grey-blue eyes; a small scar through his left eyebrow; laugh lines; a flour-dusted navy
baker's cap; a canvas apron with a wooden bench scraper in the pocket; a patient, amused expression.
```

Negative: `teenager, young man, long hair, clean-shaven, glasses, tattoos, chef's toque, plastic skin, text, watermark`

The negative blocks the drifts this look is prone to (a chef's toque instead of a cap, a younger face).

## 3. Voice

- Dials: warmth high, irony low, energy low, formality low, hype none, emoji none.
- Sample lines: `the dough was ready before I was`, `4am is quieter than any studio`, `crumb shot. no notes`.
- Never: name real bakeries as endorsements without #ad; never give health or nutrition claims.

## 4. Reference pack and lock

1. Generate four exploration headshots from the identity block at low resolution, with a small spending cap, on a
   plain warm-grey backdrop at 85 mm with soft window light.
2. Pick one face. Generate eleven more angles using that image as the reference: front, three-quarter left and right,
   profile, laughing, cap off, full body, seated, hands visible, night light, daylight.
3. Score each against the drift checklist in [../../character-consistency/SKILL.md](../../character-consistency/SKILL.md)
   and keep the twelve that pass every check.
4. Save the short identity block and three references (front, three-quarter, profile) as a reusable style in the
   image tool, or in the prompt library if the tool has no saved styles.

## 5. Result

First week: five shorts — shaping at dawn, scoring loaves, the market stall opening — each labelled as AI-generated,
with "AI-generated character" in the bio. At thumbnail size Theo reads as nobody else, which is the point of the test.
