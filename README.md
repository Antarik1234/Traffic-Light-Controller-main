# 🚦 Traffic Light Controller (Verilog / Digital Design)

## 📌 Overview

This project implements a **Traffic Light Controller** using **Verilog HDL**.
It manages traffic flow between a **main road** and a **side road** using a **sensor-based control system**.

The controller ensures efficient traffic handling by dynamically switching signals based on vehicle presence.

---

## ⚙️ Features

* 🚗 Sensor-based traffic detection
* 🔄 Automatic signal switching
* ⏱️ Timed transitions between states
* 🟢🟡🔴 Standard traffic light sequence (Red, Yellow, Green)
* 📊 Simulation waveform support
* 🧩 RTL and synthesized design included

---

## 🧠 System Working

* By default, the **main road signal remains GREEN**.
* When a vehicle is detected on the **side road (Sensor = 1)**:

  * Main Road: GREEN → YELLOW → RED
  * Side Road: RED → GREEN → YELLOW
* After the cycle completes, control returns to the main road.

---

## 🏗️ Design Details

### Signal Encoding (RYG Format)

| Binary | Meaning |
| ------ | ------- |
| 001    | Green   |
| 010    | Yellow  |
| 100    | Red     |

---

## 📂 Project Structure

```
Traffic-Light-Controller/
│
├── src/
│   └── traffic_light_controller.v
│
├── simulation/
│   └── waveform.png
│
├── synthesis/
│   ├── rtl_schematic.png
│   └── synthesized_design.png
│
├── output/
│   └── results_table.txt
│
└── README.md
```

---

## 🖥️ Simulation Results

| Time (ns) | Sensor | MAIN (RYG) | SIDE (RYG) |
| --------- | ------ | ---------- | ---------- |
| 0         | 0      | 001        | 100        |
| 100000    | 1      | 001        | 100        |
| 135000    | 1      | 010        | 100        |
| 175000    | 1      | 100        | 001        |
| 200000    | 0      | 100        | 001        |
| 235000    | 0      | 100        | 010        |
| 275000    | 0      | 001        | 100        |
| 320000    | 1      | 001        | 100        |
| 335000    | 1      | 010        | 100        |
| 375000    | 1      | 100        | 001        |
| 435000    | 1      | 100        | 010        |
| 470000    | 0      | 100        | 010        |
| 475000    | 0      | 001        | 100        |

---

## 🧪 Tools & Technologies

* Verilog HDL
* ModelSim / Xilinx Vivado (Simulation)
* Xilinx Vivado (Synthesis)

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/traffic-light-controller.git
cd traffic-light-controller
```

### 2️⃣ Run Simulation

* Open the project in ModelSim / Vivado
* Compile Verilog files
* Run:

```bash
run -all
```

---

## 📚 Applications

* Smart traffic control systems
* Embedded system design
* FPGA-based automation
* IoT-based traffic monitoring

---

## 🔮 Future Improvements

* Adaptive timing using AI/ML
* Multi-lane traffic control
* Emergency vehicle priority system
* Real-time IoT integration

---

## 👨‍💻 Author

**Agnik Maity**
Institute of Engineering & Management, Kolkata

---

## 📜 License

This project is licensed under the **GNU License**.

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
