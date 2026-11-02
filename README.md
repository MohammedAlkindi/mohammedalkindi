# Mohammed Alkindi

Computer science student at UC San Diego. I build developer tools, data systems, and formal verification experiments. Upstream contributor focused on distributed ML systems, numerical correctness, and OS interop.

In summer 2026, I was a data analyst intern at Shell Kuwait, building a Python tool that turns daily production spreadsheets into checked reports.

[Resume](https://www.alkindix.com/resume.pdf) · [Portfolio](https://www.alkindix.com) · [LinkedIn](https://www.linkedin.com/in/mohammed--alkindi) · [Email](mailto:malkindi@ucsd.edu)

## Selected projects

| Project | What I built | Explore |
| --- | --- | --- |
| **ProofX** | Number-theory experiments with seeded, replayable search ledgers and bounded Lean 4 formal checks. | [Source](https://github.com/MohammedAlkindi/proofx) · [Research notebook](https://www.proofx.org/research) |
| **Switchyard** | A CLI coordinating parallel coding agents on one repository using isolated Git worktrees and pre-merge collision detection. | [Source](https://github.com/MohammedAlkindi/switchyard) · [Demo](https://switchyardhq.vercel.app) · [npm](https://www.npmjs.com/package/@switchyardhq/switchyard) |
| **Ridge** | Spreadsheet analysis that computes statistics and data-quality evidence deterministically before optional model interpretation. | [Source](https://github.com/MohammedAlkindi/ridge) · [Demo](https://ridge-data.vercel.app) |
| **Quant** | Out-of-sample, cost-aware backtesting for trading signals, served over FastAPI with an open numerical audit log (`docs/audit.md`). | [Source](https://github.com/MohammedAlkindi/quant) · [Audit log](https://github.com/MohammedAlkindi/quant/blob/main/docs/audit.md) |
| **Pulse** | Local-first weekly review of Gmail, GitHub, and Notion activity where every claim carries an inspectable citation. | [Source](https://github.com/MohammedAlkindi/pulse) · [Walkthrough](https://pulse-overview.vercel.app/sample.html) |

## Selected merged fixes

- **Compiler numerical correctness: [microsoft/onnxscript #3027](https://github.com/microsoft/onnxscript/pull/3027).** Fusing BatchNorm into Gemm silently changed model outputs when Gemm used a non-default `beta`. I corrected the bias scaling and removed the forwarded attribute, with parameterized numerical regression tests.
- **ML distributed systems & quantization: [NVIDIA-NeMo/Automodel #4178](https://github.com/NVIDIA-NeMo/Automodel/pull/4178), [#4058](https://github.com/NVIDIA-NeMo/Automodel/pull/4058).** Fixed FP8 emulation flags for rowwise quantization recipes and mapped FSDP expert shards with `torch.chunk` memory layout under context parallelism.
- **Filesystem events: [watchdog #1204](https://github.com/gorakhargosh/watchdog/pull/1204).** Renaming `file` to `FILE` on Windows produced a false deletion event. I filtered the redundant native record and added file, directory, and genuine-deletion regression cases.
- **Windows installs: [microsoft/apm #2941](https://github.com/microsoft/apm/pull/2941).** Generated staging names consumed too much of the Windows path budget. I shortened them while preserving cleanup of older staging directories; regression tests cover path headroom and both naming formats.
- **Network serialization: [microsoft/playwright-python #2748](https://github.com/microsoft/playwright-python/pull/2748).** Preserved blank values in `Request.post_data_json` for form bodies to prevent payload dropping on downstream API validation.

As of November 2026: **[227+ merged upstream pull requests](https://github.com/search?q=author%3AMohammedAlkindi+-user%3AMohammedAlkindi+is%3Apr+is%3Amerged&type=pullrequests)**, including **[78 at Microsoft](https://github.com/search?q=author%3AMohammedAlkindi+org%3Amicrosoft+is%3Apr+is%3Amerged&type=pullrequests)** and **[22 at NVIDIA](https://github.com/search?q=author%3AMohammedAlkindi+org%3ANVIDIA+org%3ANVIDIA-NeMo+is%3Apr+is%3Amerged&type=pullrequests)**. Other contribution records: [simple-statistics](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Asimple-statistics%2Fsimple-statistics+is%3Apr+is%3Amerged&type=pullrequests), [watchdog](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Agorakhargosh%2Fwatchdog+is%3Apr+is%3Amerged&type=pullrequests), and [QwenLM](https://github.com/search?q=author%3AMohammedAlkindi+org%3AQwenLM+is%3Apr+is%3Amerged&type=pullrequests).

## Other work

[contextbill](https://contextbill.vercel.app) prices coding sessions from local transcripts. [OmanX](https://omanx.org) provides sourced visa and compliance guidance for Omani students abroad.

I use coding agents for much of this work and say so wherever a project asks. Off the keyboard: badminton and photography.
