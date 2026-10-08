
# Mohammed Alkindi

Computer science student at UC San Diego. I spent summer 2026 as a data analyst intern at Shell Kuwait, building the Python tool that turns their daily production spreadsheets into checked reports.

Most of my time on GitHub goes into fixing bugs in other people's projects, mostly Windows path handling, CI and correctness. As of October 2026 that is [161 merged pull requests across 43 repositories](https://github.com/search?q=author%3AMohammedAlkindi+-user%3AMohammedAlkindi+is%3Amerged&type=pullrequests). I use coding agents for much of this work and say so wherever a project asks.

## Where the merged work is

- [Microsoft](https://github.com/search?q=author%3AMohammedAlkindi+org%3Amicrosoft+is%3Amerged&type=pullrequests): 36, mostly docs and CI fixes in hve-core, plus apm, onnxscript and playwright-python
- [simple-statistics](https://github.com/search?q=author%3AMohammedAlkindi+org%3Asimple-statistics+is%3Amerged&type=pullrequests): 23
- [NVIDIA](https://github.com/search?q=author%3AMohammedAlkindi+org%3ANVIDIA+org%3ANVIDIA-NeMo+is%3Amerged&type=pullrequests): 19, in Automodel, NeMo Agent Toolkit and SkillSpector
- [NegPy](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Amarcinz606%2FNegPy+is%3Amerged&type=pullrequests): 17
- [watchdog](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Agorakhargosh%2Fwatchdog+is%3Amerged&type=pullrequests): 10

A few examples:

- [microsoft/apm #2941](https://github.com/microsoft/apm/pull/2941): installs failed on Windows once staging paths passed 260 characters. Shorter generated path segments fixed it.
- [microsoft/onnxscript #3027](https://github.com/microsoft/onnxscript/pull/3027): a default optimizer rule that folds BatchNorm into Gemm ignored Gemm's beta, so rewritten models returned wrong numbers with no error.
- [watchdog #1204](https://github.com/gorakhargosh/watchdog/pull/1204): renaming `file` to `FILE` on Windows fired a false deletion event.

## Projects

- [Ridge](https://ridge-data.vercel.app): spreadsheet analysis that computes the statistics before an LLM explains them.
- [Switchyard](https://switchyardhq.vercel.app): gives each coding agent its own git worktree so several can work on one repo. On npm.
- [ProofX](https://proofx.org): counterexample search for number theory conjectures, with replayable runs. Paused.
- [contextbill](https://contextbill.vercel.app): prices Claude Code sessions from your local transcripts.
- [OmanX](https://omanx.org): answers visa and compliance questions for Omani students abroad, with sources.

[LinkedIn](https://www.linkedin.com/in/mohammed--alkindi) · [alkindix.com](https://www.alkindix.com) · [Resume](https://www.alkindix.com/resume.pdf)

Off the keyboard: badminton and photography.
