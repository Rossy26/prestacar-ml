# Prestacar ML - Credit Risk Analysis

## Project Description

This project consists of building a **Machine Learning** model to evaluate the credit risk of a financial institution's clients. The main objective is to predict the probability of a client defaulting on their automotive loan ("Prestacar").

One of the main challenges addressed in this project is handling **imbalanced classes**, given that the vast majority of clients fulfill their payments, while a small fraction represents the defaulting clients.

## Data and Features

The model is trained using the `prestacar.csv` dataset, which includes the clients' financial and demographic information, such as:
- Client income.
- Loan annuity.
- Years with own home.
- Credit scores.
- Target variable: `moroso` (0 = Compliant, 1 = Defaulter).

## Technologies Used

The key tools and libraries used for developing this project are:
- **Python**: Main programming language.
- **Pandas**: For data manipulation and analysis.
- **Scikit-Learn**: For the creation, training, and evaluation of Machine Learning models (e.g., `DecisionTreeClassifier`).
- **Matplotlib / Seaborn**: For data visualization and results of different evaluation metrics.
- **Jupyter Notebook**: As an interactive development environment.

## Repository Structure

```text
📦 prestacar-ml
 ┣ 📜 notebook.ipynb     # Main notebook with exploratory analysis and model training
 ┣ 📜 prestacar.csv      # Dataset used for training (local data)
 ┣ 📜 requirements.txt   # Dependencies needed to run the project
 ┗ 📜 README.md          # Project documentation (this file)
```

## Installation and Usage

Follow these steps to run the project in your local environment:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Rossy26/prestacar-ml.git
   cd prestacar-ml
   ```

2. **Create a virtual environment (Optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the necessary dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the interactive environment:**
   Open the `notebook.ipynb` file using Jupyter Notebook or Jupyter Lab to see the full analysis and run the code cells.
   ```bash
   jupyter notebook notebook.ipynb
   ```

## Modeling and Evaluation

The project starts by establishing a **baseline** using a `DecisionTreeClassifier`. A fundamental part of the process involves:
1. **Data splitting**: Separation into training (`train`), validation (`val`), and test (`test`) sets to avoid overfitting.
2. **Training**: Fitting the models with the training data.
3. **Evaluation Metrics**: Analyzing the models' performance, paying special attention to useful metrics for a use case with imbalanced classes (such as precision, recall, f1-score, and the confusion matrix), understanding the limitations of using only accuracy.
