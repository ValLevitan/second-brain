---
type: decision
title: The diagnostic tool goes onto the installation USB stick and lives in the SDK repository, so one stick installs or diagnoses and the tool is always current — it only reads and so is safe to hand out; sending diagnostics over the modem waits for use cases and a server side; both variants, RK (ARM, street) and FP-7 (x86, casino), are worked out
date: 2026-10-02
aliases: [diagnostic tool on the install stick, диагностик тул на флешке, one stick for install and diagnostics, diagnostic tool in the SDK repository, держать вместе с SDK проектом, не надо держать отдельный тул диагностик, read-only diagnostic tool is safe, абсолютно безопасен, modem diagnostics need a server side, серверную сторону продумывать, RK is step 2, оба варианта и RK и FP-7, Dallas firmware section, GUI reused 100 percent]
source-count: 3
status: active
open-commitments: 1
open-questions: 3
---

# The diagnostic tool goes onto the installation stick and lives in the SDK repository

Put forward and settled by [[wiki/people/pavel.md|Pavel Frolov]] on the [[wiki/meetings/2026-10-02-diagnostic-tool-on-the-install-stick-for-nova-fp7-and-rk.md|Oct-2 9:01 AM "EGMs diagnostic tool" call]] (Russian), with [[wiki/people/genadi-peari.md|Genadi Peari]] asking the questions and [[wiki/people/val-levitan.md|Val]] asking from the chat [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

## The idea

Pavel: "возникла идея, поскольку сейчас работаю над SD[K] для новой платформы под новой платформой подразумеваю и наш. Нова. Фреймворк и новые материнские платы. По базе там икс 86." Then: "**Мы всегда софт устанавливаемся с [USB-стика]. И нам ничто не мешает на этот [USB-стик] положить наш диагностик тул. Чтобы он был всегда доступен на этой флешке.**" The technician "может выбрать либо ему просто поставить текущую версию игры. Или перейти в меню диагностик тул и пройти по компонентно и проверить все компоненты, которые стоят на машине." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

**Why.** "вопервых не надо держать отдельный тул диагностик. Гдето в ну на другой флешке. Всегда доступно, если чтото идёт не так на машине, то есть чтото из оборудования не установлено или не прошито или не той версии, то это сразу можно будет продиагностировать и понять, почему не идёт инсталляция." And: "это… относится к той теме, которая озвучивал недавно [Филипп]? Что там какието ошибки вылетают на этапе инсталляции с непонятным описанием" — the install errors with no useful description that [[wiki/people/felipe-miranda.md|Felipe]] raised (by context — the RIS thread on [[wiki/topics/ris-remote-install-and-machine-states.md]]) [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

**Kept in the SDK repository, so it stays current.** "если мы эта диагностик тул будем держать вместе с SDK проектом и репозитории? Он у нас будет всегда в актуальном состоянии, то есть если мы чтото меняем [в SDK]… новый модем или нам нужно включить какойто драйвер дополнительный, то это автоматически у нас будет попадать в диагностик тул. И вот эти вот сборки из SDK линукса они у нас тоже используются каждый раз при каждой сборке игр. Каждый релиз идут. И тем самым мы будем держать актуальным. Сам диагностик тул." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

## Genadi's security question — answered: it only reads

Genadi: "если это диагностика тул попадает неправильным людям. [В] плане что то они могут украсть наши?… мы и так даём техникам да на чужим это диагностику или мы не даём?" Pavel: in the current tool "из ключевого… был опциональный раздел, там прошивки Далласа ну и то мы его там, наверное, даже не разрешали. В принципе, **если мы не даем с помощью диагностики тул никаким делать какието вмешательства в машину, то он абсолютно безопасен.** Мы всего лишь можем зайти, посмотреть, какое оборудование у нас стоит, то есть какие платы можем там зажечь светодиоды… Можем что то прочитать, проверить, работает ли?" Genadi: "Тот же [IO board] проверить?" Pavel: "Да работает ли [билл-акцептор]? Например, если он подключен, работает ли принтер?… это всё мы можем как бы на этапе ещё до инсталляции сделать." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]] (The "current diagnostic tool" is the one the wiki knows from the Georgia freeze work — IP-688 on [[wiki/topics/egm-freezing-investigation.md]]; link is context, not a citation.)

## Val's chat question — diagnostics over the modem: "теоретически можем", but it needs a server side

