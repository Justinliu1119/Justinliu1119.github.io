---
title: Speed Trap

---


![](/img/projects/p4d1.png)

We construct a novel submersible safety assurance system for addressing safety concerns during underwater sightseeing tours of submersibles in the Ionian Sea. Our system incorporates multiple mathematical models and employs methods such as TDOA (Time Difference of Arrival) localization and Kalman filtering to enhance real-time and accurate prediction of the submersible movements, and to improve the success rate of search operations in case of unexpected loss of contact.

For locating the submersible, due to factors like observation noise, simple localization methods often yield significant errors in estimating the actual submersible position. Hence, we established a localization model based on acoustic signals transmitted from multiple known buoys and anchor points to continuously obtain real- time observed positions of the submersible through TDOA localization. Then, leveraging the localization model, we created a prediction model based on the Kalman filtering algorithm to optimally predict the submersible position, thereby achieving more precise prediction.

![](/img/projects/p4d2.png)

**TDOA Localization Model**

Taking advantage of the limited propagation speed of sound in water and the existence of acoustic signal transmitters and receivers, oue team deployed four surface buoys with known positions. The measured position of our submersible in this section plays an important role in the subsequent model in which we used Kalman Filtering to estimate the navigation behavior of the submarine. To achieve clock synchronization and ensure accurate positioning of the submarine, we added the fifth receiver placed at the bottom of the ocean as the clock for synchronization reference. In the submersible acoustic positioning, we use TDOA under the condition of equal sound velocity profile to simulate the position of the submersible position. Each buoy is equipped with an acoustic signal receiver for the signal emitted by the submarine transmitter every t-second.

The setup for the experiment of localization through TDOA and the generated simulation result is shown in to figures on the right.

Note: We run the simulation of TDOA based on the following instantiations:The coordinates to be stations are set to[−800 − 200 3], [−200 − 800 0], [−800 − 1000 0], [0 0 0], [−500 − 500 − 500]. We uniformly place a total of 1000 test points which represent predetermined coordinates of the submarines in space starting from coordinates [100 − 100 − 50], with intervals of 60 𝑚 along the x-axis, 60 𝑚 along the y-axis, and 30 𝑚 along the z-axis.

![](/img/projects/p4d3.png)

**Estimation of Location via Kalman Filter**

To implement the Kalman filtering algorithm, it is necessary to obtain the state transition equation of the object. Using this equation and the object's posterior estimated value at time t, as well as the assumed noise influence, the object's prior estimated value at time t+1, or the prediction result, is calculated. In this instance, the state transition equation of the Kalman filtering algorithm is derived based on the data sent from the submersible to the host ship at time t, including the submersible motion velocity and acceleration in all directions at time t, as well as the ocean current acceleration in all directions. This is combined with the optimal estimated position coordinates obtained through the Kalman filtering algorithm at time t and the assumed noise, to infer the submersible position coordinates at time t+1.

In addition to the state transition equation, the implementation of the Kalman filtering algorithm also requires a measurement equation, obtained from actual observation data and the assumed noise influence to derive the observed state. In this example, the observation equation of the Kalman filtering algorithm is based on the positioning results obtained from the location model and the assumed noise addition. The location model, as previously mentioned, calculates the submersible position coordinates by receiving acoustic signals from buoys.

After obtaining the state transition equation and the observation equation, the posterior estimate of the object at time t, derived through the Kalman filtering algorithm, can be computed. Firstly, the Kalman coefficients of the object at time t are calculated based on existing data, resulting in intermediate results of the filtering calculation. Finally, the posterior or optimal estimate of the object at time t is calculated as the sum of the object's prior estimate at time t and the product of the Kalman coefficient multiplied by the difference between the object's observation value at time t and the object's prior estimate value at time t.


