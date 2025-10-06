# SAP-1 CPU (Simple-As-Possible) — Logisim Evolution
![CPU Badge](https://img.shields.io/badge/CPU-SAP--1-brightgreen)
![Logisim Badge](https://img.shields.io/badge/Tool-Logisim--Evolution-blue)
![CUET](https://img.shields.io/badge/CUET-ETE-red)

---

## 📘 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Control Unit](#controlunit)
- [Instruction Set](#instructionset)
- [How to Run](#howtorun)

---

<a id="overview"></a>
## 🧩 Overview
This project is an implementation of the **SAP-1 (Simple As Possible) CPU** using **Logisim Evolution**.  
It demonstrates the core principles of computer architecture, including fetching, decoding, and executing 8-bit instructions through modular hardware blocks.  
The design is based on the Von Neumann architecture and contains an ALU, registers, memory, control logic, and a program counter.

![Main Circuit](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/main.png)

---
<a id="features"></a>
## ⚙️ Features
- 8-bit data bus, 4-bit address bus  
- Program Counter, Instruction Register, and Control Sequencer  
- Arithmetic Logic Unit (ALU) supporting ADD and SUB operations  
- RAM and Register File integrated with control signals  
- Step-by-step and auto clock execution modes  
- Fully modular design with labeled subcircuits  
- All components built manually in Logisim (no pre-made components)

---
<a id="architecture"></a>

## 🧠 Architecture
The SAP-1 consists of these major modules:

- **Program Counter (PC)** — holds the address of the next instruction to be executed.  
  It increments automatically after each instruction unless a jump occurs.  
  ![Program Counter](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/pc.png)

- **Memory Address Register (MAR)** — temporarily stores the memory address from which the CPU wants to read or write data.  
  It acts as the bridge between the CPU and RAM.  

- **SRAM** — stores both program instructions and data values.  
  This is the main memory of the SAP-1 where instructions and operands reside.  
  ![SRAM](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/sram.png)

- **Instruction Register (IR)** — holds the currently fetched instruction (both opcode and operand).  
  This allows the control unit to decode and execute the instruction step by step.  
  ![Instruction Register](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/ins%20reg.png)

- **Registers (A & B)** — temporary storage for arithmetic operations.  
  Register A is usually the accumulator, while B is used as a secondary operand.  
  ![Registers](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/reg.png)

- **ALU (Arithmetic Logic Unit)** — performs arithmetic operations like ADD and SUB.  
  It takes inputs from registers A and B and outputs the result back to A or the output register.  
  ![ALU](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/ALU.png)

- **Control Sequencer** — a hardwired unit that orchestrates the fetch-decode-execute cycle.  
  It generates control signals for all other components in a precise timing sequence.  
  ![Control Sequencer](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/cs.png)

---
<a id="controlunit"></a>
## 🕹️ Control Unit
The control unit uses a **hardwired sequencer** that generates timing and control signals (T1–T6) for each micro-operation.  
A state counter and decoder combination ensures correct instruction flow and clock synchronization.

![Control Sequencer](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/opcode.png)  
![State Counter](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/state_counter.png)

---
<a id="instructionset"></a>
## 🧾 Instruction Set

| Mnemonic | Opcode (Hex) | Description |
|-----------|--------------|-------------|
| LDA | 1A | Load value from memory address into Register A |
| ADD | 2B | Add value from memory address to A |
| SUB | 3C | Subtract value from memory address from A |
| STA | 4D | Store value of A into memory address |
| JMP | 50 | Jump to given address |
| OUT | 70 | Output value of Register A |
| NOP | 00 | No operation / unused |
| HLT | F0 | Halt program execution |

![Opcode Logic](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/opcode.png)  

---
<a id="howtorun"></a>
## ▶️ How to Run
1. Open the `.circ` file (`2008007_cs_project.circ`) in **Logisim Evolution**  

2. Load your **ROM program and RAM data together** as one script:
3. Turn ON the clock and observe each micro-step  
4. Check Register A, B, and output register for results  
5. Use the **Auto Load** feature for continuous execution

🎥 [Watch the demonstration video on YouTube](https://youtu.be/2j5gOPioyDY?si=CJrzVuyPzPSJmknV)

---
<a id="author"></a>
## ✍️ Author
**Nusaiba Tahsin**  
Department of Electronics and Telecommunication Engineering  
Chittagong University of Engineering and Technology (CUET)  
2025






