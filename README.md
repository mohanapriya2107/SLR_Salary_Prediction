# 📊 Salary Prediction using Simple Linear Regression

### Flask | Scikit-learn | Machine Learning | HTML/CSS | Render Deployment

---

# 📌 Project Overview

This project is a complete **Machine Learning Web Application** that predicts employee salaries based on their **Years of Experience** using **Simple Linear Regression (SLR)**.

The system was developed by:

* Training a machine learning model on a salary dataset
* Evaluating its performance using regression metrics
* Saving the trained model using Pickle
* Integrating the model into a Flask web application
* Deploying the application on Render

The application allows users to enter their years of experience and instantly receive a predicted salary value.

---

# 🎯 Objective of the Project

The main objectives of this project are:

✅ Understand Simple Linear Regression
✅ Learn Model Training & Testing
✅ Evaluate Machine Learning Models
✅ Build a Flask-based Web Application
✅ Integrate Frontend with Backend
✅ Deploy ML Applications on Cloud Platforms

---

# 🧠 Machine Learning Concept

## 📈 Simple Linear Regression (SLR)

Simple Linear Regression is a supervised machine learning algorithm used to predict a dependent variable using one independent variable.

In this project:

| Variable Type            | Variable            |
| ------------------------ | ------------------- |
| Independent Variable (X) | Years of Experience |
| Dependent Variable (Y)   | Salary              |

---

# 📐 Mathematical Formula

The regression equation is:

[
Y = mX + c
]

Where:

| Symbol | Meaning             |
| ------ | ------------------- |
| (Y)    | Predicted Salary    |
| (X)    | Years of Experience |
| (m)    | Slope               |
| (c)    | Intercept           |

---

# 📊 Regression Visualization

```text id="p3w8cx"
                     Salary
                        ↑
                        |
                        |                          *
                        |                      *
                        |                  *
                        |              *
                        |          *
                        |      *
                        |  *
                        +--------------------------------→ Experience
```

The regression model tries to fit the best straight line through all data points to minimize prediction error.

---

# ⚙️ Technologies Used

# 🖥️ Programming Language

* Python

# 📚 Libraries Used

* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Pickle
* Flask

# 🌐 Frontend

* HTML
* CSS

# ☁️ Deployment Platform

* Render

---

# 📂 Dataset Description

The dataset contains:

| Feature         | Description                  |
| --------------- | ---------------------------- |
| YearsExperience | Employee experience in years |
| Salary          | Corresponding salary         |

---

# 🔀 Data Splitting

The dataset was divided into:

| Dataset       | Percentage |
| ------------- | ---------- |
| Training Data | 80%        |
| Testing Data  | 20%        |

---

# ❓ Why Train-Test Split?

### Training Data

Used to train the model and learn patterns.

### Testing Data

Used to evaluate model performance on unseen data.

### Benefits

* Prevents overfitting
* Measures real-world performance
* Improves model reliability

---

# 🏗️ Machine Learning Workflow

```text id="j2m8ul"
                ┌────────────────────┐
                │   Dataset Input    │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Data Preprocessing │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Train-Test Split   │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ SLR Model Training │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Model Evaluation   │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Save Model (.pkl)  │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Flask Integration  │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Render Deployment  │
                └────────────────────┘
```

---

# 📊 Model Performance Analysis

# ✅ Training Performance

## 📌 R² Score (Accuracy)

[
95.62%
]

### Explanation

R² Score measures how well the model explains the relationship between input and output variables.

[
R^2 = 0.9562
]

This means:

* The model explains approximately **95.62%** of salary variation.
* The model learned the dataset effectively.
* Higher R² indicates better prediction capability.

---

# 📌 Mean Squared Error (MSE)

[
32636115.30
]

## Formula

[
MSE = \frac{1}{n}\sum (y_i - \hat{y_i})^2
]

### Explanation

MSE calculates the average squared difference between:

* Actual Salary
* Predicted Salary

### Key Points

* Lower MSE is better
* Penalizes larger errors heavily
* Indicates prediction quality

---

# 📌 Root Mean Squared Error (RMSE)

[
5712.80
]

## Formula

[
RMSE = \sqrt{MSE}
]

### Explanation

RMSE converts squared error into the original salary unit.

This means:

> The model predictions are approximately off by around 5712 salary units during training.

---

# ✅ Testing Performance

# 📌 R² Score(Coefficient of Determination)

R² Score measures how well the regression model fits the data.

### Formula

```math
R^2 = 1 - \frac{SS_{res}}{SS_{tot}}
```

### Where

* (SS_{res}) = Sum of Squared Residuals

```math
SS_{res} = \sum_{i=1}^{n}(y_i - \hat{y}_i)^2
```

* (SS_{tot}) = Total Sum of Squares

