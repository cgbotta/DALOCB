Setup Environment
1. Go to the top level of this project, at the same level as this README and requirements.txt
2. Create a new virtual environment
    - python3 -m venv ./venv
3. Activate the virtual environment
    - source venv/bin/activate
4. Install the required Python packages from requirements.txt
    - pip install -r requirements.txt

Running DALOCB Experiments
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

Running Bibtex Experiments
1. Navigate to ./Bibtext/code
2. Run
    - python3 contextual_bandit_simulations.py

Additional Data
1. This project does *not* use the full EdNet data due to its large size. Instead, we selected 50 student CSV files from KT1. The full dataset is available for download here: https://github.com/riiid/ednet
2. The full Eedi dataset is used in this project. It was downloaded from here: https://eedi.com/projects/neurips-education-challenge
