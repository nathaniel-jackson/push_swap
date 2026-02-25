# Push Swap

A limited instruction stack sorting algorithm.

Given two stacks, stack A and stack B, and the simple instructions:

- `sX` - swap the top 2 elements of stack X.
- `rX` - rotate the bottom element of stack X to the top.
- `rrX` - rotate the top element of stack X to the bottom.
- `ss` - swap the top 2 elements on both stacks. Equivelent to `sa, sb`
- `rr` - rotate the bottom element to the top on both stacks. Equivelent to `ra, rb`
- `rrr` - rotate the top element to the bottom on both stacks. Equivelent to `rra, rrb`
- `pa` - push the top element of stack B to the top of stack A.
- `pa` - push the top element of stack A to the top of stack B.

Stack A starts with a set of unsorted numbers, all unique. Stack B starts empty.
Sort all elements of stack A in order from smallest to largest

The goal is to sort the stack in as few instructions as possible.

My results (as tested by test.sh) are as follows:

Stack size 50: average ~225
Stack size 100: average ~530
Stack size 500: average ~4500
Stack size 1000: average ~12000
