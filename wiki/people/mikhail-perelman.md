---
type: person
title: Mikhail Perelman
date: 2026-07-13
aliases: [Mikhail Perelman, Misha, Миша, Mikhail, Michael]
disambiguation: "Procurement Manager (parts/vendors/shipments; the retrofit-lead "Misha"). Misha/Michael cluster (2, owner-ruled): [[wiki/people/michael-gottlieb.md|Michael Gottlieb]]=Senior VP Game Design / [[wiki/people/mikhail-perelman.md|Mikhail Perelman]]=Procurement Manager (the "retrofit Misha"). Resolve by context; queue if none."
source-count: 24
open-commitments: 5
open-questions: 3
---

# Mikhail Perelman

Mikhail Perelman ("Misha") is JVL's **Procurement Manager** (owner-confirmed 2026-07-13). On the used-machine retrofit he owns the parts side — deciding what to order and sourcing it. Owner ruling: the "Misha" who leads the retrofit is this person (the retrofit-lead mentions are attributed to him), and he is **distinct** from [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] (Senior VP of Game Design); resolve by context — procurement/parts → Perelman, game design → Gottlieb.

## Role

- Worked through the retrofit plan with Val — what parts to order and how to rebuild each machine type. [[raw/retrofit_january_7_2025.md]]
- Tracks practical parts-sourcing problems, e.g. 30-inch monitors for the Maple cabinets and whether they can be bought reliably from China/Alibaba. [[raw/retrofit_january_7_2025.md]]
- Reported that a former supplier ("Angus"/"Akira") can no longer supply those large monitors. [[raw/retrofit_january_7_2025.md]]

The transcript is in Russian; his name appears as "Миша."

## Apr 28 2025 — purchasing bill-of-material; HS tracking

On the BC status call ([[wiki/meetings/2025-04-28-business-central-labs-tariffs-status.md]]) Val wants **Michael (Perelman) focused only on purchasing bill-of-material** items (with [[wiki/people/mary.md|Mary]] handling non-BOM POs like GLI). Lev believed **Michael had been tracking HS numbers / country-of-origin** for imports — now the pressing task to formalize on the vendor card. See [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/business_central_update-apr-28-2025.md]]

## June 24–26 2025 — procurement lead on the manufacturing move to Georgia

