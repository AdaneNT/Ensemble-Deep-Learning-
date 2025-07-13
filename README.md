# Ensemble-Deep-Learning for Human Activity Recognition (HAR)

This repository provides an implementation of an **ensemble hybrid deep learning framework** for **Human Activity Recognition (HAR)** using the **WISDM** dataset. It includes stacked models combining CNNs, RNN variants (LSTM, GRU, BiLSTM, BiGRU), and classical ensemble techniques (Random Forest, Gradient Boosting) for final classification.

---

## Project Highlights

- Hybrid deep learning models: CNN-BiGRU, CNN-BiLSTM, CNN-LSTM, and CNN-GRU.
- Stack-based ensemble learning using predictions of deep models.
- Meta-learners include Random Forest and Gradient Boosting with GridSearchCV.
- High accuracy achieved on the WISDM dataset (up to **99.4%**).
- Confusion matrix visualization and classification reports for evaluation.

---

## Models Included

- `CNN-GRU_Model_train_WISDM_500.ipynb`
- `CNN-LSTM_Hybrid_model_500.ipynb`
- `CNN-BiGRU_Hybrid_model_500.ipynb`
- `CNN-BiLSTM_Hybrid_model_500.ipynb`
- `1__Stacked_ensemble_hybrid_model.ipynb` (main ensemble model)

---

## Dataset

This project uses the [WISDM v1.1 dataset](https://www.cis.fordham.edu/wisdm/dataset.php), which includes smartphone accelerometer data for six activities:

- Walking
- Jogging
- Upstairs
- Downstairs
- Sitting
- Standing

**Preprocessing steps:**

- Dropping missing values
- Label encoding of activity labels
- Under-sampling to balance activity classes
- Standardization of sensor values (`x`, `y`, `z` axes)
- Segmenting the time series using sliding windows

---

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/AdaneNT/Ensemble-Deep-Learning.git
    cd Ensemble-Deep-Learning
    ```

2. install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the WISDM dataset and place `WISDM_ar_v1.1_raw.txt` in the project folder.

4. Open and run one of the model notebooks:
    ```bash
    jupyter notebook CNN-BiGRU_Hybrid_model_500.ipynb
    ```

5. For ensemble stacking:
    ```bash
    jupyter notebook 1__Stacked_ensemble_hybrid_model.ipynb
    ```

---

## Results

| Model             | Accuracy |
|------------------|----------|
| CNN-BiGRU        | 99.96%   |
| CNN-LSTM         | ~98.5%   |
| CNN-BiLSTM       | ~99.0%   |
| Stacked Ensemble | **99.4%** |

> 📈 Confusion matrix heatmaps and classification reports are generated automatically in each notebook.

---

## 📁 Project Structure

