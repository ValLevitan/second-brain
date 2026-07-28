**JVL SYSTEMS**

**GitHub Ways Configuration**

*Architecture, Purpose & Operating Guide*

  ---------------------------- ------------------------------------------
  **Prepared by**              Val Levitan, CEO --- JVL Systems

  **Advisor**                  Aaron Bockelie

  **IT Owner**                 Andrei Bosik, IT Manager

  **Date**                     March 2026

  **Classification**           Internal --- Confidential

  **Status**                   Draft --- Active Setup
  ---------------------------- ------------------------------------------

**1. Executive Summary**

JVL Systems is establishing a proprietary AI behavior infrastructure built on top of a proven, externally-maintained "Ways" system developed by Aaron Bockelie. This document describes what that infrastructure is, why it matters, how it is architected, and how it is meant to be operated on an ongoing basis.

+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **What is a "Way"?**                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| A Way is a structured instruction file that tells Claude (the AI tool) how to behave in a specific situation --- essentially a recipe. Ways define how Claude approaches tasks, what tone it uses, what it checks before acting, and how it structures its outputs. The more precisely these are written, the more reliably and intelligently Claude performs. JVL's goal is to build and own a library of Ways that encode JVL's specific knowledge, standards, and working methods. |
+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This system is not a minor IT project. It is the foundation for how JVL will progressively embed higher intelligence into its operations. The discipline with which JVL builds, curates, and maintains its Ways will directly determine how quickly and effectively the company benefits from advances in AI. Done well, it compounds: each new Way makes the next one easier to build, and the whole library becomes more valuable over time.

**2. Purpose & Strategic Objectives**

**2.1 Why We Are Doing This**

JVL is moving deliberately toward a future where AI tools play a central role in day-to-day operations across every department. The quality of that AI's behavior depends directly on the quality of the instructions it receives. Generic AI behavior produces generic results. JVL-specific Ways, built with care and precision, produce results that reflect JVL's standards, culture, and institutional knowledge.

+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Strategic Direction (Val Levitan, March 2026)**                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "We intend to quickly evolve into using higher intelligence. Everything coming out in terms of intelligence will be much smarter than many of the people working for JVL. We will be embracing it. Developing our own ways of doing things, taking ownership of these ways, grooming them and promoting them --- intelligently, with care --- is important because it will make us as a company much smarter if we do it right. It will elevate JVL to a higher level quickly and exponentially." |
+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**2.2 Objectives**

- Build and own a library of JVL-proprietary Ways that encode company-specific knowledge, standards, and working methods.

- Establish a reliable, governed infrastructure for deploying those Ways to all JVL employees who use Claude.

- Maintain compatibility with Aaron Bockelie's upstream Ways system so JVL continuously benefits from his ongoing improvements.

- Create a quality control process so that no experimental or broken Ways reach production environments without review.

- Develop internal competency: a small group of trusted JVL staff who understand how Ways work and can evaluate, test, and contribute new ones.

- Ensure the system is Andrei Bosik's owned, long-term operational responsibility --- not a one-time setup.

**3. Architecture Overview**

The system has two distinct worlds that connect to each other: Aaron's external repository and JVL's internal repository. Understanding the relationship between these two is essential.

**3.1 Aaron's Repository (External)**

Aaron Bockelie maintains a public GitHub repository at github.com/aaronbckie/claude-code-config. This is the upstream source of the core Ways system. It contains the fundamental framework, directory structure, hooks, scripts, and agents that make Ways function. Aaron continues to actively develop and improve this system. JVL does not own or control this repository.

Aaron's repository has its own main branch and feature branches. JVL pulls from his main branch on a regular automated basis, keeping JVL's own main branch current with his latest improvements.

**3.2 JVL's Repository (Internal --- GitHub Enterprise)**

