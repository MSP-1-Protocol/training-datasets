# Quick Start

## Validate JSONL files

```bash
python tools/validate_jsonl.py datasets/baseline/v1.0.2/*.jsonl
```

## Verify checksums

```bash
python tools/verify_checksums.py datasets/baseline/v1.0.2/CHECKSUMS.sha256
```

## Current baseline

Use `datasets/baseline/v1.0.2/` for MSP-1 v1.0.2 protocol behavior and validation expectations.

The `datasets/baseline/v1.0/` and `datasets/baseline/v1.0.1/` directories is retained unchanged as the original baseline and should be treated as immutable once published.
