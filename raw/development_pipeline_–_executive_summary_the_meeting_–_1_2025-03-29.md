---
tags:
  - development-pipeline
  - iso-image
  - build-process
  - github
  - technical
  - strategy
---

Development Pipeline -- Executive summary of the meeting -- meat and
potato -- January 13, 2025:

Below is a non-technical, executive-friendly explanation of **the core
issue** the team is facing:

### **What We're Trying to Achieve**

1.  We need to create an **ISO image** (essentially a bundled
    "installer") that contains our games, math libraries, and other
    components.

2.  **Quality Assurance (QA)** and other teams sometimes need
    **flexibility** to choose which versions of our games or libraries
    go into that ISO image.

### **Where the Problem Lies**

-   Our **current build processes** (where code gets compiled and
    packaged) are mostly set up in **Bitbucket** (and sometimes
    **GitHub**). These tools let us automate how we build the product,
    but they **don't easily allow** a "point-and-click" way for QA to
    pick different versions of games or libraries---especially if that
    selection has to happen *before* the build starts.

-   **Jenkins**, a separate tool, is good at giving users a "dashboard"
    where they can select parameters (like "Game version X" or "Math
    library Y") and then trigger a build. However, this can be **less
    modern** and introduces an extra layer between our main code
    repository and the final build.

### **The Tension**

-   On one hand, **Jenkins** makes it easy for non-technical people to
    choose options with a simple user interface.

-   On the other hand, **Bitbucket/GitHub** are more **modern and
    efficient** if we keep everything (code, build scripts, parameters)
    in a single platform. They're also easier to integrate with future
    technologies like **AI** tools---but they're currently not as
    user-friendly when it comes to picking build parameters on the fly.

### **Why It Matters**

-   We want a **fully automated pipeline** that's also **flexible**. If
    we rely too heavily on Jenkins, we might create **extra complexity**
    and slow down our migration to more advanced technologies.

-   However, if we **don't** offer a user-friendly interface, our QA
    team ends up struggling (or needing more technical knowledge) to
    pick the build parameters they need.

### **In a Nutshell**

We're trying to **balance** two approaches:

1.  **Sticking to Jenkins** for its easy parameter selection (but
    potentially staying with a more "legacy" process).

2.  **Leveraging Bitbucket/GitHub** directly (more modern, better for
    the future, but needs extra engineering to give QA a simple,
    straightforward way to pick the parts they need).

The ultimate goal is to ensure building an ISO image can be **done
online,** with **less manual intervention,** while still giving
**non-technical users** an easy way to choose what goes into that build.

Question to ChatGPT-01 Pro:

"Assuming that we prefer to Leverage Bitbucket/GitHub direction, offer
the proper solution of how to build the development pipeline?"

Answer:

Below is a **high-level, step-by-step** proposal for building a **modern
development pipeline** in Bitbucket or GitHub---**without** relying on
Jenkins as the main driver. This approach balances automation,
flexibility, and ease of use for QA and non-technical staff.

## **1. Use a Single Source of Truth (Git Repository)**

1.  **Centralize** all relevant code, build scripts, and configuration
    files in **one Git repository** (or a set of well-structured repos)
    in **Bitbucket** or **GitHub**.

2.  **Version Control** everything---this ensures all changes (including
    build parameters) are traceable, revertible, and auditable.

**Why this matters:**

-   A single "source of truth" makes it straightforward to track exactly
    which combination of game modules, math libraries, etc. ended up in
    any particular ISO build.

## **2. Define Builds in a YAML Pipeline File**

1.  **Create** a bitbucket-pipelines.yml (for Bitbucket) or a
    .github/workflows/\*.yml file (for GitHub Actions) in your
    repository.

2.  **Specify** stages:

    a.  **Compile** code and run unit tests.

    b.  **Build** Docker images (if containerizing your modules).

    c.  **Assemble** final artifacts (e.g., generating the ISO).

3.  **Parameterize** your pipeline to accept variables like:

    a.  GAME_VERSION

    b.  LGS_VERSION

    c.  PROGRESSIVE_LIB_VERSION

    d.  etc.

**Why this matters:**

-   Having an "as-code" pipeline (in YAML) ensures your build process is
    consistent, transparent, and portable. Anyone who checks out the
    repo can see exactly how the pipeline is defined.

## **3. Implement Parameterization & Version Selection**

To allow QA (or other users) to choose different versions of games,
libraries, and modules **before** a build starts:

### **3.1 Use a Configuration File Approach**

-   Maintain a **separate** build-config.yml (or .json or .ini) in the
    same Git repo.

-   This file lists the **default** or **available** versions: (Code)

*gameVersion: \"v1.5.3\"*

*lgsVersion: \"17.0.2\"*

*mathModuleVersion: \"2.0.1\"*

*progressiveLibVersion: \"1.0.0\"*

**QA** can update this file **in a feature branch** (e.g., QA-branch) to
select specific versions: (Code)

*gameVersion: \"v2.0.0-rc\"*

*lgsVersion: \"17.0.5\"*

*mathModuleVersion: \"2.1.0\"*

*progressiveLibVersion: \"1.1.0\"*

When they commit the updated file, **Bitbucket/GitHub** automatically
triggers the pipeline with these parameters.

### **3.2 Optional: Predefined Build Variables**

-   Within your pipeline YAML, define **input variables** that the
    pipeline can accept.

-   Bitbucket Pipelines and GitHub Actions each let you define
    environment variables or "workflow inputs" that can be changed
    per-run (though some are more "static" than Jenkins' dynamic UI).

\# For GitHub Actions, for example:

on:

*workflow_dispatch:*

*inputs:*

*GAME_VERSION:*

*description: \"Select which game version to build\"*

*required: true*

*default: \"v1.5.3\"*

*LGS_VERSION:*

*description: \"Select which LGS version to build\"*

*required: true*

*default: \"17.0.2\"*

*jobs:*

*build:*

*runs-on: ubuntu-latest*

*steps:*

*- name: Check out*

*uses: actions/checkout@v2*

*- name: Run build script*

*run: ./build.sh \${{ github.event.inputs.GAME_VERSION }} \...*

-   

-   **Caveat**: These defaults are generally "static" in the YAML, so
    you may need a script step if you want truly **dynamic** lookups of
    available versions.

**Why this matters:**

-   By storing parameters in the repo (whether in a separate config file
    or pipeline inputs), you get full traceability. Any build is
    reproducible by checking out the specific branch/commit.

## **4. Automate Artifact Management**

1.  **Store** all built artifacts (e.g., Docker images, JAR files, final
    ISO) in an **artifact repository** (Artifactory, Nexus, or even
    simple S3 buckets).

2.  **Tag** artifacts with the corresponding version parameters.

3.  **Link** them back to the Git commit SHA for full transparency
    ("This ISO was built from commit X with game version Y.").

**Why this matters:**

-   QA and other teams can quickly find or roll back to any previous
    build.

## **5. Provide a Lightweight "UI" for Non-Technical Users**

Since Bitbucket/GitHub's built-in parameter forms can be **static**, you
can address QA's needs in **one of two ways**:

### **5.1 Branch-Based Workflow**

-   **QA** creates a new branch (e.g., QA-rc-tests) from main.

-   **Edits** the build-config.yml in that branch (changes versions).

-   **Commits** the config changes → triggers the build → pipeline picks
    up the new versions.

-   **Result**: an ISO artifact is produced and tied to that branch.

This requires QA to use basic Git operations (branching, editing a file,
committing). It's simpler than it sounds if you give them a short
"how-to" guide.

### **5.2 Custom Web Front-End (Optional Extra)**

-   A small internal web form that:

    -   **Lists** the available versions (pulled from some metadata or
        artifact repo).

    -   **Saves** the chosen versions to build-config.yml.

    -   **Commits** the file automatically to a "build" branch in
        Bitbucket/GitHub.

    -   **Triggers** the pipeline run.

**Why this matters:**

-   Either approach **avoids** forcing Jenkins onto the pipeline.

-   Option 5.2 is user-friendly for QA but does require extra dev work
    to build that UI.

## **6. Ensure Traceability & Auditability**

1.  **Always** link build logs to the Git commit that triggered them.

2.  **Tag** or **label** the final ISO artifacts with the commit SHA or
    pipeline run ID.

3.  **Archive** logs and artifacts so QA and Dev teams can see exactly
    what was built and with which parameters.

**Why this matters:**

-   This meets modern DevOps best practices, helps debugging, and speeds
    up regulatory audits or internal QA checks.

## **7. Keep the Pipeline Environment "Ephemeral"**

1.  Use **container-based builds** to avoid long-lived servers.

2.  **Spin up** a container (Bitbucket Pipelines or GitHub Actions
    runner) → **build** the product → **tear down**.

3.  **No** manual changes on the build agent---everything is in
    code/config.

**Why this matters:**

-   Ensures consistent builds without the "it worked on one Jenkins
    server but not on another" scenario.

-   Makes it easy to move or replicate builds (e.g., if you switch from
    Bitbucket to GitHub or vice versa).

## **8. Position for Future AI Integration**

-   By storing your entire pipeline and config in **version-controlled
    YAML**, you unlock the ability for AI tools (like ChatGPT or other
    coding assistants) to:

    -   **Suggest** pipeline changes.

    -   **Auto-generate** or **validate** build-config.yml updates.

    -   **Trigger** new builds via APIs.

-   If you rely heavily on Jenkins with a big customized UI, hooking
    into advanced AI solutions can get trickier and more fragile.

# **Putting It All Together**

1.  **Consolidate** all build scripts and config in Bitbucket/GitHub.

2.  **Define** the build pipeline(s) in YAML files for full automation.

3.  **Parameterize** versions either by (a) branch-based config file
    edits or (b) direct pipeline variables.

4.  Optionally **add** a small internal web form if QA needs a simple
    interface (the form just automates the branch/commit process).

5.  **Publish** resulting artifacts to a repository, labeled with
    versions and commit IDs.

6.  **Document** a simple workflow so QA/devs know how to trigger
    specialized ISO builds.

7.  **Maintain** ephemeral build environments to ensure reliability and
    consistency.

By following these steps, you'll have a **fully traceable**,
**AI-friendly**, and **modern** pipeline that doesn't depend on Jenkins
as a parameter dashboard. You can still keep Jenkins on standby for any
specialized tasks, but the main pipeline---and the future of your
DevOps---remains in your **Git-based system**.
