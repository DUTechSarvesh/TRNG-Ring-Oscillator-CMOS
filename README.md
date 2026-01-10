# 🔐 True Random Number Generator (TRNG) Using Ring Oscillator

[![GitHub](https://img.shields.io/badge/GitHub-DUTechSarvesh-181717?style=flat&logo=github)](https://github.com/DUTechSarvesh)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-sarvesh--kumar--du-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/sarvesh-kumar-du)  
[![Language](https://img.shields.io/badge/Language-VHDL%2FC%2B%2B-blue?style=flat)]()  
[![Simulation](https://img.shields.io/badge/Simulation-Passed-brightgreen?style=flat)]()  
[![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)](LICENSE)

---

## ✨ Abstract
True Random Number Generators (**TRNGs**) are crucial for cryptography & hardware security.  
This project presents a **Ring Oscillator–based TRNG** implemented in **CMOS technology**.  

✅ **Randomness Source:** Timing jitter & metastability  
✅ **Digital Conversion:** D flip-flop sampling  
✅ **Output:** High-quality digital bitstream  

---

## 1️⃣ Introduction
Random numbers are essential for:  
- 🔒 Secure communication  
- 🗝️ Cryptographic key generation  
- 🖥️ Hardware security  

**TRNGs vs PRNGs:**  
- TRNGs: Use **physical phenomena**, truly unpredictable  
- PRNGs: Algorithmic, **can be predicted**  

💡 **Ring Oscillator TRNGs:**  
- Simple & CMOS-compatible  
- Exploit **thermal noise, device mismatch, power supply variations**  

---

## 2️⃣ Motivation
Software random generators can be **predicted or attacked**.  
Hardware TRNGs use **physical entropy**, making them **secure & reliable**.  

🎯 **Goal:** Design a compact, CMOS-based TRNG for **VLSI/SoC integration**  

---

## 3️⃣ Working Principle
- 🔁 **Ring Oscillator:** Generates oscillations (odd number of inverters)  
- ⏱️ **Timing jitter & metastability:** Introduces randomness  
- 🖲️ **D Flip-Flop Sampling:** Converts analog uncertainty → digital bits  

📌 **Diagram Placeholder:**  
![Ring Oscillator Schematic](Schematic/ring_oscillator_schematic.png)  

---

## 4️⃣ Architecture
| Block | Function |
|-------|---------|
| 🔁 Ring Oscillator | Entropy source |
| 🖲️ Sampling Circuit (D Flip-Flop) | Generates digital bits |
| ⏰ Clock Source | Reference for sampling |
| 💾 Output Register | Stores generated random bits |

📌 **Architecture Diagram Placeholder:**  
![Architecture](Schematic/trng_architecture.png)  

---

## 5️⃣ Design Methodology
```text
1. Design CMOS inverters for ring oscillator
2. Build multi-stage ring oscillator
3. Implement D Flip-Flop sampling
4. Perform transient simulations
5. Observe jitter-driven randomness
6. Verify correctness
