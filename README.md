# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# involving the unexpected behavior of mutable variables when passed to functions. The `swap` function attempts to swap the values of two mutable variables, but due to pass-by-reference semantics, it modifies the original variables directly.  This can lead to unexpected results if the programmer assumes pass-by-value behavior.

## How to Reproduce

1.  Clone this repository.
2.  Open `bug.fs` in an F# IDE (like Visual Studio or Ionide).
3.  Run the code.  Observe that the output is not what one might expect from a simple variable swap.  The variables x and y are modified in place
4.  Review the `bugSolution.fs` file for a corrected version.