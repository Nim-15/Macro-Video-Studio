# Credits, cost controls, and production gates

Never invent Artistly, VideoExpress or CloneVoice pricing. Inspect the actual signed-in account and note plan limits, per-image cost, per-clip cost, retries, batch concurrency, generation duration, and export costs before offering a budget.

## Estimate
- Base video renders = number of approved scenes.
- Image renders = number of scene references plus revised images.
- Gross credits = (video renders × measured video unit cost) + (image renders × measured image unit cost) + audio/assembly costs + approved retry reserve.
- Film output duration = sum of usable clips − overlaps − trims + inserted holds.
- 60 minutes = 3,600 seconds. 360 ten-second clips assumes zero overlaps and zero trims.

## Safety gates
1. Do an initial three-to-five-clip pilot and judge output before production scale.
2. Show estimated total and user-defined hard cap before paid actions; require explicit GO.
3. Check remaining credits before each verified batch.
4. Pause when cost, feature availability or output quality deviates from assumptions.
5. Separate *estimated* credit costs, *observed* charges, and *remaining* budget in run-state records.

## Production safety
Never start subscriptions, buy credits, delete historical assets, publish outputs or disclose private workspace data without explicit authorization.
