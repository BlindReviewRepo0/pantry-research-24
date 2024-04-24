# Code Repository

## Introduction 

Code Repository of "Socioeconomic and Geographic Disparities in ...." [Full title to be revealed after acceptance]. Please note that all dataset needed for this study will be available upon request. 

----------
## How to replicate results in Conda Environment

- Install Anaconda. Enable pip dependency. 
- Create a conda environment named `fp_env`. 

```conda
conda create -n fp_env python=3.8
pip install -r requirements.txt
conda install -c conda-forge googlemaps
```
- After creating the virtual environment `fp_env`, run the following command to activate the environment: 
```conda
conda activate fp_env
```

- Place the following data files from the attached Google Drive to the `data` folder in the repository ([Google Drive Link to Data](https://drive.google.com/drive/folders/1t_jOIKYtD_pKVYPa9V6dU00FPQ6RoHv7?usp=sharing)):
    - `fp_bg_pairs.pkl` (37.1M pairs of pantry and BGs in the U.S.)
    - `bg_pantry_travel_time_updated.csv` (~238K BG and pantry pairs with transit time information)
    - `metro_fp_regression.csv` (ALL BGs in urban area with their distance to FP, ADI, travel time, accessibility, etc)
	- `rural_fp_regression.csv` (ALL BGs in rural area with their distance to FP, ADI, driving distance, accessibility, etc)
    - `ruralurbancodes2013.csv` (US county and rural/urban codes)
    - `US_2020_ADI_Census Block Group_v3.2.csv` (2020 ADI percentiles)
    - `us-state-fips.csv` (All US states and their FIPS code)
	- `nhgis0001_ds258_2020_blck_grp` (All BGs and land areas can be found in this file. For a detailed description, see `nhgis0001_ds258_2020_blck_grp_codebook.txt`)
- Run `main_urban_rural.ipynb` to replicate the results in main body texts. 
- Run `accessibility_regression_urban_rural.ipynb` to replicate the results in regression analysis. (Supplementary Table 1)
- Run `Land_area_analysis.ipynb` to replicate the results in land area analysis (Supplementary Table 2 and Supplementary Figure 8). 
- Run `data_validation/validation_supplementary_figures.ipynb` to replicate the results in FP data validation and Supplementary Figure 1. 


Please note that `prepare_data.ipynb` and `compute_travel_time.ipynb` are to show how we were able to prepare our dataset for the main study. This files will take considerable amount of time and require your own API key, so please skip to `main.ipynb` to observe the results and understand insights about our study. 

For Figure 3, Supplementary Figures 2 to 7, they were created by Tableau Desktop and require you to have your own API key to access the visuals. 

