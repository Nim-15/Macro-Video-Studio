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

The account UI shows first/last-frame controls and a separate 10-second setting, but the combined mode test rendered **7 seconds**, despite a 10-second motion prompt. First/last-frame mode therefore works in a single run, while a 10-second duration in that mode is **not verified**. The output begins on the supplied iris composition and ends on a related purple-petal composition with several glowing droplets, but it does not exactly match the supplied final image. Do not mark `videoexpress_10s` as verified. The video file reports 1920×1080; no cost amount was shown in the interface.

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

1. For chaining, inspect the actual final frame of each completed clip and use it as the next clip's first-frame reference where supported. Keep a continuity card with source/output asset IDs and frame descriptions.
2. Before the remaining four scenes, establish the cost/credit impact and a hard cap; the UI did not show a price during this test.
3. Generate one clip at a time. Stop after each render for endpoint, duration, and visual QA. Assemble only after the clips pass continuity review; the nominal 50 seconds assumes no overlap or trim.

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
