# Snapped Phishing Line 

It is another challenge on my journey of soc level 1 or you can say entry level for cybersecurity xyz....

## Objectives as per given challenges are like these

=> Analyze the the provided email samples to identify key artifacts 
=> Investigate phishing emails to understand the redirection 
=> Retrieve and examine the phishing kit used in the attack 
=> use the cti tools to investigate about the adversary 
=> analyze the  phishing kit to uncover the additional indicators 


# Tasks Questions and my Answer with approach given below 

### Q1 Begin reviewing the emails in the phish-emails folder on your desktop.Which individual received the email regarding a Quote for Services Rendered?<br>
Ans William McClean
<br>
<img width="842" height="336" alt="image" src="https://github.com/user-attachments/assets/302eb211-0100-4c52-a873-19fb2aca9561" />

### Q2 What email address was used by the adversary to send the phishing emails ? <br> 
Ans Accounts.Payable@groupmarketingonline.icu

### Q3 Investigate the attachment in the email addressed to Zoe Duncan. What is the root domain of the redirection URL found within the file? <br>
Ans kennaroads.buzz <br>
<img width="1282" height="523" alt="image" src="https://github.com/user-attachments/assets/f7032791-70ce-4232-8843-764f11c6989f" />

### Q4 Open the attachment in the web browser. which company is the login page impersonating ? <br> 
Ans microsoft <br> 
<img width="643" height="367" alt="image" src="https://github.com/user-attachments/assets/75b0b980-89eb-401d-a941-493b19e971cf" />

### Q5 Lets check if attacker left any file on the same website . navigate to the /data directory. What is the name of the archive file ? <br>
Ans Update365.zip <br> 

<img width="616" height="307" alt="image" src="https://github.com/user-attachments/assets/925f752c-833d-45f4-afb2-9245af8836c5" />


### Q6 Download the phishing kit archive to your virtual environment.Using the sha256sum command, what is the SHA256 hash of the file? <br>
Ans  ba3c15267393419eb08c7b2652b8b6b39b406ef300ae8a18fee4d16b19ac9686  <br>
<img width="888" height="496" alt="image" src="https://github.com/user-attachments/assets/f313ad77-075e-4e2c-88db-22511f538c24" />

### Q7 Investigate the file hash from the previous question using the virus total tool . Aside from phishing what other threat category is assigned to the zip archive? <br>
Ans Trojan <br>
<img width="1148" height="432" alt="image" src="https://github.com/user-attachments/assets/1e96b45b-e20d-44d2-a9a1-b6162a25a11c" />

### Q8 Review the virus total detail page fro phishing kit. How many files contain within the archive? <br>
Ans 49 <br>
<img width="538" height="260" alt="image" src="https://github.com/user-attachments/assets/ac067f5a-57c1-49ac-ac5e-8928592d6ac9" />

### Q9 Lets see if attacker has exposed any captured credentials. Navigate to the /data/update365 directory and investigate the log file. What is the email address of the  user who submitted  their credentials more the once? <br> 
Ans  michael.ascot@swiftspend.finance <br>
<img width="862" height="418" alt="image" src="https://github.com/user-attachments/assets/fbbb0acd-4363-45fd-92c0-cb82efaf854e" />

### Q10 Extract the phishing kit archive and locate the submit.php file. What email address is used by the adversary to collect compromised credentials ? <br> 
Ans  m3npat@yandex.com <br>

### Q11 Return to the phishing url and locate the flag.txt file. User cyberchef to decode the flag, What is the secret value ?
Ans THM{pL4y_w1Th_tH3_URL}


