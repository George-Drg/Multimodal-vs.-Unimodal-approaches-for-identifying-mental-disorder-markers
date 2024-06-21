# Multimodal-vs.-Unimodal-approaches-for-identifying-mental-disorder-markers
In this project I made a research on language and speech markers for mental health and I created three different models (1 unimodal text model, 1 unimodal audio model and 1 multimodal model that combines these 2). My purpose was to discover whether multimodal machine learning can perform better in identifying such markers.

> Text Model:
More than 150 features extracted (incl. their statistics).

Features:
- LIWC categories
- GloVe embeddings  (100 dimensions)
- POS-Tag counts
- PCA components (2) and clusters

All features are normalized (with Z-score method) and the feature selection is done using Recursive Feature Elimination (RFE) along with Logistic Regression and Random Forest. 
Modeling is performed on 4 ML models:
- Support Vector Machine
- Logistic Regression
- Random Forest
- Fully connected neural network, Dense Layers

Overfitting check and Visualizations are also present.


> Audio Model:

Similar amount of features, including:
- pitch
- energy
- MFCCs (13 coefficients)
- HNR
- jitter
- shimmer
- formants

All features are normalized and the same feature selection is used. 
Modeling is done on the exact same models (for proper comparison).
Overfitting check and Visualizations are present here as well.


> Multimodal Model:
Early Fusion is being applied to concatenate features of the two modalities.
3 sets of features are created:
- 20 textual features, 10 acoustic features
- 15 textual features, 15 acoustic features
- 20 textual features, 15 acoustic features
The sets were created so that there is enough experimentation concerning weight and number of features variability.

All features are nomrlized here as well and modeling is done on the same 4 ML models.
Overfitting check and Visualizations are present here as well.
