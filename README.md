# 🌊 Water Body Segmentation from Multispectral Satellite Images

This project focuses on detecting and segmenting **water bodies** using **multispectral satellite imagery** and a custom-trained **U-Net model**.

It utilizes advanced preprocessing techniques and applies deep learning to analyze remote sensing data for environmental and geospatial insights.

---

## 📂 Project Structure

📁 water-segmentation/

├── model_training.ipynb # Main notebook for training and evaluation

├── dataset/ # Folder containing image & mask tensors

├── Task.pdf # Project description

└── README.md # Project documentation


---

## 📓 Notebook Overview: `model_training.ipynb`

This Jupyter notebook covers the entire pipeline:

1. **Loading Data**: Preprocessed multispectral tensors (with bands like NDWI)
2. **Normalization**: Channel-wise scaling to [0, 1]
3. **Augmentation**: Applied on both images and masks
4. **Split dataset**: split dataset into train and test
5. **Model Architecture**: U-Net with encoder-decoder blocks
6. **Training**: Binary segmentation using Dice loss + IoU metric
7. **Evaluation**: Visual outputs + metric scores on test data
8. **Prediction**: Compare the output of model with actual output by visualization

## 🧪 Evaluation Metrics

We use several metrics to assess the performance of the model:

| Metric            | Description                                                  |
|-------------------|--------------------------------------------------------------|
| **Dice Coefficient** | Measures overlap between predicted & true masks (F1 score) |
| **IoU (Jaccard)**    | Ratio between intersection and union of masks              |

The training notebook displays live plots of **training vs validation accuracy**, and prints final scores on the test set.

output Accurecy:
```bash
Test IoU:         63.357 %
Test Dice Score:   77.55 %
```

---

## 🛠️ Tech Stack

- Python 🐍
- TensorFlow / Keras
- tifffile
- PIL
- NumPy
- albumentations ( for data augmentation )
- Satellite Data (multispectral with ~12 channels)

---
