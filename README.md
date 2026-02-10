# 🧩 FPGA Maze Game (Verilog)

![Verilog](https://img.shields.io/badge/HDL-Verilog-purple)
![FPGA](https://img.shields.io/badge/FPGA-DE1--SoC-blue)
![Graphics](https://img.shields.io/badge/Graphics-VGA%20640x480-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A **hardware-based, tile-based maze exploration game** inspired by *Wayout (1982)*, implemented entirely in **Verilog** on an **Altera DE1-SoC FPGA**.

The project features real-time VGA graphics and fully synchronous movement and collision logic implemented directly at the hardware level, with no embedded CPU or software game loop.

---

## ⚠️ Academic Integrity Notice

To comply with university academic integrity policies:

- **Source code is not included**
- **Only the compiled FPGA bitstream (`.sof`) is provided**
- This allows the project to be demonstrated on hardware without exposing implementation details

Students currently enrolled in related courses should **not copy or submit** this work for academic credit.

---

## 🎮 Game Overview

- **Resolution:** 640 × 480 (VGA)
- **Refresh Rate:** 60 Hz (25 MHz pixel clock)
- **Input:** On-board pushbuttons `KEY[4:1]`
- **Output:** VGA Monitor
- **Gameplay:** Tile-based movement with real-time wall collision detection

The player moves exactly **one tile per input**, ensuring deterministic motion, stable rendering, and precise collision handling at the hardware level.

---

## 🛠 Hardware Requirements

- **FPGA Board:** DE1-SoC (Cyclone V – 5CSEMA5F31C6)
- **VGA Monitor:** 640 × 480 support
- **On-board pushbuttons:** `KEY[4:1]`
- **USB-Blaster**

> The provided `.sof` file is **device-specific** and will not run on other FPGA boards without recompilation.

---

## 📥 Loading the Game

1. Download the `.sof` file from the `output_files/` directory
2. Connect the FPGA board via **USB-Blaster**
3. Open **Quartus Prime Programmer**
4. Select **Hardware Setup** → `USB-Blaster`
5. Add `mazegame.sof` and check **Program/Configure**
6. Click **Start**

---

## 🕹 Controls

| Key    | Action        |
|------|---------------|
| KEY[4] | Move Left     |
| KEY[3] | Move Right    |
| KEY[2] | Move Forward  |
| KEY[1] | Move Backward |
| KEY[0] | Game Reset (Active Low) |

---

## 🚀 Architecture Highlights

- 🖥 **Custom VGA Controller**  
  Generates 640×480 timing signals and pixel output entirely in hardware

- 🧱 **Maze ROM**  
  Bit-mapped tile storage representing walls and paths

- 🧭 **Tile-Based Movement Engine**  
  One-step-per-input logic with collision detection before movement

- 🔘 **Button Input Handling**  
  Debounced and synchronously sampled on-board pushbuttons

- 🎨 **Controlled Redraw Logic**  
  Prevents residual pixels and visual artifacts during movement

---

## 🧠 Control Logic

A **finite state machine (FSM)** coordinates reset, idle, and movement states.  
This ensures deterministic timing, reliable input handling, and predictable behavior across all clock cycles.

---

## 📌 Engineering Focus

This project demonstrates:

- FPGA-based graphics pipelines
- Synchronous digital design
- Hardware collision detection
- Finite state machine control
- Real-time VGA timing and rendering
- Debugging and validation directly on hardware

These skills are directly applicable to **embedded systems**, **FPGA development**, and **hardware acceleration** roles.

---

## 🎥 Live Demo

| VGA Monitor View |
|-----------------|
| [![VGA Monitor View](demo/projvideophoto.png)](https://github.com/user-attachments/assets/be4b0853-519a-4140-b1d3-de9dfa430ad4) |

---

## 👤 Author

**Apiwich Sumeksri**  
Electrical & Computer Engineering  
University of Toronto
