# Abstract
In the field of medical imaging, the classification and diagnosis of lung diseases using chest X-ray images have been a crucial area of applications in healthcare, We trained multiple models on five lung disease classes which is bacterial pneumonia ,coronavirus ,Normal ,tuberculosis , and viral pneumonia , including a custom-built CNN, a ResNet50-based transfer learning model, and a DenseNet-121 , we used ResNet50 and DenseNet-121models using PyTorch especially to enhance computation performance to training data, instead of waiting 90mintute to train the model using tensorflow library,  time consuming has become 8minutage (approximately) to train the model , we achieved 95.42% and 91.16% accuracy for custom CNN models ,where ResNet50 achieved 92% and DensNet121 91.82%,  The dataset consists of 6,054 training images, 2,016 validation images, and 2,025 test images, categorized into five disease classes,
Data preprocessing included image resizing (224×224 pixels), normalization, and augmentation to improve generalization.
The models were trained using categorical cross-entropy loss with different optimization techniques, including Adam optimizer, learning rate schedulers, and early stopping mechanisms.

# results:

-Custom CNN Model number 1 achieved 95,42% Validation accuracy, showing signs of overfitting after several epochs.
-Custom CNN Model number 2 achieved 91.16% Validation accuracy, showing the gap between Train loss and validation loss decreased.
-ResNet50 (PyTorch)  Transfer Learning Model performed better, achieving 92% validation accuracy and 86% test accuracy.
-DenseNet-121 (PyTorch) achieved 91.82% validation accuracy and 90.72% test accuracy, making it the most balanced model in terms of generalization.

# Methodology 
## Dataset
The dataset was structured into training, validation, and test sets, comprising :6,054 training images, 2,016 validation images ,and2,025 test images, Each image belongs to one of the five lung disease classes categorized into five disease classes:
-1	Bacterial Pneumonia
-2	Coronavirus Disease
-3	Normal (Healthy Lung)
-4	Tuberculosis
-5	Viral Pneumonia
## Data Preprocessing
Image resizing: All images were resized to 224×224 pixels.
Normalization: Pixel values were scaled to the [0,1] range to ensure uniformity.
Data Augmentation: Techniques such as random rotation, flipping, and rescaling were applied to reduce overfitting.




1. CNN Model number 1
Three convolutional layers with ReLU activation and max pooling.
Fully connected layers with dropout (0.6) for regularization.
Softmax output layer for multi-class classification.
Optimizer: Adam
Loss function: Categorical Cross-Entropy
Trained for 15 epochs

2. CNN Model number 2
Model Architecture
CNN was built using TensorFlow and Keras, comprising:
Three convolutional layers (32, 64, 128 filters) with ReLU activation.
Max-pooling layers after each convolution.
Flattening and fully connected layers with dropout (0.5) to prevent overfitting.
Softmax output layer with five neurons for multi-class classification.

3. ResNet50 Transfer Learning Model
Pretrained ResNet50 model on ImageNet
Unfrozen last 20 layers for additional training
Added custom fully connected layers for final classification
ReduceLROnPlateau learning rate adjustment
Trained using Adam optimizer for 50 epochs

4. DenseNet-121 Model (PyTorch Implementation)
DenseNet-121 pretrained on ImageNet, modified for lung disease classification.
Implemented dynamic learning rate scheduling (CosineAnnealingLR)
Early stopping to prevent overfitting
Trained for 30 epochs with batch normalization

# Evaluation Metrics
•	Training and validation accuracy/loss curves
•	Confusion matrices
•	Classification reports (precision, recall, F1-score)
•	Test accuracy on unseen data






# Discussion

The results obtained from the different models indicate that deep learning approaches, particularly transfer learning, significantly enhance lung disease classification accuracy, The ResNet50 and DenseNet-121 models demonstrated superior generalization capabilities compared to the custom CNN model, This improvement can be attributed to the transfer learning strategy, which leverages features extracted from large scale datasets such as ImageNet, However, despite these successes, the research also encountered challenges related to overfitting, dataset bias, and computational constraints.
One of the key aspects observed was the performance consistency across different architectures Overfitting was a challenge in the custom CNN model, requiring additional regularization techniques, The custom CNN, while effective in learning patterns, struggled with generalization, On the other hand, ResNet50 and DenseNet-121 were able to achieve higher validation accuracies, indicating that pretrained models provide a better foundation for feature extraction in medical imaging tasks.
There are Potential Improvements To enhance the models performance, several strategies should be explored. Implementing advanced regularization techniques, such as dropout, batch normalization, and L1/L2 regularization, can help mitigate overfitting by ensuring better generalization, Additionally, integrating hybrid models that combine CNNs with attention mechanisms, such as Vision Transformers, may provide improved feature extraction by focusing on the most relevant parts of the lung images.



