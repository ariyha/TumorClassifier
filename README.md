# Brain Tumor Classification Using Machine Learning

## Project Overview

This project focuses on the classification of brain tumors using image processing and machine learning techniques. The dataset consists of MRI images categorized into two classes: "No Tumor" and "Pituitary Tumor". The goal is to develop a model that can accurately classify the images into these categories.

## Project Structure

- **Training Data**: Located in the `Training` directory, containing subdirectories for each class (`no_tumor` and `pituitary_tumor`).
- **Testing Data**: Located in the `Testing` directory, used to evaluate the performance of the model.

## Libraries and Tools

The following Python libraries are used in this project:

- `numpy`: For numerical operations and handling arrays.
- `pandas`: For data manipulation and analysis.
- `matplotlib`: For data visualization.
- `scikit-learn`: For machine learning models and evaluation.
- `opencv (cv2)`: For image processing.

## Steps in the Project

1. **Data Loading and Preprocessing**:
   - Images are loaded from the `Training` directory.
   - Each image is resized to `200x200` pixels and converted to grayscale.
   - The images are flattened into 1D arrays and stored in `X`.
   - Corresponding labels are stored in `Y`, where `0` indicates "No Tumor" and `1` indicates "Pituitary Tumor".

2. **Data Splitting**:
   - The dataset is split into training and testing sets using an 80-20 split.

3. **Feature Scaling**:
   - Pixel values are scaled to a range of `[0, 1]` by dividing by 255.

4. **Model Training**:
   - Two machine learning models are trained: Logistic Regression and Support Vector Classifier (SVC).
   - The models are trained on the training set (`xtrain`, `ytrain`).

5. **Model Evaluation**:
   - The accuracy of both models is evaluated on the training and testing sets.
   - The SVC model is further used for prediction and visualization.

6. **Misclassification Analysis**:
   - Misclassified samples are identified and printed.

7. **Visualization of Predictions**:
   - Predictions on new test images are visualized with the predicted class labels.

## Results

- The training and testing accuracy for both models are printed.
- The total number of misclassified samples is displayed.
- Sample predictions are visualized using the SVC model, with images from both classes ("No Tumor" and "Pituitary Tumor").

## How to Run

1. Ensure all required libraries are installed:
   ```bash
   pip install numpy pandas matplotlib scikit-learn opencv-python
