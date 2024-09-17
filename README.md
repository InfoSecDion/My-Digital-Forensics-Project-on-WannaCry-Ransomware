# My-Digital-Forensics-Project-on-WannaCry-Ransomware

# Digital-forensics
## Description
Set up an isolated environment to safely execute the WannaCry ransomware without affecting external systems.

Conducted detailed disk forensics using Autopsy to analyze file structures, locate suspicious files, and identify the behavior of the ransomware on the infected system.

Performed memory forensics using Volatility to capture and examine memory dumps, uncovering real-time ransomware activities and process behavior.

Identified key indicators of compromise (IoCs) and documented the ransomware’s impact on both the disk and memory, providing insight into its propagation and encryption tactics.

## Steps
1. Setup up  isolated windows 10 Virutal machine without any internet connection

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/2b365fb7-9af3-4f68-bf48-7a147943ca7a)

3. Disable windows defender realtime protection and smartscreen protection
4. Download and run the wannacry ransomeware

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/0fdbf265-910c-4dad-b3ea-4403b51757f4)

5. Download and install the FTK imager in removable device
6. Use FTK imager to get Disk and memory image
7. Click file -> Select Create disk image
   
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/0ec53541-d60e-4f39-99e3-bc5831c56c94)


7. Select Logical drive
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/08bbd237-a37a-4bbc-a289-fd90c0f8d3fe)

8. Select specific Drive
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/fb35ae58-775f-4f77-90a6-44b29a134753)

9. Select File type

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/803a345a-76b1-43a3-8997-0f3be4fa3ba8)

10 . Enter evidence item information

  ![image](https://github.com/user-attachments/assets/e30546ad-3421-47ca-86d9-1c3e72fd3ee3)

11. Select image destination folder make sure enough space available in that drive (removeble drive preferable for securly analysze a image in remote testing machine from infected machine)
12. Enter image file name without extension
13. Use segmentation (optional)
14. click finish

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/017c0783-4aaf-46e6-9357-73ec53e06957)

15. immage genrated successfully in the respective drive/folder
  
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/be3e08ac-8e5d-4810-adfd-a7d00d22f6d2)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/9323f36f-46fa-4639-bf1d-7b2622ae6094)

16. click file -> select capture memory

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/37f600cd-d8be-4e27-907c-487273fddbf3)

17.  Enter Destination folder to store memory image (removeble drive preferable for securly analysze a image in remote testing machine from infected machine)
18.  click capture memory
     
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/fec21965-899e-4e46-826c-b48aeb6ce70f)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/b8b4dde0-eb0f-4c70-85df-cf9c9f1059dd)
  
19. Download and install Autopsy in test machine (isolated from infected machine)

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/668084a1-84e6-4578-b7c3-81345814cd4d)

20. Create a  new Case in Autospy

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/6f11cc33-be9d-4a23-9739-483876d62a51)

 21. Enter case information
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/63e1083c-851d-44c0-bb4d-6c2067acf12f)

   ![image](https://github.com/user-attachments/assets/af70206b-7c2c-493d-a2fa-9839abc4e800)

22. Select and add Data source
    
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/bbc2eee2-3714-410a-a951-a7395a172598)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/94680ea4-8101-46ae-8296-b3e260fff446)

23. Select Path of the disk image file (Autopsy automatically select all segments)
    
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/595d042a-1b20-48d4-a1fc-4fb0df413a66)
   
   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/53dce4d4-800c-47f0-93da-3c5d41d036aa)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/2a465fb1-fc26-4fae-aa4a-8333a1093ce7)

   ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/6f963ecf-5802-4fab-96b2-ce078e0aa48c)


  24. Analyse the Disk image with Autopsy
   
  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/596e4f85-74ff-44b6-95fb-8997da828975)

  25 .we can see wanna Decrypter.exe in executebles section

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/5eb94997-5e1e-4bdc-92e3-e409913a904a)

  ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/f9af16eb-b0da-4934-bfcd-d58837a42ef8)


26. Genrate a report

  ![image](https://github.com/user-attachments/assets/1388c01d-8cbb-491a-8933-cf8e6a400eca)


27. Use volatility workbench in windows (GUI) or volatility coandline tool in linux to analyse memory image dump

 ![image](https://github.com/George-1100/Digital-forensics/assets/76154087/98eb16e8-d1d0-4d65-b908-24dba318474f)

 28. wanna Decrypt0r process indication of wannacry infection.

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/61411f49-22d1-4e3d-8925-946a43c600b2)

![image](https://github.com/George-1100/Digital-forensics/assets/76154087/695e9819-64bc-48a3-b4a0-bae8c9db161c)
