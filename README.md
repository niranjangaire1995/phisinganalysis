# 🚨 Phishing SMS Analysis – Fake Ohio BMV Alert


This micro-project documents my analysis of a phishing SMS received on **June 11, 2025**, impersonating the **Ohio Bureau of Motor Vehicles (BMV)**. The message attempts to trick the recipient into clicking a malicious link by leveraging the **principle of authority**, demanding payment for traffic violations.


### 📱 Original Phishing SMS Content

<img src="https://github.com/user-attachments/assets/fb393723-af41-4a02-bd63-98e8ef61ccd4" width="600"/>

*Figure: Screenshot of the actual phishing SMS impersonating the Ohio BMV.*



---

### ⚠️ Red Flags

- **Urgent Language**: “Final Notice”, “Enforcement Begins”
- **Suspicious Domain**: `hxxps://ohbmv[.]gov-tollbillrcu[.]bid/pay` *(defanged for safety)*
- **Unusual Sender Number**: `+63 947 208 9476` (Philippines)
- **Poor Grammar & Suspicious Formatting**

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
<img src="https://github.com/user-attachments/assets/91801b7c-7b23-4b6f-8b0d-0d0113b46e3b" width="600"/>

---

**📱 Mobile View Emulation via DevTools:**  
<img src="https://github.com/user-attachments/assets/2a73863b-5a43-4e2d-b52e-75929dfe1444" width="400"/>

---

**📲 Smart Phone Sandbox Behavior**  
Upon opening the smart phone version of the website in a sandbox environment:  
- None of the other pages on the site work.  
- **Only the "Pay" button works**, which redirects to a **contact information page** and then to a **credit card information page**, attempting to scam the victim.  

<img src="https://github.com/user-attachments/assets/1ee0cbfb-1750-4e7e-b464-ebf8215c4137" width="600"/>
<img src="https://github.com/user-attachments/assets/b3bdb636-3031-4b77-ae4f-65c8336c9729" width="600"/>

---

**🌐 Chinese Characters in Source Code:**  
CSS comments contained simplified Chinese characters, which may indicate attacker origin or reused web templates.  
<img src="https://github.com/user-attachments/assets/68fd55eb-e962-47c1-a523-c0641133cc3b" width="600"/>

---

**🔴 Google Now Flags This Website:**  
Originally accessible during my analysis, the site is now flagged as deceptive by Google Safe Browsing.  
<img src="https://github.com/user-attachments/assets/4bc1aa1b-d517-4bdc-9008-14e0cdac5d97" width="600"/>

---


## 🛡️ Defense Recommendations

- Block malicious domains via DNS/web filter
- Educate users to spot suspicious SMS patterns
- Report phishing SMS to:
  - [FTC](https://reportfraud.ftc.gov/)
  - Mobile carriers (e.g., forward to 7726)

---

### ✅ Conclusion

This phishing SMS case demonstrates how attackers use urgency and impersonation of authority to deceive victims—specifically targeting mobile users. The fraudulent message, posing as the Ohio BMV, directed the victim to a spoofed website designed primarily for smartphones. Upon analysis in a sandbox environment, it became evident that the website’s layout and functionality were **optimized for mobile devices**, with non-functional pages except for the “Pay” button—clearly engineered to streamline the path to credit card theft.

Further investigation revealed red flags such as a **Philippine sender number**, a suspicious `.bid` domain, and **Chinese characters** embedded in the page’s source code—suggesting potential foreign threat actor involvement.

This project highlights the need for heightened user awareness and robust detection tools, especially as phishing campaigns increasingly target mobile platforms with deceptive simplicity.


