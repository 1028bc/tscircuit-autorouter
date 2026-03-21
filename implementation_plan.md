# ANTIGRAVITY SDLC: IMPLEMENTATION PLAN

## 0. CURRENT TARGET
- **Repository:** TSCIRCUIT-AUTOROUTER
- **Objective:** Resolve Pull Request #2040
- **Status:** [ ] Pending Analysis | [ ] In Progress | [ ] Verifying | [ ] Clean & Ready

## 1. ARCHITECTURAL MANDATES (NON-NEGOTIABLE)
- **Decoupled Logic:** The routing engine/calculations MUST be strictly isolated from the UI/rendering logic. 
- **Universal Math Protocol:** Any capacity, grid limit, or bounding box calculation must follow: `[Variable] > [Threshold] = [Baseline] * [Multiplier]`.
- **Buffer Rule:** Apply a 10% safety buffer to all geometric constraints and array limits to prevent overflow/clipping.

## 2. SDLC EXECUTION CHECKPOINTS
### Phase 1: Plan & Isolate
- [ ] Read PR #2040 issue description and current diff.
- [ ] Identify the exact module failing the logic/rendering split.
- [ ] Document the intended fix here before modifying code.

### Phase 2: Standardize & Execute
- [ ] Apply the fix strictly adhering to the Universal Math Protocol.
- [ ] Ensure no UI components contain raw routing calculations.

### Phase 3: Verify
- [ ] Run local autorouter unit tests.
- [ ] Confirm PR 2040 specific edge-cases pass.

### Phase 4: Clean
- [ ] Strip all `console.log`, temporary visualizers, and debug artifacts.
- [ ] Finalize code formatting.