# Ultra-Low-Power-Neural-Processing-Unit-for-IoT-Devices



This repository contains the architectures, benchmarking results, and energy-efficiency analysis

**“Low-Power VLSI Accelerators for Edge AI in IoT Devices”**

---

## 🔍 Problem

Modern IoT devices such as cameras, wearables, and sensors require **on-device AI inference** under extreme power constraints (few milliwatts).  
Running CNNs on CPUs or GPUs wastes energy due to massive data movement and inefficient memory access.

For example:
- AlexNet requires **6.6 × 10⁸ MACs per image**
- MobileNet requires **569 million MACs per inference** :contentReference[oaicite:1]{index=1}  

This makes specialized **low-power VLSI accelerators** essential.

---

## 🧠 Proposed Architecture

Edge AI accelerators consist of:

- 2D MAC processing elements  
- On-chip SRAM buffers  
- Host CPU interface  
- Optimized dataflow for reuse  

<img width="380" height="377" alt="image" src="https://github.com/user-attachments/assets/46a4c8f5-0f82-40df-ad50-9a99aa2e9998" />



---

## ⚡ Low-Power Techniques Used

The paper analyzes:

| Technique | Benefit |
|--------|-------|
| DVFS | Quadratic power savings |
| Clock & Power Gating | Eliminates idle leakage |
| Sparsity Exploitation | Skips zero weights |
| Quantization | Reduces memory energy |
| In-Memory Computing | Removes data movement |
| Near-Sensor AI | Avoids raw data transfer |

These methods enable **10×–1000× energy savings** over CPUs/GPUs :contentReference[oaicite:3]{index=3}  

---

## 🧮 Workload Characteristics

Edge AI uses **small batch (1)** inference on compact models like MobileNet.

Convolution layers dominate compute:

<img width="425" height="385" alt="image" src="https://github.com/user-attachments/assets/83753b63-4313-4cbe-9a6e-259e62383ab5" />






## 🧪 Benchmark Results

Based on published silicon results:

| Accelerator | Technology | Power | Efficiency |
|------------|------------|-------|------------|
| Eyeriss | 65nm | 278 mW | 83 GOPS/W |
| EIE | 45nm | 590 mW | 32 GOPS/W |
| ISAAC | 45nm | — | 180 GOPS/W |
| PUMA | 65nm | — | 837 GOPS/W |
| TrueNorth | 28nm | 65 mW | 10⁶ synops/J |



---

## 📉 Energy vs Latency Tradeoff
<img width="811" height="568" alt="image" src="https://github.com/user-attachments/assets/1d9cb5b2-5f66-4e5e-8f28-5dbfff66003d" />

ISAAC and PUMA achieve the **lowest energy per inference**, while digital accelerators provide **higher throughput** 

---

## 🚀 Applications

These accelerators enable:

- Smart cameras  
- Drones  
- Wearables  
- Industrial IoT  
- Edge anomaly detection  

All operating at **milliwatt-level power** 

---

## 🧾 Citation

Adinath UG Scholar
