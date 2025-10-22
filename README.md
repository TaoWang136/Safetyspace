# Safetyspace
Inferring parameter of spacing of micro-mobility users in shared space
🛴 Safetyspace
Inferring the Spacing Parameters of Micro-Mobility Users in Shared Spaces

This repository provides code and data for estimating spacing behavior between micro-mobility users (e-scooters, e-bikes, etc.) and pedestrians in shared spaces. The work aims to infer parameters that describe human comfort and safety zones during interactions.

📂 Dataset Description

The file data.csv contains the raw observation data used for spacing inference. Each row represents a frame of an interaction between a micro-mobility user and a pedestrian.

Column	Description
near_x, near_y	The pedestrian’s coordinates in the local coordinate system of the micro-mobility user.
v	The relative speed between the pedestrian and the micro-mobility user.
region	The angular region ID (1–16) indicating which sector of the polar coordinate system the pedestrian is located in.
Distance	The Euclidean distance between the two agents (micro-mobility and pedestrian).
🧠 Purpose

The goal of this repository is to estimate the spacing distribution parameters that characterize interaction comfort and conflict zones.
The estimated parameters can be used for:

Micro-mobility safety modeling,

Surrogate safety assessment,

Policy and infrastructure design for shared spaces.

📘 Code Structure
File	Description
mle_gaussian_log.ipynb	Performs maximum-likelihood estimation (MLE) of spacing distributions using the data from data.csv.
case_study.ipynb	A case study based on the SinD dataset to validate the model. The SinD dataset can be found at: https://github.com/SOTIF-AVLab/SinD/
⚙️ Environment Requirements

The code was developed and tested under the following environment:

Package	Version
numpy	1.21.6
torch	1.7.0
torchaudio	0.7.0
torchvision	0.8.0
pandas	1.1.5
matplotlib	3.5.3
scipy	1.7.3

You can install dependencies via:

pip install -r requirements.txt


(or manually install the packages with the specified versions above.)

🧩 Usage

Prepare data
Place your raw data file (data.csv) in the repository root or update the path inside the notebooks.

Run the estimation notebook
Open and execute:

jupyter notebook mle_gaussian_log.ipynb


This estimates spacing parameters using MLE.

Run the case study
To reproduce case-study analysis with the SinD dataset, execute:

jupyter notebook case_study.ipynb

📈 Output

The notebook outputs include:

Estimated distribution parameters for longitudinal and lateral spacing,

Visualization of comfort and risk zones,

Comparison plots with reference datasets.

🧾 Citation

If you use this repository or code in your research, please cite:

Wang, T., Ge, Y., Zhong, M., et al. A novel safety model for capturing interactions between micro-mobility and pedestrians in shared spaces.
