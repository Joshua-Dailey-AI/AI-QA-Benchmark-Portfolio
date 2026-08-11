# Portfolio Case Study 1: Municipal Building Permit Benchmark

## Executive Summary
This case study evaluates an AI Agent's capability to enforce complex municipal zoning and environmental policy overlays while ignoring emotional context and resolving non-standard unit conversions.

## Benchmark Specification
- Task ID: MUNI_PERMIT_001
- Target Pass Rate: <70% (Stress Test)
- Key Capabilities Tested: Multi-rule precedence, unit conversion (inches to feet), noise filtering.

## Test Results & Evaluation
- Baseline Model: Gemini 3 Flash
- Outcome: PASS (1/1)
- Key Observations: Model correctly executed 120 in -> 10 ft conversion, identified that Rule 4 (Historic Overlay) superseded Rule 2 (Expedited Size Allowance), and caught the setback violation despite emotional chatter.
- Next Steps: Adversarial iteration planned (injecting conflicting statements regarding structural permanence) to identify model failure boundary.
