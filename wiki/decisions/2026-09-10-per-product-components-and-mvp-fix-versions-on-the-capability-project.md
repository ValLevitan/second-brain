---
type: decision
title: Capabilities get per-product components — FlexPay, Flex-IQ, FlexPort, Terminal Hub — and MVP fix versions, so the one undifferentiated pile can be filtered
date: 2026-09-10
aliases: [components in the capability project, FlexPay Flex IQ FlexPort Terminal Hub components, cloud services not split out, fix versions for MVP 1 and MVP 2, all the requirements and capabilities dumped in one pile, hang the capability on the product project, filter only works by reporter]
source-count: 4
status: active
open-commitments: 2
open-questions: 1
---

# Per-product components and MVP fix versions on the capability project

Settled by the Minsk transactional group at the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept 10 2026 5:31 AM call]], in Russian, without [[wiki/people/val-levitan.md|Val]]. It is the practical answer to the filing problem that [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md|the capability level]] created and that the [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md|Sept-9 delegation of planning to Bosik and Kovalchuk]] made urgent — the capability count is growing fast and nothing in Jira distinguishes one product's capabilities from another's. [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## The problem, as stated in the room

- **One pile, and a filter that only works by reporter.** [[wiki/people/pavel.md|Pavel Frolov]] put a Jira filter of recently-created capabilities on screen and tried to widen it by date. [[wiki/people/irina-shishko.md|Irina Shishko]]: "[в]от это вот очень неудобно, что все эти… требования[ и капа]билити в одной куче свалены" — everything dumped in one pile — and the filter catches anyone who merely changed the reporter: "[е]сли где[-]то что[-]то поменяли[,] репортёра[,] и всё" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **Widening the date range does not help.** Pavel tried 20 days, then 25 — "[н]у давай, допустим[,] 20 дней… [о]н слишком много добавит" and "если 25 дней, там всё[-]таки всё равно не всё попадает" — and concluded "[н]адо какой[-]то маркер было бы" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **You cannot tell from the text which product a capability belongs to.** [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], looking at it from outside: "я бы либо маркеры добавлял, либо сделал… одинаковое нам[еновани]е, чтоб можно было разделить fl[e]x pay[,] flex i[q]" — because "читаешь[,] там[:] контроллер работает[; в]от к чему это [капа]билит[и] идёт[?]" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **How many projects are actually in play was not pinned down.** [[wiki/people/alexander-biratka.md|Alexander Biratka]] counted three, then four once cloud service implementation was added; Pavel: "[д]а[,] как минимум 4, а может даже пять[-]шесть" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].

## What was decided

- **Components will be created in the capability project, and they are per product.** Biratka asked whether the component column could be used — "там колонка есть компонент[,] наверное[,] да?… может[,] отметить[,] но каждый ка[паб]илити[,] к чему это относится" — and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] confirmed that components do not yet exist and must be made: "[и]х нету[,] [П]аш… [и]х надо создать[,] в проекте кап[…]" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **The component list: FlexPay, Flex-IQ, FlexPort, and a Terminal Hub.** Irina: "мы хотим просто либо флекс[а ай]кю[,] либо флекспей[,] либо флекс[…] порт"; Biratka added "[л]ибо там терминал хаб какой[-]нибудь"; Pavel agreed. Irina described the intent as components "типа flexpay[,] flex i[q]" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **Cloud services are not broken out as a separate component for now.** Pavel: "[к]лауд[-]сервис пока не выделяю" — after Irina warned they could otherwise breed components by the tonne: "а то мы можем тут их тоже наплодить тонну… [н]ужно ли это?" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **A capability hangs on the product project; the engineers pick the repository afterwards.** Chudinov's guidance, which settled the question: "лучше вешайте [капа]билити на… проект[ —] это флекс[-]а[й]кю [ли]бо флекспей[,] а дальше уже[…] [и]нженеры решают, на каком репозитории надо[,] и… можно ли и возможно ли это изменять" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]].
- **Fix versions are created for the MVPs.** Pavel: "[в]от фикс вер[ш]ен[,] наверное[,] нам надо завести и маркировать фикс верш[е]н[ом]", and later, naming them: "надо будет завести как минимум MVP один[,] MVP 2[,] транзакш[е]н[ ]один[,] транзакш[ен] 2." He took the job himself — "я тогда создам фикс[ ]вер[ш]ен для [MVP 1 и] VP 2" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]. *(The derived notes gloss this as fix versions "named per product rather than just '1.0'" and as Pavel's view that fix versions are the only clean way to separate MVP from non-MVP. Neither the per-product naming rule nor the "only clean way" framing is spoken in this transcript — both are stated on the [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md|Sept 9 call]] instead, so the notes appear to carry them over. Recorded here as the notes' gloss, not as Sept-10 speech.* [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]*)*

This advances, but does not fully close, the open question carried on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] — how MVP 1 and MVP 2 are separated in Jira. Pavel's fix-version route is now being built; Irina's rival proposal (use the capability status) is not mentioned in this source.

## Update, Sept 24 2026 — the MVP is a release, never an initiative

At the [[wiki/meetings/2026-09-24-nova-galaxy-jira-hierarchy-cleanup.md|Sept-24 10:00 AM call]] (Russian), [[wiki/people/irina-shishko.md|Irina Shishko]] showed that the transactional team had also made a second initiative, **IP 1202** beside **IP 1199**, so MVP 1 (ending October 1) and MVP 2 (ending October 29) could be seen apart. [[wiki/people/val-levitan.md|Val]] was "категорически против" release-named initiatives: a release is a vertical line on the timeline, and MVP 1 is found by a release filter. [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]: "фильтром фильтровать по релизу, выбрать м VP один". This keeps the fix-version route of this decision and rules out the initiative route. See [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]]. [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

*(The per-product component idea of this page is not mentioned on Sept 24; Val instead pointed to project filters, since each product has its own repository and project.)* [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — create the components in the capability project. He asked for the list in writing so he could do it fast: "[в]ы можете мне список скинуть, я посо[зд]аю быстро… [в] чатик напишите[,] я создам" — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — post the component list into the meeting chat, then go through the capabilities and tag them; she put it at about an hour out because she was on something else: "[н]о сделаешь компоненты[,] я могу это пройтись, подобавлять их в эти самые [капа]билити примерно через час, потому что я сейчас на[…]" — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [x] [[wiki/people/pavel.md|Pavel Frolov]] — create the MVP 1 and MVP 2 fix versions in Jira — due September 10 2026 — **discharged Sept 11 2026**: he opened the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 call]] reporting "в спейсе продакт cap[a]bility создал 2 релиза[ —] транзакш[е]н MVP один и транзакш[е]н [M]VP 2", dated October 1 and October 30, with [[wiki/people/irina-shishko.md|Irina Shishko]] confirming the equivalence on screen — "это релиз[,] релиз равно фикс верш[е]н здесь получается" — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The component half of this decision was **not** confirmed done a day later: on Sept 11 Pavel was still describing the Component tagging as the thing they agreed to do — "мы просто промаркируем вот то, что везде сейчас прописано flexpay… мы добавим туда, что это флекспей" — so Kovalchuk's and Irina's commitments above stand open.)* [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **Can more than one component be assigned to a single capability?** Pavel asked — "компоненты же мы можем только один выбрать, да или нет?… [н]е[ ]несколько мы можем выб[рать]?" — and Irina did not know: "[п]одожди, я не знаю насчёт несколько" — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

**§15.8:** clear — tooling and process only.

## Sources
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
