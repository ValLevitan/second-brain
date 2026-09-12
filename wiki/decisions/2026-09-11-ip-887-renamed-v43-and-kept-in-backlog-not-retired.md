---
type: decision
title: IP-887 is renamed V43 and kept in backlog, not retired — Val proposed killing it and the design team showed him the work buried underneath
date: 2026-09-11
aliases: [IP-887, IP887 renamed V43, retire 887, two South Dakotas, IP-1180, IP-1131 Dakota Bison, IP-1137 Cool Cats, GD-918, IP-1061, I live and die by Jira, moving away from IP items to capabilities]
source-count: 2
status: active
open-commitments: 3
open-questions: 1
---

# IP-887 is renamed V43 and kept in backlog, not retired

A Jira-housekeeping exchange at the [[wiki/meetings/2026-09-11-rage-sunset-and-class-a-on-nova.md|Sept 11 2026 1:00 PM game-development call]] in which [[wiki/people/val-levitan.md|Val Levitan]] proposed retiring an item outright and was talked out of it by [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] and [[wiki/people/lena.md|Lena Zhukova]], who showed him finished design work he had not been able to see. [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## What Val proposed, and why

He read IP-887 and IP-1180 as duplicates — "**do I see IP 887 and IP 1180 as redundant?… Or duplicate**… **it seems like 887 should be gone**" — and then went further: "**887 will never be done… we will never do it**"; "**it will be in Nova and we are moving away from product item into capability item. So I suggest fully retiring 887, that will never happen. And then we will have to open another IP for vertical Nova design.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

Lena's description of the two items is the clearest statement of what each holds: **887** "**was open, it's for vertical, so it's V1, it's… sitting in backlog**", and **IP-1180** "**it's for South Dakota VLT 3, which will be designed in Nova, so we created like separate IP for this**". [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Why it was not retired — there is real work underneath

- **Val could not see the content because he had not opened the subcategories.** He looked at "**IP… 1137, which is South Dakota VLT V1 Cool Cats… vertical and there's nothing in it. There's nothing in it**"; Lena: "**a lot of stuff here and it filled with images**"; Michael: "**There are subcategories. [Beneath] 1137 is the GD, GD 918, and underneath the GD 918 there's a ton of stuff.**" Val: "**Oh yeah, I didn't open that.**" ("Kido" in the transcript at this point is Keno.) [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **A whole unreleased game lives in one of these items.** Michael: "**IP 1131 is an entire game that Lena and I designed that we're going to migrate to D27 Nova for South Dakota, Dakota Bison. It's a game we specifically designed for South Dakota that only exists in IP 1131 right now. So I want to save that and we'll migrate it.**" Dakota Bison's origin is on [[wiki/projects/south-dakota-vlt-market.md]] (May 14 2026). [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **And a second one.** Michael: "**there's a whole other game, K[e]no game that was designed that has to migrate into the Nova 1180**"; Lena: "**we need to redo it for double [screen].**" She named a third piece of completed design — "**solar key[?] also like design was done. It's you don't even see it on timeline because it was done like more than months ago, but… it's filled with images and… work was done**" *(rendered "solar key"; Solar Keno is the corpus's South Dakota title — the identification is the wiki's inference, not the source's)*. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Michael's general objection:** "**Everything, I think everything is valuable. We put a lot of… we got close to getting a lot of this stuff cooking, and then we decided we were going to kill it. So there's a lot of stuff in here, valuable stuff in here. For reference.**" His first suggestion was to move it down into initiatives so it stays referable. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## What was settled instead

- **Rename, don't retire.** Michael: "**Change the name, Lena, of IP887 to V43, just so we know what it is so there's no confusion.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Keep it in backlog; archive only after migration.** Lena: "**let's keep it for now. Let's keep it in backlog**… **Once we migrate it, yeah, then we can archive.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Clean out the loose items while the workload is light, preserving what has value.** Val: "**We are going to be cleaning it out. We're in process of killing all of that, all of those loose items. So I suggest… right now we're not inundated with work… I suggest that you use this small [window] to clean up, preserve.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **And the direction of travel behind all of it:** "**we're changing how we work. We're going to be migrating more to GitHub… We're going to be moving away from IP type of items into capabilities.**" This is the same move recorded across the capability-and-requirements work of Sept 10–11 — see [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] and [[wiki/topics/nova-platform-architecture.md]]. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Why the confusion existed — "2 South Dakotas that look basically the same"

Michael diagnosed it directly, and this is the most useful naming statement in the source [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]:

> "**I think that's part of the problem is that Val is looking at 2 South Dakotas that look basically the same and they're not. One's the Nova D27 and the other one's the Rage V43, which we just recently decided we're not going to pursue.**"
> "**But basically Val, South Dakota VLT, V43 Rage is going to migrate, the games are going to migrate into the D27 South Dakota Nova.**"
> "**we just made the decision that we were doing D27 Nova last week.**"

That "last week" decision is the [[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|Sept-4 call]], where South Dakota D2703 was confirmed dual-screen rather than vertical. The **version-number** question this raises — the source calls the NOVA South Dakota "**VLT 3**" where the owner's ruling of 2026-09-01 names the first NOVA product **South Dakota VLT-2** — is recorded, unresolved, on [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]]. **Do not read this page as settling it.**

## The standing instruction it came with

Val opened the Jira block with a process request that is worth keeping on its own: mark **IP-1061** done when it is actually done — "**Mark IP 1061 completed or done when it's done. Today it's not done yet**" — because "**I live and die by Jira, so please.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Open commitments

- [ ] [[wiki/people/lena.md|Lena Zhukova]] — rename IP-887 to V43, keep it in backlog, and archive it only once the design work has migrated — due unspecified — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — clean out the loose IP items while the workload is light, preserving anything of value — due unspecified — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — mark IP-1061 done in Jira when it is actually done — due when complete — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Open questions

- **Is a separate IP needed for vertical NOVA design?** Val raised it as the counterpart to retiring 887 — "**we will have to open another IP for vertical Nova design**" — and once 887 was kept in backlog instead, the question was never returned to. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]] [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

**§15.8:** clear — tooling and product content only.

## Sources

- [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
