# Failure Rules

This document records failure patterns discovered during real underwater grading tests.

A failure rule is more valuable than a generic styling preference because it prevents repeated mistakes.

---

## FAIL-001 — AI Adds New Fish

### Symptom

New fish appear that were not present in the original image.

### Severity

Critical failure.

### Cause

Generative editing is used too aggressively in fish regions.

### Rule

Never generate new fish.

Fish count must remain consistent with the original image.

### Correction

Reject the result.

Reprocess using:

- exposure
- tone
- local contrast
- restrained clarity

Do not use generative reconstruction for fish recovery.

---

## FAIL-002 — Fish Direction Changes

### Symptom

Fish orientation or swimming direction changes after editing.

### Severity

Critical failure.

### Rule

Original fish direction must remain unchanged.

### Correction

Reject any edit that changes fish orientation.

Use non-generative local correction only.

---

## FAIL-003 — Fish Geometry Becomes Distorted

### Symptom

Fish bodies become malformed, blurred, duplicated or anatomically incorrect.

### Severity

Critical failure.

### Cause

Semantic enhancement attempts to reconstruct distant or low-detail fish.

### Rule

Do not invent fish structure.

### Correction

Prefer:

- lower enhancement strength
- local exposure
- micro-contrast
- weaker sharpening

If the fish cannot be restored credibly, preserve the original soft structure.

---

## FAIL-004 — Person Skin Remains Cyan

### Symptom

The body or face still has strong cyan / blue contamination after grading.

### Cause

Skin and water share the same correction.

### Rule

Skin should be treated separately from water whenever practical.

### Correction

Create a dedicated skin adjustment.

Restore skin color conservatively.

Do not globally warm the entire image.

---

## FAIL-005 — Skin Becomes Orange or Red

### Symptom

Skin looks unnaturally warm after red-channel recovery.

### Cause

Warm-color restoration is too aggressive.

### Rule

Underwater skin should remain believable and slightly cooler than normal land photography when appropriate.

### Correction

Reduce:

- orange
- red
- yellow
- magenta contamination

Credibility is more important than warmth.

---

## FAIL-006 — Person Is Bright but Background Becomes Fake

### Symptom

The person becomes visible, but the entire image becomes too bright or flat.

### Cause

Global exposure is used to fix a local subject problem.

### Rule

Do not brighten the full image just to save the subject.

### Correction

Use local subject exposure.

Preserve background depth.

---

## FAIL-007 — Artificial Halo Around Person

### Symptom

A bright or pale outline appears around the person after local enhancement.

### Cause

Mask edge is too hard or local exposure is too strong.

### Rule

Local correction must blend naturally.

### Correction

Refine mask edge.

Reduce local lift.

Avoid visible separation artifacts.

---

## FAIL-008 — Top Water Turns Into a Dark Blue Ceiling

### Symptom

The upper water region becomes unnaturally dark, flat or disconnected from the rest of the frame.

### Cause

Top-water haze correction is too aggressive.

### Rule

The upper region is still water, not a separate sky.

### Correction

Preserve:

- surface brightness
- natural transition
- water depth

Reduce dehaze or blue density.

---

## FAIL-009 — Top Water Stays Gray and Milky

### Symptom

The upper water area remains foggy, gray or low-contrast.

### Rule

Top-water haze requires separate review.

### Correction

Use restrained:

- dehaze
- contrast
- color cleanup

Do not eliminate all haze.

---

## FAIL-010 — Water Becomes Excessively Blue

### Symptom

The image looks like a strong blue filter has been applied.

### Cause

Blue saturation is used as the primary grading strategy.

### Rule

Underwater grading does not mean adding blue.

### Correction

First remove:

- dirty cyan
- green contamination
- gray haze

Then preserve only credible blue water color.

---

## FAIL-011 — Water Becomes Too Transparent

### Symptom

The scene loses underwater depth and begins to look like air.

### Cause

Dehaze and clarity are overused.

### Rule

Underwater images must retain atmospheric depth.

### Correction

Restore some:

- haze
- distance softness
- tonal falloff

Clear water is not the same as haze-free water.

---

## FAIL-012 — Midtones Remain Muddy

### Symptom

The image is technically brighter but still feels dull and heavy.

### Cause

Exposure is increased without improving midtone separation.

### Rule

Many underwater images are not primarily too dark.

They are too compressed in the midtones.

### Correction

Improve:

- local midtone contrast
- subject/background separation
- tonal hierarchy

Do not simply lift shadows.

---

## FAIL-013 — Fish School Is Still Too Dark

### Symptom

The person is corrected successfully but the fish school remains unreadable.

### Rule

In person + fish scenes, fish may be a secondary or co-primary subject.

