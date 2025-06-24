# 🔬 ChemPredict Pro

**ChemPredict Pro** is a cross-platform mobile application that predicts chemical properties and toxicity using SMILES notation. Built with Flutter and powered by XGBoost and RDKit, the app brings machine learning into your pocket, enabling offline analysis of molecular compounds.

---

## 📲 Features

- **SMILES Input** for compound recognition
- **Toxicity Prediction** using an XGBoost model
- **Descriptor Calculation** (Molecular Weight, LogP, TPSA, HBD, HBA, Ring Count, Rotatable Bonds, Fraction Csp³)
- **Lipinski Rule Compliance Check**
- **Dynamic UI Tabs** for Prediction, Results, Analysis, and Team
- **Confetti Animation** for positive feedback
- **Offline Inference** with locally stored model and scaler JSON

---

## ⚙️ Tech Stack

- **Flutter + Dart** (Mobile Development)
- **Python (Jupyter Notebook)** for ML pipeline and model generation
- **XGBoost + SMOTE + StandardScaler** for toxicity classification
- **RDKit** for descriptor extraction
- **Firebase-ready structure** for future backend integration
- **GitHub Actions** configured for CI

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (>=3.6.2)
- Dart SDK
- Android Studio or Visual Studio Code (Flutter setup)
- Emulator or physical device

### Installation

```bash
git clone https://github.com/ajaykrishna00-7/Drug-Analyser.git
cd Drug-Analyser
flutter pub get
flutter run
```

---

## 📁 Project Structure

```
Drug-Analyser/
├── android/
├── ios/
├── linux/
├── macos/
├── windows/
├── web/
├── .github/workflows/
├── assets/
│   ├── model.json
│   ├── scaler.json
│   ├── team1.jpg ...
├── lib/
│   └── main.dart
├── firebase/
├── firebase.json
├── pubspec.yaml
├── README.md
├── Backend_jupyter.ipynb
```

---

## 🤖 Machine Learning

- Trained using `XGBoostClassifier` on 8 molecular descriptors
- Dataset balanced using `SMOTE`
- Features scaled using `StandardScaler`
- Exported `model.json` and `scaler.json` embedded in the app
- Prediction threshold: sigmoid output > 0.5 = Toxic

Descriptor calculation is handled via RDKit in the training phase. In-app predictions are made using simulated descriptor input or external preprocessing.

---

---
> *ChemPredict Pro – Making chemical predictions smarter, faster, and mobile.*
