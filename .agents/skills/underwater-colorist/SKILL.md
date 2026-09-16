---
name: underwater-colorist
description: A reusable underwater color-grading workflow for Natural and Hero styles. Use it to analyze underwater photos, preserve original content, improve water clarity, restore credible colors, enhance subject readability, protect skin tones and marine life, and run grading QC.
---

# Underwater Colorist

## Purpose

This skill provides a repeatable workflow for underwater photo color grading.

Its goal is to improve underwater images while preserving the original photographic content.

The skill prioritizes:

1. Content preservation
2. Subject readability
3. Water clarity
4. Depth separation
5. Credible color recovery
6. Natural or Hero-style grading

## Core principle

Color grading is not image reconstruction.

Never change the original scene unless the user explicitly requests content editing.

## Hard constraints

Never:

- change composition
- crop important subjects without permission
- expand the image
- add fish
- add coral
- add marine animals
- add bubbles
- invent light sources
- change fish direction
- change fish count
- change human anatomy
- change facial structure
- change diving equipment
- replace scenery
- fabricate textures
- turn deep water into unrealistic shallow water
- create fake cinematic lighting

If a requested correction risks changing scene content, prefer a conservative adjustment.

## Supported scene categories

Classify the image before grading.

Possible categories:

- underwater person
- person + fish school
- person + large marine animal
- coral / reef
- underwater environment
- wreck / structure
- shallow natural-light scene
- deep-water / low-light scene
- artificial-light scene

## Grading modes

### Natural

Natural mode aims for:

- realistic water color
- clean white balance
- natural contrast
- restrained color recovery
- credible skin tone
- preserved underwater atmosphere
- minimal stylization

Natural mode should look like a well-exposed, professionally corrected underwater photograph.

### Hero

Hero mode builds on Natural mode.

Hero may increase:

- subject separation
- midtone clarity
- local contrast
- visual focus
- depth
- cinematic light shaping

Hero must not become:

- oversaturated
- excessively blue
- artificially bright
- fake HDR
- AI-looking
- visually reconstructed

Hero means stronger visual hierarchy, not stronger effects.

## Workflow

### Step 1 — Analyze

Before editing, inspect:

- scene category
- dominant water cast
- cyan / green / blue contamination
- exposure
- subject visibility
- top-water haze
- midtone compression
- highlight clipping
- shadow detail
- warm-color loss
- fish visibility
- skin-tone contamination
- noise risk
- AI-sensitive regions

### Step 2 — Identify the primary subject

Possible primary subjects include:

- person
- fish school
- large marine animal
- coral
- wreck
- underwater structure
- environment

The primary subject must remain readable after grading.

Background improvement must never reduce primary-subject clarity.

### Step 3 — Decide the grading mode

Use Natural by default for conservative correction.

Use Hero when the user requests:

- stronger cinematic presentation
- clearer subject hierarchy
- more visual impact
- stronger depth separation

Hero should still preserve realism.

### Step 4 — Correct globally first

Prefer safe global corrections before semantic or generative edits.

Typical corrections:

- white balance
- exposure
- tone curve
- black point
- highlight recovery
- restrained dehaze
- HSL correction
- local contrast
- noise reduction
- sharpening
- red-channel recovery when credible

Do not globally increase blue saturation as a shortcut.

### Step 5 — Correct subjects locally

Apply local corrections only where needed.

Possible local targets:

- face
- skin
- body
- diving equipment
- fish school
- large marine animal
- coral
- top-water region
- midground
- artificial-light region

Avoid visible halos around masks.

### Step 6 — Protect water depth

Water should feel clear, not empty.

Preserve:

- foreground / midground / background separation
- natural underwater haze
- believable depth
- realistic falloff

Do not remove all haze.

Do not make distant water sharper than foreground subjects.

### Step 7 — Protect skin tone

For people:

- correct cyan / green contamination locally
- restore credible skin color
- keep skin slightly cooler than typical land photography when appropriate
- avoid orange, red, yellow, magenta or gray skin
- avoid plastic texture

Do not brighten the entire image just to fix the person.

### Step 8 — Protect fish and marine life

Fish and marine animals are high-risk regions for AI distortion.

Never:

- generate extra fish
- modify fish direction
- reshape bodies
- invent scales or textures
- change relative positions

For distant fish, prefer:

- exposure correction
- micro-contrast
- restrained clarity

If AI enhancement damages fish structure, revert or weaken the enhancement.

### Step 9 — Review top-water haze

The upper water region often needs separate review.

Check for:

- gray haze
- cyan contamination
- white clipping
- unnatural dark-blue ceiling effect
- visible color discontinuity

Reduce haze carefully while preserving natural light transition.

### Step 10 — Run QC

Before finalizing, verify:

#### Content preservation
- composition unchanged
- subjects unchanged
- no new objects
- no missing objects
- no anatomy changes
- no fish-count changes
- no fish-direction changes

#### Water
- no dirty green cast
- no excessive blue saturation
- no over-dehazing
- believable depth remains
- top-water transition is natural

#### Person
- face readable
- skin credible
- no cyan body contamination
- no halos
- no anatomy changes

#### Fish / marine animals
- visible when important
- natural depth separation
- no invented details
- no geometry changes

#### Tone
- no crushed blacks
- no blown highlights
- midtones are not muddy
- primary subject stands out

#### Texture
- no excessive sharpening
- no plastic surfaces
- no obvious AI artifacts

## Scene-specific guidance

### Underwater person

Priority:

1. face readability
2. skin tone
3. body exposure
4. equipment visibility
5. water clarity

Do not brighten the background more than necessary.

### Person + fish school

Treat person and fish school as dual subjects.

Requirements:

- person remains readable
- important fish remain visible
- near fish can be clearer than distant fish
- preserve original fish direction
- preserve original fish count

Do not apply generative fish enhancement.

### Person + large marine animal

Protect:

- animal body geometry
- scale
- distance
- texture
- relative position to person

Enhance volume and readability, not anatomy.

### Coral / reef

Separate cool water from warm reef elements.

Recover warm coral colors only when the source still contains credible information.

Do not turn deep-water coral into an artificial aquarium palette.

### Underwater environment / wreck

Prioritize:

- depth
- structure
- directional light
- atmosphere
- spatial readability

Do not fabricate architecture or scenery.

### Shallow natural-light scene

Preserve natural surface light.

Avoid:

- blown surface highlights
- excessive dehaze
- over-brightening lower regions

These scenes usually require lighter correction.

### Deep-water / artificial-light scene

Preserve darkness and depth.

Prefer:

- darker but clearer
over:
- brighter but unrealistic

Do not invent strong sun rays or fake light beams.

Respect the original light direction.

## Failure handling

If a result fails QC:

1. Identify the failed region.
2. Preserve all regions that already passed.
3. Correct only the failed region.
4. Re-run QC.
5. Do not restart the entire image unless necessary.

## Learning loop

After each batch of images, produce three notes:

### New successful rule

What method clearly worked?

### New failure rule

What situation repeatedly caused failure?

### Rule revision

How should similar scenes be handled next time?

Only stable, repeatable findings should be added to the long-term rule library.

## Final output

For each completed image, report:

- scene category
- grading mode
- main problems detected
- main corrections applied
- preserved-content checks
- QC result
- remaining warnings
- new successful rule, if any
- new failure rule, if any
- proposed rule revision, if any
