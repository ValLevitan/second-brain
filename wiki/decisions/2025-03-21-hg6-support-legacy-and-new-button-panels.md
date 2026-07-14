---
type: decision
title: HG6 software to support both legacy and new button panels via one XML config
date: 2025-03-21
aliases: [dual button panel, HG6 button panel, XML key codes]
source-count: 2
status: active
---

# HG6 software to support both legacy and new button panels via one XML config

On the Mar 21 2025 Puerto Rico product-line call, the team decided that the **HG6 software will support both the legacy (old counter-board) button panel and the new panel simultaneously**, via a single **XML configuration** file that lists the key codes of both — so one software build serves both retrofit machines (old board) and CPU kits (new board), with no manual selection step. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## What was decided

- Add the old counter-board's key codes into the new XML button file alongside the new codes; the two sets don't overlap, so the panel displays as one but works for both hardware generations. [[raw/product_matrix_puerto_rico-march21-2025.md]]
- Avoid maintaining separate software versions and avoid a **manual** old-vs-new selection at setup — [[wiki/people/val-levitan.md|Val]] argued manual selection would "definitely" cause a mistake. [[raw/product_matrix_puerto_rico-march21-2025.md]]
- Do it in **software/XML**, not firmware: [[wiki/people/genadi-peari.md|Genadi]] offered to make the wiring/key mapping identical so numbers line up, but [[wiki/people/pavel.md|Pavel]] said that would require firmware changes, whereas the XML approach is simpler. [[raw/product_matrix_puerto_rico-march21-2025.md]]

## Rationale

Puerto Rico ships both retrofit cabinets (old electronics kept) and HG6 CPU kits (new electronics), each with a different counter board / panel. A single software that auto-handles both panels avoids per-machine builds and manual errors. Panel *design* still needs [[wiki/people/juan-martinez.md|Juan Martinez]]'s final approval. See [[wiki/topics/puerto-rico-product-configuration.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## Sources

- [[raw/product_matrix_puerto_rico-march21-2025.md]]
- [[raw/requirements_puerto_rico-march-21-2025.md]]
