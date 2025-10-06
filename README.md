# SAP-1 CPU (Simple-As-Possible) — Logisim Evolution
![CPU Badge](https://img.shields.io/badge/CPU-SAP--1-brightgreen)
![Logisim Badge](https://img.shields.io/badge/Tool-Logisim--Evolution-blue)
![CUET](https://img.shields.io/badge/CUET-ETC-red)

---

## 📘 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Control Unit](#control-unit)
- [Instruction Set](#instruction-set)
- [How to Run](#how-to-run)
- [Future Work](#future-work)
- [Author](#author)

---

## 🧩 Overview
This project is an implementation of the **SAP-1 (Simple As Possible) CPU** using **Logisim Evolution**.  
It demonstrates the core principles of computer architecture, including fetching, decoding, and executing 8-bit instructions through modular hardware blocks.  
The design is based on the Von Neumann architecture and contains an ALU, registers, memory, control logic, and a program counter.

![Main Circuit](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/main.png)

---

## ⚙️ Features
- 8-bit data bus, 4-bit address bus  
- Program Counter, Instruction Register, and Control Sequencer  
- Arithmetic Logic Unit (ALU) supporting ADD and SUB operations  
- RAM and Register File integrated with control signals  
- Step-by-step and auto clock execution modes  
- Fully modular design with labeled subcircuits  
- All components built manually in Logisim (no pre-made components)

![Registers](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/reg.png)  
![ALU](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/ALU.png)

---

## 🧠 Architecture
The SAP-1 consists of these major modules:
- **Program Counter (PC)** — holds the address of the next instruction  
- **Memory Address Register (MAR)** — stores current memory address  
- **SRAM** — stores program instructions and data  
- **Instruction Register (IR)** — holds opcode and operand  
- **Registers (A & B)** — for temporary data storage  
- **ALU** — performs addition and subtraction  
- **Control Sequencer** — orchestrates the fetch-decode-execute cycle

![Program Counter](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/pc.png)  
![SRAM](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/sram.png)  
![Instruction Register](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/ins%20reg.png)

---

## 🕹️ Control Unit
The control unit uses a **hardwired sequencer** that generates timing and control signals (T1–T6) for each micro-operation.  
A state counter and decoder combination ensures correct instruction flow and clock synchronization.

![Control Sequencer](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/decoder.png)  
![State Counter](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/state_counter.png)

---

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
![Opcode Decoder](https://github.com/NusaibaTahsin328/2008007_SAP1_project/blob/main/opcode.png)

---

## ▶️ How to Run
1. Open the `.circ` file (`2008007_cs_project.circ`) in **Logisim Evolution**  

2. Load your **ROM program and RAM data together** as one script:

```text
# ROM (0–7)
0: 1A  ; LDA 10
1: 2B  ; ADD 11
2: 3C  ; SUB 12
3: 4D  ; STA 13
4: 50  ; JMP 0
5: 70  ; OUT
6: 00  ; NOP / unused
7: 00  ; NOP / unused

# RAM (10–15)
10: 0A
11: 0B
12: 0C
13: 0D
14: 00
15: 00
## ▶️ How to Run
1. Turn ON the clock and observe each micro-step  
2. Check Register A, B, and output register for results  
3. Use the **Auto Load** feature for continuous execution

🎥 **Watch the demonstration video:**  
[Control Sequencer and Architecture Design of an Automated SAP-1 Microprocessor System](https://youtu.be/2j5gOPioyDY?si=CJrzVuyPzPSJmknV)

---

## ✍️ Author
**Nusaiba Tahsin**  
Department of Electronics and Telecommunication Engineering  
Chittagong University of Engineering and Technology (CUET)  
2025
