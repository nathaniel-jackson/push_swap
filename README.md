# Push Swap

A limited instruction stack sorting algorithm.

## Problem Description

Given two stacks, stack A and stack B, and the simple instructions:

- `sX` - swap the top 2 elements of stack X.
- `rX` - rotate the bottom element of stack X to the top.
- `rrX` - rotate the top element of stack X to the bottom.
- `ss` - swap the top 2 elements on both stacks. Equivelent to `sa, sb`
- `rr` - rotate the bottom element to the top on both stacks. Equivelent to `ra, rb`
- `rrr` - rotate the top element to the bottom on both stacks. Equivelent to `rra, rrb`
- `pa` - push the top element of stack B to the top of stack A.
- `pb` - push the top element of stack A to the top of stack B.

Stack A starts with a set of unsorted numbers, all unique. Stack B starts empty.
Sort all elements of stack A in order from smallest to largest

The goal is to sort the stack in as few instructions as possible.

My results (as tested by test.sh) are as follows:

Stack size 50: average ~225
Stack size 100: average ~530
Stack size 500: average ~4500
Stack size 1000: average ~12000

## Build Instructions

Requires `make clang/gcc`

To build the executable, run:

```make```

You can then execute like:

```./push_swap <nums to sort>
e.g.
./push_swap 8 4 5 7 2
```

The output will look like:

```
ra
pb
ra
ra
pb
ra
rrb
pa
pa
```

These instructions, defined above, will sort the numbers in ascending order.

## Tester

Also provided is a test script: `test.sh`

Run as `./test.sh` this script will compile the project if no file `push_swap` exists, optionally
checks [norminette](https://github.com/42School/norminette), then runs a series
of tests based on the 42 project requirenments.

This script can also be run as `./test.sh <stack_size> [-r num_stacks]`

Running like this will allow you to quickly get an average of the number of
instructions the program uses for a given stack size.
