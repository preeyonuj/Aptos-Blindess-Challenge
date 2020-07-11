# Experimenting with Aptos Blindness Challenge 
This repo is a collection of various algorithms and techniques tried on the Aptos Blindess Challenge Dataset. 

## Description
For these experiments, I have divided the Train set into Train, Val and Test, so that I can verify the results as I make improvements in the model. I am also planning to use image transformations to better accentuate the differences.

There are 5 classes in total: <br>
0 - No DR <br>
1 - Mild DR <br>
2 - Moderate DR <br>
3 - Severe DR <br>
4 - Proliferative DR <br>


### Update 1 (09-07-2020):
Set up baseline results with EfficientNet-B1. <br>
Trained the EfficientNet-B1 for 50 epochs. Although model saturates after 15 epochs. <br>
**Results:**<br>
| Confusion Matrix | Predicted class 0 | Predicted class 1 | Predicted class 2 | Predicted class 3 | Predicted class 4 |
| ------------- |:-------------:| :-------------:| :-------------:| :-------------:| :-------------:|
| **Actual class 0** | 273 | 1 | 14 | 0 | 0 |
| **Actual class 1** | 3 | 5 | 51 | 0 | 0 |
| **Actual class 2** | 13 | 5 | 141 | 0 | 0 |
| **Actual class 3** | 0 | 0 | 30 | 0 | 0 |
| **Actual class 4** | 2 | 3 | 42 | 0 | 0 |

Overall Accuracy : 0.71869 <br>
Kappa Score : 0.54697 <br>

It is very apparent that the model is biased towards class 3 i.e. it predicts most of the samples as class 3. Class 3 and 4 literally didn't have a single correct prediction.
