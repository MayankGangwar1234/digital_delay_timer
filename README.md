# LS7212 Delay Timer (Verilog)

This project implements a **Verilog model of the LS7212 programmable delay timer**. It includes the Verilog design (`delay_timer_ls7212.v`) and a comprehensive testbench (`tb_ls7212.v`) to validate its functionality across all four timing modes.

## 🔧 Features

- 8-bit programmable delay using `wb` input.
- Trigger edge detection (rising/falling).
- Four operating modes:
  - **Mode 00** – One-Shot
  - **Mode 01** – Delayed Operate
  - **Mode 10** – Delayed Release
  - **Mode 11** – Delayed Dual
- Active-low output: `delay_out_n`

## 📁 Files

| File Name           | Description                               |
|---------------------|-------------------------------------------|
| `delay_timer_ls7212.v` | Main Verilog module for the timer        |
| `tb_ls7212.v`          | Testbench for functional simulation      |
| `README.md`            | This documentation file                  |

## 🧪 How to Simulate

1. Open Vivado and create a new project.
2. Add `delay_timer_ls7212.v` to **Design Sources**.
3. Add `tb_ls7212.v` to **Simulation Sources**.
4. Set `tb_ls7212` as the **simulation top module**.
5. Run Behavioral Simulation.

## ✅ Expected Behavior

- `delay_out_n` should toggle depending on mode and trigger input.
- Width of pulse/delay is determined by `wb` (pulse width = `wb`, delay = `(2*wb + 1)/2`).
- Reset should be asserted at the beginning to initialize the timer.

## 🖥️ Waveform Example

Below is a sample output waveform:

![Waveform](screenshot.png)

## 🛠️ Requirements

- Vivado or any Verilog simulator (ModelSim, Icarus Verilog)
- Basic understanding of timing control in digital logic






