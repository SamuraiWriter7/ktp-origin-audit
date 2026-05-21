# Audit Methodology

## Purpose

This document defines the basic audit methodology for `ktp-origin-audit`.

Origin Audit is a pre-judicial observation layer within the Kazene Trace Protocol ecosystem.  
Its purpose is to organize trace-related claims in a structured, reviewable, and non-final form.

This methodology explains how reviewers should examine origin candidates, later works, evidence items, uncertainty, dispute status, and allocation-readiness signals.

Origin Audit does not determine legal ownership, authorship, plagiarism, copyright infringement, or royalty allocation.

---

## Core Methodological Principle

The central methodological principle is:

> **Observe first.  
> Review carefully.  
> Judge elsewhere.**

Origin Audit exists before judgment.

It records:

- what is observed
- what is claimed
- what is uncertain
- what is disputed
- what may require escalation
- what may be ready for downstream review

It does not issue final conclusions.

---

## 1. Audit Scope

An Origin Audit may examine trace relationships involving:

- explicit citation
- implicit absorption
- structural similarity
- conceptual overlap
- blended influence
- disputed origin claims
- pre-allocation review readiness

An Origin Audit may involve:

- human-created works
- AI-generated works
- AI-assisted works
- specifications
- articles
- essays
- protocols
- conceptual frameworks
- implementation notes
- public repository content

The methodology is designed for structural and trace analysis, not for legal enforcement.

---

## 2. Audit Inputs

A basic Origin Audit should begin with the following inputs.

### 2.1 Origin Candidate

The earlier work, source, framework, or concept that may have influenced the later work.

Recommended fields:

