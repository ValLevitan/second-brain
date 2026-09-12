---
type: decision
title: No changes go into RAGE Studio — the field complaints are answered on the OMNI platform, and what gets back-ported to RAGE is decided only after the new capabilities exist
date: 2026-09-11
aliases: [no changes in RAGE Studio, everything lands on OMNI, all changes go to the new platform, back-port to RAGE decided afterwards, device not found, IO board not found, counter board not found, half an hour of work]
source-count: 2
status: active
open-commitments: 2
open-questions: 0
---

# No changes in RAGE Studio — the complaints are answered on OMNI, and back-ports come last

Val's **first** conclusion after the room finished reading his field-complaints document, at the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|Sept 11 2026 10:33 AM call]] [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## The ruling

> "Вопервых, я не думаю что… нужно делать какиелибо изменения в реййд студию… Я думаю, что все изменения должны уже лечь на омни платформу."
> — first, I do not think any changes should be made in RAGE Studio; all the changes should land on the OMNI platform.
> [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

Two things he attached to it in the same breath:

- **The change area was already agreed.** "Мы уже говорили о том, что нужно делать изменения в риз, в ремонт и нашего света" — changes are needed in RIS and in remote/network setup. *(The last three words are garbled; the derived notes read them as "the remote and setup area". Recorded as the notes' reading.)* [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]] [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- **The modems widen what is possible.** "вдобавок к этому мы ставим сейчас, вот и модам, которые… еще расширит эти возможности" — the modems being fitted now will widen those possibilities further. See [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]]. [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

## Pavel's exception, and how Val sequenced it

[[wiki/people/pavel.md|Pavel Frolov]] agreed most of it belongs on the new platform but argued some changes could ride the RAGE releases still coming, without serious engineering: "есть какието изменения, которые можно в ближайшие релизы, которые ещё для рейч будут идти… не сильно требуют какихто там серьёзных инженерных изысканий" [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

**His example was the black-screen "device not found" message** — "для нас это уже древнее Сообщение, которое там ещё на чёрном экране отображается добавить туда, что IO bord не найден или там каунтербург не найден, но это, наверное, там полчаса работы, чтоб поправить" — an ancient message that could name the **IO board** or the **counter board** instead, at maybe **half an hour** of work [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

**Val accepted the principle but not the order of operations:** "Когда мы составим новые кейпопилотис, мы определим те, которые можно перенести ещё врач" — once the new capabilities are drawn up, we will identify which of them can be carried back into RAGE. The back-port gate is the capability set, not the effort estimate [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## Where "OMNI" sits in this wiki's own naming

Val says **"the OMNI platform"**. The corpus records that on **May 12 2026** he ruled the land-based platform would stop being called Omni — a working code-word — and be named **NOVA** (see [[wiki/topics/omni-core-advancement-and-game-templating.md]], May 12, and [[wiki/topics/nova-platform-architecture.md]]). He is using the older name here. **That the OMNI he names is the NOVA programme is an inference from the corpus, not something the source says**; the word spoken is recorded as spoken.

This matters because of what he told an operator the day before — the Passport lock cannot be changed on the current platform, but the new one "will not have it", with games arriving on it from January — where the identification of that platform was flagged as an unsupported inference. Sept 11 is the first source in which Val puts a **platform name** on where this class of fix lands, though he does not say it about the Passport specifically. The Sept-10 quotations and that flag are on [[wiki/topics/ris-remote-install-and-machine-states.md]].

## Open commitments

- [ ] Unassigned — improve the black-screen "device not found" message so it names the IO board or the counter board; Pavel put it at about half an hour of work — due an upcoming RAGE release, **gated on the capability set below** — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [ ] Unassigned — once the new capabilities are drafted, identify which of them can be carried back into RAGE — due after the Monday Sept 14 session — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

*(Neither was given an owner on the call; the derived notes mark both "[Unassigned — needs clarification]".)* [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

**§15.8:** clear — platform and process only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
