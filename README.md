# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL code: an integer counter that doesn't handle overflow correctly.

The `counter_bug.vhdl` file contains a counter that increments on each rising clock edge. However, it doesn't prevent overflow when it reaches its maximum value (15). This can lead to unpredictable behavior.

The `counter_solution.vhdl` file shows a corrected version of the counter that addresses the overflow issue.

## Bug Description
The original counter increments until it reaches 15.  Then, an increment operation would lead to undefined behavior.  This is a classic off-by-one error.

## Solution
The solution uses a modulo operation to wrap the counter back to 0 after it reaches 15. This ensures that the counter behaves correctly even when it exceeds its defined range.  It also adds explicit handling of a reset signal.

## How to use
You can simulate these VHDL files using a VHDL simulator such as ModelSim or GHDL.