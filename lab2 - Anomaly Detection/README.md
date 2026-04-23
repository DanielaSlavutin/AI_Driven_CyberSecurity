# Network Traffic Anomaly Detection

In this lab assignment, I applied a classic ML pipeline for network traffic anomaly detection. I utilized the **Isolation Forest** algorithm over a downsampled version of the **KDD Cup 1999** dataset, which represents general network traffic, to isolate malicious activities from benign "white noise".

### MITRE ATT&CK Mapping
After analyzing the dataset, the detected anomalous behaviors correspond to the following MITRE ATT&CK techniques:
* **Network Denial of Service (T1498):** Represented by volumetric impact attacks (e.g., Smurf, Neptune).
* **Active Scanning (T1595):** Represented by reconnaissance and probing activities (e.g., ipsweep, portsweep).
* **External Remote Services (T1133):** Represented by initial access attempts (e.g., warezclient).