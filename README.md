# Mohammed Alkindi

CS at UC San Diego, data analytics at Shell. I build tools that keep a result
checkable — where a number came from, what it rests on, and the point where it
stops being supported.

Most of what I ship is deterministic first: compute the evidence, then let a
model explain it. Never the other way round.

## Open source

Merged upstream:

- [simple-statistics#814](https://github.com/simple-statistics/simple-statistics/pull/814) —
  `sampleRankCorrelation` returned a different answer for the same paired data
  depending on row order whenever values tied; ties now share their average rank.
- [simple-statistics#819](https://github.com/simple-statistics/simple-statistics/pull/819) —
  a fresh Windows clone failed `npm test` before running a single test, because
  the linter chokes on CRLF; the repo's line endings are normalised to LF.
- [watchdog#1204](https://github.com/gorakhargosh/watchdog/pull/1204) — renaming
  a file to a different case on Windows emitted a spurious deletion before the
  rename; the false deletion is now coalesced away.
- [watchdog#1205](https://github.com/gorakhargosh/watchdog/pull/1205) — the docs
  claimed `BaseThread` inherits its daemon flag from the creating thread; it
  always runs as a daemon, and the docs now say so.

Open:

- [alembic#1847](https://github.com/sqlalchemy/alembic/pull/1847) — approved,
  awaiting merge — confirms a long-open `version_path` report is fixed and pins
  it with the tests the maintainer asked for.
- [multer#1450](https://github.com/expressjs/multer/pull/1450) — a clean clone
  fails 12 tests on Windows before any code is touched, because Git rewrites
  fixture line endings on checkout; the fixtures are now protected.
- [tqdm#1790](https://github.com/tqdm/tqdm/pull/1790) — the deprecated
  `tqdm._utils` shim re-exported names that no longer exist and raised on
  import; the dead re-exports are dropped.

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

**[Ridge](https://github.com/MohammedAlkindi/Ridge)** — spreadsheet analysis you
can audit. Statistics, data-quality grades and correlations are computed locally
before any AI sees the file; the model can only explain evidence that already
exists, never produce a number. No API key needed for the deterministic path.

**[ProofX](https://github.com/MohammedAlkindi/ProofX)** — directed search for
mathematical counterexamples. Every evaluation lands in a replayable ledger, and
certifiable rows are exported as Lean 4 theorems the kernel actually checks. It
claims "unrefuted at this budget", never "proved".

**[Switchyard](https://github.com/MohammedAlkindi/Switchyard)** — run several AI
coding agents on one repo without collisions. Each agent gets its own git
worktree and branch, and merge conflicts are predicted before anyone merges.

**[OmanX](https://github.com/MohammedAlkindi/OmanX)** — visa and compliance
guidance for Omani scholarship students abroad, answered only from approved
government sources, with the safety-critical routing done by deterministic
classifiers rather than the model.

## Now

Getting Ridge from "works" to "someone other than me depends on it" — pilot
feedback, evidence exports, and the parts of the analysis that still need a
human to sign off.

## Contact

[alkindix.com](https://www.alkindix.com) ·
[LinkedIn](https://www.linkedin.com/in/mohammed--alkindi) ·
alkindi.ceo@gmail.com
