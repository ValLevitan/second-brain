**GAME DEVELOPMENT**

Weekly Meeting Report

February 19, 2026

*Attendees: Val Levitan · Michael Gottlieb · Juan Martinez · Efim Podvoiski · Lena Zhukova*

  --------------- --------------------------------------------------------------------------------------------
  **Session 1**   Jira Schedule Review --- IP-531 Game Concepts · IP-556 Game Design · IP-89 Game Production

  **Session 2**   Game Review --- Georgia Vertical 2 Game Selection Screen
  --------------- --------------------------------------------------------------------------------------------

**SESSION 1 --- SCHEDULE REVIEW**

**IP-531 --- Game Concepts**

**GC-351 --- Match 3 / "Pick 3" Three-Level Progressive**

Scope: All Lines & Ways games in Georgia Vertical 2, including Twin Bison. Replaces the Peach Progressive.

  -------------------------------------------------------------------------------------------------------
  **Jira Issue**           **Status**     **Notes**
  --------------------- ----------------- ---------------------------------------------------------------
  **GC-351**             **In Progress**  Assigned to Michael Gottlieb. Triggering mechanism finalized.

  -------------------------------------------------------------------------------------------------------

**Triggering Mechanism --- Decision Finalized**

The progressive will use the same triggering mechanism as the legacy Peach Progressive to maintain player familiarity:

- 5-reel games: 3 coins nudged onto reel 3

- 3-reel games: 1 coin nudged onto reel 3

- Rodeo Spins: coin on reel 4 (unchanged)

**Pick 3 Progressive Visuals**

  -------------------------------------------------------------------------------------------------------
  **Jira Issue**                              **Status**     **Notes**
  ---------------------------------------- ----------------- --------------------------------------------
  **GC-361 --- In-Game Symbol & Meters**    **In Progress**  Assigned to Lena Zhukova. Work underway.

  **GC-360 --- Bonus Visuals**                 **To Do**     Assigned to Lena Zhukova. Not yet started.
  -------------------------------------------------------------------------------------------------------

**GC-350 --- Twin Bison**

  --------------------------------------------------------------------------------------------------------------------------------------------------------
  **Jira Issue**           **Status**     **Notes**
  --------------------- ----------------- ----------------------------------------------------------------------------------------------------------------
  **GC-350**             **In Progress**  Assigned to Michael Gottlieb. Abstract in development. Will inherit Match 3 Progressive and new screen layout.

  --------------------------------------------------------------------------------------------------------------------------------------------------------

**GC-364 --- Lion's Riches Vertical Update**

  -------------------------------------------------------------------------------------------------------------------------------------------------
  **Jira Issue**           **Status**     **Notes**
  --------------------- ----------------- ---------------------------------------------------------------------------------------------------------
  **GC-364**             **In Progress**  Assigned to Michael Gottlieb. Abstract entered yesterday. Lena's design subtasks to be created in Jira.

  -------------------------------------------------------------------------------------------------------------------------------------------------

Note: Jira currently shows "To Do." Michael confirmed he started yesterday --- status should be updated to In Progress.

**Redesign Approach**

- Pay table reduced to a small section --- no longer taking over the top half of the screen

- Scrolling message banner added above reel bundle to cycle game instructions

- Large canvas created for a prominent animal image (lion / bison)

- This layout applies to both Lion's Riches and Twin Bison

**Swift Bonus --- Deprecated**

Swift Bonus is retired across Georgia, superseded by the Match 3 Progressive. Nebraska retains its Golden Husk Progressive.

**Per-Button RTP --- Requirement Confirmed**

Individual per-button RTP adjustment remains a product requirement across all bet buttons. Minimum floor is 92%. The 88% floor previously used in Georgia is discontinued.

**IP-556 --- Game Design**

  --------------------------------------------------------------------------------------------------------------------------------------
  **Jira Issue**                                     **Status**     **Notes**
  ----------------------------------------------- ----------------- --------------------------------------------------------------------
  **IP-1017 --- Wild Colt Update (SD-VLT-2)**      **In Progress**  Nearly complete.

  **IP-1018 --- Dragon Pays Update (SD-VLT-2)**       **To Do**     Next in queue. Oriental-themed game --- approved for South Dakota.
  --------------------------------------------------------------------------------------------------------------------------------------

