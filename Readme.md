
<div align="center">

# 🔐 Secure IoT Sensor Network using TLS-based MQTT Communication

🚀 Network Security | IoT Security | Cryptography | TLS | MQTT  

![Node-RED](https://img.shields.io/badge/Node--RED-IoT-red)
![MQTT](https://img.shields.io/badge/MQTT-Secure-blue)
![TLS](https://img.shields.io/badge/TLS-Encryption-green)
![Wireshark](https://img.shields.io/badge/Wireshark-Network%20Analysis-purple)
![Security](https://img.shields.io/badge/Cybersecurity-Project-black)

</div>

---

## 🧠 Project Overview

This project demonstrates how insecure IoT communication can be transformed into a secure TLS-encrypted architecture using MQTT.

Many IoT devices transmit data without encryption, allowing attackers to intercept or modify messages.  
This implementation introduces:

✅ TLS encryption  
✅ Certificate-based authentication  
✅ Secure MQTT communication (Port 8883)  
✅ Real packet analysis using Wireshark  

---

## ⚠️ Problem Statement

Standard MQTT uses port **1883**, where data is transmitted in plaintext.

This leads to:

- Packet sniffing
- Credential exposure
- Man-in-the-Middle attacks

The goal of this project is to secure IoT data pipelines using modern cryptographic techniques.

---

## 🏗 Architecture

```

IoT Sensor (Node-RED)
│
▼
TLS Handshake (Certificates)
│
▼
Secure Mosquitto Broker (MQTTS :8883)
│
▼
Subscriber / Dashboard

```

---

## 🛠 Tech Stack

| Category | Tools |
|---|---|
| IoT Simulation | Node-RED |
| Broker | Eclipse Mosquitto |
| Cryptography | OpenSSL |
| Network Analysis | Wireshark |
| Protocol | MQTT + TLS |

---

## 🔑 TLS Certificate Generation

Certificates were generated using OpenSSL to establish mutual authentication.

<img width="862" height="300" alt="Screenshot 2025-10-31 223600" src="https://github.com/user-attachments/assets/d7a24fc5-22ce-4674-a030-18fd9400ebdd" />



Certificates Created:

- CA Certificate  
- Broker Certificate  
- Client Certificate  

---

## 🔌 Secure Node-RED MQTT Connection

Node-RED connects to the broker using TLS encryption.

<img width="2293" height="1157" alt="image" src="https://github.com/user-attachments/assets/e62a616b-3f96-4a1c-aa99-283552d7ea37" />


Key Highlights:

- mqtts://localhost:8883  
- Encrypted communication  
- Certificate validation enabled  

---

## 🧪 Insecure Phase — Plaintext MQTT (Before TLS)

Wireshark capture showing readable MQTT payload.

<img width="449" height="354" alt="Screenshot 2025-10-31 192044" src="https://github.com/user-attachments/assets/1eb1c458-862b-4b05-bd7c-4c48060ec855" />


Observation:

- JSON sensor data visible  
- No encryption  
- High vulnerability  

---

## 🔒 Secure Phase — Encrypted MQTT (After TLS)

Wireshark capture after enabling TLS.

<img width="960" height="564" alt="image" src="https://github.com/user-attachments/assets/a3c2588a-03dc-4ccb-a8aa-1e95d8ec418e" />


Observation:

- TLSv1.2 Application Data  
- Encrypted payload  
- MITM protection  

---

## 📊 Results

| Phase | Port | Encryption | Packet Visibility |
|---|---|---|---|
| Insecure MQTT | 1883 | ❌ No | Plaintext |
| Secure MQTTS | 8883 | ✅ TLS | Encrypted |

---

## 🚀 How To Run

### Start Mosquitto Broker

```

net start mosquitto

```

### Start Node-RED

```

node-red

```

Open editor:

```

[http://localhost:1880](http://localhost:1880)

```

Deploy flow and monitor secure traffic.

---

## 📂 Repository Structure

```

Secure-IoT-TLS-MQTT/
│
├── flow.json
├── mosquitto.conf
├── README.md
├── Secure_IoT_TLS_Project_Report.docx
└── screenshots/
├── openssl_setup.png
├── node_red_connected.png
├── insecure_packet.png
└── secure_tls_packet.png

```

---

## 🔐 Security Notice

Private keys are excluded from this repository:

```

*.key files are NOT uploaded

```

---

## 👨‍💻 Authors

**Harsha Vardhan KS**  

---

<div align="center">

⭐ If you found this project interesting, consider giving it a star!

</div>
```

---
