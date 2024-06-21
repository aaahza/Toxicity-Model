# Toxicity Detection Model

## Project Overview

This project involves building a machine learning model to detect toxicity in text comments. The model processes comments and predicts the presence of various types of toxicity, including toxic, severe toxic, obscene, threat, insult, and identity hate. The dataset used for training and evaluating the model is sourced from a CSV file stored on Google Drive.

## Key Features

- **Data Import and Preprocessing:** The dataset is loaded from Google Drive and preprocessed using TensorFlow's TextVectorization layer to convert text into a format suitable for training.
- **Model Architecture:** The model is a sequential neural network consisting of an embedding layer, a bidirectional LSTM layer, and multiple dense layers.
- **Training and Evaluation:** The model is trained using a training dataset, and its performance is validated using a validation dataset. Various metrics such as precision, recall, and categorical accuracy are used for evaluation.
- **Deployment:** The trained model is deployed using Gradio, providing an interactive interface for predicting the toxicity of new comments.

## Model Architecture

The model is built using TensorFlow and Keras and includes the following layers:

1. **Embedding Layer:** Converts the input text into dense vectors of fixed size.
2. **Bidirectional LSTM Layer:** Captures dependencies in the text data from both directions, improving the model's understanding of the context.
3. **Dense Layers:** Three dense layers with ReLU activation to learn complex representations of the input text.
4. **Output Layer:** A dense layer with sigmoid activation that outputs six probabilities, one for each type of toxicity.

## Performance

The model is trained for 10 epochs, showing a decreasing loss trend and improving validation loss over epochs. This indicates that the model is learning and generalizing well on the validation data. The final model is evaluated using precision, recall, and categorical accuracy to ensure its effectiveness in detecting different types of toxicity.

## Deployment

The model is deployed using Gradio, which provides an easy-to-use web interface. Users can input text comments, and the model predicts the likelihood of each type of toxicity. This interactive deployment makes the model accessible and useful for real-world applications, such as moderating online communities.

## Conclusion

This project demonstrates a complete pipeline from data preprocessing, model building, training, evaluation, and deployment for toxicity detection in comments. The model's architecture and deployment strategy ensure it is both effective and user-friendly, making it a valuable tool for identifying and managing toxic content online.
