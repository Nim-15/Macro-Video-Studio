# Photorealistic Macro Prompt Guide

## Image prompt formula
[SUBJECT + species/material if known] + [plausible microtexture and droplets] + [environment] + [professional studio/natural lighting direction] + [lens magnification and shallow depth of field] + [palette and negative space] + [16:9 cinematic composition] + [photorealism constraints].

Example: “Extreme photorealistic macro photograph of a pale violet iris petal with fine veining and tiny realistic dew beads, emerging from seamless black velvet shadow; sculpted studio side light from upper left, delicate rim light, shallow focal plane crossing one droplet, tack-sharp surface microtexture, creamy optical bokeh, understated cinematic grading, negative space toward the right, 16:9, no lettering, no artificial geometry.”

## Video prompt formula
[REFERENCE IMAGE + SUBJECT LOCK] + [visible entry effect in first 0–2 seconds] + [stable macro action and camera movement in 2–7 seconds] + [optional gradual color/subject reveal through a realistic optical/light effect] + [visible exit effect in final 7–10 seconds] + [paired cue for next clip] + [negative constraints].

Every effect must fit inside the requested clip duration. For a 10-second shot, the default rhythm is:
- 0–2s: transition-in effect.
- 2–7s: stable macro observation; optional gradual color or subject reveal.
- 7–10s: transition-out effect that prepares the next entry cue.

## Subject lock and realistic changes
Explicitly preserve the principal subject's species/material, silhouette, anatomy, proportions, texture, and position. Limit it to plausible natural motion (for example, a subtle petal tremor or a droplet refracting light). Do not deform, stretch, duplicate, melt, or morph the subject. A new species or color may emerge through a gradual rack focus, moving light, realistic refraction/caustics, soft optical bokeh, or a plausible shadow/occlusion. Show the new subject as a separate object; do not turn the old subject into it.

## In-clip transition effects
Choose restrained effects grounded in professional macro photography:
- A controlled rim-light or exposure sweep that slowly reveals the surface.
- A slow rack focus with stable geometry and lens behavior.
- Optical bokeh or lens bloom that grows or resolves gently.
- Realistic refracted highlights or caustic light through water/petal tissue.
- A gradual shift in white balance or rim-light color.
- A soft foreground shadow or out-of-focus highlight passing across frame.

The effect must begin at the clip opening or finish at its ending, remain photorealistic, and visually pair with the adjacent clip. Avoid hard cuts, black slates, abrupt flashes, glitch effects, or added editor transitions.

## Copy-ready prompt skeleton
“Animate the supplied reference image. Preserve the principal [subject/species] exactly: stable silhouette, anatomy, proportions, texture, and position; no morphing, deformation, duplication, or replacement. In 0–2 seconds, use a gradual [specific realistic light/optical effect] as the visible entry transition, matching [incoming shape/color/highlight] while the subject remains stable. In 2–7 seconds, hold a legible macro view with [one plausible action] and [one slow camera move]; [optional gradual color or separate-subject reveal using a physically plausible optical/light effect]. In 7–10 seconds, use a gradual [specific effect] as the visible exit transition, ending on [precise framing, palette, focus, and light cue] that matches the next clip's entry. Keep professional macro optics, realistic texture and stable exposure. All transitions stay inside this 10-second clip; place adjacent clips directly together with no added editor-side transition.”

## Quality checklist
- Each clip visibly begins and ends with its own transition effect.
- The main subject remains recognizable and stable throughout.
- Any subject/color change is gradual, physically plausible, and never a morph.
- Entry and exit effects pair across the boundary without an editor-side transition.
- Effects do not add time beyond the generated clip.
- Droplets obey gravity/surface tension and move only with a plausible cause.
- No jitter, flicker, artificial plastic texture, camera jump, or duplicate anatomy.
- Focus and camera movement stay slow and intentional.
- The actual final frame is saved and checked against the next entry cue.