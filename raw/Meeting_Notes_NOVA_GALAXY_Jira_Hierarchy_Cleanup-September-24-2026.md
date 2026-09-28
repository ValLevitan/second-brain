# Meeting Summary — NOVA and GALAXY state of affairs.
**Date:** September 24, 2026, 10:00 AM – 11:31 AM Eastern
**Duration:** About 91 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexander Biratko, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026]]

## Summary

Meeting held in Russian. Val called it to check that Jira is set up for NOVA and GALAXY the way the team agreed in its standards, and to fix any places where the team drifts from them.

**Where the work stands.** Pavel said there is **no GALAXY work at all** — no discussion, no work, no repositories. NOVA work is going on, but it is organized the old way: tasks sit under IP-90 Applications, initiative **IP-481 NOVA Gaming Platform Land-based**.

**Jira projects = GitHub repos.** Dmitri Kovalchuk confirmed he created all projects at the last meeting and now every repository has exactly one Jira project. Jira has extra old projects; Val said they will be closed and fade away. Two cases differ: the keys for **LGS and RGS** were already taken by old projects. Dmitri proposed keeping the key and only renaming the project (for example to "Platform Local Gaming Server", like the repo). Val agreed.

**Rename "omni" repos to "nova".** Andrei Bosik said 15 repositories still carry "omni" in the name (omni core, omni concept, omni framework and others) and should become "nova". He warned that renaming can break cross-repo builds and developers must fix their own builds. Biratko said there is no final build or ISO yet, so now is the right time; whatever breaks gets fixed. Pavel noted Zhenya is working on a manifest in the integration repo that ties repo versions into one artifact. Val agreed the rename can go ahead now.

**Capabilities and requirements.** Val gave Biratko responsibility to move all features under the right capabilities, and to create capabilities (with requirements) where they do not exist. Biratko pointed out LGS has no requirements. Pavel said LGS got a "prose" document but never went further. Val said prose plus the existing architecture means capabilities and requirements can be written quickly. Val said NOVA needs a product manager — probably Pavel for now, though he would prefer someone else (he named Kharetski as a possible good one).

**The long debate: how to structure NOVA under the top level.**
- Val first wanted the hierarchy under NOVA to follow the platform architecture (LGS, framework, math, games), so it is clear where a change lands.
- Dzmitry Chudzinau disagreed: about 90% of work touches more than one repo, a capability almost always spans several products, and scrolling through ~20 repos is awkward. He likes how Transactional MVP1 works now — group by planned release.
- Pavel worried that one list could reach 100 capabilities on a screen, and that splitting by initiative would force copies of the same capability.
- Irina explained that yesterday they created **IP-1199 and IP-1202** to separate Transactional MVP1 (ends October 1) from MVP2 (ends October 29), and the team finds it useful.

