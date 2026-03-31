# Text-Moderation Engine (Deep Learning)

This is a deep learning based NLP project that tries to detect toxic comments from text input.
Given a sentence, the model predicts whether it falls into categories like insult, threat, obscene language, identity hate, etc.

I built this mainly to understand how an actual NLP pipeline works in practice — not just theory, but the full flow from raw text to model training and predictions.

---

## Features

* Can identify different types of toxic content
* Uses a Bidirectional LSTM to understand context from both sides
* Covers the full pipeline (preprocessing → training → prediction)
* Outputs probabilities instead of just yes/no labels

---

## How it works

The overall idea is pretty straightforward:

First, the text is converted into numbers using a `TextVectorization` layer.
After that, the processed sequence is passed into a Bidirectional LSTM model.

Since LSTMs work well with sequential data, the model can capture how words relate to each other in a sentence (not just individually).

Finally, the model outputs probability scores for each toxicity category.

---

## Tech stack

* Python
* TensorFlow / Keras
* Pandas

---

## Project structure

```
Toxicity-Detector/
│
├── Train.py             # trains the model
├── Predict.py           # runs predictions using saved model
├── Toxicity_Detector.h5 # trained model file
```

---

## Dataset

The dataset used here is around 66 MB, so it’s not included in the repo.

To run this project:

1. Download the dataset from Kaggle
   https://www.kaggle.com/datasets/julian3833/jigsaw-toxic-comment-classification-challenge

2. Put the dataset inside the project folder

3. If needed, update the file path in the code

4. Train the model

```
python Train.py
```

5. Then test it

```
python Predict.py
```

---

## Why I made this

Mostly to get hands-on experience with:

* converting text into numerical form
* understanding how LSTMs actually process sequences
* making sure training and prediction pipelines stay consistent

---

## Future improvements

* Try improving accuracy (maybe different architectures)
* Reduce training time
* Add a simple UI so it’s easier to test

---

## Contributing

If you want to improve anything or experiment with it, feel free to fork and make changes.

---

## Acknowledgment

Dataset taken from Kaggle’s Toxic Comment Classification Challenge.

