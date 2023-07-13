# Forecasting-Analysis
**A project that uses ARIMA and LSTM models to predict future outcomes based on historical data.**

- This Project focus on two main parts which are the Hardware Implementation of 
Weather Monitoring System and Analysis of recorded values, to predict the future 
elements of required parameters. In this project we focused on Temperature, 
Humidity, Pressure.
By using this sensors to monitor the weather parameter that are temperature, 
humidity and Pressure the system will be able to display the weather condition 
by an analysis about the current weather with the sensor value data. All the data 
will be control by a microcontroller ESP8266 an via wifi/hotspot we send data to 
ThingSpeak. The data collected will be analyse and compare it with required 
Meteorological Data Sheets to ensure the precise of data and weather condition 
on current condition. The Internet of Things (IoT) will connect the system with 
the user wireless and online without the need of checking manually.

### Weather Monitoring System Block Diagram

![image](https://user-images.githubusercontent.com/122866331/212913309-642f7a9d-5214-4872-a058-54a0f217095c.png)

### Hardware Development

- The hardware selection is vital in this project hardware development process. 
Every hardware components are necessary to be considered first before selected 
to be utilized in the project. The components selection is according to the 
advantages and characteristic of the component to fulfil the functionality of every 
part used. For this project Node MCU, BMP180, DHT11, are used. Since we are 
working only with the prototype of the real time implementation we can really 
focus on the only essentials parameters which in our case will be temperature, 
humidity and pressure. Also, these parameters proves to be very effective when 
doing time series analysis as they are continuous in nature and they, to some 
extent depends of their old values. Some photos of our hardware implementation 
has been given below.

![image](https://user-images.githubusercontent.com/122866331/212915503-50370a7e-3506-45db-9569-4b812184c8c0.png)


### Software Devlopment

- The next phase in our project was to make use of that data that we managed to 
upload on ThingSpeak (since the amount of data we require for modelling is large 
we took a dataset directly from Kaggle and the dataset link is in the reference 
section). We used 2 of the most widely used models in order to get our 
predictions.
The first approach is Deep Learning based in which we have used RNN’s for this 
purpose and particularly LSTM’s. Going for LSTM over any other DL model is 
due the fact that it excels on retaining old time informations along with the new 
data. The reason for this behaviour is the Horizontal line that passes through the 
top of LSTM cell. 
The second approach is the ARIMA modelling which is best suited for the case 
of time series forecasting. There are three parameters which ARIMA is made of. 
The first is Auto Regressive (p) which determines on how many previous lags the 
new value depends on. The second is Integrated (d) which signifies what order of 
differencing we need to take to make our data stationary and the last is Moving 
Average (q) which determining the error of past lags which will have their affect 
in predicting the new value. 


### RESULTS

> The output when we used LSTM to predict the value of temperature (We used past 48 
values for each parameters, concatenated them along 1 axis and feed them into the 
neural network to get the following output). Tough not perfect, we got the output 
better than what we had initially expected. After a total of 37 epochs and with Adam 
optimizer and a learning rate of 0.001 we got the following output. 

![image](https://user-images.githubusercontent.com/122866331/212918587-0e1a4791-fec4-4bbf-8fd4-006ca3a94c64.png)

**Now, we had the question can we do better?** Exactly to answer this question we 
switched to ARIMA modelling to get the outputs and compare between the two 
algorithms.

![image](https://user-images.githubusercontent.com/122866331/212919541-e7cc5c5f-b6e5-4e37-ae9d-878f88e5e1ee.png)

> This was the output when we have kept the differencing factor as 0, and fixed p and q
 as 2. Definitely this is not random and we have selected these values using the parial
 correlation function in python scipy module.
 
 ### To Conclude
 
 In this project we have successfully demonstrated an end to end implementation 
of weather monitoring system. Also, we have tried to cover both grounds 
hardware and software so the reader can correlate how the data is transmitted 
from the use of Arduino to a cloud platform which in our case is thingspeak. 
Later, we took that data and have done predictive modelling on that with the 
help of two of the most widely used yet different algorithms. We then have 
successfully compared the results of both of them in a graphical format which 
can be seen in the Results and Discussion Section. Our model has advantage as 
it case highly cost effective because all it needed was a few sensors for our 
purpose and all the programming was done in Arduino IDE and Google 
Colaboratory and we have managed to get satisfactory results. On the other 
hand, since we have used only 2 sensors, we have suffered in the realtime 
accuracy and this will need further improvement to become useful enough so 
that it can be deployed on real world use cases.