**Royals Update --- Georgia and South Dakota**

All games in both markets moving to letter-based Royals (A, K, Q, J, 10) --- cleaner, modern standard. Applies to both new and previously released South Dakota games.

**IP-89 --- Game Production**

**IP-459 --- South Dakota VLT-2 Production**

Currently in active production: Black Hills Skinner, Cool Cat Keno, Liquid Glass style home screen, La Rosa, Rodeo Spins and Lion's Riches updates (just started).

Schedule note: Approximately one month extension expected due to Igor's military camp unavailability. Juan confirmed acceptance.

**IP-877 --- Calle Ocho / Florida (OMNI)**

  ------------------------------------------------------------------------------------------------------------------------
  **Jira Issue**           **Status**     **Notes**
  --------------------- ----------------- --------------------------------------------------------------------------------
  **IP-877**             **In Progress**  All art complete. No schedule attached. Resolution pending --- see Open Items.

  ------------------------------------------------------------------------------------------------------------------------

**Jackpot Rush --- South Dakota**

Removed from active schedule and archived. To be revisited for the South Dakota Vertical release.

**SESSION 2 --- GAME REVIEW**

**Georgia Vertical 2 --- Game Selection Screen**

**ADR vs. Requirements --- Clarification**

At the start of this session Efim confirmed that the progressive triggering mechanism decisions made in Session 1 are product requirements --- not Architectural Design Records (ADRs). Requirements originate from market observations by Juan and Felipe, then translated into JVL's technical answer by Michael and Efim. This confirms the approach of logging these as REQ issues in Jira.

**Current Game Selection Screen**

Lena shared the latest version of the game selection screen. The current layout reviewed:

+----------------------------------+-----------------------+------------------------+
| **Lines & Ways (6)**             | **Jackpot Rush (2)**  | **Fiery Ice Link (2)** |
+==================================+=======================+========================+
| Rodeo Queen                      | Sparkle 7             | Kyocho                 |
|                                  |                       |                        |
| Rodeo Spins                      | Sapphire Star         | Rodeo Queen            |
|                                  |                       |                        |
| *Dragon Dreams → Twin Bison\**   |                       |                        |
|                                  |                       |                        |
| *Gypsy Spirit → Lion's Riches\** |                       |                        |
|                                  |                       |                        |
| Bayou Riches                     |                       |                        |
|                                  |                       |                        |
| Queen of Luxor                   |                       |                        |
+----------------------------------+-----------------------+------------------------+

*\* Dragon Dreams and Gypsy Spirit to be replaced by Twin Bison and Lion's Riches as those games complete concept.*

**Fiery Ice Link --- Category Label**

Decision: The Fiery Ice Link section header will be updated to read "Hold and Re-Spin Games with Progressive." Reasoning: Lightning Link and Dragon Link have been in the market for over 10 years. This terminology is well understood by players and clearly communicates the gameplay mechanic, helping players find what they're looking for immediately without confusion.

Action item: Felipe should provide market data to validate or refine this label before final approval.

**Game Count --- 8 vs. 10**

A substantive debate took place on the number of games to include in the initial Georgia Vertical 2 release. The two positions were:

+---------------------------------------------------------------------------------+---------------------------------------------------------------------------------+
| **Val --- 8 Games (Standard)**                                                  | **Juan --- 10 Games (Data Collection)**                                         |
+=================================================================================+=================================================================================+
| 4 Lines & Ways, 2 Jackpot Rush, 2 Fiery Ice Link as the standard package        | 10 games across all three categories for the initial select-customer deployment |
|                                                                                 |                                                                                 |
| Additional games sold at a premium price point                                  | Primary objective of this release is data collection, not revenue optimization  |
|                                                                                 |                                                                                 |
| Games cost \~\$50K each to produce --- burn them strategically                  | More games = more comparative performance data on which titles resonate         |
|                                                                                 |                                                                                 |
| More new titles in the package (fewer retreads)                                 | After 90 days, underperforming games can be disabled to improve efficiency      |
|                                                                                 |                                                                                 |
| Removing games after a test is impractical and creates bad faith with operators | Georgia makes software updates difficult --- maximize data per deployment       |
+---------------------------------------------------------------------------------+---------------------------------------------------------------------------------+

