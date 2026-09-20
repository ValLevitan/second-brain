# Meeting Summary — Rage-Nova_conversion

**Date:** September 14, 2026, 6:38 AM - 7:21 AM Eastern
**Duration:** approximately 43 minutes
**Attendees:** Val Levitan, Igor Metelski, Irina Shishko, Pavel Frolov, Anton Leshkevich
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026]]
**Source meeting:** Rage-Nova_conversion — Microsoft Teams

## Summary

An early-morning working session. Igor Metelski showed the results of his experiments in turning horizontal Texas games into vertical ones. The answer was clear: the conversion works mechanically, but the existing art cannot carry it. The meeting ended with a different route — take the vertical Georgia COAM games as the base for Texas instead.

**The technical problem.** A horizontal machine has two Full HD monitors (1920 × 1080 each) as its main scene. A vertical machine has one Full HD monitor turned to portrait. To build a vertical scene from horizontal material, you have to stack two scenes on top of each other — for a base game, the main scene with the reels and the pay-table scene. Because the two source monitors have the same resolution, stacking them without distorting anything leaves a large empty block on the vertical screen. To keep the composition at the same aspect ratio as the portrait monitor, the two stacked 1080-high areas need roughly another 1253 pixels above them.

**Three experiments, all shown live in the scene editor.**

1. *Spicy Fruits* — fill the empty top area with some background. It looked bad: the logo was stretched and distorted, and the reel area came out very small.
2. *Midnight Money* — stretch each horizontal monitor to half the vertical screen and join them. This distorts proportions: the scene and every symbol end up about 57% taller than they should be. The abstract background hides it somewhat, but the symbols have to be distorted too so they still fit the reel frame.
3. *Dutch Mill* (a 3×3 game) — in theory the distortion should have mattered less here, but the art itself breaks. The lower screen is a street with houses, the upper is canals with houses, and the two do not blend at the join.

Igor also raised an exotic fourth option — leave the bottom monitor undistorted and stretch the top one into the remaining space — and rejected it himself: the top would be stretched more than double.

His conclusion: building the scene is not the hard part. It works, animations run on it, and the process is only moderately laborious (download the videos, join them). The problem is composition and art, and AI cannot fix it — short of asking AI to generate new art, which he called doubtful.

**Why this is different from the earlier Rage→Nova work.** That work took a horizontal game from an existing product and produced a horizontal game for Nova. The difficulty there was that Nova until then had only the vertical Kali Ochi, so the framework had to be extended for horizontal layouts. The art was already horizontal, so aspect ratios were never in question.

**The way out.** Pavel Frolov put forward what he and Igor had discussed the day before: take a vertical Georgia game and convert it into a vertical Texas game, which should be much cheaper. Igor agreed it could work, with one catch — every Georgia game uses a symbol-driven progressive, and the frames for those symbols are baked into the background video, so the video still has to be worked on. But the designers still hold the unbaked 3ds Max scenes; they can switch off the visibility of those objects and re-bake a clean video. Igor called that a perfectly workable option.

Val cut through the progressive question directly: ignore it. If they go with the Georgia COAM games, everything gets adapted anyway — they are not going to try to make things fit, they will take the game and redo it, including the maths. Igor accepted that this is a more workable scheme than guessing at element placement.

**Irina's line on layout.** Irina Shishko pushed a different arrangement — leave the top screen at its current size, keep the pay table as it is since it already has enough height and width, and enlarge the main game field instead, then see what is left at the top for the logo. Igor's answer was that replacing the background effectively means replacing the whole scene, because both the reel frame and the logo are baked into it. He can place the reels and style the symbols however he likes; what he cannot do is produce the background video. For that he needs a person who can assemble it — after which he can fit it to element positions with Claude.

**Rage or Nova — where is development faster.** Val asked directly. Igor's answer was Rage, for now:

- A large library of already-built games. For Georgia they were essentially updating existing games with new art, so the maths analysis and scene construction were already done.
- A large base of bonuses to draw on, even for something relatively new like the match-3 bonus built for the last GA COAM.
- Long history with Efim's maths — the Rage framework already implements effectively all of it. Porting that to Nova is not especially hard with Claude, but it takes time.
- Rage is comparatively well tested. Many questions are closed there that would have to be answered again for Nova.

Nova's advantage is that it runs in a browser, so Claude can launch the game itself, confirm it did not crash, take screenshots and compare them against reference ones. Development on Nova can lean on Claude much more heavily, including at acceptance. Rage has none of that — no way to interact with a running game or check how art actually looks in it. But Nova still cannot run several games in one shell: there is no notion of releasing a product, only separate games. Igor's bottom line: if a new product has to ship quickly, do it in Rage.

**State of the Nova build.** Val asked Pavel whether Nova has been brought to the state where the new architecture and tech stack could be used. Not fully. One or two games can run on the FP7. The HAL library integration is not finished. The build has not been redone the new way — the shared-object build was meant to come from an integration repository, which was discussed and never done. Today the build runs from the game repository and pulls artefacts made by hand, without AI: a newer Slackware Linux was taken, a snapshot made of the necessary files, the Linux kernel built and baked into a separate image, which then serves as the system part; games, HAL and maths are added in Docker containers and the output is an ISO image for installing on the machine.

