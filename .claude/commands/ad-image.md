---
description: Generate still image ad concepts + Higgsfield-ready prompts
argument-hint: [campaign topic, e.g. "UK Pension Roadmap - warning hook"]
allowed-tools: Read, Write, Bash
---

# Still Image Ad Studio

Campaign input: $ARGUMENTS

Generate 3 distinct still image ad concepts for Meta (Facebook/Instagram). For each:

1. **Hook type** (warning/curiosity/social proof/etc.)
2. **Headline** (under 40 chars, Meta primary text under 125 chars)
3. **Visual concept** — what's actually in frame
4. **Higgsfield prompt** — full production-ready prompt including:
   - Subject, setting, lighting, camera angle
   - Photorealism keywords (85mm lens, natural light, etc.)
   - Aspect ratio: 1:1 and 4:5 versions
5. **Text overlay** if any (keep minimal — Meta penalizes text-heavy images)
6. **Compliance flag** — note anything that needs sign-off before this runs (e.g. implied guarantees, "warning" language that could read as advice)

Save all concepts to /ad-drafts/[date]-image-concepts.md
