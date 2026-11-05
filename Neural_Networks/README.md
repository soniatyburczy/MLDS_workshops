# Neural Networks Workshop
## Recognising Sea Creature Doodles 🦈🐬🐙🦀

In this workshop, you'll teach a **neural network** to tell apart doodles of four sea animals (shark, dolphin, octopus, and crab), trained on 40,000 real drawings from Google's **Quick, Draw!** game. Along the way, you'll see how an image becomes a row of numbers, why logistic regression is really just a neural network with no hidden layers, and why a bigger network isn't always a better one. At the end, you'll draw your own doodles and watch the model guess them live. Everything runs **directly in your browser** using [Google Colab](https://colab.research.google.com/).

---

## Topics Covered

1. **Loading & Looking at the Data**
   - Downloading the Quick, Draw! `.npy` files and sampling 10,000 doodles per animal
   - Checking shapes, pixel values, and class balance with `np.bincount()`
   - Reshaping a 784-number row back into a 28 × 28 image with `plt.imshow()`
   - Finding the **baseline** (random guessing gets 25%)

2. **Preparing the Data**
   - Scaling pixels from 0–255 to 0–1
   - Stratified train/test split
   - Train vs. **validation** vs. test: which set is used for what

3. **Baseline: Logistic Regression in Keras**
   - Building a model with `keras.Sequential()` and a single `Dense` softmax layer
   - Counting parameters with `.summary()`
   - Choosing an optimizer and loss with `.compile()`, and training with `.fit()`
   - Visualizing the learned weights as one "template" per animal

4. **Adding Hidden Layers**
   - Building a 784 → 128 → 64 → 4 network with **ReLU**
   - Plotting train vs. validation accuracy across epochs
   - Spotting **overfitting** in the training curves

5. **How Many Layers?**
   - Looping over network sizes and comparing train vs. validation accuracy
   - Weighing accuracy against model size

6. **Evaluating on the Test Set**
   - Turning softmax probabilities into predictions with `argmax()`
   - Comparing random guessing, logistic regression, and the neural network
   - The confusion matrix: which animals get mixed up?
   - Looking at the doodles the model gets wrong

7. **Draw Your Own!**
   - A live drawing app built with **Gradio** that runs the model on your doodles
   - Seeing what the model "sees" once your drawing is shrunk to 28 × 28
   - Why softmax always picks an animal, even when you draw a house

---

## Workshop Format

- **Live Coding in Google Colab**: no installation required.
- **✏️ cells** where you write the code yourself.
- **💬 cells** where you stop and discuss.
- **👀 cells** for notes.
- **Challenges** at the end if you want to keep going (early stopping, dropout, a 5th animal, and a CNN).
- **Solutions notebook** provided so you can check your work after the workshop.

---

## Files

| File | What it is |
|---|---|
| `neural_networks.ipynb` | The workshop notebook (student version) |
| `neural_networks_solutions.ipynb` | Completed notebook with solutions |

> The dataset downloads directly from Google inside the notebook, so there's no file to upload.

---

## Getting Started with Google Colab

1. Open **Google Colab**: [https://colab.research.google.com/](https://colab.research.google.com/)
2. Sign in with your Google account.
3. Click **File → Upload notebook** and select `neural_networks.ipynb`.
4. Click into the first code cell and press **Shift + Enter** to run it. Keep running cells **in order** as you go.

> **Note:** The data cell downloads one file per animal (each has over 100,000 drawings), so it may take a minute the first time. If you come back later, re-run the cells from the top, since variables are cleared when the session ends.

> **Drawing app:** The last section prints a public `...gradio.live` link. Open it on your phone to draw with your finger! The link stops working once your Colab session ends.

---

## About the Dataset

The [**Quick, Draw!** dataset](https://github.com/googlecreativelab/quickdraw-dataset) comes from Google Creative Lab and contains millions of doodles drawn by players of the [Quick, Draw!](https://quickdraw.withgoogle.com/) game, where people had 20 seconds to sketch a prompt. We use the preprocessed **numpy bitmap** version, where each doodle is a 28 × 28 grayscale image (784 numbers, each 0–255 for how much ink is there), and keep 10,000 random doodles each of `shark`, `dolphin`, `octopus`, and `crab`. The dataset is available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) license.

---

## After the Workshop

By the end of this workshop, you will:
- Understand how an image is represented as numbers a model can learn from.
- Be able to build, compile, and train a feed-forward neural network in Keras.
- See how logistic regression and neural networks are related.
- Know how to use a validation set to choose a model size and spot overfitting.
- Be able to evaluate a multi-class classifier with a baseline and a confusion matrix.
- Know why a confident prediction isn't necessarily a correct one.
