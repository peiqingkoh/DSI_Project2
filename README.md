
#### Project directory:
Project2
|__ code 
|   |__ 01_ModelSelection.ipynb
|   |__ 02_Kaggle_Submissions.ipynb   
|__ datasets
|   |__ train.csv
|   |__ test.csv
|   |__ predictions.csv
|   |__ newtrain.csv
|__ files
|   |__ kaggle.png  
|__ README.md



#### Data science process as follows:
- Define the problem.
- Obtain the data.
- Explore the data.
- Model the data.
- Evaluate the model.
- Answer the problem.



#### With the given sets of data , the following steps are done
- Problem Statements
- Data Import and cleaning
- Exploratory Data Analysis & Feature Engineering
- Modelling & Evaluating
- Business Recommendations


#### After all the cleaning, EDA & features engineering, a final data set was created to do the modelling.
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**year_built**|*integer*|Train|Original construction date|
|**year_remod/add**|*integer*|Train|Remodel date (same as construction date if no remodeling or additions)|
|**mas_vnr_area**|*integer*|Train| Masonry veneer area in square feet|
|**total_bsmt_sf**|*integer*|Train|Total square feet of basement area|
|**1st_flr_sf**|*integer*|Train|First Floor square feet| 
|**gr_liv_area**|*integer*|Train|Above grade (ground) living area square feet|
|**full_bath**|*integer*|Train|Full bathrooms above grade|
|**totrms_abvgrd**|*integer*|Train|Total rooms above grade (does not include bathrooms)|
|**garage_cars**|*integer*|Train|Size of garage in car capacity|
|**garage_area**|*integer*|Train|Size of garage in square feet|
|**saleprice**|*integer*|Train|Sale price $$|
|**mssub_30**|*integer*|--|type of dwelling:1-STORY 1945 & OLDER (using one hot encoding)|
|**mssub_40**|*integer*|--|type of dwelling:1-STORY W/FINISHED ATTIC ALL AGES(using one hot encoding)|
|**mssub_45**|*integer*|--|type of dwelling:1-1/2 STORY - UNFINISHED ALL AGES (using one hot encoding)|
|**mssub_50**|*integer*|--|type of dwelling:1-1/2 STORY FINISHED ALL AGES (using one hot encoding)|
|**mssub_60**|*integer*|--|type of dwelling:2-STORY 1946 & NEWER (using one hot encoding)|
|**mssub_70**|*integer*|--|type of dwelling:2-STORY 1945 & OLDER (using one hot encoding)|
|**mssub_75**|*integer*|--|type of dwelling:2-1/2 STORY ALL AGES (using one hot encoding)|
|**mssub_80**|*integer*|--|type of dwelling:SPLIT OR MULTI-LEVEL (using one hot encoding)|
|**mssub_85**|*integer*|--|type of dwelling:SPLIT FOYER (using one hot encoding)|
|**mssub_90**|*integer*|--|type of dwelling:DUPLEX - ALL STYLES AND AGES (using one hot encoding)|
|**mssub_120**|*integer*|--|type of dwelling:1-STORY PUD (Planned Unit Development) - 1946 & NEWER (using one hot encoding)|
|**mssub_150**|*integer*|--|type of dwelling:1-1/2 STORY PUD - ALL AGES (using one hot encoding)|
|**mssub_160**|*integer*|--|type of dwelling:2-STORY PUD - 1946 & NEWER (using one hot encoding)|
|**mssub_180**|*integer*|--|type of dwelling:PUD - MULTILEVEL - INCL SPLIT LEV/FOYER (using one hot encoding)|
|**mssub_189**|*integer*|--|type of dwelling:2 FAMILY CONVERSION - ALL STYLES AND AGES (using one hot encoding)|
|**Res_Yes**|*integer*|--|Using train data set columns MS Zoning to create new column whether is it residential type(using one hot encoding)|
|**shapereg_Yes**|*integer*|--|Using train data set columns Lot Shape to create new column whether the shape of the lot is regular (using one hot encoding)|
|**lotInside_Yes**|*integer*|--|Using train data set columns Lot Config to create new column whether the lot configuration is "Inside" type (using one hot encoding)|
|**neigh_Blueste**|*integer*|--|Physical locations within Ames city limits:Bluestem(using one hot encoding) |
|**neigh_BrDale**|*integer*|--|Physical locations within Ames city limits:Briardale(using one hot encoding)|
|**neigh_BrkSide**|*integer*|--|Physical locations within Ames city limits:Brookside(using one hot encoding)|
|**neigh_ClearCr**|*integer*|--|Physical locations within Ames city limits:Clear Creek(using one hot encoding)|
|**neigh_CollgCr**|*integer*|--|Physical locations within Ames city limits:College Creek (using one hot encoding) |
|**neigh_Crawfor**|*integer*|--|Physical locations within Ames city limits:Crawford (using one hot encoding) |
|**neigh_Edwards**|*integer*|--|Physical locations within Ames city limits:Edwards (using one hot encoding) |
|**neigh_Gilbert**|*integer*|--|Physical locations within Ames city limits:Gilbert (using one hot encoding) |
|**neigh_Greens**|*integer*|--|Physical locations within Ames city limits:Greens (using one hot encoding) |
|**neigh_GrnHill**|*integer*|--|Physical locations within Ames city limits:Green Hills (using one hot encoding) |
|**neigh_IDOTRR**|*integer*|--|Physical locations within Ames city limits:Iowa DOT and Rail Road (using one hot encoding) |
|**neigh_Landmrk**|*integer*|--|Physical locations within Ames city limits:Landmark (using one hot encoding) |
|**neigh_Mitchel**|*integer*|--|Physical locations within Ames city limits:Mitchell (using one hot encoding) |
|**neigh_NAmes**|*integer*|--|Physical locations within Ames city limits:North Ames (using one hot encoding) |
|**neigh_NWAmes**|*integer*|--|Physical locations within Ames city limits:Northwest Ames (using one hot encoding) |
|**neigh_NoRidge**|*integer*|--|Physical locations within Ames city limits:Northridge (using one hot encoding) |
|**neigh_NridgHt**|*integer*|--|Physical locations within Ames city limits:Northridge Heights (using one hot encoding) |
|**neigh_OldTown**|*integer*|--|Physical locations within Ames city limits:Old Town (using one hot encoding) |
|**neigh_SWISU**|*integer*|--|Physical locations within Ames city limits:South & West of Iowa State University (using one hot encoding) |
|**neigh_Sawyer**|*integer*|--|Physical locations within Ames city limits:Sawyer (using one hot encoding) |
|**neigh_SawyerW**|*integer*|--|Physical locations within Ames city limits:Sawyer West (using one hot encoding) |
|**neigh_Somerst**|*integer*|--|Physical locations within Ames city limits:Somerset (using one hot encoding) |
|**neigh_StoneBr**|*integer*|--|Physical locations within Ames city limits:Stone Brook (using one hot encoding) |
|**neigh_Timber**|*integer*|--|Physical locations within Ames city limits:Timberland (using one hot encoding) |
|**neigh_Veenker**|*integer*|--|Physical locations within Ames city limits:Veenker (using one hot encoding) |
|**1story_Yes**|*integer*|--|Using train data set columns House Style to create new column whether is house is single story(using one hot encoding)|
|**overallqty_below**|*integer*|--|Using train data set columns Overall Qual to create new column whether overall material and finishing is above average(using one hot encoding)|
|**overcond_below**|*integer*|--|Using train data set columns Overall Qual to create new column whether overall house condition is above average(using one hot encoding)|
|**rfstyle_Gable**|*integer*|--|Type of roof:Gable (using one hot encoding)|
|**rfstyle_Gambrel**|*integer*|--|Type of roof:Gable (using one hot encoding)|
|**rfstyle_Hip**|*integer*|--|Type of roof:Hip (using one hot encoding)|
|**rfstyle_Mansard**|*integer*|--|Type of roof:Mansard (using one hot encoding)|
|**rfstyle_Shed**|*integer*|--|Type of roof:Shed (using one hot encoding)|
|**mat_morethan1_1**|*integer*|--|Using train data set columns Exterior 1 & Exterior 2  to create new column whether more than 1 materials are used for exterior(using one hot encoding)| 
|**mvtype_BrkFace**|*integer*|--|Mas Vnr Type:Brick Face (using one hot encoding)|
|**mvtype_None**|*integer*|--|Mas Vnr Type:Brick Face (using one hot encoding)|
|**mvtype_Stone**|*integer*|--|Mas Vnr Type:Stone (using one hot encoding)|
|**extqual_below**|*integer*|--|Using train data set columns Exter Qual to create new column whether exterior is above average(using one hot encoding)| 
|**fnd_CBlock**|*integer*|--|Type of foundation:Cinder Block (using one hot encoding)|
|**fnd_PConc**|*integer*|--|Type of foundation:fnd_PConc (using one hot encoding)|
|**fnd_Slab**|*integer*|--|Type of foundation:fnd_Slab (using one hot encoding)|
|**fnd_Stone**|*integer*|--|Type of foundation:Stone (using one hot encoding)|
|**fnd_Wood**|*integer*|--|Type of foundation:Wood (using one hot encoding)|
|**bsmtheight_below80inc**|*integer*|--|Using train data set columns Bsmt Qual  to create new column to group on basement height(using one hot encoding)|
|**bsmtexp_Yes**|*integer*|--|Using train data set columns Bsmt Exposure to create new column whether there is basement exposure(using one hot encoding)|
|**bsmtfin_Yes**|*integer*|--|Using train data set columns BsmtFin Type  to create new column whether basement area is finished(using one hot encoding)|
|**heatqc_below**|*integer*|--|Using train data set columns HeatingQC to create new column whether heating quality is above avg(using one hot encoding)|
|**kitqc_below**|*integer*|--|Using train data set columns KitchenQualC to create new column whether Kitchen quality is above avg(using one hot encoding)|
|**firepl_Yes**|*integer*|--|Using train data set columns FireplaceQu to create new column whether is there fireplace(using one hot encoding)|
|**gartyp_Attchd**|*integer*|--|Garage location:Attached to home(using one hot encoding)|
|**gartyp_Basment**|*integer*|--|Garage location:Basement Garage(using one hot encoding)|
|**gartyp_BuiltIn**|*integer*|--|Garage location:Built-In(using one hot encoding)|
|**gartyp_CarPort**|*integer*|--|Garage location:Car Port(using one hot encoding)|
|**gartyp_Detchd**|*integer*|--|Garage location:Detached from home(using one hot encoding)|
|**gartyp_None**|*integer*|--|Garage location:No Garage(using one hot encoding)|
|**garfin_Unfinish**|*integer*|--|Using train data set columns Garage Finish to create new column whether garage Interior finished or not(using one hot encoding)|
    

#### Modelling was done using lasso so to reduce the number features.
#### Unfortunately, number of feaures is still more than the targeted 25. So selection is based on the coeff. to do the selection
#### The next iteration of modelling should be done is going through the selected features and apply domain knowledge to reselect. Example would be features like garage cars and garage area is correlated in one way or another. So i should only be using one of the it instead of both. Modelling should also be tired on ridge to compare the performance. 


