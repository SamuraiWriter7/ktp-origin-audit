## [0.1.2] - 2026-05-21

### Added

- Added architecture overview documentation:
  - `docs/architecture-overview.md`

### Included

- Added Mermaid diagrams for:
  - high-level KTP ecosystem architecture
  - internal Origin Audit layer structure
  - example trace claim flow
  - anti-collapse model
  - Multi-Wing Review position

### Updated

- Updated `README.md` to include:
  - `docs/architecture-overview.md` in Repository Structure
  - `docs/architecture-overview.md` in Start Here
  - Architecture Overview section
  - v0.1.2 status block
  - architecture overview references in relationship sections

### Defined

- Origin Audit as the layer between Trace Intelligence Spec and downstream governance.
- The architectural boundary between:
  - Origin Audit
  - Dispute Registry
  - Allocation Readiness
  - Royalty OS / Allocation Layer
- The anti-collapse model preventing unsafe shortcuts such as:
  - similarity → copying
  - trace → ownership
  - readiness → payment approval

### Status

This release extends the Origin Audit layer with architecture overview documentation and Mermaid diagrams, making the repository structure and governance flow easier to understand.

## [0.1.1] - 2026-05-21

### Added

- Added a new Multi-Wing Review example:
  - `examples/multi-wing-review.example.json`

### Updated

- Updated `schemas/origin-audit-example.schema.json` to support the `multi-wing-review` example type.
- Added schema definitions for:
  - `source_audit_record`
  - `review_context`
  - `wing_reviews`
  - `combined_review`
- Updated `.github/workflows/validate-examples.yml` to include:
  - `examples/multi-wing-review.example.json`
  - Multi-Wing Review-specific validation checks
  - wing-level confidence validation
  - source audit record relation consistency checks

### Defined

- Multi-Wing Review as a structured review model for re-evaluating existing Origin Audit records from multiple perspectives.
- The distinction between:
  - Multi-Wing Review and final judgment
  - review consensus and verdict
  - readiness recommendation and allocation approval

### Safety Rules

- Multi-Wing Review examples must preserve governance boundaries:
  - `not_a_verdict: true`
  - `not_legal_advice: true`
  - `not_ownership_determination: true`
  - `not_royalty_allocation: true`
- Multi-Wing Review examples must not directly approve allocation.
- Multi-Wing Review examples must not convert review consensus into final authority.

### Status

This release extends the Origin Audit layer with a concrete Multi-Wing Review example and validation support, making the review model more operational while preserving the pre-judicial boundary of the repository.
