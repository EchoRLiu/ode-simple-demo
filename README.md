# Interactive Tutorial: Parameter Estimation for ODE Models

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

An interactive Jupyter notebook tutorial for learning parameter estimation in ordinary differential equation (ODE) models using pypesto, AMICI, and PEtab.

## 📚 Overview

This tutorial teaches you how to:
- Extract quantitative parameters (e.g., mRNA half-life) from noisy experimental data
- Build and fit mechanistic ODE models to time-series measurements
- Use modern tools (pypesto, AMICI, PEtab) for parameter inference
- Interpret results biologically and validate model fits

**Case Study:** Estimating mRNA degradation rates from single-cell fluorescence measurements after mRNA transfection.

**Level:** Intermediate (familiarity with Python and basic ODEs helpful)

---

## 🎯 Learning Objectives

By the end of this tutorial, you will:

1. ✅ Understand why mathematical modeling is necessary for biological data analysis
2. ✅ Know how to formulate an ODE model for gene expression dynamics
3. ✅ Be able to use the pypesto + AMICI + PEtab pipeline for parameter estimation
4. ✅ Interpret fitted parameters biologically (e.g., calculate half-lives)
5. ✅ Validate model quality through residual analysis
6. ✅ Know when to extend to hybrid approaches (Universal ODEs, Neural ODEs)

---

## 📊 Dataset

This tutorial uses single-cell fluorescence microscopy data from:

> **Fröhlich, F., Reiser, A., Fink, L. et al.** Multi-experiment nonlinear mixed effect modeling of single-cell translation kinetics after transfection. *npj Syst Biol Appl* **4**, 42 (2018). https://doi.org/10.1038/s41540-018-0079-7

**Data description:**
- **System:** mRNA → GFP translation in mammalian cells (HuH7)
- **Protein:** eGFP (stable fluorescent protein)
- **Measurement:** Time-lapse fluorescence microscopy (~500 single cells tracked for 30 hours)
- **Technology:** Micropatterned protein arrays for standardized single-cell environments
- **Original data repository:** https://doi.org/10.5281/zenodo.1228898

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- C++ compiler (for AMICI compilation)
  - **macOS:** Xcode Command Line Tools (`xcode-select --install`)
  - **Linux:** `build-essential` package
  - **Windows:** Visual Studio Build Tools

### Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/echorliu/ode-simple-demo.git
   cd ode-simple-demo
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv tutorial-env
   source tutorial-env/bin/activate  # On Windows: tutorial-env\Scripts\activate
   ```

3. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

   **Key packages:**
   - `pypesto` - Parameter estimation toolbox
   - `amici` - Fast ODE simulation (compiled C++)
   - `petab` - Standardized parameter estimation format
   - `pandas`, `numpy`, `scipy` - Data manipulation
   - `matplotlib` - Visualization

4. **Accept Xcode license (macOS only):**
   ```bash
   sudo xcodebuild -license accept
   ```

5. **Launch Jupyter:**
   ```bash
   jupyter notebook pypesto_tutorial_interactive.ipynb
   ```

## 🎓 Exercises

The tutorial includes **5 interactive exercises** with progressively increasing difficulty:

| Exercise | Topic | Difficulty | Learning Goal |
|----------|-------|------------|---------------|
| 1 | Half-life calculation | ⭐ Easy | Understand parameter-to-phenotype mapping |
| 2 | Data interpretation | ⭐ Easy | Recognize biological time delays |
| 3 | Parameter bounds | ⭐⭐ Medium | Understand optimization search space |
| 4 | Biological prediction | ⭐⭐ Medium | Apply estimated parameters |
| 5 | Model validation | ⭐⭐⭐ Hard | Assess model quality via residuals |
| Challenge | Hypothesis testing | ⭐⭐⭐ Hard | Modify and re-fit model |

Each exercise includes:
- Clear question or task
- Code cell to complete
- Hints (where helpful)
- Hidden answers (click to reveal)
- Biological interpretation