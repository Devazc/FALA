# Forecasting Analysis Using ARIMA and LSTM Models

## Abstract

The project utilizes ARIMA and LSTM models to accurately predict future temperature values for various fields. The proposed method aims to improve traditional time series forecasting methods by utilizing both models' strengths. The accuracy of the proposed method is compared to traditional models, and results show an improvement in forecasting accuracy.

## Introduction

Our project aimed to create a weather monitoring system using IoT and machine learning techniques to predict future weather patterns based on temperature and humidity data collected over time. The system was designed using Node MCU and DHT11 sensors for accurate data collection and transfer. We employed two prediction models - ARIMA and LSTM - for detailed analysis of the collected data. The comparison of these models showed that the deep learning-based LSTM model performed better than the standard ARIMA model. Weather monitoring is important in various industries like agriculture, manufacturing, construction, and smart agriculture can be achieved using machine learning techniques.

## Objective

The objective of this report is to present the key aspects and findings of the "Forecasting Analysis Using ARIMA and LSTM Models" project. The report aims to showcase the importance of accurate temperature and air quality forecasting, the proposed method's strengths and advantages over traditional methods, and the experimental results that demonstrate the method's effectiveness.

## Literature Survey

1. Reviewing different algorithms used for weather prediction, such as ARIMA, STL, SVR, random forest, neural networks.
2. Exploring time series analysis techniques, such as decomposition, differencing, smoothing, and seasonality detection.
3. Identifying commonly used evaluation metrics like RMSE, MAE, R-squared for model accuracy assessment.
4. Investigating real-time accuracy and limitations of predictive models for weather forecasting.
5. Reviewing comparative analysis of predictive models for weather forecasting to understand their strengths and weaknesses.

## Timeline

1. Weather Monitoring System - DECEMBER 2022
2. Forecasting Analysis of Temperature Using LSTM & ARIMA - FEBRAUARY 2023
3. Forecasting Analysis of Air Quality Using LSTM & ARMA - MARCH 2023
4. Data Visualization - MARCH 2023

## Weather Monitoring System

### Block Diagram
![image](https://github.com/Devazc/FALA/assets/122866331/41416eae-85fa-48a9-be36-76c6485a5247)

### The Flow of Data Analysis
![image](https://github.com/Devazc/FALA/assets/122866331/ba807018-7a95-46b0-8b4e-e162e7874cad) 


## Forecasting Analysis Using LSTM

### LSTM Model

- LSTM (Long Short-Term Memory) is a type of neural network that excels in capturing long-term dependencies and patterns in sequential data.
- In this project, we use LSTM to forecast future temperature values based on past observations.
- The LSTM model is trained on historical temperature data and then used to predict the temperature values for a given time period.

### Data Model and Architecture
> Describing The Data

![image](https://github.com/Devazc/FALA/assets/122866331/a23f64de-f86c-4321-8a87-10808466987c)

![image](https://github.com/Devazc/FALA/assets/122866331/acfa7b32-3d41-40c7-9516-55148a9f24f2)


### Temperature Prediction (LSTM)

![image](https://github.com/Devazc/FALA/assets/122866331/f20abd0f-5fed-4ab1-9689-ec7df42b0011)
> As we can see predicted output is very much following the trend of actual output but definitely some room for improvements.  


## Forecasting Analysis Using ARIMA

### ARIMA Model

- ARIMA, short for 'AutoRegressive Integrated Moving Average,' is a class of models that explains a given time series based on its own past values.
- The key idea is that the current value of any time series data can be determined by its own past values.
- For ARIMA models to work, the necessary condition is to have stationary data.

### Modelling ARIMA

- ARIMA, short for ‘Auto Regressive Integrated Moving Average’ is actually a class of models that ‘explains’ a given time series based on its own past values
- The key idea is that the current value of any time series data can be determined by its own past values.
- For ARIMA models to work the necessary condition is to have a stationary data.
- Auto Regressive (AR) model is a specific type of regression model where, the dependent variable depends on past values of itself.
- This necessarily means that the current values are correlated with values in the previous time-steps.
- The AR equation is shown below:
  
![image](https://github.com/Devazc/FALA/assets/122866331/88709848-5ad4-4a43-bb58-a499beb8a640)

- The respective weights(Ф1,Ф2 …Фp) of the corresponding lagged observations are decided by the correlation between lagged observation and the current observation.
- This (p) is called the lag order. It represents the number of prior lag observations we include in the model i.e. the number of lags which have a significant correlation with the current observation.

> Modelling ARIMA (Finding order of AR p)

![image](https://github.com/Devazc/FALA/assets/122866331/8e6d1ce2-b44e-4800-a755-e93a5ae33b9d)


### Temperature Prediction (ARIMA)

![image](https://github.com/Devazc/FALA/assets/122866331/b647a825-f00a-4137-9d61-8a43af62cc20)

> The Final predicted output and actual output of the Temperature.

## Forecasting Analysis of Air Quality Index Using LSTM & ARIMA

 - ### RNN LSTM Model - AQI Forecasting



- ### SARIMAX



- ### Air Quality Index (LSTM)



- ### Air Quality Index (ARIMA)



## Conclusion

In conclusion, our project successfully utilizes ARIMA and LSTM models for accurate temperature and air quality forecasting. The LSTM model outperformed the ARIMA model in terms of accuracy. Accurate weather forecasting is crucial in various industries, and our proposed method shows promising results. By combining the strengths of both models, we can improve the accuracy of time series forecasting for temperature and air quality. Further research and experimentation can be conducted to enhance the models and explore other factors for more comprehensive weather prediction.

---
