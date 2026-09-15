| Date | Module/Task | What Broke | What I Assumed | Root Cause / Fix |
| :--- | :--- | :--- | :--- | :--- |


1)
| 2026-09-15 | W1 - MatMul | `TypeError` on `np.zeros` | `np.zeros` takes dimensions as separate arguments | Function expects a single tuple for shape: `np.zeros((m, b))` |
np.zeros(m, b) → TypeError. Thought: forgot NumPy shape functions take a single tuple, not separate args. Fix: np.zeros((m, b)).