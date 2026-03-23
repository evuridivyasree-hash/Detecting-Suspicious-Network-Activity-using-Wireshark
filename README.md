# SOC Analyst Project | Detecting Suspicious Network Activity using Wireshark

## Project Overview
This project focuses on analyzing network traffic using Wireshark to identify normal and potentially suspicious activities.

## Objective
To capture and analyze network packets in order to detect unusual patterns such as multiple connection attempts and understand protocol behavior.

## Tools Used
- Wireshark

## Methodology

### 1. Traffic Capture
- Captured live network traffic using Wireshark

### 2. TCP SYN Analysis
- Applied filter:
  tcp.flags.syn == 1 && tcp.flags.ack == 0
- Observed connection initiation attempts

### 3. DNS Analysis
- Applied filter:
  dns
- Analyzed domain name resolution queries

### 4. HTTP/HTTPS Analysis
- Applied filter:
  tcp.port == 80 || tcp.port == 443
- Compared unencrypted and encrypted traffic

### 5. TCP Stream Analysis
- Used "Follow TCP Stream" to inspect communication
- Observed encrypted data in HTTPS traffic

### 6. Full Capture Analysis
- Reviewed complete traffic without filters
- Identified multiple protocols in use

### 7. Protocol Hierarchy
- Used statistics to analyze protocol distribution

## Findings
- Multiple TCP SYN packets observed targeting ports 80 and 443
- Repeated connection attempts from a single source
- DNS queries resolving domain names
- HTTPS traffic was encrypted using TLS

## Conclusion
The project demonstrates how Wireshark can be used by SOC analysts to monitor network traffic, identify suspicious patterns, and understand secure communication protocols.

## 📷 Screenshots
![TCP SYN Analysis png](https://github.com/user-attachments/assets/01c28fed-a023-47d9-ba8c-9b522f6d85cd)
![DNS Analysis png](https://github.com/user-attachments/assets/c54cb9be-6d4f-4581-96e7-923f52efbf24)
![DNS Analysis2 png](https://github.com/user-attachments/assets/b7a0d059-ce2d-403a-97ad-81c05f065bc9)
![HTTP Analysis png](https://github.com/user-attachments/assets/892ac41f-919a-44e5-85d1-ba69d69460b4)
![HTTPS Analysis png](https://github.com/user-attachments/assets/b3a275c7-e887-4387-a0de-b462a16e717b)
![Full Capture Analysis png](https://github.com/user-attachments/assets/39337786-a2ef-4b16-88fc-154721ce10b6)
![Protocol Hierarchy png](https://github.com/user-attachments/assets/4c3a2040-f350-4047-97dd-a370ee1ddb36)
![Protocol Hierarchy1 png](https://github.com/user-attachments/assets/94707b59-72a3-4342-8a41-1976fb01fb1c)
# Detecting-Suspicious-Network-Activity-using-Wireshark
