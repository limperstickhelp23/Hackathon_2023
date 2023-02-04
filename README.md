# Hackathon_2023
Predicting whether an ESP pump will fail in the next 30 days 
Goal: Develop a data analytics and machine learning workflow in Python to:

prediction / classification "fail" or "not fail" within 30 days for 40 artificial lift Electronic Submersible Pumps
Background
In order to prevent the production loss caused by Electronic Submersible Pump (ESP) failures in artificial lift operations.
This will require:

data analysis and evaluation of multiple data sources and a variety of features
feature engineering including feature selection, feature transformations and feature imputation to address missing data
integration of domain expertise at every step
selection, training and tuning robust machine learning prediction models
The model will be applied to support preventative maintenance by identifying ESPs within 30 days of failure for inspection and repair.

#Available Data Files Inventory

#Well / ESP Data
wellData.csv - data on 166 unique ESPs installed on 146 wells. All ESPs not in the solution.csv are assumed to have failed.
The features include:

#AL_Bottom_Depth (ft) - the depth at which an ESP is positioned in the well
ESP_Pump_Stages - the number of impellers that impart a pressure rise to the fluid
DLS_Critical (degree/100ft) - critical dogleg severity; until a dog-leg reaches this threshold value, no drill stem fatigue damage occurs
ESP_Motor_Frequency_Rating (Hz) - rated frequency of the motor
ESP_Motor_Current_Rating (A) - rated current of the motor
ESP_Motor_Voltage_Rating (V) - rated voltage of the motor
DLS_at_Set_Depth (degree/100ft) - dogleg severity at the depth of the ESP
Failure_Type - ESP failure type; can be "electrical", "pump", or "tubing"
Failure_Type_Detail - detailed ESP failure type; can be "motor", "penetrator", "stage", etc
Status - ESP status; can be either "failed", "active", or missing. Missing status indicates that an ESP is a test case
Daily Data
dailyData.csv - dynamic data collected daily. For each well, there will be a row of data for each day that the ESP is installed.
The features include:

OIL (bbl) - oil production
GAS (SCF) - gas production
WATER (bbl) - water production
DOWN_TIME_HOURS - the amount of time the well was shut for per day
Oil_Intake (bbl) - the amount of oil that enters the system
Water_Intake (bbl) - the amount of water that enters the system
Gas_Intake (SCF) - the amount of gas that enters the system
Liquid_Intake (bbl) - the amount of liquid that enters the system
Gas_Saturation_at_Intake - ratio of the amount of gas entering the system to the total volume
Gas_Saturation_at_Discharge - ratio of the amount of gas leaving the system to the total volume
Gas_Separator_Efficiency - ratio of the reduced volume of free gas to the volume before entering the separator
Pump_Delta_Pressure (psi) - the difference between discharge and intake pressure
Power_Ratio - ratio of pump power to drive power
Power_Difference (psi) - the difference between drive and pump power
Problem Set
solution.csv - a list of the ESPs to be predicted if they will fail in 30 days. Note, these ESPs in the daily data have not failed yet.
The features include:

Well_ID - anonymized, unique well indicator
AL_Key - artificial lift key, unique index ESP, e.g., ESP_1 1st ESP in well, ESP_2 2nd ESP in well
Fail in 30 days - hackathon solution to be entered by the team, 1 = WILL fail in 30 days, 0 = WILL NOT fail in 30 days
Comments:

all the well names are anonymized (replaced with simple indices).
NaN in the file indicate missing data.

Solution Table - a .csv file with your predictions for the test cases using the template given in solution.csv in this directory.
