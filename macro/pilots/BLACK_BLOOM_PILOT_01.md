# BLACK BLOOM · Pilot production 01

**Status:** The first pass contains five 10-second clips on the saved timeline from 00:00 to 00:50. The user reviewed them and requested transition and subject-stability corrections. A v3 prompt pass now follows the user's copy-ready structure and one-image chaining rule. Two BB-001 v3 candidates failed endpoint-focus QA. One v3.1 retry failed endpoint visibility. The approved v3.2 fixed-camera test completed; its 0:10 endpoint is bright and detailed enough for continuity, and it has been saved as `BB-001_IRIS_LAST_FRAME_10S_V3_2` in My AI Images. Camera movement exceeded the prompt, but no clear subject deformation was visible.

## Goal

Produce five connected 10-second macro clips with visible in-clip entry and exit effects on a pure black background. Keep each effect within its clip duration. Style: premium botanical studio macro, realistic water droplets, very shallow optical focus, professional upper-left lighting, restrained motion. Nominal sequence length: **50 seconds** using direct adjacency; in-clip transition effects mark boundaries and no editor-side transitions are added.

## Verified VideoExpress route

Use **Create Video From Prompt** for the 10-second target. In Advanced Mode, enable **Manual Video Length, sec** and set it to **10**. The BB-001 prompt-mode test played at 0:10 / 0:10 in 16:9 at 1920×1080.

For each dependent clip:
1. In Media Library → **My AI Videos**, close the creator if needed, find the finished clip, and choose **Add to Timeline**.
2. From the finished clip's context menu, choose **Save Last Frame**. Name it `BB-00N_SUBJECT_LAST_FRAME_10S` and confirm it appears in **My AI Images**. This avoids seeking to the exact timeline boundary, which can show black after the clip ends.
3. Start **Create Video From Prompt**. Choose **Use from Library → My AI Images** and select the previous scene's saved endpoint.
4. Confirm the selected image, 16:9, **Photorealistic (Cinematic)**, Advanced Mode, and Manual Video Length = 10. Replace both sample prompts.
5. State that the selected image is the exact opening composition. Describe plausible motion and the planned exit state; do not ask the model to morph one flower species into another.
6. Generate one clip. Retrieve it from **Media Library → My AI Videos**, play it, verify runtime and continuity, add it to the timeline, save its endpoint, and continue.

## Generation discipline

- Reuse assets already in My AI Images/My AI Videos before creating replacements.
- Generate one approved master still for BB-001 only. For every later clip, use the preceding clip's saved endpoint; create a replacement still only if that endpoint is missing or unusable.
- Run one clip at a time because each next input depends on the actual preceding output.
- Check prompt, reference, aspect ratio, and 10-second setting before submitting.
- Never rerun an unchanged prompt. For a failed clip, record the defect, change only the relevant prompt or reference, and allow at most one targeted retry before revising the scene plan.
- Keep a checkpoint after every clip: scene ID, prompt version, source image, video asset, measured runtime, endpoint image, visible credit use, QA notes, and next scene.
- Existing membership generations are authorized for this pilot. Do not purchase top-ups, upgrades, or another subscription without explicit user authorization. Record usage only when shown in the account.

## Transition chain and current observations

The revised v3 prompt book is authoritative. Every clip must begin and end with a gradual in-clip light or optical effect; place clips directly adjacent with no editor-side cut, dissolve, wipe, fade, or separate transition duration. Preserve each subject's identity, species, silhouette, anatomy, proportions, texture, and position. Any color or subject change must happen gradually through plausible light, focus, refraction, bokeh, or shadow; reveal a new subject as distinct, never morph one into another. All effects fit inside the 10-second clip.

