# JVL second brain — weekly update, 31 October 2026

## The short version

**14 meetings came in, from Saturday 24 October to Friday 30 October.** There was no new South Dakota report this week. I tested 146 facts against the recordings by hand, and all 146 were right. I also tested 133 quotes picked at random, and all were right. Everything is saved and sent to GitHub.

## What came in

**1. The new game engine and Miranda (29–30 October).**
- On 29 October you stopped Miranda development. You see no future in it. Miranda is not the base for the new engine. It must be preserved properly (prose, data contracts, repositories).
- Your order of work for the new engine: describe the full engine, split it into MVP 1, 2 and 3, make the schedules and a test environment, and only then write code.
- Anton, Igor and Alexander (Biratka) build it together, not Anton alone.
- MVP 1 must let Claude run the engine on the designer's computer.

**2. The AI game design agent (24, 29 and 30 October).**
- Evgeny Kharetski showed the agent twice. It writes game briefs in Teams and leads a designer who is stuck.
- On 24 October you ruled: code is the only source of truth, not Confluence. Claude will build a wiki page for each old game from the old SVN code.
- On 29 October Bosik proposed one company second brain for all AI agents, with access limited for each agent. The game agent gets game knowledge only, no meetings and no transactions.
- You asked for one full test: from a brief to a finished game on the production server.
- On 30 October you ruled: study competitor games for new mechanics, not maths, and only games in JVL's markets. The method is tested first on JVL's own games by 6 November.

**3. NOVA remote update (30 October).**
- Remote update is for NOVA only, and Texas comes first.
- The full design is written first; the MVP split comes after. The review is Friday 6 November, 9 AM.

**4. Flex-Port and the stand-ups (26–30 October).**
- The Flex-Port now counts meter pulses from 30 to 150 ms, because a Banilla machine pulsed at 125 ms.
- A second cash-out inside the timeout is added to the first one.
- The screen shows the cash-out amount in whole dollars as the pulses come in.
- The first installs go in bill-validator plus pulse mode. SAS worked only with Aristocrat.
- New team rules: Claude branches must carry a Jira number and be deleted when the task closes, and Claude is never a co-author of a commit. The default build button must build with default settings.
- Yavorski is blocked from merging into the Flex-Port main code.

**5. Reports and hardware (29 October).**
- Tableau is dropped. Machine reports become an Excel export from the old CMS, limited by role and region, 6 months at most, ready by 7 November.
- Nathan showed the first data contract written by the AI agent. The agent's instructions move to the persona repository. Next review is Wednesday 4 November.

## What the wiki learned

- **13 new decisions** and 14 meeting pages. No new people.
- **Changed:** the 5 October rule that reopened a finished feature by itself is dropped. Now the person who made the story moves it by hand.

## For you

1. **Your staffing talk with Pavel and Irina (29 October).** You asked that it stay between the three of you. I kept the staffing plans and the views on named people out of the brain. Pay talk is also out, by the standing rule. Should any of it go in?
2. **Efim and maths (24 October).** You said JVL may soon not need someone like Efim to make maths; he would only check it. I kept it as your view, not a decision. Is that right?
3. **Yavorski.** He still merges old code, and he is now blocked. Pavel will ask you if the work with him is over.
4. **Who writes up the mechanics of JVL's newer games:** Igor or Evgeny Kharetski?
5. **Persona repository and the company second brain.** Both came up on 29 October. How do they fit together?

## Health

Everything checked out. The October month-close check runs next week, because files for 31 October may still arrive.
