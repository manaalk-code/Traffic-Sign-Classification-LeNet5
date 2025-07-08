# Traffic Sign Classification using LeNet-5 based Deep Neural Network

This system was awarded **1st Position at the COMSATS EXPO 2024**.
A deep learning-based real-time traffic sign classification system built and deployed using a custom Pakistani dataset and the LeNet-5 architecture.

### Background 

This is my Final Year Project at COMSATS University, where I developed and deployed a deep learning model for **Pakistani traffic sign classification** using the LeNet-5 architecture. 
This project was inspired by the well-known GTSRB (German Traffic Sign Recognition Benchmark), which is widely used in traffic sign classification research.
Initially, we used this dataset to validate our CNN architecture and training pipeline. Our model, based on LeNet-5, achieved a strong **97.95% accuracy** on the GTSRB test set, confirming our approach.

However, our actual objective was to develop a system tailored for **Pakistani traffic signs**, where no large, standardized public dataset was available.

---

### 🇵🇰 Creation of the Pakistani Traffic Sign Dataset

Due to the unavailability of a local dataset, we created a new dataset from scratch. Here’s how:

- We **selected 12 traffic sign classes** from GTSRB that closely resembled signs on Pakistani roads for consistency and comparability.
- Images were captured using a **standard mobile phone camera**, with 40–50 images per class.
- We introduced **real-world variability** using:
  - Flipping
  - Brightness variation
  - Blur simulation
  - Cropping and rotations
- Final dataset included approximately **10,000 images**, ensuring robust training conditions.

---

###  Preprocessing & Model Architecture

To align with LeNet-5 requirements and handle image variability:
- All images were **resized to 32×32**
- **Grayscale conversion** reduced data complexity
- **Histogram equalization** improved contrast
- The model architecture included:
  - Two `Conv2D` layers with `AveragePooling`
  - Fully connected layers with 120, 84, and 12 output neurons
  - Softmax activation for classification

---

### ⚠️ Challenges Faced

While adapting the model from GTSRB to Pakistani signs, we encountered multiple challenges:

- **Resolution Mismatch**  
  Pakistani images were high-res, while GTSRB was low-res — causing severe accuracy drops initially.
- **Dataset Variability**  
  Unlike German signs, Pakistani signs lacked visual standardization — adding unpredictability.
- **Poor Initial Accuracy**  
  Accuracy was under 50% on early versions of the local dataset.
- **Over-Aggressive Preprocessing**  
  Some preprocessing methods worsened results instead of improving them.

---

### SOLUTIONS 

To overcome these issues:

-  **downscaled Pakistani images** to match GTSRB resolution
- Introduced extensive **data augmentation**:
  - Brightness/contrast tuning
  - Simulated blurring
  - Random flips, crops, and rotations
- Expanded the dataset to improve model generalization
- Tuned preprocessing steps to retain features critical for classification

As a result, successfully improved accuracy to **91%** on the Pakistani dataset.

---

###  Real-Time Deployment

The final model was deployed on a **Raspberry Pi 3 using TensorFlow Lite**, enabling real-time classification of traffic signs using a live camera feed.

The model was able to predict most signs accurately, but we noted occasional confusion between visually similar signs (e.g. danger vs signal ahead) — which is typical in real-world scenarios and valuable feedback for future refinement.

---

###  Project Structure

| File/Folder                | Purpose |
|---------------------------|---------|
| `Pakistani_TrafficSigns.ipynb` | Main notebook for model training, evaluation |
| `GTSRB_trafficSigns.ipynb`    | German dataset version (baseline) |
| `sample_dataset/`             | Small sample of 12-class dataset |
| `results/`                    | Accuracy graphs, confusion matrix, class overview |
| `individual_predictions/`     | Single image predictions and confidence outputs |
| `preprocessing/`              | Before vs after sample |
| `requirements.txt`            | Required Python packages |
| `LICENSE`                     | MIT License |

---


###  📁 Dataset Access
A **sample dataset** is included.  
For full Pakistani dataset access (12 classes), contact:

📧 **manaalkhurram90@gmail.com**

---

###  How to Run

1. Clone this repo or download ZIP  
2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open `Pakistani_TrafficSigns.ipynb`  
4. Run all cells in sequence

---

##  Author
**Manaal Khurram**  
Electronics Engineer – COMSATS University Islamabad   
[GitHub](https://github.com/manaalk-code)
[LinkedIn](https://www.linkedin.com/in/manaal-khurram-07a016308)

---

## License
This project is licensed under the MIT License.