| Clip | Timeline | Current result | QA note |
|---|---:|---|---|
| BB-001 Iris | 00:00–00:10 | 10s, 1920×1080; endpoint `BB-001_IRIS_LAST_FRAME_10S` | Test render is on the saved timeline; visual approval and QA score pending. |
| BB-002 Orchid | 00:10–00:20 | 10s, 1920×1080; endpoint `BB-002_ORCHID_LAST_FRAME_10S.png` | Opening keeps violet petal/dew-drop composition. Mid-clip is soft lilac focus; orchid identity is unclear. Review before using as a quality target. |
| BB-003 Rose retry | 00:20–00:30 | Job `8ebacb3e-4a65-496f-b12c-357270cf3eb5`, 10s, 1920×1080; endpoint `BB-003_ROSE_RETRY_LAST_FRAME_10S.png` | Retrieved from My AI Videos, replaces the soft original, and resolves into a recognizable focused ivory rose. Exit is a warm close rose, not the planned creamy crescent. |
| BB-004 Calendula | 00:30–00:40 | Job `9725abe9-0160-4b10-a305-770a5f2ef303`, 10s, 1920×1080; endpoint `BB-004_CALENDULA_LAST_FRAME_10S` | Corrected render shows one orange flower with clear radial grooves and no rose overlap. Exit is a small dark orange-green bud, not the planned amber bokeh. Two earlier overlay/unclear candidates were rejected. |
| BB-005 Dahlia | 00:40–00:50 | Job `47376f6e-b3ce-445b-9829-4e270846ae0e`, 10s, 1920×1080; endpoint `BB-005_DAHLIA_LAST_FRAME_10S` | Opens on the actual BB-004 bud, shows a recognizable burgundy dahlia near 00:05, and fades nearly to black at 00:10. |

The current sequence is a **continuity and workflow proof**, not yet an approved quality master. BB-002 legibility and the BB-003→BB-004 visual handoff need review. BB-004→BB-005 follows the actual saved bud, so it no longer depends on the originally planned bokeh cue.

## Pilot review and scale gate

Score each clip 0–5 for botanical realism, water physics, camera stability, lighting continuity, entry/exit match, and temporal stability. Reject obvious anatomy defects, floating droplets, conspicuous morphing, flicker, or motion jumps.

Before extending production, review the complete 00:00–00:50 timeline at clip boundaries, record the scores, and decide whether to revise the weak links. Do not mark this pilot approved for a 60-minute production until that review is complete.

A 60-minute timeline made only from contiguous 10-second clips would require 360 clips. Treat that as a duration calculation, not a recommendation: test longer pacing and editorial reuse (carefully reviewed loops, still-image camera moves, and sound beds) before estimating generation volume. Measure the assembled timeline; transitions and overlaps affect runtime.

## Records

`pilot_state.example.json` contains the render IDs, current statuses, endpoint names, and verified workflow. This pilot is managed through the Artistly and VideoExpress interfaces; the repository does not contain an API integration. Keep credentials out of the repository.


## User correction · one-image chain and transition prompt v3

The first-pass review identified four requirements for the corrected run:

1. Every clip visibly opens with a transition-in effect and closes with a transition-out effect.
2. Keep principal subjects stable and recognizable. Avoid extreme changes, deformation, stretching, duplication, or species morphing; show only gradual, plausible macro-photography changes.
3. A subject or color change may occur within a clip through a creative but realistic light/optical effect.
4. The paired in-clip effects alone mark adjacent scene boundaries. Place clips directly together and add no editor-side transition or extra duration.

The copy-ready video prompt uses the exact section order and timing the user supplied: **ENTRY TRANSITION, 0–2s; MAIN ACTION, 2–8s; EXIT TRANSITION, 8–10s**. Generate only the BB-001 master still; each subsequent clip uses the actual last frame of the previous clip.

The Artistly master still generated for BB-001 is visible in Artistly Personal Designs, but the VideoExpress **My Artistly Images** folder was empty, so it was not available as a source for the video render. The two v3 jobs instead used the already available `BB-001_IRIS_LAST_FRAME_10S.png` in **My AI Images**.

Two v3 candidates are present in **My AI Videos** (6.17 MB and 4.73 MB; the UI did not map their IDs to file sizes). The 6.17 MB candidate was reviewed first; its 0:10 frame was too soft/defocused to use. The 4.73 MB candidate was then played in VideoExpress; it also progressively pushed into the droplet but ended with the droplet/petal visibly soft and lacking sufficient detail for a chain endpoint. Neither candidate was added to the timeline, and no endpoint was saved. The duplicate submission resulted in two renders. A single planned targeted retry also completed; no further generation is authorized under the current pilot retry rule.

