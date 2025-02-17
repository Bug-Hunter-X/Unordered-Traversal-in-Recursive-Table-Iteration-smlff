# Lua Recursive Table Traversal Issue

This repository demonstrates a potential issue with recursive table traversal in Lua when using the `pairs` iterator.  The `pairs` iterator does not guarantee any specific order of iteration, which can lead to unexpected results if the code relies on a consistent order.

The `bug.lua` file contains code that recursively traverses a table.  The order of processing might not be consistent across different Lua versions or implementations, resulting in unpredictable behavior.

The `bugSolution.lua` file offers a solution that uses a sorted iteration to ensure a deterministic traversal order.