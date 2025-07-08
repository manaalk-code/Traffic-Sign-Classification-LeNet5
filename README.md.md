# Traffic Sign Classification using LeNet-5

This is my Final Year Project at COMSATS University, where I developed and deployed a deep learning model for **Pakistani traffic sign classification** using the LeNet-5 architecture.

---

## Highlights
- Built a **custom dataset** of 12 Pakistani traffic sign classes
- Applied preprocessing: Resizing, grayscale, histogram equalization, augmentation
- Achieved **91% accuracy** on our final trained model
- Trained first on **GTSRB dataset** (97.95% accuracy), then transferred to local dataset
- Deployed using **TensorFlow Lite** on **Raspberry Pi 3** for real-time classification
- Won **1st Position at COMSATS EXPO 2024**

---

## 🧠 Project Structure

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

## ⚠️ Known Challenges
- Signs with similar structure sometimes confused the model (e.g. Danger vs Traffic Signal Ahead)
- Accuracy improved significantly after augmentation and dataset expansion

---

## 📁 Dataset Access
A **sample dataset** is included.  
For full Pakistani dataset access (12 classes), contact:

📧 **manaalkhurram90@gmail.com**

---

## 🛠️ How to Run

1. Clone this repo or download ZIP  
2. Install dependencies:
```bash
pip install -r requirements.txt
3. Open `Pakistani_TrafficSigns.ipynb`  
4. Run all cells in sequence

---

##  Author
**Manaal Khurram**  
Electronics Engineer – COMSATS University Islamabad   
[GitHub](https://github.com/manaalk-code)
[LinkedIn](www.linkedin.com/in/manaal-khurram-07a016308)

---

## License
This project is licensed under the MIT License.
