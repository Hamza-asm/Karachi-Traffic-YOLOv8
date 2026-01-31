# 🛺 Karachi-Traffic-Vision: Detecting Rickshaws & Suzukis with AI

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![YOLOv8](https://img.shields.io/badge/Model-YOLOv8m-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📄 Project Overview
This project addresses the challenge of traffic monitoring in developing countries like Pakistan, where standard AI models fail to recognize unique local vehicles.

Using **YOLOv8m**, I developed a real-time detection system capable of identifying 8 distinct vehicle classes, specifically targeting region-specific types like **Rickshaws** and **Suzuki** that are often missed by global datasets.

## 🎯 Key Features
* **Custom Dataset:** Manually collected and annotated data from real-world local traffic scenes.
* **Localized Classes:** Detects `Rickshaw`, `Suzuki`,`Cart` , alongside standard `Car`, `Bus`, `Truck`, and `Bike`.
* **Real-Time Analysis:** Built on the YOLOv8m architecture for a balance of speed and accuracy.

## 📊 Results & Visualizations
The model achieved an overall **mAP@0.5 of 0.542**.

### ✅ Success Stories
The system excelled at detecting distinctive local vehicles:
* **Rickshaws:** Achieved **87.6% accuracy**, proving the model successfully learned this unique geometry.
* **Bikes:** Strong detection with **70.5% accuracy**.

### 📉 Challenges
* **Suzuki vs. Van:** The model struggled to distinguish `Suzuki` from standard `Vans` due to their similar boxy silhouettes.

### 1. Performance Metrics
| Precision-Recall Curve | Confusion Matrix |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/db543e6f-91a5-444d-abdd-04bb2ffcb993" alt="BoxPR_curve" width="100%"/> | <img src="https://github.com/user-attachments/assets/9bfe473f-9546-4afc-a65f-f9251f12f3c5" alt="confusion_matrix" width="100%"/> |

*Figure 1: Quantitative Analysis. The PR Curve (Left) demonstrates high accuracy for Rickshaws (Purple line), while the Confusion Matrix (Right) highlights the specific misclassification between Suzukis and standard Vans.*

### 2. Visual Detection (Ground Truth vs. Predictions)
Below is a sample batch from the validation set showing the model's actual bounding box predictions.

![val_batch0_pred](https://github.com/user-attachments/assets/5e5fffb0-6753-4e51-afae-23d4134a806e)

*Figure 2: Real-world detection results. Note the correct identification of Rickshaws and Bikes in complex traffic.*

## 🛠️ Tech Stack
* **Language:** Python
* **Framework:** Ultralytics YOLOv8
* **Environment:** Google Colab (GPU accelerated)
* **Annotation:** Roboflow / LabelImg

## 🔮 Future Work
* **Hard Negative Mining:** To fix the confusion between Suzuki Bolans and Cars.
* **Larger Dataset:** Expanding the dataset to include night-time traffic conditions.

## 📝 Author
**Hamza Ali Khan** Final Year BSCS Student, Hamdard University.
