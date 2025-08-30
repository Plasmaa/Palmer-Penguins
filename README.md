# 🐧 Penguin Species Classification with Machine Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A comprehensive machine learning project that classifies penguin species from the Palmer Archipelago using morphological measurements. This project demonstrates a complete supervised classification workflow with extensive evaluation of multiple algorithms.

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Methodology](#-methodology)
- [Results](#-results)
- [Applications](#-applications)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

## 🎯 Overview

This project implements a supervised machine learning classification system to identify penguin species based on physical characteristics and location data. The Palmer Penguins dataset serves as a modern alternative to the classic Iris dataset, providing more realistic data challenges including missing values and categorical features.

## 📊 Dataset

**Dataset Source:** [Palmer Penguins on Kaggle](https://www.kaggle.com/datasets/parulpandey/palmer-archipelago-antarctica-penguin-data)

**Features:**
- `species`: Target variable (Adelie, Chinstrap, Gentoo)
- `island`: Island name (Dream, Torgersen, Biscoe)
- `bill_length_mm`: Culmen length (mm)
- `bill_depth_mm`: Culmen depth (mm)
- `flipper_length_mm`: Flipper length (mm)
- `body_mass_g`: Body mass (grams)
- `sex`: Penguin sex

**Dataset Statistics:**
- Total entries: 344
- Features: 7
- Missing values: Present (handled in preprocessing)

## 📁 Project Structure

```
penguin-classification/
│
├── notebooks/
│   └── Penguin_Classification_Full.ipynb  # Complete Jupyter notebook
│
├── src/
│   ├── data_loading.py          # Data loading utilities
│   ├── preprocessing.py         # Data cleaning and preprocessing
│   ├── visualization.py         # EDA visualization functions
│   ├── modeling.py              # Model training and evaluation
│   └── prediction.py            # Prediction utilities
│
├── data/
│   └── penguins.csv             # Dataset (optional local copy)
│
├── results/
│   ├── confusion_matrices/      # Saved confusion matrices
│   ├── roc_curves/              # ROC curve visualizations
│   └── performance_metrics.csv  # Model performance comparison
│
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

## 💻 Installation

### Option 1: Google Colab (Recommended)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10xy0ZIxJ5IB8BQdsledRiC3_2bR9IkCd?usp=sharing)

### Option 2: Local Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/penguin-classification.git
cd penguin-classification
```

2. Create a virtual environment (optional but recommended):
```bash
python -m venv penguin_env
source penguin_env/bin/activate  # On Windows: penguin_env\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

### Running the Complete Analysis

1. **Jupyter Notebook**: Open and run `notebooks/Penguin_Classification_Full.ipynb`
2. **Google Colab**: Use the provided Colab link above

### Key Sections to Execute:

1. Data loading and inspection
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Model training (multiple algorithms)
5. Model evaluation and comparison
6. Prediction on new data

## 🔧 Methodology

### 1. Data Preprocessing
- Handled missing values through row removal
- Encoded categorical features (island, sex) using One-Hot Encoding
- Scaled numerical features using StandardScaler
- Performed train-test split (80-20) with stratification

### 2. Exploratory Data Analysis
- Pairplot visualization of feature relationships by species
- Correlation heatmap of numerical features
- Species distribution analysis
- Boxplots of numerical features across species

### 3. Model Implementation
Implemented and compared six classification algorithms:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine (SVC)
- Gradient Boosting Classifier
- K-Nearest Neighbors Classifier

### 4. Model Evaluation
Comprehensive evaluation using:
- Accuracy scores
- Classification reports (precision, recall, F1-score)
- Confusion matrices
- ROC curves and AUC scores (One-vs-Rest approach)

## 📈 Results

### Performance Summary:

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Random Forest | 100% | 1.00 | 1.00 | 1.00 |
| Support Vector Machine | 100% | 1.00 | 1.00 | 1.00 |
| Logistic Regression | 98.51% | 0.99 | 0.99 | 0.99 |
| K-Nearest Neighbors | 98.51% | 0.99 | 0.99 | 0.99 |
| Gradient Boosting | 97.01% | 0.97 | 0.97 | 0.97 |
| Decision Tree | 92.54% | 0.93 | 0.93 | 0.93 |

### Key Findings:
- Random Forest and SVM achieved perfect classification on the test set
- All models showed strong performance (≥92% accuracy)
- High correlation observed between flipper length and body mass (0.87)
- Bill depth shows negative correlation with other features

## 🎯 Applications

This classification system has several practical applications:

1. **Species Identification**: Quick field identification from measurements
2. **Conservation Efforts**: Targeted resource allocation for specific species
3. **Research Studies**: Population monitoring and ecological studies
4. **Educational Tools**: Teaching biodiversity and machine learning concepts

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. 

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- **Dataset Source**: [Dr. Kristen Gorman](https://www.uaf.edu/cfos/people/faculty/detail/kristen-gorman.php) and the [Palmer Station LTER](https://pal.lternet.edu/)
- **Dataset Curator**: [Allison Horst](https://github.com/allisonhorst/palmerpenguins)
- **Inspiration**: This project was developed as part of learning supervised machine learning classification techniques

## 📞 Contact

For questions or suggestions about this project, please open an issue or contact:

**Your Name**  
- Email: your.email@example.com  
- GitHub: [YourGitHubUsername](https://github.com/YourGitHubUsername)  
- LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)

---

**⭐ If you found this project helpful, please give it a star!**