Outcome: Val went on record disagreeing with the 10-game initial release but deferred the go-to-market game count decision to Juan. No change to the current 10-game layout was made.

**Layout Flexibility --- Requirement Established**

Val directed that the game selection screen layout must be flexible enough to support multiple configurations without requiring re-approval. The specific requirement stated:

  -----------------------------------------------------------------------
  **Category**                 **Min Games**           **Max Games**
  ----------------------- ----------------------- -----------------------
  Lines & Ways                     **4**                   **8**

  Jackpot Rush                     **2**                   **4**

  Fiery Ice Link                   **2**                   **4**
  -----------------------------------------------------------------------

Games must auto-center/reflow within each category section when titles are enabled or disabled. Lena confirmed multiple layouts are already prepared as standard practice.

**Long-Term Georgia Strategy --- Discussion Only**

The following topics were raised for future consideration. No decisions were made.

- Peach 1, 2, and 3 refresh on D27 with Match 3 Progressive, Liquid Glass UI, and enhanced nudge

- Jackpot Rush and Fiery Ice Link D27 versions (noting Aristocrat has both vertical and dual-screen versions in Georgia)

- Georgia Vertical 3: a release that incorporates the top performers from Vertical 2 alongside new titles

- Whether future releases will always be 6 entirely new games, or may include proven titles from previous releases

**New Nudge --- RTP Context**

Val took personal responsibility for the new nudge underperformance in the field. He confirmed the root cause was the 88% RTP setting on the lowest bet button, a setup error he directed. He stated that with the corrected 92% floor now in place for new deployments, he expects at least a 20% performance improvement over the previous average in new locations.

**DECISIONS MADE**

**Session 1 --- Schedule Review**

  --------------------------------------------------------------------------------------------------------------------------------------------------
   **\#**  **Decision**
  -------- -----------------------------------------------------------------------------------------------------------------------------------------
   **1**   Match 3 / Pick 3 Progressive will use the same triggering mechanism as the Peach Progressive (coins on specific reels).

   **2**   Match 3 Progressive applies to all Lines & Ways games in Georgia Vertical 2, including Twin Bison. Excludes Jackpot Rush and Fiery Ice.

   **3**   Swift Bonus is deprecated for Georgia. Nebraska retains the Golden Husk Progressive.

   **4**   Lion's Riches and Twin Bison will both use the new screen layout (reduced pay table, scrolling banner, large canvas animal image).

   **5**   Letter-based Royals (A, K, Q, J, 10) adopted for both Georgia and South Dakota --- cleaner, modern standard.

   **6**   Per-button RTP remains individually adjustable. Minimum floor set at 92% --- 88% floor discontinued.

   **7**   Jackpot Rush for South Dakota archived. To be revisited for the South Dakota Vertical release.

   **8**   Dragon Pays (Oriental-themed) approved for South Dakota --- one such title is acceptable.

   **9**   Approximately one month schedule extension accepted due to Igor's military camp unavailability.

   **10**  Efim to provide Fiery Ice progressive RTP parameters to Michael and Juan as a baseline reference.
  --------------------------------------------------------------------------------------------------------------------------------------------------

**Session 2 --- Game Review**

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   **\#**  **Decision**
  -------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   **11**  The progressive triggering mechanism decisions are product requirements --- not ADRs. Confirmed by Efim. Originate from Juan/Felipe market observations, interpreted by Michael.

   **12**  Fiery Ice Link category on the game selection screen will be relabeled "Hold and Re-Spin Games with Progressive."

   **13**  Dragon Dreams and Gypsy Spirit to be replaced on the game selection screen by Twin Bison and Lion's Riches as those games complete concept.

   **14**  Game selection screen layout must support flexible configurations: Lines & Ways 4--8, Jackpot Rush 2--4, Fiery Ice Link 2--4. Games must auto-center/reflow when enabled or disabled.

   **15**  Go-to-market game count decision deferred to Juan. Val's position (8 games standard) and reasoning are on record.
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**OPEN ITEMS & QUESTIONS**

