<p align="center">
  <a href="https://wildlabs.net/discussion/wildlabs-awards-2024-boutscout-monitoring-system-avian-nesting-behavior-studies" target="_blank">
    <img src="assets/logoboutscout.png" width="600px" />
  </a>
</p>

# BoutScout: A Deep Learning Framework for Automatic Detection of Incubation Events in Avian Nests Using Temperature Time Series

BoutScout is a deep learning-based tool designed to automatically classify avian incubation behavior from nest temperature time series. It helps researchers detect **on-bouts**, **off-bouts**, and **nocturnal incubation** using a BiLSTM architecture trained on thousands of annotated days across diverse tropical bird species.

This repository contains a cleaned and organized version of the final model, supplementary notebooks, and scripts used for testing and deployment. All files were versioned and pushed directly from a local development environment using PyCharm and Git.

---

## Features

✔ Automatically classifies incubation events from temperature data  
✔ Handles noisy and multiday sequences  
✔ Trained on diverse Neotropical bird species  
✔ Can be adapted to other sensors or event types  
✔ Final model available in `.pth` format  
✔ Supplementary analysis notebooks included  

---

## Input Format

You should provide a CSV or DataFrame-like structure with:
- One column for egg/nest temperature
- One column for ambient temperature (optional, but recommended)
- A timestamp column named `tiempo` in datetime format

---

## Output

- Per-minute classification: `On`, `Off`, `Nocturnal`, or `Error`
- Day-by-day visualizations of classification output
- Summary statistics per nest/day

---

##  Model Info
🧠
- Type: BiLSTM (Bidirectional Long Short-Term Memory)
- Input: 1440 time steps (one day of 1-min resolution)
- Output: sequence of state labels per minute
- Loss function: CrossEntropyLoss
- Optimizer: Adam
- Framework: PyTorch

---

## 🗂️ Folder Structure

```
BoutScout_Model/
│
├── notebooks/
│   ├── supplementary_1.ipynb # First Modelling 8/2
│   ├── supplementary_2.ipynb # Cross Validation 5-Fold Modelling
│   └── supplementary_3.ipynb # Final Modelling Full-dataset
├── model/
│   └── modelo_entrenado_final_total.pth
├── assets/
│   └── boutscout_logo.png
├── .gitignore
├── README.md
```

---

## 📦 Installation & Usage

This project was tested locally using Python 3.10+ and PyTorch. To reproduce results or use the model:

```bash
git clone https://github.com/jorgelizarazo94/BoutScout_Model.git
cd BoutScout_Model
# Install dependencies
pip install -r requirements.txt
```

---

## **Contact**

For questions, collaboration, or access to more information:  
📧 jorge.lizarazo.b@gmail.com  
🐛 [GitHub Issues](https://github.com/jorgelizarazo94/BoutScout_Model/issues)

https://jorgelizarazo.link/

---

<p align="center">
  <a href="https://wildlabs.net/" target="_blank">
    <img src="assets/logo.png" width="800px" />
  </a>
</p>


*Nature pens the mysteries; we humbly decipher them*