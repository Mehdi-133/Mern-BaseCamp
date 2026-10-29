# 🖼️ Workshop visual pack

> ✅ **Visual assets checked, 28 October 2026.** This verifies preparation quality, not learner understanding or live-demo behavior.

| Asset | Purpose | Format | Used in | Verification |
| --- | --- | --- | --- | --- |
| [Context map](context-map.png), [editable source](context-map.svg) | Explain the six exact files, entry point, feature spec and responsibility | SVG + PNG, 1600 × 1430 | Activity README and concept lesson | ✅ PNG opened and visually inspected after feedback arrow correction; labels, contrast, spacing and arrow direction checked |
| [Engineering loop](engineering-loop.png), [editable source](engineering-loop.svg) | Show clarify → brief → specify → implement → verify → record, including correction loop | SVG + PNG, 1600 × 1020 | Concept lesson | ✅ PNG opened and visually inspected; check/fail arrows and example labels reviewed |

## 🧪 Other preparation checks

- Source archive and eight inert snapshots compared byte for byte; all matched.
- Both SVG documents parsed and PNGs decoded; dimensions confirmed.
- Local lesson/index/image links and Markdown fences checked.
- Interactive chat explorer checked in Chromium at 320, 736 and 1024 pixels; no horizontal overflow or clipped diagram labels. All six selections changed the question/example; no JavaScript page errors. Desktop/mobile screenshots visually inspected.
- Browser launch initially required filesystem/process permission; the approved rerun passed. The optional CLI package was not cached, so the already-bundled Playwright library performed the checks without installing packages.
- Repository whitespace checked; original source snapshots preserve source bytes locally and are excluded from public Git publication.

The interactive explorer is conversation content, not a hosted workshop website. The repository lesson and diagrams remain useful independently. No application, API behavior, classroom comparison, rehearsal or understanding result is claimed.
