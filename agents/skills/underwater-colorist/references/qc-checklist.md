# Underwater Grading QC Checklist

This checklist defines the final quality-control process for underwater image grading.

A result must not be approved only because it “looks better.”

The image must pass content preservation, subject readability, water quality, tonal structure, color credibility and artifact checks.

---

## 1. QC Principle

Approval priority:

1. Content preservation
2. Subject integrity
3. Water realism
4. Tonal readability
5. Color credibility
6. Texture quality
7. Style quality

If a lower-priority goal conflicts with a higher-priority goal, the higher-priority goal wins.

---

# 2. Critical Content Preservation Check

Any failure in this section means:

**REJECT THE RESULT**

Check:

- [ ] composition unchanged
- [ ] image boundaries unchanged unless explicitly requested
- [ ] no unintended crop
- [ ] no unintended expansion
- [ ] no new fish
- [ ] no missing fish
- [ ] fish direction unchanged
- [ ] fish count preserved
- [ ] marine-animal geometry unchanged
- [ ] no invented coral
- [ ] no invented marine life
- [ ] no invented bubbles
- [ ] no invented scenery
- [ ] no new architecture or structure
- [ ] no new light source
- [ ] human face unchanged
- [ ] human body geometry unchanged
- [ ] hands and fingers unchanged
- [ ] diving equipment unchanged

If any item fails:

QC Status = CRITICAL FAILURE

---

# 3. Primary Subject Check

Identify the primary subject first.

Possible subjects:

- person
- person + fish
- large marine animal
- coral / reef
- wreck
- underwater structure
- environment

Check:

- [ ] primary subject is immediately readable
- [ ] subject is not lost in the background
- [ ] subject exposure is sufficient
- [ ] subject midtones are readable
- [ ] subject detail remains credible
- [ ] subject is not over-brightened
- [ ] subject does not look artificially pasted into the image
- [ ] no visible local-adjustment halo

If the subject remains unreadable:

QC Status = MAJOR FAILURE

---

# 4. Person Check

Use when people are present.

## Face

- [ ] face remains structurally unchanged
- [ ] face is readable
- [ ] face is not over-smoothed
- [ ] face does not contain AI reconstruction artifacts
- [ ] skin does not appear cyan
- [ ] skin does not appear green
- [ ] skin does not appear orange
- [ ] skin does not appear red
- [ ] skin does not appear magenta
- [ ] skin retains natural texture

## Body

- [ ] body geometry unchanged
- [ ] hands and fingers unchanged
- [ ] skin tone consistent with face
- [ ] body is not excessively blue or cyan
- [ ] body exposure is appropriate
- [ ] no artificial glow around limbs

## Equipment

- [ ] mask unchanged
- [ ] regulator unchanged
- [ ] tank unchanged
- [ ] fins unchanged
- [ ] clothing unchanged
- [ ] logos/text are preserved unless removal was explicitly requested

---

# 5. Fish School Check

Use whenever fish are visually meaningful.

- [ ] no new fish
- [ ] no missing important fish
- [ ] fish direction unchanged
- [ ] fish body geometry preserved
- [ ] no duplicated fish
- [ ] no merged fish
- [ ] no AI-generated fish texture
- [ ] important fish remain visible
- [ ] near fish are not softer than distant fish without reason
- [ ] distant fish retain realistic softness
- [ ] fish school maintains natural depth layering

For person + fish scenes:

- [ ] person is readable
- [ ] fish school is readable
- [ ] person and fish are not flattened into the same tonal layer

---

# 6. Large Marine Animal Check

Use for whale shark, shark, turtle, ray and other large animals.

- [ ] body geometry unchanged
- [ ] fins / tail / shell unchanged
- [ ] original orientation preserved
- [ ] original scale preserved
- [ ] original relative position preserved
- [ ] person-to-animal distance preserved
- [ ] no invented texture
- [ ] body volume remains believable
- [ ] animal is readable without looking reconstructed

