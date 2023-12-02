# cf860
TMU CIND860  - Advanced Data Analytics Project

Diabetic Retinopathy Detection and Classification


NOTE: I have swapped out the RFMiD2.0 dataset in favor of the Kaggle APTOS 2019 Blindness Detection competition dataset as the Primary datast (https://www.kaggle.com/competitions/aptos2019-blindness-detection/data)

The Aptos dataset includes 3,662 CFP images collected from subjects living in rural areas of India

			Sikder, N., Chowdhury, M. S., Arif, A. S. M., & Nahid, A. A. (2019, December). Early blindness detection based on retinal images using ensemble learning. In 2019 22nd International Conference on Computer and Information Technology (ICCIT) (pp. 1-6). IEEE.

Also used is the Diabetic Retinopathy Detection dataset.  It is more genetically and geographically heterogeneous than Aptos and serves as a secondary dataset for testing only

Files:

Nov 30 Module 4 Submission:

Files (shown in order of methodology as presented in Final Report)

1. APTOS_CLAHE_preprocessing.ipynb

   Function: apply image preprocessing (CLAHE) to the APTOS dataset

PLEASE NOTE regarding all EDA files: Pandas Profiling used but output does not display in GitHub.  
All the relevant Pandas Profiling is included in the Final Report.

2. APTOS_EDA.ipynb 

   Function: EDA on the APTOS dataset (i.e. class distribution)

3. APTOS_Image_EDAv1.ipynb

    Function: EDA on the APTOS image files (dimensions and filesize [bytes])

4. DR_Detection_Kaggle_EyePACS_EDA.ipynb

   Function: EDA on the secondary testing Diabetic Retinopathy Detection eyePACS dataset (i.e. class distribution)

5. DR_Detection_EyePACS_Image_EDAv1.ipynb

   Function: EDA on the Diabetic Retinopathy Detection eyePACS dataset image files (dimensions and filesize [bytes])

6. APTOS_FCN_clahe_Tuner.ipynb

   Function: construct a basic CNN and apply hypertuning. Train, validate and test on APTOS and test on Diabetic Retinopathy Detection eyePACS

7. APTOS_FCN_clahe_TUNED_CrossVal_v1.ipynb

   Function: based on the output hypertuned model from APTOS_FCN_clahe_Tuner.ipynb, retrain with 5-fold cross validation and test using APTOS and test on Diabetic Retinopathy Detection eyePACS

8. APTOS_MobileNetv2CLAHE_n29.ipynb

   Function: Use MobileNetV2 pre-trained architecture as basis for initial model, train and validate on APTOS, fine-tune with ImageNet weights to retrain, validate and test on APTOS and test on test on Diabetic Retinopathy Detection eyePACS

9. APTOS_EfficientNetV2B3_CLAHE_n29.ipynb.ipynb

   Function: Use EfficientNetV2B3 pre-trained architecture as basis for initial model, train and validate on APTOS, fine-tune with ImageNet weights to retrain, validate and test on APTOS and test on test on Diabetic Retinopathy Detection eyePACS

10. AptosResNetNov9v3cfg.ipynb

   Function: NOT REFERENCED IN THE FINAL REPORT.  Used as an initial template for transfer learning pipeline

*********************************************************************************

Nov 15

   AptosEDAv3.ipynb: Exploratory Data Analysis of APTOS dataset - corrected the pie chart labels


Nov 10

   AptosResNetNov9v3cfg.ipynb
   
   * This model classifies 5 levels of Diabetic Retinopathy 'No DR', 'Mild', 'Moderate', 'Severe', 'Proliferative DR' and is trained and tested on the full APTOS dataset. It uses transfer learning and is based on ResNet18.  It is adapted from https://www.coursera.org/learn/retinopathy-detection-using-deep-learning/supplement/em4yb/project-based-course-overview

   AptosMobileNetVsNov10v1cfg.ipynb

   * This file uses a MobileNetV2 model to undertake the same task on the same dataset as AptosResNetNov9v3cfg.ipynb.  I'm in the process of diagnosing why it performs extremely poorly - there must be configuration error or other issue.
     
   RFMiD2ResNetNov10v1cfg.ipynb
   
   * This file is based on AptosResNetNov9v3cfg.ipynb but performs a different task (classifying the 5 most prevalent classes (healthy and 4 retinal diseases) on an altogether different dataset RFMiD2.0; I am investigating why the model will not fit: I get an error:  

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

