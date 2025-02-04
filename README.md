# Lua Pairs Iterator Unexpected Order Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when used with nested tables that are modified during iteration.  The `bug.lua` file shows the original code that exhibits unexpected behavior, whereas `bugSolution.lua` shows the corrected code with improved handling of nested tables. 

The bug arises from the fact that `pairs` doesn't guarantee a specific order of iteration. When nesting tables and altering them within loops using `pairs`, the iterator might get confused, skipping elements or leading to unpredictable results.  The solution involves using a different iteration strategy to avoid this issue and ensure more reliable results when iterating over nested tables and modifying their content during the loop.