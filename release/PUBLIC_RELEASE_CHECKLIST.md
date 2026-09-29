# AEGI Public Release Checklist v0.1

Status: INTERNAL CONTROL FOR PUBLIC PROMOTION

No artifact is promoted into `aegi-public` or `aegi.global` unless this checklist is completed against a traceable canonical source.

## 1. Identity and custody

- [ ] Canonical source is recorded.
- [ ] Artifact ID and version are explicit.
- [ ] Source owner is known.
- [ ] Release date is recorded.
- [ ] Supersedes / superseded-by relationship is recorded where applicable.

## 2. Evidence level

One and only one level is selected:

- [ ] Concept / architecture only
- [ ] Synthetic demo
- [ ] Frozen benchmark / evaluation evidence
- [ ] Controlled customer evaluation
- [ ] Controlled pilot
- [ ] Production evidence

The artifact must not imply a higher evidence level than the selected level.

## 3. Claim boundary

- [ ] No production-readiness claim unless separately evidenced and approved.
- [ ] No regulator approval / endorsement claim.
- [ ] No fraud-loss-reduction claim unless directly measured in the stated scope.
- [ ] No predictive-superiority claim unless benchmark evidence supports it.
- [ ] No autonomous-blocking claim.
- [ ] No automatic production-promotion claim.
- [ ] Core claims are limited to declared evidence identity/scope/version/integrity/conformance boundaries.

## 4. Confidentiality / IP

- [ ] No customer data or customer-identifying information.
- [ ] No private keys, credentials, secrets or signing material.
- [ ] No restricted CTS / golden vectors.
- [ ] No exploit-sensitive failure details.
- [ ] No patent-sensitive implementation detail without explicit disclosure approval.
- [ ] No partner/customer-local schemas unless approved for publication.

## 5. Integrity

- [ ] Public artifact checksum is generated where applicable.
- [ ] Signature is generated where the active release policy requires it.
- [ ] Published file matches approved source bytes or approved export.
- [ ] Limitations and scope statements remain attached to the artifact.

## 6. Withdrawal / supersession

- [ ] Withdrawal owner is known.
- [ ] Superseded artifacts remain traceable or are explicitly revoked/removed under policy.
- [ ] Website/reference links are updated if the public artifact changes state.

## Decision

- Disclosure decision: `APPROVE_PUBLIC | HOLD | REJECT`
- Approver:
- Canonical source:
- Artifact/version:
- Evidence level:
- Notes:

This checklist is a disclosure control. It is not itself evidence of production readiness, regulatory approval, or AEGI certification.
