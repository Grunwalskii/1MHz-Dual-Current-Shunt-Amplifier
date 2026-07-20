# ⚡ 1MHz Dual-Range Current Shunt Amplifier

High-bandwidth, high-precision dual-range current shunt measurement module. Featuring two independent sensing stages ($50\text{ m}\Omega$ for high-current paths and $500\text{ m}\Omega$ for low-current profiling), this board is engineered for dynamic, high-speed power analysis across a wide range of loads, achieving up to $1\text{ MHz}$ bandwidth performance.

![Rendering](https://github.com/Grunwalskii/1MHz-Dual-Current-Shunt-Amplifier/blob/main/Images/3DRendering.png)

## 🛠️ Key Architectural Features

### 1. Dual-Range Precision Sensing
* **High-Current (HC) Stage:** Employs a precision $50\text{ m}\Omega$ inline shunt resistor (`R3`) coupled with an operational amplifier stage providing a stable $20\times$ differential gain ($R_2/R_1 = 20\text{ k}\Omega / 1\text{ k}\Omega$).
* **Low-Current (LC) Stage:** Employs a higher sensitivity $500\text{ m}\Omega$ inline shunt resistor (`R6`) paired with an identical $20\times$ differential gain amplifier configuration ($R_{10}/R_7 = 20\text{ k}\Omega / 1\text{ k}\Omega$).
* **Dedicated Analog Outputs:** Yields independent, buffered analog voltage outputs (`HCOUT` and `LCOUT`) tailored for direct oscilloscope observation or high-speed ADC sampling.

### 2. High-Performance Signal Conditioning
* **Amplifier Core:** Powered by the **OPA2322AIDGKR** (`U1`), a dual, low-noise, low-power, rail-to-rail input/output operational amplifier featuring excellent bandwidth capabilities ($20\text{ MHz}$ GBW product) to effortlessly sustain clean signals up to the target $1\text{ MHz}$ measurement threshold.

### 3. Floating Measurement
* **True Floating Measurement (High-Side & Low-Side Versatility):** Standard mains-powered test equipment or USB power supplies share a common ground with the target system. By powering the OPA2322 via an isolated coin-cell battery (`U4`) and the `HX4002` charge pump, the entire amplifier circuit becomes **fully floating**. This allows you to safely insert the shunts anywhere in the circuit—either on the high-side (before the load) or the low-side (after the load)—without creating dangerous ground loops that ruin measurements or damage equipment.

---

## 🔌 Core Interface Map

### Sensing Terminals
* `HC+` / `HC-`: High-current shunt path inputs ($50\text{ m}\Omega$).
* `LC+` / `LC-`: Low-current shunt path inputs ($500\text{ m}\Omega$).

### Output Test Points
* `HCOUT`: Analog signal output for the High-Current stage.
* `LCOUT`: Analog signal output for the Low-Current stage.

* ## Support

If you enjoy this project and want to support its development, you can buy me a coffee:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/W1L623I6WG)
