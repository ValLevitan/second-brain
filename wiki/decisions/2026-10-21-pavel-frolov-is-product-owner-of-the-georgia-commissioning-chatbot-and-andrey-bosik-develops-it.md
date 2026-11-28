---
type: decision
title: Pavel Frolov is product owner of the Georgia commissioning chatbot and Andrey Bosik develops it — the machine itself calls Intralot and a chatbot answers the commissioning questions, every call is recorded, and a failed call goes to a live technician (Val, Oct 21 2026)
date: 2026-10-21
aliases: [commissioning chatbot, Georgia commissioning chatbot, chatbot for commissioning machines, комиссия чат бот, чат бот для комиссии машин, commission machine button, machine calls Intralot, Pavel product owner of the chatbot, Bosik develops the chatbot, voice over IP in the cloud]
source-count: 8
status: active
open-commitments: 4
open-questions: 2
---

# Pavel Frolov is product owner of the Georgia commissioning chatbot; Andrey Bosik develops it (Oct 21 2026)

Decided by [[wiki/people/val-levitan.md|Val Levitan]] on an ad-hoc Teams call with [[wiki/people/pavel.md|Pavel Frolov]] (Russian), recorded in two segments: 9:44–9:55 AM and 9:57–9:58 AM Eastern. See the [[wiki/meetings/2026-10-21-pavel-frolov-use-case-docs-and-commissioning-chatbot.md|meeting stub]]. Val restarted the recording only to repeat the decision: "Я хочу повторить, я сейчас включил запись" [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]].

## What was decided

- **Pavel is the product owner.** Val: "Мы назначили вас, Павел? Продукт тонором на этот… Комиссией чат батт." Pavel: "Хорошо да подходит." [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- **Andrey Bosik is the developer.** Val: "Андрея босика назначили девелопером на этот чат бот." Bosik was not on the call [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]].
- **Pavel's first work.** He may first need to define some spikes for Bosik. If they come out positive ("что я понимаю 100% позитивные"), Pavel will meanwhile write a set of capabilities for the new implementation: "нужно будет юзор краны добавить, и в Galaxy нужно будет добавить функционал" (user screens, and functions in Galaxy) [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]].
- **Why Pavel.** Val: he will be a good product owner because he is not a developer on either side, "Кроме может быть на Нижнем уровне в машине чтото" [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]].

## What the chatbot is (Val's picture, segment 1)

- **The problem.** Commissioning a machine in Georgia is a voice call. It is made by the machine owner or the technician, not by JVL. Val wants the chatbot to talk instead, because the call asks nothing the machine cannot know: "они ничего не спрашивают Того, что машина может не знать… там никто про погоду не говорит" [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]].
- **The flow.** The machine has a phone module and a button, "комиссию машину". The machine dials Intralot ("Машина набирает номер телефона интерлот"). A live person answers and asks for the machine number, the location number and other data; the chatbot answers. JVL records the call from the start. If commissioning fails, the call is forwarded to a live technician; JVL studies the call, upgrades the chatbot, and tries again on another machine. Val expects to cover all the variants "В течение там трёх месяцев" [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]].
- **Why Val thinks it works.** He has seen such a system live at a friend's company: "То есть я знаю, что это возможно" [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]].
- **Pavel's first idea, and why it fails.** Pavel suggested collecting recordings of all commissioning calls — "штук там 40 100" — to learn every case. Val: "Мы не можем их собрать, потому что это не мы разговариваем" [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]].
- **Pavel's design sketch.** It needs a voice-over-IP integration ("интеграция с войс оw IP"). The voice part can live in the cloud, where any AI and unlimited resources can be used; the machine gets only a simple API from the cloud — "дай мне свой IP, дай мне своё положение". New questions are added in later iterations [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]].

## How it sits against earlier sources