**Session 1 --- Schedule Review**

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   **\#**  **Open Item / Question**                                                                                                                                                                     **Owner**
  -------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------
   **1**   Progressive name not yet final: "Pick 3" vs. "Match 3." Must be resolved before Lena finalizes visuals, as the name will appear in the game UI.                                             **Michael**

   **2**   Total RTP allocation for progressive base levels needs agreement (discussed range: 2--3%). Prerequisite for Efim to finalize game math. Efim to share Fiery Ice parameters first.    **Efim / Michael / Juan**

   **3**   IP-877 (Calle Ocho): All art complete. Decision needed --- close the IP or keep open with a schedule if developer tasks remain.                                                           **Val / Lena**

   **4**   GC-364 status needs to be updated from "To Do" to "In Progress." Lena also needs to create her design subtasks under this issue.                                                        **Michael / Lena**

   **5**   GC-360 and GC-361 descriptions still contain template placeholder text. Acceptance criteria not documented.                                                                                 **Michael**

   **6**   IP-1017 and IP-1018 descriptions appear to be copy-pasted incorrectly and do not match the actual games.                                                                                **Michael / Juan**
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Session 2 --- Game Review**

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   **\#**  **Open Item / Question**                                                                                                                                                       **Owner**
  -------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------
   **7**   Final game count for Georgia Vertical 2 initial release (8 vs. 10) --- deferred to Juan. Val's disagreement is on record.                                                       **Juan**

   **8**   Felipe to provide market data and feedback on the game selection screen layout and category labels before final approval.                                                  **Juan / Felipe**

   **9**   Pricing model for additional game packs (Val's proposal: standard 8-game pack at price X; additional games at premium) was not resolved. Needs a follow-up decision.         **Val / Juan**

   **10**  Whether 2 three-by-three games is sufficient in a 4 L&W configuration, or whether a minimum of 3 three-by-threes should be a requirement.                                  **Michael / Juan**

   **11**  D27 refresh strategy for Georgia --- is there a viable refresh cycle? Opportunity assessment needed.                                                                       **Juan / Michael**

   **12**  Georgia Vertical 3 planning --- no timeline or scope discussed. Flagged as a future strategic topic.                                                                    **Val / Juan / Michael**

   **13**  Jackpot Rush category label --- Michael suggested "Collect Jackpot Rush symbols to win progressives" as descriptive text. Not yet decided.                                 **Michael / Juan**
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**PROPOSED REQUIREMENTS --- PENDING TEAM CONFIRMATION**

*The following five requirements were identified across both sessions. They are drafted in the format used by the JVL Product Requirements project (REQ) and are presented here for team review and confirmation. Upon approval, they will be created as formal REQ issues in Jira and linked to the relevant game concept and production issues.*

**From Session 1 --- Schedule Review**

**REQ-DRAFT-1 --- Scrolling Message Banner Above Reel Bundle**

+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **REQ-DRAFT-1**         | **Scrolling Message Banner Above Reel Bundle**                                                                                                                                                                                                                                                                   |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Status**     | **Draft**                                                                                                                                                                                                                                                                                                        |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Origin**              | Games Review Meeting --- February 19, 2026 --- GC-364 Lion's Riches layout discussion                                                                                                                                                                                                                            |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Links**      | GC-364 (Lion's Riches Update), GC-350 (Twin Bison)                                                                                                                                                                                                                                                               |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Description**         | As part of the new vertical screen layout for Lion's Riches and Twin Bison, the game must display a scrolling text banner positioned above the reel bundle. This banner communicates key game instructions to the player on an ongoing basis, replacing the role previously served by the full-screen pay table. |
|                         |                                                                                                                                                                                                                                                                                                                  |
|                         | Example messages: "3 coin stacks trigger Match 3 Progressive", "3 \[symbol\] triggers Free Spins."                                                                                                                                                                                                               |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Acceptance Criteria** | 1.  A scrolling text banner is displayed above the reel bundle at all times during base game play.                                                                                                                                                                                                               |
|                         |                                                                                                                                                                                                                                                                                                                  |
|                         | 2.  The banner cycles through a configurable list of game instruction messages.                                                                                                                                                                                                                                  |
|                         |                                                                                                                                                                                                                                                                                                                  |
|                         | 3.  Messages accurately describe triggering conditions for all active features (progressive, free spins, etc.).                                                                                                                                                                                                  |
|                         |                                                                                                                                                                                                                                                                                                                  |
|                         | 4.  The banner does not obscure the reel bundle or any active game element.                                                                                                                                                                                                                                      |
|                         |                                                                                                                                                                                                                                                                                                                  |
|                         | 5.  The requirement applies to both Lion's Riches Vertical and Twin Bison.                                                                                                                                                                                                                                       |
+-------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**REQ-DRAFT-2 --- Dynamic Adjustable Progressive Hit Frequency Per Level**

