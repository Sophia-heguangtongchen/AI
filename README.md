# Traffic Sign Recognition Project

## Introduction
Write an AI to identify which traffic sign appears in a photograph.



## Experiment 1: Adding Dropout Layers
Without altering the model's structure, only dropout layers were added at the end.

Observing the results, in the early stages of training, adding dropout layers slowed down the rate of loss reduction, and the accuracy was lower compared to the model without dropout layers. However, in the end, the model with dropout layers achieved better accuracy and lower loss. Additionally, it exhibited improved generalization performance.

without adding dropout layers：
Epoch 1/10
500/500 [==============================] - 18s 32ms/step - loss: 1.9664 - accuracy: 0.6291  
Epoch 2/10
500/500 [==============================] - 14s 29ms/step - loss: 0.3734 - accuracy: 0.9020
Epoch 3/10
500/500 [==============================] - 16s 31ms/step - loss: 0.2130 - accuracy: 0.9441
Epoch 4/10
500/500 [==============================] - 15s 30ms/step - loss: 0.1589 - accuracy: 0.9588
Epoch 5/10
500/500 [==============================] - 14s 28ms/step - loss: 0.1494 - accuracy: 0.9607
Epoch 6/10
500/500 [==============================] - 15s 29ms/step - loss: 0.1133 - accuracy: 0.9688
Epoch 7/10
500/500 [==============================] - 14s 29ms/step - loss: 0.1146 - accuracy: 0.9700
Epoch 8/10
500/500 [==============================] - 14s 28ms/step - loss: 0.1526 - accuracy: 0.9610
Epoch 9/10
500/500 [==============================] - 14s 29ms/step - loss: 0.1053 - accuracy: 0.9732
Epoch 10/10
500/500 [==============================] - 14s 28ms/step - loss: 0.1040 - accuracy: 0.9735
333/333 - 3s - loss: 0.2702 - accuracy: 0.9395 - 3s/epoch - 8ms/step

with the addition of dropout layers：
Epoch 1/10
500/500 [==============================] - 15s 28ms/step - loss: 2.8832 - accuracy: 0.3257
Epoch 2/10
500/500 [==============================] - 14s 28ms/step - loss: 1.0674 - accuracy: 0.6993
Epoch 3/10
500/500 [==============================] - 14s 28ms/step - loss: 0.6238 - accuracy: 0.8171
Epoch 4/10
500/500 [==============================] - 14s 27ms/step - loss: 0.4656 - accuracy: 0.8639
Epoch 5/10
500/500 [==============================] - 14s 27ms/step - loss: 0.3518 - accuracy: 0.8966
Epoch 6/10
500/500 [==============================] - 15s 29ms/step - loss: 0.2848 - accuracy: 0.9182
Epoch 7/10
500/500 [==============================] - 16s 32ms/step - loss: 0.2642 - accuracy: 0.9246
Epoch 8/10
500/500 [==============================] - 15s 29ms/step - loss: 0.2537 - accuracy: 0.9279
Epoch 9/10
500/500 [==============================] - 16s 31ms/step - loss: 0.2151 - accuracy: 0.9398
Epoch 10/10
500/500 [==============================] - 14s 29ms/step - loss: 0.1837 - accuracy: 0.9480
333/333 - 3s - loss: 0.1125 - accuracy: 0.9733 - 3s/epoch - 8ms/step


## Experiment 2:an additional hidden layer with 256 neurons was added.
Observing the results, compared to the original model and the second model, 
this model has the lowest accuracy, indicating that having more hidden layers does not necessarily result in higher accuracy.
Epoch 1/10
500/500 [==============================] - 17s 31ms/step - loss: 3.1421 - accuracy: 0.2050  
Epoch 2/10
500/500 [==============================] - 16s 31ms/step - loss: 1.8165 - accuracy: 0.4516
Epoch 3/10
500/500 [==============================] - 15s 30ms/step - loss: 1.2425 - accuracy: 0.6214
Epoch 4/10
500/500 [==============================] - 16s 32ms/step - loss: 0.8754 - accuracy: 0.7264
Epoch 5/10
500/500 [==============================] - 14s 29ms/step - loss: 0.6643 - accuracy: 0.7932
Epoch 6/10
500/500 [==============================] - 14s 29ms/step - loss: 0.5566 - accuracy: 0.8330
Epoch 7/10
500/500 [==============================] - 14s 29ms/step - loss: 0.4544 - accuracy: 0.8704
Epoch 8/10
500/500 [==============================] - 14s 29ms/step - loss: 0.3965 - accuracy: 0.8871
Epoch 9/10
500/500 [==============================] - 14s 28ms/step - loss: 0.3550 - accuracy: 0.8968
Epoch 10/10
500/500 [==============================] - 14s 29ms/step - loss: 0.3520 - accuracy: 0.9044
333/333 - 3s - loss: 0.2198 - accuracy: 0.9412 - 3s/epoch - 8ms/step

### Based on accuracy and the generalization performance of the model, I choose the model from the second experiment.