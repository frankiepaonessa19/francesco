# Production Build Kit — "The Super Blind Spot" (Concept 1 video)
**Date:** 2026-07-05
**Client:** Titan Wealth Australia
**Deliverable:** ~22s video ad · 4:5 master + 9:16 Reels crop
**Pipeline:** Higgsfield (stills) → Runway Gen-4.5 (image-to-video) → CapCut/Premiere (edit, VO, captions, end card)

Work through the steps in order. Every prompt below is copy-paste ready.

---

## STEP 1 — Generate the character anchor (Higgsfield)

Generate this FIRST. The best seed becomes your character reference for every other still — this is what keeps the same man across all shots.

**Settings:** Photorealism mode · 4:5 · generate 8 seeds

```
Photorealistic candid portrait of an Australian man in his early 50s sitting
at a warm timber kitchen table in the early evening, reading a printed
financial statement, reading glasses resting low on his nose, one hand
touching his forehead in quiet concentration, open laptop glowing softly
beside him, modern Australian home interior with eucalyptus branch in a vase
blurred in background, warm tungsten practical lighting mixed with cool dusk
window light, shot on 85mm lens at f/1.8, shallow depth of field, natural
skin texture, editorial documentary photography style, natural light,
subtle film grain
```

**Selection criteria (in order):** natural hands → natural eyes → believable glasses → consistent lighting. Save the winning image as `blindspot_hero.png` and note its seed. This still is ALSO your Shot 2 input — one generation, two jobs.

---

## STEP 2 — Generate the remaining stills (Higgsfield)

Use `blindspot_hero.png` as character/style reference on stills B and C.

### Still A — statement macro (feeds Shot 1) — no character needed
```
Photorealistic top-down close-up of a printed financial statement on a warm
timber kitchen table, a pen resting beside it, one line of the statement
subtly circled in blue ink, warm tungsten evening light, 85mm macro lens,
shallow depth of field, editorial documentary photography, subtle film grain
```
Save as `blindspot_statement.png`.
*Tip: keep the statement text soft/out of focus — AI text renders as gibberish and sharp fake numbers are a compliance problem. The circled line should read as a shape, not legible figures.*

### Still B — laptop OTS (feeds Shot 3) — use character reference
```
Photorealistic over-the-shoulder shot of an Australian man in his early 50s
at night leaning toward an open laptop at a warm timber kitchen table,
laptop screen glow illuminating his face, reading glasses on, dark warm
room with a single lamp in background, 85mm lens, shallow depth of field,
editorial documentary photography, subtle film grain
```
Save as `blindspot_laptop.png`.
*Tip: laptop screen should be a soft glow, not readable UI.*

### Still C — the exhale (feeds Shot 4) — use character reference
```
Photorealistic medium close-up of an Australian man in his early 50s at a
warm timber kitchen table at night, laptop half closed in front of him,
leaning back with a faint relieved smile, reading glasses pushed up onto
his head, warm lamp light, 85mm lens, shallow depth of field, editorial
documentary photography, subtle film grain
```
Save as `blindspot_exhale.png`.

**Checkpoint before Step 3:** line up hero, B and C side by side. Same face, same glasses, same shirt, same room? If not, regenerate the failures with the character reference weighted higher. Do not proceed into Runway with a drifting character — it's the #1 thing that makes AI ads read as fake.

---

## STEP 3 — Animate each shot (Runway Gen-4.5, image-to-video)

Upload the still listed for each shot, paste the prompt, generate 3–4 takes per shot. Generate at the durations below (slightly long — you'll trim in the edit; Gen-4.5's first/last half-second are the most stable cut points).

### Shot 1 · input `blindspot_statement.png` · duration 4s (edit uses 0:00–0:03)
```
Close-up top-down shot: a printed superannuation statement lying on a warm
timber kitchen table, a hand slides it into frame and circles a line with a
pen, slow push in toward the circled figure, warm evening tungsten light,
shallow depth of field, photorealistic, subtle handheld drift
```
**Reject if:** the hand deforms, or the pen writes legible fake numbers.

### Shot 2 · input `blindspot_hero.png` · duration 7s (edit uses 0:03–0:09)
```
Medium shot: a man in his early 50s at a kitchen table in the evening
reading a financial statement, reading glasses low on his nose, he pauses
and touches his forehead in quiet concentration, slow lateral dolly right,
warm tungsten practicals mixed with cool dusk window light, photorealistic,
cinematic, natural micro-expressions
```
**Reject if:** expression turns theatrical/distressed — the brief is quiet concentration, not despair.

