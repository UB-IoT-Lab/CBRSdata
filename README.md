# CBRS KPI and Weather Datasets
The dataset has been introduced in the following papers:

1. [Propagation Analysis in the CBRS Spectrum: Path Loss Characterization and Environmental Impacts](https://doi.org/10.36227/techrxiv.173144788.88858804/v1)
2. [A Machine Learning Framework for Weather-Based Signal Strength Prediction in Private LTE/5G Networks](https://www.techrxiv.org/users/692934/articles/1239831-a-machine-learning-framework-for-weather-based-signal-strength-prediction-in-private-lte-5g-networks)
3. [Experimental Analysis of the Impact of Weather on Signal Strength in the CBRS Frequency Spectrum](https://doi.org/10.36227/techrxiv.171710034.48434625/v1)


# About Dataset
## Context
The release of the 150 MHz-wide Citizens Broadband Radio Service (CBRS) spectrum (3550-3700 MHz within the 3.5 GHz range) has created opportunities for unlicensed users and enterprise organizations to establish their own private mobile networks. This spectrum is utilized in sectors such as healthcare, education, smart cities, warehousing, and industrial operations, where high security, reliable performance, and robust network control are essential and cannot always be achieved through commercial mobile carriers.
## Content
### Network KPI Dataset
The "KPI" folder contains the network Key Performance Indicator (KPI) dataset from two CBRS deployments in NY, USA: kpi_data_buffalo.zip KPI data from a CBRS network deployed in downtown Buffalo, NY, and kpi_data_elmira.csv KPI data from another CBRS network deployed in Elmira, NY. 

#### Buffalo KPI Dataset
The kpi_data_buffalo.zip dataset contains KPI data, including Reference Signal Received Power (RSRP), Signal-to-Interference-plus-Noise Ratio (SINR), Reference Signal Received Quality (RSRQ), Received Signal Strength Indicator (RSSI) from a CBRS-based private LTE network deployed in the Fruitbelt neighborhood of Buffalo, NY. Data was collected at 32 static locations using Customer Premises Equipment (CPE) transceivers mounted on exterior walls of homes to communicate with the Base Station (BS). The BS has four directive antennas, and the CPEs that collect data have at most four antennas. The data collection spanned over two years, from June 20, 2022, to August 20, 2024, with an hourly sampling rate. Key features of the KPI dataset include:

- productclass: the series of CPE antenna, such as the Telrad CPE series
- serial: the serial number assigned to the CPE antenna, unique for each device
- coll_time_round: data collection time
- result_id: a unique identifier for the result entry
- model: model number of the CPE, indicating the specific type or variant of the equipment
- imsi: International Mobile Subscriber Identity (IMSI) number
- ue_wan_ip: IP address assigned to the CPE device on the WAN (Wide Area Network).
- ue_up_time: uptime of the CPE device, indicating how long it has been operational since the last reset/powered-on
- serving_enb_id: identifier for the eNodeB (Base Station) to which the CPE is connected
- tx_power: transmission power of the CPE, measured in dBm
- rsrp0, rsrp1, rsrp2, rsrp3: Reference Signal Received Power (RSRP) for four antennas/receivers in the CPE device, measured in dBm
- mean_AvgRsrp: average RSRP value calculated from the individual RSRP measurements
- sinr0, sinr1, sinr2, sinr3: Signal-to-Interference-plus-Noise Ratio (SINR) for four antennas/receivers in the CPE device, measured in dB
- mean_AvgSinr: average SINR value calculated from the individual SINR measurements
- rsrq, rsrq1, rsrq2, rsrq3: Reference Signal Received Quality (RSRQ) for for four antennas/receivers in the CPE device, measured in dB
- mean_AvgRsrq: average RSRQ value calculated from the individual RSRQ measurements
- rssi, rssi0, rssi1, rssi2, rssi3: Received Signal Strength Indicator (RSSI), for four antennas/receivers in the CPE device, measured in dBm
- mean_AvgRssi: average RSSI value calculated from the individual RSSI measurements
- distance: distance between the CPE and the serving base station. Note: Ignore this parameter; rather, use **sensor_distance**.
- sensor_distance: distance between the CPE and the serving base station, measured in Kilometer (km)

#### Elmira KPI Dataset
The kpi_data_elmira.csv dataset contains Reference Signal Received Power (RSRP) data from a CBRS-based private LTE network deployed in the City of Elmira, NY. Data was collected at 12 static locations using CPE transceivers mounted on exterior walls of homes to communicate with the Base Station (BS). The data collection spanned over two years, from March 7, 2024, to November 11, 2024 (Continuing), with an hourly sampling rate. Key features of the KPI dataset include:

- coll_time_round: data collection time
- Date Time (RAW): Serial date number representing the exact moment of data collectio.
- RSRP_Wo_Round: The raw, unrounded Reference Signal Received Power(RSRP) measured in dBm. Example: -79.2368421052632 dBm.
- mean_AvgRsrp: The RSRP value after rounding to the nearest decimal places. Example: -79.2368 dBm.
- Downtime: The percentage of time the antenna was non-operational.
- Downtime (RAW): The exact downtime count.
- Coverage: The percentage of time the antenna experienced signal coverage.
- Coverage (RAW): The numerical value representing the antenna experienced signal coverage.
- serial: The unique serial number of the CPE antenna.
- sensor_distance: The distance in km from the CPE antenna to a specified reference point. Example: 0.05685216 meters.

### Weather Dataset
The weather dataset contains historical weather records obtained from [Oikolab](https://oikolab.com/) for the same location and time period (hourly resolution), which includes:

- datetime (UTC): data collection time. Note, although the name says UTC, it has already been adjusted in EST time
- coordinates (lat,lon): location for where the data has been collected
- temperature (degC): temperature 2 meters above the ground, in degrees Celsius (°𝐶)
- relative_humidity (0-1): relative humidity, ranging from 0 to 1
- absolute_humidity (𝑔/𝑚3): absolute humidity, in grams per cubic (𝑔/𝑚3)
- wind_speed (𝑚/𝑠): Wind speed at 10 m above the surface, in 𝑚/𝑠
- total_precipitation (mm of water equivalent): accumulated liquid and frozen water, comprising rain and snow, that falls to the Earth's surface, in mm of water equivalent
- surface_pressure (Pa): pressure of the atmosphere at the surface of land, sea, and inland water in 𝑃𝑎
- snowfall (mm of water equivalent): accumulated snow that falls to the Earth's surface, measured in mm of water equivalent. It is the sum of large-scale snowfall and convective snowfall.
- snow_depth (mm of water equivalent): depth of the snow data ground, measured in mm of water equivalent
- rainfall (mm): rainfall, in mm

## Acknowledgements
This work was supported by the Center of Excellence in Materials
Informatics (CMI) at the University at Buffalo, and by Integrated Systems.

More details on current and past projects on related topics are available on [Lab Site](https://www.acsu.buffalo.edu/~filippom/).
## Citing the paper
If you find this data helpful, please cite:

1.

	Dash, B. K., Caezza, J. A., & Malandra, F. (2024). Propagation Analysis in the CBRS Spectrum: Path Loss Characterization and Environmental Impacts. Authorea Preprints.
2.

	Devasenapathy, K., Caezza, J. A., & Malandra, F. (2024). A Machine Learning Framework for Weather-Based Signal Strength Prediction in Private LTE/5G Networks. Authorea Preprints.
3. 

  	Dash, B. K., Caezza, J. A., & Malandra, F. (2024). Experimental Analysis of the Impact of Weather on Signal Strength in the CBRS Frequency Spectrum. Authorea Preprints.
4.

  	Dash, B. K., Caezza, J. A., & Malandra, F. (2023, November). Experimental Network Performance Analysis from a CBRS-based Private Mobile Network. In 2023 IEEE Future Networks World Forum (FNWF) (pp. 1-6). IEEE.