```math
SS_{tot} = \sum_{i=1}^{n}(y_i - \bar{y})^2
```

### Interpretation

* (R^2 = 1) → Perfect Prediction
* (R^2 = 0) → Model performs poorly
* Higher R² Score indicates better model performance

---

# 📌 Mean Squared Error

MSE measures the average squared difference between actual and predicted values.

### Formula

```math
MSE = \frac{1}{n-1}\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
```

### Where

* (y_i) = Actual Value
* (\hat{y}_i) = Predicted Value
* (n) = Number of Data Points

### Interpretation

* Lower MSE indicates better model accuracy.
* Penalizes larger errors more heavily.

---

# 📌 Root Mean Squared Error

RMSE is the square root of Mean Squared Error.

### Formula

```math
RMSE = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(y_i-\hat{y}_i)^2}
```

### Interpretation

* RMSE gives error in the same unit as the target variable.
* Lower RMSE indicates better predictions.
* Easier to interpret than MSE because it is in the original scale.

---

# 💾 Model Serialization

After training, the model was saved using Pickle serialization.

## Saving Model

```python id="p9jlwm"
import pickle

pickle.dump(model, open("SLR_MODEL.pkl", "wb"))
```

## Saved File

```text id="jlwm0x"
SLR_MODEL.pkl
```

This allows the trained model to be reused without retraining.

---

# 🌐 Flask Web Application

The trained model was integrated into a Flask web application.

---

# 🔄 Application Workflow

```text id="jlwmx9"
 User Input
      │
      ▼
┌───────────────┐
│ index.html    │
└──────┬────────┘
       │ POST Request
       ▼
┌───────────────┐
│ Flask Backend │
│    app.py     │
└──────┬────────┘
       │
       ▼
┌───────────────┐
│ SLR_MODEL.pkl │
└──────┬────────┘
       │ Prediction
       ▼
┌───────────────┐
│ Predicted     │
│ Salary Output │
└───────────────┘
```

---

# 🖥️ Frontend Development

The frontend was developed using:

* HTML
* CSS

## Features

✅ User-friendly interface
✅ Experience input field
✅ Submit button
✅ Dynamic prediction display
✅ Responsive design

The frontend file is stored inside:

```text id="jlwm4z"
templates/index.html
```

---

# ⚡ Backend Development

The backend was developed using Flask.

## Functionalities

### Routing

Handles webpage navigation.

### Form Handling

Receives user input from HTML forms.

### Model Loading

Loads the saved `.pkl` model.

### Prediction

Predicts salary based on experience.

### Rendering

Displays prediction results dynamically.

---

# 📁 Project Structure

```text id="jlwm1k"
Salary-Prediction/
│
├── app.py
├── SLR_MODEL.pkl
├── requirements.txt
│
├── templates/
│   └── index.html
│
├── Procfile
│
└── README.md
```

---

# 🚀 Deployment on Render

The application was successfully deployed using Render Cloud Platform.

## Deployment Steps

1️⃣ Upload project to GitHub
2️⃣ Connect GitHub repository with Render
3️⃣ Configure Build & Start Commands
4️⃣ Deploy application

---

# 🔥 Key Learning Outcomes

Through this project, the following concepts were learned:

✅ Machine Learning Workflow
✅ Data Splitting
✅ Model Training & Testing
✅ Linear Regression
✅ Model Evaluation Metrics
✅ Flask Framework
✅ Frontend-Backend Integration
✅ Pickle Serialization
✅ Cloud Deployment

---

# 🔮 Future Enhancements

Possible future improvements:

🚀 Multiple Linear Regression
🚀 Advanced UI/UX Design
🚀 Database Integration
🚀 User Authentication
🚀 Real-time Analytics Dashboard
🚀 Docker Deployment
🚀 REST API Development
🚀 Deep Learning Models

---

# 👨‍💻 Author

## Mohana Priya Korukoppula

### AI & Machine Learning Enthusiast

---

# 🔗 Professional Links

## GitHub

Add your GitHub profile:

```text id="jlwmz1"
https://github.com/mohanapriya2107
```

---

## LinkedIn

Add your LinkedIn profile:

```text id="jlwmz2"
https://www.linkedin.com/in/mohana-priya-579b04253/
```

---

# 📧 Contact

```text id="jlwmz4"
korukoppulamohanapriya@gmail.com
```

---

# ✅ Conclusion

This project demonstrates the complete lifecycle of a Machine Learning application from:

* Data preprocessing
* Model training
* Performance evaluation
* Model serialization
* Flask integration
* Frontend development
* Cloud deployment

The Simple Linear Regression model achieved excellent prediction accuracy and was successfully integrated into a dynamic Flask web application capable of predicting salaries based on user input.

---