---

# 7. Water Color Check

Check:

- [ ] water no longer contains distracting dirty green contamination
- [ ] cyan contamination is controlled
- [ ] blue saturation is believable
- [ ] water does not look like a global blue filter
- [ ] water does not look like swimming-pool blue
- [ ] deep water still feels deep
- [ ] shallow water still feels shallow
- [ ] water remains visually transparent where appropriate
- [ ] color transitions are smooth
- [ ] no strong color banding or regional mismatch

Key question:

Does the water look cleaner, or merely bluer?

If merely bluer:

QC Status = FAIL

---

# 8. Water Transparency and Haze Check

- [ ] dirty gray haze reduced where necessary
- [ ] natural underwater haze preserved
- [ ] distant objects remain softer than near objects
- [ ] water does not look like air
- [ ] dehaze is not excessive
- [ ] visibility feels believable for the scene
- [ ] depth falloff remains natural

Key rule:

Clear water is not haze-free water.

---

# 9. Top-Water Region Check

The upper water region must be reviewed separately.

Check:

- [ ] no milky gray haze
- [ ] no dirty cyan/green contamination
- [ ] no clipped white surface region
- [ ] no unnatural dark-blue ceiling
- [ ] no obvious tonal break between upper and lower water
- [ ] surface brightness remains believable
- [ ] light transition remains smooth
- [ ] no fake sky effect

---

# 10. Midtone Check

Midtones are one of the most important QC areas.

Check:

- [ ] image no longer feels muddy
- [ ] primary subject separates from background
- [ ] fish visibility is sufficient
- [ ] reef structure is readable
- [ ] mid-water region is not flat
- [ ] midtones are not excessively lifted
- [ ] image retains underwater depth

If the image is brighter but still muddy:

QC Status = FAIL

---

# 11. Shadow Check

- [ ] important subjects are not crushed
- [ ] dark areas retain useful information where needed
- [ ] blacks are not lifted into gray unnecessarily
- [ ] shadows support scene depth
- [ ] deep-water scenes remain appropriately dark

Dark is acceptable.

Dead black on important subjects is not.

---

# 12. Highlight Check

Check:

- [ ] surface highlights retain transition
- [ ] bubbles retain texture
- [ ] white equipment retains detail
- [ ] fish reflections are not clipped unnaturally
- [ ] artificial-light hotspots remain believable
- [ ] highlights are not used as fake dramatic effects

---

# 13. Color Recovery Check

Check:

- [ ] warm color recovery is credible
- [ ] no excessive red recovery
- [ ] no excessive orange recovery
- [ ] no excessive yellow contamination
- [ ] neutral objects remain neutral enough
- [ ] coral colors remain believable
- [ ] skin color remains believable

Key principle:

Credibility is more important than color richness.

---

# 14. Coral / Reef Check

- [ ] reef separates from water
- [ ] coral is readable
- [ ] warm colors are restrained
- [ ] pale coral is not uniformly yellow
- [ ] reef does not look like an aquarium filter
- [ ] no invented coral detail
- [ ] no invented coral structure

---

# 15. Artificial Light Check

Use for dive-light or deep-water scenes.

- [ ] original light direction preserved
- [ ] light source remains believable
- [ ] brightness decays naturally with distance
- [ ] no huge flat white region
- [ ] no fake cinematic beam
- [ ] no invented sun ray
- [ ] objects outside the original light path are not artificially illuminated
- [ ] scene darkness is preserved where appropriate

---

# 16. Sharpness Check

- [ ] primary subject has sufficient detail
- [ ] face is not over-sharpened
- [ ] skin is not crunchy
- [ ] fish edges remain natural
- [ ] water particles are not exaggerated
- [ ] distant fish remain softer
- [ ] distant water remains softer
- [ ] entire frame is not sharpened uniformly

Sharpness should follow depth.

---

