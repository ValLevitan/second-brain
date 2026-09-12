---
type: decision
title: The Passport is preserved, not killed — the bindings are good and JVL is using them wrongly in this market, so the fix is to record and flag component changes rather than forbid them
date: 2026-09-11
aliases: [the passport must not be killed, паспорт убивать не надо, do not confuse RIS and passport, the bindings are good we use them wrongly, unit 17 changed its bill acceptor, record instead of forbid, operator nominates who may update the passport, they like that the passport exists]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# The Passport is preserved — the bindings are good, JVL uses them wrongly in this market

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|Sept 11 2026 10:33 AM call]], in answer to [[wiki/people/pavel.md|Pavel Frolov]]'s read of the field complaints. **This is the first internal ruling on the Passport after two weeks of operators complaining about it to Val's face.** Background and the operator-side quotations are on [[wiki/topics/ris-remote-install-and-machine-states.md]]. The derived notes state the ruling as "**The passport is preserved, not removed** — the bindings are good and are simply being used wrongly in this market" and attribute it to Val [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## The misreading Val rejected twice

Pavel: "Технином не нравится то, что всё таки у нас есть ремонт и нишевал setap, что они бы лучше бы работали вручную" — technicians dislike that we have remote and network setup at all, and would rather work manually [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

Val, flatly and twice: "Нет… Нет, это абсолютно неправда. Им нравится, что у нас есть ремотен ещё сета" — no, that is absolutely untrue; they like that we have remote setup [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## What they actually object to — and it is one specific thing

- **Val likes some of the restrictions himself**, including ones that force a call: "мне нравится, что у нас есть некоторые элементы… Рестрикшин, которые они должны позвонить филиппе" [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]. See [[wiki/people/felipe-miranda.md]].
- **The objection is having to call to get a new RIS issued:** "они должны позвонить Филипп, и чтоб он для них сделал новый риск, если б они сами могли сделать новый рис, это было бы прекрасно" — they have to call Felipe so he makes them a new RIS; if they could make a new RIS themselves, that would be wonderful [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].
- **RIS and the Passport must not be confused.** "Не надо путать рис и паспорт… им нравится тот факт, что у нас есть паспорт" — do not confuse RIS and passport; they like the fact that we have a passport [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]. **The corpus has been treating these as one grievance; this source separates them.**

## The market distinction he drew

The Latin-American rule does not apply here: "у них нету тех проблем, которые у нас были в Латинской Америке. К примеру, мы тебе не разрешаем меня, сбил их цептор, пока мы тебе сами не разрешили. Вот такой был у нас реклама" — they do not have the problems we had in Latin America, e.g. we do not permit you to change the bill acceptor until we ourselves permit it; that was our regulation [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

**What the same binding should do instead — record, flag, advise:**

> "А здесь мы можем сказать… Что ты меняешь, белый рецептор? Или просто оставить флаг или сказать ты так наши номер 17 и ты поменял вот белых центр какогото числа? Или мы можем сказать, что у тебя белый сектор требует… Модификации какойто или форму апгрейд."
> — here we can say that you are changing a bill acceptor, or simply leave a flag, or say: you are our unit number 17 and you changed a bill acceptor on such-and-such a date; or we can say your bill acceptor needs some modification or a firmware upgrade.
> [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

**The verdict, in one line:** "все эти привязки они хорошие… Но мы их неправильно пользуемся. На данном рынке" — all these bindings are good, but we are using them wrongly in this market [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

**And the instruction:** "паспорт паспорт убивать не надо, паспорт нужно сохранить… Его нужно сохранить" — the passport must not be killed, the passport must be preserved [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## The implementation constraint, and who gets to update a Passport

Pavel named what stands in the way today: "текущая просто имплементация… подразумевает, что обновление паспорта делается только для тех… людей, которые заведены у нас в CMS" — the current implementation only lets people who are entered in JVL's CMS update a passport. And his proposal for the new one: "если мы уходим… [в] новую реализацию CMS… то мы должны давать оператору назначать людей, которые могут это делать" — under the new CMS implementation the operator must be allowed to nominate the people who may do it [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

Val agreed with one qualification: "Если он хочет… а если он не хочет, то… он может сказать, я не хочу этим заниматься" — if he wants to; if he does not want to, he can say he does not want to deal with it [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## How this sits against Sept 2 and Sept 10 — recorded, not reconciled

The corpus already holds two customer-facing positions on the same lock, in opposite directions, neither of which mentions the other:

- **Sept 2, to [[wiki/organizations/lucky-coin.md|Lucky Coin]]:** "Then you don't need that feature, and we should remove it."
- **Sept 10, to [[wiki/organizations/diamond-amusement.md|Diamond Amusement]]:** it is "the jugular of the whole operating system… I cannot simply say, okay, get rid of it" — removal comes only with the new platform.

**Sept 11 is a third, internal position and it is not the same as either:** the Passport stays, on every platform, and what changes is what JVL does with it in this market. It does not resolve the Sept-2/Sept-10 pair — nothing in this source mentions either conversation — and the open contradiction on [[wiki/topics/ris-remote-install-and-machine-states.md]] stands. Both earlier quotations and their citations are on that page.

**§15.8:** clear — product control design only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
