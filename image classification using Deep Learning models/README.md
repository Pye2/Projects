# image classification using Deep Learning models Project

In this project, I implemented several deep learning models to classify images of cars and planes, leveraging Convolutional Neural Networks (CNN), Recurrent Neural Networks (RNN), and Fully Connected Neural Networks (FNN), This classification task is essential in the context of image recognition, providing insights into effective methods for distinguishing between visually similar objects, I used TensorFlow and Keras libraries for model creation and training, aiming to maximize classification accuracy while exploring model architecture impacts.


# Data Collection and Preprocessing 

The dataset consists of images categorized into two classes: cars and planes, I loaded and processed images from the specified directories, resizing them to 224x224 pixels, The images were normalized to enhance model training efficiency by scaling pixel values between 0 and 1, I split the data into training and validation sets, ensuring reliable evaluation of the models performance, This process involved converting the images to numpy arrays and reshaping them when necessary to fit specific model architectures, This preprocessing aimed to ensure consistency across CNN, RNN, and FNN models. 
# results from the CNN model: 
• Training Accuracy: 96.7% by the last epoch 
• Validation Accuracy: 88.9% by the last epoch 
• F1-Score: The CNN achieved an F1-score of approximately 0.89, reflecting 
balanced precision and recall between both classes. 
• Confusion Matrix: A good distribution of correctly classified images, with 
minor misclassifications, demonstrating robustness.
# results from the RNN model: 
• Training Accuracy: 84% at the final epoch 
• Validation Accuracy: 83.9% at the final epoch 
• F1-Score: Approximately 0.84, indicating a slight decline compared to the 
CNN model, but still showing reasonable accuracy for binary classification. 
• Confusion Matrix: Reasonable distribution of correct classifications, with 
some limitations in handling complex spatial dependencies.  
results from the FNN model: 
• Training Accuracy: 85.6% at the final epoch 
• Validation Accuracy: 83.4% at the final epoch 
• F1-Score: The FNN achieved an F1-score close to 0.83, reflecting satisfactory 
classification performance but slightly lower than the CNN. 
• Confusion Matrix: Performance indicated higher misclassifications for FNN 
due to limited spatial context, as each pixel was processed independently. 
# Model Evaluation and Comparison 
I compared the three models using metrics such as accuracy, precision, recall, and 
F1 score, The CNN model performed the best overall, likely due to its architectural 
advantage in capturing spatial patterns in image data, The RNN model, while novel in 
its application to images, performed slightly below the CNN due to the limitations in 
interpreting spatial hierarchies, The FNN, on the other hand, showed the least 
accuracy, emphasizing the importance of spatial processing layers for image data,
The Receiver Operating Characteristic (ROC) curve further demonstrated the CNN 
models superior performance, with Area Under the Curve (AUC) nearing 0.9, 
compared to 0.84 and 0.83 for the RNN and FNN, respectively, This analysis suggests 
that convolutional layers are more suitable for image classification tasks where 
spatial patterns are crucial.



Data Source: https://www.kaggle.com/datasets/aymanalzahrani7/cars-and-plans-pictures-dataset
