# Asynchronous FIFO Design (Verilog)

## 📌 Overview

This project implements an **Asynchronous FIFO (First-In-First-Out)** buffer in SystemVerilog, designed for reliable data transfer between **different clock domains**. It addresses clock domain crossing (CDC) challenges using synchronization techniques and Gray code pointers.

---

## ⚙️ Features

* Dual clock operation (independent read & write clocks)
* Safe Clock Domain Crossing (CDC)
* Gray code pointer implementation
* Full and Empty flag detection
* Parameterized FIFO depth and width
* Synthesizable design

---

## 🧠 Design Details

* Separate **read** and **write pointers** maintained in different clock domains
* Pointers converted to **Gray code** to minimize metastability issues
* Multi-stage synchronizers used for safe pointer transfer across domains
* Full/Empty conditions determined using pointer comparison logic

---

## 📁 Project Structure

```
Async-FIFO/
├── src/
│   └── async_fifo.sv        # FIFO design
├── tb/
│   └── tb_async_fifo.sv     # Testbench
├── constraints/
│   └── fifo.xdc             # (optional, if FPGA used)
└── README.md
```

---

## 🧪 Simulation

The testbench verifies:

* Correct data ordering (FIFO behavior)
* Full and Empty flag conditions
* Operation under different read/write clock frequencies

Run simulation using:

* Xilinx Vivado Simulator / ModelSim / any SV-compatible simulator

---

## 🛠️ Tools Used

* SystemVerilog
* Xilinx Vivado

---

## 📊 Applications

* Clock domain crossing (CDC) systems
* High-speed data buffering
* FPGA-based communication interfaces

---

## 📌 Author

[Aadi Khandekar]

---

## ⭐ Notes

This project focuses on **robust CDC design practices**, which are critical in digital systems and frequently tested in hardware design interviews.