```text
id
title
creator
source_type
publication_status
reference_url
observed_contribution_type

2.2 Later Work

The later work or output being compared against the origin candidate.

Recommended fields:

id
title
creator
source_type
publication_status
reference_url
2.3 Trace Claim

The claim being examined.

Recommended fields:

claim_id
claim_type
relation_type
claim_statement

The trace claim should be written as an observation or hypothesis, not as a verdict.

3. Audit Workflow

The recommended workflow is:

1. Identify the trace claim
2. Identify origin candidate or candidates
3. Identify the later work
4. Collect evidence items
5. Classify the relation type
6. Assess uncertainty
7. Record dispute status
8. Review allocation-readiness signals
9. Preserve governance boundaries
10. Recommend next step

Each step should preserve the distinction between evidence and judgment.

4. Relation Type Classification

Origin Audit currently uses five main relation types.

4.1 Explicit Citation

A later work directly cites, links to, or acknowledges an earlier source.

Recommended handling:

explicit citation → observed trace relationship
explicit citation ≠ ownership determination
explicit citation ≠ allocation approval
4.2 Implicit Absorption

A later work appears to absorb structural or conceptual features from an earlier source without explicit citation.

Recommended handling:

implicit absorption → trace hypothesis
implicit absorption ≠ proven copying
implicit absorption ≠ proven misconduct
4.3 Blended Influence

A later work appears to combine influence from multiple origin candidates.

Recommended handling:

blended influence → distributed trace pattern
blended influence ≠ exclusive origin claim
4.4 Disputed Trace Claim

A trace relationship is claimed by one party but contested or unresolved.

Recommended handling:

disputed trace claim → preserve and escalate if needed
disputed trace claim ≠ resolved judgment
4.5 Allocation Readiness Review

A trace claim has been organized enough to be considered for downstream allocation-readiness review.

Recommended handling:

allocation readiness → may proceed to downstream review
allocation readiness ≠ allocation approval
5. Evidence Collection

Evidence should be recorded as discrete evidence items.

Each evidence item should include:

evidence_id
evidence_type
description
observed_features
strength

Optional fields may include:

location
related_origin_candidate
submitted_by

Evidence should be concrete enough for another reviewer to inspect.

6. Evidence Types

Common evidence types include:

direct_citation
acknowledgement
explicit_reference
structural_similarity
conceptual_overlap
protocol_pattern_similarity
absence_of_explicit_citation
source_distribution
review_record
dispute_check
independent_development_claim
insufficient_access_evidence

Evidence types should describe the kind of observation being made, not the final conclusion.

7. Evidence Strength

Evidence strength may be classified as:

weak
moderate
strong
Weak Evidence

Weak evidence may include:

vague resemblance
shared general topic
common terminology
broad cultural similarity
unsupported assertion

Weak evidence should not support strong conclusions.

Moderate Evidence

Moderate evidence may include:

identifiable structural similarity
conceptual overlap
similar sequence of ideas
repeated pattern alignment
partial acknowledgement
plausible but incomplete trace relationship

Moderate evidence may support a trace hypothesis, but not a verdict.

Strong Evidence

Strong evidence may include:

direct citation
explicit acknowledgement
clear source link
documented reuse
strong structural alignment with supporting context
confirmed review record

Strong evidence may support escalation or downstream review, but still does not automatically determine ownership or allocation.

8. Structural Similarity Review

When reviewing structural similarity, reviewers should compare:

sequence of ideas
layer structure
conceptual ordering
terminology clusters
protocol patterns
governance structure
evidence-handling patterns
review and escalation logic

Reviewers should not rely only on surface wording.

A work may use different words while preserving a similar structure.
A work may also use similar words while having a different structure.

The audit should focus on structure, not accusation.

9. Implicit Absorption Review

Implicit absorption should be handled with special caution.

Reviewers should ask:

Is the similarity structural or merely topical?
Is the pattern uncommon enough to matter?
Is there evidence of exposure or access?
Could the similarity come from shared discourse?
Could this be parallel development?
Could AI mediation have blended the trace?
Are there multiple possible origin candidates?

Implicit absorption should usually be marked as:

assessment_status: observed_with_uncertainty

It should not be treated as final proof.

10. Blended Influence Review

For blended influence, reviewers should identify each candidate’s possible role.

Possible contribution roles include:

structural framework influence
conceptual language influence
protocol pattern influence
stylistic influence
governance framing influence
implementation pattern influence

Preliminary contribution mapping may be recorded, but it must not be treated as allocation.

Recommended boundary:

preliminary_weight ≠ allocation_weight
11. Dispute Review

When a trace claim is disputed, the audit must preserve both sides.

A disputed audit record should include:

claimant position
respondent position
evidence submitted by each side
unresolved uncertainty
dispute status
recommended escalation path

Origin Audit should not resolve disputes internally.

Recommended path:

Origin Audit
→ Dispute Registry
→ Allocation Readiness
→ Royalty OS / Allocation Layer
12. Allocation Readiness Review

Allocation readiness should only be considered when:

evidence is organized
relation type is clear
uncertainty is documented
dispute status is checked
review status is explicit
governance boundaries are preserved

Even when ready, the record must state:

allocation_approved: false

Origin Audit may prepare a claim for allocation review.
It must not approve payment, royalty percentage, or ownership.

13. Confidence Assessment

Confidence should be recorded as a number between 0 and 1.

Suggested interpretation:

0.00–0.39 = low confidence
0.40–0.59 = medium confidence
0.60–0.79 = medium-high confidence
0.80–1.00 = high confidence

However, confidence is only a review signal.

It is not:

truth
legal certainty
moral judgment
allocation weight
proof of ownership

A high-confidence trace relationship may still require dispute review or governance review.

14. Governance Boundary Check

Every Origin Audit record should preserve the following constraints:

not_a_verdict: true
not_legal_advice: true
not_ownership_determination: true
not_royalty_allocation: true

These fields are methodological safety constraints.

If any of these boundaries are removed, weakened, or contradicted, the record should not be treated as a valid Origin Audit record.

15. Recommended Output Statuses

An audit may end with one of the following practical outcomes.

Observed

A trace relationship is clearly observed, often through explicit citation.

Observed with Uncertainty

A possible trace relationship is observed, but evidence is incomplete or ambiguous.

Requires Review

The case needs further human, AI-assisted, or Multi-Wing Review.

Requires Escalation

The case is disputed, high-impact, or unsuitable for direct handling inside Origin Audit.

Ready for Downstream Review

The case may proceed to Allocation Readiness or another downstream governance process.

This does not mean allocation is approved.

16. Minimum Valid Audit Checklist

Before an audit record is finalized, reviewers should confirm:

[ ] The trace claim is clearly stated.
[ ] Origin candidate or candidates are identified.
[ ] The later work is identified.
[ ] Evidence items are listed.
[ ] Evidence strength is recorded.
[ ] Relation type is classified.
[ ] Confidence score is provided.
[ ] Uncertainty notes are included.
[ ] Review status is explicit.
[ ] Dispute status is explicit.
[ ] Allocation readiness is not confused with allocation approval.
[ ] Governance safety boundaries are preserved.
17. Anti-Overclaiming Rules

Reviewers should avoid the following errors:

similarity → copying
citation → ownership
confidence → truth
readiness → approval
dispute → guilt
absence of citation → misconduct
influence → allocation
trace → verdict

These shortcuts are structurally unsafe.

Origin Audit exists to prevent exactly this kind of premature collapse.

18. Methodological Summary

Origin Audit is a method for organizing trace claims before judgment.

It helps reviewers move from raw similarity or citation toward structured observation.

The correct methodological flow is:

claim
→ evidence
→ relation type
→ uncertainty
→ review status
→ dispute status
→ readiness signal
→ downstream escalation if needed

The incorrect flow is:

similarity
→ accusation
→ ownership
→ payment

Origin Audit rejects that shortcut.

Final Principle

Origin Audit should make trace culture slower, clearer, and safer.

Its highest value is not speed.
Its highest value is preventing premature judgment.

Trace carefully.
Preserve uncertainty.
Escalate responsibly.