### Shot 3 · input `blindspot_laptop.png` · duration 7s (edit uses 0:09–0:15)
```
Over-the-shoulder shot: a man in his early 50s leaning toward an open laptop
on a kitchen table at night, screen glow on his face, he scrolls slowly and
gives a subtle nod as he reads, static camera with gentle breathing
movement, warm dark room where laptop light dominates, photorealistic,
cinematic
```
**Reject if:** the screen resolves into readable fake UI or text.

### Shot 4 · input `blindspot_exhale.png` · duration 5s (edit uses 0:15–0:19)
```
Medium close-up: a man in his early 50s closes his laptop halfway, leans
back, small relieved exhale and a faint smile, slow push in, warm lamp
light, photorealistic, natural relaxed body language
```
**Reject if:** the smile overshoots into grin territory — relief, not triumph.

### Shot 5 — CTA end card (0:19–0:22) — built in the edit, NOT Runway
- Off-white background, Titan Wealth Australia logo centred
- Line 1: **Book your free super review**
- Button graphic: "Learn more"
- Small print bottom: AFSL number + general advice warning (get exact wording from compliance — see Step 6)

---

## STEP 4 — Voiceover (ElevenLabs or VO artist)

Australian accent, male or female, calm and unhurried — think trusted GP, not salesperson. If using ElevenLabs: stability ~55, similarity ~75, speed 0.95.

**Script (record as one take, mark the beats):**

> *(0:03)* Most Australians set and forget their super. And fees quietly do their work in the background.
> *(0:09)* A thirty-minute review can show you exactly what you're paying — and what your options are.
> *(0:15)* That's it. Now you know.
> *(0:19)* Titan Wealth Australia. Book your free super review.

⚠️ Two lines in this script are pending compliance sign-off (see Step 6). Record after sign-off, or record both the original and the fallback lines:
- Fallback for line 1: "…and fees add up in the background."
- Fallback for line 2: "A thirty-minute review can show you what you're paying — and what your options are." (drops "exactly")

---

## STEP 5 — Edit assembly (CapCut / Premiere)

**Timeline (4:5 master, 1080×1350, 25fps):**

| Time | Video | Audio | Caption |
|---|---|---|---|
| 0:00–0:03 | Shot 1 | Paper foley + low pulse starts. NO VO. | "When did you last check your super fees?" — punches in word by word |
| 0:03–0:09 | Shot 2 | VO line 1, pulse continues | "set and forget" (mirrors VO) |
| 0:09–0:15 | Shot 3 | VO line 2 | "30-minute review. No cost."* |
| 0:15–0:19 | Shot 4 | VO line 3, pulse softens | "Clarity feels good." |
| 0:19–0:22 | End card | VO line 4, music resolves | (card carries the text) |

*"No cost" caption only if compliance confirms the review is genuinely unconditional — otherwise "30-minute review. Free."… which has the same problem, so the safe fallback is just "A 30-minute review."

**Edit notes:**
- Cut on motion where possible (pen circle completing → cut; nod → cut).
- Captions: clean geometric sans (Inter/Montserrat), white with 80% black backing bar, centre-safe for the 9:16 crop.
- Music: single low pulse bed, -18 LUFS under VO; VO at -14 LUFS integrated.
- Export: 4:5 H.264 master, then reframe centre-crop to 9:16 for Reels (action was framed centre-safe for this).

---

## STEP 6 — Compliance gate (BEFORE publishing) ⚠️

Do not publish until each item is signed off:

1. **"Fees quietly do their work"** — implies harm from fund fees; approve or use fallback "fees add up".
2. **"Exactly what you're paying"** — confirm the review deliverable actually shows this.
3. **"No cost" / "free"** — must be unconditionally true; state any conditions.
4. **General advice warning + AFSL number** — confirm required wording and whether it must be in-video (end card) or landing-page-only per Titan's licence conditions (ASIC RG 234).
5. **Synthetic actor + AI voice disclosure** — confirm Titan policy on AI-generated people/voice in financial promotions.
6. **Landing page** — AFSL, general advice warning, privacy policy live before spend starts.

---

## Asset checklist

- [ ] `blindspot_hero.png` (character anchor + Shot 2 input)
- [ ] `blindspot_statement.png` (Shot 1 input)
- [ ] `blindspot_laptop.png` (Shot 3 input)
- [ ] `blindspot_exhale.png` (Shot 4 input)
- [ ] 4× Runway clips (best take each, downloaded at max quality)
- [ ] VO file (plus fallback lines)
- [ ] End card (logo, CTA, AFSL small print)
- [ ] 4:5 master export + 9:16 crop
- [ ] Compliance sign-off on all 6 gate items
