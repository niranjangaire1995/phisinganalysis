# 🚨 Phishing SMS Analysis – Fake Ohio BMV Alert
This Micro-project has my analysis of a phising SMS I Received. The sender is impersonating the Ohio State Department of Motor Vehicles(BMV). The text message is trying to trick Recipients into clicking the malicious Link which follows one of the social engineering principles i.e. The Principles of Authority by askin people to pay for their unpaid traffic violations.


## 🧾 Summary

- **Attack Type**: SMS Phishing (Smishing)
- **Impersonated Entity**: Ohio BMV
- **Goal**: Credential theft or financial fraud via a fake payment site

## Analysis:

Urlscan.io report:
https://urlscan.io/result/01976041-15dd-73d3-9cf4-dbc3baeb7d30/
![image](https://github.com/user-attachments/assets/f35a9241-c091-4162-94d1-c14571b21e3c)
![image](https://github.com/user-attachments/assets/1917d1ae-4494-4918-b36e-c6150b80a701)
![image](https://github.com/user-attachments/assets/7a71d7cc-74bd-41d4-9356-e8d3dcb41451)



Virus Total:
url: https://www.virustotal.com/gui/url/69bddb273b28f656db8a5607bd233bdbd5bf037c1a1fd0757dc44dd81977c7c2?nocache=1
![image](https://github.com/user-attachments/assets/d03dfd8c-a826-4188-bc25-33c04635b356)


Hybrid Analysis:
Url: https://www.hybrid-analysis.com/sample/8b16f4ced9af945a047ff321fcb940459ba24915a2b34bab1aba36e001041b3f
![image](https://github.com/user-attachments/assets/57b8e380-6674-48ff-b715-1edc4390a346)


Reverse DNS tool:
![image](https://github.com/user-attachments/assets/a8bc1433-47bb-45bd-8497-fe8cd47f06c8)
https://mxtoolbox.com/SuperTool.aspx?action=+https%3a%2f%2fohbmv.gov-tollbillrcu.bid%2fpay&run=toolpage

URL1Png: This showed 404 error.
![image](https://github.com/user-attachments/assets/c20fc2ab-653b-44b5-87ab-ce30a93e279a)

I then opened the website in a sandbox environment: The issue persists. The website cannot be accessed.
![image](https://github.com/user-attachments/assets/91801b7c-7b23-4b6f-8b0d-0d0113b46e3b)

Using the developer tools to change the website view to a smart phone view:
![image](https://github.com/user-attachments/assets/2a73863b-5a43-4e2d-b52e-75929dfe1444)


Presence of the chinese alphabets in the comments section :
![image](https://github.com/user-attachments/assets/68fd55eb-e962-47c1-a523-c0641133cc3b)

Looks like google added this later, it was showing earlier when I was doing the analysis:
![image](https://github.com/user-attachments/assets/4bc1aa1b-d517-4bdc-9008-14e0cdac5d97)



-  Urgent language ("Final Notice", "Enforcement Begins")
- Unfamiliar domain: `hxxps://ohbmv[.]gov-tollbillrcu[.]bid/pay`           [Domain has been defanged to protect the viewers from accidentally clicking the link]
- Unusual sender phone number: `+63 947 208 9476` (Philippine country code)
- Threats of legal action and credit score damage
- Grammatical issues and suspicious formatting



## 🛡️ Defense Recommendations

- Block malicious domains via DNS/web filter
- Educate users to spot suspicious SMS patterns
- Report phishing SMS to FTC and your mobile provider

## 📄 License

This repository is open-sourced under the MIT License.

---

**Author:**  
Niranjan Gaire  
Cybersecurity Enthusiast (BTL1 Path)
