HypKG: Hypergraph-based Knowledge Graph Contextualization for Disease Prediction
An implementation of the HypKG paper, using simulated data, adapted to predict diseases from patient visits using hypergraphs of clinical knowledge, with applications in under-resourced healthcare environments.

🧠 Project Summary
HypKG models patient visits as hyperedges in a knowledge graph, enabling it to learn rich contextual relationships among symptoms, clinical findings, and diseases. This repository provides a complete end-to-end implementation using simulated data, designed with a clear path toward real-world integration for disease prediction, especially tailored for African and global health settings with limited data resources.

🗂️ Folder Structure
.
├── Data/                              #label file
│   ├── edge-labels-mimics3.txt
│   ├── hyperedges-mimic3.txt
│   └── node-embeddings-mimic3
├── HypKG implementation.ipynb        # Jupyter notebook with implementation
├── README.md                         # This documentation file
├── attribute_to_kg_entity.json       # Attribute to KG entity mapping
├── entity_embeddings.pkl             # Saved KG embeddings
├── requirements.txt                  # Python dependencies
├── simulated_kg_test.tsv             #Simulated KG data
├── simulated_kg_train.tsv
├── simulated_kg.tsv

✅ Setup Instructions
git clone https://github.com/yourusername/HypKG.git
cd HypKG
pip install -r requirements.txt
Dependencies
pykeen

torch

scikit-learn

numpy

pandas

⚡PerformanceMicro 
F1 Score:  1.0000
Macro F1 Score:  0.7200
Micro AUC:       1.0
Macro AUC:       nan
Precision@3:     1.0000
Precision@5:     1.0000
