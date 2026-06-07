# Pipelined-MIPS32-Processor-using-Verilog
5-stage pipelined MIPS32 processor implemented in Verilog HDL.  Simulated using Xilinx Vivado. Based on NPTEL Hardware Modeling course.


## Overview
A 5-stage pipelined MIPS32 processor implemented in Verilog HDL.
Simulated and synthesized using Xilinx Vivado.
Developed as a learning project based on NPTEL Hardware Modeling Using Verilog course
by IIT Kharagpur.

## Pipeline Stages
1. **IF** - Instruction Fetch
2. **ID** - Instruction Decode & Register Read
3. **EX** - Execute (ALU Operations)
4. **MEM** - Memory Access
5. **WB** - Write Back

## Supported Instructions

| Instruction | Type | Opcode |
|-------------|------|--------|
| ADD | RR_ALU | 000000 |
| SUB | RR_ALU | 000001 |
| AND | RR_ALU | 000010 |
| OR  | RR_ALU | 000011 |
| SLT | RR_ALU | 000100 |
| MUL | RR_ALU | 000101 |
| ADDI | RM_ALU | 001010 |
| SUBI | RM_ALU | 001011 |
| SLTI | RM_ALU | 001100 |
| LW  | LOAD  | 001000 |
| SW  | STORE | 001001 |
| BEQZ | BRANCH | 001110 |
| BNEQZ | BRANCH | 001101 |
| HLT | HALT | 111111 |

## Test Program
The testbench runs the following program:
# Pipelined MIPS32 Processor in Verilog

## Overview
A 5-stage pipelined MIPS32 processor implemented in Verilog HDL.
Simulated and synthesized using Xilinx Vivado.
Developed as a learning project based on NPTEL Hardware Modeling Using Verilog course
by IIT Kharagpur.

## Pipeline Stages
1. **IF** - Instruction Fetch
2. **ID** - Instruction Decode & Register Read
3. **EX** - Execute (ALU Operations)
4. **MEM** - Memory Access
5. **WB** - Write Back

## Supported Instructions

| Instruction | Type | Opcode |
|-------------|------|--------|
| ADD | RR_ALU | 000000 |
| SUB | RR_ALU | 000001 |
| AND | RR_ALU | 000010 |
| OR  | RR_ALU | 000011 |
| SLT | RR_ALU | 000100 |
| MUL | RR_ALU | 000101 |
| ADDI | RM_ALU | 001010 |
| SUBI | RM_ALU | 001011 |
| SLTI | RM_ALU | 001100 |
| LW  | LOAD  | 001000 |
| SW  | STORE | 001001 |
| BEQZ | BRANCH | 001110 |
| BNEQZ | BRANCH | 001101 |
| HLT | HALT | 111111 |

## Test Program
The testbench runs the following program:
# Pipelined MIPS32 Processor in Verilog

## Overview
A 5-stage pipelined MIPS32 processor implemented in Verilog HDL.
Simulated and synthesized using Xilinx Vivado.
Developed as a learning project based on NPTEL Hardware Modeling Using Verilog course
by IIT Kharagpur.

## Pipeline Stages
1. **IF** - Instruction Fetch
2. **ID** - Instruction Decode & Register Read
3. **EX** - Execute (ALU Operations)
4. **MEM** - Memory Access
5. **WB** - Write Back

## Supported Instructions

| Instruction | Type | Opcode |
|-------------|------|--------|
| ADD | RR_ALU | 000000 |
| SUB | RR_ALU | 000001 |
| AND | RR_ALU | 000010 |
| OR  | RR_ALU | 000011 |
| SLT | RR_ALU | 000100 |
| MUL | RR_ALU | 000101 |
| ADDI | RM_ALU | 001010 |
| SUBI | RM_ALU | 001011 |
| SLTI | RM_ALU | 001100 |
| LW  | LOAD  | 001000 |
| SW  | STORE | 001001 |
| BEQZ | BRANCH | 001110 |
| BNEQZ | BRANCH | 001101 |
| HLT | HALT | 111111 |

## Test Program
The testbench runs the following program:ADDI R1, R0, 10     # R1 = 10
ADDI R2, R0, 20     # R2 = 20
ADDI R3, R0, 25     # R3 = 25
OR   R7, R7, R7     # NOP (pipeline bubble)
OR   R7, R7, R7     # NOP (pipeline bubble)
ADD  R4, R1, R2     # R4 = R1 + R2 = 30
OR   R7, R7, R7     # NOP (pipeline bubble)
ADD  R5, R4, R3     # R5 = R4 + R3 = 55
HLT                 # Stop


## Expected Output
R0 =  0
R1 = 10
R2 = 20
R3 = 25
R4 = 30
R5 = 55

## Files
| File | Description |
|------|-------------|
| `pipe_MIPS32.v` | Main processor module |
| `add_mips32.v` | Testbench |

## Tools Used
- Xilinx Vivado 2023
- Verilog HDL

## How to Run
1. Open Vivado
2. Create a new project
3. Add `pipe_MIPS32.v` as design source
4. Add `add_mips32.v` as simulation source
5. Run Behavioral Simulation
6. Add internal signals from SST panel to wave window
7. Click Restart then Run All

## What I Learned
- 5-stage pipeline architecture
- Verilog HDL coding and debugging
- Handling pipeline hazards using NOP instructions
- Branch handling in pipelined processors
- Simulation and synthesis using Xilinx Vivado

## Bugs Fixed During Development
- Fixed case sensitivity issue (`ID_EX_TYPE` → `ID_EX_type`)
- Fixed typo (`MEM_WR_type` → `MEM_WB_type`)
- Fixed `endelse` → `end else`
- Moved memory initialization inside processor module
  for Vivado synthesis compatibility

## Reference
This project was developed as part of learning from:
- **Course**: Hardware Modeling Using Verilog
- **Platform**: NPTEL Online Certification Courses  
- **Institute**: IIT Kharagpur
- **Instructor**: Prof. Indranil Sen Gupta, IIT Kharagpur
- **Course Link**: https://nptel.ac.in

> Note: This is a learning/educational project.
> Original course material belongs to IIT Kharagpur and NPTEL.

## Author
Tanuja Wagare
B.Tech (Electronics & Communication / VLSI)

