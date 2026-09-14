# SIH26180---KrishiEdge
Plant Nutrient Deficiency Detection - TinyML CNN

**Overview**

This is the TinyML/AI module of our Smart India Hackathon (SIH) smart farming project.

The system uses a lightweight Convolutional Neural Network (CNN) to classify plant leaf images based on nutrient deficiency.

**Technology**

- Python
- TensorFlow
- Keras
- CNN
- TensorFlow Lite
- INT8 Quantization
- TinyML

**Model**

The CNN takes plant leaf images as input.

Input image size:

96 × 96 × 3

The model contains lightweight convolutional layers with 16, 32 and 64 filters.

After training, the model is converted to TensorFlow Lite and INT8 quantization is applied for TinyML/edge-device deployment.

**Current Implementation**

The Python program:

1. Extracts the plant nutrient dataset.
2. Loads training and testing images.
3. Detects the classes automatically.
4. Resizes images to 96 × 96.
5. Performs data augmentation.
6. Trains a lightweight CNN.
7. Evaluates the trained model.
8. Converts the model to TensorFlow Lite.
9. Creates an INT8 quantized TFLite model.
10. Saves the class labels.
11. Displays the INT8 model size and test accuracy.

**Dataset**

The dataset is not included in this repository.

The program expects the dataset to contain:

Nutrition_dataset/
├── train/
│   ├── class folders
│   └── images
│
└── test/
    ├── class folders
    └── images

How to Run

Install the required library:

pip install tensorflow

Then update the dataset ZIP path in "train_tinyml.py":

ZIP_DATASET_PATH = r"C:\Users\ad212\Downloads\archive(5).zip"

Run:

python train_tinyml.py

**Output**

After successful execution, the program creates:

- "plant_tinyml_model.keras"
- "plant_model_float32.tflite"
- "plant_model_int8.tflite"
- "labels.txt"

The main TinyML output is:

plant_model_int8.tflite

SIH Contribution

This repository represents the plant nutrient deficiency detection and TinyML CNN component of the overall SIH smart farming solution.