### Correction

Evaluate fish separately.

Use:

- local exposure
- tonal separation
- restrained micro-contrast

Do not globally brighten the water.

---

## FAIL-014 — Person and Fish Are Brightened Equally

### Symptom

The image loses depth because person and fish occupy the same tonal layer.

### Rule

Person + fish scenes require layered treatment.

### Correction

Separate:

- person
- near fish
- mid fish
- distant fish

Near elements may be clearer than distant ones.

---

## FAIL-015 — Artificial Light Looks AI-Generated

### Symptom

Light appears too wide, too smooth, too strong or inconsistent with the original scene.

### Cause

A new light source is effectively invented.

### Rule

Do not invent lighting.

Respect original direction and intensity.

### Correction

Use existing light information only.

Deep-water lighting should remain limited and directional.

---

## FAIL-016 — Deep Water Becomes Shallow-Looking

### Symptom

A deep scene looks like tropical shallow water after grading.

### Cause

Over-brightening, excessive blue cleanup or unrealistic warm recovery.

### Rule

Depth must remain believable.

### Correction

Retain:

- darker water
- limited visibility
- stronger falloff
- restrained color recovery

Darker but clearer is preferable to brighter but fake.

---

## FAIL-017 — Coral Becomes Artificially Orange or Yellow

### Symptom

Reef or coral colors look like an aquarium filter.

### Cause

Warm-color recovery exceeds source information.

### Rule

Only recover warm colors when credible information exists.

### Correction

Reduce saturation and warm shift.

Keep pale coral from becoming uniformly yellow.

---

## FAIL-018 — Pale Objects Are Tinted Yellow

### Symptom

White or pale coral, equipment or sand becomes yellow after warm recovery.

### Rule

Warm recovery must not contaminate neutral areas.

### Correction

Protect pale and neutral regions separately.

---

## FAIL-019 — Over-Sharpening

### Symptom

Fish, water particles, skin or distant scenery appear crunchy or artificial.

### Cause

Sharpening is applied globally.

### Rule

Sharpness should follow depth.

### Correction

Prioritize:

- subject
- foreground
- important structure

Keep distant water and fish softer.

---

## FAIL-020 — Noise Explodes After Brightening

### Symptom

Blue, green or chroma noise becomes obvious in shadow regions.

### Cause

Dark regions are lifted before noise control.

### Rule

Noise risk must be considered before aggressive exposure recovery.

### Correction

Reduce noise first.

Then apply restrained local sharpening.

---

## FAIL-021 — AI Repairs Hands or Face Incorrectly

### Symptom

Hands, fingers, face or anatomy change after editing.

### Severity

Critical failure.

### Rule

Human anatomy must remain unchanged.

### Correction

Reject the generative edit.

Use conservative local tonal correction instead.

---

## FAIL-022 — Composition Changes

### Symptom

The image is cropped, expanded or rearranged unintentionally.

### Severity

Critical failure.

### Rule

Color grading must preserve the original composition unless the user explicitly requests otherwise.

### Correction

Reject the result.

---

## FAIL-023 — Existing Light Direction Changes

### Symptom

The edited image suggests a different primary light direction.

### Rule

Original light logic must be preserved.

### Correction

Remove invented or contradictory lighting.

---

## FAIL-024 — Hero Mode Becomes a Filter

### Symptom

Hero mode looks like:

- stronger blue
- stronger contrast
- stronger saturation
- stronger sharpening

without better visual hierarchy.

### Rule

Hero means stronger focus, not stronger effects.

### Correction

Return to Natural.

Then selectively improve:

- subject hierarchy
- depth
- midtone clarity
- local separation

---

## FAIL-025 — Good Shallow-Water Source Is Over-Processed

### Symptom

A naturally good shallow-water image becomes worse after unnecessary editing.

### Rule

High-quality source images require less intervention.

### Correction

Use lighter grading.

Preserve original natural light and color.

---

## Failure Severity Levels

### Level 1 — Critical

Reject the result.

Examples:

- new fish
- changed fish direction
- changed anatomy
- changed composition
- fabricated marine life
- major geometry change

### Level 2 — Major

Reprocess the affected region.

Examples:

- severe skin-color error
- unrealistic water color
- artificial light
- over-dehazing
- subject still unreadable

### Level 3 — Minor

Local correction is sufficient.

Examples:

- slight top haze
- slightly muddy midtones
- minor color contamination
- weak subject separation

---

## Failure Review Procedure

When a failure occurs:

1. identify the exact failed region
2. classify the failure type
3. determine severity
4. preserve all regions that already passed
5. repair only the failed area when possible
6. run QC again
7. record the failure pattern if it is new
8. update the long-term rule library only when the pattern is repeatable
