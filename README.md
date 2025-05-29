Benchmarking Evolutionary Conservation Features for microRNA Target Site Classification
Michele Terribile FYP2025.

This is the Github Repository that houses all the codes used for my FYP.

folder- tezicode

file- Balanced_dataset.tsv               # The full dataset used for training and testing

folder- all                               # Models trained with conservation scores (with phylop and phastcons)
file contents of folder all- LogisticRegression.ipynb
                             NeuralNetwork.ipynb
                             RandomForest.ipynb
                             SVM.ipynb

folder- genemirnasequence           # Models trained without conservation scores (without pyhlop and phastcons)
file contents of folder genemirnasequence-    logisticregression.ipynb
                                              neuralnetwork.ipynb
                                              randomforest.ipynb
                                              svm.ipynb

README.md                          # This file

Usage:

All scripts are standard Python files and can be run directly in **Visual Studio Code** using the "Run Python File" button at the top right of the editor.



To run the Random Forest model **with conservation scores**:

1. Open `all/RandomForest.py` in VS Code.
2. Click the **"Run Python File"** button (arrow/triangle) in the top right corner.
3. Once it is done, a python file is generated and popped up displaying the ROC-AUC curve graph.
4. When you close the ROC-AUC graph, another python file pops up with the Precion-Recall graph.
5. Once that is closed, the terminal has finished executing and is ready to be ran again.

To run the Neural Network **without conservation scores**:

1. Open `genemirnasequence/neuralnetwork.py` in VS Code.
2. Click the **"Run Python File"** button.

> ⚠️ **Important:** Make sure the path to the dataset (`Balanced_dataset.tsv`) is correct in your script.  
> If you get a "file not found" error, adjust the relative or absolute path accordingly based on where you're running the script from.
> Running time may vary, with SVM models typically taking longer. Please be patient and wait until the program completes execution.

Terminal Output Description:
The terminal prints a detailed count of all 256 possible 4-mer frequencies for both gene and ncRNA sequences.

Prints the shape of:
Gene k-mers
ncRNA k-mers
phyloP scores
phastCons scores
Final feature matrix X (combined)

Displays:
First 10 values of the feature matrix
Last two conservation features
Column-wise means
First 10 labels and unique classes

Splits the dataset (80% training, 20% testing).

Trains the model and shows cross-validation performance

Saves and reloads the model, evaluates on test data

Terminal outputs metrics and 2 phyton files are generated thisplaying the ROC-AUC graph and the Precision Recall graph.
