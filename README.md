# Sepsis Optimal Treatment Plan Using GAN and Reinforcement Learning

This project presents an end-to-end pipeline for recommending optimal treatment strategies for ICU patients with sepsis. It combines advanced data preprocessing, GAN-based class balancing, traditional machine learning models, and reinforcement learning (RL) to simulate and refine treatment decisions.

---

## 🔬 Project Overview

- Developed a clinical decision support system for sepsis cases.
- Addressed severe class imbalance with GAN-generated synthetic samples.
- Evaluated multiple ML classifiers and deployed a custom reinforcement learning environment for adaptive treatment.
- Final model simulates treatment over 30 time steps and rewards clinically sound interventions.

---

## 📁 Dataset

- **Source**: ICU patient data (1.5M+ records)
- **Features**: Vitals (HR, O2Sat, SBP, etc.), Demographics, Admission data
- **Target**: Binary sepsis label

---

## ⚙️ Preprocessing Pipeline

- Dropped features with excessive missing values
- Median imputation for numerical fields
- Outlier detection and removal via IQR
- Aggregated records by patient ID for time-series compatibility

---

## 🧠 ML Models

- Logistic Regression
- Random Forest
- XGBoost
- SVM

Evaluated on accuracy, precision, recall, and ROC-AUC to select best classifier.

---

## 🤖 Reinforcement Learning Component

A custom RL environment (`SepsisEnv`) was implemented using PyTorch. Key elements:

- **State**: Vitals and observations at each step
- **Action Space**: 8 possible interventions (e.g., Oxygen, Ventilation, Vasopressors, or combinations)
- **Reward Function**: Encourages clinically appropriate actions, penalizes incorrect treatments
- **Model**: Dueling Deep Q-Network (DQN) with Prioritized Experience Replay
- **Training**: 2000 episodes using advanced replay techniques

---

## 📈 Results

- Reinforcement learning agent showed increasing reward trends during training.
- Realistic patient response simulated for different age groups.
- Achieved adaptive decision-making across varied vitals and conditions.

---

## 📦 Files

- `SepsisOptimalTreatmentPlan.ipynb`: Main ML pipeline
- `RL_Part.ipynb`: Reinforcement learning implementation
- `README.md`: You're reading it
- `LICENSE`: MIT License

---

## 📊 Visual Outputs

- Reward progression over training episodes
- Action-based vitals improvement charts
- Histograms for return distribution

---

## 🧪 Test Scenarios

Tested the RL agent on multiple synthetic patient profiles, simulating ICU interventions with realistic vitals feedback loops. Results showed the model adapting well across different clinical scenarios.

---

## 🛠️ Technologies Used

- Python, NumPy, pandas, matplotlib, scikit-learn
- PyTorch (for RL)
- GANs for data augmentation

---

## 📝 License

This project is licensed under the MIT License.

---

## 🚀 Future Scope

- Deploy the model into an interactive dashboard for clinicians.
- Fine-tune with real-time hospital data feeds.
- Explore alternative RL algorithms like PPO or A3C.

---

