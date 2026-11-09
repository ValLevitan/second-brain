# Meeting Summary — Call with Genadi Peari (ad-hoc)
**Date:** November 3, 2026, 2:50 PM – 2:55 PM Eastern
**Duration:** ~5 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Genadi_Parts_Export_from_BC_to_GitHub-November-3-2026]]

## Summary

Held in Russian. Ad-hoc 1:1 call with no calendar entry.

Val called to ask whether Genadi is exporting the parts from Business Central. Genadi: he is importing all parts from BC into the GitHub repository they created. The repository has folders by category; each category has its own rules, because data contracts are created per category. Each part gets a small subfolder with its data contract, readme file and all engineering information.

Val said this worries him: it sounded like Genadi would maintain the rules and data contracts by hand in those small subfolders. Genadi: he will not touch anything; Claude does it all. The rule was written so there is no human interaction. His only manual job is to put the JVL documentation in. Yesterday he got access and started. Claude did not know how part numbers are built, so Genadi wrote a rule for the part-number standard; after that it worked and pointed out gaps for half a day. He is building the base now so everything runs automatically. Some parts, like a screw, only have a description; a monitor needs a data contract; Claude has to be told the difference.

Val: once all the rules and standards are in place, any export is instant. Then, after everything is in GitHub, should MSBC be cleaned and the parts loaded again from the new system? Genadi: not sure; the parts will live in GitHub as the source and nothing more is needed; everything can be generated from there. Val: he was afraid it was manual work; with about a thousand parts that would not be possible. Resolved.

## Decisions Made

No formal decisions recorded.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Continue building the rules so the BC parts import into the GitHub repository by category runs automatically | TBD | Normal | |

## Open Questions

- Whether MSBC parts are cleaned and reloaded from GitHub once the repository is the source. (Val raised; Genadi unsure)

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026*
*Source meeting: Call with Genadi Peari (ad-hoc, no calendar entry)*
