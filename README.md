# Sentiment-RuReview-Classifier
Test sample (last 3 columns) - dataset of real reviews of tourist attractions from Yandex maps.

The purpose of this benchmark is to evaluate how hyperparameters affect the learning outcomes of a simple LSTM network.

A total of 46 models have been trained, the internal architecture is the same.

The established probability threshold for the transition from neutral to polar class is 0.5. Only two classes are defined on the test dataset: positive (grades 4 and 5) and negative (grades 1, 2 and 3).

A possible extension of the model is a change in the probability threshold.

___
Models trained on USE-M embeddings (128 neurons).
| № | Epochs | Batch | Learning rate | Criterion | F1 val | Precision | Recall | F1 yan | Precision | Recall |
| - | ------ | ----- | ------------- | --------- | ------ | --------- | ------ | ------ | --------- | ------ |
| 1 | 10 | 64 | 0.0001 | CEL | 0.5128 | 0.6189 | 0.6169 | 0.8857 | 0.9069 | 0.8715 |
| 2 | 5 | 32 | 0.001 | CEL | 0.4952 | 0.5547 | 0.609 | 0.9086 | 0.9086 | 0.9086 |
| 3 | 5 | 16 | 0.001 | CEL | 0.5009 | 0.6285 | 0.6162 | 0.869 | 0.9088 | 0.8453 |
| 4 | 10 | 64 | 0.0001 | MSE | 0.7222 | 0.7374 | 0.7163 | 0.8811 | **0.9106** | 0.8629 |
| 5 | 7 | 32 | 0.001 | MSE | 0.7244 | 0.7588 | 0.7186 | 0.8665 | 0.9034 | 0.8434 |
| 6 | 5 | 16 | 0.001 | MSE | 0.7291 | 0.7462 | 0.7232 | 0.8702 | 0.9096 | 0.8468 |
___
Models trained on rubert-tiny2 embeddings (256 neurons).
| № | Epochs | Batch | Learning rate | Criterion | F1 val | Precision | Recall | F1 yan | Precision | Recall |
| - | ------ | ----- | ------------- | --------- | ------ | --------- | ------ | ------ | --------- | ------ |
| 22 | 15 | 128 | 0.001 | CEL | 0.4878 | 0.6388 | 0.6034 | **0.8839** | 0.9035 | 0.8704 |
| 23 | 10 | 64 | 0.001 | CEL | 0.4814 | 0.5769 | 0.6002 | 0.8472 | 0.9092 | 0.8131 |
| 24 | 7 | 32 | 0.001 | CEL | 0.4863 | 0.6194 | 0.6036 | 0.7801 | 0.9085 | 0.7191 |
| 25 | 5 | 16 | 0.001 | CEL | 0.4692 | 0.5594 | 0.5685 | 0.6084 | 0.9127 | 0.5146 |
| 26 | 15 | 128 | 0.001 | MSE | 0.7177 | 0.7463 | 0.7102 | 0.7968 | 0.9064 | 0.7419 |
| 27 | 10 | 64 | 0.001 | MSE | 0.7203 | 0.7369 | 0.7161 | 0.8758 | 0.9052 | 0.8569 |
| 28 | 7 | 32 | 0.001 | MSE | 0.7178 | 0.7373 | 0.7134 | 0.8753 | 0.9034 | 0.8569 |
| 29 | 5 | 16 | 0.001 | MSE | 0.7103 | 0.7371 | 0.703 | 0.8556 | 0.91 | 0.825 |
