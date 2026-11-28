---
type: decision
title: Sebastian stops testing the Georgia modem today and finishes it on Friday from a simple checklist that Ivan makes out of his LTE-modem test plan (due the Minsk evening of Nov 26), because the modem change has no requirement with acceptance criteria yet; modem support instructions are needed anyway (how to check it works, see its state, know the data reaches the server, find problems); the South Dakota VLT build gets the new RIS but not the modem, and the next build also answers GLI's two open issues; the SD VLT RIS capabilities stay in Jira because of GLI (not moved to GitHub), and Pavel proposes one capability with one feature for merging the commits; about one week of testing is accepted (Val, with Pavel Frolov and Irina Shishko, Nov 25 2026)
date: 2026-11-25
aliases: [RIS+Modem Flex-GACOM Status update, RIS Modem Sebastian Checklist and SD VLT RIS Port, Nov 25 RIS and modem call, 75 acceptance criteria for RIS, modem checklist for Sebastian, LTE modem test plan, план тестирования л т и модема, Sebastian off the modem today, снимем его с того чтобы он сегодня проверял модем, modem support instructions, инструкции как проверять работоспособность, modem wrong requirement link, неправильная ссылка, SD VLT new RIS not modem, модель не добавляем, не для сауздаты локалити, SD VLT fixes and RIS improvements, capabilities 304-310, one capability one feature for the merge, merge into another branch, неделя, GLI two issues]
source-count: 2
status: active
open-commitments: 6
open-questions: 2
---

# Sebastian stops modem testing until Ivan's checklist; South Dakota VLT gets the new RIS, not the modem; about a week of testing (Nov 25 2026)

