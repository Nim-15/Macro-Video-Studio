# Photorealistic Macro Prompt Guide

## Image prompt formula
[SUBJECT + species/material if known] + [plausible microtexture and droplets] + [environment] + [professional studio/natural lighting direction] + [lens magnification and shallow depth of field] + [palette and negative space] + [16:9 cinematic composition] + [photorealism constraints].

Example: “Extreme photorealistic macro photograph of a pale violet iris petal with fine veining and tiny realistic dew beads, emerging from seamless black velvet shadow; sculpted studio side light from upper left, delicate rim light, shallow focal plane crossing one droplet, tack-sharp surface microtexture, creamy optical bokeh, understated cinematic grading, negative space toward the right, 16:9, no lettering, no artificial geometry.”

## Video prompt formula
[REFERENCE IMAGE and scene ID] + [single plausible subject action] + [single deliberate camera movement] + [focus behavior] + [lighting continuity] + [10-second rhythm] + [precise first-frame alignment] + [precise exit-frame geometry].

Example: “Start on the supplied iris frame. Over ten seconds, move the macro camera forward at an almost imperceptible speed while a natural dew droplet refracts the rim light. Hold the petal's vein orientation and left-side key illumination. Slowly rack focus toward the central droplet only. End with the droplet occupying the right third, violet petal receding into black. No warping, floating droplets, text, or jump cuts.”

## In/out matched transition pair
Clip N exit: describe *exact* subject position, framing, focal plane, lighting, motion vector, palette and remaining negative space. Save the extracted last frame as a named asset if the editor supports it.

Clip N+1 entry: use that **actual** frame as reference when available, explicitly preserve geometry and exposure, and evolve via subtle focus shift, lighting reveal or tracked lateral move. If the tool lacks last-frame input support, mark the transition as an editor-side dissolve or match cut; do not claim seamless continuity.

## Quality checklist
- Subject structures are plausible and not duplicated.
- Droplets obey gravity/surface tension and move only with a plausible cause.
- No jittering, morphs or synthetic plastic texture.
- Focus moves slowly and intentionally.
- Camera and light directions match the adjacent shot.
- Ending shot state is documented and can be independently checked.
