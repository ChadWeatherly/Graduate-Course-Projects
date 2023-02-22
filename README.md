# Long Short-Term Memory Network Distillation

As part of a graduate Advanced Machine Learning course, this project was created as my final project. In it, my goal was to utilize Distillation for an LSTM, to see if a regular neural network could be distilled time-series information from an LSTM network. See the final_report.pdf for the detailed findings.

__Abstract__

As deep learning continues to grow in its use and application, there is a need for less complex models. While large organizations with large amounts of resources (large university groups, national laboratories, Google, Amazon, Microsoft, etc.) may have the computational capability needed for training and deploying complex models, it is often infeasible for many applications. Distillation is a form of transfer learning that aims to teach a less complex student model the same decision boundary as a larger complex model. It has been shown that distillation can reduce model size while maintaining accuracy. In this project, we have a large swath of COVID-19 data from Google at different days. The goal is to train a larger deep learning model using a Long Short-Term Memory (LSTM) layer that learns the data in a time series format, but then transfers this knowledge to a less-complex student model without an LSTM layer. If the student model can learn successfully without an LSTM layer, then it would show that the time series information can be learned without a specific time-specific component implemented in the architecture itself.




<img width="839" alt="Screenshot 2023-02-21 at 9 26 13 PM" src="https://user-images.githubusercontent.com/45674547/220513697-2f6c9878-9430-4022-9e63-7d8026f1c1f4.png">



The below charts convey the training and testing losses (respectively) of each of the student models, where "FNN" models are those trained on the data and "Student" models are those trained only on the LSTM Teacher outputs, and each of the 5 models for both types was trained on 4/5 K-folds:



<img width="810" alt="Screenshot 2023-02-21 at 9 30 00 PM" src="https://user-images.githubusercontent.com/45674547/220514221-2fb90607-20b9-4a6d-9492-b9b7f7646ffa.png">



<img width="810" alt="Screenshot 2023-02-21 at 9 30 16 PM" src="https://user-images.githubusercontent.com/45674547/220514272-72dc32e8-8898-4b11-8a87-37573cca86ed.png">
