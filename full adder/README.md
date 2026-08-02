# 1-Bit Full Adder using Verilog

## Overview

This project implements a 1-bit Full Adder in Verilog HDL.

A Full Adder adds three binary inputs:
- A
- B
- Cin (Carry Input)

and produces:
- Sum
- Cout (Carry Output)

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
|0|0|0|0|0|
|0|0|1|1|0|
|0|1|0|1|0|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|1|
|1|1|0|0|1|
|1|1|1|1|1|

## Boolean Equations

Sum = A ⊕ B ⊕ Cin

Cout = (A & B) | (B & Cin) | (A & Cin)

## Files

- full_adder.v → Verilog design
- tb_full_adder.v → Testbench
- simulation_output.txt → Simulation results

## Simulation Tool

- Icarus Verilog
- GTKWave

## Run

Compile

```bash
iverilog -o fulladder full_adder.v tb_full_adder.v
```

Run

```bash
vvp fulladder
```

Generate waveform

```bash
gtkwave fulladder.vcd
```

## Author

Your Name