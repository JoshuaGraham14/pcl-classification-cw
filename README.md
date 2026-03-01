# PCL Classification Project

This project detects Patronizing and Condescending Language (PCL) using the Don't Patronize Me dataset.

Trained on Google Colab using NVIDIA RTX PRO 6000 Blackwell Server Edition.

## Predictions 

Predictions (dev.txt and test.txt) can be found in `predictions/`

## Model

The best performing model can be found in `BestModel/FINAL_MODEL.ipynb`

## Notes on implementation

- I spent well over 20 hours trying to improve on my F1 score, but with not much luck and being incredibly frustrating.
- Although my EDA suggested that cutting the max token length at 128 would be fine, in practice my model performed better on experiments using 256.
- My model, despite using a larger and more capable model (DeBERTa vs RoBERTa), only just surpassed the 0.48 baseline, and this is touched upon in my report. But in a nutshell, the small 10% validation split along with the severely imbalanced dataset made making any significant improvements very challenging, and using some sort of k-fold cross-validation or data augmentation techniques would have been a good idea had I had more time!