**Resume:** the v3.1 retry (job `61e23ee8-24a8-446b-adf2-74cb15ee8c7c`, 6.25 MB) completed at 10 seconds but its 0:10 frame is nearly black and lacks useful droplet/petal detail. It was rejected, not added to the timeline, and no endpoint was saved. Replan BB-001 to keep the subject visibly detailed at 0:10 and avoid a whole-frame exposure fade. The prompt book now has a revised v3.2 shot plan: fixed camera, locked focus and subject exposure, localized light effects only, and no whole-frame fade. Job `0bae5c1a-83d7-4f0c-a9e7-5b38d32654d5` completed (6.55 MB; 10s, 1920×1080). Its final frame was visually checked, saved as `BB-001_IRIS_LAST_FRAME_10S_V3_2`, and approved as the starting reference for BB-002. BB-002 job `b9530504-825c-4ac9-ab32-9601322c2194` has been submitted from that saved frame and is pending in My AI Videos.


## BB-002 v3.2 endpoint review

BB-002 job `b9530504-825c-4ac9-ab32-9601322c2194` completed at 10 seconds, 1920×1080, 6.19 MB. Its opening closely matches the saved BB-001 v3.2 endpoint. At 0:04 the lilac form remains soft and orchid identity is unclear; at 0:09 the iris petal, radial veins, and attached droplet are sharp and stable, while a distinct Phalaenopsis shape is not legible. The endpoint is suitable for chain continuity but the orchid reveal missed its visual target. Saved the actual last frame to My AI Images as `BB-002_ORCHID_LAST_FRAME_10S_V3_2`. BB-003 may proceed from this exact endpoint; keep camera/focus/exposure locked and make the intended rose reveal readable through restrained in-clip lighting.


## BB-003 v3.2 render in progress

Submitted BB-003 job `59555434-96aa-4a5d-84f7-df39577de405` from the exact saved `BB-002_ORCHID_LAST_FRAME_10S_V3_2` reference. Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Manual Video Length = 10 seconds; automatic prompt enhancement off. The revised prompt keeps the iris/droplet sharp with locked camera, focus, and exposure, and reveals a distinct ivory rose only through localized background light. Review the render's opening and 0:10 endpoint before continuing.


## BB-003 v3.2 endpoint review

BB-003 job `59555434-96aa-4a5d-84f7-df39577de405` completed at 10 seconds, 1920×1080, 4.27 MB. The opening keeps the violet iris and attached droplet but reinterprets the composition rather than matching BB-002's saved frame exactly; an ivory flower is already visible in the background. At 0:10 the droplet and iris remain detailed and the cream flower stays distinct but soft; no clear species morphing is visible. Saved the endpoint as `BB-003_ROSE_LAST_FRAME_10S_V3_2` in My AI Images. It is usable for continuity with composition drift recorded. BB-004 should start from this actual endpoint and respect its framing.


## BB-004 v3.2 render in progress

Submitted BB-004 job `ccd9bc50-68fe-4ab8-bea6-260c1f45f8a7` from the exact saved `BB-003_ROSE_LAST_FRAME_10S_V3_2` reference. Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Manual Video Length = 10 seconds; automatic prompt enhancement off. The prompt follows the actual iris/rose composition and aims to reveal a separate calendula through localized amber light while preserving the subjects and locked camera/focus/exposure. Review the opening and final frame before continuing.


## BB-004 v3.2 endpoint review

BB-004 job `ccd9bc50-68fe-4ab8-bea6-260c1f45f8a7` completed at 10 seconds, 1920×1080, 5.56 MB. The opening retains the violet petal, droplet, and ivory flower with a slight warm glow already present. At 0:10 a distinct orange radial-petal flower appears, but visually overlaps/blends with the ivory rose, and the droplet darkens significantly. The iris remains recognizable. Saved `BB-004_CALENDULA_LAST_FRAME_10S_V3_2` in My AI Images for continuity, with these limitations recorded. BB-005 should use this actual endpoint and avoid overlapping flower silhouettes while keeping the droplet bright and legible.


