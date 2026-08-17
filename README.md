# Mohammed Alkindi

CS at UC San Diego, data analytics at Shell. I build tools that keep a result
checkable — where a number came from, what it rests on, and the point where it
stops being supported.

Most of what I ship is deterministic first: compute the evidence, then let a
model explain it. Never the other way round.

## Open source

Nine merged upstream, across five projects. A recurring theme: hosted CI runs
Linux, or a Windows *Server* image with elevation — so a whole class of defect
is invisible to it until someone runs the suite on an ordinary Windows machine.

**[simple-statistics](https://github.com/simple-statistics/simple-statistics)**

- [#814](https://github.com/simple-statistics/simple-statistics/pull/814) —
  `sampleRankCorrelation` returned a different answer for the same paired data
  depending on row order whenever values tied; ties now share their average rank.
- [#819](https://github.com/simple-statistics/simple-statistics/pull/819) —
  a fresh Windows clone failed `npm test` before running a single test, because
  the linter chokes on CRLF; the repo's line endings are normalised to LF.
- [#823](https://github.com/simple-statistics/simple-statistics/pull/823) —
  `perceptron`'s `predict` and `train` could return `null`, which the type
  declarations denied; callers type-checked against a lie.
- [#833](https://github.com/simple-statistics/simple-statistics/pull/833) —
  `approxEqual`'s tolerance argument is optional in the implementation and was
  required in the types.

**[watchdog](https://github.com/gorakhargosh/watchdog)**

- [#1204](https://github.com/gorakhargosh/watchdog/pull/1204) — renaming a file
  to a different case on Windows emitted a spurious deletion before the rename;
  the false deletion is now coalesced away.
- [#1205](https://github.com/gorakhargosh/watchdog/pull/1205) — the docs claimed
  `BaseThread` inherits its daemon flag from the creating thread; it always runs
  as a daemon, and the docs now say so.

**[NegPy](https://github.com/marcinz606/NegPy)**

- [#836](https://github.com/marcinz606/NegPy/pull/836) — the test suite read
  source files in the platform's default codepage and split paths on `/`, so it
  failed on any non-UTF-8 Windows box.
- [#840](https://github.com/marcinz606/NegPy/pull/840) — script generation and
  resource lookup assumed POSIX paths; both are now platform-independent.
- [#870](https://github.com/marcinz606/NegPy/pull/870) — the Windows updater
  wrote a swap script that broke on any profile path containing non-ASCII
  characters.

Currently **31 open** upstream pull requests, including
[openai-python#3634](https://github.com/openai/openai-python/pull/3634) (a
default Windows checkout fails four tests before any code is touched — CRLF
fixture rewriting, plus a `delenv` that deletes the variable a `setenv` just
set, because Windows' environment is case-insensitive),
[pywin32#2789](https://github.com/mhammond/pywin32/pull/2789) (tests that assume
features Windows *Home* editions don't ship),
[rust-clippy#17567](https://github.com/rust-lang/rust-clippy/pull/17567) (a
`missing_const_for_thread_local` false positive on targets with no native
`#[thread_local]`), and work in
[twine](https://github.com/pypa/twine/pull/1372),
[distutils](https://github.com/pypa/distutils/pull/427),
[alembic](https://github.com/sqlalchemy/alembic/pull/1847) and
[futures-rs](https://github.com/rust-lang/futures-rs/pull/3042).

Also:

- Filed [watchdog#1206](https://github.com/gorakhargosh/watchdog/issues/1206) —
  a test that passes in the project's own Windows CI but fails deterministically
  on native Windows 11, with the mechanism diagnosed.
- Reviewed [watchdog#1176](https://github.com/gorakhargosh/watchdog/pull/1176) —
  its regression tests skip on Windows because symlinks need elevation, so I
  verified the defect through hard links, which don't: the case the author's
  own suite couldn't reach.
- Co-author credit on [openclaw `34c90a8`](https://github.com/openclaw/openclaw/commit/34c90a8cb3fe32a657c6812d1b4087fba6c988b0)
  — orphaned Windows child-process trees — landed via maintainer PR
  [#115535](https://github.com/openclaw/openclaw/pull/115535).

## Projects

**[Ridge](https://github.com/MohammedAlkindi/ridge)** ([live](https://ridge-data.vercel.app)) —
spreadsheet analysis you can audit. Statistics, data-quality grades and
correlations are computed locally before any AI sees the file; the model can
only explain evidence that already exists, never produce a number. No API key
needed for the deterministic path. 548 tests, green in CI.

**[ProofX](https://github.com/MohammedAlkindi/proofx)** ([live](https://proofx.org)) —
directed search for mathematical counterexamples. Every evaluation lands in a
replayable ledger, and certifiable rows are exported as theorems a proof kernel
actually checks. It claims "unrefuted at this budget", never "proved".

**[Quant](https://github.com/MohammedAlkindi/quant)** — research-first quant
trading: cost-aware, out-of-sample backtesting with reproducible baselines and a
keyless FastAPI signal service. Built so a result that doesn't survive
transaction costs is reported as a failure rather than tuned until it passes.

**[Switchyard](https://github.com/MohammedAlkindi/switchyard)** ([live](https://switchyardhq.vercel.app)) —
run several AI coding agents on one repo without collisions. Each agent gets its
own git worktree and branch, and merge conflicts are predicted before anyone
merges.

**[OmanX](https://github.com/MohammedAlkindi/omanx)** ([live](https://omanx.org)) —
visa and compliance guidance for Omani scholarship students abroad, answered
only from approved government sources, with the safety-critical routing done by
deterministic classifiers rather than the model.

## Now

Getting Ridge from "works" to "someone other than me depends on it" — pilot
feedback, evidence exports, and the parts of the analysis that still need a
human to sign off. Alongside it, working the Windows-portability seam upstream:
the bugs that only appear on a machine no hosted runner can be.

## Contact

[LinkedIn](https://www.linkedin.com/in/mohammed--alkindi)
