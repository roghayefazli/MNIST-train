# MNIST-train

### TFKerasMNIST.ipynb

This Jupyter Notebook demonstrates how to build, train, and evaluate a simple neural network using TensorFlow and Keras to classify handwritten digits from the MNIST dataset.

#### Project Overview

The notebook walks through the entire machine learning pipeline for a multi-class classification problem:

1.  **Data Preparation:** It loads the MNIST dataset using `tensorflow_datasets`, which automatically handles splitting the data into training and testing sets.
2.  **Preprocessing:** The image data is normalized to a range of 0-1 and the dataset is configured for efficient training using caching, shuffling, and prefetching.
3.  **Model Architecture:** A simple `Sequential` model is defined, consisting of:
      * A `Flatten` layer to convert the 28x28 pixel images into a 1D array.
      * A `Dense` hidden layer with 100 units and `relu` activation.
      * A `Dense` output layer with 10 units (one for each digit from 0 to 9) and a `softmax` activation function for probability distribution.
4.  **Training:** The model is compiled with the `Adam` optimizer and `SparseCategoricalCrossentropy` loss. It is then trained for 10 epochs on the training data and validated on the test data.
5.  **Prediction:** The notebook concludes by using the trained model to predict the class of a test image and displays the result.

#### Requirements

This project requires the following Python libraries:

  * `tensorflow`
  * `tensorflow_datasets`
  * `numpy`

You can install these dependencies using pip:

```bash
pip install tensorflow tensorflow_datasets numpy
```

#### How to Run

1.  **Install Dependencies:** Ensure you have all the required libraries installed.
2.  **Open the Notebook:** Open `TFKerasMNIST.ipynb` in a Jupyter Notebook environment (e.g., JupyterLab or Google Colab).
3.  **Execute Cells:** Run the cells sequentially to load the data, build and train the model, and perform a sample prediction. The output of the training process will be visible in the notebook, showing the loss and accuracy metrics for each epoch.