JVL maintains its own private repository at github.com/enterprises/jvl. This is where all JVL-specific configuration lives. Because JVL uses GitHub Enterprise, a traditional public "fork" is not possible. Instead, JVL maintains its own copy and synchronizes from Aaron's repository via automated Git pull. The internal repository contains several branches, each serving a distinct purpose.

  ------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Branch**          **Purpose**

  **/main**           JVL's synchronized copy of Aaron's Ways. Contains core hooks, scripts, documentation, and the base agent. Updated automatically via Git pull from Aaron's main. No JVL-specific content lives here --- it stays clean so updates can flow in without conflict.

  **/jvl**            The JVL proprietary branch. This is where all JVL-specific Ways files and the JVL-specific agent live. This branch contains only the additions that make Ways work JVL's way. It never flows back into Aaron's repository. This is JVL's intellectual property.

  **/\[username\]**   Personal experimentation branches for individual users. Staff can build and test their own Ways here. Good ideas can be promoted upward via Pull Request. These branches can live indefinitely if the person finds them useful.

  **/test-qa**        Automated testing branch. When a merge is attempted, the system runs automated scoring tests here to verify that nothing is broken before the changes are allowed to proceed to Stage.

  **/stage**          Pre-production branch. A designated group of trusted users are subscribed to this branch. They use it in their real work and provide feedback before anything is released to all employees.

  **/prod**           Production branch. What every JVL employee's machine receives. Promoted from Stage by Andrei once Stage validation is complete. Distributed automatically via the existing script infrastructure.
  ------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**4. How It Functions --- The Pipeline**

The system operates as a software delivery pipeline. This is the same discipline used in professional software development, applied to AI behavior. The pipeline ensures that only tested, reviewed content reaches JVL employees. Below is the end-to-end flow.

+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **The JVL Ways Pipeline --- End to End**                                                                                                                                                                                                                                                                                                                      |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Step**                | **Stage**                                   | **What Happens**                                                                                                                                                                                                                                                                      |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **1**                   | **Git Pull (Automated)**                    | Aaron releases updates to his repository. JVL's automated script pulls those changes into JVL's /main branch. This keeps JVL current with the latest core improvements without any manual action required.                                                                            |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **2**                   | **JVL Branch Development**                  | Authorized staff add new JVL-specific Ways to the /jvl branch. These are Ways that encode JVL's specific knowledge, standards, and working methods. They have no impact on Aaron's system.                                                                                            |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **3**                   | **Personal Branch Contribution (Optional)** | Individual users may develop personal Ways in their own branches. When a personal Way is ready for broader use, the person submits a Pull Request to the JVL branch for review.                                                                                                       |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **4**                   | **Integration Merge**                       | The JVL branch content is merged with /main to form a combined whole. This is where the JVL-specific Ways join the core Ways framework. If the merge proceeds cleanly, it proceeds automatically. If there are conflicts, they require manual resolution by Andrei before proceeding. |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **5**                   | **Automated Test / QA**                     | The merged result is scored automatically using tests built into the Ways system. These tests verify that the Ways function correctly and meet quality thresholds. This is the first quality gate. Failures are routed back for correction.                                           |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **6**                   | **Stage**                                   | The tested build is deployed to a designated group of trusted users who use it in their real daily work. They are not running formal tests --- they are simply working normally and noticing whether anything has degraded or improved. This is the human quality gate.               |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **7**                   | **Prod Release**                            | Once Stage feedback is neutral to positive, Andrei triggers the production release. The existing script infrastructure performs a Git pull on every subscribed employee's machine. All users receive the updated Ways automatically.                                                  |
+-------------------------+---------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Why Not Go Straight to Prod?**                                                                                                                                                                                                                                                                                                                                      |
|                                                                                                                                                                                                                                                                                                                                                                       |
| The Stage layer exists to protect employees from content that passed automated tests but still behaves unexpectedly in real use. Without Stage, a misconfigured Way could deploy to everyone's machine and disrupt their Claude behavior company-wide. The Stage layer, combined with trusted human reviewers, catches these issues before they cause broader impact. |
+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**5. Branch Naming & Organizational Conventions**

Clear naming conventions prevent confusion as the number of branches and contributors grows. The following conventions were established during the March 2026 architecture sessions.

- Personal branches use the individual's username in lowercase: /val, /andrei, /\[username\], etc.

