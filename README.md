# 2×1 Multiplexer using Verilog

## Overview

This project implements a **2×1 Multiplexer (MUX)** in Verilog HDL. A multiplexer selects one of two input signals based on the value of a select line and forwards it to the output.

## Truth Table

| Select (S) | Output (Y) |
|------------|------------|
| 0 | I0 |
| 1 | I1 |

## Circuit Logic

```
Y = S'·I0 + S·I1
```

## Inputs

- I0 : Input 0
- I1 : Input 1
- S : Select line

## Output

- Y : Selected output

## Project Structure

```
2x1-multiplexer-verilog/
├── src/
├── tb/
├── sim/
├── images/
└── README.md
```

## Simulation

Compile:

```bash
iverilog -o mux src/mux2x1.v tb/mux2x1_tb.v
```

Run:

```bash
vvp mux
```

Open waveform:

```bash
gtkwave mux2x1.vcd
```

## Expected Results

| S | I0 | I1 | Y |
|---|----|----|---|
|0|0|0|0|
|0|0|1|0|
|0|1|0|1|
|0|1|1|1|
|1|0|0|0|
|1|0|1|1|
|1|1|0|0|
|1|1|1|1|

## Applications

- Data routing
- Bus selection
- Digital communication
- Processor datapaths
- FPGA and ASIC design

## Author

Your Name

## License

MIT License