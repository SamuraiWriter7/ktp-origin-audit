# Origin Audit v1.0 Graduation Criteria

## Purpose

This document defines the graduation criteria for promoting `ktp-origin-audit` from an experimental v0.1 repository to **Origin Audit v1.0** within the Kazene Trace Protocol ecosystem.

Origin Audit v1.0 should not merely provide examples.  
It should define a stable pre-judicial audit layer for observing, reviewing, validating, and escalating trace-related claims before judgment, dispute resolution, or allocation.

In short:

```text
v0.1 = examples and validation prototype
v1.0 = stable pre-judicial origin audit layer

Core Graduation Principle

Origin Audit may graduate to v1.0 only if it preserves the following principle:

Audit records are not verdicts.

This principle must remain structurally enforced across:

examples
schemas
workflows
review guidelines
audit methodology
dispute escalation
allocation-readiness handling
README documentation

If Origin Audit begins to function as an ownership judgment, legal ruling, plagiarism detector, or royalty allocator, it should not be considered ready for v1.0.

1. Required Repository Scope

To qualify for v1.0, ktp-origin-audit should clearly define its scope as:

Pre-judicial observation and review layer for trace claims.

It must explicitly state that it is not:

a legal judgment system
a copyright enforcement system
a plagiarism detector
a final origin authority
a royalty allocation engine
an ownership registry

The repository should focus on:

observing trace relationships
preserving uncertainty
organizing evidence
recording dispute status
preparing downstream review
validating audit structure
2. Required Example Categories

Origin Audit v1.0 should include at least the following five validated example categories:

explicit-citation
implicit-absorption
blended-influence
disputed-trace-claim
allocation-readiness-review

Each category should have:

one valid JSON example
schema validation coverage
relation type alignment
confidence score
evidence items
review status
dispute status
allocation-readiness status
governance safety notes
2.1 Explicit Citation

Must demonstrate that direct citation is evidence of a trace relationship, but not ownership or allocation approval.

2.2 Implicit Absorption

Must demonstrate how to record possible structural influence without explicit citation while preserving uncertainty.

2.3 Blended Influence

Must demonstrate how to record distributed influence from multiple origin candidates without reducing the case to a single origin.

2.4 Disputed Trace Claim

Must demonstrate how to preserve claimant and respondent positions without resolving the dispute internally.

2.5 Allocation Readiness Review

Must demonstrate that allocation readiness is not allocation approval.

3. Required Schema Stability

Origin Audit v1.0 should include a stable schema:

schemas/origin-audit-example.schema.json

The schema should validate:

example_id
example_type
protocol
summary
trace_claim
evidence
audit_assessment
review_status
dispute_status
allocation_readiness
governance_notes
metadata

The schema should enforce the following safety constraints:

not_a_verdict: true
not_legal_advice: true
not_ownership_determination: true
not_royalty_allocation: true

It should also ensure that:

confidence is between 0 and 1
relation types match example types
disputed claims do not proceed directly to allocation review
allocation approval is not permitted inside Origin Audit records
only allocation-readiness examples may set ready_for_allocation_review: true
4. Required Validation Workflow

Origin Audit v1.0 should include an automated validation workflow:

.github/workflows/validate-examples.yml

The workflow should validate:

JSON syntax
schema compliance
required example files
confidence score range
relation type consistency
claim type consistency
governance boundary fields
dispute/allocation safety rules

A v1.0 release should not be created unless validation passes.

Recommended validation outcome:

All Origin Audit examples passed validation.
5. Required Review Guidelines

Origin Audit v1.0 should include:

docs/review-guidelines.md

This document should define the review culture of Origin Audit.

It should clearly state:

audit examples are not verdicts
observation must be separated from judgment
structural similarity is not proof of copying
explicit citation is not allocation approval
disputed claims must be preserved, not prematurely resolved
allocation readiness is not allocation approval
confidence scores are review signals, not truth scores
Multi-Wing Review may be used for complex cases

Without review guidelines, Origin Audit remains a data format rather than a review culture.

6. Required Audit Methodology

Origin Audit v1.0 should include:

docs/audit-methodology.md

This document should define how an audit is conducted.

It should include:

audit inputs
relation type classification
evidence collection
evidence strength
structural similarity review
implicit absorption review
blended influence review
dispute review
allocation-readiness review
confidence assessment
governance boundary checks
minimum valid audit checklist
anti-overclaiming rules

The methodology should make the audit process repeatable without turning it into automatic judgment.

7. Required Relationship to Trace Intelligence Spec

Origin Audit v1.0 should include:

docs/relationship-to-trace-intelligence-spec.md

This document should explain how Origin Audit relates to the broader Trace Intelligence Specification.

The relationship should be defined as:

Trace Intelligence Spec = structural language
Origin Audit = applied review and observation layer

Origin Audit should not replace Trace Intelligence Spec.
It should operationalize it through examples, methodology, validation, and review culture.

8. Required Dispute Boundary

Origin Audit v1.0 should clearly define its boundary with dispute handling.

It may:

record dispute status
preserve claimant positions
preserve respondent positions
recommend escalation
prepare evidence for dispute review

It must not:

resolve disputes
declare winners
assign blame
determine ownership
determine legal infringement

A future integration document may define:

docs/relationship-to-dispute-registry.md

Recommended boundary:

Origin Audit records disputes.
Dispute Registry manages disputes.
9. Required Allocation Boundary

Origin Audit v1.0 should clearly define its boundary with allocation and royalty systems.

It may:

organize evidence for downstream allocation review
record whether a case is ready for allocation review
preserve contribution mapping signals
recommend escalation to Allocation Readiness

It must not:

approve allocation
assign royalty percentages
determine payment
determine ownership
replace Royalty OS governance

Recommended boundary:

Origin Audit prepares.
Allocation Readiness reviews.
Royalty OS allocates.
10. Required Governance Safety Fields

All v1.0-compatible examples should include governance fields.

Minimum required governance fields:

{
  "not_a_verdict": true,
  "not_legal_advice": true,
  "not_ownership_determination": true,
  "not_royalty_allocation": true
}

These fields are not decorative.

They are safety constraints that prevent Origin Audit from collapsing into premature judgment.

11. Required Confidence Discipline

Origin Audit v1.0 should use confidence scores carefully.

Recommended confidence interpretation:

0.00–0.39 = low
0.40–0.59 = medium
0.60–0.79 = medium_high
0.80–1.00 = high

However:

confidence ≠ truth
confidence ≠ legal certainty
confidence ≠ ownership
confidence ≠ allocation weight

A v1.0 Origin Audit record should always preserve uncertainty notes, even when confidence is high.

12. Required Anti-Overclaiming Rules

Origin Audit v1.0 should explicitly reject the following unsafe shortcuts:

similarity → copying
citation → ownership
confidence → truth
readiness → approval
dispute → guilt
absence of citation → misconduct
influence → allocation
trace → verdict

A repository that allows these collapses should not be considered v1.0-ready.

13. Optional but Recommended v1.0 Enhancements

The following are not strictly required for v1.0, but are recommended:

docs/relationship-to-dispute-registry.md
docs/relationship-to-allocation-readiness.md
docs/multi-wing-review-model.md
tests/
negative examples
compliance test runner
CHANGELOG.md
CITATION.cff
SECURITY.md
CONTRIBUTING.md

These may be added before or after v1.0 depending on repository maturity.

14. Graduation Checklist

Origin Audit may be considered ready for v1.0 when the following checklist is satisfied:

[ ] README defines Origin Audit as a pre-judicial observation layer.
[ ] Five core examples are present.
[ ] All examples validate against the schema.
[ ] Schema enforces governance safety boundaries.
[ ] GitHub Actions validation passes.
[ ] Review Guidelines are present.
[ ] Audit Methodology is present.
[ ] Relationship to Trace Intelligence Spec is documented.
[ ] Dispute boundary is documented.
[ ] Allocation boundary is documented.
[ ] Confidence scores are bounded and explained.
[ ] Allocation approval is prohibited inside Origin Audit.
[ ] Disputed claims cannot proceed directly to allocation review.
[ ] Governance notes are required in all examples.
[ ] Anti-overclaiming rules are documented.
[ ] License and citation files are present.
[ ] Changelog documents the v1.0 release.
15. Suggested v1.0 Release Definition

A possible v1.0 release may be defined as:

Origin Audit v1.0 is the first stable pre-judicial audit layer for observing, reviewing, validating, and escalating trace claims within the Kazene Trace Protocol ecosystem.

It provides:

validated examples
a reusable schema
automated validation
review guidelines
audit methodology
governance boundaries
escalation principles

It does not provide:

legal judgment
authorship determination
ownership assignment
plagiarism ruling
royalty allocation
16. Versioning Guidance

Recommended version progression:

v0.1.0 = initial examples, schema, and validation workflow
v0.2.0 = expanded docs and relationship documents
v0.3.0 = dispute and allocation integration notes
v0.4.0 = Multi-Wing Review model and negative examples
v1.0.0 = stable Origin Audit layer

This progression allows the repository to mature without rushing into final authority.

Summary

Origin Audit v1.0 should represent a stable, safe, and reviewable layer for trace-related claims.

Its purpose is not to judge faster.
Its purpose is to prevent unsafe judgment.

The repository may graduate to v1.0 only when it can reliably preserve the difference between:

trace and ownership
evidence and verdict
review and enforcement
readiness and approval
audit and allocation

Final guiding principle:

A mature Origin Audit system does not rush to decide.
It makes responsible decision-making possible elsewhere.