- The JVL proprietary branch is always /jvl. This is the only branch that feeds into Stage.

- Do not create additional "main" branches. /main is reserved exclusively for the synchronized copy of Aaron's work.

- Personal branches may live indefinitely. There is no requirement to delete them after a contribution.

- All Ways files in the /jvl branch must follow Aaron's established directory structure: /hooks/ways/jvldomain/way1/... and /agents/jvlagent1.md.

- The JVL agent file (/agents/jvlagent1.md) is the JVL-specific agent definition. It lives in the /jvl branch and is never committed to /main.

**6. Roles & Responsibilities**

The system requires clear ownership to function. The following roles were established as part of the March 2026 architecture and setup sessions.

  ------------------------- --------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Person / Role**         **Title**             **Responsibilities**

  **Val Levitan**           CEO                   Sets strategic direction for which Ways JVL builds. Owns the source documents and architectural thinking that Ways are built from. Approves the overall direction of the Ways library. May maintain a personal branch for experimentation. Does not manage the technical infrastructure.

  **Andrei Bosik**          IT Manager (Global)   Owns the JVL GitHub repository and the full pipeline infrastructure. Responsible for the automated sync from Aaron's repo, maintaining the /jvl branch, managing the merge and release process, operating the Stage environment, and distributing Prod to all employees. This is a long-term operational responsibility, not a one-time setup.

  **Aaron Bockelie**        External Advisor      Maintains the upstream Ways system at github.com/aaronbckie/claude-code-config. Guides JVL on how to structure, build, and test new Ways. Provides the prompt templates used to generate new Ways from JVL's source documents. Does not have write access to JVL's internal repository.

  **Trusted Stage Users**   Designated Staff      A small group of technically capable JVL employees who are subscribed to the Stage branch. They use Claude in their real daily work and provide informal feedback on whether behavior has improved, degraded, or changed unexpectedly. Candidates should have regular hands-on experience with Claude Code. Must develop working familiarity with how Ways function to be effective in this role.

  **JVL Employees**         End Users (Prod)      Receive the production Ways automatically via Andrei's distribution script. May optionally request a personal branch if they wish to experiment. Do not interact with the pipeline directly.
  ------------------------- --------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**7. How to Build a New JVL Way --- Step by Step**

This section describes the practical process for creating a new Way from scratch, using the method established during the March 2026 sessions. The process combines a source document with a structured prompt, and uses Claude Code to generate the actual Way files.

**7.1 Prerequisites**

- Andrei has the JVL repository set up locally with the /jvl branch checked out.

- Claude Code (CLI) is installed and functional in Andrei's Ubuntu environment.

- Aaron has provided the standard prompt template for Way generation.

- A source document exists describing the behavior or process to be encoded as a Way.

**7.2 The Process**

1.  Prepare the source document. Val or the relevant subject-matter expert writes a document describing the JVL-specific behavior, standard, or process to be encoded. This document does not need to be in any special format --- it just needs to clearly explain what JVL does and why.

2.  Open Claude Code in the JVL repository directory (the .cloud directory where the git repo lives).

3.  Paste the prompt template provided by Aaron into Claude Code. Do not press Enter yet.

4.  Copy the full text of the source document and paste it immediately after the prompt, so the entire prompt and document text form a single input.

5.  Press Enter. Claude Code will create the working branch, decompose the source document into properly structured Way files, and place them in the correct directory structure.

6.  Review the generated Way files. Confirm they are structured correctly and reflect the intent of the source document.

7.  Commit the Way files to the personal branch.

8.  When ready for broader use, submit a Pull Request from the personal branch into /jvl.

9.  Andrei reviews the Pull Request and merges it into /jvl when satisfied.

10. Andrei triggers the integration merge, automated tests run, and the Way progresses through Stage to Prod via the standard pipeline.

+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Important Note on API Availability**                                                                                                                                                                                                                                                                                                                                                                               |
|                                                                                                                                                                                                                                                                                                                                                                                                                      |
| During the March 18 session, the Anthropic API experienced an outage that prevented completion of the first Way generation. This is a known risk for any session that depends on Claude Code. If the API is unavailable, save the combined prompt and document as a plain text file and attempt the session again when service resumes. When resuming, continue the existing session rather than starting a new one. |
+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**8. Ongoing Maintenance & Hygiene**

