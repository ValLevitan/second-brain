---
type: meeting
title: Figma-to-testing workflow explainer — Aaron (Aug 12 2025)
date: 2025-08-12
aliases: [figma to testing, visual regression testing, Figma prototyping]
source-count: 1
---

# Figma-to-testing workflow explainer — Aaron (Aug 12 2025)

**Date:** 2025-08-12 · **Speaker:** [[wiki/people/aaron.md|Aaron Bockelie]] (short single-speaker explainer; distinct from the larger figma-to-testing/development session).

Aaron walks through the modern **Figma → React → automated-testing** workflow: a Figma prototype is the "CAD"/design reference (not runnable software); its UI is exported to React pages checked into source control as the real product UI; then **TypeScript tests via a testing framework** acquire the running app's visual presentation and **visually compare it to the Figma reference** (a mismatch flags a failing test), plus directly invoking the UI elements to confirm they react correctly. He uses **Netflix** as the worked example.

Substance on [[wiki/topics/test-automation-strategy.md]] (visual-regression / Figma section).

## Sources

- [[raw/figma_to_testing_transcript.md]]
