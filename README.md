# First-Time Charge Nurse: The Shift-Lead Field Manual

An education-only manual for nurses asked to take the charge role for the first time. Plain English, step by step, never condescending: the way a friend would explain it.

**Education only — not medical advice.** This manual teaches role-taking, fairness habits, scripts, staffing math, and communication patterns. It does not teach clinical care and never overrides your facility's policies, your manager, your house supervisor, or your clinical team. When in doubt, the policy manual and your escalation chain come first.

Built by [Asdale Dynamics, LLC](https://dylanasdale.github.io) — beginner-friendly AI education, books, and practical tools, published local-first.

This is the *shift-lead role* manual. It is deliberately distinct from its siblings:

- **new-nurse-first-year-guide** — surviving year one itself (the orientee's side of the story).
- **nurse-preceptor-toolkit-guide** — being assigned to teach a new hire one-on-one.
- **This manual** — what changes when your shift is about the whole unit instead of four or five rooms.

## What is inside

| Chapter | One-liner |
|---|---|
| 00 · Read this first | Scope, ground rules, how to run the manual |
| 01 · Saying yes and the first day | The ask, the yes, and your first hour at the desk |
| 02 · Assignment fairness | Building the grid nobody will hate by mid-shift |
| 03 · Shift huddle scripts | A five-minute huddle you can actually run |
| 04 · Flow and bed math | Capacity math: discharges, admits, and the board |
| 05 · Family call scripts | Kind, brief, boundary-keeping calls by situation |
| 06 · When to escalate | Green/amber/red — who to call, and when |
| 07 · Weathering the storm | Sick calls, surges, and holding the middle hours |
| 08 · End-of-shift debrief | Handoff up, thank-down, and the five-minute debrief |
| 09 · Glossary | Charge-desk words, translated |
| Worksheets (6) | Charge-day setup, assignment grid, huddle card, escalation card, family-call notes, debrief sheet |

## Run it (local-first, offline)

No dependencies. Python 3.10+ standard library only.

```bash
python3 build.py            # builds the static site into site/ and validates links
python3 build.py --check-only   # validate sources without writing anything
python3 -m unittest discover -s tests -v   # run the test suite
```

Then open `site/index.html` in any browser. No server, no network, no accounts, no analytics — nothing leaves your machine. Worksheets are print-styled, so `Ctrl/Cmd+P` gives clean printable pages. (`python3 -m http.server --directory site` works too if you prefer a local server.)

## Project layout

```
build.py        stdlib-only static site generator (markdown -> HTML) + validation
docs/           the manual, chapter by chapter (markdown)
worksheets/     printable worksheets and pocket cards (markdown)
tests/          unittest suite for the renderer, build, and repo integrity
site/           generated output (gitignored; rebuild anytime)
```

## Related projects

This manual complements its sibling tools:

- **new-nurse-first-year-guide** — the first-year survival manual.
- **nurse-preceptor-toolkit-guide** — the precepting toolkit.
- **sbar-report-builder-webapp** — builds SBAR handoff reports in a form; pairs naturally with the escalation chapter.
- **shift-brain-sheet-maker** — assembles a one-page brain sheet; pairs with the charge-day setup sheet.

## Privacy and safety

- Local-first: the build and the site make zero network requests (enforced by a strict Content-Security-Policy in every generated page).
- No secrets, no API keys, no patient data, no personal data — the worksheets are blank shells by design, and a test suite checks for accidental credentials.
- Education-only framing is asserted on every page, in every chapter, and in every worksheet.

## License

MIT — see [LICENSE](LICENSE). Copyright (c) 2026 Asdale Dynamics, LLC.
