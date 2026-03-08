# Perceptra - PS1 Bone Fracture AI

## Overview
This project focuses on fracture analysis from X-ray radiographs. Our final direction is a 17-class fracture-type classification pipeline trained on the Human Bone Fracture C17 Dataset. We also built a binary fracture vs not-fracture baseline earlier to validate the full engineering pipeline end to end.

## Final Main Run
- Dataset: Human Bone Fracture C17 Dataset
- Total images: 2149
- Classes: 17
- Model: EfficientNet-B3
- Image size: 300
- Epochs run: 18
- Best epoch: 12
- Best validation macro F1: 0.5204
- Test accuracy: 0.5139
- Test macro F1: 0.5069
- Top-3 accuracy: 0.7430
- ROC-AUC OVR Macro: 0.8741
- Inference time: 5.08 ms/image

## Why This Direction
The binary baseline was useful for validating preprocessing, training, checkpointing, explainability, and CSV export. However, the final project direction is the 17-class C17 setup because it is much closer to the fracture-type classification intent of PS1.

## Included Outputs
- final_results.csv
- model_performance_analysis.csv
- per_class_metrics.csv
- test_predictions.csv
- best_model.pth
- training_curves.png
- confusion_matrix.png
- roc_curve.png
- gradcam_examples.png

## Notes
This is a hard fine-grained classification problem with a relatively small and imbalanced dataset. Accuracy alone does not tell the full story, so macro F1, class-wise analysis, ROC behavior, and Grad-CAM were included in the final package.
