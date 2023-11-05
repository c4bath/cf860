# cf860
TMU CIND860  - Advanced Data Analytics Project

Diabetic Retinopathy Detection and Classification

Nov 4

NOTE: I have swapped out the RFMiD2.0 dataset in favor of the Kaggle APTOS 2019 Blindness Detection competition dataset (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

1. AptosDatasetLoader.ipynb: This file:
  * downloads the APTOS dataset zip file (9.51GB) from the Kaggle APTOS 2019 Blindness Detection competition to google drive
  * unzips the file
  * Moves the zip contents to the specified google drive folders
    

2. AptosEDAv2.ipynb: Exploratory Data Analysis of APTOS dataset


3. AptosSampler.ipynb: Sampling (for compute and memory resource constraints):
   Sampling (for compute and memory resource constraints):
   * 10% of the 3,662 images from the initial APTOS training set split 70/30 into train_small and test_small
   * creates .csv files train_small and test_small with 'id_code' and 'diagnosis' for the corresponding sample sets
   * original class balances preserved
