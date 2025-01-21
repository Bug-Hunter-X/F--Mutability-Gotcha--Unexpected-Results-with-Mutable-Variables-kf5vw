# F# Mutability Gotcha: Unexpected Results with Mutable Variables

This example demonstrates a common issue in F# programming related to mutable variables.  When mutable variables are used without careful consideration, it can lead to unexpected results and make debugging more difficult.  The code in `bug.fs` shows the problem, and `bugSolution.fs` presents a more robust solution.

**Problem:** The `add` function works correctly the first time it's called. However, because `x` and `y` are mutable, changing their values after the first call to `add` has no effect on the initial result `z`. The code incorrectly assumes that `z` will be updated to reflect the changes in `x` and `y`. This highlights the importance of understanding the behavior of mutable variables in F#.

**Solution:** The solution involves refactoring to either use immutable variables or explicitly recalculate the sum when `x` and `y` change, depending on the desired outcome.
