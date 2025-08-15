# DL\_Keras\_Model\_Subclassing — Custom Models with TensorFlow/Keras

---

## 1) Project Title

**Deep Learning with Keras Model Subclassing — Custom Architectures, Loss Functions, and Training Loops**

---

## 2) Problem Statement and Goal of Project

This project demonstrates **full customization of deep learning models** in TensorFlow/Keras using the **Model Subclassing API**.
The aim is to:

* Build custom model architectures by directly subclassing `tf.keras.Model`.
* Implement **custom layers**, **user-defined loss functions**, and **forward passes** with complete flexibility.
* Showcase advanced training workflows and model control beyond the standard Sequential/Functional APIs.

---

## 3) Solution Approach

The notebook implements:

1. **Custom Model Definition**

   * Inherits from `tf.keras.Model`.
   * Defines layers inside `__init__` and the forward computation in `call(...)`.
2. **Custom Loss Function**

   * Implemented directly in Python with TensorFlow operations.
3. **Flexible Training**

   * Uses the Keras `.compile()` / `.fit()` workflow but allows custom training logic if needed.
4. **MNIST Classification Example**

   * Uses TFDS to load, normalize, and one-hot encode the dataset.
   * Trains the custom model on 28×28 grayscale images.
5. **Model Diagram**

   * Created using `keras.utils.plot_model(...)` to visualize the architecture.

This approach gives **full control** over architecture design and training behavior, enabling experimentation that’s difficult with high-level APIs.

---

## 4) Technologies & Libraries

* **Python**
* **TensorFlow / Keras**
* **TensorFlow Datasets (TFDS)**
* **NumPy**
* **pydot / graphviz** (for architecture visualization)

---

## 5) Description about Dataset

* **MNIST** (from TFDS)

  * Handwritten digits (0–9).
  * Input shape: `(28, 28, 1)` grayscale images.
  * Labels: One-hot encoded with depth = 10.
* Data processing steps in code:

  * Normalization (`tf.divide(..., 255.0)`)
  * One-hot encoding (`tf.one_hot(..., depth=10)`)
  * Shuffling, batching, and prefetching with `tf.data`.

---

## 6) Installation & Execution Guide

**Prerequisites**

* Python 3.x
* TensorFlow (GPU optional, but recommended)

**Install (pip)**

```bash
pip install tensorflow tensorflow-datasets numpy pydot graphviz
```

> On some systems you must also install Graphviz binaries:
> `sudo apt-get install graphviz`

**Run**

1. Open `model_subclassing_me.ipynb` in Jupyter/VS Code.
2. Execute cells sequentially.
3. The notebook will:

   * Download MNIST automatically on first run.
   * Train the custom model.
   * Save model diagrams (if the diagram cell is executed).

---

## 7) Key Results / Performance

* **Not provided.**
  The notebook demonstrates the **mechanics** of model subclassing and training rather than optimizing for maximum accuracy.

---

## 8) Screenshots / Sample Output

* **Not provided in repository.**
  Running the diagram cell will save a `.png` visualization of the custom model locally.

---

## 9) Additional Learnings / Reflections

* **Subclassing `tf.keras.Model`** offers **complete freedom** in architecture and training control.
* This flexibility is useful for **research, custom loss integration, and non-standard forward passes**.
* The project reinforces understanding of **TensorFlow low-level operations** combined with Keras high-level utilities.
* Lower performance in some runs is **intentional** to focus on the API’s mechanics, not leaderboard scores.

---

## 👤 Author

**Mehran Asgari**
**Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
**GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.

---

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

---

اگر بخوای میتونم همین README رو هم با فرمت و نام‌گذاری هماهنگ با بقیه ریپازیتوری‌هات (مثل `DL_TensorFlow_LowLevelAPI_CustomModel`) بازنویسی کنم تا گیت‌هابت کاملاً یکدست بشه.
آیا این کار رو انجام بدم؟
