# 3-Bit Mod-7 Up/Down Counter

## The Task

Create an up/down counter using both **JK and D flip-flops**. The counter must have both count-up and count-down functionality controlled by a switch, and must skip state 4 (`100`) in both count directions.

This project implements a **3-bit synchronous mod-7 up/down counter** with state 4 (`100`) excluded.

## The Design

This is a synchronous counter. On each clock pulse, the circuit transitions to the next valid state while skipping `100`.
Three flip-flops are used to store the 3-bit state of the counter:

- A **JK flip-flop** for the LSB
- A **D flip-flop** for the middle bit
- A **JK flip-flop** for the MSB

**Switch = 1** → Count Up, **Switch = 0** → Count Down

Combinational logic generates the required flip-flop input signals for both the count-up and count-down sequences.

A **74LS157 quad 2-to-1 multiplexer** uses the direction-control switch to select between the up-count and down-count logic. The selected signals are then applied to the flip-flops, determining the next state of the counter.

## Components

- 2 × JK Flip-Flops (`74LS73`)
- 1 × D Flip-Flop (`74LS74`)
- 1 × Quad 2-to-1 Multiplexer (`74LS157`)
- AND, OR, and NOT gates
- Up/Down direction switch

## Concepts Demonstrated

### Custom counter design

- Synchronous sequential logic
- JK flip-flop excitation logic
- D flip-flop next-state logic
- Boolean logic
- Multiplexing
- State-transition design