# 17. Noise Check

- [ ] shadow noise is controlled
- [ ] chroma noise is not obvious
- [ ] blue/green noise is not amplified
- [ ] noise reduction has not destroyed important texture
- [ ] sharpening has not re-amplified noise

Preferred sequence:

Noise reduction → tonal correction → restrained sharpening.

---

# 18. Natural Mode Check

When using Natural mode, confirm:

- [ ] image feels clean
- [ ] image feels believable
- [ ] water remains natural
- [ ] color recovery is restrained
- [ ] subject readability improved
- [ ] original atmosphere remains recognizable
- [ ] processing is not visually obvious

Natural should feel invisible.

---

# 19. Hero Mode Check

When using Hero mode, confirm:

- [ ] Natural baseline remains believable
- [ ] primary subject hierarchy is stronger
- [ ] midtone structure is improved
- [ ] depth is stronger
- [ ] local contrast is intentional
- [ ] image is not merely more blue
- [ ] image is not merely more saturated
- [ ] image is not merely more sharpened
- [ ] lighting remains realistic
- [ ] image does not look synthetic

Hero should feel intentional, not artificial.

---

# 20. Scene-Specific Pass Check

## Underwater Person

Pass if:

- person is readable
- skin is credible
- background remains believable
- no anatomy change
- no local halo

## Person + Fish

Pass if:

- person readable
- important fish readable
- fish direction preserved
- fish count preserved
- depth hierarchy exists

## Large Marine Animal

Pass if:

- geometry preserved
- scale preserved
- relationship with person preserved
- volume improved credibly

## Coral / Reef

Pass if:

- water is cleaner
- reef separates from water
- warm recovery remains believable
- no artificial aquarium look

## Environment / Wreck

Pass if:

- structure readable
- spatial depth preserved
- haze controlled
- no invented scenery

## Shallow Natural Light

Pass if:

- original good light preserved
- image is not over-processed
- surface highlights remain natural

## Deep Water

Pass if:

- subject readable
- darkness preserved
- no fake shallow-water appearance
- no fake light beam

---

# 21. Severity Classification

## Level 1 — Critical Failure

Reject immediately.

Examples:

- new fish
- fish direction changed
- anatomy changed
- composition changed
- new marine life
- fabricated scenery
- major geometry change

Result status:

REJECTED

---

## Level 2 — Major Failure

Affected region must be reprocessed.

Examples:

- severe skin-color error
- subject still unreadable
- fake lighting
- excessive blue
- excessive dehaze
- fish school still too dark

Result status:

REVISION REQUIRED

---

## Level 3 — Minor Warning

Local correction may be sufficient.

Examples:

- slight top haze
- slight midtone muddiness
- small color contamination
- minor sharpening issue

Result status:

PASS WITH WARNINGS

---

# 22. Final QC Status

Use one of the following:

## PASSED

All critical and major checks pass.

## PASSED WITH WARNINGS

No critical or major failure exists, but minor issues remain.

## REVISION REQUIRED

One or more major failures remain.

## REJECTED

Any critical content-preservation failure exists.

---

# 23. Final QC Report Template

For each completed image, report:

Scene:
Mode:

Primary subject:

Detected problems:
- 
- 
- 

Corrections applied:
- 
- 
- 

Content preservation:
- PASS / FAIL

Subject readability:
- PASS / FAIL

Water color:
- PASS / FAIL

Water transparency:
- PASS / FAIL

Skin:
- PASS / FAIL / N/A

Fish:
- PASS / FAIL / N/A

Lighting:
- PASS / FAIL

Tone:
- PASS / FAIL

Texture:
- PASS / FAIL

AI artifact check:
- PASS / FAIL

Final status:
PASSED / PASSED WITH WARNINGS / REVISION REQUIRED / REJECTED

Remaining warnings:
- 
- 

New successful rule:
- 

New failure rule:
- 

Proposed rule revision:
- 
