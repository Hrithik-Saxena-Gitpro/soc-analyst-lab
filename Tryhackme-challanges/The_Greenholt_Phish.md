# The Greenholt Phish

## Overview
- **Platform:** Tryhackme 
- **Subject:** Use the knowledge attained to analyze a malicious email.
- **Goal:** Your goal is to analyze the provided email sample and determine whether it is legitimate or part of a phishing attempt.
- **Status:** Done

## Objective 
- Analyze the provided email to identify and extract key artifacts
- Investigate the message source to determine its origin and authenticity
- Use analysis tools to assess the potential maliciousness of the email

## Problem Solved as per requirement of room 

Q1 What is the Transfer Reference Number listed in the email's Subject line?
Answer : 09674321

Q2 What is the display name of the sender?
Answer : Mr.James Jackson 

Q3 Continue investigating the email headers.
What is the sender's email address?
Answer : info@mutawamarine.com

Q4 What email address will receive a reply to this email?
Answer : info.mutawamarine@mail.com

Q5 Begin analyzing the message source.
What is the originating IP address of this email?

Answer : We can see this in via going mail view source it is in earliest header of the email
112.119.71.157 

<img width="1055" height="409" alt="image" src="https://github.com/user-attachments/assets/659a8eda-cea7-45ab-84da-664e40c830d4" />


Q6 Investigate the IP address from the previous question.
Who is the owner of the originating IP?
Answer : Hostpapa ( Used who is lookup to get the details of the ip address orgname done on this ip address 112.119.71.157  ) 

<img width="595" height="638" alt="image" src="https://github.com/user-attachments/assets/1819cc7f-3add-417d-a96d-ad5fd5a221a3" />
 
Q7 Run an SPF record check on the Return-Path domain identified in the email headers.
What is the full SPF record for this domain?
Answer : i used dig command with +short and TXT flags  

<img width="803" height="155" alt="image" src="https://github.com/user-attachments/assets/f906d816-757c-4c41-b439-eacf019487a3" />

Q8 Perform a DMARC lookup for the Return-Path domain found in the email headers.
What is the complete DMARC record for this domain?
Answer : v=DMARC1; p=quarantine; fo=1 ( DMARC is basicall y a authentication to check email header to prevent the email spoofing and phishing 

<img width="803" height="155" alt="image" src="https://github.com/user-attachments/assets/11f44d11-cb35-484f-9f90-7e8376e9a59b" />

Q9 What is the file name of the attachment found in the email?
Answer : SWT_#09674321___PDF__.CAB

Q10 Download the attachment to your virtual environment.
Using the sha256sum command, what is the SHA256 hash of the file?
Answer : we can use the sha256sum command to check hash256 of the file 
2e91c533615a9bb8929ac4bb76707b2444597ce063d84a4b33525e25074fff3f

<img width="834" height="70" alt="image" src="https://github.com/user-attachments/assets/e2b70199-86d0-48fd-8395-a5d62b4f94f3" />


Q11 investigate the file hash from the previous question using VirusTotal.
What is the attachment's file size in KB (e.g., 122.31 KB)?
Answer : 400.26 KB 

<img width="1219" height="203" alt="image" src="https://github.com/user-attachments/assets/367e476a-879b-4988-be54-59dc151a7e7c" />

Q12 Continue your research on the file.
What is the actual file type of the attachment?
Answer :  its RAR ( A RAR file is a proprietary data container and compressed archive format) 

<img width="499" height="203" alt="image" src="https://github.com/user-attachments/assets/81650ccc-7bd3-4095-a98a-892051366b3c" />























