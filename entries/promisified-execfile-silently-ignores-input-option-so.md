---
id: promisified-execfile-silently-ignores-input-option-so
claim: Promisified execFile silently ignores an input option, so anything reading stdin
  hangs forever. Spawn and write to stdin instead.
scope: global
status: provisional
conditions:
  paths:
    - src/**/*.ts
  prose: When shelling out to a command that reads stdin — gh api --input -, git
    hash-object, anything piped.
provenance:
  - url: https://github.com/adamstallard/igor/commit/ec71667
    author: adamstallard
    at: 2026-09-13
supersedes: []
---

The `input` option belongs to `execFileSync`, not to `execFile`. The promisified form accepts it, ignores it, and the child waits on input that never arrives — so the failure is a hang rather than an error, which is the expensive kind to diagnose.
