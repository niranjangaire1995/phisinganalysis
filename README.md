# 🚨 Phishing SMS Analysis – Fake Ohio BMV Alert

This micro-project documents my analysis of a phishing SMS received on **June 11, 2025**, impersonating the **Ohio Bureau of Motor Vehicles (BMV)**. The message attempts to trick the recipient into clicking a malicious link by leveraging the **principle of authority**, demanding payment for traffic violations.

---

## 🧾 Summary

- **Attack Type**: SMS Phishing (Smishing)  
- **Impersonated Entity**: Ohio BMV  
- **Objective**: Credential theft or financial fraud via a fake payment site  

---

## 🔍 Analysis

**🛰️ Urlscan.io report:**  
[https://urlscan.io/result/01976041-15dd-73d3-9cf4-dbc3baeb7d30/](https://urlscan.io/result/01976041-15dd-73d3-9cf4-dbc3baeb7d30/)  
<img src="https://github.com/user-attachments/assets/f35a9241-c091-4162-94d1-c14571b21e3c" width="600"/>

<img src="https://github.com/user-attachments/assets/1917d1ae-4494-4918-b36e-c6150b80a701" width="600"/>
<img src="https://github.com/user-attachments/assets/7a71d7cc-74bd-41d4-9356-e8d3dcb41451" width="600"/>

---

**🧪 VirusTotal:**  
URL: [View Report](https://www.virustotal.com/gui/url/69bddb273b28f656db8a5607bd233bdbd5bf037c1a1fd0757dc44dd81977c7c2?nocache=1)  
<img src="https://github.com/user-attachments/assets/d03dfd8c-a826-4188-bc25-33c04635b356" width="600"/>

---

**🧬 Hybrid Analysis:**  
URL: [View Report](https://www.hybrid-analysis.com/sample/8b16f4ced9af945a047ff321fcb940459ba24915a2b34bab1aba36e001041b3f)  
<img src="https://github.com/user-attachments/assets/57b8e380-6674-48ff-b715-1edc4390a346" width="600"/>

---

**🔎 Reverse DNS Lookup:**  
[MXToolbox Result](https://mxtoolbox.com/SuperTool.aspx?action=+https%3a%2f%2fohbmv.gov-tollbillrcu.bid%2fpay&run=toolpage)  
<img src="https://github.com/user-attachments/assets/a8bc1433-47bb-45bd-8497-fe8cd47f06c8" width="600"/>

---

**🖼️ URL1Png Result (404 Error):**  
<img src="https://github.com/user-attachments/assets/c20fc2ab-653b-44b5-87ab-ce30a93e279a" width="600"/>

---

**🔒 Sandbox Browser Behavior:**  
Even in a sandbox environment, the site remains inaccessible.  
<img src="https://github.com/user-attachments/assets/91801b7c-7b23-4b6f-8b
