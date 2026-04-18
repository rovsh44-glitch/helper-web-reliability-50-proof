# HELPER Web Reliability 50 Proof Bundle

Bundle ID: `web_reliability_50_v1`
Generated: 2026-04-18T13:18:09.5824345Z

## Scope

- frozen corpus: `web_reliability_mini_50_v2.jsonl`
- frozen target lock manifest included
- source data exported from one final frozen full-50 live rerun
- private-core runtime logs, raw request envelopes, internal trace payloads, and absolute local paths are excluded

## Run Summary

- total cases: 50
- ok cases: 50
- clarification cases: 5
- cases with sources: 45
- average citation coverage: 0.589

## Boundary

- included: prompts, sanitized final responses, source URLs/titles, grounding metrics, frozen corpus, frozen target lock, manifest, checksums
- excluded: `requestEnvelope`, `rawResponse`, `conversationId`, `turnId`, runtime logs, internal search traces, absolute local paths

## Residual Interpretation

- `grounded` means the public-safe final answer retained passage-backed support after sanitization.
- `grounded_with_limits` means the system kept bounded uncertainty in the final answer.
- `clarification_required` means the prompt was intentionally not forced into noisy search.

## Reproduction Inputs

- corpus: `corpus/web_reliability_mini_50_v2.jsonl`
- target lock: `corpus/web_reliability_mini_50_v2.targets.lock.json`
- sanitized results: `results/web_reliability_50_results.sanitized.jsonl`
- checksums: `CHECKSUMS.sha256`
