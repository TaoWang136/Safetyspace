# 🛴 Safetyspace
### Inferring the Spacing Parameters of Micro-Mobility Users in Shared Spaces

This repository provides code and data for estimating **spacing behavior** between micro-mobility users (e-scooters, e-bikes, etc.) and pedestrians in shared spaces. We infer parameters that describe human comfort/safety zones during interactions.

---

## 📂 Data

**`data.csv`** is the raw dataset. Each row corresponds to one observation frame of an interaction.

| Column      | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `near_x`    | Pedestrian **x** coordinate in the micro-mobility user’s **local frame**.   |
| `near_y`    | Pedestrian **y** coordinate in the micro-mobility user’s **local frame**.   |
| `v`         | **Relative speed** between the pedestrian and the micro-mobility user.      |
| `region`    | **Polar sector ID** (1–16) indicating the pedestrian’s angular region.      |
| `Distance`  | **Euclidean distance** between the two agents.                              |

> The case study uses the SinD dataset (link below).

---

## 📘 Repository Contents

- `mle_gaussian_log.ipynb` — Maximum-likelihood estimation (MLE) of spacing distributions using `data.csv`.
- `case_study.ipynb` — Case study with the **SinD** dataset to validate the model.  
  SinD: https://github.com/SOTIF-AVLab/SinD/

---

## ⚙️ Environment

numpy==1.21.6\
torch==1.7.0
torchaudio==0.7.0
torchvision==0.8.0
pandas==1.1.5
matplotlib==3.5.3
scipy==1.7.3


The project was tested with the following versions:

