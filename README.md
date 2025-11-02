
---

## 🫁 Pneumonia Detection from Chest X-Ray Images using Transfer Learning

This project explores how deep learning models can assist in detecting **pneumonia from chest X-ray scans**.
It was developed as a **learning & research-grade experiment** to understand medical imaging with CNNs, not as a final clinical tool.

Our focus:

* ✅ Understanding transfer learning on medical images
* ✅ Comparing multiple CNN architectures
* ✅ Observing class imbalance effects
* ✅ Using **Grad-CAM** for explainability
* ✅ Practicing ethical ML — no exaggerated claims

---

## 📦 Dataset

**Chest X-Ray (Pneumonia) dataset**
Classes: `NORMAL` vs `PNEUMONIA`

Folder-split dataset ~ train / test / val

> This dataset is commonly used in research papers for pneumonia classification experiments.

---

## 🧠 Models Used & Why

We experimented with 4 well-known CNN architectures:

| Model           | Reason for Choice                                |
| --------------- | ------------------------------------------------ |
| **DenseNet121** | Strong performance in medical imaging literature |
| ResNet50        | Classic baseline for deep feature extraction     |
| EfficientNetB0  | Parameter-efficient modern architecture          |
| MobileNetV2     | Lightweight model for low-resource inference     |

Each started from **ImageNet weights** → fine-tuned on chest X-rays.

---

## 📊 Key Observations

* **DenseNet121 performed best** after fine-tuning
* Increasing epochs improved generalization
* Class imbalance affected early results
* Threshold tuning (~0.69) improved decision boundary
* Augmentation helped reduce overfitting

> Final results are promising but **not production / clinical ready**
> This is part of a learning journey.

---

## 📈 Evaluation & What We Learned

We calculated:

* ✅ Accuracy
* ✅ Precision, Recall, F1
* ✅ Confusion Matrix
* ✅ ROC-AUC
* ✅ Grad-CAM visualizations

**Why this matters:**
Medical models must be interpretable — not just accurate.
Grad-CAM helped verify model focus on lung regions (and spot mistakes).

---

## 🔍 Explainability (Grad-CAM)

Heatmaps were generated to visualize what the model looks at.

| Example Output                            |
| ----------------------------------------- |
| *(grad-cam images go here once uploaded)* |

Some images showed correct lung attention ✅
Some highlighted irrelevant areas ❌

> This reflection was an important learning outcome.

---

## 📁 Project Structure

```
📂 project
│── notebook.ipynb  ~ full training & testing
│── models/         ~ saved .h5 models
│── results/        ~ CM, ROC, Grad-CAM
│── README.md       ~ (this file)
```

---

## ⚙️ Workflow in Colab

1️⃣ Load and inspect dataset
2️⃣ Create generators + augmentation
3️⃣ Train multiple CNNs
4️⃣ Compare metrics
5️⃣ Tune threshold
6️⃣ Generate Grad-CAM maps
7️⃣ Save best model

Each stage helped understand ML lifecycle in medical imaging.

---

## 🪫 Limitations & Ethical Note

* Small validation subset
* Short training due to Colab compute limits
* No external validation data
* Not medically approved

⚠️ **This project does not diagnose disease.**
It is only an academic exercise.

---

## 🎯 What This Project Achieved

* Built practical intuition for medical deep learning
* Gained hands-on experience in transfer learning
* Understood model interpretability importance
* Learned responsible reporting of results

---

## 🙋‍♀️ Author Note

This project was created as part of my journey in **AI & Data Science**, focusing on healthcare applications and ethical ML.

Feel free to explore, learn, and suggest improvements!

If you found this useful, ⭐ the repo 🌟

---

