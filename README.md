# EyeAge-Prediction-FundusDL

This repository contains the full codebase for the study:  
**"A Deep Learning Approach to Predict Biological Age using Eye Fundus Images"**  

> We present a deep learning-based method that predicts biological age from fundus images using CNN architectures (VGG16, FasterViT, LCNet). This project features data preprocessing, model training, and robust evaluation across multiple external datasets.

---

## 🧪 Project Structure

| Notebook | Purpose |
|----------|---------|
| `data_process.ipynb` | Image loading, quality control, preprocessing, and dataset saving |
| `model_training.ipynb` | Deep learning model definition (e.g., VGG16, LCNet), training, and internal validation |
| `Evaluation.ipynb` | Model testing on external datasets, subgroup analysis, Grad-CAM visualization |

---

## 📊 Datasets Used

| Dataset Name | Usage | Source Population | Labels |
|--------------|-------|-------------------|--------|
| NTUH | Training / Validation / Internal Test | Taiwan | Chronological Age |
| ODIR-5K | External Test | China | Chronological Age |
| SMGD | External Test | Multiple | Chronological Age |
| Taiwanese' Dataset | External Test | Taiwan | Biological Age / Chronological Age |

---

## 🧠 Models

The following CNN backbones were tested:

- VGG16 (ImageNet-pretrained)
- FasterViT
- LCNet (lightweight custom backbone)

---

## 🔥 Highlights

- **Best MAE**: 4.17 years using LCNet on NTUH dataset
- **Robust across age, sex, and disease subgroups**
- **Grad-CAM**: Highlights retinal arcade vessels as aging-relevant regions

---

## 📦 Installation

We provide both `conda` and `pip` requirement files:

```bash
# Using conda
conda env create -f conda_requirements.yml
conda activate eyeage_env

# OR using pip
pip install -r pip_requirements.txt
```

---

## ▶️ Quick Start

```bash
# Step 1: Preprocess dataset
Run `data_process.ipynb`

# Step 2: Train the model
Run `model_training.ipynb`

# Step 3: Evaluate performance
Run `Evaluation.ipynb`
```

All paths in the notebook assume the following folder structure:

```
.
├── original_data/
├── evaluation_dataset/
├── Dataset/
├── *.ipynb
```

---

## 📈 Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Pearson Correlation (r)
- Grad-CAM Heatmap Visualizations

---

## 🛡️ License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

This work was supported by:
- NTU Center of Genomics and Precision Medicine
- Ministry of Science and Technology (MOST), Taiwan
- NTUH Department of Ophthalmology

We thank all collaborators and contributors to the dataset and analysis pipeline.
