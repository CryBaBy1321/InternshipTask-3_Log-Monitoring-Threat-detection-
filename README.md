# InternshipTask-3_Log-Monitoring-Threat-detection-
in this repo i show the use of the splunk and how did i monitor all the windos logs step by step 

Here is the login page of the splunk when u open this interface shown 
<img width="1919" height="1079" alt="Screenshot 2026-06-10 161300" src="https://github.com/user-attachments/assets/7f867b33-0d88-4d23-998b-8dc58a8ccf5e" />

then in the next step 
you have to select the middle option monitor 
<img width="1458" height="594" alt="Screenshot 2026-06-10 163111" src="https://github.com/user-attachments/assets/b7b0ca71-abe9-496c-8db1-c60c3e766640" />

then we select "Local event logs "
option from the below 
<img width="1814" height="931" alt="Screenshot 2026-06-10 163404" src="https://github.com/user-attachments/assets/cf216afd-fc33-4e89-9984-cc6e9281a339" />

then we select application , system , securtiy from the given oiptions 
<img width="899" height="625" alt="Screenshot 2026-06-10 163643" src="https://github.com/user-attachments/assets/423b4e2f-6d88-45c8-b37e-941f0348f7de" />

then we just make sleep mode using Win+L and try to add worng password and the after 2 or 3 try we login by using right password here below are the logs of the succssfully login and the code i search is    index=main source="WinEventLog:Security" EventCode=4624
<img width="1919" height="1079" alt="Screenshot 2026-06-10 165013" src="https://github.com/user-attachments/assets/abf3c55d-ed92-41a9-afce-9caaf8b3f664" />

Then did the same to finf the failed login attempts use this one to check 
index=main source="WinEventLog:Security" EventCode=4625
| stats count by Account_Name
<img width="1913" height="1055" alt="Screenshot 2026-06-10 165030" src="https://github.com/user-attachments/assets/624fd8c4-2d60-48d8-8967-8551604d7a33" />

Here are the Dashboard view of all the logs i found on the system 
<img width="1920" height="1080" alt="Screenshot 2026-06-10 171331" src="https://github.com/user-attachments/assets/3b2cc67b-d96b-44eb-a3bc-96b68921b2c6" />
<img width="1920" height="1080" alt="Screenshot 2026-06-10 171011" src="https://github.com/user-attachments/assets/fd08599a-47e9-44df-abcd-6c639bd302f8" />
<img width="1920" height="1020" alt="Screenshot 2026-06-10 171611" src="https://github.com/user-attachments/assets/9f45fee3-908b-4773-9c95-a19c320f56b7" />


Now the alert creation when the logs appears this is how you can make one
<img width="1920" height="1020" alt="Screenshot 2026-06-11 145319" src="https://github.com/user-attachments/assets/15dd0f9c-90a4-4875-b6f1-16d7b662a577" />
and this is the dasboard of that alert 
<img width="1920" height="1020" alt="Screenshot 2026-06-11 145341" src="https://github.com/user-attachments/assets/af48cbf6-990d-412f-9954-ece008eb7225" />









