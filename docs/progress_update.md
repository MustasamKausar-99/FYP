# FYP Progress Update

## What I have done so far
- Selected the NSL-KDD dataset and loaded the official training and test files (KDDTrain+.txt and KDDTest+.txt) into Google Colab.
- Confirmed the dataset structure (43 columns including the label) and checked the distribution of classes.
- Converted the problem into binary classification (Normal vs Attack) to match the first stage of the project.
- Preprocessed the data:
  - One-hot encoded categorical features (protocol_type, service, flag)
  - Split data into train/test sets
  - Standardised numerical features using StandardScaler
- Built and tested baseline and hybrid models:
  - Baseline Logistic Regression (for comparison)
  - Hybrid CNN–LSTM model (1D CNN layers + LSTM + dense output)
- Evaluated models using accuracy, precision/recall/F1, and confusion matrix.
- Saved results and uploaded the notebook + screenshots to GitHub for progress tracking.

## Why I used the TXT files (not CSV)
The NSL-KDD repository provides the official dataset in .txt format (comma-separated). Using the TXT versions avoids formatting differences and keeps the dataset consistent with most published research that uses KDDTrain+.txt and KDDTest+.txt. Pandas can read these files the same way as CSV by setting the separator as a comma.

## Current results (summary)
- Logistic Regression achieved a strong baseline performance.
- The CNN–LSTM hybrid achieved higher accuracy than the baseline, showing the hybrid approach improves detection.

## What I will do next
- Train the CNN–LSTM with better tuning (more epochs, early stopping, dropout tuning).
- Evaluate on the official test set (KDDTest+.txt) and report final metrics.
- Extend from binary classification to multi-class attack categories (Normal, DoS, Probe, R2L, U2R) if required by the project scope.
- Start the adversarial attack part (implement the FGSM attack first, then a stronger attack (PGD) and test how accuracy drops under attack and compare robustness.
