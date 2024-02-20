### Project Overview:
The project aims to develop a credit card fraud detection system using Artificial Neural Networks (ANN).

### Dataset Description:
The dataset comprises credit card transactions made by European cardholders in September 2013. It spans two days and contains 492 frauds out of 284,807 transactions, making it highly unbalanced with frauds accounting for 0.172% of all transactions. The dataset includes only numerical input variables resulting from Principal Component Analysis (PCA). While features V1 to V28 represent principal components obtained from PCA, 'Time' and 'Amount' are original features. 'Time' denotes the seconds elapsed between each transaction and the first one in the dataset, while 'Amount' signifies the transaction amount. The 'Class' feature denotes fraud (1) or non-fraud (0).

### Handling Class Imbalance:
Due to the class imbalance ratio, accuracy is best measured using the Area Under the Precision-Recall Curve (AUPRC), as confusion matrix accuracy is not meaningful for unbalanced classification.

### Proposed Solution:
The proposed solution involves employing Artificial Neural Networks with varying numbers of hidden layers using the Keras library, enhancing model depth for improved training. Three Multi-Layer Perceptrons (MLPs) are constructed:

1. **Single Hidden Layer MLP:**
   - Consists of three layers: input, hidden, and output.
   - Input layer: 29 neurons, hidden layer: 65 neurons, output layer: one neuron.
   - Utilizes a custom activation function and sigmoid function in the output layer.
   - Dropout is introduced to address overfitting.

2. **Two Hidden Layers MLP:**
   - Includes four layers: input, two hidden, and output.
   - Input layer: 29 neurons, two hidden layers: 65 neurons each, output layer: one neuron.
   - Employs a custom activation function for one hidden layer and ReLU for the other.
   - Dropout is maintained due to observed overfitting.

3. **Three Hidden Layers MLP:**
   - Comprises five layers: input, three hidden, and output.
   - Input layer: 29 neurons, three hidden layers: 65 neurons each, output layer: one neuron.
   - Special activation function for one hidden layer, ReLU for the other two.
   - Dropout is retained for model regularization.

### Conclusion:
Implementing Artificial Neural Networks with varied hidden layers and activation functions, along with dropout regularization, enhances the model's ability to detect credit card fraud effectively.
