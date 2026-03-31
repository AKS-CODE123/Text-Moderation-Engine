

### Project: Text Moderation Engine

The sheer amount of user-generated content online today makes manual moderation basically impossible. You can't scale a team of humans to read every single comment being posted 24/7. Most platforms still use basic word-filters, but those are easy to bypass and they don't understand context—like, they might flag a word that isn’t actually being used in a toxic way.

I built this **Text Moderation Engine** to solve that using deep learning. Instead of just looking for "bad words," the model analyzes the intent and context of a sentence to classify it into different types of toxicity automatically.

---

### Key Objectives

The main focus of this project was to move away from rigid, rule-based systems and build something more fluid:

*   **Multi-label Classification:** I wanted the model to be able to tag a single comment with multiple labels (like "toxic," "threat," or "insult") at the same time.
*   **Text Vectorization:** I used a TextVectorization layer to handle the preprocessing—stripping punctuation, lowercasing, and mapping words to integers so the neural network can process them.
*   **Bidirectional LSTM:** This is the core of the model. Standard RNNs only read in one direction, but a Bi-LSTM reads the sentence both ways. This is huge for moderation because the meaning of a word usually depends on what comes after it, not just what came before.
*   **Vocabulary Persistence:** A common mistake is using a different vocab for training and testing. I made sure to save the specific vocabulary from the training phase so the model stays consistent when it's making real-world predictions.

---

### Scope & Limits

For now, the engine is built specifically for English text. It’s strictly for text-based comments, so it doesn't handle images or audio files. Since it’s trained on a static dataset, its "knowledge" of toxicity is based on what’s in that data—it’s great at catching standard abuse, but it’s always going to be a work in progress when it comes to brand-new slang or super subtle sarcasm.

---

### Final Outcomes

By the end of the project, I had a working pipeline that takes a raw string and returns a set of toxicity scores. 

*   Successfully trained a model that can flag harmful content in real-time.
*   Implemented a multi-label output system that gives a nuanced breakdown of the text.
*   Created a consistent training-to-prediction workflow that doesn't break when you feed it new data.

Basically, it's a way to automate the "dirty work" of content moderation, making it a lot easier to maintain a decent environment in online communities without needing a massive team of moderators.
