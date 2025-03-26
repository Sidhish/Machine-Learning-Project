# Code-Switching and Code-Mixing Statement Analysis Using TF-IDF

## Overview
This project analyzes code-switching and code-mixing in text statements using TF-IDF and logistic regression. It classifies sentences into three categories:
- **Code-Switched** (mixing full sentences or clauses from different languages)
- **Code-Mixed** (mixing words or phrases within a sentence)
- **Monolingual** (single-language text)

## Dataset
The dataset used for training and evaluation is a CSV file named `code_switching_code_mixing_dataset_100k.csv`, containing:
- **text**: The input text
- **label**: The corresponding classification label (code-switched, code-mixed, monolingual)

## Installation and Dependencies
To run this project, ensure you have the following dependencies installed:
```bash
pip install pandas scikit-learn matplotlib seaborn
```

## Implementation
1. **Load Dataset**: Reads the CSV file into a Pandas DataFrame.
2. **Preprocessing**:
   - Splits the dataset into training and testing sets.
   - Transforms text using TF-IDF (unigrams and bigrams, max 500 features).
3. **Model Training**:
   - Uses logistic regression (One-vs-Rest approach) to classify text.
4. **Evaluation**:
   - Calculates accuracy and generates a classification report.
   - Displays a confusion matrix using Seaborn.
5. **Prediction**:
   - Classifies new sentences to demonstrate model predictions.

## Usage
Run the script in a Python environment to train and evaluate the model:
```bash
python code_switching_analysis.py
```
To predict new sentences, modify the `new_sentences` list in the script.

## Output
- **Accuracy Score**
- **Classification Report**
- **Confusion Matrix Visualization**
- **Predictions for New Sentences**

## Example Prediction
Input:
```python
new_sentences = [
    'Can you help me with this tarea?',
    'This is an excelente opportunity',
    'The party was very fun'
]
```
Output:
```bash
Sentence: 'Can you help me with this tarea?' -> Prediction: code-switched
Sentence: 'This is an excelente opportunity' -> Prediction: code-mixed
Sentence: 'The party was very fun' -> Prediction: monolingual
```

## Contribution
Feel free to contribute by improving the dataset, experimenting with different models, or enhancing the feature extraction process.

## License
This project is open-source under the MIT License.

