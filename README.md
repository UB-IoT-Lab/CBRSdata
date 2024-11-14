# CBRS KPI and Weather Datasets
The dataset has been introduced in our IEEE TAP 24 paper: [A Machine Learning Framework for Weather-Based Signal Strength Prediction in Private LTE/5G Networks]()
# About Dataset
## Context
The release of the 150 MHz-wide Citizens Broadband Radio Service (CBRS) spectrum (3550-3700 MHz within the 3.5 GHz range) has created opportunities for unlicensed users and enterprise organizations to establish their own private mobile networks. This spectrum is utilized in sectors such as healthcare, education, smart cities, warehousing, and industrial operations, where high security, reliable performance, and robust network control are essential and cannot always be achieved through commercial mobile carriers. Received Signal Strength (RSS), which measures both radiation and signal attenuation, is a vital metric for assessing wireless communication performance. Significant drops in signal strength can lead to link failures, and fluctuations can affect the quality of service. Therefore, developing a highly accurate and efficient signal strength prediction model is crucial for maintaining network reliability in 5G and beyond 5G (B5G) networks.
## Content
The dataset contains Key Performance Indicator (KPI) data, including Reference Signal Received Power (RSRP), from a CBRS-based private LTE network deployed in the Fruitbelt neighborhood of Buffalo, NY. Data was collected at 32 static locations using Customer Premises Equipment (CPE) transceivers mounted on exterior walls of homes to communicate with the Base Station (BS). The data collection spanned two years, from June 20, 2022, to May 31, 2024, with an hourly sampling rate. Key features of the KPI dataset include:
- tx_power: transmission power of the CPE, measured in dBm
- serving_enb_id: identifier for the BS antenna connected to the CPE
- mean_Rsrp: hourly mean RSRP in dBm
- sensor_distance: distance between each CPE and the BS, measured in kilometers (Km)
Additionally, a dataset containing weather-related features was obtained from [Oikolab](https://oikolab.com/) for the same location and time period, which includes:
- temperature (degC): temperature 2 meters above the ground, in degrees Celsius (°𝐶)
- relative_humidity (0-1): relative humidity, ranging from 0 to 1
- absolute_humidity (𝑔/𝑚3): absolute humidity, in grams per cubic (𝑔/𝑚3)
- wind_speed (𝑚/𝑠): wind speed, in 𝑚/𝑠
- surface_pressure (Pa): surface pressure, in 𝑃𝑎
- snowfall (mm of water equivalent): snowfall, in millimeters of water (mm of WE)
- rainfall (mm): rainfall, in mm
- total_precipitation (mm of water equivalent): total precipitation, including rainfall and snowfall, in mm of WE
## Acknowledgements
This work was supported by the Center of Excellence in Materials
Informatics (CMI) at the University at Buffalo, and by Integrated Systems.

More details on current and past projects on related topics are available on [Lab Site]().
## Citing the paper
If you find this data helpful, please cite:

	Citation1
	Citation2
	Citation3