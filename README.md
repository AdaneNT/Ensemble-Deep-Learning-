## Sensor Fusion  and Ensemble Deep Learning for Wearable Sensor Data Analysis
**Human Activity Recognition (HAR) using Smart Belt, WISDM, and UCI Datasets**

> **"Efficient Human Gait Activity Recognition Based on Sensor Fusion and Intelligent Stacking Framework"**  
> *Adane Tarekegn, et al.*  
> *IEEE Sensors Journal, November 2023*  
> [DOI: 10.1109/JSEN.2023.3319353](https://doi.org/10.1109/JSEN.2023.3319353)


## Highlights
- Deep learning models (CNN-LSTM, CNN-BiLSTM, CNN-GRU, CNN-BiGRU)
- Classical ensemble learners (Random Forest, Gradient Boosting)
- Stacked meta-learning architecture
- Evaluation on three datasets: Smart Belt, WISDM, and UCI HAR

---

## Models Included

| Model Notebook                          | Description                         |
|----------------------------------------|-------------------------------------|
| `CNN-GRU_Model_train_WISDM_500.ipynb`  | CNN with GRU                        |
| `CNN-LSTM_Hybrid_model_500.ipynb`      | CNN with LSTM                       |
| `CNN-BiGRU_Hybrid_model_500.ipynb`     | CNN with Bi-directional GRU         |
| `CNN-BiLSTM_Hybrid_model_500.ipynb`    | CNN with Bi-directional LSTM        |
| `1__Stacked_ensemble_hybrid_model.ipynb`| Final ensemble using RF and GBoost |

---
## Dataset Information

### 1. Smart Belt Dataset
- Collected from 12 participants using a custom belt with 3 IMU sensors (sampling rate: 100 Hz)
- Activities: Walking, walking upstairs/downstairs, sitting, standing, lying
- Annotated using [**NOVA**](https://github.com/hcmlab/nova)
- Dataset available in the [`Datasets/`](./Datasets/) folder (`smart_belt_dataset.csv`)  
  or [external link](https://alamedaproject.eu/)
- Oversampling applied to balance activity classes
  
### 2. WISDM v1.1
- Smartphone accelerometer data
- 6 activity classes: Walking, Jogging, Upstairs, Downstairs, Sitting, Standing
- Sampling rate: 20 Hz
- Used **undersampling** for class balancing
- WISDM Dataset Dataset link : https://www.cis.fordham.edu/wisdm/dataset.php
  
### 3. UCI HAR
- IMU data (accelerometer + gyroscope) from smartphones
- 6 activities: Walking, Upstairs, Downstairs, Sitting, Standing, Lying
- Sampling rate: 50 Hz
- Preprocessed and balanced → no resampling needed
- UCI HAR Dataset Dataset link: https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones

---
## Framework Overview

The architecture of the WS-HGAR model, combining sensor fusion, hybrid deep learning, and stacking ensemble:

![Framework Overview](figures/ws-hgar-framework.png)

*Figure 1: End-to-end structure of the proposed WS-HGAR model as described in the paper.*

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/AdaneNT/Ensemble-Deep-Learning.git
cd Ensemble-Deep-Learning
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download the  dataset and place it in the project folder.

Launch Jupyter and run any model notebook:

```bash
jupyter notebook CNN-BiGRU_Hybrid_model_500.ipynb
```

For the ensemble model:

```bash
jupyter notebook 1__Stacked_ensemble_hybrid_model.ipynb
```

---

## 📖 Citation

If you use this work, please cite the paper:

```bibtex
@article{tarekegn2023gait,
  author    = {A. N. Tarekegn and M. Sajjad and F. A. Cheikh and M. Ullah and K. Muhammad},
  title     = {Efficient Human Gait Activity Recognition Based on Sensor Fusion and Intelligent Stacking Framework},
  journal   = {IEEE Sensors Journal},
  volume    = {23},
  number    = {22},
  pages     = {28355--28369},
  year      = {2023},
  month     = {Nov. 15},
  doi       = {10.1109/JSEN.2023.3319353},
  keywords  = {Intelligent sensors;Activity recognition;Belts;Monitoring;Feature extraction;Medical services;Stacking;Belt sensor;deep learning (DL);gait activity recognition;sensor fusion;stacking ensemble;wearable sensor}
}

```
[DOI: 10.1007/978-3-031-29695-1_17](https://doi.org/10.1007/978-3-031-29695-1_17)
