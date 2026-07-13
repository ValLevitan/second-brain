---
type: person
title: Aaron
date: 2026-07-12
aliases: [Aaron, Aron, Erin, Eric, Aaron Bockelie]
source-count: 12
---

# Aaron

Aaron works with Val on JVL's product roadmap and Jira planning, and leads JVL's engineering-process modernization — the build pipeline and AI-assisted development.

## Role

- Val works with Aaron to organise JVL's products and initiatives in Jira, and to groom the 2025 plan before a team meeting. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val says he is "speaking to Aaron" about whether the Flex S cabinets should sit at the "product" level or be reorganised. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val asked Aaron to help groom the 2025 plan and attach Jira links to the high-level initiatives, aiming to be ready for a team meeting the week of the 13th. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Build-pipeline and DevOps push (Jan 13)

- On the development-pipeline call, Aaron pushed the Minsk team away from Jenkins toward a Git-native build pipeline — arguing for portability, automation, clean/disposable build environments, and full traceability, and for embedding QA in the build system rather than giving them a Jenkins control panel. [[raw/development_pipeline_january_13_2025.md]]
- He challenged whether the parameterization complexity was a real requirement or legacy baggage, and set homework to research GitHub capabilities equivalent to Jenkins. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]

## AI-assisted development lead (Jan 14)

- Aaron ran the hands-on AI-development workshop for the Minsk team, teaching VS Code + Cline + OpenRouter + MCP, the "maximizer" risk, the "70% problem," and `.clinerules`. He built a Bitbucket MCP server live. See [[wiki/topics/ai-assisted-development.md]]. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Val positioned Aaron as the current in-house expert on AI tooling but said he wants someone to eventually surpass him and lead JVL there. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- At the Jan 15 decision meeting Aaron drove the successful proposal to move JVL off Jenkins to a Git-native, "serverless" build system on GitHub, with a small set of build archetypes and post-build instrumentation. He wrote the English summary of the decisions in the meeting chat and coined "simplify and add lightness." See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]] and [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Val asked Aaron (with Pavel) to break the build-system work out into JIRA features on the board rather than run it as a side project. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Separately, the QA/test-automation consultant said his testing proposal was developed "in consultation with Aaron"; Aaron is to attend the planned testing-architecture meeting. See [[wiki/topics/test-automation-strategy.md]]. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Feature-coaching and DevSecOps grooming (Jan 16–20)

- **DTP-53 (Jan 16–17):** Aaron coached Pavel to turn the Git-native pipeline work (JIRA feature DTP-53) into proper stories and feature descriptions — playing "Scrum Master" on Jan 16, then on Jan 17 insisting features be written from the customer's perspective and documented Git-natively. He demoed prompt styles in Claude but warned against over-relying on AI. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]] [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- **FP7 bottleneck testing (Jan 17):** attended and helped drive the bottleneck questioning; Val repeatedly held Aaron up as the model of pushing him hard without worrying about his feelings. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- **GitHub org structure + DevSecOps grooming (Jan 20):** co-coached Andrei with Val on GitHub organization structure and on aligning a Miro board with the Jira roadmap plus the ITSM operating model. See [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_organization-jan-20-2025.md]] [[raw/meeting_various-jan-20-2025.md]]

His surname is given as **Bockelie** on the Jan 21 continuous-delivery transcript. (First name may appear elsewhere transcribed as "Aron," "Erin," or "Eric.") [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Continuous-delivery architecture and Minsk IT structure (Jan 21–22)

- **CD architecture (Jan 21):** with Jason, walked Val through the three-layer "everything as code" pipeline (product / environment / platform repos plus an integrator), the testing pyramid, and containers-over-disk-images; drove the group to the MVP "Hello World first" step. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]] and [[wiki/decisions/2025-01-21-build-git-native-hello-world-environment-first.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- **Minsk IT structure (Jan 22):** in a short planning call, agreed to convert the Miro board into Jira initiatives/products, shift application-support work to Dima and DevOps work to Andrei, and educate Andrei on DevOps (Andrei agreed). See [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/it_structure_minsk-jan-22-2025.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]]
- [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/meeting_various-jan-20-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/it_structure_minsk-jan-22-2025.md]]
