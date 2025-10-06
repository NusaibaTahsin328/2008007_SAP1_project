# SAP-1 CPU (Simple-As-Possible) — Logisim Evolution
![CPU Badge](https://img.shields.io/badge/CPU-SAP--1-brightgreen)
![Logisim Badge](https://img.shields.io/badge/Tool-Logisim--Evolution-blue)

---

## 📘 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Control Unit](#control-unit)
- [Instruction Set](#instruction-set)
- [How to Run](#how-to-run)
- [Figures](#figures)
- [Future Work](#future-work)
- [Author](#author)

---

## 🧩 Overview
This project is my implementation of the **SAP-1 (Simple As Possible) CPU** using **Logisim Evolution**.  
It demonstrates the core principles of computer architecture — fetching, decoding, and executing 8-bit instructions through modular hardware blocks.

The design follows the Von Neumann architecture and includes ALU, registers, memory, control logic, and a program counter.

---

## ⚙️ Features
- 8-bit data bus, 4-bit address bus  
- Program Counter, Instruction Register, and Control Sequencer  
- Arithmetic Logic Unit (ALU) supporting ADD and SUB operations  
- RAM and Register File integrated with control signals  
- Step-by-step and auto clock execution modes  
- Fully modular design with labeled subcircuits  
- All components built manually in Logisim (no pre-made components)

---

## 🧠 Architecture
![Main Circuit](Images/main.png)

The SAP-1 consists of the following major modules:
- **Program Counter (PC)** — holds the address of the next instruction  
- **Memory Address Register (MAR)** — stores current memory address  
- **RAM (SRAM)** — stores program instructions and data  
- **Instruction Register (IR)** — holds opcode and operand  
- **Registers (A & B)** — for temporary data storage  
- **ALU** — performs addition and subtraction  
- **Control Section** — orchestrates the fetch-decode-execute cycle

---

## 🕹️ Control Unit
![Control Unit](Images/decoder.png)

The control unit is a **hardwired sequencer**.  
It generates timing and control signals (T1–T6) to activate micro-operations for each instruction.  
A counter and decoder combination ensure instruction flow and clock synchronization.

---

## 🧾 Instruction Set

| Mnemonic | Opcode (Hex) | Description |
|-----------|---------------|-------------|
| LDA | 1D | Load value into Register A |
| LDB | 2E | Load value into Register B |
| ADD | 30 | Add B to A |
| SUB | 40 | Subtract B from A |
| STA | 5F | Store A into memory |
| JMP | 65 | Jump to given address |
| HLT | F0 | Halt program execution |

---

## ▶️ How to Run
1. Open the `.circ` file (`2008007_cs_project.circ`) in **Logisim Evolution**  
2. Load your hex program into ROM:
3. Turn ON the clock and observe each micro-step  
4. Check Register A, B, and output register for results  
5. Use the **Auto Load** feature for continuous execution

---

## 🖼️ Figures

| # | Description | Image |
|---|--------------|-------|
| 1 | ALU | ![ALU](Images/ALU.png) |
| 2 | Auto Load Circuit | ![Auto Load](Images/auto_load.png) |
| 3 | Control Signals | ![CS](Images/cs.png) |
| 4 | Decoder | ![Decoder](Images/decoder.png) |
| 5 | Instruction Register | ![Instruction Register](Images/ins%20reg.png) |
| 6 | Main Circuit | ![Main Circuit](Images/main.png) |
| 7 | Opcode Logic | ![Opcode](Images/opcode.png) |
| 8 | Program Counter | ![PC](Images/pc.png) |
| 9 | Registers | ![Registers](Images/reg.png) |
| 10 | SRAM | ![SRAM](Images/sram.png) |
| 11 | SRAM Cell | ![SRAM Cell](Images/sram_cell.png) |
| 12 | State Counter | ![State Counter](Images/state_counter.png) |

---
🎥 **Watch the demonstration video:**  
[Control Sequencer and Architecture Design of an Automated SAP-1 Microprocessor System](https://youtu.be/2j5gOPioyDY?si=CJrzVuyPzPSJmknV)

---
## 🚀 Future Work
- Add instructions: `OUT`, `JZ`, and `NOP`  
- Implement microprogrammed control logic  
- Extend to **SAP-2** with branching and flag registers  
- Display unit (7-segment) integration

---

## ✍️ Author
**Nusaiba Tahsin**  
Department of Electronics and Telecommunication Engineering  
Chittagong University of Engineering and Technology (CUET)  
2025

---


