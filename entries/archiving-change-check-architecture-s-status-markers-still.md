---
id: archiving-change-check-architecture-s-status-markers-still
claim: When archiving a change, check that the architecture's status markers still
  describe reality.
scope: global
status: provisional
conditions:
  paths:
    - openspec/**
  prose: When archiving an OpenSpec change, or otherwise marking work complete in one
    place while a design document tracks its status in another.
provenance:
  - url: https://github.com/adamstallard/igor/commit/1535ca6
    author: adamstallard
    at: 2026-09-14
supersedes: []
---

Status recorded in two places drifts, and the copy nobody edits goes quiet rather than wrong. Thirteen sections sat marked scoped or planned for work that had shipped, and the README announced that only the lore half existed while the whole loop was running against live repositories.
