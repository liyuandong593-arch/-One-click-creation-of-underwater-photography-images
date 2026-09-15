# Known Limitations

Current version: V0.1 Beta

This Skill is still under active testing.

## Current limitations

### 1. Fish schools are high-risk

Distant or dense fish schools may be distorted by semantic or generative enhancement.

Preferred strategy:

- exposure correction
- tone correction
- micro-contrast
- restrained clarity

Avoid generative reconstruction.

### 2. Human hands and faces are sensitive

AI enhancement may alter:

- fingers
- hands
- facial structure
- diving equipment

Any anatomy change is a critical failure.

### 3. Deep-water scenes remain difficult

Deep scenes may contain:

- severe color loss
- high noise
- low subject visibility
- strong artificial-light falloff

The system should prefer darker but credible results over bright but unrealistic results.

### 4. Warm-color recovery is limited by source information

If red, orange or skin-tone information is no longer present in the source, the system must not fabricate it.

### 5. Video consistency is not production-ready

Frame-by-frame grading may produce temporal inconsistency.

Current version is primarily optimized for still images.

### 6. AI image-generation quality varies by model

The Skill can provide decision rules and QC, but final visual quality still depends on the image model or editing engine used.

### 7. No automatic guarantee of perfect content preservation

Even with strict rules, AI editing may still accidentally alter:

- fish
- coral
- anatomy
- texture
- lighting
- composition

Human review is still required.

## Recommended Use

Use this Skill as:

- a grading decision framework
- a scene-classification system
- a QC system
- a rule-learning system

Do not treat it as a fully autonomous production pipeline yet.