Pavel, reading the chat: "Вал спрашивает, можем ли мы использовать sell mode? Для Того, чтобы в процессе инсталляции… Если если чтото идёт не так. Сделать диагностику и отправить это через модем. Теоретически можем. Но эта информация попадёт кудато на сервер. Это надо ещё серверную [сторону] продумывать. Вот а то что как бы изначально предлагается это то, что видит. Техник или то, что видит человек, который устанавливает софт." ("sell mode" is read as *cell modem* — **inference** from the sentences that follow; the derived notes keep "sell mode".) [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

Genadi's next step: "ты запустил диагностик [тул] у тебя машина в принципе уже. Способна. Создать, наверное, и логи можно какието можно физически отослать, её поднял к ней можно даже подключиться, наверное… следующим шагом… Рассмотреть, как решать проблемы, Кроме диагностирования." Pavel: the modem "даёт нам какието дополнительные функциональности даже на этапе там диагностик ту[л] или на на этапе инсталляции. Но опять таки тут надо продумывать какие [use cases] мы хотим получить через [модем]. Потому что это затрагивает, ну, работу сразу с разных сторон." The use cases "может прийти из разных источников, в том числе от вас вал. Вот Андрея может быть от Филиппа" ("Андрея" — **not resolved**, see the stub) [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

## Scope, people and timing

"с моей стороны, наверное, надо пока что. Продумать. Что минимально мы можем поддержать и какие вообще шаги нам нужны? Кого надо привлечь к этому? И. Когда освобождаются ресурсы." Then: "когда освободятся ресурсы после транзакшнл, наверное, можно будет когото использовать там Того же Владимира. Наверно, чтобы график юзер интерфейс сделать ну обновлённый. Под диагностик тул в целом, наверное, то, что было сделано когдато в диагностике тул многое из бэкэнда. Там, наверное, можно переиспользовать. Больше именно новая [FP-7] материнка и какойто там график юзер интерфейс продумать ну современный под наш. Новые реалии." ([[wiki/people/vladimir-samusenko.md|Vladimir]] by context.) On the chat's point about Claude: "всё правильно с клодом… Добавить диагностик тут переписать график юзера, интерфейс. Это ну совсем не небольшая такая задача. Ну это итерационная задача. Много как бы запросов ответов от Клода, но в принципе она делается. Не очень долго, даже наверное." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

## Two products, "для записи"

"**мы говорим сейчас о 2 разных продуктах, 1 из них это RK [based], то есть на арм платформе то что для стрит машин. И это будет идти быстрее и 2 платформа [FP-7] это икс 86 платформа и в основном для казино.**" On RK: "это наверное степ 2 это всётаки абсолютно. Другая платформа, и там этот тул надо будет. По большому счету… не полностью переписываться, но процентов на 50, 60, наверное, будет отличаться от график юзаинтерфейс, наверное, может быть на 100% переиспользован." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

## The ruling

"Хорошо, если нет замечаний, тогда будем прорабатывать. [Прорабатывать] оба варианта и RK и [FP-7]." Genadi: "Очень хорошо. Спасибо." [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

In one line: **the diagnostic tool ships on the same USB stick as the installer and is built from the SDK repository, so it is always there and always current; it reads and lights, never writes, so it is safe in anyone's hands; on-screen diagnostics for the technician come first, modem-borne diagnostics wait for use cases and a server side; both the RK and the FP-7 variant are worked out, RK as step two.** The derived notes record the same two decisions and the same single undertaking [[raw/Meeting_Notes_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

## Where it sits

- It grows out of the SDK work on [[wiki/decisions/2026-09-29-the-amd-environment-is-rebuilt-from-the-rk3568-sdk-pavels-ten-day-spike-and-the-rk3576-waits.md]] — "сейчас работаю над SD[K] для новой платформы… икс 86" is that spike (Oct-2 note there).
- The platform picture is on [[wiki/topics/nova-platform-architecture.md]] (Oct 2, 9:01 AM); FP-7 on [[wiki/topics/fp7-hardware-platform.md]].
- The install errors it answers are the RIS thread's error-code complaints ([[wiki/topics/ris-remote-install-and-machine-states.md]], Oct 2, 9:01 AM).
- The Sept-7 rule that every device must show what it sees ([[wiki/decisions/2026-09-07-every-jvl-device-must-show-what-it-sees.md]]) is the Flex-side cousin of this — link is context, not a citation.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — think through the minimum the diagnostic tool can support, the steps, whom to involve and when resources free up (after Transactional), including which modem use cases to take; then work out both variants, RK and FP-7 — due unspecified — [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

## Open questions

- Which use cases for diagnostics over the modem (sending results during installation) are wanted, and who supplies them — Val, "Андрей" (unresolved) and Felipe were named as sources; a server side would be needed — [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
- Should the tool also fix problems, not only diagnose them — Genadi's "следующим шагом" — [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
- What exactly Val asked with "sell mode" — read as the cell modem (inference); the chat text is not in the transcript — [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]

**§15.8:** clear — a product idea only. **§15 #9:** none.

## Note, Oct 23 2026 — Pavel drafts the diagnostic tool with Claude

At the [[wiki/meetings/2026-10-23-technician-loyalty-and-developers-as-product-owners.md|Oct-23 "coffee machine" chat]] (Russian) [[wiki/people/pavel.md|Pavel]] said that today, with Claude, he prepared "По крайней мере драфт на диагностику… добавить диагностик тул в нашем стагер" ("стагер" as heard; read as this tool by context — **inference**) — "посмотрим, что получится" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. A first draft only; the commitment above stays open.

## Sources
- [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]
- [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
- [[raw/Meeting_Notes_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
