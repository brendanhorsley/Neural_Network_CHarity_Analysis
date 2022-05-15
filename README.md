# Neural Network Charity Analysis

## Overview
The purpose of this analysis was to examine data on organizations that recieved funds from Alphabet Soup's business team.
Alphabet Soup wanted to create a machine learning model that was able to predict whether an organization would use funding wisely based on this data.
If the machine learning model was able to accurately predict this information it would greatly aid their business in deciding which organizations to supply with funds.

## Results
The target variable for this project is the "IS_SUCCESSFUL" column which is a binary value of 1 or 0 representing whether the charity was successful in raising and using their money.
The model was trained through many features such as, but not limited to: the industry sector of the organization, their income, and the amount of funding requested.
The original machine learning model used 2 different hidden node layers.
It used the "sigmoid" activation on the output layer.
![firstAccuracy](https://user-images.githubusercontent.com/96553988/168489164-037c6fcd-a18e-47e0-991d-c63cf88f63e1.png)
The original model had an accuracy of 72% after 100 epochs.
The original model used 44 nodes on the first layer and 10 nodes on the second layer.
The first optimization attempt increased the nodes to 80 and 20 respectively to see if this would bring the accuracy above 75%.
![opt1](https://user-images.githubusercontent.com/96553988/168489245-560b3c21-cdee-43ac-97c5-a48f77952a04.png)
The optimized model only increased accuracy by 0.2%, with an accuracy of 72.4% after 100 epochs.
This was not a large enough increase in accuracy to reach our desired amount.
The second optimization attempt used the "tanh" activation instead of "sigmoid", these activations are similarly applicable to our data.
![opt2](https://user-images.githubusercontent.com/96553988/168489303-43891a20-5b07-435b-9a9b-95fd8e2e73fb.png)
With the use of the tanh activation our model's accuracy once again, barely increased and failed to reach our target accuracy.
The final optimization attempt was to increase the number of epochs to allow our model more time to train.
Since the tanh activation yielded the greatest accuracy of the 3 models up to this point, we used this version of the model in our final attempt.
![opt3](https://user-images.githubusercontent.com/96553988/168489347-3d8fe3d6-9956-46fd-855f-702b9c953346.png)
After 300 epochs the tanh activation model still failed to reach our target accuracy of >=75%.

## Summary
Despite three optimization attempts our model was unable to produce at least 75% accuracy. 
Further optimizations would be needed for this model to accurately predict whether an organization would successfully use the funding from Alphabet Soup.
Despite our model's failure to reach the target accuracy, the model was very close to the target.
One optimization that could allow the model to reach the target goal that was not explored would be the addition of more data bins.
Giving the model more data on each organization to train on might allow this model to reach the target accuracy and become effective in it's predictions.
