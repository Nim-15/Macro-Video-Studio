# Black Bloom · tool preflight and run plan

**Checked:** 2026-10-22  
**Scope:** inspected the signed-in Artistly and VideoExpress interfaces, prepared BB-001 prompts, and attempted to submit the VideoExpress first/last-frame form. The interface stopped the request before generation because no endpoint images were selected. No images or video were created and no credits were consumed.

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
- No duration control is visible in the First Frame, Last Frame form. A 10-second clip in that specific mode is **not yet verified**.
- In the separate “Create Video From Prompt” mode, Advanced Mode exposes “Manual Video Length, sec” with a 3–10 second slider (initial value 5). This verifies a 10-second setting in that mode, but not its availability together with first/last-frame control.
- The First Frame, Last Frame form rejected the video submission with “Please select images for the first and last frames.” No generation started.
- Read-only inspection found the “Images” and “My Artistly Images” library folders empty. No personal images were selected or uploaded.
- The interface does not display the image or video cost before generation.

## Operational conclusion

The account UI shows first/last-frame controls and a separate 10-second setting, but it does **not** confirm that they work together in one video-generation run. Do not mark `videoexpress_10s` and `videoexpress_first_frame_reference` as jointly verified. The first approved test is blocked until both endpoint images exist. Creating those images requires additional generation actions, or the user can supply existing endpoint images.

## Prepared Black Bloom sequence

The existing prompt book remains authoritative for the five subjects and visual direction:

1. **BB-001 Iris:** start from its Artistly still; end at the soft violet droplet highlight on the left third.
2. **BB-002 Orchid:** begin by matching that violet highlight; end on the pale lilac highlight near upper center.
3. **BB-003 Rose:** begin on that glint; end on the defocused creamy crescent at right.
4. **BB-004 Calendula:** begin on the crescent; end on the small amber bokeh point lower center.
5. **BB-005 Dahlia:** begin on the amber point; end on the stable burgundy silhouette fading to black.

For each clip, preserve 16:9, black background, upper-left key/rim direction, restrained macro motion, and the prompt book's botanical realism constraints.

## BB-001 test prompts

The following text was entered in the VideoExpress form but not submitted for generation:

- **First frame:** photorealistic extreme macro of a single deep-violet iris petal on pure black; radial veins; a large clear dew droplet on the left third; restrained upper-left cool rim, faint warm bounce, shallow focus, landscape 16:9.
- **Last frame:** soft, out-of-focus violet dew highlight on the left third, pure black negative space on the right, same droplet placement and light direction.
- **Motion:** 10-second continuous slow macro push, subtle petal movement, rack focus from the iris veins to the anchored droplet; end on the left-third violet orb.

## Execution gates

1. Supply existing endpoint images or explicitly approve the required image-generation actions for this test. The app requires both first and last images before it will accept the video.
2. Before generating endpoint images, verify/record the actual allowance or cost if the application exposes it. No price was shown in the idle form.
3. Verify whether the First Frame, Last Frame mode can produce 10 seconds and use both endpoint images in one render. If it cannot, revise the test before further spending.
4. For chaining, inspect the actual final frame of each completed clip and use it as the next clip's first-frame reference where supported. Keep a continuity card with source/output asset IDs and frame descriptions.
5. For the full five-scene pilot, price stills, frame assets, video renders, and any retry reserve. Agree on a hard credit cap and obtain explicit user GO.
6. Generate one clip at a time. Stop after each render for endpoint, duration, and visual QA. Assemble only after the clips pass continuity review; the nominal 50 seconds assumes no overlap or trim.

## Public product references

- VideoExpress tutorials: https://videoexpress.ai/tutorials/index.html
- VideoExpress feature and plan page: https://videoexpress.ai/
- Artistly tutorials: https://artistly.ai/tutorials2/
- Artistly: https://artistly.ai/
