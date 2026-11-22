# 🚦 Traffic Light Controller Using Verilog HDL

![Verilog](https://img.shields.io/badge/Language-Verilog-blue)
![FPGA](https://img.shields.io/badge/Platform-FPGA-orange)
![Vivado](https://img.shields.io/badge/Tool-Xilinx%20Vivado-red)
![FSM](https://img.shields.io/badge/Design-Moore%20FSM-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This project implements an automatic four-way traffic light controller using **Verilog Hardware Description Language (HDL)** and a **Moore Finite State Machine (FSM)**.

The system controls traffic signals for two intersecting roads:

- North-South (NS)
- East-West (EW)

The controller automatically switches between RED, YELLOW, and GREEN signals using a clock-based timing mechanism.

The design is developed for RTL simulation and FPGA implementation using Xilinx Vivado.

## 🎯 Objectives

- Design an automatic four-way traffic light controller.
- Implement a Moore Finite State Machine using Verilog HDL.
- Generate traffic signals using clock-based timing.
- Control signal duration using a counter.
- Verify the design using a Verilog testbench.
- Understand FSM-based digital system design.

## 🛠️ Tools and Technologies

| Component | Technology |
|---|---|
| HDL | Verilog |
| Design Software | Xilinx Vivado |
| Simulation | Vivado Simulator |
| Architecture | Moore FSM |
| Implementation | FPGA |

## ⚙️ System Architecture

The controller consists of:

1. Clock input
2. Reset input
3. Timing counter
4. Four-state Moore FSM
5. Traffic signal output logic

## 🔄 FSM State Sequence

The controller operates through four states:

| State | North-South | East-West |
|---|---|---|
| NS_GREEN | GREEN | RED |
| NS_YELLOW | YELLOW | RED |
| EW_GREEN | RED | GREEN |
| EW_YELLOW | RED | YELLOW |

### State Transition Diagram

```text
       +-----------+
       | NS_GREEN  |
       +-----------+
             |
             v
       +-----------+
       | NS_YELLOW |
       +-----------+
             |
             v
       +-----------+
       | EW_GREEN  |
       +-----------+
             |
             v
       +-----------+
       | EW_YELLOW |
       +-----------+
             |
             |
             +--------> NS_GREEN
```

## 💻 Verilog Source Code

The main Verilog module is available in:

`src/traffic_light.v`

The module includes:
- State declaration
- Clock counter
- State transition logic
- Moore output logic
- Asynchronous reset

## 🧪 Testbench

The testbench is available in:

`testbench/traffic_light_tb.v`

It generates the clock signal, applies reset, and observes the traffic signal outputs.

Short timing parameters are used to verify all four states quickly during simulation.

## 📊 Expected Simulation Results

| State | NS_R | NS_Y | NS_G | EW_R | EW_Y | EW_G |
|---|---:|---:|---:|---:|---:|---:|
| NS_GREEN | 0 | 0 | 1 | 1 | 0 | 0 |
| NS_YELLOW | 0 | 1 | 0 | 1 | 0 | 0 |
| EW_GREEN | 1 | 0 | 0 | 0 | 0 | 1 |
| EW_YELLOW | 1 | 0 | 0 | 0 | 1 | 0 |

## 📁 Project Structure

```text
Verilog-Traffic-Light-Controller/
│
├── README.md
├── LICENSE
│
├── src/
│   └── traffic_light.v
│
├── testbench/
│   └── traffic_light_tb.v
│
├── diagrams/
│   ├── block_diagram.png
│   └── state_diagram.png
│
├── simulation/
│   └── waveform.png
│
└── report/
    └── Traffic_Light_Controller_Report.pdf
```

## ▶️ How to Run the Project

1. Install and open Xilinx Vivado.
2. Create a new RTL project.
3. Add `traffic_light.v` under Design Sources.
4. Add `traffic_light_tb.v` under Simulation Sources.
5. Set `traffic_light_tb` as the simulation top module.
6. Run Behavioral Simulation.
7. Observe the output waveforms.
8. Verify the four-state traffic signal sequence.

## ⭐ Features

- Automatic traffic signal control.
- Four-state Moore FSM architecture.
- Clock-based timing control.
- Adjustable green and yellow durations.
- Reset functionality.
- Synthesizable RTL design.

## 🚀 Future Enhancements

- Vehicle density detection using IR sensors.
- Emergency vehicle priority.
- Pedestrian crossing control.
- Adaptive traffic signal timing.
- Real-time intelligent traffic management.

## 📚 Applications

- Automatic road traffic control.
- Four-way intersection management.
- FPGA-based digital system projects.
- Educational FSM implementation.

## 👨‍💻 Author

**prawin.r**

Third Year – Electronics and Communication Engineering (ECE)



---

⭐ If you find this project useful, consider giving this repository a star!

**Thank you for visiting my project!**
