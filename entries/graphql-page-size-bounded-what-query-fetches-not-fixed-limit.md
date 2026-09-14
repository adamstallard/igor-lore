---
id: graphql-page-size-bounded-what-query-fetches-not-fixed-limit
claim: GraphQL page size is bounded by what the query fetches, not by a fixed limit.
  Start below the measured ceiling and halve on refusal.
scope: global
status: active
conditions:
  paths:
    - src/github-adapter.ts
  prose: When paginating a GitHub GraphQL search that fetches issue or pull request bodies.
provenance:
  - url: https://github.com/adamstallard/igor/commit/c8f4115
    author: adamstallard
    at: 2026-09-13
supersedes: []
reviewed:
  by: adamstallard
  at: 2026-09-14
---

Measured: 100 issues per page is refused with "Resource limits for this query exceeded" once bodies are included; 30 succeeds. The ceiling moves with body length, so it is a property of the repository rather than a constant worth hardcoding.
