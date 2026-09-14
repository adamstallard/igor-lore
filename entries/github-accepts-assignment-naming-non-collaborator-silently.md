---
id: github-accepts-assignment-naming-non-collaborator-silently
claim: GitHub accepts an assignment naming a non-collaborator and silently drops them.
  Read the assignees back rather than trusting the call succeeded.
scope: global
status: active
conditions:
  paths:
    - src/github*.ts
  prose: When assigning anyone to an issue or pull request.
provenance:
  - url: https://github.com/adamstallard/igor/commit/ec71667
    author: adamstallard
    at: 2026-09-13
  - url: https://github.com/adamstallard/igor/commit/c8f4115
    author: adamstallard
    at: 2026-09-13
supersedes: []
reviewed:
  by: adamstallard
  at: 2026-09-14
---

The API returns 200 and an assignees array that does not contain the person asked for. A claim that did not stick must refuse the work, because proceeding means working an item nobody can see is held.
