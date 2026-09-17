---
id: archive-openspec-change-every-requirement-met-not-every-task
claim: Archive an OpenSpec change when every requirement is met, not when every task is
  ticked.
scope: global
status: active
conditions:
  paths:
    - openspec/**
  prose: When deciding whether an OpenSpec change is ready to archive, or reading a
    tasks.md with unticked boxes and wondering whether the change is done.
provenance:
  - author: adamstallard
    at: 2026-09-17
supersedes: []
reviewed:
  by: adamstallard
  at: 2026-09-17
---

Requirements live in the spec deltas and define what the change must be true of. Tasks are a plan for getting there, and a plan can be wrong: a task can be superseded, split, or found unnecessary once the code exists. Gating the archive on a fully ticked tasks.md holds a finished change open, and invites ticking boxes to clear the gate rather than because the work happened. An in-force requirement that turns out to be unimplemented is a bug to fix against the live spec, not a reason to keep the change unarchived.
