# Traffic Light Controller using Verilog

This project implements a simple **traffic light controller** using Verilog HDL. It is designed as a **Finite State Machine (FSM)** to control signal lights for a T-intersection with defined time delays for each state.

## 🚦 Features

- Controls Red, Yellow, and Green lights for both main and side roads.
- Implements FSM-based logic with defined state transitions.
- Configurable timing for each signal state (e.g., Green: 10s, Yellow: 3s).
- Testbench provided for simulation and verification.
- Includes design diagrams and state tables.

## 📁 Files Included

- `RTL Code.txt`: Verilog source code for the FSM
- `Testbench.txt`: Verilog testbench for simulation
- `State_Diagram.png`: Visual state diagram of the controller
- `State_Table.png`: State transition table
- `Logic_Diagram.png`: Logic circuit design
- `RTL_Schematic_View.png`: RTL schematic from synthesis
- `Directions.png`: Intersection layout

## 🛠 Tools Used

- **Xilinx ISE** / **Vivado** for simulation and synthesis
- **ModelSim** (optional) for behavioral simulation
- Any compatible FPGA board (e.g., Spartan-3/6) for implementation

## 🔧 How It Works

The controller cycles through four primary states:
1. Main Road Green
2. Main Road Yellow
3. Side Road Green
4. Side Road Yellow

Each state lasts for a specific duration (configured using counters), and transitions are controlled by a synchronous FSM.

## 📌 To Do

- Add pedestrian crossing support
- Add vehicle sensor input for adaptive timing
- Extend for a 4-way intersection

## 👨‍💻 Author

- **Virupakshayya Hiremath**

---

Feel free to clone, modify, and improve. Contributions are welcome!
