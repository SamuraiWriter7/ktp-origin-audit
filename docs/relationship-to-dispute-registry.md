# Relationship to Dispute Registry

## Purpose

This document explains how `ktp-origin-audit` relates to a Dispute Registry within the Kazene Trace Protocol ecosystem.

Origin Audit is a pre-judicial observation and review layer.  
It records trace-related claims, evidence, uncertainty, and dispute status.

A Dispute Registry is a downstream governance layer.  
It manages formally disputed claims, tracks dispute lifecycle states, and preserves the procedural history of contested trace relationships.

In short:

```text
Origin Audit records disputes.
Dispute Registry manages disputes.

1. Core Boundary

The most important boundary is:

Origin Audit may identify and preserve a dispute, but it must not resolve the dispute.

Origin Audit may record that:

a trace claim exists
the claim is contested
claimant and respondent positions differ
evidence is incomplete
uncertainty remains
escalation is recommended

However, Origin Audit must not:

declare a winning side
determine final origin
assign blame
determine legal infringement
determine ownership
approve allocation
resolve the dispute internally

This boundary prevents Origin Audit from becoming an accidental court.

2. Layer Relationship

The relationship between Origin Audit and Dispute Registry can be understood as follows:

Origin Audit
→ observes trace claims
→ records evidence
→ preserves uncertainty
→ detects dispute status
→ recommends escalation

Dispute Registry
→ receives disputed claims
→ records formal dispute lifecycle
→ tracks claimant and respondent positions
→ manages review status
→ records resolution state
→ produces downstream governance signals

Origin Audit prepares the case.
Dispute Registry manages the contested process.

3. When a Case Should Be Escalated

An Origin Audit record should be considered for escalation to a Dispute Registry when:

dispute_status.is_disputed is true
a claimant contests the origin or influence relationship
a respondent denies the claimed trace relationship
multiple origin candidates make competing claims
evidence is significant but unresolved
allocation review is being considered but dispute remains active
the case has high governance, reputational, or economic impact
confidence is insufficient for downstream readiness
human or Multi-Wing Review recommends escalation

Recommended escalation signal:

{
  "is_disputed": true,
  "dispute_reference": {
    "registry": "Dispute Registry",
    "status": "not_yet_registered",
    "suggested_dispute_id": "dispute-trace-claim-001"
  }
}
4. What Origin Audit Should Pass Forward

When escalating to a Dispute Registry, Origin Audit should pass forward structured information such as:

trace_claim
origin_candidate or origin_candidates
derived_or_later_work
claimant position
respondent position
evidence items
evidence summary
confidence score
uncertainty notes
review status
dispute status
allocation readiness status
governance notes

The purpose is not to decide the dispute, but to provide a clean evidence package for downstream governance.

5. Dispute Registry Responsibilities

A Dispute Registry may be responsible for:

assigning a dispute ID
recording dispute lifecycle state
preserving claimant statements
preserving respondent statements
tracking submitted evidence
recording review events
recording status transitions
linking to Origin Audit records
linking to Allocation Readiness records
documenting resolution or unresolved status

Possible dispute lifecycle states may include:

not_yet_registered
submitted
under_review
needs_more_evidence
contested
resolved
dismissed
superseded
reopened

These states belong to the Dispute Registry, not to Origin Audit.

6. Origin Audit Status vs Dispute Status

Origin Audit and Dispute Registry use related but distinct statuses.

Origin Audit Status

Origin Audit may use statuses such as:

observed
observed_with_uncertainty
disputed_and_unresolved
reviewed_for_allocation_readiness

These describe the audit assessment.

Dispute Registry Status

A Dispute Registry may use statuses such as:

submitted
under_review
contested
resolved
dismissed
reopened

These describe the procedural state of a formal dispute.

The two should not be confused.

7. Disputed Claims and Allocation

A disputed claim should not proceed directly to allocation review.

Recommended safety rule:

if dispute_status.is_disputed == true
then allocation_readiness.ready_for_allocation_review should be false

This rule prevents unresolved disputes from being converted into payment, ownership, or royalty decisions.

Origin Audit may recommend:

Escalate to Dispute Registry before allocation-readiness review.

But it must not bypass dispute handling.

8. Example Flow

A typical flow may look like this:

1. A trace claim is recorded in Origin Audit.
2. Evidence suggests possible structural influence.
3. The later creator contests the claim.
4. Origin Audit marks the case as disputed.
5. Allocation readiness is set to false.
6. The case is recommended for Dispute Registry escalation.
7. Dispute Registry opens a formal dispute record.
8. Additional review occurs outside Origin Audit.
9. Only after dispute clarification may downstream allocation review be considered.

This keeps the process safe and layered.

9. Anti-Collapse Principle

Origin Audit must avoid the following unsafe collapses:

dispute → guilt
claim → verdict
similarity → infringement
absence of citation → misconduct
confidence → truth
dispute record → allocation approval

A dispute record means the matter requires governance.
It does not mean the claim is true or false.

10. Multi-Wing Review and Dispute Escalation

Multi-Wing Review may help decide whether a case should be escalated.

Different wings may review:

structural similarity
conceptual overlap
provenance evidence
claimant position
respondent position
dispute risk
allocation-readiness risk

However, Multi-Wing Review inside Origin Audit should still remain pre-judicial.

It may recommend escalation.
It should not replace Dispute Registry resolution.

11. Governance Boundary

Origin Audit must preserve the following governance boundaries even when a case is disputed:

{
  "not_a_verdict": true,
  "not_legal_advice": true,
  "not_ownership_determination": true,
  "not_royalty_allocation": true
}

These fields are especially important in disputed cases.

A disputed trace claim is more likely to be misused as an accusation, so the safety boundaries must remain explicit.

12. Recommended Integration Model

A clean integration model is:

Origin Audit Record
        │
        ▼
Dispute Registry Entry
        │
        ▼
Dispute Review / Governance Process
        │
        ▼
Resolution or Unresolved Status
        │
        ▼
Allocation Readiness Re-check
        │
        ▼
Royalty OS / Allocation Layer

This model ensures that disputes are handled before allocation.

13. Minimal Dispute Handoff Package

A minimal handoff package from Origin Audit to Dispute Registry should include:

{
  "origin_audit_example_id": "ktp-origin-audit-disputed-trace-claim-001",
  "trace_claim_id": "trace-claim-disputed-001",
  "relation_type": "disputed_trace_claim",
  "claimant_position": "preserved",
  "respondent_position": "preserved",
  "evidence_summary": "available",
  "confidence": 0.55,
  "audit_assessment_status": "disputed_and_unresolved",
  "allocation_ready": false,
  "recommended_next_step": "Escalate to Dispute Registry"
}

This package should be treated as a structured input, not a conclusion.

Summary

ktp-origin-audit and Dispute Registry serve different roles.

Origin Audit = pre-judicial observation and dispute detection
Dispute Registry = formal dispute lifecycle management

Origin Audit prepares disputed trace claims safely.
Dispute Registry handles the contested process.

Final principle:

Do not resolve disputes where they are only meant to be observed.
