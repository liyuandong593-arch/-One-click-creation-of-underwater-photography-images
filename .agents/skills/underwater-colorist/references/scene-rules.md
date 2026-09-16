# Underwater Scene Rules

This document defines scene-specific grading rules learned from real underwater image tests.

General principle:

Preserve content first.  
Improve readability second.  
Apply style last.

---

## 1. Underwater Person

### Goal

Make the person the primary visual subject while preserving a believable underwater environment.

### Common Problems

- face too dark
- skin contaminated by cyan or blue
- body merges into background
- diving equipment lacks detail
- entire image is brightened just to save the person
- artificial halo around the body

### Recommended Treatment

- adjust person exposure locally
- protect face and skin separately
- restore skin tone conservatively
- improve midtone separation
- keep background slightly less prominent
- preserve natural water depth

### Do Not

- modify face shape
- modify hands or fingers
- modify body geometry
- replace equipment
- create artificial rim lighting
- make skin look like land photography

### QC

The person should be readable immediately without looking artificially pasted onto the background.

---

## 2. Person + Fish School

### Goal

Treat the person and important fish school as dual subjects.

### Common Problems

- person becomes visible but fish remain black
- fish are brightened uniformly and lose depth
- AI changes fish direction
- AI invents new fish
- fish geometry becomes distorted
- person and fish merge into the same tonal layer

### Recommended Treatment

1. establish person readability
2. recover important fish visibility
3. separate near, middle and distant fish
4. use exposure and micro-contrast before generative enhancement
5. preserve original fish direction and density

Near fish may be clearer.

Distant fish should remain softer and more integrated with the water.

### Hard Rules

Never generate additional fish.

Never change fish direction.

Never intentionally change fish count.

### Failure Strategy

If distant fish are damaged by AI enhancement:

- revert the enhancement
- reduce the local correction
- if an already-corrupted generated region cannot be restored, prefer clean water over inventing replacement fish

---

## 3. Person + Large Marine Animal

Examples:

- whale shark
- shark
- turtle
- ray

### Goal

Preserve the scale and relationship between the person and the animal.

### Priorities

- animal body geometry
- animal volume
- original distance
- original orientation
- person readability
- believable water depth

### Recommended Treatment

Enhance:

- silhouette readability
- body volume
- local exposure
- restrained texture visibility

### Do Not

- redraw body structure
- invent texture
- reshape fins
- change animal size
- move the animal
- change person-to-animal distance

The final result should feel like a better photograph of the same moment.

---

## 4. Coral / Reef

### Goal

Create separation between cool water and warmer reef elements without producing artificial aquarium colors.

### Common Problems

- reef remains muddy
- entire frame is blue
- warm recovery becomes orange or yellow
- pale objects become uniformly yellow
- water and coral lose separation

### Recommended Treatment

- clean cyan / green contamination from the water
- preserve cool water
- recover warm brown, orange or red reef colors only when credible source information exists
- increase local separation instead of global saturation
- protect pale coral from yellow contamination

### Important Preference

Transparent water is preferred over heavily saturated blue water.

Coral should be visible and attractive, but still believable.

---

## 5. Pure Underwater Environment

Includes:

- open water
- underwater terrain
- wreck
- cave
- underwater structure

### Goal

Create spatial depth, clarity and atmosphere without relying on a human subject.

### Priorities

- foreground / midground / background separation
- structure readability
- water clarity
- directional light
- believable haze

### Recommended Treatment

- reduce dirty cyan or green contamination
- open muddy midtones
- preserve atmospheric perspective
- keep distant areas softer
- enhance structural contrast locally

### Do Not

- fabricate architecture
- add objects
- add marine life
- remove all haze
- sharpen the entire scene uniformly

---

## 6. Shallow Natural-Light Scene

### Typical Characteristics

- strong natural light
- better retained color
- clearer water
- higher success rate

### Goal

Preserve the original light advantage while cleaning the image.

### Recommended Treatment

- retain natural surface highlights
- reduce gray haze carefully
- improve midtone clarity
- recover subject readability with light local corrections
- avoid aggressive stylization

### Common Failure

Over-processing a good source image and making it worse.

For shallow scenes, less correction is often better.

---

## 7. Deep-Water / Low-Light Scene

### Goal

Preserve the feeling of depth while making important subjects readable.

### Key Principle

Darker but clearer is usually better than brighter but unrealistic.

### Common Problems

- subject becomes completely black
- global exposure destroys deep-water atmosphere
- fake sunlight appears
- artificial beam looks AI-generated
- noise becomes obvious after brightening

### Recommended Treatment

- lift the primary subject locally
- open midtones selectively
- retain strong dark-water atmosphere
- reduce noise before sharpening
- respect existing light direction

### Do Not

- turn deep water into shallow tropical water
- create strong sunlight where none exists
- fabricate dramatic volumetric beams

---

## 8. Artificial-Light / Dive-Light Scene

### Goal

Preserve realistic artificial-light behavior.

### Important Rules

Light must follow the original source direction.

Brightness should decay naturally with distance.

### Avoid

- huge flat white light patches
- fake cinematic beam
- lighting subjects that were not illuminated originally
- inconsistent light direction

At greater depth, artificial light should feel directional and limited rather than globally illuminating the scene.

---

## 9. Top-Water Region

The upper part of underwater images is a recurring high-risk area.

### Common Problems

- gray haze
- milky water
- cyan / green contamination
- clipped highlights
- unnatural dark-blue ceiling
- visible transition between upper and lower water

### Recommended Treatment

- reduce dirty haze
- preserve surface brightness
- improve blue-water density carefully
- maintain smooth transition to mid-water

### Rule

Do not treat the upper water region as a separate artificial sky.

---

## 10. Midtone Rule

A recurring project finding:

Many underwater images are not primarily too dark.

They are too muddy in the midtones.

Before aggressively lifting shadows:

- inspect midtone separation
- inspect subject/background separation
- inspect local contrast

Improving midtones often produces more natural clarity than globally increasing exposure.

---

## 11. Water Color Rule

Never assume:

underwater = more blue

First determine whether the source contains:

- natural blue water
- cyan contamination
- green contamination
- gray haze
- excessive blue saturation

The target is clean and believable water, not maximum blue saturation.

---

## 12. Fish High-Risk Rule

Fish schools are one of the most fragile AI-editing regions.

Preferred correction order:

1. exposure
2. tone
3. micro-contrast
4. restrained clarity
5. only then consider semantic enhancement

If semantic enhancement changes fish structure, reject it.

---

## 13. Person Skin Rule

Person skin should be processed independently from the water whenever practical.

Avoid shared color correction that causes:

- cyan skin
- green skin
- orange skin
- magenta skin

Skin should remain believable within an underwater context.

---

## 14. Hero Scene Rule

Hero mode is not a separate reality.

Start from a credible Natural correction.

Then strengthen:

- primary subject hierarchy
- depth
- local contrast
- midtone readability
- selective color separation

Do not achieve Hero mode by:

- adding blue
- adding saturation
- adding sharpening
- adding fake light

Hero means stronger visual focus.
