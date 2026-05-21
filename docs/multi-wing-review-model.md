# Multi-Wing Review Model

## Purpose

This document defines the Multi-Wing Review model for `ktp-origin-audit`.

Origin Audit is a pre-judicial observation and review layer within the Kazene Trace Protocol ecosystem.  
Some trace claims are too complex to be reviewed safely from a single perspective.

Multi-Wing Review provides a structured way to examine trace claims from multiple independent review angles before dispute escalation, allocation-readiness review, or downstream governance.

In short:

```text
Single review may miss structure.
Multi-Wing Review reduces single-perspective bias.

1. Core Principle

The core principle of Multi-Wing Review is:

Multiple perspectives may improve review quality, but they do not create final authority.

Multi-Wing Review may strengthen an audit assessment, clarify uncertainty, or recommend escalation.

However, it must not:

issue legal judgment
determine final origin
assign ownership
approve allocation
replace Dispute Registry
replace Allocation Readiness
replace Royalty OS governance

Multi-Wing Review supports better observation.
It does not convert observation into verdict.

2. Why Multi-Wing Review Is Needed

Trace claims may involve several kinds of uncertainty:

structural similarity
conceptual overlap
implicit absorption
blended influence
disputed origin claims
unclear provenance
AI-mediated synthesis
missing citation
possible parallel development
downstream allocation risk

A single reviewer may focus too heavily on one dimension.

For example:

A structural reviewer may see strong pattern similarity.
A provenance reviewer may find weak access evidence.
A dispute reviewer may detect unresolved contestation.
An allocation reviewer may reject readiness.

Multi-Wing Review allows these perspectives to coexist without prematurely collapsing the case into a single conclusion.

3. Suggested Review Wings

The following wings may be used depending on the case.

3.1 Trace Structure Wing

Focus:

structural similarity
sequence of ideas
layer architecture
conceptual ordering
protocol pattern
framework resemblance

Primary question:

Does the later work show a meaningful structural relationship to the origin candidate?

This wing should not determine copying or ownership.

3.2 Provenance Wing

Focus:

explicit citation
source links
publication sequence
access signals
acknowledgement
public availability
documented reuse

Primary question:

Is there evidence that the later work had access to, cited, or relied on the origin candidate?

This wing should distinguish direct provenance from inferred structural similarity.

3.3 Linguistic and Conceptual Wing

Focus:

terminology overlap
conceptual framing
repeated key phrases
semantic similarity
distinctive vocabulary
conceptual dependency

Primary question:

Does the later work reuse or transform distinctive language or concepts from the origin candidate?

This wing should separate common discourse from distinctive conceptual borrowing.

3.4 Dispute-Risk Wing

Focus:

claimant position
respondent position
competing claims
unresolved objections
reputational risk
escalation need

Primary question:

Is this trace claim contested or likely to require Dispute Registry escalation?

This wing should preserve dispute status without resolving the dispute.

3.5 Allocation-Readiness Wing

Focus:

evidence organization
dispute status
contribution mapping
governance boundaries
readiness signals
downstream allocation risk

Primary question:

Is the case organized enough to proceed to Allocation Readiness review?

This wing must preserve the principle:

allocation readiness ≠ allocation approval
3.6 Governance Wing

Focus:

safety boundaries
overclaiming risk
legal-adjacent risk
misuse risk
review integrity
protocol compliance

Primary question:

Does the audit preserve the required governance boundaries?

Required boundaries:

{
  "not_a_verdict": true,
  "not_legal_advice": true,
  "not_ownership_determination": true,
  "not_royalty_allocation": true
}
4. Recommended Review Flow

A typical Multi-Wing Review may follow this flow:

1. Origin Audit record is created.
2. Trace Structure Wing reviews structural relationship.
3. Provenance Wing reviews citation and access evidence.
4. Linguistic and Conceptual Wing reviews terminology and concepts.
5. Dispute-Risk Wing reviews contested status.
6. Allocation-Readiness Wing reviews readiness signals.
7. Governance Wing checks safety boundaries.
8. Combined review summary is produced.
9. Recommended next step is recorded.

The combined summary should preserve differences between wings.

It should not force artificial consensus.

5. Review Output

Each wing may produce a short structured review.

Recommended fields:

{
  "wing_id": "trace-structure-wing",
  "review_focus": "structural_similarity",
  "finding": "meaningful_structural_similarity_observed",
  "confidence": 0.72,
  "uncertainty_notes": [
    "Similarity may reflect shared discourse or parallel development."
  ],
  "recommended_next_step": "Preserve as trace hypothesis and compare with provenance evidence."
}

A combined Multi-Wing Review may include:

{
  "multi_wing_review_status": "completed",
  "overall_recommendation": "requires_dispute_registry_escalation",
  "consensus_level": "partial",
  "wing_findings": [
    "trace_structure_wing",
    "provenance_wing",
    "dispute_risk_wing",
    "governance_wing"
  ]
}
6. Consensus Levels

Multi-Wing Review may use the following consensus levels:

none
weak
partial
strong
unanimous
None

Wings disagree significantly, and no safe shared assessment exists.

Weak

Some overlapping signals exist, but uncertainty remains high.

Partial

Several wings support the same direction, but important uncertainty remains.

Strong

Most wings support the same direction, with documented uncertainty.

Unanimous

All wings support the same direction.

Even unanimous review is not a verdict.
It only strengthens the review signal.

7. Recommended Overall Recommendations

A Multi-Wing Review may end with one of the following recommendations:

record_as_observed
record_as_observed_with_uncertainty
requires_more_evidence
requires_dispute_registry_escalation
requires_allocation_readiness_review
not_ready_for_allocation_review
ready_for_downstream_review

These are review recommendations, not final decisions.

8. Multi-Wing Review and Dispute Registry

Multi-Wing Review may recommend Dispute Registry escalation when:

claimant and respondent positions conflict
evidence is significant but unresolved
multiple origin candidates make competing claims
provenance evidence is weak but structural evidence is strong
allocation is being considered despite dispute risk

Recommended path:

Origin Audit
→ Multi-Wing Review
→ Dispute Registry
→ Dispute clarification
→ Allocation Readiness re-check

Multi-Wing Review should not resolve the dispute internally.

9. Multi-Wing Review and Allocation Readiness

Multi-Wing Review may recommend Allocation Readiness review when:

evidence is organized
relation type is clear
dispute status is not active
uncertainty is documented
contribution mapping remains descriptive
governance boundaries are intact

Recommended path:

Origin Audit
→ Multi-Wing Review
→ Allocation Readiness
→ Royalty OS / Allocation Layer

Important boundary:

Multi-Wing Review may recommend readiness.
Multi-Wing Review must not approve allocation.
10. Anti-Bias Function

Multi-Wing Review helps reduce several risks:

single-reviewer bias
surface-wording bias
overconfidence bias
citation bias
anti-citation bias
allocation pressure
dispute suppression
premature verdict collapse

Each wing acts as a counterweight to the others.

For example:

Trace Structure Wing may detect hidden similarity.
Provenance Wing may limit overclaiming.
Dispute-Risk Wing may prevent unsafe allocation.
Governance Wing may preserve safety boundaries.

This is the practical value of Multi-Wing Review.

11. Anti-Overclaiming Rules

Multi-Wing Review must reject the following shortcuts:

multi-wing agreement → final verdict
strong structure signal → copying
provenance gap → misconduct
conceptual overlap → ownership
allocation readiness signal → payment approval
dispute-risk signal → guilt
consensus → legal certainty

Multi-Wing Review improves audit quality.
It does not create legal or allocation authority.

12. Minimum Multi-Wing Review Checklist

Before a Multi-Wing Review is finalized, reviewers should confirm:

[ ] Each wing has a clearly defined focus.
[ ] Each wing records findings separately.
[ ] Confidence scores are bounded between 0 and 1.
[ ] Uncertainty notes are preserved.
[ ] Dispute status is checked.
[ ] Allocation readiness is not confused with allocation approval.
[ ] Governance boundaries remain intact.
[ ] No wing issues a legal or ownership verdict.
[ ] The combined summary preserves disagreements.
[ ] Recommended next step is clearly stated.
13. Example Multi-Wing Review Summary
{
  "multi_wing_review_id": "multi-wing-review-001",
  "origin_audit_example_id": "ktp-origin-audit-implicit-absorption-001",
  "review_status": "completed",
  "consensus_level": "partial",
  "wing_results": [
    {
      "wing_id": "trace-structure-wing",
      "finding": "moderate structural similarity observed",
      "confidence": 0.68
    },
    {
      "wing_id": "provenance-wing",
      "finding": "no explicit citation or access evidence found",
      "confidence": 0.54
    },
    {
      "wing_id": "dispute-risk-wing",
      "finding": "no formal dispute currently registered",
      "confidence": 0.76
    },
    {
      "wing_id": "allocation-readiness-wing",
      "finding": "not ready for allocation review",
      "confidence": 0.81
    },
    {
      "wing_id": "governance-wing",
      "finding": "safety boundaries preserved",
      "confidence": 0.9
    }
  ],
  "overall_recommendation": "record_as_observed_with_uncertainty",
  "notes": [
    "Structural similarity is meaningful but not sufficient for judgment.",
    "No allocation readiness is recommended at this stage.",
    "Further provenance evidence may be needed if the claim becomes disputed."
  ]
}
14. Relationship to Kazene Trace Protocol

Within the Kazene Trace Protocol ecosystem, Multi-Wing Review functions as a review coordination model.

Kazene Trace Protocol
→ Origin Audit
→ Multi-Wing Review
→ Dispute Registry / Allocation Readiness
→ Royalty OS / Allocation Layer

It helps ensure that trace claims are reviewed across multiple dimensions before being escalated.

Summary

Multi-Wing Review is a structured review model for complex trace claims.

It does not replace Origin Audit.
It strengthens Origin Audit.

It does not replace Dispute Registry.
It helps determine whether escalation is needed.

It does not replace Allocation Readiness.
It helps determine whether readiness review is appropriate.

Final principle:

Many wings may see more clearly,
but even many wings must not pretend to be the judge.
