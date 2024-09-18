# Digital-Forensics-Project-on-WannaCry-Ransomware

# Digital-forensics

![image](https://github.com/user-attachments/assets/293d9c05-aace-4d09-ac78-b2d31a0b08e8)

# Introduction and Background Story:

WannaCry is one of the most notorious ransomware attacks, hitting the world in May 2017. It spread fast, crippling over 200,000 computers in 150 countries, including the UK’s National Health Service. The attack exploited a known vulnerability in Windows (SMB protocol), which had a patch available months before, but many systems hadn’t been updated. The malware used EternalBlue, a leaked NSA exploit, to spread like wildfire through networks.

Even today, WannaCry is a key lesson for cybersecurity. It showed how vital it is to stay on top of patching systems, keeping networks segmented, and having a solid incident response plan in place. Cybersecurity analysts must constantly watch for vulnerabilities and know how to respond quickly to ransomware attacks, which have only gotten more sophisticated since then.

# Overview:

In the digital forensics lab, we use tools like Autopsy to dig into compromised systems, looking for encrypted files and traces of the malware. Volatility helps analyze memory dumps to track how the ransomware worked, especially how it used EternalBlue to move across networks. Understanding how WannaCry operated helps us stay ahead of modern threats and be better prepared to handle future attacks.


![image](https://github.com/user-attachments/assets/f87b38f6-2d02-468d-b767-f886d786cb1d)

## Description
Set up an isolated environment to safely execute the WannaCry ransomware, ensuring external systems were not affected.

Conducted detailed disk forensics using Autopsy to analyze file structures, locate suspicious files, and identify the ransomware's behavior on the infected system.

Performed memory forensics using Volatility to capture and analyze memory dumps, uncovering real-time ransomware activities and process behaviors.

Identified key Indicators of Compromise (IoCs) and documented the ransomware's impact on both the disk and memory, providing insights into its propagation and encryption tactics.

## Steps
1. Set up an isolated Windows 10 virtual machine without any internet connection.

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/2b365fb7-9af3-4f68-bf48-7a147943ca7a)

2. Disable Windows Defender real-time protection and SmartScreen protection.
3. Download and run the WannaCry ransomware.

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/0fdbf265-910c-4dad-b3ea-4403b51757f4)

4. Download and install FTK Imager on a removable device.
5. Use FTK Imager to acquire the disk and memory images.
6. Click File, then select Create Disk Image.
   
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/0ec53541-d60e-4f39-99e3-bc5831c56c94)


7. Select the logical drive.
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/08bbd237-a37a-4bbc-a289-fd90c0f8d3fe)

8. Select the specific drive.
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/fb35ae58-775f-4f77-90a6-44b29a134753)

9. Select the file type.

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/803a345a-76b1-43a3-8997-0f3be4fa3ba8)

10 . Enter the evidence item information.

  ![image](https://github.com/user-attachments/assets/e30546ad-3421-47ca-86d9-1c3e72fd3ee3)

11. Select the image destination folder and ensure there is enough space available on the drive (a removable drive is preferable for securely analyzing the image on a remote testing machine, isolated from the infected system).
12. Enter the image file name without the extension.
13. Use segmentation (optional).
14. Click finish.

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/017c0783-4aaf-46e6-9357-73ec53e06957)

15. The image was generated successfully in the designated drive/folder.
  
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/be3e08ac-8e5d-4810-adfd-a7d00d22f6d2)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/9323f36f-46fa-4639-bf1d-7b2622ae6094)

16. Click File, then select Capture Memory.

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/37f600cd-d8be-4e27-907c-487273fddbf3)

17.  Enter the destination folder to store the memory image (a removable drive is preferable for securely analyzing the image on a remote testing machine, isolated from the infected system).
18.  Click capture memory.
     
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/fec21965-899e-4e46-826c-b48aeb6ce70f)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/b8b4dde0-eb0f-4c70-85df-cf9c9f1059dd)
  
19. Download and install Autopsy on a test machine (isolated from the infected machine).

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/668084a1-84e6-4578-b7c3-81345814cd4d)

20. Create a new Case in Autopsy.

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/6f11cc33-be9d-4a23-9739-483876d62a51)

 21. Enter the case information.
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/63e1083c-851d-44c0-bb4d-6c2067acf12f)

   ![image](https://github.com/user-attachments/assets/af70206b-7c2c-493d-a2fa-9839abc4e800)

22. Select and add the data source.
    
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/bbc2eee2-3714-410a-a951-a7395a172598)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/94680ea4-8101-46ae-8296-b3e260fff446)

23. Select the path of the disk image file (Autopsy will automatically select all segments).
    
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/595d042a-1b20-48d4-a1fc-4fb0df413a66)
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/53dce4d4-800c-47f0-93da-3c5d41d036aa)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/2a465fb1-fc26-4fae-aa4a-8333a1093ce7)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/6f963ecf-5802-4fab-96b2-ce078e0aa48c)


  24. Analyze the disk image using Autopsy.
   
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/596e4f85-74ff-44b6-95fb-8997da828975)

  25. We can see Wanna Decryptor.exe in the executables section.

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/5eb94997-5e1e-4bdc-92e3-e409913a904a)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/f9af16eb-b0da-4934-bfcd-d58837a42ef8)


26. Generate the report.

  ![image](https://github.com/user-attachments/assets/1388c01d-8cbb-491a-8933-cf8e6a400eca)


27. Use Volatility Workbench in Windows (GUI) or the Volatility command-line tool in Linux to analyze the memory image dump.

 ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/98eb16e8-d1d0-4d65-b908-24dba318474f)

 28. The Wanna Decrypt0r process is an indication of a WannaCry infection.

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/61411f49-22d1-4e3d-8925-946a43c600b2)

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/695e9819-64bc-48a3-b4a0-bae8c9db161c)

## Conclusion

In my Digital Forensics project on WannaCry ransomware, I aimed to fully analyze the malware's behavior by setting up a secure, isolated Windows 10 virtual machine to safely execute the ransomware without risking external systems.

Disabled Windows Defender and SmartScreen protection to allow the ransomware to run unhindered, simulating a real-world infection.

Used FTK Imager to acquire both disk and memory images from the infected system, preserving critical data for analysis.

Utilized Autopsy for disk forensics, which allowed me to:

 - Examine the file system and locate suspicious files.
 
 - Identify how WannaCry modified key system structures.
 
 - Detect Wanna Decryptor.exe in the executables section, confirming the presence of the ransomware.
 
Performed memory forensics using Volatility to capture and analyze RAM dumps, enabling me to:

 - Track real-time ransomware activity.
 
 - Understand how the encryption routines were deployed to lock system files.
 
 - Document key Indicators of Compromise (IoCs) such as suspicious processes and system modifications.
 
Through this investigation, I gained valuable insights into WannaCry's propagation methods, encryption tactics, and overall system impact. This project sharpened my skills in both disk and memory forensics, providing a comprehensive understanding of how ransomware operates and how to detect and analyze its behavior in a real-world environment.

## Lessons learned:

Hands-on labs are crucial for security analysts because they replicate real-world attack scenarios, like WannaCry, allowing us to practice how we’d handle them in real time. Theoretical knowledge is great, but actually using tools like Autopsy and Volatility to investigate and respond to incidents gives us the experience we need to react quickly and effectively when something happens.

By working through these scenarios, we build muscle memory for identifying signs of an attack, analyzing compromised systems, and taking the right steps to mitigate the damage.
