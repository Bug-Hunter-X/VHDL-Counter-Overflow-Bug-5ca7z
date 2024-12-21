# VHDL Counter Overflow Bug

This repository demonstrates a potential overflow bug in a simple VHDL counter. The counter is designed to count from 0 to 15, but if not handled properly, it might exhibit unexpected behavior once it reaches its limit.

## Bug Description

The provided VHDL code implements a counter that increments on every rising edge of a clock signal. However, the use of the integer type, without proper range checking or saturation, introduces a potential overflow risk. If the counter reaches its maximum value (15), further incrementing could lead to unintended behavior, like wrapping around to a negative number or causing simulation errors. 

## Solution

A robust solution involves either using an unsigned type or explicitly handling the overflow case within the counter logic. The updated solution incorporates this explicit check to avoid potential issues.