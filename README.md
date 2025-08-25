# 🔒 AnomalyGuard — Self-/Unsupervised Anomaly Detection for IoT & Networks

**AnomalyGuard** is a research-friendly collection of Jupyter notebooks comparing **self‑supervised** and **unsupervised** anomaly detection methods across multiple traffic and sensor datasets (e.g., edge, MQTT, UNSW, WUSTL, X‑IIoT).
It provides clear, reproducible workflows for training, evaluation, and qualitative analysis.

> This repository is an independent, educational adaptation and rewrite. Markdown explanations and comments have been refreshed; minor structural edits improve readability and reproducibility.

---

## 📁 Repository Layout (updated)

```
AnomalyGuard/                       # Reworked SAFE notebooks
  ├─ AnomalyGuard_Detection.ipynb   # End‑to‑end detection workflow
  └─ AnomalyGuard_MAE.ipynb         # Masked autoencoder representation learning

SSL_Benchmarks/                     # Self‑supervised & deep one‑class baselines
  ├─ DeepOD_edge.ipynb
  ├─ DeepOD_mqtt.ipynb
  ├─ DeepOD_unsw.ipynb
  ├─ DeepOD_wustl.ipynb
  ├─ DeepOD_xiiot.ipynb
  ├─ MAE_xiiot.ipynb
  └─ VAE_xiiot.ipynb

Unsupervised_Benchmarks/            # Classical & modern unsupervised methods
  ├─ edge-unsupervised.ipynb
  ├─ mqtt-unsupervised.ipynb
  ├─ unsw-unsupervised.ipynb
  ├─ wustl-unsupervised.ipynb
  └─ x-iiot-unsupervised.ipynb

requirements.txt
README.md
.gitignore
```

---

## 🧭 What’s Inside

- **AnomalyGuard notebooks (reworked):**
  - `AnomalyGuard_Detection.ipynb` — complete pipeline, metrics and reporting
  - `AnomalyGuard_MAE.ipynb` — MAE pretext task for robust embeddings

- **Self‑Supervised baselines (`SSL_Benchmarks/`):**
  - Deep one‑class variants and generative approaches (DeepOD, MAE, VAE)

- **Unsupervised baselines (`Unsupervised_Benchmarks/`):**
  - Classical clustering / density / reconstruction methods per dataset

Each notebook begins with a **provenance header** and refreshed markdown to clarify intent and workflow.

---

## ⚙️ Environment & Setup

Create a fresh environment (Python 3.10+ recommended) and install requirements:
```bash
python -m venv .venv
source .venv/bin/activate            # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Minimal `requirements.txt` (extend as needed):
```txt
jupyter
numpy
pandas
scikit-learn
matplotlib
seaborn
torch
torchvision
tqdm
pyod
einops
```

> Some notebooks may require extra packages depending on your CUDA/CPU setup.

---

## ▶️ How to Run

1. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
2. Open a target notebook (e.g., `AnomalyGuard/AnomalyGuard_Detection.ipynb`).
3. Run cells top‑to‑bottom. Refer to the intro cell for configuration notes.

---

## 📊 Metrics & Reporting

- Common metrics (AUROC, F1, precision/recall) printed per run.
- Save tables/figures as CSV/PNG for downstream comparison and paper‑ready charts.

**Results template (example):**

| Dataset | Method   | AUROC | F1   | Notes |
|--------:|----------|------:|-----:|------|
| edge    | DeepOD   | 0.94  | 0.88 | default params |
| mqtt    | MAE      | 0.91  | 0.85 | lr=1e-4 |
| unsw    | VAE      | 0.89  | 0.83 | tuned epochs |

---

## 🗂 Datasets

Place datasets under a local `data/` folder or update paths inside notebooks to your environment.  
Please follow each dataset’s license/terms of use.

---

## 🔍 Provenance

This repository is an **independent adaptation** in which:
- Markdown cells and comments were rewritten in my own words.
- Minor structural edits and logging were added for clarity.
- Notebook names and folders were **renamed** to reflect the new project identity.

**Adaptation date:** 2025-08-25  
**Author:** Atharva Prakash Patil

---

## 📜 License & Citation

Choose a license appropriate to your use (e.g., MIT/Apache‑2.0) and cite any upstream datasets/papers you build upon.
