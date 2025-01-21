# **Daily Temperature Data Prediction with Markov Chains** ⛈️🌡️

This project implements a Markov chain model to predict weather states (Cold, Mild, Warm) based on daily temperature data. The dataset is processed, cleaned, and analyzed to generate predictions for future weather states.

---

## **Table of Contents** 📚

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Usage](#usage)
  - [Data Cleaning](#data-cleaning)
  - [State Classification](#state-classification)
  - [Markov Transition Matrix](#markov-transition-matrix)
  - [Visualizations](#visualizations)
  - [Weather Prediction](#weather-prediction)
  - [Model Evaluation](#model-evaluation)
- [Results](#results)
- [Conclusion](#conclusion)

---

## **Project Overview** 📖

This project predicts future weather states (Cold, Mild, Warm) using daily temperature data with a Markov chain model. It includes steps for data preparation, cleaning, state classification, matrix calculation, visualizations, and predictions.

---

## **Required Libraries** ⚙️

The required libraries include:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

---

## **Dataset** 📑

The dataset is loaded from a CSV file (`weather_data.csv`) containing the following columns:
- `Date`: The date of observation.
- `Temperature_C`: The daily temperature in Celsius.

Make sure to place the dataset in the correct directory, or adjust the file path in the code.

---

## **Usage** 🎬

### **Data Cleaning** 🧹

The dataset undergoes the following cleaning steps:
- Handling missing values by replacing them with the mean temperature.
- Removing duplicate rows.
- Identifying and removing outliers using the Interquartile Range (IQR) method.

```python
df = load_and_clean_data(file_path)
```

---


## **State Classification** ❄️🔥

The temperatures are classified into three states:

- **Cold**: Below 15°C
- **Mild**: Between 15°C and 25°C
- **Warm**: Above 25°C

---

## **Markov Transition Matrix** 🧮

The transition matrix is calculated by counting the occurrences of state transitions. This matrix is normalized to represent probabilities of moving from one state to another.

---

## **Visualizations** 📊

- **Temperature Over Time**: Visualizes the daily temperature trends.
- **State Distribution**: Displays the frequency of each weather state.
- **Transition Matrix Heatmap**: Shows the probabilities of transitioning between states.

---

## **Weather Prediction** 🤖

Using the transition matrix, future weather states are predicted.

---

## **Model Evaluation** 📉

The model is evaluated by comparing the predicted states to actual states in the dataset, calculating the error rate.

---

## **Results** 📈

The results include:

- **Transition Matrix**: Probabilities of transitioning between weather states.
- **Predicted States**: The predicted weather states for the given number of days.
- **Actual States**: The true weather states from the dataset.
- **Error Rate**: The proportion of incorrect predictions.

---

## **Conclusion** 🎯

The project successfully demonstrates how a Markov chain model can be applied to predict future weather states based on daily temperature data. The predictions are evaluated, and the model's performance is quantified by the error rate.
