---
id: under-exactoptionalpropertytypes-assigning-possibly
claim: Under exactOptionalPropertyTypes, assigning a possibly-undefined value to an
  optional property is an error. Spread the key conditionally instead.
scope: global
status: provisional
conditions:
  paths:
    - src/**/*.ts
  prose: When building an object literal with an optional field whose value may be undefined.
provenance:
  - url: https://github.com/adamstallard/igor/commit/c9b9b6e
    author: adamstallard
    at: 2026-09-13
supersedes: []
---

`{ x: maybeUndefined }` fails where `{ ...(v === undefined ? {} : { x: v }) }` passes. The pattern recurs throughout this codebase; matching it is cheaper than relaxing the compiler setting.
