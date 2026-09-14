---
id: verify-against-live-api-reasoning-about-fixtures-test-shape
claim: Verify against the live API rather than reasoning about it. Fixtures test the
  shape; only a real call tests the assumption.
scope: global
status: provisional
conditions:
  paths:
    - src/**/*.ts
  prose: Before relying on how an external API behaves — its limits, what it accepts, what
    it silently ignores — and before writing a constant derived from that behaviour.
provenance:
  - url: https://github.com/adamstallard/igor/commit/c8f4115
    author: adamstallard
    at: 2026-09-14
  - url: https://github.com/adamstallard/igor/commit/1b8aef0
    author: adamstallard
    at: 2026-09-14
  - url: https://github.com/adamstallard/igor/commit/18112e1
    author: adamstallard
    at: 2026-09-14
  - url: https://github.com/adamstallard/igor/commit/188a762
    author: adamstallard
    at: 2026-09-14
supersedes: []
---

Every substantial finding in this project came from a live call contradicting something that seemed obvious: a page size the API refuses, an identity it will not accept as an assignee, a cost five times the estimate taken from a trivial prompt, and a whole calibration subsystem built for a number the CLI reports for free. None were discoverable by reading documentation or reasoning carefully.
