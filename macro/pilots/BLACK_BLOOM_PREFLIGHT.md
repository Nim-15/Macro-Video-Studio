# Black Bloom · tool preflight and run plan

**Checked:** 2026-10-23  
**Scope:** inspected the signed-in Artistly and VideoExpress interfaces, prepared BB-001 prompts, and ran one authorized VideoExpress first/last-frame test with generated endpoint images. One test video and two stills were generated; no other Black Bloom clips were started.

## Observed in the applications

### Artistly

- Dashboard identifies Artistly v6.5 and links to its image design tools.
- The “Create Design” route offers Fast AI Image Designer and Advanced AI Image Designer.
- The Fast AI Image Designer has a Photorealism category and offers 16:9 output at 1344 × 768 px.
- Artistly's dashboard links to VideoExpress as a separate tool for turning Artistly images into video.
- Still generation and its cost/allowance have not been tested.

### VideoExpress

- The signed-in editor exposes a “First Frame, Last Frame” generation mode.
- Its form has separate First Frame Prompt and Last Frame Smart Edit fields, with separate “First Frame from Library (beta)” and “Last Frame from Library (beta)” selectors. It also exposes Create First Image, Create Last Image, and Create Video actions.
- The 16:9 landscape choice is present in this mode. The form recommends 9:16 for best quality and prompt adherence, so 16:9 pilot quality remains to be assessed.
- No duration control is visible in the First Frame, Last Frame form. A 10-second clip in that specific mode is **not supported by this test result**: the generated test clip played for 7 seconds.
- In the separate “Create Video From Prompt” mode, Advanced Mode exposes “Manual Video Length, sec” with a 3–10 second slider (initial value 5). This verifies a 10-second setting in that mode, but not its availability together with first/last-frame control.
- The initial submission attempt was rejected with “Please select images for the first and last frames.” After generating and selecting the two endpoint images, one BB-001 test video completed.
- Before the test, the “Images” and “My Artistly Images” library folders were empty. The test used generated endpoint images, not personal uploads.
- The interface does not display the image or video cost before generation.

## Operational conclusion

The account UI exposes two workable routes with different behavior. **First Frame, Last Frame** accepted both generated endpoints but produced a 7-second video and only approximated its final image. **Create Video From Prompt** with Advanced Mode and Manual Video Length set to 10 produced a video confirmed at 0:10 / 0:10. That clip was added to the editor timeline; the playhead was set to 00:00:10; Save Current Frame stored `BB-001_IRIS_LAST_FRAME_10S.png` in My AI Images; the saved image was selectable as the starting image in a new Create Video From Prompt form. This verifies a practical chained workflow via editor frame capture, but does not test a second generated clip. Both videos report 1920×1080. No numeric credit charge was displayed.

## Prepared Black Bloom sequence

The existing prompt book remains authoritative for the five subjects and visual direction:

1. **BB-001 Iris:** start from its Artistly still; end at the soft violet droplet highlight on the left third.
2. **BB-002 Orchid:** begin by matching that violet highlight; end on the pale lilac highlight near upper center.
3. **BB-003 Rose:** begin on that glint; end on the defocused creamy crescent at right.
4. **BB-004 Calendula:** begin on the crescent; end on the small amber bokeh point lower center.
5. **BB-005 Dahlia:** begin on the amber point; end on the stable burgundy silhouette fading to black.

For each clip, preserve 16:9, black background, upper-left key/rim direction, restrained macro motion, and the prompt book's botanical realism constraints.

## BB-001 test prompts

The following prompts were entered in the VideoExpress form and used for the BB-001 test:

- **First frame:** photorealistic extreme macro of a single deep-violet iris petal on pure black; radial veins; a large clear dew droplet on the left third; restrained upper-left cool rim, faint warm bounce, shallow focus, landscape 16:9.
- **Last frame:** soft, out-of-focus violet dew highlight on the left third, pure black negative space on the right, same droplet placement and light direction.
- **Motion:** 10-second continuous slow macro push, subtle petal movement, rack focus from the iris veins to the anchored droplet; end on the left-third violet orb.

## Execution gates

1. Use Create Video From Prompt with Advanced Mode and Manual Video Length = 10 for each scene. Add each completed clip to the timeline, move the playhead to its end, save the current frame to My AI Images, then select that image as the next clip's starting reference. Preserve each transition card's subject, light, composition and movement cues.
2. Before the remaining three Black Bloom scenes, check the current credit/allowance balance and estimate the run cost. The interface did not display a numeric charge for either test.
3. Generate one scene at a time and verify duration, saved endpoint and visual continuity before continuing. The five-clip pilot should use this chained route; the 7-second First Frame, Last Frame result is unsuitable for the 10-second target.

## Public product references

- VideoExpress tutorials: https://videoexpress.ai/tutorials/index.html
- VideoExpress feature and plan page: https://videoexpress.ai/
- Artistly tutorials: https://artistly.ai/tutorials2/
- Artistly: https://artistly.ai/


## BB-001 test result · 2026-10-23

- Generated first-frame image: `e8e9ff41-8a05-4966-ac58-b460182a79c7`.
- Generated last-frame image: `f07103f6-09dc-4414-863b-a8795adc2e24`.
- VideoExpress completed one MP4 in First Frame, Last Frame mode. Its player showed **0:07 / 0:07**, although the motion prompt requested 10 seconds. The observed output is 1920×1080.
- The opening image visibly matches the iris petal and dew composition. The closing image remains a purple petal with luminous droplets; it is compositionally related to the supplied end frame, but not an exact match to the single-soft-orb instruction.
- Result: **first/last image mode confirmed; 10-second duration and exact end-frame adherence failed this test.** No additional pilot clips were generated.
- VideoExpress did not show a numeric credit charge or price in the generation interface, so the consumed amount cannot be reported from the observed UI.


## BB-002 workflow verification · 2026-10-23

- In Create Video From Prompt, Advanced Mode exposed “Manual Video Length, sec”; it was enabled and set to **10**. The image type was “Photorealistic (Cinematic)” and aspect ratio 16:9.
- Generated one photorealistic violet iris image as the base and one 10-second macro video (video ID: `e988ac91-3941-4a2c-9a7d-8e8aa94b521a`). The player visibly reported **0:10 / 0:10**.
- Added the MP4 to the timeline. At playhead **00:00:10**, used **Save current frame**, named the saved image `BB-001_IRIS_LAST_FRAME_10S`. VideoExpress confirmed it was saved to **My AI Images**; the image list showed `BB-001_IRIS_LAST_FRAME_10S.png` at 1920×1080.
- Opened a new Create Video From Prompt form and selected that saved frame with **Use from Library**. It appeared as the form's image reference, confirming it is reusable as the next clip's start. No second chained video was generated.
- Verified route: **10-second prompt video → Add to Timeline → seek to clip end → Save Current Frame → select saved image as next prompt-video reference**.
