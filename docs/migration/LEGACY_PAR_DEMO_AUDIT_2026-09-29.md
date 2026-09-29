# Legacy PAR Demo Migration Audit — 2026-09-29

Status: **REVIEWABLE / NOT YET APPROVED FOR MIGRATION**

## Source repository

`hoangtm3979/aegi-par-demo`

Observed repository state at audit time includes:

- `README.md`;
- `AUTHORITY_FREEZE_20260925.md`;
- `Dockerfile`;
- `PRODUCTION_ACCEPTANCE_UI_1.1.md`;
- `SHA256SUMS.json`;
- `UI_RELEASE.json`;
- `acceptance/`;
- `submission_overlay/`;
- backend/application ZIP artifacts.

The repository is substantially more reviewable than the legacy Shared-Risk-Context ZIP-only repository because it exposes authority, acceptance and release-control material directly in the source tree.

## Source-declared boundaries that must be preserved

The source README states that local UI testing was completed but its described state is not itself a new benchmark or proof of real-world anti-fraud effectiveness. It also explicitly states that images are sent to the server, OCR is not claimed, and no bank/telco/police integration is claimed.

The authority freeze binds the engine to `PAR_CORE v0.4.2-rc4`, records frozen backend and benchmark identities, states that UI-only work must not change backend policy/scoring/evidence semantics, and explicitly disclaims incremental action-level superiority and real-world effectiveness.

## Migration decision

Do **not** wholesale-transfer the repository into `aegi-public`.

`aegi-public` is an approved public evidence/examples surface, not a historical deployment mirror. Migration must therefore be selective and pass the public-release custody gate already defined in this repository.

## Candidate material for selective promotion

Potentially promotable after review:

- release/authority freeze record;
- public-safe acceptance summary;
- public-safe UI release manifest;
- hash manifest/checksum evidence;
- selected screenshots or static demonstration material where rights and disclosure boundaries are clear;
- a reduced public README that preserves evidence limitations.

## Material requiring additional review or likely exclusion

- backend ZIP/application bundle;
- deployment-specific secrets/configuration if any;
- internal acceptance details that expose unnecessary implementation information;
- any content whose evidence status cannot be mapped to the current AEGI public-release schema;
- any wording that could be read as production effectiveness, independent expert validation, or bank integration evidence.

## Required promotion gate

Before any artifact enters `aegi-public`:

1. identify canonical source and version;
2. verify integrity/hash where applicable;
3. classify evidence level;
4. map every public claim to supporting evidence and limitations;
5. confirm no restricted IP, secrets or customer data;
6. bind owner, approval date and supersession/withdrawal path;
7. create an AEGI public release record;
8. promote by pull request rather than repository transfer.

## Current classification

- Historical/public-demo value: **HIGH**
- Reviewability: **GOOD**
- Wholesale migration allowed: **NO**
- Selective promotion possible: **YES, AFTER GATE**
- Current public canonical status in `aegi-public`: **NONE YET**

This audit does not re-certify the historical runtime or benchmark; it only determines migration handling under the current AEGI89 source-of-truth model.
