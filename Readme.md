ChipMark '77
============

A simple Chip8 benchmarking utility.

## Overview
A simple Chip8 benchmarking utility. Counts the number of 50-instruction
benchmark passes can be completed in 30 frames. Using the assumption that
60 frames is equal to one second of realtime, kOPS (1000s of Operations
Per Second) is calculated and displayed.

For use with the [Octo Chip8 compiler](https://johnearnest.github.io/Octo/).

## Details
Operates by counting how many loops of a benchmark function can be run in 30 frames.
The benchmark function plus loop overhead is designed to be exactly 50 instructions.

Accuracy suffers at slow speeds. For example, at 7 cycles/frame (420 cycles/sec), the
loop can only run 4 times before the delay timer elapses during the 5th loop. The counter
is large enough to accommodate speeds of at least 100 million operations per second.
