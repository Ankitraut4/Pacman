# PACMAN GAME

Perceptron Classifier for Digit and Pacman Data - 
This project implements a basic Perceptron Classifier for digit and Pacman-related classification tasks. The core classifier is designed to learn from labeled training data to distinguish between different categories, using a simple linear model. The project includes separate scripts for general classification tasks, data handling, and a specific adaptation for Pacman data classification.


![image](https://github.com/user-attachments/assets/28d2af1a-929b-4b22-a4a7-f52af37fc597)




Project Structure

perceptron.py: Contains the implementation of the PerceptronClassifier, a basic perceptron model that can be trained on any labeled dataset to make predictions. This file includes methods for training, classification, and interpretation of learned weights.

dataClassifier.py: A command-line utility script for configuring, training, and testing classifiers on different datasets. Supports both digit and Pacman datasets, and handles command-line options to customize the classifier and data processing.

perceptron_pacman.py: Extends the base PerceptronClassifier specifically for Pacman classification tasks, implementing any custom behavior needed for this specialized application.


Prerequisites - 

Python 3.x , 
Necessary libraries (standard Python libraries should suffice i.e. numpy, keras, etc; no additional libraries are required unless specified for data handling)

Installation

1. Clone this repository to your local machine.

2. Ensure you have Python 3 installed.

3. (Optional) Create a virtual environment:

bash code :- 

  python3 -m venv venv

source venv/bin/activate  # On Windows use `venv\Scripts\activate`

Usage

Running the Classifier To train and test the classifier on a dataset, use the dataClassifier.py script. You can specify various options, such as the dataset (Pacman or digit), the classifier type, and the number of iterations for training.

Example Command:

bash code :- 

  python dataClassifier.py -c perceptron -d digits -t 10

Options:

-c or --classifier: Selects the classifier type. Options include perceptron.
-d or --dataset: Specifies the dataset. Options are digits or pacman.
-t or --training: Specifies the number of training iterations.


Testing on Pacman Data The perceptron classifier is adapted for Pacman data in perceptron_pacman.py. This adaptation is loaded automatically if the Pacman dataset is selected in dataClassifier.py.

File Descriptions

1]perceptron.py: Implements the core perceptron algorithm, including:

   train: Trains the classifier by adjusting weights based on misclassifications.
 
   classify: Classifies input data by selecting the label with the highest feature-weighted score.

   findHighWeightFeatures: Returns the highest-weighted features for interpretation purposes.

2]dataClassifier.py: A utility for training/testing classifiers with options for data source, classifier type, and training iterations. It loads the appropriate dataset and evaluates classifier performance on training, validation, and test sets.

3]perceptron_pacman.py: Extends the perceptron classifier for use with Pacman-specific tasks, with custom handling in the classify method for Pacman-related data nuances.

Examples

1] Training the Perceptron on Digit Data:

bash code:-

  python dataClassifier.py -c perceptron -d digits -t 10

2] Training the Perceptron on Pacman Data:

bash code:- 

  python dataClassifier.py -c perceptron -d pacman -t 10



Contributing - 
Feel free to open issues, submit pull requests, or suggest improvements!

License -This project is open-source. You may use, distribute, and modify it under the terms specified in the LICENSE file.
