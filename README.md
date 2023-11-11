# cf860
TMU CIND860  - Advanced Data Analytics Project

Diabetic Retinopathy Detection and Classification


NOTE: I have swapped out the RFMiD2.0 dataset in favor of the Kaggle APTOS 2019 Blindness Detection competition dataset (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

Files:

Nov 10

Nov 8
   Transfer_learning_and_finetuningNov7v2.ipynb
   * Based on https://www.tensorflow.org/tutorials/images/transfer_learning
   * As of Nov 8, does not work correctly. In[86] model.fit - val_accuracy is 0.2692 for all epochs. Likewise in IN[93] (fine-tuning), val_accuracy is 0.5 for all epochs


Nov 5

   AptosSamplerTrain.ipynb: Sampling (for compute and memory resource constraints):
   Sampling (for compute and memory resource constraints):
   * Difference from '3.AptosSampler.ipynb' - deal with train/test split split in subsequent modeling files
   * 10% of the 3,662 images from the initial APTOS train_setinto train_small2
   * creates .csv file train_small and test_small with 'id_code' and 'diagnosis' for the corresponding sample set
   * original class balances preserved
  
Nov 4

  AptosDatasetLoader.ipynb: This file:
  * downloads the APTOS dataset zip file (9.51GB) from the Kaggle APTOS 2019 Blindness Detection competition to google drive
  * unzips the file
  * Moves the zip contents to the specified google drive folders
    
Nov 4
 
 AptosEDAv2.ipynb: Exploratory Data Analysis of APTOS dataset

Nov 4

   AptosSampler.ipynb: Sampling (for compute and memory resource constraints):
   Sampling (for compute and memory resource constraints):
   * 10% of the 3,662 images from the initial APTOS train_set split 70/30 into train_small and test_small
   * creates .csv files train_small and test_small with 'id_code' and 'diagnosis' for the corresponding sample sets
   * original class balances preserved

