# cf860
TMU CIND860  - Advanced Data Analytics Project

Diabetic Retinopathy Detection and Classification


NOTE: I have swapped out the RFMiD2.0 dataset in favor of the Kaggle APTOS 2019 Blindness Detection competition dataset (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

Files:

Nov 4

1. AptosDatasetLoader.ipynb: This file:
  * downloads the APTOS dataset zip file (9.51GB) from the Kaggle APTOS 2019 Blindness Detection competition to google drive
  * unzips the file
  * Moves the zip contents to the specified google drive folders
    
Nov 4

2. AptosEDAv2.ipynb: Exploratory Data Analysis of APTOS dataset

Nov 4

3. AptosSampler.ipynb: Sampling (for compute and memory resource constraints):
   Sampling (for compute and memory resource constraints):
   * 10% of the 3,662 images from the initial APTOS train_set split 70/30 into train_small and test_small
   * creates .csv files train_small and test_small with 'id_code' and 'diagnosis' for the corresponding sample sets
   * original class balances preserved

Nov 5

4. AptosSamplerTrain.ipynb: Sampling (for compute and memory resource constraints):
   Sampling (for compute and memory resource constraints):
   * Difference from '3.AptosSampler.ipynb' - deal with train/test split split in subsequent modeling files
   * 10% of the 3,662 images from the initial APTOS train_setinto train_small2
   * creates .csv file train_small and test_small with 'id_code' and 'diagnosis' for the corresponding sample set
   * original class balances preserved
