# Benchmarking Evolutionary Conservation Features for microRNA Target Site Classification

**Author:** Michele Terribile  
**Project:** Final Year Project 2025

This is the GitHub repository that houses all the code and data used for my FYP.

---

##  Repository Structure

├── Balanced_dataset.tsv # Full dataset used for training and testing
├── README.md # This file
├── tezicode/ # Main project folder
│
├── all/ # Models trained WITH conservation scores (phyloP and phastCons)
│ ├── LogisticRegression.ipynb
│ ├── NeuralNetwork.ipynb
│ ├── RandomForest.ipynb
│ └── SVM.ipynb
│
└── genemirnasequence/ # Models trained WITHOUT conservation scores
├── logisticregression.ipynb
├── neuralnetwork.ipynb
├── randomforest.ipynb
└── svm.ipynb

---

## 🚀 Usage

All scripts are Jupyter Notebooks and can be run in **Visual Studio Code** using the "Run Python File" button or in **Jupyter Notebook**.

### ▶️ To run the Random Forest model **with conservation scores**:

1. Open `all/RandomForest.ipynb` in VS Code or Jupyter.
2. Click the **"Run All"** button or run each cell sequentially.
3. After training, the script:
   - Displays the **ROC-AUC curve** in a new window.
   - Once closed, displays the **Precision-Recall curve**.
4. When both graphs are closed, the **script has finished executing**.

### ▶️ To run the Neural Network model **without conservation scores**:

1. Open `genemirnasequence/neuralnetwork.ipynb`.
2. Click the **"Run All"** button or run each cell sequentially.

> ⚠️ **Important:**  
> Ensure the path to `Balanced_dataset.tsv` is correct in your script.  
> If you encounter a "file not found" error, update the relative or absolute path accordingly.  
> SVM models may take longer to execute — please wait for them to finish.

---

## 📤 Terminal Output Overview

Each script prints the following during execution:

- Frequencies of all **256 possible 4-mers** for gene and ncRNA sequences.
- Shapes of:
  - Gene k-mers
  - ncRNA k-mers
  - `phyloP` scores
  - `phastCons` scores
  - Combined feature matrix `X`
- Previews:
  - First 10 values of the feature matrix
  - Last two conservation features
  - Column-wise means
  - First 10 labels and all unique classes
- Splits the dataset (80% training, 20% testing)
- Trains the model and performs cross-validation
- Saves and reloads the model
- Evaluates the model on test data
- Displays:
  - **ROC-AUC graph**
  - **Precision-Recall graph**

Once both graphs are closed, the terminal is ready for a new run.

---
