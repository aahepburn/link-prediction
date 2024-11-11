# Link Prediction Classifier

## Feature Extraction 

The function create_features extracts various features between pairs of nodes in a graph G using network metrics and node attributes. 

For each pair of nodes:

- Common neighbors: Number of nodes that are neighbors to both nodes.
- Jaccard coefficient: A measure of similarity based on shared neighbors.
- Preferential attachment: A score that measures the likelihood of a link based on node degrees.
- Adamic-Adar index: Another similarity measure based on shared neighbors, weighted by their degrees.
- Same attribute: A binary feature indicating whether the two nodes have the same attribute value.
- Degree difference: Absolute difference in degrees of the two nodes.
- Total degree: Sum of the degrees of the two nodes.
- Average clustering coefficient: The average clustering coefficient of the two nodes.
- Same community: A binary feature indicating if the two nodes belong to the same community based on label propagation.

## Random Forest Model and Hyperparameter Tuning
- Randomized search with cross-validation (RandomizedSearchCV) to tune the model. The model is optimized based on the F1 score.

## Model Evaluation 
The best Random Forest model is evaluated on the test set, where accuracy, precision, recall, and F1 score are printed. Feature importance scores are also displayed.
