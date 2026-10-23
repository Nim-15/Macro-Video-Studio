# Membership credits, generation efficiency, and production controls

Use the user's existing paid membership for the pilot. Treat included credits as available for authorized production, while tracking actual use whenever VideoExpress or Artistly exposes it. No top-up, upgrade, or new subscription without explicit user authorization. Do not invent per-generation prices or assume the membership is unlimited.

## Efficient generation plan
- Inspect existing My AI Images and My AI Videos first. Reuse an approved image or endpoint whenever it fits the shot.
- Generate only the initial still needed to establish the first scene. For chained scenes, save each finished clip's endpoint in the editor and reuse it from My AI Images as the next clip's image reference.
- Use the tested VideoExpress route: Create Video From Prompt, 16:9, Photorealistic (Cinematic), Advanced Mode, Manual Video Length = 10 seconds.
- Produce dependent clips sequentially, one at a time; each actual endpoint is needed before setting the following clip's start reference.
- Before each render, verify scene ID, reference image, both prompt fields, settings and transition handoff. This catches avoidable renders caused by placeholder text or the wrong settings.
- Review each output before proceeding. Record actual runtime, visible credit use, asset IDs and QA result. Never rerun an unchanged prompt.
- If a render has a specific defect, make one targeted correction and retry at most once before rethinking the shot.

## Planning math
- Five 10-second pilot clips = 50 seconds of generated footage before trims and overlaps.
- A 60-minute program at 10 seconds per clip would require 360 usable clips only if there are no trims or overlaps; calculate final runtime from the actual timeline.
- Estimate expected membership-credit use from the account's current usage display and observed generation cost when available. Separate observed use from estimates; if no numeric cost is exposed, state that clearly.
