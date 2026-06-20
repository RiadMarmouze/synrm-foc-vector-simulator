# SynRM FOC Vector & Torque Simulator

> Interactive visualization tool for Field-Oriented Control (FOC) of Synchronous Reluctance Motors (SynRM) with MTPA optimization

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with HTML](https://img.shields.io/badge/Made%20with-HTML5-E34F26)](https://html.spec.whatwg.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.0-38B2AC)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Mathematical Foundation](#mathematical-foundation)
- [Live Demo](#live-demo)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [Technical Architecture](#technical-architecture)
- [Thesis Context](#thesis-context)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Overview

This interactive web application serves as a pedagogical tool for understanding **Field-Oriented Control (FOC)** in **Synchronous Reluctance Motors (SynRM)**. It visualizes the relationship between current vectors, electromagnetic torque, and efficiency optimization through **Maximum Torque per Ampere (MTPA)** control.

Built as part of a Master's thesis in Electromechanical Engineering, the simulator provides real-time feedback on how adjustments to direct and quadrature currents affect motor performance, making abstract control theory tangible and intuitive.

---

## ✨ Key Features

### 🎛️ Interactive Control Panel
- **Real-time slider controls** for `i_d` and `i_q` currents (0-30A range)
- **Adjustable machine parameters**: Pole pairs, `L_d`, and `L_q` inductances
- **One-click presets**: MTPA (45°), High Flux, and Dynamic Load configurations

### 📊 Real-time Metrics Display
- **Electromagnetic torque** (Tₑ) in N·m
- **Stator current magnitude** (Iₛ) in Amperes RMS
- **Current vector angle** (β) relative to d-axis
- **Saliency ratio** (ξ = L_d/L_q)

### 🎨 Interactive Vector Visualization
- 2D vector diagram showing:
  - d-axis current component (i_d)
  - q-axis current component (i_q)
  - Resultant stator current vector (Iₛ)
  - Torque hyperbola curve
  - Optimal MTPA trajectory (45° line)
- **Dynamic arrowheads** and **scaling** for clear visualization
- **High-DPI canvas** support for crisp rendering

### ⚡ Intelligent Feedback
- **MTPA status alerts**: Real-time assessment of efficiency
- **Visual cues**: Color-coded warnings when deviating from optimal operation
- **Educational tooltips**: Explanatory labels throughout the interface

---

## 📐 Mathematical Foundation

The simulator is built on the fundamental torque equation for SynRM:

$$T_e = \frac{3}{2} \cdot p \cdot (L_d - L_q) \cdot i_d \cdot i_q$$

Where:
- $T_e$ = Electromagnetic torque (N·m)
- $p$ = Number of pole pairs
- $L_d$ = Direct-axis inductance (H)
- $L_q$ = Quadrature-axis inductance (H)
- $i_d$ = Direct-axis current (A)
- $i_q$ = Quadrature-axis current (A)

### MTPA Principle
Maximum Torque per Ampere is achieved when the current vector angle $\beta = 45^\circ$, meaning:

$$i_d = i_q$$

This configuration maximizes torque for a given stator current magnitude, improving motor efficiency.

### Current Vector Angle
$$\beta = \tan^{-1}\left(\frac{i_q}{i_d}\right)$$

### Stator Current Magnitude
$$I_s = \sqrt{i_d^2 + i_q^2}$$

### Saliency Ratio
$$\xi = \frac{L_d}{L_q}$$

Higher saliency ratios indicate better torque production capability in SynRM.

---

## 🚀 Live Demo

**[View Live Simulator](https://your-username.github.io/synrm-foc-vector-simulator)**

*Replace the URL with your actual deployment link*

---

## 💻 Installation

### Option 1: Direct Download
```bash
# Clone the repository
git clone https://github.com/your-username/synrm-foc-vector-simulator.git

# Navigate to the project directory
cd synrm-foc-vector-simulator

# Open index.html in your browser
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