Taken at the [[wiki/meetings/2026-11-25-ris-modem-sebastian-checklist-and-sd-vlt-ris-port.md|Nov 25 2026, 11:02 AM "RIS+Modem Flex-GACOM Status update"]] (Russian, about 28 minutes) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]] [[raw/Meeting_Notes_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]. About minutes 0:33–6:05 were transcribed as broken English with no usable content [[raw/Meeting_Notes_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are kept as heard.)*

## 1. The Georgia modem test — Sebastian waits for a checklist

- **Val's start.** "Я вчера разговаривал с соборщивым, он сказал, что он должен был проверить 75 критерий" for RIS ("соборщивым" = [[wiki/people/sebastian.md|Sebastian]], the notes' reading; the call is [[wiki/meetings/2026-11-24-sebastian-ga-coam-acceptance-test-73-of-75-and-modem-not-tested.md|Nov 24]]). Val: "Я всегонавсего восхищен. Тем, что у него было 75. Экстерпс критерия, который должен был проверить, и мне это понравилось" — and he wants the same for the modem [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **What Sebastian checks now.** Pavel: if the machine is offline "у него выскочит окошко с кюаром. Он отсканирует кюар"; on the phone "Ему в ответ будет написано, ваш запрос принят, и после этого он может ввести активовший код." "Он сейчас не проверяет весь функционал работы вайфай. Он проверяет только то, что было запрошено. На изменение"; the change asked only for the modem, so that it could not easily be switched off [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]. That routine is [[wiki/decisions/2026-11-05-the-modem-stays-always-on-with-no-operator-on-off-screen-and-is-disabled-only-through-a-deliberate-qr-scan-server-event-and-activation-code-routine.md]].
- **No requirement.** Irina: "я вижу, у нас здесь нет требования"; there is a feature and a capability description; the link points to "не то требованието неправильная ссылка"; "Нужно сделать требования сакс критерием" (with acceptance criteria). But "Есть план тестирования, который касается л т и модема, и здесь прописаны кейсы, которые нужно выполнить" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **Why it matters.** Val does not want Sebastian to "сделал неполную работу или просто тотался на ровном месте, не знал, куда он идёт" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **Instructions are needed anyway.** Pavel: "нам всё равно для модома надо инструкции, как проверять работоспособность" — with a tool heard as "лайвсети", in the setup of the regular software and of regular games: "как увидеть, в каком он сейчас состоянии… Про диагностировать проблем." This is needed even after machines work with the modem, when "через 3 месяца к нам придут и скажут. Ваш модем не работает?" Val: "как знать, что данные, которые поступают на сервер?" Pavel: it may show how the modem should grow, "потому что сейчас он у нас очень ограниченно умеет" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **The ruling.** Val: "давайте может быть снимем его с Того, чтобы он сегодня проверял модем. Допишем ему инструкции, которые нужно, когда он в пятницу вернётся на работу. Он сможет это доделать?" — "Договорились." Pavel: "Инструкции попросим написать 1 вариант Ивана." Irina: the test plan just needs to become a list convenient "для Себастьяна и ещё для кого то"; [[wiki/people/ivan.md|Ivan]] has it and worked from it. It was already 8 PM in Minsk, so Val: "Ваш вечер завтра пусть иван отправит" the checklist [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].

## 2. South Dakota VLT — the new RIS, not the modem

- **RIS in.** Val: "Я предлагаю добавить туда рис. Это большие хорошие инструменты, которые очень полезны." Pavel: "Да, хорошо" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **Modem out.** Irina asked "и модем тоже"; Val: "Я говорю, модель не добавляем." Irina, on GLI certification: a machine without a modem — "Функционал, который им проверять не нужно." Pavel: GLI may look into the code; Irina: "мы им скажем, что этот функционал не для сауздаты локалити. Как обычно." Val: "Я я бы не добавлял в моем. Но араяс я бы добавил бы" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **GLI's findings.** Irina: "Мы часть починили, мы с ними согласились. Вот 2 ошибки мы им попросили. Это самое нам дать больше информации"; GLI was slow "но уже начали это самое отвечать"; "там не очень понятно, что реально есть ли это проблема." So "нам нужно сейчас добавить RS. И вот ответ на вот эти 2" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]. GLI: [[wiki/organizations/gli.md]].

## 3. Where the work sits, and how much of it

- **Jira.** There is a release for SD VLT fixes with RIS improvements (Irina, as heard: "сдавил те фиксы сент рис о"); its capabilities run "304 тире 310" ("Ну до 10"). They have no features: "женя их туда ещё не переносил"; Pavel: they were created after an earlier meeting "Но дальше не пошла" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]. "женя" = [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], who does the RIS work (**inference**; the notes say "Evgeny").
- **Not to GitHub.** Val asked whether to move them to GitHub. Irina: "это не переносится это джелай Да да, это принципиально ставили там" — placed there on purpose for GLI. Val: "Окей, хорошо… разница не очень" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]] [[raw/Meeting_Notes_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **One capability is enough (Pavel's proposal).** Irina: "это уже будет не реализация, просто это самое он смержит. Все изменения, которые касаются этих фич в другой бранч". Pavel: "это избыточное такое количество капобилитис на эту работу"; one capability to apply the RIS improvements to SD, one feature "на перенос этих. Камитов", then testing "для вани, чтобы проверить, что для этой версии то же самое отработало." Val: "Друзья меня устраивает любой вариант… это промежуточный вариант" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]. Pavel will plan these capabilities on the Minsk side [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].
- **About a week.** Irina: Kharetski moves the changes "сразу, как только скажет"; testing "я скажем так, сказала бы неделя", because "То, что проверял на джорджии, нужно сейчас проверить снбот на с двлти" and GLI must go through it again — "это если всё гладко идёт эта неделя." Val: "Хорошо неделя" [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]].

## How it sits against earlier rulings

- **Nov 23 / Nov 24 — the Georgia modem field test.** On Nov 23 build 4377 with the modem was to be tested by Elizabeth and Sebastian on different modems before the lab; on Nov 24 Sebastian had not tested the modem and expected another half day or day. On Nov 25 he is taken off it until the checklist — **evolution**; noted on [[wiki/decisions/2026-11-23-the-20-revision-2-boards-go-back-to-alekseev-for-repair-build-4377-with-the-modem-is-field-tested-on-different-modems-before-the-lab-and-remote-updates-and-wi-fi-setup-are-the-two-must-haves.md]].
- **Oct 6 — the RIS line for Georgia.** The RIS MVP 1 changes were built for Georgia only — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]]. On Nov 25 the RIS improvements are to be merged into the South Dakota VLT branch too — **evolution** (the wiki reads it as an extension, not a reversal).
- **Oct 6 — "every machine ships with a modem."** That ruling's market is not named in its title; South Dakota VLT now goes without the modem. Whether these conflict is **unclear** — [[wiki/decisions/2026-10-06-every-machine-ships-with-a-modem-and-customers-are-told-reports-are-free-for-a-limited-time-with-an-opt-out.md]] (queued for the owner, not resolved).
- Project record: [[wiki/projects/south-dakota-vlt-market.md]] (Nov 25); RIS topic: [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 25).

## Open commitments

- [ ] [[wiki/people/ivan.md|Ivan]] — turn his LTE-modem test plan into a simple checklist for Sebastian and send it — due Thu Nov 26 2026, Minsk evening — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [ ] [[wiki/people/sebastian.md|Sebastian]] — finish the Georgia modem test from the checklist — due Fri Nov 27 2026 (back at work) — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — have modem support instructions written (check it works, its state, data reaching the server, diagnose problems) — due unspecified — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — plan the SD VLT RIS capabilities on the Minsk side (possibly one capability, one feature) — due unspecified — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] ("женя" — **inference**) — merge the RIS-improvement commits into the SD VLT branch — due as soon as asked — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [ ] [[wiki/people/ivan.md|Ivan]] ("ваня") — test the SD VLT build with the RIS changes — due about one week — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]

## Open questions

- Are GLI's two open South Dakota issues real problems? GLI has started to answer — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- Which requirement, with acceptance criteria, belongs to the Georgia modem capability? The current link is wrong — [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]

**§15.8:** clear. **§15 #9:** clear — capability numbers only.

## Sources

- [[raw/Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
- [[raw/Meeting_Notes_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026.md]]
