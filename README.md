Dataset:
## UCI Machine Learning Repository - Connectionist Bench (Sonar, Mines vs. Rocks)
Sejnowski,Terry and Gorman,R.. Connectionist Bench (Sonar, Mines vs. Rocks). UCI Machine Learning Repository. https://doi.org/10.24432/C5T01Q.

#####
SpotOnCheck  
Sonar Ensemble is a Showcase Project to introduce simple Ensemble Methods and the effects of Tuning Hyperparameters.
With a variety of different classifiers, we want to get a first look and start a comparision of classifiers. Since the dataset
is a classification problem, we start via comparing the logloss metric.
Without surprise, tree-based boosting models are performing best, so we keep these models for the next step.
##
Building Ensemble  
Regarding for creating a suitable benchmark, we take the best models and compare their results with a stacking classifier and a soft voting classifier aswell on it.
There is a good performance boost visible with the soft voting classifier.
##
Hyperparameter Tuning  
For the inidividual models, we are performing a Hyperparameter Search with Optuna. The best performing parameters for the corresponding models are saved.
##
Ensembles with tuned Hyperparameter
The best Hyperparameters are passed to the models and we are repeating our Ensemble building with the tuned Hyperparameters.
The logloss metris are not improving on point, but the standard derivation is improving significant, which results in more robost and better model building.

