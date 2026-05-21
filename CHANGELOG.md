# Changelog

All notable changes to this project will be documented in this file.

This repository follows a simple versioning model during the early Origin Audit phase.

---

## [0.1.0-draft] - 2026-05-21

### Added

- Initial `ktp-origin-audit` repository structure.
- Added five core Origin Audit examples:
  - `examples/explicit-citation.example.json`
  - `examples/implicit-absorption.example.json`
  - `examples/blended-influence.example.json`
  - `examples/disputed-trace-claim.example.json`
  - `examples/allocation-readiness-review.example.json`
- Added JSON Schema:
  - `schemas/origin-audit-example.schema.json`
- Added GitHub Actions validation workflow:
  - `.github/workflows/validate-examples.yml`
- Added review and methodology documents:
  - `docs/review-guidelines.md`
  - `docs/audit-methodology.md`
- Added ecosystem relationship documents:
  - `docs/relationship-to-trace-intelligence-spec.md`
  - `docs/relationship-to-dispute-registry.md`
  - `docs/relationship-to-allocation-readiness.md`
  - `docs/multi-wing-review-model.md`
- Added v1.0 graduation criteria:
  - `docs/origin-audit-v1.0-graduation-criteria.md`

### Defined

- Origin Audit as a pre-judicial observation and review layer.
- Core principle: `Audit examples are not verdicts.`
- Governance safety boundaries:
  - `not_a_verdict: true`
  - `not_legal_advice: true`
  - `not_ownership_determination: true`
  - `not_royalty_allocation: true`
- Distinction between:
  - trace and ownership
  - evidence and verdict
  - dispute and resolution
  - allocation readiness and allocation approval

### Validation

- Added automated validation for:
  - JSON syntax
  - schema compliance
  - relation type consistency
  - claim type consistency
  - confidence score range
  - dispute/allocation safety rules
  - governance safety fields

### Status

This release is an experimental draft intended to establish the minimum working structure of the Origin Audit layer within the Kazene Trace Protocol ecosystem.
