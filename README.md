# Underwater Colorist

AI-assisted underwater color grading Skill for Natural and Hero workflows.

这个项目用于水下照片的 AI 调色与质量检查，目标是在不改变原始构图、人物、鱼群、珊瑚和环境内容的前提下，改善：

- 水体通透度
- 主体清晰度
- 人物肤色
- 鱼群层次
- 珊瑚与水体分离
- 水下空间感
- Natural / Hero 两种风格表现

## Current Status

Beta / Experimental

当前版本已经可以用于真实水下图片测试，但仍处于规则迭代阶段。

重点目标不是“一键生成夸张效果”，而是建立一套可复用、可验证、可持续优化的水下调色流程。

## Core Principles

- Color grading is not image reconstruction.
- Do not change composition.
- Do not add fish.
- Do not change fish direction.
- Do not modify human anatomy.
- Do not invent lighting.
- Preserve underwater depth.
- Prefer credible color over excessive saturation.

## Supported Scenes

- Underwater person
- Person + fish school
- Person + large marine animal
- Coral / reef
- Underwater environment
- Wreck / structure
- Shallow natural-light scene
- Deep-water / low-light scene
- Artificial-light scene

## Grading Modes

### Natural

Natural mode focuses on:

- realistic water color
- clean white balance
- restrained color recovery
- believable skin tone
- natural depth
- minimal stylization

### Hero

Hero mode is built on Natural.

Hero focuses on:

- stronger subject hierarchy
- cleaner midtones
- better depth separation
- stronger local contrast
- more cinematic presentation

Hero does not mean:

- more blue
- more saturation
- more sharpening
- fake lighting

## Skill Structure

```text
.agents/
└── skills/
    └── underwater-colorist/
        ├── SKILL.md
        └── references/
            ├── core-rules.md
            ├── scene-rules.md
            ├── failure-rules.md
            ├── natural-mode.md
            ├── hero-mode.md
            └── qc-checklist.md
How to Use

Use this repository with Codex or another compatible Skill workflow.

The Skill should:

analyze the underwater image
classify the scene
diagnose water color, exposure, haze and subject visibility
select Natural or Hero mode
apply the relevant rules
run QC
record new successful rules, failure rules and rule revisions
Important Limitations

Current limitations include:

AI may distort distant fish
complex fish schools remain high-risk
deep-water artificial lighting requires careful review
video temporal consistency is not yet production-ready
final visual quality may vary across different image models
Feedback

Real-world underwater images are extremely valuable for improving this project.

Useful feedback includes:

camera / device
depth
water condition
scene type
grading mode
before / after result
success points
failure points
whether AI altered any original content
License / Usage

This repository is publicly viewable for testing, learning and research.

Commercial use, paid redistribution, SaaS packaging, resale or commercial integration is not automatically granted.

Commercial licensing should be discussed separately with the project owner.

Project Goal

The long-term goal is to build a reusable underwater color-grading decision system that improves through real test cases, failure patterns and structured QC.

The system should become better because it learns from repeated visual decisions, not because it simply applies stronger effects.
