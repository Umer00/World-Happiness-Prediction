# 🌍 World Happiness Prediction

### Exploring Global Happiness Through Data Analysis & Machine Learning

**What makes a country happy?** Is it economic prosperity, social support, better health, or the freedom to make life choices?

This project explores global happiness data using Python, data visualization, and machine learning. It analyzes the factors associated with happiness across countries and builds regression models to predict happiness scores based on social and economic indicators.

The project includes Exploratory Data Analysis (EDA), correlation analysis, data visualization, and a comparison of three machine learning algorithms.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Project Objectives](#-project-objectives)
- [Dataset](#-dataset)
- [Key Features](#-key-features)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Machine Learning Models](#-machine-learning-models)
- [Model Evaluation](#-model-evaluation)
- [Technologies Used](#️-technologies-used)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Key Learnings](#-key-learnings)
- [Future Improvements](#-future-improvements)
- [License](#-license)

---

## 📖 Project Overview

The World Happiness Report provides insights into how people evaluate their quality of life across different countries.

This project uses the 2019 World Happiness dataset to investigate the relationship between happiness scores and several country-level indicators, including GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption.

After exploring and visualizing the data, three regression algorithms are trained and evaluated to understand how effectively they can estimate a country's happiness score.

The project demonstrates a complete introductory machine learning workflow, from understanding a dataset to evaluating predictive models.

## 🎯 Project Objectives

- Explore global happiness data and understand its main features.
- Identify patterns among countries with different happiness scores.
- Analyze relationships between economic, social, and health indicators.
- Visualize the highest-ranking countries across selected indicators.
- Examine correlations between numerical variables.
- Train multiple regression models to predict happiness scores.
- Compare model performance using Mean Squared Error (MSE) and R² Score.
- Understand how machine learning can support data-driven analysis.

## 📊 Dataset

**File:** `2019.csv`

The dataset contains 156 country-level records and 9 columns, including country rankings, happiness scores, and related indicators.

### Dataset Features

| Feature | Description |
|---|---|
| `Overall rank` | Country's overall happiness ranking. |
| `Country or region` | Name of the country or region. |
| `Score` | Reported happiness score; the prediction target. |
| `GDP per capita` | Indicator of economic prosperity. |
| `Social support` | Measure related to available social support. |
| `Healthy life expectancy` | Indicator of expected healthy lifespan. |
| `Freedom to make life choices` | Measure of perceived freedom in life decisions. |
| `Generosity` | Indicator associated with generosity. |
| `Perceptions of corruption` | Measure of perceived corruption. |

For model training, `Score` is used as the target variable. `Country or region` and `Overall rank` are excluded from the input features, while the six numerical indicators are used as predictors.

## ✨ Key Features

### 🔎 Exploratory Data Analysis

Explore the dataset to understand its structure, numerical indicators, and country-level happiness scores.

### 📈 Data Visualization

Create charts to compare countries across selected indicators and make patterns easier to understand.

### 🌡️ Correlation Analysis

Use a correlation heatmap to examine relationships between numerical variables and the happiness score.

### 🤖 Machine Learning

Train three regression models to estimate happiness scores from the selected indicators.

### 📏 Performance Evaluation

Compare model predictions with actual scores using MSE and R² Score.

### 🔬 Model Comparison

Evaluate the strengths and limitations of different regression approaches using the same train-test split.

## 📉 Exploratory Data Analysis

The notebook includes visual analysis of selected indicators, including:

- **Top 5 Happiest Countries:** Compare countries with the highest happiness scores.
- **Top 5 Countries by Freedom:** Explore countries with higher freedom-to-make-life-choices values.
- **Top 5 Countries by Healthy Life Expectancy:** Compare countries based on healthy life expectancy.
- **Correlation Heatmap:** Visualize correlations among numerical indicators.

These visualizations help explore the dataset before applying machine learning models.

## 🧠 Machine Learning Models

The project uses three regression algorithms from Scikit-learn.

### 1. Linear Regression

Linear Regression estimates the relationship between the selected input variables and the happiness score. It provides a useful baseline for understanding how numerical indicators can be used for prediction.

### 2. Decision Tree Regressor

The Decision Tree Regressor learns decision rules from the training data. In this project, the tree is configured with a maximum depth of 4 to limit its complexity.

### 3. Random Forest Regressor

The Random Forest Regressor combines predictions from multiple decision trees. The model uses 100 estimators to produce its predictions.

### Training Workflow

1. Select the six numerical predictor variables.
2. Set `Score` as the target variable.
3. Split the dataset into 80% training data and 20% testing data.
4. Train each regression model using the training data.
5. Generate predictions on the test data.
6. Evaluate and compare the results using MSE and R² Score.

The notebook uses `random_state=17` for the train-test split to make the split reproducible.

## 🏆 Model Evaluation

The notebook's recorded evaluation results are summarized below.

| Model | Mean Squared Error (MSE) | R² Score |
|---|---:|---:|
| Linear Regression | 0.2486 | 0.8077 |
| Decision Tree Regressor | 0.3720 | 0.7123 |
| Random Forest Regressor | 0.2526 | 0.8046 |

### Understanding the Results

- **Linear Regression** achieves the lowest MSE and highest R² Score among the three models in the recorded results.
- **Random Forest** performs closely to Linear Regression, with a slightly higher MSE and slightly lower R² Score.
- **Decision Tree** records a higher MSE and lower R² Score than the other two models.

Based on these results, Linear Regression performs best on this particular test split.

The R² Score of approximately 0.81 indicates that the model explains around 80.8% of the variation in the test-set happiness scores. This does not mean that the model predicts every country's score with 80.8% accuracy.

These results are specific to the dataset and evaluation setup; further validation would be required to establish how well the models generalize to other years or countries.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical charts and correlation heatmap |
| Scikit-learn | Regression models and evaluation metrics |
| Jupyter Notebook | Interactive development and analysis |
| Git & GitHub | Version control and project hosting |

## 📁 Project Structure

```text
World-Happiness-Prediction/
│
├── 2019.csv
│   └── World Happiness dataset for 2019
│
├── World_Happiness_Prediction.ipynb
│   └── Data analysis, visualizations,
│       regression models, and evaluation
│
├── README.md
│   └── Project documentation
│
└── LICENSE
    └── MIT License
```

## 🚀 Getting Started

Follow these steps to run the project on your computer.

### Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- Git (optional)

### Step 1: Clone the Repository

```bash
git clone https://github.com/Umer00/World-Happiness-Prediction.git
```

### Step 2: Navigate to the Project Directory

```bash
cd World-Happiness-Prediction
```

### Step 3: Install the Required Libraries

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Open the Notebook

Open `World_Happiness_Prediction.ipynb` and run the cells sequentially.

**Important:** Keep `2019.csv` in the same directory as the notebook so the dataset can be loaded using the appropriate file path.

You can also open the notebook in Google Colab and upload the CSV file when required.

## 💡 Key Learnings

This project provides practical experience in:

- Exploratory Data Analysis (EDA)
- Data visualization and correlation analysis
- Understanding socioeconomic indicators
- Feature selection and target variable definition
- Training regression models with Scikit-learn
- Splitting data into training and testing sets
- Evaluating models using MSE and R² Score
- Comparing different machine learning algorithms
- Interpreting model performance and prediction errors

## 🔮 Future Improvements

Possible extensions to the project include:

- Analyze multiple years of World Happiness Report data.
- Compare happiness trends over time.
- Add a predicted-versus-actual score visualization.
- Investigate feature importance and statistical relationships.
- Apply cross-validation for more reliable model comparison.
- Tune model hyperparameters to improve performance.
- Test models on a separate year to evaluate generalization.
- Develop an interactive dashboard for exploring country-level indicators and predictions.

## 📜 License

This project is licensed under the MIT License. See the [`LICENSE`](LICENSE) file for details.

---

**Exploring global happiness through data, statistics, and machine learning.** 🌍
