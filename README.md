# 📡 Microstrip Patch Antenna Dimension Calculator

A professional web-based calculator for designing **Rectangular Inset-Fed Microstrip Patch Antennas**. The calculator computes the initial antenna dimensions using standard transmission-line equations and generates CST Studio Suite modeling coordinates, reducing manual calculations and improving design efficiency.

---

## ✨ Features

- Calculate initial dimensions for a Rectangular Inset-Fed Microstrip Patch Antenna
- Uses standard transmission-line equations
- Automatic 50 Ω feed width calculation using Hammerstad and Jensen equations
- Generates CST modeling coordinate formulas
- Professional engineering user interface
- Dark mode design
- Input validation
- Responsive layout
- Results displayed in millimeters (mm)
- Dimension table for quick reference
- CST Modeling Formula Reference
- Top-view antenna geometry visualization
- CSV and PDF export support (if enabled)

---

## 📥 Input Parameters

- Frequency (GHz)
- Dielectric Constant (εr)
- Substrate Thickness (ST) (mm)
- Copper Thickness (CT) (mm)

**Default Values**

- Frequency = 0 GHz
- Dielectric Constant = 0
- Substrate Thickness = 1.6 mm
- Copper Thickness = 0.035 mm

Feed impedance is fixed internally at **50 Ω**.

---

## 📤 Output Dimensions

The calculator generates the following dimensions:

- Ground Length (GL)
- Ground Width (GW)
- Substrate Length (SL)
- Substrate Width (SW)
- Patch Length (PL)
- Patch Width (PW)
- Feed Length (FL)
- Feed Width (FW)
- Inset Length (IL)
- Inset Width (IW)

All values are displayed in **millimeters (mm)**.

---

## 📐 CST Modeling Formula Reference

The calculator also generates coordinate formulas for direct use in CST Studio Suite.

### Ground

```
Xmin = 0
Xmax = GW

Ymin = 0
Ymax = GL

Zmin = -CT
Zmax = 0
```

### Substrate

```
Xmin = 0
Xmax = GW

Ymin = 0
Ymax = GL

Zmin = 0
Zmax = ST
```

### Patch

```
Xmin = (GW/2) - (PW/2)
Xmax = (GW/2) + (PW/2)

Ymin = FL
Ymax = FL + PL

Zmin = ST
Zmax = ST + CT
```

### Feed Line

```
Xmin = (GW/2) - (FW/2)
Xmax = (GW/2) + (FW/2)

Ymin = 0
Ymax = FL

Zmin = ST
Zmax = ST + CT
```

### Inset

```
Xmin = (GW/2) + (FW/2)
Xmax = (GW/2) + (FW/2) + IW

Ymin = FL
Ymax = FL + IL

Zmin = ST
Zmax = ST + CT
```

---

## 🛠 Technologies Used

- HTML5
- CSS3
- JavaScript

---

## 🎯 Purpose

This calculator was developed to simplify the preliminary design of rectangular inset-fed microstrip patch antennas. It minimizes manual calculations and provides accurate starting dimensions that can be directly used in CST Studio Suite for simulation and optimization.

---

## ⚠️ Note

The generated dimensions are analytical starting values and are approximately **90% accurate**. For optimum antenna performance, parameters such as **Patch Length (PL)** and **Ground Length (GL)** should be fine-tuned in CST Studio Suite to achieve the desired resonant frequency and improve antenna characteristics such as S11, VSWR, Gain, and Radiation Pattern.

---

## 👨‍💻 Author

**Dhanush S. Poojary**

Electronics and Communication Engineering (ECE)

NMAM Institute of Technology (NMAMIT), Nitte

---

## 📄 License

This project is intended for educational, research, and engineering purposes.
