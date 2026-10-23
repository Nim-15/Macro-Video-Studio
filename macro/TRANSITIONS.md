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

The tested route is **Create Video From Prompt → add the finished clip to the timeline → save the endpoint with the clip's Media Library context menu → Save Last Frame → select that still from My AI Images in the next prompt-video form**. BB-001 and BB-002 were both 10-second, 1920×1080 clips; BB-002 followed BB-001 contiguously and its 831 KB saved endpoint was selectable for the next prompt. Using Save Last Frame is simpler and avoids seeking to the exact timeline boundary, which showed black at the 20-second boundary. The BB-002 render retained the violet-droplet palette, but the orchid remained indistinct and mostly soft focus.

Treat this as a reusable start-frame handoff, not proof that the next generated clip will reproduce it pixel-perfectly. Verify the opening frame on every render. If the scene change would require implausible flower morphing, use a controlled optical match cut or short editor dissolve while keeping the authored transition shape, color, and light cue.


BB-003 rendered at 10 seconds / 1920×1080 from `BB-002_ORCHID_LAST_FRAME_10S.png` and was added at 00:20–00:30. Opening continuity is strong; the later ivory petal forms remain soft focus and the rose identity is only partly legible. The endpoint `BB-003_ROSE_LAST_FRAME_10S.png` (545.04 KB) is available in My AI Images. Review before continuing; an editor-side optical match cut to the amber calendula crescent may avoid carrying the soft endpoint as an image reference.


BB-003 targeted retry `8ebacb3e-4a65-496f-b12c-357270cf3eb5` completed according to VideoExpress notification, but remains unreviewed because it did not appear in the library's `My AI Videos` or `Videos` folders. Keep the existing 00:20–00:30 clip until this candidate can be inspected; do not propagate another generation before review.
