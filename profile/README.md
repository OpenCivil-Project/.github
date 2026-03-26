<div align="center">

<img src="https://github.com/OpenCivil-Project/OpenCivil/raw/main/images/hero-main.png" alt="OpenCivil Banner" width="100%"/>

<br/>

# 🏗️ OpenCivil Project

### *A Transparent 3D Structural Analysis Engine for Learning Finite Element Methods*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/OpenCivil-Project/OpenCivil/blob/main/LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-blue.svg)](https://github.com/OpenCivil-Project/OpenCivil/releases)
[![Version](https://img.shields.io/badge/version-v0.655%20Pre--Alpha-orange.svg)](https://github.com/OpenCivil-Project/OpenCivil/releases/latest)
[![METU](https://img.shields.io/badge/METU-Civil%20Engineering-red.svg)](https://ce.metu.edu.tr)
[![Website](https://img.shields.io/badge/Website-opencivil--project.github.io-green.svg)](https://opencivil-project.github.io/)

</div>

---

## 👋 Welcome to the OpenCivil Project

**OpenCivil** bridges the gap between simplified 2D textbook problems and complex commercial "black box" software. Instead of hiding the math, OpenCivil shows you every matrix, every transformation, every step — while delivering results validated to **6–7 decimal place accuracy** against industry-standard commercial FEM tools.

> *"Not just a solver — a window into the mathematics of structural engineering."*

---

## 🔬 What We're Building

| Repository | Description | Status |
|------------|-------------|--------|
| [**OpenCivil**](https://github.com/OpenCivil-Project/OpenCivil) | Core 3D FEA desktop application | 🟠 Pre-Alpha |

### Core Capabilities

**🧮 "Glass Box" FEM Solver**
Full visibility into 12×12 stiffness matrices, transformation matrices, and fixed-end force vectors — no black box, ever.

**📐 Advanced Structural Modeling**
3D Timoshenko beam theory · Rigid end offsets · Cardinal insertion points · Member releases via static condensation · Eccentric connections

**📊 Multiple Analysis Types**
- Linear Static Analysis (3D frame, load combinations, reactions)
- Modal Analysis (eigenvalue solver, mode shape animation, mass participation)
- Response Spectrum Analysis (TBDY 2018 compliant, CQC/SRSS combination)
- Linear Time History Analysis (Newmark-β, real-time earthquake animation)

**🇹🇷 Turkish Seismic Code (TBDY 2018)**
Built-in spectrum generator, site class effects (ZA–ZE), validated against official TBDY 2018 examples.

---

## ✅ Validated Accuracy

OpenCivil results are independently verified against commercial FEM software:

| Analysis Type | Accuracy |
|---------------|----------|
| Linear Static — displacements, reactions, forces | ✅ 6+ decimal agreement |
| Modal Analysis — periods, mode shapes, mass participation | ✅ 7+ decimal agreement |
| Response Spectrum — spectral accelerations, base shear | ✅ 6+ decimal agreement |

---

## 🎯 Who Is This For?

**Students** — Inspect the math powering commercial software. Verify hand calculations against a proven-correct solver. Export matrices to MATLAB or Python for homework.

**Educators** — Replace simplified 2D examples with real 3D problems. Use OpenCivil as a teaching companion to SAP2000 or ETABS.

**Researchers** — Export human-readable JSON project files. Use the `pip install opencivil` Python API for headless batch analysis.

---

## 🚀 Getting Started

```bash
# Install via Windows Installer (recommended)
# Download from: https://github.com/OpenCivil-Project/OpenCivil/releases/latest

# Or run from source
git clone https://github.com/OpenCivil-Project/OpenCivil.git
cd OpenCivil
pip install -r requirements.txt
python app/main.py
```

Or install the Python API for scripting:
```bash
pip install opencivil
```

---

## 🗺️ Roadmap

- [x] Linear Static Analysis
- [x] Modal Analysis
- [x] Response Spectrum Analysis (TBDY 2018)
- [x] Linear Time History Analysis
- [x] Python API (`pip install opencivil`)
- [ ] Nonlinear Analysis (P-Delta)
- [ ] Steel connection design checks
- [ ] Concrete section design (ACI / Eurocode)
- [ ] DXF import/export
- [ ] Extended validation documentation

---

## 👨‍💻 About the Developer

**Shaikh Ahmed Azad** — Civil Engineering Student at [Middle East Technical University (METU)](https://metu.edu.tr), Ankara, Turkey.

Specializing in computational structural engineering and earthquake engineering. Published researcher (INTER 2026, Norway) and national finalist in DASK Earthquake Resistant Building Design Competition (2026).

📧 [ahmed.azad@metu.edu.tr](mailto:ahmed.azad@metu.edu.tr) · 🌐 [opencivil-project.github.io](https://opencivil-project.github.io/) · 💻 [GitHub](https://github.com/ShaikhAhmedAzad)

---

## 🤝 Contributing & Feedback

The project is in active **Pre-Alpha** development. Code contributions are not open yet, but your feedback is invaluable:

- 🐛 [Report a Bug](https://github.com/OpenCivil-Project/OpenCivil/issues)
- 💡 [Request a Feature](https://github.com/OpenCivil-Project/OpenCivil/discussions)
- ⭐ Star the repo if OpenCivil helped you learn FEM!

---

## 📄 Citation

```bibtex
@software{azad2025opencivil,
  author  = {Azad, Shaikh Ahmed},
  title   = {OpenCivil: A Transparent 3D Structural Analysis Engine for Learning Finite Element Methods},
  year    = {2025},
  version = {0.655},
  url     = {https://github.com/OpenCivil-Project/OpenCivil}
}
```

---

<div align="center">

**⭐ If OpenCivil helped you understand FEM, give it a star — it means a lot!**

[📥 Download](https://github.com/OpenCivil-Project/OpenCivil/releases/latest) · [🐛 Issues](https://github.com/OpenCivil-Project/OpenCivil/issues) · [🌐 Website](https://opencivil-project.github.io/)

<br/>

*MIT Licensed · Built with ❤️ at METU, Ankara*

</div>
