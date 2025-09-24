# Introduction
This section talks about password-protected files, and how they can be cracked with brute force or dictionary attacks.

# Cracking ZIP Files Activity and Quiz

1. Launch kali linux and then download the file.
2. Unzip the file using the command *unzip filename* replacing the filename with the name of the downloaded file
3. Navigate to SBT_Steg_Lab using the command *cd SBT_ZIP_Cracking*

To get started, make sure you have downloaded the file(s) and read the instructions location on the Cracking ZIP Files Activity and Quiz section. Let's get started below (for context, I am using a Kali Linux 2022 VM ARM-based).

 

What is the working password to unlock BruteForceAttack.zip?

After running the command seen in the image below, I found the password to be a1b3c5


![image](https://github.com/user-attachments/assets/9e538706-fab5-4f8c-90a6-2098c67cf84f)

 
What is the working password to unlock DictionaryAttack.zip?

Utilizing the same method from above, I found the password to be FRIENDSHIPSTARS

![image](https://github.com/user-attachments/assets/b0b9331d-fa20-4700-bfe5-b48c802ca60a)


What is the text string inside FLAG1.txt?

After unzipping BruteForceAttack.zip with the password a1b3c5, I managed to find the string: J201AKKLO

![image](https://github.com/user-attachments/assets/9060458c-31fc-428a-bab6-d731a9c6cd65)

What is the text string inside FLAG2.txt?

After unzipping DictionaryAttack.zip with the password FRIENDSHIPSTARS, I managed to find the string: 91MD0QL11

![image](https://github.com/user-attachments/assets/99e99899-069b-4a94-ad71-016c5c349fd5)

