# Wine Review Classification Model

This project is a wine review classification model designed to classify wine reviews as high-quality or low-quality based on textual descriptions. Using a Recurrent Neural Network (RNN) with LSTM layers, the model analyzes wine reviews to predict wine quality. This project is built with TensorFlow and TensorFlow Hub, utilizing pre-trained embeddings and custom text preprocessing.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model Architecture](#model-architecture)
4. [Installation](#installation)
5. [Results](#results)
6. [Future Enhancements](#future-enhancements)

## Project Overview

The Wine Review Classification Model uses Natural Language Processing (NLP) techniques to classify wine reviews as high-quality or low-quality based on a score threshold. The model processes wine descriptions, leveraging a TensorFlow Hub embedding layer and a Recurrent Neural Network (RNN) with LSTM layers to learn meaningful patterns from text data.

## Dataset

- **Source**: The dataset consists of wine reviews with columns for country, description, points, price, variety, and winery.
- **Preprocessing**: Reviews with missing descriptions or points were removed. Points were converted to binary labels, with a score above 90 classified as "high quality" and below 90 as "low quality."

## Model Architecture

The model uses the following architecture:
1. **Text Embedding**: A pre-trained text embedding from TensorFlow Hub (`nnlm-en-dim50`) converts text to a numerical format.
2. **LSTM Layers**: LSTM (Long Short-Term Memory) layers capture sequential patterns in the text, making them ideal for handling the nuances of language.
3. **Dense Layers**: Two dense layers with dropout regularization help in fine-tuning the model's performance.
4. **Output Layer**: A sigmoid-activated output layer provides binary classification (high-quality or low-quality).

### Hyperparameters
- **Learning Rate**: 0.001
- **Batch Size**: 1024
- **Epochs**: 5

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/wine-review-classification.git
   cd wine-review-classification

## Results
The model achieved 84% accuracy on test data, demonstrating effective classification between high-quality and low-quality wine reviews.

## Future Enhancements

- **Fine-Tuning Embeddings**: Experiment with other embedding models from TensorFlow Hub for improved language understanding.
- **Hyperparameter Tuning**: Adjust learning rate, batch size, and LSTM units for optimal performance.
- **Multi-Class Classification**: Extend the model to predict specific quality scores instead of binary classification.

