# Hydrozoan: Artifact

Artifact of the paper *Hydrozoan: Latency-Adaptive DAG Consensus under Mixed Byzantine
and Crash Faults*. Hydrozoan is an uncertified DAG consensus protocol that commits a
leader in two message delays when few validators are faulty and in three otherwise,
reading both commit paths off the same DAG.

## Contents

| File | What it holds |
|---|---|
| [`lean.pdf`](lean.pdf) | **Lean formalization.** How the safety and liveness proofs of Hydrozoan and Optimal-Hydrozoan are machine-checked in Lean 4: the module layout, the trusted base a reader audits, the modeling choices, and a table mapping every lemma and theorem of the paper to its Lean statement. |
| [`testbed.pdf`](testbed.pdf) | **Testbed details.** The AWS deployment (instance type, regions, validator placement, measured inter-region latencies), the load and crash schedules, run lengths, and how latencies are measured and aggregated for the paper's evaluation. |
| [`simulation.pdf`](simulation.pdf) | **Simulation results.** The discrete-event simulator, which runs the unmodified consensus code over simulated links, its calibration against the testbed, and the experiments the testbed cannot run: equivocating leaders, crash sweeps without a remote tail, and the full resilience plane. |

Each note is self-contained. Section, lemma, figure and table numbers without a letter
prefix (L, T, S) refer to the paper.

## Related repositories

- **Lean 4 formalization:** <https://anonymous.4open.science/r/lean-dag>
- **Implementation (Rust):** <https://anonymous.4open.science/r/uncertified-dag-fabric>
