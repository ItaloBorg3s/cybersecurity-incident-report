Aqui está o **README.md** com as melhorias e a formatação que você solicitou, incluindo as alterações para tornar o conteúdo mais técnico e organizado, conforme discutido:

---

# **Cybersecurity Incident Report** 🛡️

## **Overview**

This repository contains my ongoing cybersecurity project, which focuses on analyzing a security incident. The project involves using **Wireshark**, **tcpdump**, and **Shell Scripting** to investigate a network security issue, specifically a **SYN Flood attack**. The goal of this project is to demonstrate practical knowledge and develop skills in **incident response**, **network traffic analysis**, and **security best practices**.

---

## **🚨 Incident Description**

### **Section 1: Identify the type of attack that may have caused this network interruption**

One potential explanation for the website's connection timeout error message is a **DoS (Denial of Service) attack**, specifically a **SYN Flood**. This type of attack aims to overwhelm the target server by sending numerous **SYN packets** in quick succession. The **logs show** that the web server became unresponsive after receiving a high volume of these packets, causing the server to be unable to process new legitimate connection requests.

This event could be categorized as a **Layer 3** or **Layer 4 attack** in the OSI model, specifically a **SYN Flood DoS attack**.

---

### **Section 2: Explain how the attack is causing the website to malfunction**

When website visitors attempt to establish a connection with the web server, a **three-way handshake** occurs using the **TCP protocol**. This handshake is made up of three steps:

1. **SYN (Synchronize)**: The client sends a request to establish a connection.
2. **SYN-ACK (Synchronize-Acknowledge)**: The server responds with an acknowledgment.
3. **ACK (Acknowledge)**: The client sends an acknowledgment back to the server to complete the handshake.

In a **SYN Flood attack**, a malicious actor sends a **large number of SYN packets** all at once. The server reserves resources for each incoming SYN request, but since the attacker never completes the handshake (doesn’t send the ACK), the connections remain **half-open**. As a result, the server's resources become exhausted, preventing it from processing legitimate connection requests and causing a **website malfunction**.

---

### **Section 3: Explain what the logs indicate and how that affects the server**

The logs indicate a significant increase in **half-open connections**, where the server is holding resources for connections that are never completed. This causes the server to run out of available connections, leading to a **server timeout**. 

As a result, legitimate users attempting to connect to the website are unable to establish a connection and instead receive a **connection timeout error message**. This is a direct consequence of the **SYN Flood attack**, where the attacker effectively exhausts the server’s connection capacity by flooding it with incomplete handshakes.

---

## **🔧 Tools & Technologies**

- **Wireshark** – Packet analysis tool used to inspect network traffic.
- **tcpdump** – Command-line tool for capturing network traffic, used in this project for traffic inspection.
- **Shell Scripting** – Automating tasks and analysis through shell scripts in Linux.
- **ISO 27000 standards** – Framework for establishing, implementing, operating, monitoring, and improving information security management systems (ISMS).
- **Linux** – Operating system used for the analysis and implementation of security measures.

---

## **📂 Project Files**

The project files are available in the **docs/** folder, which includes:

- The **PDF report** detailing the findings and analysis of the incident.
- The **Wireshark TCP/HTTP logs** in PDF format.

Feel free to explore and review the files for a deeper understanding of the incident analysis.
