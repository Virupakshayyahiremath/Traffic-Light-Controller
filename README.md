# 🚦 Traffic Light Controller using Verilog

This project implements a **Traffic Light Controller** using a **Finite State Machine (FSM)** in **Verilog HDL**. The system manages traffic lights for:
- Two main roads (M1 and M2)
- A main-turn (MT) road
- A side (S) road

The FSM transitions through **6 distinct states** with specified timing to ensure smooth and coordinated traffic movement.

---

## 📁 Repository Contents

| File/Folder        | Description |
|--------------------|-------------|
| `RTL Code.txt`     | Verilog RTL code for the traffic light controller |
| `Testbench.txt`    | Verilog testbench to simulate the design |
| `Logic_Diagram.png`| Block/logic diagram of the controller |
| `State_Diagram.png`| FSM state diagram |
| `State_Table.png`  | State transition table |
| `RTL_Schematic_View.png` | Synthesized RTL schematic (from simulation tool) |
| `traffic_light_waveform.png` | Waveform output from simulation |
| `README.md`        | Project documentation |

---

## ⚙️ FSM Design Overview

The controller cycles through **6 states (S1 to S6)** with defined durations:

| State | M1 | M2 | MT | S | Duration |
|-------|----|----|----|---|----------|
| S1    | G  | G  | R  | R | 7 units  |
| S2    | G  | Y  | R  | R | 2 units  |
| S3    | G  | R  | G  | R | 5 units  |
| S4    | Y  | R  | Y  | R | 2 units  |
| S5    | R  | R  | R  | G | 3 units  |
| S6    | R  | R  | R  | Y | 2 units  |

*(G: Green, Y: Yellow, R: Red)*  
*(Each light is encoded as 3-bit: 001=Green, 010=Yellow, 100=Red)*

---

## 🔍 Simulation Output

The design was simulated using **EDA Playground** with **Icarus Verilog**. The testbench applies clock and reset, and logs signal activity over time.

### ✅ EPWave Output Screenshot:

![Traffic Light FSM Waveform](traffic_light_waveform.png)

---

## ▶️ How to Run the Design

### 🧪 1. Run on [EDA Playground](https://edaplayground.com)

- Use `SystemVerilog/Verilog` as the language.
- Paste RTL code in `design.sv` and testbench in `testbench.sv`.
- Select **Icarus Verilog** as simulator.
- Add this in your testbench to enable waveform:

```verilog
initial begin
  $dumpfile("dump.vcd");
  $dumpvars(0, testbench);
end
