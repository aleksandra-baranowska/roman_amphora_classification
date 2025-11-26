# roman_amphora_classification

This project explored a dataset of Roman amphora stamps, types, find locations, and associated Roman provinces. The goal was to train a machine learning model capable of predicting the likely province of origin for a given artifact, based on the stamp text and vessel type. The project investigates whether stamped codes or amphora types can be used to predict the Roman province associated with an artifact. Ultimately, it aims to combine archaeological reasoning with computational approaches.

## Files in the repository:

- Jupyter notebook containing the code used to conduct exploratory data analysis, model training and evaluation, and a single example prediction
- classififcation_report - a full per-class evaluation output
- EDA plots

## Libraries used:  
pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  

## Dataset
The dataset was provided by Project Mercury, and is available on the website: 
https://projectmercury.eu/datasets/#cities under "Amphora stamps (CEIPAC: Rubio et al. 2018)", originally from:  
Rubio-Campillo, X., Montanier,, J.M., Rull, G., Bermúdez Lorenzo, J.M., Moros Díaz, J., Pérez González, J., Remesal Rodríguez, J. (2018) The ecology of Roman trade. Reconstructing provincial connectivity with similarity measures, Journal of Archaeological Science, 92, pp. 37-47. doi:10.1016/j.jas.2018.02.010

## Model and training

A logistic regression classifier was trained on "code" and "type" do predict "name" (province). The results are as follows:
| Metric     | Value   |
|------------|---------|
| Accuracy   | 0.54    |
| Precision  | 0.31    |
| Recall     | 0.19    |
| F1 Score   | 0.21    |

The evaluation metrics are much better for individual classes which were heavily overrepresented in the dataset. F1 score for the best-performing classes:
Italia	0.825451
Lusitania	0.724138
Tarraconensis	0.667333
| Province      | F1 value |
|---------------|----------|
| Italia        | 0.82     |
| Lusitania     | 0.72     |
| Tarraconensis | 0.67     |

