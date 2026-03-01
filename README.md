# ⚡ Low-Power PTL Full Adder Design (16T vs 18T)

## 📌 Project Overview

This project implements and compares two low-power Full Adder designs using **Pass-Transistor Logic (PTL)**:

- 🔹 16-Transistor (16T) Full Adder  
- 🔹 18-Transistor (18T) Full Adder  

The work is based on the IEEE paper:

**“Low-Power Pass-Transistor Logic-Based Full Ader”**  
IEEE Document ID: 9875091  

All circuits were designed and simulated using **LTspice with 22nm technology models**.

The goal is to analyze:

- ⚡ Power Consumption  
- ⏱ Propagation Delay  
- 📊 Power-Delay Product (PDP)  
- 🔁 Design Trade-offs  

---

## 🧠 Why Pass-Transistor Logic (PTL)?

Compared to conventional CMOS logic:

### ✅ PTL Advantages
- Lower transistor count  
- Reduced power consumption  
- Shorter signal paths  
- Compact design  

### ⚠ PTL Limitations
- Threshold voltage loss  
- Non full-swing outputs  
- Weaker driving strength  
- More sensitive to glitches  

This project studies how different PTL structures handle these trade-offs.

---

## 🏗 Implemented Designs

### 🔹 16T Full Adder
- PTL-based design  
- Uses inverter for signal restoration  
- Higher parasitic loading at SUM node  
- Slightly higher power consumption  

### 🔹 18T Full Adder
- Parallel XOR-based structure  
- Reduced SUM critical path  
- Improved delay performance  
- Slight increase in carry delay  

---

## 📊 Simulation Results (22nm Model)

| Parameter | 16T Adder | 18T Adder |
|-----------|-----------|-----------|
| Avg Power | 3.79 × 10⁻⁹ W | 3.56 × 10⁻⁹ W |
| Sum Delay | 2.00 × 10⁻⁸ s | 4.94 × 10⁻⁹ s |
| Carry Delay | 2.08 × 10⁻⁸ s | 2.50 × 10⁻⁸ s |
| PDP (Sum) | 1.76 × 10⁻¹⁴ | 1.76 × 10⁻¹⁴ |

---

## 🔎 Key Observations

- 🔋 18T consumes ~6% less power  
- 🚀 18T improves SUM delay by ~4×  
- Carry delay slightly increases in 18T  
- Removing inverter reduces parasitic capacitance  
- Practical results differ slightly from IEEE claims due to 22nm model usage  

---

## 🛠 Tools & Technologies Used

- LTspice  
- 22nm MOSFET Model  
- Pass-Transistor Logic (PTL)  
- DCMOS Concepts  
- Power & Delay Analysis  

---

## 📁 Repository Contents

- `/circuits` → LTspice simulation files (.asc)  
- `/presentation` → Project presentation slides  
- `/results` → Comparison data and analysis  

---

## 🎯 Conclusion

The 18T PTL Full Adder provides better SUM delay performance and slightly lower power consumption compared to the 16T design. However, design trade-offs exist in carry delay and driving strength.

This project demonstrates practical VLSI design trade-offs in low-power digital circuits.

---

## 👨‍💻 Team Members

- Harsh Modi  
- Kunal Narang  
- Yash Khetan  
- Akshat Tyagi  
- Swayam Kotecha  
- Sarthak Raj  

---

⭐ If you found this project helpful, feel free to star the repository.