The value of this system depends entirely on how well it is maintained over time. The architecture is designed to be low-friction, but it requires consistent discipline from Andrei and the trusted users group.

**8.1 Keeping Current with Aaron's Repository**

Andrei's team already runs an automated script that updates Claude Code configs across all employee machines. This same script must incorporate the Git pull from Aaron's repository into JVL's /main branch. The frequency should be at minimum weekly, ideally daily. When Aaron releases a significant update or notes a breaking change in his version notes, Andrei should review the release notes and confirm compatibility with JVL's /jvl branch before allowing the update to flow through to Prod.

**8.2 Reviewing Personal Branch Contributions**

Periodically --- monthly is a reasonable starting cadence --- Andrei should review all active personal branches to identify any Ways that have been created and might be worth promoting to the /jvl branch. This review process is how good individual ideas become company-wide assets. It does not need to be exhaustive; a quick scan for new commits in personal branches is sufficient.

**8.3 Stage Feedback Loop**

Trusted Stage users should understand what they are being asked to do: use Claude normally and notice if anything seems off or improved. Andrei should have a simple way to collect this feedback --- a Slack channel or a recurring check-in is sufficient. The bar for promotion from Stage to Prod is neutral to positive sentiment, not perfection.

**8.4 Building Internal Competency**

The system's long-term health depends on JVL having more than one person who understands how Ways work. JVL should identify and develop at least two or three staff members who can evaluate, test, and contribute Ways. Candidates should be active daily users of Claude Code. This is an investment in institutional capability, not just technical infrastructure, and it directly determines how effectively the system scales across the organization.

**9. Key Decisions & Constraints**

The following decisions and constraints were confirmed during the March 2026 architecture sessions and should be treated as standing policy.

  ---------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Decision / Constraint**                                  **Detail**

  **JVL Ways are proprietary**                               Content in the /jvl branch never flows back into Aaron's public repository. It is JVL intellectual property.

  **No true GitHub fork possible**                           JVL's GitHub Enterprise subscription does not support public forks. The /main branch synchronized via Git pull is the equivalent solution.

  **Andrei owns the pipeline**                               The CI/CD process, branch management, Stage, and Prod release are Andrei's responsibility. This is a standing operational duty, not a project deliverable.

  **Do not push directly to Prod**                           All changes must pass through Test-QA and Stage before reaching Prod. No exceptions, regardless of how confident the author is in the change.

  **Merge conflicts are Andrei's responsibility**            When a merge conflict occurs between /jvl and /main, Andrei resolves it manually. The resolution is typically to adjust the /jvl branch so it is compatible with the current /main.

  **Aaron's breaking changes require attention**             When Aaron notes a breaking change in his version notes, JVL must review the /jvl branch for compatibility before allowing the update into Stage.

  **The Confluence diagram is the reference architecture**   The whiteboard diagram created during the March 18 session is the canonical visual reference for this system. It is stored at the JVL Confluence link shared during that session.
  ---------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**10. Immediate Next Steps**

The following actions are outstanding as of March 18, 2026, to be addressed in the next session.

11. Andrei confirms the /jvl branch has been created in JVL's private GitHub Enterprise repository.

12. Aaron's prompt template is saved as a plain text file by Andrei, ready to use in the next Claude Code session.

13. Val's source document is confirmed available and accessible for the Way generation session.

14. The next working session is scheduled. Aaron will guide Andrei through the first live Way generation: paste the prompt, paste Val's document, let Claude Code create the Way files, commit, and test.

15. Andrei identifies and confirms the initial Trusted Stage Users group. Selected individuals are briefed on their role and what to look for when evaluating Stage builds.

16. Andrei reviews the Confluence architecture diagram with his team to confirm shared understanding of the full pipeline before the next session.

*JVL Systems \| Internal Confidential \| March 2026*
