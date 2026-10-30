# Drawing-to-3D

**Generating 3D CAD models from 2D drawings using neural networks**

A research and engineering project exploring how deep learning can reconstruct 3D CAD models from 2D technical drawings. The repository combines source code, trained models, experimental results, and a thesis.

---

## Overview

Creating 3D models from 2D drawings is traditionally a manual, time-consuming CAD task. This project investigates whether modern neural architectures can automate this process end-to-end.

Every major architectural choice is documented as an Architecture Decision Record (ADR) in `docs/adr/`.

**Key goals:**
- Build a reproducible pipeline: `2D drawing → features → 3D CAD model`.
- Train and evaluate neural models on a curated dataset of drawings.
- Document the research process and decisions.

---

## Project Structure

| Path | Purpose |
|------|---------|
| `data/raw/` | Original, unmodified data (drawings, scans, source datasets). |
| `data/processed/` | Cleaned and prepared data ready for training/evaluation. |
| `src/models/` | Neural network architectures and model definitions. |
| `src/training/` | Training loops, loss functions, hyperparameter configs. |
| `src/evaluation/` | Metrics, evaluation scripts, comparison against baselines. |
| `src/utils/` | Shared utilities (data loading, logging, visualization). |
| `models/checkpoints/` | Trained model weights and checkpoints. |
| `docs/thesis/` | Thesis chapters in Markdown. |
| `docs/assets/` | Figures, diagrams, and other assets used in the thesis. |
| `docs/adr/` | Architecture Decision Records — why each key decision was made. |
| `scripts/` | Helper scripts (e.g., thesis build via Pandoc). |
| `results/figures/` | Generated plots and visualizations. |
| `results/tables/` | Generated result tables (metrics, comparisons). |

**Note:** The thesis is written in Markdown and assembled into `.docx` via Pandoc. See `docs/thesis/README.md` (coming soon) for the build instructions.

---

## Getting Started

> The project is in early development. Setup instructions will be expanded as the pipeline is implemented.

```bash
# Clone the repository
git clone https://github.com/deep-learning-engineer/neural-cad-reconstruction.git
cd neural-cad-reconstruction

# (Optional) Create a virtual environment
python -m venv .venv
source .venv/bin/activate   # on Windows: .venv\Scripts\activate

# Install dependencies (requirements.txt to be added)
# pip install -r requirements.txt
```

---

## License

This project is licensed under the **Mozilla Public License 2.0 (MPL-2.0)**.
See the [`LICENSE`](LICENSE) file for the full text.

---

## Author

**Ganzha Eduard**
- Institution: Far Eastern Federal University (FEFU), Institute of Mathematics and Computer Technologies (IMCT)
- Thesis topic: *Создание 3D моделей по чертежам*
- Contact: edik.ganzha.05@gmail.com 

