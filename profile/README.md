<div align="center">

<!-- Autoplay, looped, muted demo video -->
<img src="https://github.com/OpenCivil-Project/.github/raw/main/profile/Home1.gif" width="100%"/>
<br/>

# OpenCivil Project

### *A Transparent 3D Structural Analysis Engine for Learning Finite Element Methods*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/OpenCivil-Project/OpenCivil/blob/main/LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-blue.svg)](https://github.com/OpenCivil-Project/OpenCivil/releases)
[![Version](https://img.shields.io/badge/version-v0.7%20Pre--Alpha-orange.svg)](https://github.com/OpenCivil-Project/OpenCivil/releases/latest)
[![pip](https://img.shields.io/badge/pip%20install-opencivil-blue?logo=python)](https://pypi.org/project/opencivil/)
[![METU](https://img.shields.io/badge/METU-Civil%20Engineering-red.svg)](https://ce.metu.edu.tr)
[![Website](https://img.shields.io/badge/Website-opencivil--project.github.io-brightgreen.svg)](https://opencivil-project.github.io/)

</div>

---

## 👋 Welcome to the OpenCivil Project

**OpenCivil** bridges the gap between simplified 2D textbook problems and complex commercial "black box" software. Instead of hiding the math, OpenCivil shows you every matrix, every transformation, every step — while delivering results validated to **6–7 decimal place accuracy** against industry-standard commercial FEM tools like SAP2000.

> *"Not just a solver — a window into the mathematics of structural engineering."*

---

## 📦 Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [**OpenCivil**](https://github.com/OpenCivil-Project/OpenCivil) | Core 3D FEA desktop application (GUI + all solvers) | 🟠 Pre-Alpha |
| [**opencivil** (PyPI)](https://pypi.org/project/opencivil/) | Standalone Python API for headless / batch analysis | 🟠 Pre-Alpha |

---

## ✨ What's Inside

### 🔬 "Glass Box" FEM Solver
Full visibility into 12×12 stiffness matrices, transformation matrices, and fixed-end force vectors — no black box, ever. Every matrix is inspectable and exportable to JSON, MATLAB, or Python.

### 🧱 Dual Element Libraries

**3D Frame / Beam Elements**
- Timoshenko beam theory with shear deformation
- Rigid end offsets · Cardinal insertion points (11 positions)
- Member releases via static condensation · Eccentric connections
- True-to-scale 3D extrusions (I-beams, pipes, tubes, rectangular, trapezoidal)

**Tet10 Quadratic Solid Elements** *(New)*
- 10-node quadratic tetrahedra — eliminates shear locking in bending
- Full 3D stress field recovery: σxx, σyy, σzz, τxy, τyz, τxz
- Von Mises stress contour visualization (blue → cyan → green → yellow → red)
- Automatic Gmsh meshing of frame cross-sections into solid Tet10 meshes
- Rigid link MPCs coupling solid nodes to frame beam endpoints
- `pip install opencivil` API supports solid analysis in headless batch mode

### 📊 Analysis Suite

| Analysis Type | Description |
|---------------|-------------|
| **Linear Static** | Full 3D frame · Distributed, point & nodal loads · Self-weight · Load combinations |
| **Modal (Eigenvalue)** | Shift-invert solver · Mode shape animation · Mass participation factors |
| **Response Spectrum** | TBDY 2018 compliant (CQC/SRSS) · Site classes ZA–ZE · Validated |
| **Linear Time History** | Newmark-β Modal Superposition · Real-time 3D earthquake animation |
| **Solid FEM** | Tet10 stress analysis · Von Mises contours · Coupled frame–solid models |

### 🖥️ Dual Interface: GUI + Terminal

OpenCivil ships with two ways to work — use them together or separately:

**Visual GUI** — PyQt6 / OpenGL desktop application  
Click-to-model, animated deformed shapes, 3D stress contours, matrix inspector, free body diagrams.

**Embedded Terminal Panel** — VSCode-style bottom panel inside the GUI  
Type commands while your model is live on screen. Every CLI command instantly updates the canvas. Full command history (↑/↓), stdout/stderr capture, and `clear` / `undo` / `redo` support.

```
OC> node 0 0 0
OC> node 5 0 0
OC> mat Steel 2.1e8 0.3 7850 Steel
OC> sec S1 Steel rect 0.3 0.5
OC> frame 1 2 S1
OC> support 1 1 1 1 1 1 1
OC> solve
```

**Standalone Terminal** — launch `launch_terminal.py` or `python cli.py` for a pure command-line REPL, independent of the GUI.

**Python API** — install separately via pip for scripted / headless batch analysis:
```bash
pip install opencivil
```

---

## ✅ Validated Accuracy

| Analysis Type | Result |
|---------------|--------|
| Linear Static — displacements, reactions, forces | ✅ 6+ decimal agreement vs SAP2000 |
| Modal Analysis — periods, mode shapes, mass participation | ✅ 7+ decimal agreement |
| Response Spectrum — spectral accelerations, base shear (TBDY 2018) | ✅ 6+ decimal agreement |

---

## 🎯 Who Is This For?

**Students** — Inspect the math powering commercial software. Verify hand calculations against a proven-correct solver. Export stiffness matrices to MATLAB or Python for homework.

**Educators** — Use real 3D problems instead of simplified 2D examples. Use OpenCivil as a validated teaching companion to SAP2000 or ETABS. Completely free.

**Researchers** — Export human-readable JSON project files. Use the `pip install opencivil` Python API for batch analysis pipelines.

---

## 🚀 Getting Started

**Desktop Application (Windows Installer):**
```bash
# Download from Releases and run the installer — no Python required
# https://github.com/OpenCivil-Project/OpenCivil/releases/latest
```

**Run from Source:**
```bash
git clone https://github.com/OpenCivil-Project/OpenCivil.git
cd OpenCivil
pip install -r requirements.txt
python app/main.py
```

**Python API (headless / batch):**
```bash
pip install opencivil
```

**Standalone Terminal:**
```bash
python cli.py               # blank model
python cli.py model.mf      # load existing project
```

---

## 🗺️ Roadmap

- [x] Linear Static Analysis
- [x] Modal Analysis (Eigenvalue)
- [x] Response Spectrum Analysis (TBDY 2018)
- [x] Linear Time History Analysis (Newmark-β)
- [x] Tet10 Quadratic Solid FEM with Von Mises contours
- [x] Embedded GUI Terminal Panel
- [x] Standalone CLI Terminal
- [x] Python API (`pip install opencivil`)
- [ ] Nonlinear Analysis (P-Delta)
- [ ] Steel connection design checks
- [ ] Concrete section design (ACI / Eurocode)
- [ ] DXF import / export
- [ ] Extended validation documentation

---

## 👨‍💻 About the Developer

**Shaikh Ahmed Azad** — 4th year Civil Engineering student at [Middle East Technical University (METU)](https://metu.edu.tr), Ankara, Turkey.

Specializing in computational structural engineering and earthquake engineering. Published researcher (INTER 2026, Norway) and national finalist in the DASK Earthquake Resistant Building Design Competition (2026).

📧 [ahmed.azad@metu.edu.tr](mailto:ahmed.azad@metu.edu.tr) · 🌐 [opencivil-project.github.io](https://opencivil-project.github.io/) · 💻 [GitHub](https://github.com/ShaikhAhmedAzad)

---

## 🤝 Contributing & Feedback

The project is in active **Pre-Alpha** development. Code contributions are not open yet, but your feedback shapes the roadmap:

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
  version = {0.7},
  url     = {https://github.com/OpenCivil-Project/OpenCivil}
}
```

---

<div align="center">

**⭐ If OpenCivil helped you understand FEM, give it a star — it means a lot!**

[📥 Download](https://github.com/OpenCivil-Project/OpenCivil/releases/latest) · [🐛 Issues](https://github.com/OpenCivil-Project/OpenCivil/issues) · [🌐 Website](https://opencivil-project.github.io/) · [🐍 PyPI](https://pypi.org/project/opencivil/)

<br/>

*MIT Licensed · Built with ❤️ at METU, Ankara*

</div>
