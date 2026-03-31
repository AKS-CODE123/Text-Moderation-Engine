# Text-Moderation-Engine (Deep Learning)

This project is a simple deep learning model that tries to detect toxic comments from text input.  
You can give it a sentence, and it will predict whether it falls into categories like insult, threat, obscene, etc.

I mainly built this project to get a better understanding of how real NLP pipelines work — starting from raw text all the way to predictions.

---

## How it works

The workflow is pretty straightforward:

- First, the input text is converted into numbers using a TextVectorization layer  
- Then those vectors are passed into a Bidirectional LSTM model  
- Finally, the model outputs probabilities for different toxicity labels  

---

## Tech stack

- Python  
- TensorFlow / Keras  
- Pandas  

---

## Project structure

- `Train.py` → used to train the model  
- `Predict.py` → loads the trained model and runs predictions  
- `Toxicity_Detector.h5` → saved model file  

---

## Dataset

The dataset is around 66 MB, so it’s not included in the repo.

To run this project:

1. Download the dataset from Kaggle:  
   https://www.kaggle.com/datasets/julian3833/jigsaw-toxic-comment-classification-challenge  
2. Put the dataset in the project folder  
3. Update file paths in the code if needed  
4. Run `Train.py` to train the model  
5. Use `Predict.py` to check predictions  

---

## Why I made this

Mostly to understand a few things better:

- how text is converted into numerical format  
- how LSTMs deal with sequential data  
- and how to keep things consistent between training and prediction  

---

## Things I might improve later

- Try to improve accuracy  
- Make training faster  
- Maybe add a small UI so it's easier to test inputs  