## BB-005 v3.2 render in progress

Submitted the final pilot clip, BB-005 job `33e10c28-01e7-4371-95cd-b84a43c04a2d`, from `BB-004_CALENDULA_LAST_FRAME_10S_V3_2`. Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Manual Video Length = 10 seconds; automatic prompt enhancement off. The prompt keeps the actual iris/droplet and flower layers, then introduces only a small separate burgundy dahlia petal at the far right. Review the opening and endpoint before saving it or assembling the five-clip v3.2 chain on the timeline.


## BB-005 v3.2 endpoint review and pilot chain status

BB-005 job `33e10c28-01e7-4371-95cd-b84a43c04a2d` completed at 10 seconds, 1920×1080, 4.77 MB. Its opening broadly retains the BB-004 violet petal/droplet and orange/cream layers, with some composition drift. At 0:09 the droplet and foreground petal are readable and a small burgundy dahlia-like form appears separately at far right. Several flower layers still overlap visually, and the ivory flower remains prominent; no clear subject morphing is visible. Saved `BB-005_DAHLIA_LAST_FRAME_10S_V3_2` in My AI Images.

All five v3.2 clips now have reviewed saved endpoints and can be assembled in sequence. Their continuity is visually workable, but BB-002's orchid identity is soft, BB-003/004 drift in composition, and BB-004/005 show overlapping layers. The five updated renders are **not yet assembled on the timeline**. Next, create a separate v3.2 timeline or project copy, preserve the existing first-pass project, place BB-001–BB-005 contiguously with no editor-side transitions, then review the full 50-second chain at all four boundaries.


## v3.2 chain assembled

Created and saved a separate VideoExpress project named **Black Bloom Pilot 01 - v3.2 Chained**, after saving the pre-existing first-pass project. Added the five reviewed v3.2 videos in order using **Add to Timeline** at 00:00, 00:10, 00:20, 00:30, and 00:40. The timeline shows five adjacent 10-second clips, with no editor-side transition clips, and its timecode reaches 00:00:50. The BB-001→BB-002 and BB-002→BB-003 placements were visually checked at 00:10 and 00:20; all five clip placements are visible contiguously in the saved timeline. Project save succeeded.

The chain is assembled, but final boundary-by-boundary playback review and quality scoring remain. Known issues: BB-002's orchid identity is soft/unclear; BB-003 reframes relative to its input; BB-004 has visually overlapping flower layers and a darker droplet; BB-005 retains multiple overlapping layers. Review the four boundaries before treating the sequence as a quality-approved master or expanding toward a longer production.


## User acceptance and next iteration

The user confirmed that the production process is complete and correct, including the five-clip chain and its joins. Keep the validated workflow unchanged: one 10-second render per clip, the immediately preceding saved last frame as the next clip's starting image, entry and exit effects contained inside each clip, and direct adjacency on the timeline without extra editor transitions. The next work is limited to improving prompt-driven composition and subject readability. Make targeted prompt revisions one scene at a time and review before spending further generation credits; do not rerun unchanged prompts. The existing first-pass project remains preserved.


## Targeted prompt refinement: BB-002 v3.3

Reviewed the documented v3.2 QA and prepared one targeted prompt revision for the orchid reveal. The observed issue was that the orchid remained soft and unrecognizable, while the incoming iris and droplet stayed sharp. The v3.3 prompt now specifies the Phalaenopsis lip, broad rounded petals, central column, natural veins, and visible surface detail; fixes the bloom to frame right at roughly 45–55% of the frame; locks camera, focus, and exposure; and uses a narrow lilac light reveal with black negative space separating the incoming iris from the orchid. It also lets the outgoing iris recede into shadow without morphing.

This is a prompt-only revision; no new video has been generated. The approved v3.2 project and joins remain untouched. Next validation, if the prompt is accepted, is one 10-second BB-002 render from the existing BB-001 v3.2 saved last frame, followed by endpoint review before any other generation.


## BB-002 v3.3 readability test result

