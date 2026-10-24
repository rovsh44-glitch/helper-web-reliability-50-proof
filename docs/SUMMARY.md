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

## Deeper Slices (2026-10-24 addendum)

An independent re-read of the raw sanitized results surfaced slices the original summary did not state.
Nothing below changes the data; it makes the bundle self-describing. All numbers are recomputable from
`results/web_reliability_50_results.sanitized.jsonl`.

- `unverified` (missing from the status list above): 11/50 cases carry `groundingStatus=unverified` -
  the pipeline completed but claim-level verification did not confirm passage support.
- Expected-vs-actual grounding tier: 32/50 cases match their corpus `expectedGrounding`.
- Citation coverage is bimodal, not centered: 16 cases at 0.0 and 24 cases at 1.0 produce the 0.589
  average. The mean alone overstates the typical mid-range case.
- Per-class expected-tier match: C01 5/5, C02 4/5, C03 2/5, C04 1/5, C05 4/5, C06 4/5, C07 3/5,
  C08 1/5, C09 3/5, C10 5/5. In the sparse-evidence class C08, 4/5 cases report `grounded` where the
  corpus expected a bounded answer - the degradation path under-fired on this class.
- Verified claims: 102/131 across the run.
- This bundle is a historical April 2026 artifact; the current core is months of releases ahead of it.
