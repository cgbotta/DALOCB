> **Note:**
> After cloning the repo, you need to download additional data to run the main experiments.


Step 1: Setup Environment
1. Go to the top level of this project, at the same level as this README and requirements.txt
2. Create a new virtual environment
    - python3 -m venv ./venv
3. Activate the virtual environment
    - source venv/bin/activate
4. Install the required Python packages from requirements.txt
    - pip install -r requirements.txt

Step 2: Load the Data
1. The full Eedi dataset is used in this project, and needs to be downloaded. Go to the following link: https://eedi.com/projects/neurips-education-challenge and scroll down to the Dataset section and click "Download Eedi Dataset".
2. From the downloaded data, you will need to move the "metadata" directory and "train_data" directory into this repository under the (currently empty) DALOCB/data/eedi directory. You will now have the following:
    - DALOCB/data/eedi/metadata
    - DALOCB/data/eedi/train_data

Step 3: Running DALOCB Experiments
1. Navigate to ./DALOCB/code
2. All experiments are run using main.py as follows:
    - python3 main.py --experiment [EXPERIMENT]
3. python3 main.py --help shows a list of all available experiments
    - eedi_compare
        - Comparing LOCB, DALOCB, and DALOCB + static on Eedi dataset
    - ednet_compare
        - Comparing LOCB and DALOCB on EdNet dataset
    - ednet_compare_cluster_size
        - Comparing different cluster size hyperparameters on EdNet dataset
    - ednet_compare_user_update_frequency
        - Comparing different user update frequency hyperparameters on EdNet dataset
    - ednet_compare_cluster_update_frequency
        - Comparing different cluster update frequency hyperparameters on EdNet dataset

4. For Example:
    - python3 main.py --experiment ednet_compare

Step 4: Running Bibtex Experiments
1. Navigate to ./Bibtext/code
2. Run
    - python3 contextual_bandit_simulations.py

Additional Data
1. This project does *not* use the full EdNet data due to its large size. Instead, we selected 50 student CSV files from KT1. The full dataset is available for download here: https://github.com/riiid/ednet

If you would like to use or reference this work:
- This code is the product of the forthcoming dissertation, titled "Diversity-Aware Local Clustering in Bandits" submitted by Colton Botta for the degree of Master of Science, School of Informatics, University of Edinburgh, 2022. A link to the full dissertation will be added once publicly released.