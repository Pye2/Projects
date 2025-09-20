# UQU Chatbot Assistant

This project focuses on an intelligent chatbot that assists students
at Umm Al-Qura University by answering frequently asked questions regarding
admissions, academic policies, and university procedures, The dataset comprises user
queries in Arabic and English, making the classification task more complex due to
linguistic variability and contextual differences, The main challenge in designing
this chatbot lies in accurately classifying diverse user intents while ensuring high
response accuracy, To address this, various NLP techniques, including text
preprocessing, intent classification, and response generation, were employed, The
chatbot was developed using machine learning-based models to ensure efficient query
handling and seamless interaction with users.

# Methodology
The chatbot development process involved several key steps aimed at
building a deep learning-based model using LSTM and GRU :
## 1. Building the LSTM Model :
 - A (Sequential) model was used, including an (Embedding) layer to
accommodate the vocabulary size.
 - Two LSTM layers were added, the first containing 128 units with
(return_sequences = True) for sequential learning.
 - A (Dropout) layer with 20% probability was applied to prevent
overfitting and enhance generalization.
 - A fully connected (Dense) layer with 64 units and a (relu) activation
function was included.
 - The output layer, a (Dense) layer , utilized (softmax) activation for
intent classification .
## 2. Building the GRU Model :
 - A (Sequential) model was used, including an (Embedding) layer to
handle the discovered vocabulary.
 - Two GRU layers were added, the first containing 128 units with
(return_sequences = True) to allow sequential learning.
 - (Dropout) layers with a 20% probability were included to improve
generalization and reduce overfitting.
 - A fully connected (Dense) layer with 64 units and a (relu) activation
function was utilized.
 - The output layer consisted of a (Dense) layer using (softmax) activation
to classify user intents.



# Data Preprocessing :
 - Text was converted into numerical sequences using (Tokenizer).
 - (pad sequences) was applied to ensure uniform sequence length.
 - (Label Encoder) was used to transform categorical labels into numeric
form, followed by (one-hot encoding).
# 4. Model Compilation and Training :
 - The models were compiled using (categorical cross entropy) as the
loss function, (adam) as the optimizer, and (accuracy) as the evaluation
metric.
 - Both models were trained for 35 epochs with a batch size of 8 .
# 5. Saving the Model and Preprocessing Tools :
 - The trained models were saved as (chatbot_lstm_model.h5) and
(chatbot_gru_model.h5).
 - The (Tokenizer) was saved in JSON format for later use.
 - (Label Encoder) was stored using (pickle) for easy retrieval
