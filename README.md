# cf860
TMU CIND860  - Advanced Data Analytics Project

Nov 4

1. AptosDatasetLoader.ipynb: This file
  * downloads the APTOS dataset zip file (9.51GB) from the Kaggle APTOS 2019 Blindness Detection competition (https://www.kaggle.com/competitions/aptos2019-  blindness-detection/data) to google drive
  * unzips the file
  * Moves the zip contents to the specified google drive folders

2. AptosEDAv2.ipynb: Exploratory Data Analysis of APTOS dataset (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data?select=test_images)

3. AptosSampler.ipynb: Sampling (for compute and memory resource constraints):
  * 10% of the 3,662 images from the initial APTOS training set split 70/30 into train_small and test_small
  * Original class balances preserved
