# Data Validation


## 1. About `data_validation.ipynb`

- This file is used to randomly select 100 food pantries for validation, the resulting data file is `random_100_fp.csv` 


## 2. About `random_100_fp.csv` and `addresses_with_entity_names.csv`
- In `random_100_fp.csv`, each column represents:
    - `addresses`: address of a FP
- In `addresses_with_entity_names.csv`, each column represents: 
    - `address`: address from `random_100_fp.csv`
    - `Entity Name`: The name of the address
    - `Category`: category listed on the Google Map page
    - addtional columns contains related info if found any: website or opening hours


## 3. About `food_pantries_1.csv` and `food_pantries_2.csv`
- `food_pantries_1.csv` and `food_pantries_2.xlsx` contain 150 food pantries, each randomly selected by two evaluators, with three FPs from each of the 50 states. Each file includes the state name, food pantry name, and FP addresses.


## 4. About `missing_fps_details_1.csv` and  `missing_fps_details_2.csv`
- `missing_fps_details_1.csv` and  `missing_fps_details_2.csv` contain the FPs not included in `all_fp_addresses`, which contains all the addresses in our created FP dataset.
- In `missing_fps_details_1.csv`, Each column represents:
    - `fb`: name of the food pantry
    - `address`: The address of the food pantry
    - `type`: category listed on the Google Map page
	- `NumberofReviews`: number of the reviews on the Google Map page
	- `WebsitePresence`: website for the FP
	- `yearsofoperaton`: Establishment year for the food pantry
	- `area`: rural or urban
	- `IfDistribution`: If that is a distribution center
	- `Other`: Other related info for the FP
- In `missing_fps_details_2.csv`, Each column represents:
    - `address`: The address of the food pantry
	- `Name`: name of the food pantry
    - `Website`: website for the FP
	- `NumberofReviews`: number of the reviews on the Google Map page
	- `Rate`: Rate for the food pantry
	- `Years`: Establishment year for the food pantry
	- `IfDistribution`: If that is a distribution center
	- `Other`: Other related info for the FP

## 5. About `validation_supplementary_figures.ipynb`

- `validation_supplementary_figures.ipynb` is used to identify the common and missing FPs. Since we used fuzzy matching to find the common FPs, the results might not be 100% accurate. We performed a manual check, so the original common FPs found by fuzzy matching are saved in `fb_in_common_1.csv` and `fb_in_common_2.csv`. The verified ones are saved in `fb_in_common_1_checked.csv` and `fb_in_common_2_checked.csv`. 
------ 