- **Evolution of the 8:02 AM wish.** At the [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md|Oct-21 Dutch Mill review]] earlier that morning Val asked for a chatbot that talks with Intralot and asked that Bosik be aimed at it. This call names the use (commissioning), the product owner and the developer — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]], [[wiki/organizations/intralot.md]].
- **Not the same as the location-owner voice bot.** [[wiki/decisions/2026-10-16-location-owner-calls-would-use-a-bought-voice-bot-service-not-one-jvl-builds.md]] covers calls to Georgia location owners through a bought service. This chatbot is a machine calling Intralot to commission itself. The sources do not link the two (**inference**: different callers and purposes).
- **Who Val first named.** In segment 1 Val said he wanted to appoint "себаша" as product manager for commissioning machines in Georgia, and at the end asked whether "собращен" is still needed as product owner; the segment ends before an answer [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]. The notes read the name as "maybe Sebastian" [[raw/Meeting_Notes_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]. Who it is stays **unclear**. Segment 2 then makes Pavel the product owner.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — define spikes for Andrey Bosik on the commissioning chatbot, if needed — due unspecified — [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — write the capability set for the chatbot build (user screens, Galaxy functions) while the spikes run — due unspecified — [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — develop the commissioning chatbot (assigned by Val; not on the call) — due unspecified — [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — review Pavel's workflow document for the voice assistant that arranges decommissioning and commissioning — due unspecified — [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]

## Open questions

- Who is "себаша" / "собращен", the person Val first named as product owner (the notes: maybe Sebastian)? — [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]] [[raw/Meeting_Notes_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]
- Pavel said he does not yet see the exact steps of commissioning ("пока не вижу чётко их чётких шагов"); Val described the call, but the full list of questions Intralot asks is not known, and JVL cannot record the calls today — [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]

**§15.8:** clear. **§15 #9:** clear — no machine, location or licence numbers were given.

## Note, Oct 23 2026 — Pavel's workflow document goes to Bosik; the bot does not shorten the wait

At the [[wiki/meetings/2026-10-23-technician-loyalty-and-developers-as-product-owners.md|Oct-23 "coffee machine" chat]] (Russian) [[wiki/people/pavel.md|Pavel]] said that the day before he prepared "документ, описывающий воркфлум в целом. И какие там есть нюансы" for the automatic assistant that calls and arranges decommissioning and commissioning, and sent it to Andrey to look at; Val: "Андрею босику" — Pavel: "Да да да" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. The notes list Bosik's review of it as an undertaking [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. Later [[wiki/people/andrey-bosik.md|Bosik]] said a voice bot calling the regulator "не сократит время декамишин" — the technician still has to wait on site; Pavel: the key is to take re-commissioning out of every case that does not need it [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. The wider plan: [[wiki/decisions/2026-10-23-to-sell-in-georgia-jvl-must-win-back-the-operators-technicians-by-making-its-machines-easier-to-service-starting-with-the-lighter-ris-in-november.md]]. Nothing here says spikes are defined or capabilities written, so Pavel's commitments stay open.

## Note, Nov 23 2026 — Val brings the bot to the NOVA team: buy the voice part, do the integration; Intralot likes it

At the [[wiki/meetings/2026-11-23-nova-sync-ip-481-root-and-weekly-mvp-plan.md|Nov-23 NOVA sync meeting]] (Russian) Val raised the bot as something "никто из вас не слышал": the call takes "гдето минут 20" by Intralot's count and about two hours by JVL's people; the bot should make the call, hand back to the technician when needed, and send a report. JVL should not design the voice technology — "У меня есть минимум одно предложение… И коз звонка $4 в час"; he knows "как минимум 3" such companies; JVL builds a good integration. "Я уже разговаривал с интерлотом, и эта идея очень нравится." [[raw/Meeting_Transcript_NOVA_Sync_IP-481_Root_and_Weekly_MVP_Plan-November-23-2026.md]]. No one was assigned at this meeting [[raw/Meeting_Notes_NOVA_Sync_IP-481_Root_and_Weekly_MVP_Plan-November-23-2026.md]], so the Oct-21 roles (Pavel product owner, Bosik developer) are not changed by it, and Pavel's and Bosik's commitments stay open. Record: [[wiki/decisions/2026-11-23-nova-is-the-one-name-ip-481-is-the-root-initiative-owned-by-biratka-one-weekly-mvp-spans-hardware-system-and-studio-and-maths-and-sound-go-into-the-brief-agent.md]].

## Sources
- [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]
- [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]

- [[raw/Meeting_Transcript_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]
- [[raw/Meeting_Notes_Pavel_Frolov_Use_Case_Docs_and_Commissioning_Chatbot-October-21-2026.md]]
- [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [[raw/Meeting_Notes_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Sync_IP-481_Root_and_Weekly_MVP_Plan-November-23-2026.md]]
- [[raw/Meeting_Notes_NOVA_Sync_IP-481_Root_and_Weekly_MVP_Plan-November-23-2026.md]]
