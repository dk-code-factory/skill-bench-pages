# Skill Bench Pages

Public benchmark dashboard and reports for comparing agent review skills.

**Dashboard:** https://dk-code-factory.github.io/skill-bench-pages/

This repository contains generated benchmark exports. Tooling, source evidence, and skill tuning
campaigns are maintained separately in the private Skill Bench repository. Tuning evidence is
excluded from public reports, scores, answer-key sources, and embedded dashboard data.

## Publishing updates

1. In the private Skill Bench checkout, run `make bench-publish` and
   `make bench-publish-check`. These render completed, classified benchmark snapshots without
   making model calls.
2. Run `make bench-export OUTPUT=/path/to/skill-bench-pages/docs`. The exporter copies only its
   generated public inventory and removes superseded exports.
3. Commit and push to `main`. GitHub Pages deploys from `main` at `/docs`.

Cohort-local results remain distinct from the reviewed, sealed canonical answer key. Selecting a
skill through tuning requires a separate benchmark evaluation; tuning trials are never promoted.
