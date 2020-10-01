
###-----------------------------------------------------------------------------------------------------------------------------
This is the instruction for running the code for the paper submitted to ICLR-2021:
"On the Discovery of Feature Importance Distribution: An Overlooked Area"


1. Place folder "fid" in your working directory

2. Skip this step if you are fine with running the code in parallel using 10 CPU cores
   Otherwise, use the following commands to specify n_jobs (number of CPU cores used when parallelizing, the default value is 10):
   
   vim ./fid/code/script/run_all.txt
   vim ./fid/code/python/fiblr/Setting.py
   vim ./fid/code/python/others/Setting.py

   Please note that it took us around 15 hours to complete testing the three methods on the 5 real-world datasets (when running the code in parallel using 10 CPU cores). The high running time is partially due to a large dataset (Alternative splicing), and partially due to fine-tuning the hyperparameters (using 10-fold cross-validation) of each method tested in the experiments.

3. Skip this step if you are fine with running the code using the same parameter grids used in our experiments (for hyperparameter tuning) 
   Otherwise, use the following commands to specify your own parameter grids:
   
   vim ./fid/code/python/fiblr/Setting.py
   vim ./fid/code/python/others/Setting.py

   Please note that using different parameter grids could lead to results different from those reported in the paper

4. Use the following command to run the code:

   ./fid/code/script/run_all.txt

###-----------------------------------------------------------------------------------------------------------------------------



###-----------------------------------------------------------------------------------------------------------------------------
These are the requirements for the environments. Please note that they are not the minimum requirements. Instead, they are the ones that enable the above instruction to work.


1. Install Anaconda
   Go to: https://docs.anaconda.com/anaconda/install/ (or google install anaconda when broken link)
   Go to the "System requirements" section, choose your operating system and follow the corresponding instructions

2. Install imblearn (for oversampling the minority classes)
   Use the following command to install imblearn:

   conda install -c conda-forge imbalanced-learn

###-----------------------------------------------------------------------------------------------------------------------------