The targeted render completed in VideoExpress at 10 seconds, 1920×1080, 5.89 MB (job `4d2f2226-f8ca-402f-9a58-8966acc5ef24`). It starts from `BB-001_IRIS_LAST_FRAME_10S_V3_2`. The Phalaenopsis is now clearly recognizable, with its broad petals and characteristic central lip; the iris recedes separately into shadow. The endpoint is a tighter close-up than requested and crops part of the upper petal, so composition still needs refinement. Saved the endpoint as `BB-002_ORCHID_LAST_FRAME_10S_V3_3` in My AI Images.

This is a separate prompt test only: it was not added to or substituted into the user-approved v3.2 timeline. For the next iteration, refine BB-003 from the actual v3.3 orchid endpoint and specify fixed camera distance, generous framing margins, readable rose anatomy, and no overlapping flower layers. Review the prompt before the next generation.


## BB-003 v3.3 rose test and next prompt

The BB-003 v3.3 render completed at 10 seconds, 1920×1080, 4.25 MB (job `3bc10d9e-a4c5-4a26-b3c4-cf4115b66380`) from `BB-002_ORCHID_LAST_FRAME_10S_V3_3`. The ending is a clear, centered ivory rose with a recognizable layered spiral and central curl. The rose reads as a separate subject, with less flower overlap. Two composition issues remain: outer petals touch or crop at the upper/lower frame edge, and the rose begins appearing before the 2-second entry hold ends. Saved the endpoint as `BB-003_ROSE_LAST_FRAME_10S_V3_3` in My AI Images.

Prepared a BB-004 v3.3 prompt from that actual rose endpoint. It delays the calendula reveal until after the opening hold, specifies visible ray petals and central disk, locks camera framing, gives the new flower black margins, and lets the outgoing rose recede into shadow as a separate subject. The BB-003 test is separate and has not been added to the accepted v3.2 project. BB-004 is ready for one targeted render after prompt review.


## BB-004 v3.3 result and v3.4 prompt refinement

BB-004 job `9d42dc21-fee7-476a-98b8-e35081294df2` completed as a 10-second 1920×1080 render (4.47 MB) from `BB-003_ROSE_LAST_FRAME_10S_V3_3`. Visual review at 0:04 and 0:08 showed the incoming ivory rose still dominating; no recognizable calendula appeared. At 0:10 the image was very dark and the rose remained the visible subject. The delayed entry, new-subject reveal, and exposure hold all missed their targets. No endpoint was saved, and the trial was not added to the accepted v3.2 timeline.

The BB-004 v3.4 prompt now calls for a complete, unmistakable calendula by mid-clip, with its circular disk and narrow radial petals visible, a fixed camera and exposure, full framing margins, and the incoming rose kept anatomically separate as it recedes into localized shadow. The final frame must keep the calendula bright and stable. The next run should use the same v3.3 rose endpoint and save an endpoint only if it is useful for BB-005. The approved v3.2 timeline and its joins remain unchanged.


## BB-004 v3.4 endpoint review

BB-004 v3.4 job `6d834f3d-2154-4d75-b3ba-78d0463ec529` completed at 10 seconds, 1920×1080, 4.04 MB, from `BB-003_ROSE_LAST_FRAME_10S_V3_3`. The first seconds retain the centered rose. By 0:03 a separate orange radial flower begins to appear; at 0:07–0:10 its central disk and ray petals are clearly legible as a calendula, while the rose recedes as a distinct dim bloom. A restrained dolly-back creates separation without visible flower morphing. The light dips during the exit transition, then the final frame settles bright with the full calendula silhouette inside the frame and narrow margins. Saved the actual endpoint as `BB-004_CALENDULA_LAST_FRAME_10S_V3_4` in My AI Images.

This v3.4 render remains a separate test and was not added to the user-approved v3.2 timeline. BB-004 v3.3 failed and no endpoint was saved from it. Next, prepare BB-005 from the saved v3.4 calendula endpoint; reveal a distinct burgundy dahlia while preserving flower separation, full margins, and a stable bright endpoint.


## BB-005 v3.4 trial and endpoint review

