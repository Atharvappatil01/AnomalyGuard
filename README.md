# 🔒 AnomalyGuard: Self-/Unsupervised Anomaly Detection for IoT & Networks

**AnomalyGuard** is a research-friendly collection of Jupyter notebooks that compare **self-supervised** and **unsupervised** anomaly detection baselines across multiple datasets (edge, MQTT, UNSW, WUSTL, X-IIoT, etc.).  
It provides clear, reproducible workflows for training, evaluation, and qualitative analysis.

> This repository is an independent, educational rework and extension. All wording, structure, and explanations have been rewritten for clarity and originality.

---

## 🧭 What’s Inside

- **SAFE Notebooks (Reworked)**  
  - `SAFE_Detection.ipynb`: end-to-end detection workflow, metrics, and reporting  
  - `SAFE_MAE.ipynb`: masked autoencoding approach for representation learning

- **Self-Supervised Baselines (SSL)**  
  - `DeepOD_*.ipynb`: deep one-class variants over multiple datasets  
  - `MAE_xiiot.ipynb`, `VAE_xiiot.ipynb`: generative pretext tasks for robust embeddings

- **Unsupervised Baselines**  
  - `*-unsupervised.ipynb`: classic and modern unsupervised methods (per dataset)

Each notebook now includes a short **provenance header** and **refreshed markdown** to improve readability and reduce duplication from prior art.

---

## 📦 Environment & Setup

Create a fresh Python environment (3.10+ recommended) and install typical packages:
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

You can start with a minimal `requirements.txt` (tweak as needed):
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
```
> Some notebooks may require additional packages (e.g., `pyod`, `einops`); install them as prompted.

---

## 📁 Suggested Structure

```
AnomalyGuard/
├─ notebooks/
│  ├─ SAFE_Detection.ipynb
│  ├─ SAFE_MAE.ipynb
│  ├─ SSL-baselines/
│  │  ├─ DeepOD_edge.ipynb
│  │  ├─ DeepOD_mqtt.ipynb
│  │  └─ ...
│  └─ unsupervised/
│     ├─ edge-unsupervised.ipynb
│     ├─ mqtt-unsupervised.ipynb
│     └─ ...
├─ data/                 # (place datasets here or mount paths)
├─ requirements.txt
└─ README.md
```

> This repository keeps the original layout for convenience, but feel free to reorganize using the structure above.

---

## ▶️ How to Run

1. Launch Jupyter:
```bash
jupyter notebook
```
2. Open the notebook for your target dataset (e.g., `SSL-baselines/DeepOD_edge.ipynb`).  
3. Run cells top-to-bottom. See the introduction cell for configuration tips.

---

## 📊 Results & Reporting

Every notebook prints common metrics (e.g., AUROC, F1, precision/recall) and includes plots to compare models.  
You’re encouraged to export results (CSV) and figures (PNG/PDF) for downstream analysis and paper-ready charts.

---

## 🔍 Provenance

This repository is an **independent adaptation** and **original rewrite** of educational materials in this area.  
- Introductory markdown, code comments, variable naming, and logging have been rewritten for clarity.  
- A **provenance header** has been added to each notebook indicating this adaptation and date.

---

## 📜 License & Citation

If you build on this work, please cite this repository and any upstream datasets or papers you use.

**Author:** Atharva Prakash Patil  
**Year:** 2025
