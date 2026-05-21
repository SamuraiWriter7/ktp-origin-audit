# Relationship to Allocation Readiness

## Purpose

This document explains how `ktp-origin-audit` relates to Allocation Readiness within the Kazene Trace Protocol ecosystem.

Origin Audit is a pre-judicial observation and review layer.  
It records trace claims, evidence, uncertainty, dispute status, and review signals.

Allocation Readiness is a downstream preparation layer.  
It determines whether a trace claim is sufficiently organized, reviewed, and governance-safe to proceed toward a separate Royalty OS or Allocation Layer.

In short:

```text
Origin Audit prepares trace records.
Allocation Readiness checks whether they can proceed.
Royalty OS performs allocation.

1. Core Boundary

The most important boundary is:

Allocation readiness is not allocation approval.

Origin Audit may indicate that a trace claim appears ready for downstream allocation review.

However, Origin Audit must not:

approve payment
assign royalty percentages
determine ownership
determine authorship
determine legal entitlement
determine final contribution weight
bypass dispute handling
replace Royalty OS governance

A record may be ready for review without being approved for allocation.

2. Layer Relationship

The relationship between Origin Audit and Allocation Readiness can be understood as follows:

Origin Audit
→ observes trace relationships
→ records evidence
→ preserves uncertainty
→ records dispute status
→ organizes review notes
→ may recommend allocation-readiness review

Allocation Readiness
→ checks whether evidence is sufficient
→ verifies dispute status
→ checks governance boundaries
→ reviews contribution signals
→ prepares downstream allocation package
→ sends eligible cases to Royalty OS / Allocation Layer

Origin Audit prepares.
Allocation Readiness evaluates readiness.
Royalty OS allocates.

3. What Origin Audit May Provide

Origin Audit may provide the following inputs to Allocation Readiness:

trace_claim
origin_candidate or origin_candidates
derived_or_later_work
evidence_items
evidence_summary
audit_assessment
confidence score
uncertainty notes
review status
dispute status
contribution mapping signals
governance notes
recommended next step

These inputs should be treated as structured review material, not as final allocation decisions.

4. Required Preconditions for Allocation Readiness

A trace claim should only be considered for allocation-readiness review when:

evidence is clearly organized
relation type is classified
uncertainty notes are present
review status is explicit
dispute status is checked
governance safety fields are preserved
contribution mapping is descriptive, not distributive
allocation is not already approved inside Origin Audit

Recommended minimum condition:

{
  "ready_for_allocation_review": true,
  "allocation_approved": false
}

This means the case may proceed to downstream review.
It does not mean payment or royalty distribution has been approved.

5. Dispute Status Requirement

A disputed claim should not proceed directly to allocation-readiness review.

Recommended safety rule:

if dispute_status.is_disputed == true
then allocation_readiness.ready_for_allocation_review should be false

If a dispute is active or unresolved, the recommended path is:

Origin Audit
→ Dispute Registry
→ Dispute clarification
→ Allocation Readiness re-check
→ Royalty OS / Allocation Layer

This prevents unresolved disputes from being converted into payment claims.

6. Contribution Mapping Boundary

Origin Audit may include preliminary contribution mapping.

For example:

{
  "observed_role": "framework and structural influence",
  "preliminary_weight": "high",
  "allocation_weight": null
}

This is allowed because it describes a review signal.

However:

preliminary_weight ≠ allocation_weight
observed_role ≠ royalty percentage
contribution signal ≠ payment decision

Contribution mapping inside Origin Audit should remain descriptive.

Allocation weights, if any, must be determined by a separate Allocation Readiness or Royalty OS process.

7. Allocation Readiness Signals

Origin Audit may produce readiness signals such as:

not_ready
ready_for_downstream_review
requires_dispute_resolution
requires_more_evidence
requires_multi_wing_review
requires_governance_check

These signals help downstream systems decide what should happen next.

They do not authorize allocation.

8. Example Flow

A typical flow may look like this:

1. A trace claim is recorded in Origin Audit.
2. Evidence is collected and validated.
3. Reviewers confirm that the claim is not currently disputed.
4. Uncertainty notes are preserved.
5. Contribution signals are recorded descriptively.
6. Origin Audit marks the case as ready for downstream allocation review.
7. Allocation Readiness performs a separate review.
8. Royalty OS or Allocation Layer makes any actual allocation decision.

This keeps preparation, review, and allocation clearly separated.

9. Unsafe Shortcuts to Avoid

Origin Audit and Allocation Readiness must avoid the following unsafe collapses:

citation → payment
influence → entitlement
confidence → royalty percentage
readiness → approval
preliminary weight → allocation weight
trace claim → ownership
reviewed evidence → final allocation

These shortcuts are structurally unsafe.

Origin Audit exists partly to prevent these collapses.

10. Governance Boundary

All Origin Audit records that interact with Allocation Readiness should preserve the following governance boundaries:

{
  "not_a_verdict": true,
  "not_legal_advice": true,
  "not_ownership_determination": true,
  "not_royalty_allocation": true
}

These fields are especially important when allocation is being considered.

Without them, an audit record may be misread as a payment claim or ownership assertion.

11. Minimal Allocation Readiness Handoff Package

A minimal handoff package from Origin Audit to Allocation Readiness may include:

{
  "origin_audit_example_id": "ktp-origin-audit-allocation-readiness-review-001",
  "trace_claim_id": "trace-claim-allocation-readiness-001",
  "relation_type": "allocation_readiness_review",
  "evidence_summary": "available",
  "confidence": 0.82,
  "audit_assessment_status": "reviewed_for_allocation_readiness",
  "is_disputed": false,
  "ready_for_allocation_review": true,
  "allocation_approved": false,
  "recommended_next_step": "Escalate to Allocation Readiness or Royalty OS review"
}

This package should be treated as a preparation signal, not as an allocation decision.

12. Recommended Integration Model

A clean integration model is:

Origin Audit Record
        │
        ▼
Allocation Readiness Review
        │
        ▼
Governance / Dispute Re-check
        │
        ▼
Contribution Weighting Review
        │
        ▼
Royalty OS / Allocation Layer

This model ensures that evidence is not converted into payment without review.

13. Relationship to Royalty OS

Royalty OS or an Allocation Layer may eventually use Origin Audit and Allocation Readiness outputs.

However, Royalty OS should only receive cases that have passed:

evidence organization
uncertainty preservation
dispute check
readiness review
governance review
contribution weighting review

Origin Audit alone should never be enough to trigger Royalty OS allocation.

Recommended boundary:

Origin Audit = evidence and observation
Allocation Readiness = readiness and governance check
Royalty OS = allocation decision
14. Multi-Wing Review Before Allocation

Before any high-impact allocation process, Multi-Wing Review may be recommended.

Possible review wings include:

trace structure wing
provenance wing
dispute-risk wing
contribution-mapping wing
governance wing
allocation-readiness wing

The purpose is to reduce single-perspective bias before downstream allocation.

Multi-Wing Review may recommend readiness.
It should not directly assign royalties inside Origin Audit.

Summary

ktp-origin-audit and Allocation Readiness serve different roles.

Origin Audit = observes and prepares
Allocation Readiness = checks whether downstream review is appropriate
Royalty OS = performs allocation

The key principle is:

Ready for allocation review does not mean allocation approved.

Final boundary:

Trace is not payment.
Readiness is not approval.
Audit is not allocation.
