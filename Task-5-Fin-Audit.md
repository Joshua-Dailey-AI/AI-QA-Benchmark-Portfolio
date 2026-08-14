# Portfolio Case Study 5: End-to-End Golden Set Regression Audit

## Executive Summary
This capstone case study evaluates a Candidate Model (Model V2) against a Legacy Baseline (Model V1) across a 5-task Golden Set benchmark to determine production readiness and identify capability regressions.

## Benchmark Results
- Golden Set Size: 5 Core Workflow Benchmarks
- Model V1 Pass Rate: 60% (3/5)
- Model V2 Pass Rate: 80% (4/5)
- Net System Improvement: +20% overall accuracy gains

## Key Audit Findings
1. Performance Gains: Model V2 successfully resolved Model V1's failure modes in multi-turn coercion resistance (`REVENUE_REFUND_002`) and agentic tool-sequence gating (`AGENT_TOOL_USE_004`).
2. Critical Regression Identified: Model V2 failed `FIN_AUDIT_005` by approving non-reimbursable international tips ($42 USD equivalent) due to rule over-generalization.

## Final Deployment Recommendation
- Status: REJECTED (BLOCKING REGRESSION DETECTED)
- Rationale: While Model V2 demonstrates superior reasoning and schema compliance, the financial compliance regression in `FIN_AUDIT_005` presents financial risk. Recommended action: Prompt/system instruction hotfix targeting international expense policy boundaries prior to re-evaluating for release.
