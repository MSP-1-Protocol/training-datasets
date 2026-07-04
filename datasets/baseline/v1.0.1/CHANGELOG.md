# MSP-1 Training Datasets — Baseline v1.0.1 Changelog

Created: 2026-07-04
Protocol target: MSP-1 v1.0.1

## Summary

This dataset version harmonizes the baseline training data with MSP-1 v1.0.1 while preserving the published v1.0 directory unchanged.

## Main changes from v1.0

- Updated current-generation examples from `protocol.version: "1.0.0"` to `protocol.version: "1.0.1"`.
- Replaced `page.title.required` assumptions with v1.0.1 page identity behavior: `page.id` and `page.url` are the minimal required page fields.
- Reframed `page.title` as a compatibility field and `page.name` as the preferred current naming field.
- Added explicit deprecated-compatibility handling for `compliance`.
- Updated trust examples so `trust.level` uses `low`, `medium`, or `high`; verification process status belongs in `verified` / `verificationLevel` when declared.
- Softened unknown-field handling to advisory guidance for the baseline dataset unless a stricter implementation profile elects to reject.
- Retained strict discovery endpoint guidance for `/.well-known/msp.json`.

## Compatibility note

The v1.0 dataset remains available for legacy behavior comparison. New MSP-1 v1.0.1 tools should consume this directory when testing current protocol behavior.
