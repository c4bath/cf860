# cf860
TMU CIND860  - Advanced Data Analytics Project

Diabetic Retinopathy Detection and Classification


NOTE: I have swapped out the RFMiD2.0 dataset in favor of the Kaggle APTOS 2019 Blindness Detection competition dataset (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

Files:

Nov 10
   AptosResNetNov9v3cfg.ipynb
   * This model classifies 5 levels of Diabetic Retinopathy 'No DR', 'Mild', 'Moderate', 'Severe', 'Proliferative DR'. It uses transfer learning and is based on ResNet18.  It is adapted from https://www.coursera.org/learn/retinopathy-detection-using-deep-learning/supplement/em4yb/project-based-course-overview

   AptosMobileNetVsNov10v1cfg.ipynb
   * This file uses a MobileNetV2 model to undertake the same task on the same dataset as AptosResNetNov9v3cfg.ipynb.  I'm in the process of diagnosing why it performs extremely poorly - there must be configuration error or other issue.
     
   RFMiD2ResNetNov10v1cfg.ipynb
   *THis file is based on AptosResNetNov9v3cfg.ipynb but performs a different task (classifying the 5 most prevalent classes (healthy and 4 retinal diseases) on an altogether different dataset RFMiD2.0 I am investigating why the model will not fit: I get an error  

" ValueError: logits and labels must have the same shape, received "


   
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

