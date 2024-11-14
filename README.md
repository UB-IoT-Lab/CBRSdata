# CBRS KPI and Weather Datasets
The dataset has been introduced in the following papers:

1. [Propagation Analysis in the CBRS Spectrum: Path Loss Characterization and Environmental Impacts](https://doi.org/10.36227/techrxiv.173144788.88858804/v1)
2. [A Machine Learning Framework for Weather-Based Signal Strength Prediction in Private LTE/5G Networks](https://www.techrxiv.org/users/692934/articles/1239831-a-machine-learning-framework-for-weather-based-signal-strength-prediction-in-private-lte-5g-networks)
3. [Experimental Analysis of the Impact of Weather on Signal Strength in the CBRS Frequency Spectrum](https://doi.org/10.36227/techrxiv.171710034.48434625/v1)


# About Dataset
## Context
The release of the 150 MHz-wide Citizens Broadband Radio Service (CBRS) spectrum (3550-3700 MHz within the 3.5 GHz range) has created opportunities for unlicensed users and enterprise organizations to establish their own private mobile networks. This spectrum is utilized in sectors such as healthcare, education, smart cities, warehousing, and industrial operations, where high security, reliable performance, and robust network control are essential and cannot always be achieved through commercial mobile carriers. Received Signal Strength (RSS), which measures both radiation and signal attenuation, is a vital metric for assessing wireless communication performance. Significant drops in signal strength can lead to link failures, and fluctuations can affect the quality of service. Therefore, developing a highly accurate and efficient signal strength prediction model is crucial for maintaining network reliability in 5G and beyond 5G (B5G) networks.
## Content
### KPI Dataset
The dataset contains Key Performance Indicator (KPI) data, including Reference Signal Received Power (RSRP), Signal-to-Interference-plus-Noise Ratio (SINR), Reference Signal Received Quality (RSRQ), Received Signal Strength Indicator (RSSI) from a CBRS-based private LTE network deployed in the Fruitbelt neighborhood of Buffalo, NY. Data was collected at 32 static locations using Customer Premises Equipment (CPE) transceivers mounted on exterior walls of homes to communicate with the Base Station (BS). The BS has four directive antennas, and the CPEs that collect data have at most four antennas. The data collection spanned over two years, from June 20, 2022, to August 20, 2024, with an hourly sampling rate. Key features of the KPI dataset include:
-productclass: the series of the CPE antenna, such as Telrad CPE series
-serial: the serial number assigned to the CPE antenna, unique for each device
-coll_time_round: data collection time
result_id: a unique identifier for the result entry
model: model number of the CPE, indicating the specific type or variant of the equipment
imsi: International Mobile Subscriber Identity (IMSI) number
ue_wan_ip: IP address assigned to the CPE device on the WAN (Wide Area Network).
ue_up_time: uptime of the CPE device, indicating how long it has been operational since the last reset/powered on
serving_enb_id: identifier for the eNodeB (Base Station) to which the CPE is connected
tx_power: transmission power of the CPE, measured in dBm
rsrp0, rsrp1, rsrp2, rsrp3: Reference Signal Received Power (RSRP) for four antennas/receivers in the CPE device, measured in dBm
mean_AvgRsrp: average RSRP value calculated from the individual RSRP measurements
sinr0, sinr1, sinr2, sinr3: Signal-to-Interference-plus-Noise Ratio (SINR) for four antennas/receivers in the CPE device, measured in dB
mean_AvgSinr: average SINR value calculated from the individual SINR measurements
rsrq, rsrq1, rsrq2, rsrq3: Reference Signal Received Quality (RSRQ) for for four antennas/receivers in the CPE device, measured in dB
mean_AvgRsrq: average RSRQ value calculated from the individual RSRQ measurements
rssi, rssi0, rssi1, rssi2, rssi3: Received Signal Strength Indicator (RSSI), for four antennas/receivers in the CPE device, measured in dBm
mean_AvgRssi: average RSSI value calculated from the individual RSSI measurements
distance: distance between the CPE and the serving base station. Note: Ignore this parameter; rather, use **sensor_distance**.
sensor_distance: distance between the CPE and the serving base station, measured in Kilometer (Km)


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
