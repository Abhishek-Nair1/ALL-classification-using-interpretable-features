# ALL-classification-using-interpretable-features
Acute Lymphoblastic Leukemia classification using clinically interpretable features, emphasizing interpretability and generalization.

This project focuses on building a machine learning pipeline for classifying Acute Lymphoblastic Leukemia (ALL) using clinically meaningful and medically interpretable features rather than relying solely on low-level image representations. The goal was to align feature engineering with diagnostic criteria used in clinical practice while maintaining strong predictive performance.

Focused on extracting features relating to cells, nucleus shape and size.

## Workflow  

### 1. Data Loading & Visualization
- Loaded image tensors from saved dataset.
- Visualized random samples using Matplotlib.
- Verified class balance using label counts.

### 2. Baseline Model: Raw Pixel Classification
- Images reshaped into 2D feature vectors.
- Stratified train-test split (80–20).
- Random Forest classifier trained on raw pixel features.
- Established a performance benchmark using unstructured pixel information.

### 3. Medically Relevant Feature Engineering
- Extracted clinically interpretable features instead of relying solely on raw pixels.
- Morphological measurements.
- Shape-based descriptors.
- Intensity statistics.

### 4. Model Comparison on Engineered Features
- Evaluated multiple models:
  - Random Forest
  - Gradient Boosting
  - AdaBoost
  - Decision Tree
  - Support Vector Machine
  - k-Nearest Neighbors
  - LightGBM
- Compared performance across models.

### 5. Advanced Model: LightGBM Optimization
- Performed grid search over: num_leaves, learning_rate, n_estimators
- Selected and retrained the best-performing configuration.
