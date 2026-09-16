1)
| Date | Module/Task | What Broke | What I Assumed | Root Cause / Fix |
| :--- | :--- | :--- | :--- | :--- |
| 2026-09-15 | W1 - MatMul | `TypeError` on `np.zeros` | `np.zeros` takes dimensions as separate arguments | Function expects a single tuple for shape: `np.zeros((m, b))` |
np.zeros(m, b) → TypeError. Thought: forgot NumPy shape functions take a single tuple, not separate args. Fix: np.zeros((m, b)).


2)
| Date | Module/Task | What Broke | What I Assumed | Root Cause / Fix |
| :--- | :--- | :--- | :--- | :--- |
| 2026-09-16 | W1 - Eigen | `AttributeError` on `np.linalg.allclose` | Assumed `allclose` was a linear algebra function | It is a top-level general array utility. Changed to `np.allclose()` |