+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **REQ-DRAFT-2**         | **Dynamic Adjustable Progressive Hit Frequency Per Level**                                                                                                                                                                                                                                                                                                                                    |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Status**     | **Draft**                                                                                                                                                                                                                                                                                                                                                                                     |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Origin**              | Games Review Meeting --- February 19, 2026 --- GC-351 progressive math discussion (Efim)                                                                                                                                                                                                                                                                                                      |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Links**      | GC-351 (Pick 3 / Match 3 Progressive)                                                                                                                                                                                                                                                                                                                                                         |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Description**         | Unlike previous JVL progressives with fixed, predetermined hit frequencies, the Match 3 three-level progressive requires a flexible, dynamically adjustable hit frequency per level. The frequency must be driven by the RTP allocation assigned to each progressive level, allowing the math engine to derive hit frequency from configured base RTP values rather than hard-coded outcomes. |
|                         |                                                                                                                                                                                                                                                                                                                                                                                               |
|                         | This flexibility is a prerequisite for finalizing the game math for all Lines & Ways games in Georgia Vertical 2.                                                                                                                                                                                                                                                                             |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Acceptance Criteria** | 6.  The progressive hit frequency for each level is derived from the configured RTP allocation for that level, not hard-coded.                                                                                                                                                                                                                                                                |
|                         |                                                                                                                                                                                                                                                                                                                                                                                               |
|                         | 7.  RTP base values for each progressive level can be configured independently.                                                                                                                                                                                                                                                                                                               |
|                         |                                                                                                                                                                                                                                                                                                                                                                                               |
|                         | 8.  Changes to RTP base values produce corresponding changes in observed hit frequency.                                                                                                                                                                                                                                                                                                       |
|                         |                                                                                                                                                                                                                                                                                                                                                                                               |
|                         | 9.  The system supports independent configuration of base RTP and increment RTP per level.                                                                                                                                                                                                                                                                                                    |
|                         |                                                                                                                                                                                                                                                                                                                                                                                               |
|                         | 10. Total progressive RTP across all three levels does not exceed the agreed allocation (to be confirmed by Efim, Michael, and Juan).                                                                                                                                                                                                                                                         |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**REQ-DRAFT-3 --- Match 3 Progressive --- Game Scope Definition**

+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **REQ-DRAFT-3**         | **Match 3 Progressive --- Game Scope Definition**                                                                                                                                                                 |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Status**     | **Draft**                                                                                                                                                                                                         |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Origin**              | Games Review Meeting --- February 19, 2026 --- GC-351, GC-350, and GC-364 scope discussion                                                                                                                        |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Links**      | GC-351, GC-350, GC-364, IP-535                                                                                                                                                                                    |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Description**         | The Match 3 three-level progressive (GC-351) must be formally scoped to define which Georgia Vertical 2 titles include it and which do not. This prevents ambiguity during design, production, and certification. |
|                         |                                                                                                                                                                                                                   |
|                         | In scope: All Lines & Ways games in Georgia Vertical 2, including Twin Bison (GC-350) and Lion's Riches Vertical Update (GC-364).                                                                                 |
|                         |                                                                                                                                                                                                                   |
|                         | Explicitly excluded: Jackpot Rush, Fiery Ice. The Match 3 Progressive fully replaces the Peach Progressive in all in-scope titles. Swift Bonus is not present in any in-scope title.                              |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Acceptance Criteria** | 11. Every Lines & Ways game in Georgia Vertical 2 includes the Match 3 Progressive as defined in GC-351.                                                                                                          |
|                         |                                                                                                                                                                                                                   |
|                         | 12. Jackpot Rush and Fiery Ice do not include the Match 3 Progressive.                                                                                                                                            |
|                         |                                                                                                                                                                                                                   |
|                         | 13. The Match 3 Progressive fully replaces the Peach Progressive in all in-scope titles.                                                                                                                          |
|                         |                                                                                                                                                                                                                   |
|                         | 14. Swift Bonus is not present in any Georgia Vertical 2 in-scope title.                                                                                                                                          |
|                         |                                                                                                                                                                                                                   |
|                         | 15. The scope list is documented and linked to GC-351 in Jira.                                                                                                                                                    |
+-------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**From Session 2 --- Game Review**

