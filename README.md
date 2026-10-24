# P1 Math HK · Furry Red Ball Math Explorer

Interactive, bilingual (繁中 / English) P1–P2 maths practice for Hong Kong early-primary students — with a real printable A4 worksheet generator.

Live site: **https://furryredball.github.io/P1-Math-HK/**

## What's inside

Single-file app (`index.html`) — no build step. The only external dependency is three.js r128 from cdnjs, used by the 3D shapes module (with a built-in SVG fallback if WebGL is unavailable).

| Module | 內容 | Focus |
|---|---|---|
| 1 | P1 加減與十格陣 | Make-10 addition, regrouping subtraction, missing addend |
| 2 | P1/P2 雙語應用題 | Comparison traps, two-step word problems, HK money & change |
| 3 | P2 乘除與退位 | 2-digit borrowing, multiplication as groups |
| 4 | 🏆 奧數挑戰 | Queue overlap, sawing intervals, age invariance |
| 5 | 3D 立體圖形 | Cylinder / cube / cuboid / cone / sphere / square pyramid — face, curved-surface, vertex & edge counts, everyday-object recognition, and property questions (rolls any direction, single apex, all-square faces, 5 faces…) answered from a side-by-side 3D comparison |

## Features

- **Procedural question engine** — every question is generated with randomised numbers plus matched distractor options, so it never runs out and can't be memorised.
- **Switchable visual helper** — ten-frames, bar models and the 3D shape viewer are hidden by default (no spoilers); toggle on for support. Using the helper is tracked separately from unassisted work.
- **Interactive 3D shape viewer** — each 3D question renders the actual solid in three.js: auto-rotating, drag to spin, green edge lines on polyhedra so vertices and edges are countable. Falls back to an inline SVG diagram when WebGL is unavailable.
- **3D comparison gallery** — property questions ("which one rolls in every direction?", "which has exactly one apex?") show all four answer options as separate rotatable models, each labelled under its tile, so the child compares real solids instead of guessing from words.
- **Unambiguous property questions** — every property question has exactly one shape in the library that fits, so there is no arguable second answer.
- **Printable worksheets** — print the current question as a single practice card, or generate a 10-question mixed A4 paper with a score box, name/class/date header, working area (incl. printed ten-frames), A/B/C/D tick circles on multiple-choice 3D questions, and an optional answer key with Socratic teaching clues on the last page.
- **Bilingual toggle** — Bilingual / 繁體中文 / English.
- **Cantonese + English text to speech** via the browser's Web Speech API.
- **Parent diagnostic report** — correct answers, unassisted solves, logic accuracy (word problems + olympiad), and hint count. Persisted in `localStorage`.

## Notes

- Stats are stored per-browser in `localStorage` (`redball_stats_v5`), so each device keeps its own progress.
- Worksheet pages are tuned for A4 portrait, 12mm × 15mm margins; the answer key starts on its own page.
- Pure static site — open `index.html` directly in a browser, or host on any static host.

## Local development

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

---

Furry Green Pets · family learning tooling
