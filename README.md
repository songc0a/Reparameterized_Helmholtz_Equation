# PINN-based Seismic Wavefield Simulation for Helmholtz Equation Parameterized by Amplitude and Unwrapped Phase

This repository contains the partial source code and execution results for the paper **"PINN-based Seismic Wavefield Simulation for Helmholtz Equation Parameterized by Amplitude and Unwrapped Phase"**. The paper is currently under review in the journal *Geophysics*.

## 💡 Methodology Highlights

When solving the frequency-domain Helmholtz equation, conventional Physics-Informed Neural Networks (PINNs) struggle to fit the severe spatial oscillations of complex-valued wavefields due to the spectral bias of neural networks.

This project proposes a novel **reparameterized scattered Helmholtz equation**. By decoupling the wavefield into **Amplitude** and **Unwrapped Phase**, we transform the task of fitting high-frequency oscillations into a smooth function fitting task, at which neural networks excel. Experiments demonstrate that this method achieves a significant improvement in computational accuracy for both 2D and 3D complex models, even when using simple fully connected networks.

---

## 🔒 Repository Status: Phased Release

To protect core intellectual property prior to formal publication, this repository is currently in a **phased release** state.

**✅ Currently Available (Review Phase):**
* **`architecture/`**: The PINN backbone network architecture and activation function configurations used in the paper.
* **`results/`**: The output results of the novel loss function and the conventional loss function.

**🚀 Upcoming (To be open-sourced immediately upon official publication):**
* **Core Loss Function**: The novel loss function based on the  **Helmholtz Equation Parameterized by Amplitude and Unwrapped Phase**.

---

## ⚙️ Environment Setup

The code is implemented in Python using TensorFlow 2.4.0. To ensure the reproducibility of the experimental results, the code execution is restricted to a deterministic computational mode.

**Dependencies:**
* Python 3.7.16
* TensorFlow 2.4.0
* cuda 10.1
* NumPy 1.21.5

**Quick Installation:**
```bash
pip install tensorflow==2.4.0 numpy==1.21.5
