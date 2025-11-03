# Booth's Algorithm Visualizer

A graphical, step-by-step simulation of Booth’s Multiplication Algorithm built using **HTML**, **CSS**, and **JavaScript**.  
This project visually demonstrates how signed binary multiplication is performed at the register level, making it ideal for **Computer Organization and Architecture** coursework or demonstrations.

---

## Live Demo

**URL:** [https://boothsalgorithmvisual.netlify.app](https://boothsalgorithmvisual.netlify.app)  

---

## About the Project

Booth’s Algorithm is an efficient method for multiplying signed binary numbers using **two’s complement arithmetic**.  
This visualizer simulates the internal register operations performed by a processor’s **Arithmetic Logic Unit (ALU)** during multiplication.

The user can initialize registers, step through each operation, or run the algorithm automatically while observing how each register (`A`, `Q`, `M`, `Q(-1)`) changes in every iteration.

---

## Features

- Accepts signed decimal inputs (positive and negative)
- Converts input values into binary using two’s complement
- Displays live register values:
  - `A` — Accumulator  
  - `Q` — Multiplier  
  - `M` — Multiplicand  
  - `Q(-1)` — Previous bit
- Step-by-step execution with “Play” and “Reset” controls
- Demonstrates arithmetic right shift operations
- Logs every iteration in a dynamic table
- Clean, responsive user interface

---

## Tech Stack

| Component | Technology |
|------------|-------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Hosting | Netlify |
| Version Control | Git & GitHub |

---

## Booth’s Algorithm Summary

| Bit Pair (Q₀ Q₋₁) | Operation |
|--------------------|------------|
| 00 | No operation |
| 01 | Add `M` to `A` |
| 10 | Subtract `M` from `A` |
| 11 | No operation |

After each operation, perform an **arithmetic right shift** on `(A, Q, Q₋₁)` and repeat for *n* cycles (equal to the bit width).


