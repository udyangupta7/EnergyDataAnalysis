# EnergyDataAnalysis:
As the countries try to diversify their energy portfolios in the present world and effect a greater reliance on cleaner power, 
they are left with one major problem: the power generated by a solar panel or a wind turbine is never uniform and depends on a range of external factors 
intensity of solar radiation, cloud cover, wind speed that can’t be controlled. To caculate the energy output, we followed the following steps to clean the dataset from the raw.zip folder:

1. The folder raw.zip are the raw files which were measured in a station. As the name indicates, there are 2 inverters, 1 energy meter (named MFM) and 1 meteorological substation (named WMS)

2. The raw data is a stream of data which gets recorded by the sensors on the field and is sent over the cloud.
 
3. The raw data is cleansed into a Gen-1 data format, here the following operations are performed:

a. For Inverters: The column i32 indicates the timestamp of the row. Make this as the first column in the Gen1 file and rename the column header to ‘Timestamp’.

b. For Energy meters (MFM): Same rules as above, only difference is timestamp column is 'm63'.

c. For Energy meters (MFM): Same rules as above, only difference is timestamp column is 'w23'

d. The station ID for the given raw data is IN-023C    

e. Year needs to be determined based on the timestamp of the file

f. Year-Month needs to be determined based on the timestamp of the file Substation-ID depends on the substation read (example Inverter-1, MFM, WMS etc)