Doing it properly means rebuilding that repository on the same Linux used for RK — Debian, as Pavel recalled — so everything sits in one development system. The RK kernel already exists; a small piece of work is needed so it builds for the LAN-based machines. And the integration repository still has to be created, collecting artefacts from the separate repositories. On RK the work is already possible today, but RK also needs its integration repository, from which they would then take the build made for the RK SDK that exists now for Transactional — slightly less work there.

Igor started to object to the OmniCore submodule pulled into the Nova framework; Pavel said it is no longer relevant — Sasha and Daniil merged everything into one repository a few days ago — and Igor withdrew.

**Close.** Val stopped the meeting, saying anything further that morning would waste time and everyone needed to absorb what had been shown. He thanked Igor for the experiments and called them very useful, and apologised to Anton Leshkevich for getting him up early. Pavel began to raise a topic involving Yuri Valentinovich and finding a group of people; Val deferred it to a separate conversation and said he would call back on it.

## Decisions Made

- **Direct algorithmic conversion of horizontal Texas games to vertical is not viable with the existing art.** The scene conversion itself works, but composition and art break in every variant tried. (Igor Metelski, accepted by the group)
- **The route for a vertical Texas product is to start from the vertical Georgia COAM games**, not from the horizontal Texas ones. (Pavel Frolov proposed; Val Levitan adopted; Igor Metelski agreed it is more workable)
- **Everything in those games gets adapted, including the maths.** Val's direction was not to try to make the existing setup fit. (Val Levitan)
- **The progressive type is not a constraint on this decision.** Val told the group to disregard the mystery-versus-symbol-driven progressive question at this stage. (Val Levitan)
- **The baked-in progressive frames are solvable** — designers still hold the unbaked 3ds Max scenes and can re-bake background video without those objects. (Igor Metelski)
- **Considered and rejected: stretching the top screen into the remaining space** while leaving the bottom undistorted. More than double vertical distortion. (Igor Metelski, self-rejected)
- **The OmniCore submodule concern is closed** — already merged into a single repository. (Pavel Frolov; Igor Metelski withdrew the point)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Call Pavel Frolov back on the Yuri Valentinovich / team-sourcing topic in a separate conversation | September 14, 2026 | Normal | Pavel raised it at the close; Val deferred it out of this meeting |

No other firm commitments were made. Igor's offer to try further scene layouts was explicitly conditional — "if we want to pursue this" — and the meeting moved away from that path.

## Open Questions

- **Who assembles the background video.** Igor can position reels and style symbols but cannot produce background video. He needs a person for it, and then can fit it to element positions with Claude. No name was proposed.
- **Whether the Texas vertical product carries a symbol-driven progressive or something else.** Val set it aside rather than answering it.
- **Whether the maths rework for Texas is scoped.** Val said the maths will be redone; nobody sized it.
- **When the Nova integration repository and the Debian-based kernel build get done.** Pavel described what "properly" looks like for both LAN-based machines and RK; no owner or date was set.
- **Nova still cannot package several games into one product.** Named as the reason a fast new product should go to Rage; no plan was set for closing it.
- **Yuri Valentinovich and finding a group of people.** Cut off and moved to a separate call.

## Notes on the transcript

The meeting was held in Russian and the Teams transcription garbles most product and technical terms. Readings that are near-certain from context: "речь" / "рейдж" / "рэдж" / "реййд" / "речь вбор" / "речь в ремворк" = Rage / Rage framework; "нова" / "ново" / "ногу" / "номере" = Nova; "спайси фрут" / "спасти фрутс" / "спайси фронт" = Spicy Fruits; "мид нейтмани" / "миднайтмане" = Midnight Money; "дачмил" / "уточ мила" / "сдача милым" = Dutch Mill (game title uncertain); "калиочи" / "кали очи" = Kali Ochi (game title uncertain); "г кма" / "гка" / "джорджия коам" / "джорджия коан" = Georgia COAM; "ф п севен" = FP7; "лакваринукс" = Slackware Linux; "сошки" = .so shared libraries; "халл" / "хал" = HAL; "транзакл" = Transactional; "рк" / "RK" / "IK" = the RK platform; "омникор" / "магникора" = OmniCore; "сценезитер" = scene editor; "Клод" = Claude; "символ dreven" / "символ daning" / "символ древний прогрессив" = symbol-driven progressive; "мистери" / "мистер ли" / "мистер репрогрессии" = mystery progressive; "релы" / "рилы" / "делов" / "стрелов" / "стлов" = reels; "лояутов" = layouts; "пэкграундом" = background; "snote" / "снот" = snapshot; "автосэмаксе" = 3ds Max; "фил" = an existing product family (name unclear); "sausd data nor pays" = an existing product name, not recoverable from the audio.

Worth confirming with Val before being treated as fact: the exact Texas game titles used in the three experiments, the product name behind "фил", and whether "Дебиан" was actually settled as the RK Linux (Pavel said "помоему" — "I think"). Val's request to Irina at the start for a "рыбу" (a template) with contacts is too garbled to record as an action. The raw transcript is preserved unchanged, in Russian.

## Dispatch Log

*(empty — captured by the scheduled meeting-watcher sweep, no dispatch)*

---
*Processed from Teams transcript on September 14, 2026, 8:00 AM Eastern*
*Source meeting: Rage-Nova_conversion*
