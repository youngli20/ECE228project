--------------------------------------------------------------------------------
                                README
                        Modulation Classification
             Group 38: Kartik Kulgod, Young Li, Parker Martin
--------------------------------------------------------------------------------
-- Loading Instructions

    1.  All of our code is in one file, CNN_Modulation_Classifier.ipynb. 
    2.  To run it, you will need our dataset. Download the "RadioML 2016.10A" 
        dataset from https://www.deepsig.ai/datasets. Extract the dataset from 
        the tarball.
    3.  Upload RML2016.10a_dict.pkl and CNN_Modulation_Classifier.ipynb to 
        datahub.  

--------------------------------------------------------------------------------
-- Running Instructions

Our code is well organized, and divided into sections and subsections. Please
refer to "Code Table of Contents" below to see the structure of our Jupyter 
Notebook.

    1.  Open CNN_Modulation_Classifier.ipynb. It should be in the same directory
        as your RML2016.10a_dict.pkl dataset on datahub.
    2.  Use a Python 3 Kernel.
    3.  You can run the entire file from start to finish. This will show the 
        progress we made in model accuracy over the course of hyperparameter 
        tuning.
    4.  You can alternatively run our final model only by running:
            - All of Section 1 (General Setup)
            - All of Section 3 (Convolutional Neural Network: With Dropout)

--------------------------------------------------------------------------------
-- Code Table of Contents (CNN_Modulation_Classifier.ipynb)

1. General Setup
    1.1 Import Statements
    1.2 Load Dataset
    1.3 Visualize Example Time Series from Dataset
    1.4 Create Pytorch Dataset Class
    1.5 Create Data Arrays
    1.6 Create DataLoaders for Each Data Array
2. Convolutional Neural Network: No Dropout
    2.1 Define CNN Model (No Dropout)
    2.2 Train with Positive SNR Only (0 to 18 dB)
        2.2.1 Intialize NN, Optimizer, and Loss Function
        2.2.2 Train Neural Net with Positive SNR Data Only (0 to 18 dB)
            2.2.2.1 Plot Training Loss vs Epoch
            2.2.2.2 Save Model Parameters
        2.2.3 Test Neural Net
            2.2.3.1 Print Model Accuracy vs SNR
            2.2.3.2 Plot Model Accuracy vs SNR
    2.3 Train with All SNR Data (-20 to 18 dB)
        2.3.1 Intialize NN, Optimizer, and Loss Function
        2.3.2 Train Neural Net with All SNR Data (-20 to 18 dB)
            2.3.2.1 Plot Training Loss vs Epoch
            2.3.2.2 Save Model Parameters
        2.3.3 Test Neural Net
            2.3.3.1 Print Model Accuracy vs SNR
            2.3.3.2 Plot Model Accuracy vs SNR
    2.4 Modify Train/Test Split Ratio and Check for Overfitting
        2.4.1 Create New DataLoaders with 70:30 Train/Test Split for Positive 
              SNR Data
        2.4.2 Intialize NN, Optimizer, and Loss Function
        2.4.3 Define Function for Testing Against Validation Data (No Dropout)
        2.4.4 Train Neural Net and Test with Validation Data
            2.4.4.1 Plot Training and Validation Loss vs Epoch
            2.4.4.2 Plot Training and Validation Loss vs Epoch (Paper Version)
            2.4.4.3 Save Model Parameters
        2.4.5 Test Neural Net
            2.4.5.1 Print Model Accuracy vs SNR
            2.4.5.2 Plot Model Accuracy vs SNR
3. Convolutional Neural Network: With Dropout
    3.1 Define CNN Model (With Dropout)
    3.2 Train with Positive SNR Only (0 to 18 dB) and 70:30 Train/Test Split
        3.2.1 Create New DataLoaders with 70:30 Train/Test Split for Positive 
              SNR Data
        3.2.2 Intialize NN, Optimizer, and Loss Function
        3.2.3 Define Function for Testing Against Validation Data (With Dropout)
        3.2.4 Train Neural Net and Test with Validation Data
            3.2.4.1 Plot Training and Validation Loss vs Epoch
            3.2.4.2 Plot Training and Validation Loss vs Epoch (Paper Version)
            3.2.4.3 Save Model Parameters
        3.2.5 Test Neural Net & Collect Confusion Matrix Data
            3.2.5.1 Print Model Accuracy vs SNR
            3.2.5.2 Plot Model Accuracy vs SNR
            3.2.5.3 Plot Model Accuracy vs SNR (Paper Version)
        3.2.6 Function for Plotting Confusion Matrixes
        3.2.7 Plot Confusion Matrix for Each SNR
4. Miscellaneous
    4.1 Hyperparameter Tuning Results
    
--------------------------------------------------------------------------------