Prepared the BB-005 prompt from the actual `BB-004_CALENDULA_LAST_FRAME_10S_V3_4` endpoint. The prompt holds the calendula at the opening, lets the dim rose remnant recede first, then reveals a separate burgundy dahlia at frame left with a controlled macro dolly-back and no flower morphing.

BB-005 job `6a288ce0-53ef-425e-93f8-b381c9092d27` completed at 10 seconds, 1920×1080, 5.50 MB. At 0:06, the dahlia's layered burgundy petals and center are clearly recognizable; the calendula recedes separately at frame right. By 0:09–0:10 the dahlia dominates in a sharp macro close-up. The upper petals have a slight top-edge crop, but there is no clear species morphing or bloom overlap. Saved the actual last frame as `BB-005_DAHLIA_LAST_FRAME_10S_V3_4` in My AI Images.

This is a separate test, not a replacement for the accepted v3.2 timeline. BB-004 v3.4 and BB-005 v3.4 now form the latest endpoint chain for those scenes; the next quality check is to review the revised clips and joins together in a separate trial project before choosing whether to replace anything in the approved project.


## BB-004 → BB-005 v3.4 seam test

Saved a separate VideoExpress project named **Black Bloom - Seam Test BB-004 to BB-005 v3.4**. The Open Project list shows it separately from the accepted **Black Bloom Pilot 01 - v3.2 Chained** project. BB-004 v3.4 and BB-005 v3.4 are placed directly adjacent on one track: 10 seconds each, 20 seconds total, with no editor-side transition.

The boundary was checked at 00:09 and 00:10. The calendula with the dim outgoing rose remnant carries into the BB-005 opening without an obvious visual jump. **The BB-004→BB-005 seam passes.** At 00:16, the new burgundy dahlia is recognizable, but its scale crops the bloom at the left and upper frame edges. Refine BB-005 framing before considering any replacement of a clip in the approved v3.2 project; keep both projects separate.


## BB-005 v3.5 framing correction submitted

The v3.4 seam test passes, but the dahlia is cropped at the left and upper edges during its reveal. Submitted one targeted BB-005 correction from the actual `BB-004_CALENDULA_LAST_FRAME_10S_V3_4` endpoint (VideoExpress job `8203cf15-829b-443d-865d-02be9b21650e`). The revised prompt locks the camera and limits the complete dahlia to 35% of frame width and 55% of frame height, with at least 8% margins from the top, left, and bottom. It requires the complete bloom and center to be readable by 6 seconds and held within frame through 10 seconds.

Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Video Only, Manual Video Length = 10 seconds, prompt enhancement off. The render is pending in My AI Videos. Review 00:06, 00:09, and 00:10 before saving its endpoint or adding it to a separate seam test. Do not alter the accepted v3.2 timeline.


## BB-005 v3.5 framing test result

BB-005 v3.5 (job `8203cf15-829b-443d-865d-02be9b21650e`) completed at 10 seconds, 1920×1080, 5.83 MB. The opening matches the BB-004 v3.4 endpoint. At 00:06, 00:09, and 00:10 the burgundy dahlia remains oversized and cropped at the frame edges despite explicit size limits and margins. Rejected: no endpoint saved and no timeline insertion. Revise the shot approach before another attempt.


## BB-005 v3.6 wide-macro test submitted

To address the repeated crop, the scene plan now uses a wide macro composition from a moderate working distance, with the camera stationary and the complete dahlia kept small in frame (about 20–25% of frame width) against broad black negative space. Submitted one render from the same `BB-004_CALENDULA_LAST_FRAME_10S_V3_4` endpoint (job `8561d318-fbed-415f-b224-fe158aaed617`). Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Video Only, Manual Video Length = 10 seconds, prompt enhancement off. The render is pending in My AI Videos; inspect the opening, 00:06, 00:09, and 00:10 before accepting it. Keep it out of the timeline if the flower is still cropped, and preserve the approved v3.2 project.



## BB-005 v3.6 wide-macro result and separate seam test

