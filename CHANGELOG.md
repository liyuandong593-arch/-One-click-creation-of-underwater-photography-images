# Changelog

All notable changes to the Underwater Colorist Skill will be documented in this file.

This project is currently in active Beta development.

---

## [0.1.0] - 2026-09-15

### Added

- Initial public Beta structure
- `SKILL.md`
- Core grading rules
- Scene-specific grading rules
- Failure rules
- Natural mode rules
- Hero mode rules
- QC checklist
- Known limitations document
- User feedback template
- README documentation

### Core Capabilities

- Underwater scene classification
- Natural and Hero grading modes
- Water color cleanup
- Midtone improvement
- Subject readability enhancement
- Skin-tone protection
- Fish and marine-life protection
- Coral / reef color separation
- Top-water haze review
- Deep-water grading guidance
- Artificial-light scene guidance
- Final QC and failure classification

### Core Safety Rules

- Do not change composition
- Do not expand the image unless explicitly requested
- Do not add fish
- Do not change fish direction
- Do not change fish count
- Do not alter human anatomy
- Do not alter facial structure
- Do not modify diving equipment
- Do not invent coral or marine life
- Do not invent lighting
- Do not fabricate scenery
- Preserve original underwater depth

### Learning Loop Added

Each completed image batch should produce:

1. New successful rule
2. New failure rule
3. Proposed rule revision

Only repeatable findings should be promoted into the long-term rule library.

### Known Limitations

- Dense and distant fish schools remain high-risk
- Human hands and faces may be distorted by generative enhancement
- Deep-water scenes remain difficult
- Warm-color recovery depends on source information
- Video temporal consistency is not production-ready
- Final visual quality still depends on the image/editing model used
- Human QC is still required

---

## Planned for 0.2.0

- Collect real-world user test cases
- Add structured before / after case records
- Improve fish-school handling
- Improve skin-tone recovery rules
- Add clearer shallow-water / deep-water branching
- Add stronger scene-specific QC thresholds
- Add camera and device metadata guidance
- Add test-case library
- Add repeatable benchmark images
- Improve feedback-to-rule update workflow

---

## Versioning Policy

### Patch

Example:

`0.1.1`

Use for:

- wording fixes
- small rule corrections
- documentation cleanup
- minor QC adjustments

### Minor

Example:

`0.2.0`

Use for:

- new scene types
- new grading modes
- new QC logic
- significant rule-library expansion

### Major

Example:

`1.0.0`

Use when the Skill reaches stable production readiness with:

- validated workflows
- repeatable results
- mature QC
- stable rule structure
- documented limitations
- sufficient real-world test coverage
