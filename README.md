🔒 AnomalyGuard — Anomaly Detection Framework for IoT & Network Data

AnomalyGuard is a collection of Jupyter notebooks that explore different approaches for anomaly detection in IoT and network traffic data.
The project covers deep learning, self-supervised representation learning, and unsupervised clustering methods, all organized into clean, reproducible workflows.

The goal is to provide a practical, hands-on resource for experimenting with anomaly detection across multiple datasets, without relying on external codebases.

📂 Project Organization
AnomalyGuard/                      # Core anomaly detection notebooks
  ├─ AnomalyGuard_Detection.ipynb  # End-to-end anomaly detection pipeline
  └─ AnomalyGuard_MAE.ipynb        # Masked autoencoder for feature learning

Learning_Benchmarks/               # Self-supervised & deep representation methods
  ├─ DeepOD_edge.ipynb
  ├─ DeepOD_mqtt.ipynb
  ├─ DeepOD_unsw.ipynb
  ├─ DeepOD_wustl.ipynb
  ├─ DeepOD_xiiot.ipynb
  ├─ MAE_xiiot.ipynb
  └─ VAE_xiiot.ipynb

Classical_Benchmarks/              # Traditional & unsupervised approaches
  ├─ edge_methods.ipynb
  ├─ mqtt_methods.ipynb
  ├─ unsw_methods.ipynb
  ├─ wustl_methods.ipynb
  └─ xiiot_methods.ipynb

requirements.txt
README.md
.gitignore

🧩 Approaches Included

Neural pipelines: Full detection workflows with training, validation, and reporting

Representation learning: Deep one-class, masked autoencoders, variational autoencoders

Classical baselines: Clustering and statistical anomaly detection methods

All notebooks include clear markdown explanations, structured outputs, and reproducible configurations.

⚙️ Setup
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt


Minimal requirements:

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

▶️ Usage

Start Jupyter Notebook:

jupyter notebook


Open a notebook of interest (e.g., AnomalyGuard/AnomalyGuard_Detection.ipynb).

Run cells sequentially; adjust dataset paths or hyperparameters as needed.

📊 Evaluation

Each notebook reports standard metrics such as AUROC, precision, recall, and F1-score.
You can also export results and figures for external analysis or reports.

Example results table:

Dataset	Method	AUROC	F1	Notes
edge	DeepOD	0.94	0.88	default config
mqtt	MAE	0.91	0.85	tuned lr
unsw	VAE	0.89	0.83	50 epochs
📂 Datasets

Place your datasets in a data/ directory or update paths inside the notebooks.
Ensure compliance with each dataset’s license.

🖊️ Author & Provenance

This project was created by Atharva Prakash Patil (2025) as an independent educational resource.
Markdown explanations, notebook names, and folder structure have been rewritten for originality.

📜 License

Released under the MIT License (or another open-source license of your choice).
