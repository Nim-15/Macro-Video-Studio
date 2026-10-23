# Macro Film Transitions

**Default preference:** a continuous-frame handoff. Each clip has an authored entry and exit state; do not assume the model or editor implements it.

## Transition types
1. **Direct continuation:** same reference frame, subtle movement continues; use only after first/last-frame capability test.
2. **Optical match cut:** match droplet positions, petal contours, highlights or micro-patterns, even with a different subject.
3. **Rack-focus handoff:** scene N ends in defocus, scene N+1 begins near the same focal color/shapes and resolves gradually.
4. **Editor dissolve:** 0.5–2 seconds when justified, with timeline overlap counted.
5. **Chapter blackout:** deliberate dark pause for a new visual family; count time toward final runtime.

## Continuity card for every adjacent pair
- A final frame URI, if available.
- A frame description (subject coordinates, scale, motion, illumination, focus distance and color).
- B opening reference URI/description and matching restrictions.
- Transition type, proposed overlap and independently measured final timing.

## Timing
For pure cuts and 360 clips × 10s, runtime = 3,600s. For overlapping dissolves, actual timeline is **sum of clip lengths minus overlap duration**, plus other edits/holds. Do not promise exactly 60 minutes until the timeline is measured.

## Verified chained handoff · VideoExpress

The tested pilot route is **Create Video From Prompt → Add to Timeline → seek to the clip end → Save current frame → select that saved still from My AI Images for the next prompt-video form**. A 10-second BB-001 output was observed at 0:10 / 0:10 and the saved frame was selectable in the next form.

Treat this as a reusable start-frame handoff, not proof that the next generated clip will reproduce it pixel-perfectly. Verify the opening frame on every render. If the scene change would require implausible flower morphing, use a controlled optical match cut or short editor dissolve while keeping the authored transition shape, color, and light cue.
