# Black Bloom · tool preflight and run plan

**Checked:** 2026-10-22  
**Scope:** read-only inspection of the signed-in Artistly and VideoExpress interfaces. No prompts were submitted to generators; no images or videos were created; no credits were consumed.

## Observed in the applications

### Artistly

- Dashboard identifies Artistly v6.5 and links to its image design tools.
- The “Create Design” route offers Fast AI Image Designer and Advanced AI Image Designer.
- Artistly's dashboard links to VideoExpress as a separate tool for turning Artistly images into video.
- Use Artistly for the five Black Bloom stills/reference images. Image generation has not been tested and must be cost-checked in the account before any run.

### VideoExpress

- The signed-in editor exposes a “First Frame, Last Frame” generation mode.
- Its form has separate First Frame Prompt and Last Frame Smart Edit fields, and separate “First Frame from Library (beta)” and “Last Frame from Library (beta)” selectors. It also exposes Create First Image, Create Last Image, and Create Video actions. These actions were not run.
- The 16:9 landscape choice is present in this mode. The form recommends 9:16 for best quality and prompt adherence, so 16:9 pilot quality remains to be assessed.
- No duration control was visible in the First Frame, Last Frame form during this inspection. Thus, a 10-second clip in that specific mode is **not verified**.
- In the separate “Create Video From Prompt” mode, Advanced Mode exposes “Manual Video Length, sec” with a 3–10 second slider (initial value 5). This verifies a 10-second setting in that mode, but not its availability in First Frame, Last Frame mode.
- “Create Video” in the prompt-based mode was disabled until a still was created. The still-generation action was not run.

## Operational conclusion

The account UI confirms that first/last-frame controls and a 10-second duration setting exist, but it does **not** yet confirm that they work together in one video-generation run. Do not mark `videoexpress_10s` and `videoexpress_first_frame_reference` as jointly verified based on this inspection. Also verify actual rendered duration and endpoint behavior on an approved test before using the mode for the pilot.

## Prepared Black Bloom sequence

The existing prompt book remains authoritative for the five subjects and visual direction:

1. **BB-001 Iris:** start from its Artistly still; end at the soft violet droplet highlight on the left third.
2. **BB-002 Orchid:** begin by matching that violet highlight; end on the pale lilac highlight near upper center.
3. **BB-003 Rose:** begin on that glint; end on the defocused creamy crescent at right.
4. **BB-004 Calendula:** begin on the crescent; end on the small amber bokeh point lower center.
5. **BB-005 Dahlia:** begin on the amber point; end on the stable burgundy silhouette fading to black.

For each clip, preserve 16:9, black background, upper-left key/rim direction, restrained macro motion, and the prompt book's botanical realism constraints.

## Execution gates

1. Check the account's current cost/allowance for still creation, first/last image creation, and video rendering. Record all prices before generating.
2. Test whether the First Frame, Last Frame mode can produce 10 seconds and use both endpoint images in the same render. If not, use the separate 3–10 second mode only if it can accept the needed reference stills; otherwise revise the transition plan before spending.
3. For chaining, inspect the actual final frame of each completed clip and use it as the next clip's first-frame reference where supported. Keep a continuity card with source/output asset IDs and frame descriptions.
4. Price the five-scene pilot, including stills, frame assets, video renders, and one approved retry allowance. Set a hard credit cap and obtain explicit user GO.
5. Generate one clip at a time. Stop after each render for endpoint, duration, and visual QA. Continue only within the approved cap.
6. Assemble only after all five clips pass continuity QA. Measure final timeline length; the nominal 50 seconds assumes no overlap or trim.

## Public product references

- VideoExpress tutorials: https://videoexpress.ai/tutorials/index.html
- VideoExpress feature and plan page: https://videoexpress.ai/
- Artistly tutorials: https://artistly.ai/tutorials2/
- Artistly: https://artistly.ai/
