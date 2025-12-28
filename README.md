# FPGA Maze Game (Verilog)

A hardware-based, tile-based maze exploration game inspired by *Wayout (1982)*, implemented entirely in **Verilog** on an **Intel/Altera DE1-SoC FPGA**. The project features real-time VGA graphics, PS/2 keyboard input, and fully synchronous movement and collision logic implemented at the hardware level.

---

## ⚠️ Academic Integrity Notice
To comply with university academic integrity policies:
- **Source code is not included**
- **Only the compiled FPGA bitstream (.sof) is provided**
- This allows users to run the game on hardware without exposing implementation details

---

## 🎮 Game Overview
- **Resolution:** 640×480 (VGA)
- **Refresh Rate:** 60 Hz (25 MHz pixel clock)
- **Input:** PS/2 Keyboard
- **Output:** VGA Monitor
- **Gameplay:** Tile-based movement with real-time wall collision detection

The player moves one tile per keypress, ensuring deterministic, glitch-free motion and precise collision handling.

---

## 🛠 Hardware Requirements
- **FPGA Board:** DE1-SoC (Cyclone V – 5CSEMA5F31C6)
- **VGA Monitor:** 640×480 support
- **PS/2 Keyboard**
- **USB-Blaster**

> The provided `.sof` file is device-specific and will not run on other boards without recompilation.

---

## 📥 Programming Instructions
1. Download the `.sof` file from `output_files/`
2. Connect the FPGA via USB-Blaster
3. Open **Quartus Prime Programmer**
4. Select **USB-Blaster** under Hardware Setup
5. Add the `.sof` file and check **Program/Configure**
6. Click **Start**

---

## 🕹 Controls
| Key | Action |
|---|---|
| Arrow Keys | Move player (Up / Down / Left / Right) |
| KEY[0] | Hardware Reset (Active Low) |

---

## 🚀 Architecture Highlights
- **Custom VGA Controller:** Generates 640×480 timing and pixel output
- **Maze ROM:** Bit-mapped tile storage for walls and paths
- **Tile-Based Movement Engine:** One-step-per-input logic with collision checks
- **PS/2 Keyboard Decoder:** Stable make/break handling without key ghosting
- **Clean Redraw Logic:** Prevents residual pixels and screen artifacts

---

## 🧠 Control Logic
A finite state machine coordinates reset, idle, and movement states, ensuring deterministic timing, reliable input handling, and predictable hardware behavior.

---

## 📌 Engineering Focus
This project demonstrates real-time digital design, FPGA graphics pipelines, synchronous control logic, and hardware-level debugging—skills directly applicable to embedded systems and FPGA-based development.
