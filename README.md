# 🏠 Ames Real Estate Intelligence: High-Precision Valuation Model
## 🎯 The Business Challenge (Addressing Pain Points)
In the volatile Ames housing market, investors and homeowners face three critical risks:

The Overpayment Trap: Paying a premium for properties based on "gut feeling" rather than data-backed value.

Feature Fatigue: With over 80 variables (from roof material to basement height), humans cannot accurately calculate which renovations actually yield the highest ROI.

Outlier Bias: Unusual property sales can distort market averages, leading to expensive valuation errors.

The Solution: This project utilizes an optimized Lasso Regression model to provide a "clean" valuation, capturing 89.32% of price variance while filtering out the noise of irrelevant features.

## 🛠️ Technical Strategy
To ensure the highest accuracy, I implemented a robust machine learning pipeline:

Data Integrity: Handled missing values for 30+ features and utilized Z-Score filtering to remove extreme outliers that skew traditional appraisals.

Feature Engineering: Applied One-Hot Encoding to 23+ neighborhoods and property styles, allowing the model to treat location as a distinct value driver.

Target Optimization: Used Log Transformation on sale prices to stabilize variance and predict percentage-based growth rather than just raw dollars.

The Lasso Filter: Implemented L1 Regularization (Lasso) to automatically perform feature selection, identifying the "True Drivers" of value and muting 0-impact variables.

## 📈 Key Market Insights (What Drives Price?)
Based on the Lasso model coefficients, the top 3 drivers for property value in Ames are:

Above Ground Living Area: Every standard deviation increase in living space correlates to a ~11.5% increase in price.

Overall Quality: Material and finish quality remains a non-linear value multiplier.

Location Premiums: Specific neighborhoods (e.g., Stone Brook, Northridge) carry a significant statistical premium regardless of house size.
Source: [Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-ML0232EN-SkillsNetwork/asset/Ames_Housing_Data1.tsv)

## 📊 Model PerformanceModel R-Squared (Accuracy) RMSE 
- Linear Regression 0.8925
- Ridge Regression 0.8926
- Lasso Regression 0.8932 Winner

## Data fields
Here's a brief version of what you'll find in the data description file.

- SalePrice - the property's sale price in dollars. This is the target variable that you're trying to predict.
- MSSubClass: The building class
- MSZoning: The general zoning classification
- LotFrontage: Linear feet of street connected to property
- LotArea: Lot size in square feet
- Street: Type of road access
- Alley: Type of alley access
- LotShape: General shape of property
- LandContour: Flatness of the property
- Utilities: Type of utilities available
- LotConfig: Lot configuration
- LandSlope: Slope of property
- Neighborhood: Physical locations within Ames city limits
- Condition1: Proximity to main road or railroad
- Condition2: Proximity to main road or railroad (if a second is present)
- BldgType: Type of dwelling
- HouseStyle: Style of dwelling
- OverallQual: Overall material and finish quality
- OverallCond: Overall condition rating
- YearBuilt: Original construction date
- YearRemodAdd: Remodel date
- RoofStyle: Type of roof
- RoofMatl: Roof material
- Exterior1st: Exterior covering on house
- Exterior2nd: Exterior covering on house (if more than one material)
- MasVnrType: Masonry veneer type
- MasVnrArea: Masonry veneer area in square feet
- ExterQual: Exterior material quality
- ExterCond: Present condition of the material on the exterior
- Foundation: Type of foundation
- BsmtQual: Height of the basement
- BsmtCond: General condition of the basement
- BsmtExposure: Walkout or garden level basement walls
- BsmtFinType1: Quality of basement finished area
- BsmtFinSF1: Type 1 finished square feet
- BsmtFinType2: Quality of second finished area (if present)
- BsmtFinSF2: Type 2 finished square feet
- BsmtUnfSF: Unfinished square feet of basement area
- TotalBsmtSF: Total square feet of basement area
- Heating: Type of heating
- HeatingQC: Heating quality and condition
- CentralAir: Central air conditioning
- Electrical: Electrical system
- 1stFlrSF: First Floor square feet
- 2ndFlrSF: Second floor square feet
- LowQualFinSF: Low quality finished square feet (all floors)
- GrLivArea: Above grade (ground) living area square feet
- BsmtFullBath: Basement full bathrooms
- BsmtHalfBath: Basement half bathrooms
- FullBath: Full bathrooms above grade
- HalfBath: Half baths above grade
- Bedroom: Number of bedrooms above basement level
- Kitchen: Number of kitchens
- KitchenQual: Kitchen quality
- TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
- Functional: Home functionality rating
- Fireplaces: Number of fireplaces
- FireplaceQu: Fireplace quality
- GarageType: Garage location
- GarageYrBlt: Year garage was built
- GarageFinish: Interior finish of the garage
- GarageCars: Size of garage in car capacity
- GarageArea: Size of garage in square feet
- GarageQual: Garage quality
- GarageCond: Garage condition
- PavedDrive: Paved driveway
- WoodDeckSF: Wood deck area in square feet
- OpenPorchSF: Open porch area in square feet
- EnclosedPorch: Enclosed porch area in square feet
- 3SsnPorch: Three season porch area in square feet
- ScreenPorch: Screen porch area in square feet
- PoolArea: Pool area in square feet
- PoolQC: Pool quality
- Fence: Fence quality
- MiscFeature: Miscellaneous feature not covered in other categories
- MiscVal: $Value of miscellaneous feature
- MoSold: Month Sold
- YrSold: Year Sold
- SaleType: Type of sale
- SaleCondition: Condition of sale
