# MNIST Digit Classification with CNN and TensorBoard

This repository contains a Jupyter notebook demonstrating a Convolutional Neural Network (CNN) for classifying handwritten digits from the MNIST dataset. It also integrates TensorFlow's TensorBoard for visualizing training metrics and a custom callback for logging confusion matrices.

This notebook was adapted from an authored by thumarbrijesh@gmail.com.

## Project Structure

- `mnist_cnn_tensorboard.ipynb`: The main Jupyter notebook with all the code for data loading, model definition, training, evaluation, and visualization.
- `logs/`: Directory for TensorBoard logs, including scalar summaries and confusion matrix images.

## Setup and Installation

To run this notebook, you'll need a Python environment with TensorFlow, Keras, Matplotlib, Seaborn, and Pandas installed. You can install these using pip:

```bash
pip install tensorflow matplotlib seaborn pandas scikit-learn
```

If running in Google Colab, most of these libraries are pre-installed. You may only need to load the TensorBoard extension.

## Usage

1.  **Open the Notebook**: Open `mnist_cnn_tensorboard.ipynb` in a Jupyter environment (e.g., Jupyter Lab, Google Colab).
2.  **Run Cells**: Execute all cells sequentially. The notebook will:
    -   Load and preprocess the MNIST dataset.
    -   Define and train a CNN model.
    -   Evaluate the model and display performance metrics (accuracy, precision, recall, specificity, F1-score).
    -   Train a second model with custom TensorBoard callbacks to log confusion matrices per epoch.
3.  **Launch TensorBoard**: A cell in the notebook launches TensorBoard. After running it, you can access the TensorBoard interface (usually at a local URL or a Colab-provided link) to visualize the training process and the logged confusion matrices.

## Results

The model achieves high accuracy on the MNIST dataset. The confusion matrix and per-class metrics provide a detailed view of the model's performance:

### Overall Accuracy
`Overall Accuracy: 0.9915`

### Per-Class Metrics

```
Class  Precision   Recall  Specificity  F1-Score
     0   0.989889 0.998980     0.998891  0.994413
     1   0.986945 0.999119     0.998308  0.992995
     2   0.994163 0.990310     0.999331  0.992233
     3   0.990157 0.996040     0.998888  0.993090
     4   0.989909 0.998982     0.998891  0.994425
     5   0.991021 0.989910     0.999122  0.990466
     6   0.996839 0.987474     0.999668  0.992134
     7   0.984541 0.991245     0.998217  0.987882
     8   0.996901 0.990760     0.999668  0.993821
     9   0.995935 0.971259     0.999555  0.983442

Macro-Averaged Precision: 0.9916
Macro-Averaged Recall: 0.9914
Macro-Averaged Specificity: 0.9991
Macro-Averaged F1-Score: 0.9915
```

### Confusion Matrix

(A confusion matrix image will be generated and logged to TensorBoard during training. You can view it there.)

## Acknowledgements

-   TensorFlow team for the Keras API and TensorBoard.
-   MNIST dataset maintainers.
