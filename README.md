# QCG Open Project 2025: Quantum Machine Learning Classifier

## 📋 Project Overview
This project is a part of the **QCG Open Projects 2025**. It demonstrates the implementation of a **Variational Quantum Classifier (VQC)** to solve binary classification problems. By leveraging quantum feature maps and entangling layers, the model learns to classify complex data by mapping it into a high-dimensional Hilbert space.

The repository includes implementations using standard healthcare data (Diabetes dataset) to showcase the practical utility of Hybrid Quantum-Classical Algorithms.

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `qml.ipynb` | The core notebook containing the VQC architecture, circuit training, and initial results. |
| `qml_newdataset.ipynb` | Extension notebook testing the model robustness on a secondary dataset. |
| `diabetes.csv` | Primary dataset containing diagnostic features for classification. |
| `dataset.csv` | Supplemental dataset used for benchmarking and validation. |

---

## 🧠 Technical Workflow



### 1. Data Pre-processing
Classical data from `diabetes.csv` is normalized using **Min-Max Scaling** to ensure feature values are compatible with quantum gate rotation ranges ($[0, \pi]$ or $[0, 2\pi]$).

### 2. Quantum Feature Mapping
We utilize **Angle Encoding** or **ZZFeatureMap** to transform classical vectors into quantum states $|\psi\rangle$. This step is crucial for capturing non-linear relationships that are difficult for classical kernels to identify.

### 3. Variational Circuit (Ansatz)
The trainable part of the circuit consists of:
* **Rotation Layers:** Parameterized $R_y$ and $R_z$ gates.
* **Entanglement Layers:** CNOT gates to create quantum correlations between features.

### 4. Optimization
A classical optimizer (e.g., **COBYLA** or **Adam**)  (COBYLA) in this case is used to iteratively update the circuit parameters by minimizing the Cross-Entropy loss calculated from quantum measurements.

---

## 🚀 Getting Started

### Prerequisites
* Python 3.9+
* Jupyter Notebook or VS Code

### Installation
1. Clone this repository:
   ```bash
   git clone [https://github.com/Rasp05-ops/qcg_project.git](https://github.com/Rasp05-ops/qcg_project.git)
   cd qcg_project