On the manufacturing-relocation sessions ([[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]) Perelman ("Misha"/"Michael") owns the procurement/logistics side of moving assembly from Canada to the new Louisville, Georgia warehouse. His tasks: find **subcontractors** for the warehouse electrical + pneumatic wiring; source an **electric pump truck**; travel to Georgia with [[wiki/people/genadi-peari.md|Genadi Peari]] (~2–3 weeks) to examine the warehouse and meet an electrician, a pneumatic company, a **metal fabricator**, and a couple of operator locations; push all supplier **quotations to DDP (Delivered Duty Paid) into the US** and begin placing destination-Atlanta orders (~30 days out); and obtain competitive quotes from **American manufacturers**. He needs **Business Central** access for JVL Systems (with Gennady) and confirmed there are ~**100 sets of Flex** whose components ship to Georgia. He agreed a trip "makes sense." [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## July 3 2025 — relocation execution status (vendors + Georgia warehouse layout)

On the July-3 alignment review ([[wiki/meetings/2025-07-03-procurement-relocation-georgia.md]]; Russian) Perelman reported progress a week after the June-24/26 decision, with Val pressing that "nothing has moved." His sourcing status: he had a **list of four US metal fabricators** to contact Monday (using Gena's drawings); monitor quotes from the California distributor **bySearch** (~7-year supplier — no clean quote yet) and **Alpha** (21.5"/27" — showing ~$70/monitor tariff, ~70–90% of the ~$95–100 unit cost, under DDP), with the **43"** still unquoted; upcoming meetings with **StarTech** (a Chinese LCD manufacturer with an England facility, Jul 10) and **General Touch** (touch screens, Jul 7); **power supplies** bought through a US distributor (MeanWell/Sagir); **PC/CPU boards** stocked through September with two China sources (**Nika** + a cheaper newer one). On the warehouse he mapped racking options (11 racks along the slanted wall / ~44 skids vs a perpendicular ~21-rack layout, 15-ft height, 12-ft forklift aisles). Val's direction: get a **used-racking company** to lay it out from a drawing, and — the recurring frustration — **copy Val and Genadi on all vendor correspondence** and send **everyone a DDP-quotation request**. See [[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]] and [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/procurement_production_relocation-july-3-2025.md]]

## May 11 2026 — material-requirements report to be delivered via the BC MCP

On a [[wiki/people/val-levitan.md|Val]] / Perelman / [[wiki/people/lev-rudky.md|Lev Rudky]] call ([[wiki/meetings/2026-05-11-bc-material-requirements-mcp.md]]) Misha, as procurement manager, spelled out the material-requirements (MRP) report he wants — the one-click Navision report Anatoly built him, which the standard Business Central report does not reproduce. His model: input a part/subassembly/machine with a target quantity; get a **consolidated shortage list** (one row per unique part, netting stock + on-order + in-transit) enriched with **vendor + last price + minimum order quantity**, grouped by vendor for POs, plus a per-subassembly side-list for cross-checking. Today he builds the consolidation himself in an **Excel pivot table** on top of the BC export. Val proposed delivering it not by modifying BC but through the **BC MCP layer** (Claude doing the consolidation/enrichment in one step), and made Misha the canonical **"procurement manager" persona** for the requirements Val will draft from the transcript + Misha's example Excel. Misha to send the Excel sample immediately. Substance on [[wiki/topics/business-central-erp-implementation.md]] (May-11). §15.8 clear. [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]] [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]

## Aug 12 2026 (in absentia) — the purchasing lag, and where an agent would fit

On the [[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug-12 Val–Genadi hardware-standard session]], Genadi gave a live example: he had told Misha that a quotation for 43-inch touch screens for the next month had come in, a week had passed and the PO approval had not been sent — "it's between chairs and there's no one to remind them". Val's picture of the fix: a purchasing agent with access to Business Central prepares all the purchase orders and Misha gets approval rights to release them. Genadi also said he had raised a missing bezel with Misha because of an upcoming show. **§15.8:** Val's personal remarks about Misha in the same passage are withheld. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Sept 4 2026 — the China route for the Flex-Slim brackets, and the 100-Flex-Port order

Two procurement threads on the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept-4 midday production call]], both routed through "Миша" — resolved to Perelman by the procurement/parts/vendor context (§4) [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]:

- **The Flex-Slim brackets and harnesses go through him to China.** [[wiki/people/genadi-peari.md|Genadi]]: "что Миша может сделать… В Китае попросить за неделю сделать и прислать самолетом. Скажем, 10 [се]тов… ну в лучшем случае 2 недели." Val took China and told Genadi to ask for a rush through him: "Я бы хотел бы, чтобы вы попросили их… [через] Миша… Они всегда идут навстречу, им только нужно сказать." Ruling: [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]].
- **He is also the one to start ordering the harnesses for 100 Flex-Ports.** Genadi had spent time the previous day pushing him and [[wiki/people/elizabeth.md|Elizabeth Palomino]] to move that order — "чтобы она пошла, посчитала, чтобы он харнес[ы] начал заказывать" — and expected "Миша должен… маленькие какието заслать [orders]" for the Flex-Port SAS harnesses too.

## Sept 14 2026 — Val names him as the man who controls the RK3576 supply

