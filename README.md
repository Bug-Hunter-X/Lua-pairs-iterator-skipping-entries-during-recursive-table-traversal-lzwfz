# Lua pairs iterator bug
This repository demonstrates a potential issue with Lua's `pairs` iterator when used recursively on tables that are modified during iteration.  The bug is that entries in a nested table might be skipped under certain conditions, leading to incomplete processing of the data.

The `bug.lua` file contains code demonstrating the problem. The `bugSolution.lua` file provides a corrected version that addresses the issue, ensuring complete traversal and processing of all table entries, even during recursive calls.

## How to reproduce
1. Clone this repository.
2. Run `bug.lua`.  Observe that not all values are processed.
3. Run `bugSolution.lua`. Observe that all values are processed.