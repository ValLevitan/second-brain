# Meeting Summary — Conversion Cycle: Texas Rage Horizontal to Texas NOVA Vertical
**Date:** October 18, 2026, 8:04 AM – 8:44 AM Eastern
**Duration:** ~40 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026]]

## Summary

Held in Russian.

**Vertical Dutch Mill on Rage (Igor showed it).** Igor built the vertical Dutch Mill from the existing horizontal assets. He made a master frame from the old resources, improved it with ChatGPT and Gemini, then animated it with Claude. Texas games are older and their art is simpler than Dragon Pays, so more work was needed. The result: base game, one Dutch Mill bonus, and one bonus shared by all games of the product. Sky, windmill, girl and background are animated. 4 symbols were redrawn to match the new style and animated. The help screen is new. The shared bonus got the least time and is the least polished. All of this took one week. Sergey Klimenovich had trouble with access to AI tools; it was fixed today.

**Video loops.** AI video tools loop animations poorly, and idle animations must loop with no visible jump. Programmatic animation made with Claude (windmill blades, sky) loops correctly. Part of the girl's video had to be finished with Claude. Igor thinks Sergey will find the right prompts and references with more tries.

**Estimate.** The other Texas games are more abstract and should be easier than Dutch Mill. Igor estimates the move of one game to NOVA at no more than "15:00" (as heard; most likely 15 hours), including tests. Games live in separate repositories, so several can run in parallel once their art is ready. Efim sent Igor the math in a container; Igor will run it locally. Igor needs only the Dutch Mill repository to start.

**Can an artist do this alone?** Val asked if Sergey can be trained to do the whole job, with Igor improving the working environment step by step until any good graphic designer can move games from one market to another. Igor: likely possible, but it must be tried. Today the "environment" is the md files, prose, ADRs and contracts in the repositories. Pavel noted that Anton Leshkevich and Daniil (about 50% free) are also available, while Sergey can work only on weekends or about 2 hours a day. Val prefers Sergey because he is a graphic designer and can improve the art on the fly. Val said this is secret for now; later it can go to all artists under the VP / design director.

**Three kinds of tool sets (Pavel).** (1) Rage horizontal to Rage vertical; (2) Rage vertical to NOVA vertical; (3) from a finished NOVA game, make many new games with new art and new math.

**Rage is closed.** Irina asked whether the re-skin is for Rage or NOVA. Val: Rage is finished. Nothing more is done for Rage; everything is done only on NOVA.

**Re-skin test.** Igor proposed that Sergey re-skin Dutch Mill (new theme, same structure) with no help from Igor, to test how well the tools are documented. Pavel said Sergey needs a theme or concept art to start; he will not invent one. Val: base it on a theme, not on existing art; the art is made from scratch. **Val will ask Michael to write a new theme abstract to replace Dutch Mill — the abstract only.** Pavel agreed. Before that, **Igor writes a technical spec of what the abstract must describe**: scenes, components on each scene, placeholders (Irina's examples: main elements, symbols, bonuses, trees, sky, ground). Pavel warned Michael may feel the process is upside down; Val said he will handle Michael.

**Meeting rule.** Val asked people not to answer while a question is still being asked: question, pause, answer. He needs time to follow.

**Next steps.** Val asked Pavel or Igor to propose the next 2 weeks of steps, with undertakings for developers and artists and milestones to check. Only the Wednesday milestone was set in this meeting.

## Decisions Made

- **Rage is finished; all new work is done only on NOVA.** (Decided by Val Levitan)
- **Milestone: first iteration of Dutch Mill moved from Rage to NOVA, reviewed at a meeting on Wednesday Oct 21.** (Decided by Val Levitan)
- **The re-skin test starts from a new theme abstract written by Michael (abstract only), built on Igor's technical spec; the art is made from scratch.** (Decided by Val Levitan; Pavel Frolov agreed)
- **Meeting today at 11:00 AM Canadian (Eastern) time to review Igor's spec.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Write the technical spec of what the theme abstract must describe (scenes, components, placeholders) and send it | Oct 18, 2026, before 11:00 AM ET | High | Igor: "today"; Val: "in a couple of hours" |
| 2 | Val Levitan | Hold the 11:00 AM ET meeting today to review the spec | Oct 18, 2026 | High | Igor, Pavel, Irina confirmed they are available |
| 3 | Igor Metelski | Move Dutch Mill from Rage to NOVA (first iteration, with tests) | Oct 21, 2026 | High | Estimate "15:00" as heard (likely 15 hours) |
| 4 | Val Levitan | Set the Wednesday meeting to review the Dutch Mill NOVA iteration | Oct 21, 2026 | Normal | |
| 5 | [Unassigned — needs clarification] | Give Igor access to the Dutch Mill repository | Before work starts | High | Igor's only blocker |
| 6 | Val Levitan | Ask Michael to write a new theme abstract replacing Dutch Mill (abstract only) | After the spec review | Normal | |
| 7 | Igor Metelski | Remove the intermediate Rage scene step; send art straight to the OMNI scene converter | TBD | Normal | Igor: "I will do it" |
| 8 | Sergey Klimenovich | Keep testing AI video tools to get clean looping animations | TBD | Low | Not present |

## Open Questions

- Who proposes the next 2 weeks of steps, undertakings and milestones for developers and artists? Val asked Pavel or Igor; no one took it in the meeting. (Raised by Val)
- Will Sergey (weekends / ~2 hours a day) do the re-skin, or Anton Leshkevich or Daniil? Not settled. (Raised by Pavel)

## Dispatch Log

- 2026-10-18 9:19 AM ET — Teams invites sent on Val's request (items 2 and 4) to Igor, Pavel, Irina, Evgeny: "Review - technical spec for the Dutch Mill theme abstract" Oct 18 11:00–11:30 AM ET; "Review - Dutch Mill on NOVA, first iteration" Oct 21 8:00–9:00 AM ET.

---
*Processed from Teams transcript on 2026-10-18*
*Source meeting: Conversion Cycle: Texas Rage Horizontal to Texas NOVA Vertical*
