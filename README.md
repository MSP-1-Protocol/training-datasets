# training-datasets

Versioned, checksum-verified training datasets for MSP-1 protocol behavior and validation.

## Overview

This repository contains baseline datasets intended to define expected behavior, validation patterns, compatibility handling, and edge cases for the MSP-1 protocol.

The datasets are:

- **Model-agnostic** — not tuned to any specific LLM
- **Versioned** — changes are introduced only through new dataset versions
- **Checksum-verified** — integrity can be independently validated
- **Deterministic** — identical inputs produce identical artifacts

This repository is designed to be consumed by humans, tools, and automated systems that require a stable reference for MSP-1 interpretation.

## Available Dataset Versions

| Dataset version | Protocol target | Status | Notes |
|---|---:|---|---|
| `datasets/baseline/v1.0.2/` | MSP-1 v1.0.2 | Current | Context-surface patch: dedicated JSON-LD contexts and legacy v1.0.1 compatibility handling. |
| `datasets/baseline/v1.0.1/` | MSP-1 v1.0.1 | Archived / immutable | Harmonized patch update for v1.0.1 behavior, compatibility handling, and compliance deprecation. |
| `datasets/baseline/v1.0/` | MSP-1 v1.0.x | Legacy / immutable | Original baseline retained for compatibility and historical comparison. |

## Repository Structure

```text
training-datasets/
├─ README.md
├─ QUICK_START.md
├─ LICENSE
├─ NOTICE
├─ datasets/
│  └─ baseline/
│     ├─ v1.0/
│     │  ├─ msp1_protocol_behavior_baseline.jsonl
│     │  ├─ msp1_protocol_validation_subset.jsonl
│     │  ├─ dataset_metadata.json
│     │  └─ CHECKSUMS.sha256
│     ├─ v1.0.1/
│     │  ├─ msp1_protocol_behavior_baseline.jsonl
│     │  ├─ msp1_protocol_validation_subset.jsonl
│     │  ├─ dataset_metadata.json
│     │  ├─ CHANGELOG.md
│     │  └─ CHECKSUMS.sha256
│     └─ v1.0.2/
│        ├─ msp1_protocol_behavior_baseline.jsonl
│        ├─ msp1_protocol_validation_subset.jsonl
│        ├─ dataset_metadata.json
│        ├─ CHANGELOG.md
│        └─ CHECKSUMS.sha256
└─ tools/
   ├─ validate_jsonl.py
   └─ verify_checksums.py
```

## Dataset Versioning

- Dataset versions are immutable once published.
- Any change requires a new version directory, such as `v1.0.1`, `v1.1`, or `v2.0`.
- Existing version contents must not be modified after publication.
- Integrity is verified via the accompanying `CHECKSUMS.sha256` file.

## Integrity Verification

Each dataset version includes a `CHECKSUMS.sha256` file.

Consumers are expected to verify checksums before use to ensure dataset integrity and provenance.

```bash
python tools/validate_jsonl.py datasets/baseline/v1.0.2/*.jsonl
python tools/verify_checksums.py datasets/baseline/v1.0.2/CHECKSUMS.sha256
```

## License

All datasets and tooling in this repository are released under the Apache License, Version 2.0, unless otherwise noted.
