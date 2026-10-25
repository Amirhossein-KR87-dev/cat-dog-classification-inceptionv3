# 🐱🐶 Cat vs Dog Image Classification

A deep learning project that classifies images as cats or dogs using **transfer learning with InceptionV3**.

## 📌 Project Overview

The goal of this project is to build an image classification model that can distinguish between cats and dogs.

The model uses **InceptionV3 pretrained on ImageNet** as its base model. The pretrained layers are frozen, and a custom classification head is added for binary classification.

### Model Architecture

```text
InceptionV3 (ImageNet)
        ↓
GlobalAveragePooling2D
        ↓
Dense (128, ReLU)
        ↓
Dropout (0.5)
        ↓
Dense (1, Sigmoid)
        ↓
Cat / Dog
```

## 📂 Project Structure

```text
cat-dog-classification/
│
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── Images/
│
├── models/
│   └── cat_dog_inceptionv3.keras
│
├── train_model.ipynb
├── predict_image.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

- `data/`: Contains the training, validation, and test datasets.
- `Images/`: Stores images used for prediction or demonstration.
- `models/`: Stores the trained model.
- `train_model.ipynb`: Notebook for preparing the data and training the model.
- `predict_image.ipynb`: Notebook for loading the trained model and making predictions.
- `requirements.txt`: Lists the Python packages required by the project.

> The dataset is not included in this repository because of its size. You may need to download it separately.

## 🧠 Technologies

- Python
- TensorFlow and Keras
- InceptionV3
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## 📊 Dataset

The project uses images of cats and dogs for binary image classification.

The dataset is organized into three subsets:

- **Training:** Used to train the model.
- **Validation:** Used to monitor the model's performance during training.
- **Test:** Reserved for evaluating the trained model on unseen images.

Images are resized to **299 × 299 pixels**, the input size used by InceptionV3, and preprocessed using InceptionV3's `preprocess_input` function.

*Add the original dataset source and license here before publishing.*

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd cat-dog-classification
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 🚀 Training

1. Make sure the dataset is organized in the expected directory structure.
2. Open `train_model.ipynb`.
3. Run the notebook cells to train the model.

The trained model is saved to:

```text
models/cat_dog_inceptionv3.keras
```

## 🔍 Prediction

1. Make sure the trained model exists in the `models/` directory.
2. Place an image in the `Images/` directory.
3. Open `predict_image.ipynb`.
4. Set the image path and run the notebook to predict whether the image contains a cat or a dog.

Example output:

```text
Prediction: Dog
Confidence: 94.21%
```

*The output above is an example only, not a measured result from this project.*

## 📈 Results

Add your actual results after training and evaluating the model.

```text
Training Accuracy: [your result]
Validation Accuracy: [your result]
Test Accuracy: [your result]
```

You can also include plots showing training and validation accuracy and loss.

## 🔮 Future Improvements

- Fine-tune selected layers of InceptionV3.
- Apply data augmentation.
- Evaluate performance on the test dataset.
- Create a confusion matrix.
- Test the model on real-world images.
- Build a real-time cat and dog classifier using OpenCV.

## 👨‍💻 Author

**Amirhossein**

This project is part of my learning journey in deep learning and computer vision. It helps me practice transfer learning, image preprocessing, model training, and image classification.