**REQ-DRAFT-4 --- Game Selection Screen --- Flexible Game Count Layout**

+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **REQ-DRAFT-4**         | **Game Selection Screen --- Flexible Game Count Layout with Auto-Reflow**                                                                                                                                                                                                                           |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Status**     | **Draft**                                                                                                                                                                                                                                                                                           |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Origin**              | Game Review Meeting --- February 19, 2026 --- Georgia Vertical 2 layout discussion (Val, Michael, Juan, Lena)                                                                                                                                                                                       |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Links**      | IP-535 (GA COAM Game Concepts)                                                                                                                                                                                                                                                                      |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Description**         | The Georgia Vertical 2 game selection screen must support variable numbers of games per category without requiring redesign or regulatory re-approval. When the number of games in a category changes, the layout must automatically center and reflow the game icons within that category section. |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | Supported ranges: Lines & Ways --- 4 to 8 games. Jackpot Rush --- 2 to 4 games. Fiery Ice Link --- 2 to 4 games.                                                                                                                                                                                    |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | This flexibility allows the field team to enable or disable titles per location via RIS without impacting the approved screen layout.                                                                                                                                                               |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Acceptance Criteria** | 16. The game selection screen renders correctly with any number of games within the defined range for each category.                                                                                                                                                                                |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | 17. Game icons auto-center within each category section when the count changes.                                                                                                                                                                                                                     |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | 18. The layout does not break, overlap, or leave unbalanced whitespace at any supported configuration.                                                                                                                                                                                              |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | 19. Enabling or disabling individual game titles via RIS does not require a layout redesign or resubmission for approval.                                                                                                                                                                           |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | 20. Jackpot Rush and Fiery Ice Link sections remain positioned as close to the player as possible (below Lines & Ways).                                                                                                                                                                             |
|                         |                                                                                                                                                                                                                                                                                                     |
|                         | 21. The screen renders correctly at all supported configurations simultaneously across different RIS profiles.                                                                                                                                                                                      |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**REQ-DRAFT-5 --- Fiery Ice Link Category Label**

+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **REQ-DRAFT-5**         | **Fiery Ice Link Category Label --- "Hold and Re-Spin Games with Progressive"**                                                                                                                                                                                                                                                                                                |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Status**     | **Draft**                                                                                                                                                                                                                                                                                                                                                                      |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Origin**              | Game Review Meeting --- February 19, 2026 --- Georgia Vertical 2 game selection screen discussion (Michael, Juan)                                                                                                                                                                                                                                                              |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Proposed Links**      | IP-535 (GA COAM Game Concepts), GC-359 (Fiery Ice Link Visual Presentation)                                                                                                                                                                                                                                                                                                    |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Description**         | The Fiery Ice Link category section on the Georgia Vertical 2 game selection screen must be labeled "Hold and Re-Spin Games with Progressive." This terminology is well established in the market (Lightning Link, Dragon Link) and immediately communicates the gameplay mechanic to players, reducing confusion and helping players find the game type they are looking for. |
|                         |                                                                                                                                                                                                                                                                                                                                                                                |
|                         | This label replaces any prior or placeholder category header for the Fiery Ice Link section.                                                                                                                                                                                                                                                                                   |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Acceptance Criteria** | 22. The Fiery Ice Link section header on the game selection screen reads exactly: "Hold and Re-Spin Games with Progressive."                                                                                                                                                                                                                                                   |
|                         |                                                                                                                                                                                                                                                                                                                                                                                |
|                         | 23. The label is consistent across all approved layout configurations (2 and 4 game variants).                                                                                                                                                                                                                                                                                 |
|                         |                                                                                                                                                                                                                                                                                                                                                                                |
|                         | 24. The label styling is visually consistent with the other category headers on the same screen.                                                                                                                                                                                                                                                                               |
|                         |                                                                                                                                                                                                                                                                                                                                                                                |
|                         | 25. Market data from Felipe confirming or refining the label is obtained prior to final regulatory submission.                                                                                                                                                                                                                                                                 |
+-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

*JVL Systems --- Confidential --- Internal Use Only*
