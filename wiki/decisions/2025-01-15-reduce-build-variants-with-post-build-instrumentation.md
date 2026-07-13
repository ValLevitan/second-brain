---
type: decision
title: Reduce build variants to a few archetypes with post-build instrumentation
date: 2025-01-15
aliases: [build archetypes, instrumentation post-build, simplify and add lightness]
source-count: 3
status: active
open-commitments: 0
open-questions: 1
---

# Reduce build variants to a few archetypes with post-build instrumentation (2025-01-15)

**Decision:** Instead of the many Jenkins build parameters (historically 10-15 directives), JVL will produce a small set of official build archetypes and move build-time diagnostics/"instrumentation" to a **post-build** configuration step rather than compiling them in. [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

**Decided by:** Val and the engineering team (Aaron proposed it; Pavel, Sasha, Anton, Andrei agreed). Sasha agreed but asked not to hard-cap the number of builds — add more only if needed. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## What was decided

- Collapse the parameter sprawl into roughly **four archetypes**: production non-instrumented, production instrumented, debug, and debug instrumented (exact set not finalised; the point is "a very small amount"). Aaron's slogan: "simplify and add lightness." [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Instrumentation = hooks/tools into the code** (extra logging, test harnesses, the ability to engage otherwise-private functions) that add overhead and are normally excluded from production. It is implemented as **additional external library files/modules loaded at runtime**; a non-instrumented build simply omits those files, so the hooks are present in code but do nothing. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- **GLI handling:** JVL will submit a **non-instrumented** build to GLI, plus a documented procedure showing how the instrumentation would be installed. This lets GLI do lighter review and inspect the instrumentation if they wish, while the shipped article stays close to production. (Copying the instrumentation files in changes the image CRC.) See [[wiki/topics/gli-certification-bottleneck.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Motivation from experience: a six-month unresolved software issue turned out to be one build parameter switched off — a parameter QA arguably should not have been able to toggle. Almost none of the many build variants are ever shipped to customers (roughly one or two out of hundreds). [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- Switching platforms is treated as the moment to "clean house" on legacy directives whose meaning no one remembers. [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]

## Open questions

- The exact final list of build archetypes and which build directives to keep vs. retire is not yet settled (Sasha wants flexibility to add more; "instrumentation" not yet precisely defined). [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]] and [[wiki/topics/build-pipeline-parameterization.md]].

## Sources

- [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
