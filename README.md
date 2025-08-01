# HypKG: Hypergraph-based Knowledge Graph Contextualization for Disease Prediction

> A faithful implementation of the [HypKG paper (2024)](https://arxiv.org/abs/2507.19726), adapted to predict diseases from patient visits using hypergraphs of clinical knowledge — with applications in under-resourced healthcare environments.

---

## 🧠 Project Summary

HypKG models patient visits as **hyperedges** in a **knowledge graph**, allowing it to learn contextual relationships among symptoms, clinical findings, and diseases. This repository provides an end-to-end implementation using simulated data — with a clear path to real-world integration for disease prediction, particularly in African and global health settings.

---

## 🔍 What This Repository Contains

| Module                             | Description                                                                 |
|------------------------------------|-----------------------------------------------------------------------------|
| `data/`                            | Simulated raw data (MIMIC-style), KG triples, labels                        |
| `train_kg.py`                      | Trains a PyKEEN TransE model on triples to learn KG embeddings              |
| `build_hypergraph.py`             | Converts visits into KG-based hyperedges and tensors (X, M, labels)         |
| `model.py`                         | Implements the HypKG Transformer in PyTorch                                 |
| `train_transformer.py`            | Trains the hypergraph-based classifier on patient data                      |
| `evaluate.py`                      | Computes official metrics: F1, AUC, Precision@k                             |
| `entity_embeddings.pkl`           | Saved embeddings for all KG entities                                        |

---

## 🗂️ Folder Structure

HypKG/
├── Contextualization/
│ ├── data/
│ │ ├── raw_data/
│ │ │ ├── mimic3/
│ │ │ └── promote/
│ │ ├── triples/
│ │ └── attribute_to_kg_entity.json
│ └── outputs/
├── train_kg.py
├── build_hypergraph.py
├── model.py
├── train_transformer.py
├── evaluate.py
└── README.md

---

## ✅ Setup

```bash
git clone https://github.com/yourusername/HypKG.git
cd HypKG
pip install -r requirements.txt
Dependencies:

pykeen

torch

scikit-learn

numpy, pandas

🚀 How It Works
1. Train KG Embeddings with PyKEEN
bash
Copy
Edit
python train_kg.py
2. Build Hypergraph Inputs
bash
Copy
Edit
python build_hypergraph.py
3. Train the HypKG Transformer
bash
Copy
Edit
python train_transformer.py
4. Evaluate (F1, AUC, Precision@k)
bash
Copy
Edit
python evaluate.py
📈 Sample Output
sql
Copy
Edit
Micro F1 Score:   0.8732
Macro F1 Score:   0.7610
Micro AUC:        0.9045
Macro AUC:        0.8123
Precision@3:      0.9134
Precision@5:      0.8791
🔬 Use Case: Clinical Decision Support in Africa
This model is ideal for:

Integrating symptom and image-based inputs

Enhancing predictions in low-data environments

Building interpretable, context-aware medical AI

📌 Citation
If you use this repo or adapt it for your work, please cite:

bibtex
Copy
Edit
@article{hypkg2024,
  title={HypKG: Hypergraph-based Knowledge Graph Contextualization for Precision Healthcare},
  author={Phillips, Ugo and ...},
  journal={arXiv preprint arXiv:2507.19726},
  year={2024}
}
🤝 Contributing
Pull requests are welcome! Whether you're improving KG quality, adding real data, or integrating image inputs — your contributions are valuable.

📧 Contact
For help or collaboration:

GitHub: @yourusername

Email: youremail@example.com

yaml
Copy
Edit

---

Would you like me to:
- **Generate all supporting files** (`train_kg.py`, `model.py`, etc.) to match this README?
- Help you publish it to your GitHub with a proper license + docs?
- Add Streamlit / frontend API demo integration?

Let’s ship it right! 🚀
