---
description: Generate video ad concepts with Runway Gen-4.5 shot lists
argument-hint: [campaign topic]
allowed-tools: Read, Write, Bash
---

# Video Ad Studio

Campaign input: $ARGUMENTS

Generate 2 video ad concepts, 15-30 seconds each, structured for Runway Gen-4.5 (image-to-video). For each concept:

1. **Hook (0-3s)** — the scroll-stopper line/visual
2. **Shot list** — 3-5 shots, each with:
   - Duration (Gen-4.5 supports 2-10s per generation)
   - Camera direction (e.g. "slow push in", "static wide")
   - Runway prompt text (lead with shot type per Runway's prompting guide)
   - Reference image needed (what still image feeds this shot)
3. **Voiceover/caption script** — synced to shots
4. **CTA (final 3-5s)**
5. **Compliance flag** — anything needing sign-off before publishing

Save to /ad-drafts/[date]-video-concepts.md
