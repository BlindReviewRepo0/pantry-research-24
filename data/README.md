# Data File Repository


## 1. About `fp_bg_pairs.pkl`

- The pickle file of 37.1M pairs of food pantries (FPs) and Census Block Groups (BGs) that are located within 25 miles of the FPs. 
- Each column represents: 
    - `address`: address of a FP
    - `ad_lat`: The corresponding FP's GPS latitude
    - `ad_lon`: The corresponding FP's GPS longitude
    - `bg_fips`: The 12-digit FIPS code of a BG that is located within 25 miles of the FP
    - `bg_lat`: The corresponding BG's latitude
    - `bg_lon`: The corresponding BG's longitude
    - `distance_mi`: The haversine distance between the FP and the BG (in mile)

- The file can be loaded by `pandas.read_pickle` and managed with all `pandas` functions. 
    - For example, all the unique addresses of FPs can be collected and stored to a list, by calling `pandas.DataFrame(fp_bg_pairs.pkl)['address'].unique().tolist()`. 


## 2. About `bg_pantry_time_updated.csv`
- The .csv file of ~238K BGs that are identified to be located at least one of FPs within 25 miles. 
- ADI are indicators of socio-economic advantageness of each BG (higher ADI = more disadvantaged BG)
- Each column represents: 
    - `bg_fips`: The 12-digit FIPS code of a BG
    - `address`: address of a FP
    - `distance_mi`: The haversine distance between the FP and the BG (in mile)
    - `transit_time`: the travel time by public transit between a BG and its nearest FP 
    - `walking_time`: the travel time by walking between a BG and its nearest FP 
    - `ADI_NATRANK`: The national ADI percentile of a BG (out of 100) 
    - `ADI_STATERNK`: The ADI decile of a BG within a state (out of 10) 
    - `bg_state`: the state (e.g., MA) of the BG
    - `bg_county`: the FIPS code of the county (e.g., Hampshire County) of the BG
    - `status`: rurality status of a BG
    - `access`: the shortest travel time (transit or walking) between a BG and its nearest FP

## 3. About `metro_fp_regression.csv`
- Each column represents: 
    - `bg_fips`: The 12-digit FIPS code of a BG
    - `address`: address of a FP
    - `distance_mi`: The haversine distance between the FP and the BG (in mile)
    - `transit_time`: the travel time by public transit between a BG and its nearest FP 
    - `walking_time`: the travel time by walking between a BG and its nearest FP 
	- `driving_distance`: the driving distance between a BG and its nearest FP
    - `ADI_NATRANK`: The national ADI percentile of a BG (out of 100) 
    - `ADI_STATERNK`: The ADI decile of a BG within a state (out of 10) 
    - `bg_state`: the state (e.g., MA) of the BG
    - `bg_county`: the FIPS code of the county (e.g., Hampshire County) of the BG
    - `status`: rurality status of a BG
    - `access`: the shortest travel time (transit or walking) between a BG and its nearest FP
	- `catogory`: High, medium or low access
## 4. About `rural_fp_regression.csv`
- Same as `metro_fp_regression.csv`

------ 

## 5. Additional Data

- `ruralurbancodes2013.csv` (US county and rural/urban codes)
- `US_2020_ADI_Census Block Group_v3.2.csv` (2020 ADI percentiles)
- `us-state-fips.csv` (All US states and their FIPS code)
- `nhgis0001_ds258_2020_blck_grp` (All BGs and land areas can be found in this file. For a detailed description, see `nhgis0001_ds258_2020_blck_grp_codebook.txt`)
- `all_rural_rest_pairs_1056_fipstr.csv` (Considering that land areas are typically larger for BGs in rural areas than in urban areas (see land area analysis), for BGs that do not have FPs within 25 miles in rural areas we computed distance of FPs located within 50 miles. This file contains the rest of BGs in rural areasthat have FPs within 50 miles)