At the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept-14 12:04 PM hardware call]] Val wanted the new compute boards moved: "**Значит, нам нужно срочно нажать на поставку RK 35 76 Минск. И это кто это контролирует? Это миша контролирует. Миша перельман**" — he asks who controls it and answers himself, **by full name**, which is unusual in this corpus and removes the normal §4 ambiguity [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

[[wiki/people/genadi-peari.md|Genadi]] did not know the order's status — "**я не знаю статус… Этот инвойс… вышел[?] я не знаю**" — then read the figures off his screen: supplier rendered "**тач, интеллигент**" (Touch Intelligent, name uncertain), about **$300 plus shipment**, "**3 секси чтото**" (three sixty something) all in, being **2 samples at $150** and about **$65 freight to Minsk**. Full record on [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**A second shipment on the same call, this one to Belarus.** Asked where the arrived validator/recycler had landed, Genadi's reply is mostly garbled but carries "**миша организовывает [ship]м[е]нт в Белоруссию**" — Misha organising the shipment to Belarus. Same procurement/shipment context, resolved to Perelman the same way (§4) [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**§15.8:** clear — freight and component cost only.

## Open commitments (Sept 14 2026)

- [ ] Mikhail Perelman — push the RK3576 delivery to Minsk (2 samples, ~$300 plus ~$65 freight) — due urgently. *(Val names him as the person who controls it; the transcript does not record the instruction being given to him or accepted, and the derived notes flag the same gap.)* — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sept 23 2026 (11:05 AM) — named on the morning alignment call

On the [[wiki/meetings/2026-09-23-texas-flex-slim-release-street-cabinet-and-bom-source-of-truth.md|Sept-23 Val–Genadi call]], Genadi said he did not see Mikhail moving on the Georgia order and asked whether Val had told him to wait. Val said no: Mikhail had issued many purchase orders ("прочих сордеров"), which Val signed, but Val is managing cash. He wants the suppliers' terms negotiated so that the release or the payment can move, because "там везде стоит предоплата". He said he would try to sit with Mikhail that day and go through the signed orders to decide what to pay. *(That the 1:02 PM walkthrough below is that meeting is an inference.)* [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]

**§15.8:** Val's remarks on this call about how Mikhail deals with suppliers are a personal performance judgement and are **withheld**.

## Sept 23 2026 — the open purchase-order walkthrough: who gets paid now

On the [[wiki/meetings/2026-09-23-open-purchase-order-payment-walkthrough.md|Sept-23 1:02 PM call]] Val and Misha went down the file of open purchase orders, vendor by vendor, with [[wiki/people/genadi-peari.md|Genadi]] joining in. Val's aim was triage, not an audit: "Я пытаюсь найти меньше работы для себя." Misha: "Я тоже так хочу." Vendor names and figures below are as spoken; the transcript garbles many of them [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].

- **Mold payments that are late.** One line was a mold order of **$28,000**, of which **$12,000** was paid; **$7,405** is due now — the second payment, owed in June and still not made at the end of September. Val: "Окей, так я должен заплатить 7 405, правильно?" Misha: "7 405." [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- **A May order of $6,960** should have been paid by August; a prepayment was made and the final payment is open. Misha checked PO 370 — "это прессформа да там 30% можно заплатить" — and on **$11,600** that is "3000 там 480" ($3,480). *(Inference: $6,960 is 60% of $11,600, so this is probably the same mold order.)* [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- **PO 313, $28,000 mold** — "там 30%": this is the second 30%, and the last 30% is spread "на полгода помесячной" (monthly over half a year) [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **Small POs pass.** Val: "$200 и $100 это не проблема" and "4 $475 тоже не проблема." PO 440 ($200) is a mold modification, nothing to ship. PO 485 ($475) is one missing Flex part; 100 came by air, 500 were cast because it is cheap, and the other 400 ride in the general shipment. A 20-piece order of two parts ("сети 23"), $130, needs air [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **Flex parts for the 43 (PO 464).** Parts that must be paid before shipment, "все детали для флекса и в основном для… Ви 43." There is some stock, but "до конца года не хватит." Shipped at the end of September, they arrive about "начало ноября." [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- **Prepayment before shipment is the vendors' rule.** PO 501 is DDP delivery for those POs; "dt p это то, что все требуют оплатить до отправки." Val asked if paying the other invoices would make them relax it. Misha: no, and not only this vendor — Everglory demanded the same that day ("40% за детали 100% за детей", garbled) [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **General Touch ("gen touch"), PO 446, $6,700.** 21-inch touchscreens, 100 at $67 each, and no stock. Misha: the PO "висит, неподписаны очень давно"; some may have to go by air. The three could not agree on the weight (Misha about 3–4 kg; Genadi about 400 g; Val about half a kilo). Misha: glass must ship crated on skids, so "упаковка может весить больше, чем… товар." *(Supplier read as the General Touch named in July 2025 above — inference.)* [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- **The Echo motherboard vendor waits.** Val: "это можно подождать." Misha agreed — they performed badly in the spring and delayed one release by three months; it is the Echo motherboard, and they could not find the processor. See [[wiki/topics/echo-home-gaming-device.md]] (Sept 23) [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **Paid because urgent.** A vendor rendered "хуан джо"/"хонг джинг": three POs that must be paid, "один из них вообще нужно абсолютно срочно." PO 453 is hardware for the 43-inch, sea only; the other two are for new projects. Stock check: part 346 has **87** pieces — "Закончить сентябрь и октябрь и всё." **Shenzhen Everglory** — "очень срочно": touchscreens for the 43 must ship by air and sea express; that payment was not in the file yet and would come to Val for signature today, after a change Misha asked for. Two more Everglory POs: samples sent to Minsk/Kiev, and touchscreen-board components after some were lost — [[wiki/people/elizabeth.md|Elizabeth]] asked for 15 sets. The invoice was issued in July; Misha: better to pay now [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **Can wait.** A small order already delivered, with the vendor asking for nothing ("джиндау"); a vendor whose payment "может быть до лэйн бай туинс" (delayed by two weeks, as Val read it); and **StarTech** — "компания, где мы покупаем телевизоры" — where Misha had ordered 70 more small TVs on top of 30 in stock, to reach 100: "Мы можем потерпеть." [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- **Springs: part by air.** A $3,000 order of 500 springs. Misha preferred sea (heavy, bought in bulk). He said stock covers 80 machines; Val said that is not enough and asked to fly part. Misha: "давай я попрошу, чтобы он отправил, допустим, ещё 100 штук самолётом, остальное морем." Genadi asked why pay extra for air when the vendor ships in a week on request. Misha: JVL's own payment also takes a week, so starting today is already the fast case [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].
- **Unclear.** Dongguan Bashida (small sums, vendor not pressing) — the outcome is garbled ("Тонал пей"); probably wait. Hong Kong Wanlin (harnesses) — shipping mode unclear [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]].

**§15.8:** clear — supplier and freight economics only.

## Open commitments (Sept 23 2026)

- [ ] Mikhail Perelman — ask the springs supplier to air-ship about 100 springs and send the rest by sea — due unspecified — [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- [ ] Mikhail Perelman — get the urgent Everglory payment (with the transfer change he asked for) to Val for signature — due Sept 23 2026 ("Должна сегодня прийти к тебе на подпись") — [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]

## Open questions

- What report or BOM does Mikhail need to place orders from, and who gives it to him? Genadi says he still has none; Val says it is a parallel problem; not settled — [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- General Touch PO 446 (100 touchscreens, $6,700, no stock, unsigned a long time): pay now, fly part, or hold? The talk moved to weight and packaging and did not come back to it. — [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- Part 346 runs out after October (87 on hand). No reorder was stated. — [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]

## Sept 24 2026 — named on the BOM and modem items (inference)

On the [[wiki/meetings/2026-09-24-hardware-repo-bom-source-of-truth-and-street-cabinet-layout.md|Sept-24 4:38 PM alignment call]], [[wiki/people/genadi-peari.md|Genadi]] named "Mikhail" among the people who use his part-number Excel ("for Felipe, sales people, Lev, Mikhail") and among those who can mark a new revision in BC ("или Михаил или я"). He also said "Misha" had bought a small number of LTE modules, which are now hard to buy locally (count garbled). All three mentions are read as Mikhail Perelman by the procurement/parts context — inference. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

## Sept 30 2026 (in absentia) — "you tell Michael which lock he orders" (inference)

On the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept-30 10:00 AM GitHub-to-MSBC meeting]] Val, arguing that nothing in a machine is improvised, said to Genadi: "You specify the hole, you specify the lock, and you tell Michael which lock he orders, and you tell Elizabeth which lock goes where." "Michael" is read as Mikhail Perelman by the ordering/procurement context — inference. It places him as the one who orders purchased parts off Genadi's specification, consistent with the Apr-28 2025 PO role model above [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## Oct 1 2026 — the purchase order is cut from 300 to 100; the stock figure under it; the supplier's one-month lead time

On the [[wiki/meetings/2026-10-01-mikhail-perelman-po-cut-to-100-units-and-stock-count.md|Oct-1 3:44 PM call]] (Russian; Val and Mikhail only) [[raw/Meeting_Transcript_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]]:

- **The order he was writing.** Mikhail wanted to release a PO; Val refused 300 units ("я не хочу замыкать деньги на 300 штук"), refused Mikhail's 200 ("На 200 на 200 штук ты согласишься"), and set 100: "мне хватит 100 у меня нету бенефита в 200 в 500 в миллион." Mikhail: "Я переделаю заказ на 100 штук. И отправлю." Ruling: [[wiki/decisions/2026-10-01-the-purchase-order-is-cut-to-100-units-not-300-or-200.md]]. The part is not named clearly in the source ("риун", garbled).
- **What his orders rest on.** "до пересчета мне лёва никаких файлов не давал… После этого лева сделал файл… 1 августа он его сделал там 29 июля, и я его получил. Вот на этих цифрах я базирую мои заказы… Насколько они правильные? Все я не уверен. У меня другого нет." The 233-unit line in that file against 29 now in BC is on [[wiki/topics/business-central-erp-implementation.md]] (Oct 1 2026). He had asked the person who counted to recheck: "я переспрашивал несколько раз она мне сказала, что нет"; she "уже внесла изменения в BC, там 29 штук числятся". He keeps no written exchange about it: "Мне не нужна такая переписка, у меня есть новая цифра в би си."
- **The supplier.** A Chinese supplier, away for a holiday from Oct 1 and back on the 7th; electronics now harder and dearer; lead time "месяц… минимум" where he could once ask for two weeks; a long-standing supplier with good terms (the term itself garbled). Val: "одно другого не касается."
- **Val wants to deal with the supplier himself.** "познакомь меня с этими людьми… Отправь мне, пожалуйста имя я с кем ты разговариваешь." Mikhail: "Хорошо." Dates: "Сроки я еще не могу сказать."

The derived notes carry the same decision and two undertakings [[raw/Meeting_Notes_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]].

**On the next call, in absentia.** Ten minutes later [[wiki/people/lev-rudky.md|Lev]] told Val that the 233 came from a block of July count data he had not posted, that "миша знает, что я ему пришлю файл", and that Mikhail knows the gap is on the BC side ("Он значил твоя вина?" — "Да"). Lev drew one exception: if Elizabeth had told Mikhail a part was missing and he had not had the quantity corrected, that part is not the BC load's error (the passage is broken; the notes' reading). "Миша" = Perelman by the PO/file context (§4) [[raw/Meeting_Transcript_Lev_Rudky_Missed_Inventory_Adjustments-October-1-2026.md]]. See [[wiki/meetings/2026-10-01-lev-rudky-missed-inventory-adjustments.md]].

**§15.8:** Val's sharper remarks to Mikhail about the conversation itself are withheld; order size, supplier and lead-time facts are company procurement and are recorded.

## Open commitments (Oct 1 2026)

- [ ] Mikhail Perelman — redo the purchase order for 100 units (not 300) and send it — due unspecified — [[raw/Meeting_Transcript_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]]
- [ ] Mikhail Perelman — send Val the names of the supplier contacts and introduce him to them — due unspecified — [[raw/Meeting_Transcript_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]]

## Oct 5 2026 (in absentia) — "no report to work with yet", and the 57-versus-65 monitor count

On the [[wiki/meetings/2026-10-05-design-to-msbc-zero-trust-repos-and-data-contracts.md|Oct-5 1:19 PM Val–Genadi meeting]] on the GitHub-to-MSBC BOM (Russian part), Genadi pushed back on the plan: "У меня просто есть чувство, что мы немножко оторваны от реальности. У миши до сих пор нету репорта, с которым он работает." Later: "А миша говорит, а я не могу ничего делать с этим. У меня нет репорта. Убилов материал." [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]

- **Val: a real problem, but a parallel one.** "Мишина проблема существует изза друг изза других вещей, которые да нужно адресовывать. Также важно, как и это, но совершенно идёт параллельно." Fixing it does not fix stock or the inventory report; and the cause may be Mikhail, Lev ("лёвы") or the physical count — he is not sure [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].
- **The example from that day.** "сколько мониторов? 57 или 65? Компьютер показывает 65. Она посчитала 57, когда миша сказал… у меня компьютер показывает 65, она пошла и посчитала да 65." The person who counted is not named. Val said an AI COO persona he is setting up will push weekly spot checks of part numbers (the notes' reading of a garbled line) [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].
- "миша" = Mikhail Perelman by the report/stock context (§4); the notes name him in full [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].

**§15.8:** Val's evaluative words about Mikhail's stance are held; the facts above are company procurement and inventory.

## Oct 8 2026 (in absentia) — leaving from January; Mary proposed to take over; his report and how ordering runs today

Named throughout the [[wiki/meetings/2026-10-08-genadi-bom-standard-flex-slim-metal-mikhail-hand-over-and-data-contracts.md|Oct 8 3:59 PM call]] between Val and Genadi ("Миша" = Mikhail Perelman by the procurement context, §4) [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]:

- **Leaving.** Val: "Миша будет уходить с января месяца"; Val expects it sooner ("на самом деле так не будет"). Val proposes [[wiki/people/mary.md|Mary]] takes over his role, with training from Oct 19 through November and half of December; Mikhail may help in January and February if needed. The notes record the same [[raw/Meeting_Notes_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]. See [[wiki/decisions/2026-10-08-mary-takes-over-mikhail-perelmans-ordering-role-with-training-from-october-19.md]].
- **Ordering without him.** Val: "чтобы мы без миши могли заказывать" — the goal of the week of Oct 12–20; see [[wiki/decisions/2026-10-08-msbc-stops-being-the-bom-source-and-the-week-of-october-12-goes-to-ordering-without-mikhail.md]].
- **His report, as Genadi describes it.** Enter a product number and a quantity; it shows the flat structure with on hand, on order, in shipment and the shortage — "Это самое главное… единственное, что с чем он работает." (On Oct 5 Genadi said he still had no report; the two may be different reports — unclear.)
- **How he sends drawings.** By email, forwarding the file list from his report.
- **Boards through Alekseev.** Mikhail tells [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] what to order; Genadi thinks Alekseev orders online and Mikhail pays, but does not know how that works without a PO.
- **Flex Slim metal.** The full cabinet metal for 100 units had not been started as of Oct 8 — see [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]] (Oct-8 update).

**§15.8 / §15 #1:** no reason for leaving was given and none is recorded; remarks judging his work and any personal detail are not recorded.

## Oct 13 2026 (in absentia) — his Excel report must go; off the BOM work from next week

At the [[wiki/meetings/2026-10-13-github-msbc-ai-bom-control-gate-and-msbc-only-reports.md|Oct 13 "GitHub-MSBC" meeting]] Val said the report Mikhail works from — MSBC data exported to Excel and worked in a pivot table, made for him by Lev — freezes the facts (for example once a month) and must disappear: procurement reports come only from MSBC. Arrival dates are taken roughly from him because vendors are not asked for transport invoices. Val repeated that Mikhail is leaving and said he is to come off this work from next week. See [[wiki/decisions/2026-10-13-procurement-reports-come-only-from-msbc-and-the-excel-export-report-goes-away.md]] and [[wiki/decisions/2026-10-13-the-agent-builds-the-bom-as-a-control-gate-taught-by-data-contracts-not-cad-and-genadi-finds-why-it-is-wrong.md]] [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]. Val's personal remarks about him are not recorded.

## Sources

- [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]

- [[raw/Meeting_Transcript_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]]
- [[raw/Meeting_Notes_Mikhail_Perelman_PO_Cut_to_100_Units_and_Stock_Count-October-1-2026.md]]
- [[raw/Meeting_Transcript_Lev_Rudky_Missed_Inventory_Adjustments-October-1-2026.md]]

- [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_Open_Purchase_Order_Payment_Walkthrough-September-23-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/retrofit_january_7_2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/procurement_relocation-june-24-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [[raw/procurement_production_relocation-july-3-2025.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [[raw/Meeting_Notes_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
