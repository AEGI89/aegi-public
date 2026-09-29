# AEGI PAR Demo → AEGI Public Migration Audit v0.1

Status: **SELECTIVE MIGRATION CANDIDATE — WORDING NORMALIZATION REQUIRED**

## Source reviewed

Legacy public repository:

`hoangtm3979/aegi-par-demo`

Reviewed source artifacts include:

- `README.md`
- `AUTHORITY_FREEZE_20260925.md`
- `UI_RELEASE.json`
- `PRODUCTION_ACCEPTANCE_UI_1.1.md`
- repository-level checksum/release/acceptance structure observed at root

## Positive controls observed

The legacy repository already contains useful release discipline:

- frozen backend identity and SHA-256;
- explicit UI/backend separation;
- external smoke/runtime acceptance evidence;
- benchmark limitations;
- explicit statement that UI acceptance is not an effectiveness benchmark;
- explicit statement that benchmark results do not establish real-world fraud-loss reduction;
- authority freeze that blocks backend/policy/dataset changes during the UI-only pass;
- checksum and acceptance artifacts at repository root.

These are useful public-release primitives and should be preserved when materially relevant.

## Main disclosure risk

The source uses the label `PRODUCTION_ACCEPTED` for the deployed public demo UI/runtime.

The detailed acceptance document limits that statement to deployment/runtime/UI behavior and explicitly says it is not an effectiveness benchmark or evidence of real-world fraud reduction. However, when copied into the broader AEGI public namespace, the short label `PRODUCTION_ACCEPTED` could be misread as:

- production-banking readiness;
- customer production approval;
- production reliance approval;
- regulator endorsement;
- validated fraud effectiveness.

That interpretation is not supported by the reviewed source.

## Migration decision

Do **not** transfer the legacy repository wholesale into `AEGI89/aegi-public`.

Use selective promotion under the AEGI Public Release Checklist.

Recommended classification:

| Artifact | Decision | Condition |
|---|---|---|
| README / public scope text | REWRITE / MIGRATE SELECTIVELY | Align terminology with current AEGI public claim boundary |
| Authority freeze | KEEP AS HISTORICAL EVIDENCE | Preserve exact engine/hash/date and historical context |
| UI acceptance evidence | KEEP AS HISTORICAL DEMO-RUNTIME EVIDENCE | Relabel context as `PUBLIC_DEMO_RUNTIME_ACCEPTED` or equivalent when summarized |
| `UI_RELEASE.json` | MIGRATE ONLY WITH WRAPPER / NORMALIZED PUBLIC RECORD | Do not expose bare `PRODUCTION_ACCEPTED` without deployment-only explanation |
| SHA256SUMS / checksum evidence | KEEP IF BYTES ARE ALSO PROMOTED | Recompute/verify against promoted artifact bytes |
| Backend ZIP | HOLD | Binary/source/IP review required before any public promotion |
| Dockerfile | HOLD / TECHNICAL REVIEW | Public value and dependency/IP exposure must be reviewed |
| acceptance/submission overlays | REVIEW INDIVIDUALLY | Promote only artifacts still useful and boundary-compliant |

## Required public wording

When the legacy UI/runtime acceptance is referenced publicly, the meaning must be explicit, for example:

> Public demo runtime acceptance confirms the declared UI/API deployment and external smoke checks for that frozen demo release. It does not establish production-banking readiness, fraud-loss reduction, independent validation, regulatory approval, or customer production reliance.

## Evidence-level classification

Default public evidence level for these artifacts is:

`SYNTHETIC_DEMO` / `FROZEN_EVALUATION`

as applicable to the individual artifact. It must not be promoted to `PRODUCTION_EVIDENCE` solely because the demo was deployed to a production hosting environment.

## Next action

Create a clean public-demo release package from approved source artifacts rather than migrating repository history wholesale. The package should receive a new AEGI public release record, checksum, limitations statement and canonical-source reference.
