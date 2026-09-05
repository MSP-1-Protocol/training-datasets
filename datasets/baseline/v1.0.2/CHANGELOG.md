# MSP-1 Training Datasets — Baseline v1.0.2 Changelog

Created: 2026-09-05
Protocol target: MSP-1 v1.0.2

## Summary

This dataset version aligns the established baseline with MSP-1 v1.0.2 while preserving the v1.0.1 dataset structure and record counts.

## Main changes from v1.0.1

- Updated current-generation examples to `protocol.version: "1.0.2"`.
- Replaced schema-as-context URLs in new declarations with the dedicated page and site `/context/` resources.
- Added focused behavior for context/schema separation, page/site context matching, JSON-LD 1.1 processing-version distinction, and legacy v1.0.1 migration.
- Retained `page.id` and `page.url` as the minimal required page identity fields; clean v1.0.2 output does not emit `page.title`, and `page.name` remains optional.
- Continued deprecated-compatibility handling for `compliance`: advisory review, graceful parsing, and no new emission.
- Preserved MSP-1's established vocabulary, declaration structure, declarative posture, and non-binding semantics.

## Compatibility note

The v1.0.1 dataset remains available unchanged for historical comparison. Its schema-as-context examples represent the legacy context architecture. New and repaired declarations should use the matching v1.0.2 `/context/` resource.
