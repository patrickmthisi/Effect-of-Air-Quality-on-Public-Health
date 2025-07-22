# Effect-of-Air-Quality-on-Public-Health
## Project aims and description:
In this short study, we aim to investigate the impact of air quality on public health using Google's TabNet classifier on a highly imbalanced multi-class dataset. The following concepts can be gleaned from this study:
 - Performing Bayesian hyperparameter optimisation using Optuna to get an optimal set of hyperparameters for the weighted TabNet model.
 - Constructing a TabNet ensemble classifier.
The dataset for the project was sourced from: https://www.kaggle.com/datasets/rabieelkharoua/air-quality-and-health-impact-dataset.

## Conclusion and recommendation:
The dataset exhibited severe class imbalance, with some classes representing less than 1% of the total samples, as highlighted in the EDA file. To address this, a weighted TabNet classifier was employed to ensure the model gave appropriate attention to minority classes. Since accuracy is an unreliable metric in such contexts, we instead optimized the model using balanced accuracy, which better reflects performance across all classes. An ensemble of 10 TabNet models was then constructed to enhance generalization and robustness. On the out-of-sample test set, the ensemble achieved a weighted average precision of 0.6302 and a ROC AUC of 0.8266, demonstrating its ability to correctly classify instances from under-represented classes.