**Where it landed (Val's final position, Pavel: "this approach suits everyone").**
- Under the NOVA platform: **one long, flat list of capabilities**. Views come from **filters** — by Jira project (= repo), release, status, assignee. LGS, framework and each game are already Jira projects, so filtering by project works.
- **A release is not part of the hierarchy.** Val is firmly against initiatives named after a release (like "MVP1"). Releases should be Jira releases shown as **vertical lines on the timeline**. Dmitri Kovalchuk suggested filtering by release; Pavel showed a release filter live, and Val liked it. Pavel said the same release then has to exist in every project, and features must carry it too.
- **Top level.** Val said IP-1204 should be the value stream **Core**, with the NOVA and GALAXY platforms under it. Pavel said the existing IP-738 "Core" is really helper tools; Val said to rename that one to **Tools**, and Pavel agreed to call the stream Core.
- **Transactional.** Irina moved items during the meeting. Val disliked the current initiative name. Pavel said it covers FlexPort and Flex Pay too, not only Flex IQ. Val proposed keeping one **Transactional** initiative with its capabilities under it, and seeing FlexPort, Flex IQ and so on through project filters.
- **Remove the IP layer for products.** FlexPort, IQ, Dispenser and similar are already repos/projects, so they should not also be initiatives. Old features under them must be moved to existing or new capabilities and closed. Val said Claude Code can do much of this.
- Chudzinau: "Let's do it first and then see" how filters work when moving a capability from one MVP to another.

**GALAXY.** Val wants "Transactional Galaxy" renamed to **Galaxy Platform**, and IP-1095 moved under Core. Chudzinau argued server and machine work belong together: either everything under GALAXY or everything under NOVA, or capabilities will split again. Pavel thinks the transactional server and the NOVA server barely overlap. Irina said the capabilities now under GALAXY (IP-1096 set) move to IP-1199. Chudzinau expects only two platforms to remain, with CMS kept as legacy; RAGE the same; progressives and math move to NOVA. This was not settled.

**Top-level value streams.** Val said he clearly sees three: **Games, Core, Hardware**. The game production / design / concept IPs are parked for now.

**Why Val wants this done now.** He does not want the meeting to end in talk only, and he does not want Pavel acting as the team's secretary. He asked Biratko and Chudzinau to move their own capabilities themselves.

## Decisions Made

- **Jira projects match GitHub repos one-to-one; LGS and RGS projects keep their keys and get renamed to match the repos.** (Dmitri Kovalchuk proposed; Val agreed)
- **Repositories with "omni" in the name are renamed to "nova" now**, fixing any broken builds after. (Andrei Bosik proposed; Val agreed; Biratko supported)
- **Under the NOVA platform, capabilities sit in one flat list; views come from filters** (project, release, status, assignee). (Val; Pavel: acceptable to all; Chudzinau wants to see it working first)
- **Releases are Jira releases shown as vertical timeline lines, not initiatives in the hierarchy.** (Val)
- **The top value stream is named Core, with NOVA and GALAXY platforms under it; the old IP-738 "Core" is renamed Tools.** (Val; Pavel agreed)
- **Product-level IPs (FlexPort, IQ, Dispenser, etc.) are removed; their features move under capabilities.** (Val; Pavel, Chudzinau and Dmitri Kovalchuk agreed)
- **Game production / design / concept IPs are parked.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Groom Jira: remove the product IP layer, attach features to existing or new capabilities (using Claude), then set up releases (MVP1, MVP2) as timeline lines | Report time needed by Tue Sep 29, 2026 | High | Val asked; Dmitri: "I can try" |
| 2 | Dmitri Kovalchuk | Rename the LGS and RGS Jira projects to match their repos (keys stay) | TBD | Normal | |
| 3 | Andrei Bosik | Rename the ~15 "omni" repositories to "nova" | TBD (Val: can do now) | Normal | Developers fix broken builds |
| 4 | Alexander Biratko | Move NOVA features under the right capabilities; create missing capabilities and requirements | Thu Sep 25, 2026 (morning) | High | Val wants it by tomorrow morning |
| 5 | Dzmitry Chudzinau | Move his own capabilities into the new structure himself | Thu Sep 25, 2026 (morning) | High | So Pavel is not the secretary |
| 6 | All attendees | Tag the features they work on with the release, so release filters work in every project | TBD | Normal | Pavel's proposal |
| 7 | Pavel Frolov | Rename IP-481 / IP-1204 per the Core / Tools decision | TBD | Normal | Pavel started during the meeting |
| 8 | Val Levitan | Move the next meeting with Pavel and Irina by 15 minutes | Sep 24, 2026 | Low | |

## Open Questions

- **GALAXY structure:** separate Galaxy Platform under Core, or one platform holding both server and machine capabilities? (Chudzinau vs Val; Pavel's view differs) — not settled.
- **Who is NOVA's product manager?** Probably Pavel for now; Val wants someone else. (Val)
- **Where games and game design live** (IP-90 vs a Games value stream) — parked by Val. (Irina raised)
- Whether the flat list stays usable once filters are in use. (Chudzinau)

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026, 12:20 PM Eastern*
*Source meeting: NOVA and GALAXY state of affairs.*
