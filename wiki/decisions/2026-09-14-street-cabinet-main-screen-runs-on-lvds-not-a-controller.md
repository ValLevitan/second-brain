---
type: decision
title: The street cabinet's main screen runs on LVDS with JVL's own cable and adapter; the optional second screen keeps HDMI and a controller
date: 2026-09-14
aliases: [LVDS main output, street cabinet screen connection, save the controller, controller costs 35, our own cable our own adapter, only Full HD, вложится в тысячу долларов, Flex S screen, forty nine after 43]
source-count: 5
status: active
open-commitments: 0
open-questions: 2
---

# The street cabinet's main screen runs on LVDS, not through a controller

Settled at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept 14 2026 12:04 PM call]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]]. It belongs to the [[wiki/topics/low-cost-street-machine.md|low-cost street-machine]] programme — the machine Val opens as "**флекс эс это стрит машина**" (Flex S, the street machine) [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## What was decided

- **Main screen:** LVDS straight to the board, driven by **JVL's own cable and adapter**, with no bought-in controller.
- **Second screen (optional):** HDMI, with a controller — the arrangement already used on Flex IQ.
- **Consequence Genadi stated and nobody challenged:** "**Только фулл эйч ди мы зашиваем**" — only Full HD gets locked in [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

[[wiki/people/pavel.md|Pavel]] read the decision back in his own words: "**решение, тогда что [LVDS] постараться сделать основным? Чтобы сэкономить на контроллере. И делать именно на своём контроле это… на своих кабелях и переходниках**", and then "**А у опциональный 2 экран это тогда уже h dmi. С контроллером**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The transcript renders "LVDS" several ways — "лв д с", "илвик", and, in Genadi's key sentence, "**у людей с**". They are all speech-to-text renderings of the same three letters; read in context, an **inference**, and the rendering is left as-is inside the quotes.)*

## The money, as spoken

[[wiki/people/genadi-peari.md|Genadi]] did the arithmetic out loud: "**Так контроллер стоит 35, по моему так будет стоить наш кабель, наш адаптер. Это всё будет стоить 15, 20. Ну как мы с экономия раунд 15 $20 да?**" — the controller costs about $35; JVL's own cable plus adapter would cost $15–20; so the saving is around **$15–20** per machine [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

He was not enthusiastic about it himself: "**Как это не не эффективно, верно сразу**" — this is not efficient [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## Why Val fixed it anyway — the reason is irreversibility, not the $15

Val's argument was that the choice will not be revisited once made, so it has to be made now rather than left open: "**А если мы уже пойдём в одну сторону в какуюто сторону выберем, можем менять не будем это… Окончательно**" — if we go one way, we will not change it; definitively [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

And the cost target is what makes $15–20 worth locking: "**Да, потому что идея вложится в тысячу долларов**" — because the idea is to fit inside **a thousand dollars** [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**That $1,000 is a tighter build target than the corpus previously carried.** The June-8 2026 framing was a whole device under **$2,000** including the bill acceptor, leaving the machine itself around **$1,200**; the June-16 session set a **$5,000** sell price. The September figure is the current build target and supersedes the ~$1,200; the $5,000 sell price is a different number and is untouched. [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]] [[raw/Meeting_Notes_Street_Cabinet_Design_Direction-June-16-2026.md]]

## What it reverses

The **July 29 2026** board review reached the opposite preference: "One video interface is LVDS (**impractical**); the team prefers a board variant with **2–3 uniform HDMI outputs**" [[raw/Meeting_Notes_RK3588_Game_Performance_Findings-July-29-2026.md]]. Seven weeks later LVDS becomes the main output by choice, on cost grounds, for this machine.

Recorded as **evolution, not contradiction** (§11): different dates, a later source superseding an earlier preference, with the July position preserved above. Nobody on the Sept-14 call refers back to the July view.

## The screen-size constraint that frames it

Genadi raised the size question in the same passage, unprompted, as a budget warning: "**учтите, что если мы будем 43 [inch] а монитором идти вверх. Это будет у нас только 4 кей… а 4 кей и [LVDS] мы не сможем тянуть на этой [board]. И поэтому… там очень сильно вырастает цена на тачскрин это некс это форти найн после 43**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

- At **43 inches and above**, the panels available are **4K only**;
- the board cannot drive 4K;
- and the touchscreen price **rises sharply** past 43, because the next size up is **49**.

This is the first hard constraint in the corpus on the **43–49 inch** range the June-16 session had left open ("exact screen size… final pick depends on cost sourcing"), and it pushes toward the bottom of that range. [[raw/Meeting_Notes_Street_Cabinet_Design_Direction-June-16-2026.md]]

## How the second screen is wired

Genadi described it by analogy rather than by specification: the second screen is "**та же тот же вариант, как мы сделали [на IQ]. То же самое. Берется наш, мы делаем себе адаптер, как нам удобно**" — the same arrangement as on IQ, with JVL's own adapter [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]. *(The transcript renders the product as "**найки**"; read as "на IQ" — an **inference** from context, and the reading the derived notes also take.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

Pavel's original question — which the decision answers — was whether a board sits in between or whether "**это сразу от китайцев будет идти экраны с контроллерами, чтобы [LVDS] сигналом подключаться к плате? И подсветка, чтобы работала**" — screens arriving from the Chinese suppliers with controllers already fitted, and the backlight working [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## Open questions

- **Can LVDS in fact drive the main screen?** It is agreed as the direction and not proven; Pavel's own wording is "**постараться сделать основным**" — *try* to make it the main. The derived notes list the same question — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- **What screen size does the machine actually get?** 43 inches is the practical ceiling on this reasoning, but no size is chosen in the source — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**§15.8:** clear — component and build-cost economics only; no named-person compensation appears in either Sept-14 12:04 file.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- [[raw/Meeting_Notes_Street_Cabinet_Design_Direction-June-16-2026.md]]
- [[raw/Meeting_Notes_RK3588_Game_Performance_Findings-July-29-2026.md]]
