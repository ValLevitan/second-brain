---
type: decision
title: The AI PM keeps its 0.80 confidence threshold for creating Jira tasks; instead of lowering it, meetings must get more concrete and give the PM clear instructions (Val, Oct 14 2026)
date: 2026-10-14
aliases: [keep the 0.80 threshold, порог 0.80, порог 0,80, не понижать порог, AI PM confidence threshold, meeting rigor over a lower threshold, Keep 0.80 Threshold and Meeting Rigor, more concrete meetings for the AI PM]
source-count: 6
status: active
open-commitments: 2
open-questions: 0
---

# The AI PM keeps its 0.80 threshold; meetings get more concrete instead

Set on the [[wiki/meetings/2026-10-14-ai-pm-keep-the-0-80-threshold-and-meeting-rigor.md|Oct 14 2026 AI PM update]] (10:03 AM, Russian) by [[wiki/people/val-levitan.md|Val Levitan]], with [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]] on the call [[raw/Meeting_Notes_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]. Which of the two said what is not marked in the sources. The whole picture is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]].

## What was decided

Do not lower the AI PM's threshold for now. Instead, ask the people in meetings to discuss the problems that need tasks more concretely, and to instruct the PM more clearly. Val: "Хорошо, оставим порог там, где он есть сейчас, и просто толкнем наших. Поможем нашим людям, подскажем им на месте, что конкретика у нас слабоватая." [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]

Speaker 2 agreed: "Не лишено смысла. Я соглашусь с этим абсолютно. Давайте так и сделаем." [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]

## What the threshold is

Speaker 4 explained it when Val asked. Each phrase or fact gets a score. The threshold is set at 0.80: at or above it the item is treated as reliable, and either a task is created or a decision is recorded. Below it (0.75, 0.7, 0.65) nothing is done. Some items scored 0.75 and "совсем чуть-чуть не попал" [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].

## Why the question came up

Speaker 2 reported that so far, in Jira, the agent had only written comments and created one task. The team was thinking of lowering the threshold so it sends more to Jira. They first wanted to collect more material, decide what really should have gone to Jira, and set new criteria from that [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].

## Val's reasons

- **Even a good human PM needs to be told.** Even a free project manager who understands everything sometimes needs to hear "мы решаем, что вот это нужно сделать", and then he goes and does it [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].
- **The main cause is the meetings, not the bar.** A high threshold may be one reason, but Val thinks the main reason the PM opens few tasks is that the team does not talk concretely about them. He listened to some recordings and believes the meetings are run "размыто и неподготовленно и без определенного фокуса" [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].
- **The bar can push people.** If the threshold stays and people see they must be more concrete, this may push them to prepare more deeply for meetings and agree better on concrete things [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].
- **He did not argue the number.** "я не стану сейчас спорить, как это высокие или невысокие… Мне лично не нравится, как проходят митинги, поэтому я я попросил бы, пока порог не трогать." [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]

## How this fits earlier state

- On Oct 8 Bosik said the Listener's rules are strict, unsure items go to an internal draft document, and the thresholds may be lowered later — see [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]. This decision holds the threshold where it is for now. "пока" (for now) is Val's word; no review date was set [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]].
- The same morning, at the Oct-14 Minsk stand-up, Kovalchuk said "у него сейчас гайки закручены" — the agent hesitates before creating anything in Jira [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]. That this is the same 0.80 bar is an **inference**.
- It matches Val's Oct-8 principle that one clear position beats "разжижению бульона" (link drawn here — **inference**; see [[wiki/people/val-levitan.md]], Oct 8).

## Open commitments

- [ ] Speaker 2 (Kovalchuk or Bosik — not marked) — take Val's comment to the people who can influence meeting quality: be concrete, prepare, instruct the PM clearly (Val: "Вы это замечание доведете до людей, которые могут на это повлиять") — due unspecified — [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]] [[raw/Meeting_Notes_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]
- [ ] Speaker 4 (Kovalchuk or Bosik — not marked) — later, review the saved scores to see what missed the threshold and why ("вся запись хранится, у какого предложения какой порог"); proposed, not dated — due unspecified — [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]

**§15.8:** clear — no pay matters. **§15 #9:** none.

## Note, Oct 15 2026 — at the stand-up: address the agent directly

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 Minsk stand-up]] Khamin said the feature he had asked for the day before was not created by the agent. [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]: "чтобы агент чтото создавал, его нужно напрямую спросить" — say "создай мне вот это". Asked whether the agent ignores a need it only notices in passing, he said it scores how true each statement is "и всё, что ниже порога в 00:08 он не не воспринимает" — "это никуда не попадает" [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]. The notes read the threshold as 0.80 [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]; that it is the same bar as this decision is an **inference**. This matches Val's line here: the meetings, not the bar, must change.

## Sources
- [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
