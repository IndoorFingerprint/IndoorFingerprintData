In this project, we have released a large dataset that contains fingerprints from 1469 large shopping malls and a office building.

- **Shopping Mall Dataset**：We provide **1469 shopping malls data**, including **POI information in the mall**, **WiFi fingerprint data in the mall** and **User requests information**.
<!-- ![1](https://github.com/IndoorFingerprint/IndoorFingerprintData/blob/main/pics/shopVisiting.png) -->
<div align=center>
<img src="https://github.com/IndoorFingerprint/IndoorFingerprintData/blob/main/pics/shopVisiting.png" width="50%" height="50%">
</div>

- **Office Building Dataset**：We provide indoor RSSI data of an office building with an area of 31695  square meters, including **WiFi fingerprint data in the building** and **User requests information in the building**. 
<div align=center>
<img src="https://github.com/IndoorFingerprint/IndoorFingerprintData/blob/main/pics/officeBuliding.png" width="50%" height="50%">
</div>


---


#  Part1. Shop Visting Dataset

##  1.1 POI_CategoryInfo
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ----- | ------- | --------- | --------- | ---- |
| 1 | Category_ID | string | shop type ID ||
| 2 | Category_Name | string | shop type name ||

##  1.2 Wifi-POI NameMatching Sample
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ------ | ------- | --------- | --------- | ---- |
|1 | Wifi | string |  shop ID | anonymized. |
|2 | Wifi_Name | string | The name of Wifi | |
|3 | POI_ID | string | POI ID | anonymized.  |
|4 | POI_Name | string | The name of POI | |
|5 | POI_Category | int | POI Category ID | anonymized.  Using 1.1 POI_CategoryInfo to Matching. |
|6 | Wifi_latitude | double | wifi location - longitude | anonymized.|
|7 | Wifi_longitude | double | wifi location - longitude | anonymized.|
|8 | POI_latitude | double | poi location - latitude | anonymized.|
|9 | POI_longitude | double | poi location - longitude | anonymized.|


## 1.3 Wifi Fingerprint Info
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ----- | ------- | --------- | --------- | ---- |
| 1 | Wifi | string | MAC address (WiFi unique identification code)  | anonymized.|
| 2 | Floor | string |  Office Building Floor | |
| 3 | Latitude | double | The positon of user's request which contains the Wifi | anonymized. |
| 4 | Longitude | double | The positon of user's request which contains the Wifi | anonymized. |
| 5 | Rssi | int | RSSI (strength) of the Wifi | Example: -67 |
| 6 | Grid_latlng | string | The fingerprint grid's position computed from Wifi's position | anonymized. |


## 1.4 User Request Info
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ----- | ------- | --------- | --------- | ---- |
| 1 | Query | string | The WiFi environment when behavior occurs, including MAC address (WiFi unique identification code), RSSI (strength) | anonymized. <br> Example: M001,-67; M002,-86; M003,-90; <br> Explanation: Wi-Fi list separated by semicolons. Each data contains two items: M001 is the MAC address after anonymous processing and -67 is the RSSI strength. The larger the value, the stronger the signal|

---

# Part2. Office Building Dataset

## 2.1 Wifi Fingerprint Info
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ----- | ------- | --------- | --------- | ---- |
| 1 | Wifi | string | MAC address (WiFi unique identification code)  | anonymized.|
| 2 | Floor | string |  Office Building Floor | |
| 3 | Latitude | double | The positon of user's request which contains the Wifi | anonymized. |
| 4 | Longitude | double | The positon of user's request which contains the Wifi | anonymized. |
| 5 | Rssi | int | RSSI (strength) of the Wifi | Example: -67 |
| 6 | Grid_latlng | string | The fingerprint grid's position computed from Wifi's position | anonymized. |


## 2.2 User Request Info
| Field Index  | Field Name  |  Field type | Field description  | Remarks |
| ----- | ------- | --------- | --------- | ---- |
| 1 | Query | string | The WiFi environment when behavior occurs, including MAC address (WiFi unique identification code), RSSI (strength) | anonymized. <br> Example: M001,-67; M002,-86; M003,-90; <br> Explanation: Wi-Fi list separated by semicolons. Each data contains two items: M001 is the MAC address after anonymous processing and -67 is the RSSI strength. The larger the value, the stronger the signal|
