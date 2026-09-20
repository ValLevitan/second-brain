---
type: decision
title: Nobody downloads and installs builds by hand — Val kills the manual build-delivery request outright and sets a 30-day target for the environment that does it automatically, with Flex-Port the known gap
date: 2026-09-14
aliases: [stop downloading builds, 30-day target, automatic build environment, FlexPort cannot be updated remotely, скачивать неправильно, build delivery process, remote update gap]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# Nobody downloads and installs builds — 30 days to finish it

The first exchange of the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]], and the one place [[wiki/people/val-levitan.md|Val Levitan]] cut a request off mid-sentence.

## What was asked for

[[wiki/people/andrei-klimovich.md|Andrei Klimovich]]'s second agenda item was build delivery: as soon as anything is testable he wants regular builds, tested, with feedback, as a standing process — "чтобы у нас это был постоянный процесс." He was explicit that he could handle the mechanics himself: "ссылка[,] доступ к гиту у меня есть[;] я могу всё сам скачивать, устанавливать, но мне нужно с вашей стороны хотя бы краткий список того, что вошло в этот билд" — he only wanted a short list of what went into each build [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Val's answer

> "**Я прошу прощения, это невозможно… Я не хочу, чтобы мне чего скачивали и устанавливали. Я бы хотел бы, чтобы Босик установил [environment], который это делает сам.**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

When Klimovich answered that the task already exists as remote update inside a capability *(he names a number the transcript garbles as "05:01"; not asserted here)*, Val rejected the framing rather than the plan: "**[н]ет, нет, нет, я думаю, что вы всё[-]таки не понимаете меня. Скачивать неправильно, и мы не хотим это делать… [п]оэтому давайте мы быстрее пойдём к тому, что мы не будем скачивать.**" He then made it Klimovich's own job — "**ваша задача[ —] чтобы не заставить нас… скачивать[;] вот это главное**" — and set the clock: "**[о]кей, давайте поставим себе задачу сделать в течение 30 дней, хорошо?**" Klimovich: "[я] только поддерживаю" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The state of play the ruling was made against

- [[wiki/people/andrey-bosik.md|Andrey Bosik]]: the automatic environment is nearly there — "[н]у у нас уже оно почти готово."
- [[wiki/people/pavel.md|Pavel Frolov]] narrowed it immediately: "**[п]ока что не всё готово[,] пока что мы не умеем обновлять Флекс[-]порт… [п]оэтому Флекс[-]порт придётся пока что скачивать и ставить, как ставили раньше**." Bosik agreed the port is the exception [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Remote update was already pulled into MVP 1 three days earlier, along with the Flex-Port master-device half of remote firmware update — see [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]. What is new here is that **manual download-and-install is now forbidden as a working practice, not merely scheduled away**, and that the port is named as the remaining gap.

*(Inference, not stated in the source: a 30-day target set on Sept 14 lands around Oct 14 — after the October-1 first installation. Nobody on the call reconciled the two dates.)*

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] and [[wiki/people/pavel.md|Pavel Frolov]] — finish the automatic update environment so nobody has to download and install builds by hand, **Flex-Port included** — due within 30 days of Sept 14 2026, the target Val set on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes record the same exchange and the same 30-day target, and attribute the FlexPort correction to Pavel Frolov.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — engineering practice only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
