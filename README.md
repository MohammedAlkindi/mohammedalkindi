# Mohammed Alkindi

Computer science student at UC San Diego. Upstream contributor with **[230+ merged pull requests](https://github.com/search?q=author%3AMohammedAlkindi+-user%3AMohammedAlkindi+is%3Apr+is%3Amerged&type=pullrequests)** across Microsoft, NVIDIA, and open-source runtimes. Focused on distributed ML systems, numerical correctness, OS interoperability, and deterministic data infrastructure.

In summer 2026, I was a data analyst intern at Shell Kuwait, building a Python tool that validated daily production spreadsheets into checked reports.

[Resume](https://www.alkindix.com/resume.pdf) · [Portfolio](https://www.alkindix.com) · [LinkedIn](https://www.linkedin.com/in/mohammed--alkindi) · [Email](mailto:malkindi@ucsd.edu)

---

### Merged into work maintained by

<p align="left">
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3Amicrosoft+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/Microsoft-18181b?style=for-the-badge&logo=microsoft&logoColor=white" alt="Microsoft" />
  </a>
  &nbsp;
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3ANVIDIA+org%3ANVIDIA-NeMo+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/NVIDIA-18181b?style=for-the-badge&logo=nvidia&logoColor=white" alt="NVIDIA" />
  </a>
  &nbsp;
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3Aaws+org%3Aaws-powertools+org%3Aaws-samples+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/AWS-18181b?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />
  </a>
  &nbsp;
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3Arust-lang+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/rust--lang-18181b?style=for-the-badge&logo=rust&logoColor=white" alt="rust-lang" />
  </a>
  &nbsp;
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3Apydantic+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/Pydantic-18181b?style=for-the-badge&logo=pydantic&logoColor=white" alt="Pydantic" />
  </a>
  &nbsp;
  <a href="https://github.com/search?q=author%3AMohammedAlkindi+org%3Aexpressjs+is%3Apr+is%3Amerged&type=pullrequests">
    <img src="https://img.shields.io/badge/Express-18181b?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  </a>
</p>

<sub>Also merged at tox, pdm, mcp-use, pywin32, and MindsDB, among others.</sub>

---

### Tools I reach for

<p align="left">
  <img src="https://skillicons.dev/icons?i=ts,js,py,swift,react,nextjs,nodejs,bun,fastapi,electron,pytorch,tailwind,cloudflare,supabase,postgres,docker&perline=8" alt="Tools I reach for" />
</p>

---

## Selected projects

| Project | What I built | Explore |
| --- | --- | --- |
| **ProofX** | Number-theory experiments with seeded, replayable search ledgers and bounded Lean 4 formal checks. | [Source](https://github.com/MohammedAlkindi/proofx) · [Research notebook](https://www.proofx.org/research) |
| **Switchyard** | Multi-agent coordination CLI with isolated Git worktrees, pre-merge collision detection, and token accounting via ContextBill. | [Source](https://github.com/MohammedAlkindi/switchyard) · [Demo](https://switchyardhq.vercel.app) · [npm](https://www.npmjs.com/package/@switchyardhq/switchyard) |
| **Ridge** | Spreadsheet analysis computing statistics and data-quality evidence deterministically before optional model interpretation. | [Source](https://github.com/MohammedAlkindi/ridge) · [Demo](https://ridge-data.vercel.app) |
| **OmanX** | Sourced visa and compliance guidance platform for Omani scholarship students abroad. | [Live Platform](https://omanx.org) |

## Selected merged fixes

- **Compiler numerical correctness: [microsoft/onnxscript #3027](https://github.com/microsoft/onnxscript/pull/3027).** Fusing BatchNorm into Gemm silently changed model outputs when Gemm used a non-default `beta`. Corrected bias scaling and attribute forwarding with parameterized regression tests.
- **ML distributed systems and quantization: [NVIDIA-NeMo/Automodel #4178](https://github.com/NVIDIA-NeMo/Automodel/pull/4178), [#4058](https://github.com/NVIDIA-NeMo/Automodel/pull/4058).** Fixed FP8 emulation flags for rowwise quantization recipes and mapped FSDP expert shards with `torch.chunk` memory layout under context parallelism.
- **Filesystem events & OS race conditions: [watchdog #1204](https://github.com/gorakhargosh/watchdog/pull/1204).** Renaming `file` to `FILE` on Windows produced a false deletion event. Filtered redundant native records with file, directory, and genuine-deletion regression cases.
- **Windows installs & path budget: [microsoft/apm #2941](https://github.com/microsoft/apm/pull/2941).** Generated staging names consumed excessive Windows path budget. Shortened staging paths while preserving cleanup headroom and legacy naming formats.
- **Network serialization: [microsoft/playwright-python #2748](https://github.com/microsoft/playwright-python/pull/2748).** Preserved blank values in `Request.post_data_json` for form bodies to prevent payload dropping on downstream API validation.

As of November 2026: **[230+ merged upstream pull requests](https://github.com/search?q=author%3AMohammedAlkindi+-user%3AMohammedAlkindi+is%3Apr+is%3Amerged&type=pullrequests)**, including **[78 at Microsoft](https://github.com/search?q=author%3AMohammedAlkindi+org%3Amicrosoft+is%3Apr+is%3Amerged&type=pullrequests)** and **[22 at NVIDIA](https://github.com/search?q=author%3AMohammedAlkindi+org%3ANVIDIA+org%3ANVIDIA-NeMo+is%3Apr+is%3Amerged&type=pullrequests)**. Other core contribution records: [TypeChat](https://github.com/microsoft/TypeChat/pulls?q=is%3Apr+author%3AMohammedAlkindi+is%3Amerged), [simple-statistics](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Asimple-statistics%2Fsimple-statistics+is%3Apr+is%3Amerged&type=pullrequests), [watchdog](https://github.com/search?q=author%3AMohammedAlkindi+repo%3Agorakhargosh%2Fwatchdog+is%3Apr+is%3Amerged&type=pullrequests), and [QwenLM](https://github.com/search?q=author%3AMohammedAlkindi+org%3AQwenLM+is%3Apr+is%3Amerged&type=pullrequests).

## How I build

- **Deterministic computation first.** Models summarize and explain, but numbers, statistics, and signals are computed deterministically.
- **Reproducible execution ledgers.** Every experiment and backtest records seeds, revisions, and execution traces so outcomes can be replayed and audited.
- **Upstream correctness.** Defects are solved by reproducing the failure, writing the regression test first, and fitting maintainer constraints.

> **Activity note:** My GitHub contribution graph reflects daily engineering, upstream pull requests, and workspace telemetry from local agent harnesses. I prioritize verifiable upstream merges and reproducible test coverage over raw commit volume.