BB-005 v3.6 (job `8561d318-fbed-415f-b224-fe158aaed617`) completed at 10 seconds, 1920×1080, 7.26 MB from `BB-004_CALENDULA_LAST_FRAME_10S_V3_4`. The opening continues the incoming calendula/rose-remnant composition without an obvious jump. Around 00:06 the burgundy dahlia grows too large and is cropped; by 00:09–00:10 its silhouette is mostly/fully inside frame, while the calendula remains bright and cropped at frame right. Saved the actual endpoint as `BB-005_DAHLIA_LAST_FRAME_10S_V3_6` in My AI Images. This is a candidate, not an approved replacement.

Created and saved a separate 20-second VideoExpress project named **Black Bloom - Seam Test BB-004 to BB-005 v3.6**, with BB-004 v3.4 followed directly by BB-005 v3.6 and no editor-side transition. At 00:09–00:10 the flower composition carries into the new clip without an obvious abrupt jump; at 00:11 the dahlia becomes dominant while the outgoing flower composition remains visible. **The seam passes for continuity.** The v3.6 crop/scale issue remains in the clip itself, so do not promote it into the approved timeline without a separate selection decision. The accepted **Black Bloom Pilot 01 - v3.2 Chained** project remains unchanged.

Next: compare the v3.6 framing candidate in the saved test project. If it is accepted, promote it only into a new pilot iteration; otherwise refine the prompt to keep the dahlia small throughout and reduce the bright cropped calendula at frame right.


## BB-005 v3.7 fixed-scale retry submitted

After the v3.6 seam passed but its dahlia grew oversized mid-clip, submitted one targeted BB-005 retry from the same actual `BB-004_CALENDULA_LAST_FRAME_10S_V3_4` source. VideoExpress job: `f5921870-e16e-489f-a2ab-e5c3468b635a`. The v3.7 prompt holds the camera and lens distance fixed, reveals the burgundy dahlia through localized rim light, dims the outgoing rose and calendula, and requires the complete dahlia to remain at a consistent 20–25% frame width with black separation and generous margins throughout. Settings: 16:9, Photorealistic (Cinematic), Advanced Mode, Video Only, Manual Video Length = 10 seconds, prompt enhancement off. The job is rendering in My AI Videos. Review its opening, middle, and endpoint before saving an endpoint or adding it to another test project. The accepted v3.2 chain remains unchanged.


## BB-005 v3.7 result — scale prompt rejected

VideoExpress job `f5921870-e16e-489f-a2ab-e5c3468b635a` completed at 10 seconds, 1920×1080, 5.60 MB from `BB-004_CALENDULA_LAST_FRAME_10S_V3_4`. The opening at 00:00 matches the saved source composition. At 00:05 the dahlia and calendula both occupy much of the frame, with the dahlia cut off at the left edge. At 00:09 the dahlia has grown oversized and is cropped at the left and bottom; the calendula remains a large, dim competing subject. The v3.7 scale-lock prompt did not achieve the requested framing. Rejected: no endpoint saved and no timeline insertion.

Prompt-only scale constraints have failed repeatedly. Do not spend another generation on the same approach. Next, change the method first: inspect whether a duplicated clip can be resized/repositioned in VideoExpress without regeneration, or prepare a wider source composition that keeps the dahlia farther from the camera. Test that method separately, leaving **Black Bloom Pilot 01 - v3.2 Chained** and the saved v3.6 seam project untouched.


## Non-generative Resize and Move diagnostic

To avoid another prompt-only render, duplicated the v3.6 seam project as **Black Bloom - BB-005 Resize Test v3.7** and tested VideoExpress's timeline **Resize and move** control on BB-005 v3.6. Reducing the full clip image to about 80% creates black margins and makes the flower smaller in the frame. However, at 00:17 the dahlia remains cut at the source video's own left/bottom boundary; scaling the frame cannot restore petals the render already cropped. Saved this diagnostic copy separately. It is not a composition fix and is not promoted to the approved project.

**Next:** keep the accepted v3.2 chain as the production baseline and finish its four-boundary QA. For a later BB-005 visual iteration, change the source/shot strategy materially before generating again; do not repeat prompt-only scale limits or use Resize and move as a crop repair.
