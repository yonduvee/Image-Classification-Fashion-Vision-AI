# Fashion Vision AI — Image Classification

A deep learning project for fashion image classification using a **Convolutional Neural Network (CNN)** and a **Dense Neural Network**. The project is organized around a Jupyter Notebook, with saved Keras models and an `outputs/` directory for generated results.

## Project Overview

Fashion Vision AI explores image classification with two neural-network approaches. The main workflow is documented in `image_classification.ipynb`, and the trained models are stored as `.keras` files so they can be loaded again without repeating training.

## Repository Structure

```text
Image-Classification-Fashion-Vision-AI/
├── models/
│   ├── cnn_model.keras
│   └── dense_model.keras
├── outputs/
├── image_classification.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

> The `.gitignore` and `README.md` entries refer to the files you are adding locally; they may not yet appear on the remote repository.

## Models

| Model | Saved file | Description |
| --- | --- | --- |
| Convolutional Neural Network | `models/cnn_model.keras` | Neural-network model for learning visual patterns in images. |
| Dense Neural Network | `models/dense_model.keras` | Fully connected neural-network approach for comparison. |

For the exact layer configurations, training setup, and evaluation results, see the notebook.

## Tech Stack

- Python
- TensorFlow and Keras
- NumPy and pandas
- scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook

Dependency versions are listed in `requirements.txt`.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yonduvee/Image-Classification-Fashion-Vision-AI.git
cd Image-Classification-Fashion-Vision-AI
```

### 2. Create and activate a virtual environment

**Windows PowerShell:**

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

> The requirements include development/pre-release dependencies. Installation may depend on your Python version and operating system.

### 4. Open the notebook

```bash
jupyter notebook image_classification.ipynb
```

Run the cells in order after checking any dataset paths required by the notebook. The original training dataset is not included in the repository structure shown here.

## Saved Models and Outputs

- `models/cnn_model.keras` — saved CNN model.
- `models/dense_model.keras` — saved Dense model.
- `outputs/` — project-generated output artifacts. Consult this folder and the notebook for available plots and predictions.

A saved model can be loaded in Python with Keras:

```python
from tensorflow import keras

cnn_model = keras.models.load_model("models/cnn_model.keras")
dense_model = keras.models.load_model("models/dense_model.keras")
```

To run predictions correctly, use the same preprocessing and input shape that were used during training, as defined in the notebook.

## Reproducibility Notes

- Refer to `image_classification.ipynb` for model architectures, preprocessing, training, and evaluation details.
- Ensure that the expected dataset is available before rerunning training cells.
- This README intentionally does not claim an accuracy score or dataset specification that has not been verified from the notebook.
- The `venv/` folder should remain excluded from Git; the saved model files in `models/` should stay included.

## Repository

[Image-Classification-Fashion-Vision-AI on GitHub](https://github.com/yonduvee/Image-Classification-Fashion-Vision-AI)
