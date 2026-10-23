# Mohammed Alkindi

Computer science student at UC San Diego. I build developer tools and data systems, and fix Windows, CI, and numerical correctness bugs in open source.

In summer 2026, I was a data analyst intern at Shell Kuwait, building a Python tool that turns daily production spreadsheets into checked reports.

[Resume](https://www.alkindix.com/resume.pdf) · [Portfolio](https://www.alkindix.com) · [LinkedIn](https://www.linkedin.com/in/mohammed--alkindi)

## Selected projects

| Project | What I built | Explore |
| --- | --- | --- |
| **Switchyard** | A CLI that gives each coding agent an isolated git worktree and detects collisions before merging. | [Source](https://github.com/MohammedAlkindi/switchyard) · [Demo](https://switchyardhq.vercel.app) · [npm](https://www.npmjs.com/package/@switchyardhq/switchyard) |
| **Ridge** | Spreadsheet analysis that computes statistics and data-quality evidence deterministically before optional model interpretation. | [Source](https://github.com/MohammedAlkindi/ridge) · [Demo](https://ridge-data.vercel.app) |
| **ProofX** | Number-theory experiments with seeded, replayable search ledgers and bounded Lean checks. | [Source](https://github.com/MohammedAlkindi/proofx) · [Research notebook](https://www.proofx.org/research) |

## Selected merged fixes

- **Numerical correctness: [microsoft/onnxscript #3027](https://github.com/microsoft/onnxscript/pull/3027).** Fusing BatchNorm into Gemm silently changed model outputs when Gemm used a non-default `beta`. I corrected the bias scaling and removed the forwarded attribute, with parameterized numerical regression tests.
- **Windows installs: [microsoft/apm #2941](https://github.com/microsoft/apm/pull/2941).** Generated staging names consumed too much of the Windows path budget. I shortened them while preserving cleanup of older staging directories; regression tests cover path headroom and both naming formats.
- **Filesystem events: [watchdog #1204](https://github.com/gorakhargosh/watchdog/pull/1204).** Renaming `file` to `FILE` on Windows produced a false deletion event. I filtered the redundant native record and added file, directory, and genuine-deletion regression cases.

As of October 22, 2026: [196 merged upstream pull requests](https://github.com/search?q=author%3AMohammedAlkindi+-user%3AMohammedAlkindi+is%3Apr+is%3Amerged&type=pullrequests), including [58 at Microsoft](https://github.com/search?q=author%3AMohammedAlkindi+org%3Amicrosoft+is%3Apr+is%3Amerged&type=pullrequests). Other contribution records: [simple-statistics](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Asimple-statistics%2Fsimple-statistics+is%3Apr+is%3Amerged&type=pullrequests), [NVIDIA](https://github.com/search?q=author%3AMohammedAlkindi+org%3ANVIDIA+org%3ANVIDIA-NeMo+is%3Apr+is%3Amerged&type=pullrequests), and [NegPy](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Amarcinz606%2FNegPy+is%3Apr+is%3Amerged&type=pullrequests).

## Other work

[contextbill](https://contextbill.vercel.app) prices coding sessions from local transcripts. [OmanX](https://omanx.org) provides sourced visa and compliance guidance for Omani students abroad.

I use coding agents for much of this work and say so wherever a project asks. Off the keyboard: badminton and photography.
