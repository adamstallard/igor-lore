---
id: gh-slurp-cannot-combined-jq-paginate-memory-filter-code
claim: gh --slurp cannot be combined with --jq. Paginate into memory and filter in code.
scope: global
status: provisional
conditions:
  paths:
    - src/*.ts
  prose: When paging a gh api call and wanting to filter the result.
provenance:
  - url: https://github.com/adamstallard/igor/commit/cfe3fef
    author: adamstallard
    at: 2026-09-13
supersedes: []
---

Pages arrive as an array of arrays, so the caller flattens before filtering.
