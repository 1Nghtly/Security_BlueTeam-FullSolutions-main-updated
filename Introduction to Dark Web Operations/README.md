# Dark Web Operation Challenge Brief
```bash
Last month, our efforts led to the successful dismantling of a major drug trafficking network operating within the UK through the TOR network. The network's primary marketplace was taken down, significantly disrupting their operations and preventing further illicit substances from reaching our streets. However, critical intelligence suggests that one of the masterminds behind this network evaded capture and continued their illegal activities. They have established a platform to "tell their stories" of criminal exploits, serving as a covert hub for their operations. Your mission is to bring this individual to justice. This will not be easy, but we are confident in your expertise and ability to achieve this mission. Your success is pivotal to dismantling this criminal enterprise and safeguarding the public.

 
1] Gain Access to the Site: (Visit the URL below. Right-click and select “Inspect Element” when presented with a login screen. Select the ‘Console’ tab and enter the command: generateUserCredentials(). Decode the answer, and you’re good to go!) 

2] Find evidence that the individual(s) is involved in drug trafficking
 
3] Find any information about the locations in which these criminals congregate.

4] Site: http://panznjcktrpezyln5frnjxf5gv4xoyi7wvd3ykeu6bejxvbynhfpasqd.onion

 Requested Info:
==============================
1) What command is used in the Console to generate valid credentials? Provide the credentials, too. (Format: Command, Username, Password)
2) After logging in, what are the titles of the three pinned posts seen on the website in ASCII text? Please place them in respective order. (Format: Post 1, Post 2, Post 3)
3) Look at the Messages board. They are mentioning another illegal site. Provide its name. (Format: Hacker Group Name)
4) A transaction log is mistakenly visible under the “Recent Transactions” section. Provide the customer’s full name, email address, and the purpose of the transaction. (Format: Full Name, Email, Xxxxxxx and Xxxxx)
5) It looks like the user PJ is hosting an illegal party. What city is this taking place and when? We could catch him there and shut down this entire operation. (Format: City, Month DD, YYYY)
6) What is the email of the user selling ‘stolen’ car parts? (Format: Email)
```
# Approach
Download Tor Browser from [here](https://www.torproject.org/download/).

For security reasons, consider using a Virtual Machine (VM) or a VPN before connecting.

Open Tor Browser, connect, & paste the following link: [http://panznjcktrpezyln5frnjxf5gv4xoyi7wvd3ykeu6bejxvbynhfpasqd.onion](http://panznjcktrpezyln5frnjxf5gv4xoyi7wvd3ykeu6bejxvbynhfpasqd.onion)

![image](https://github.com/user-attachments/assets/ddcc322f-0915-4a30-9994-29f2da303a90)

Click on "Login" to reach the login page:

![image](https://github.com/user-attachments/assets/47665bf4-0f2e-473b-8c46-7e50dbc971a6)

Right-click, select "Inspect," navigate to the console, & execute the generateUserCredentials() command:

![image](https://github.com/user-attachments/assets/ca3ae97b-aff3-4a24-8dea-9294c05c6eb8)

Get a Base64 encoded string & Lets Decode everything. I used [Cyberchef](https://gchq.github.io/CyberChef/) to decode.

![image](https://github.com/ZuanAce/SecurityBlueTeam_challenge/assets/147037911/91ee091b-737e-41ab-a163-181d586f5d0b)

Login using the decoded credentials.

![image](https://github.com/user-attachments/assets/375a2a46-ad76-49f0-8f23-f2b5167ef58f)

1) What command is used in the Console to generate valid credentials? Provide the credentials, too. (Format: Command, Username, Password) 
- generateUserCredentials(), KF7ybuD1, Alyhfot0V9VIWm6W

2) After logging in, what are the titles of the three pinned posts seen on the website in ASCII text? Please place them in respective order. (Format: Post 1, Post 2, Post 3)

We can see hexadecimal ASCII values, which are easy to decode.

![image](https://github.com/user-attachments/assets/17e99ca1-fa43-4781-b4d8-688abaf77ae7)

Let’s break each post title down and convert the hex values to readable ASCII text.

I used [Rapidtables](https://www.rapidtables.com/convert/number/hex-to-ascii.html) to decode.

![image](https://github.com/user-attachments/assets/714679fa-fe91-450f-960d-5265eb6bd297)

- Now we can see that the answer is Drugs, Pleasure, Drops

3. Look at the Messages board. They are mentioning another illegal site. Provide its name. (Format: Hacker Group Name)

![image](https://github.com/user-attachments/assets/70110972-2060-4219-8890-8a1b6a39f203)

After clicking on the link from the user "Basilisk95" we'll get taken to a new site "$ ./Midnite... Darkness... Awaits"

![image](https://github.com/user-attachments/assets/e1514ba1-2b26-4341-ae49-652f9b3231b6)

- The answer is Midnite

4. A transaction log is mistakenly visible under the “Recent Transactions” section. Provide the customer’s full name, email address, and the purpose of the transaction. (Format: Full Name, Email, Xxxxxxx and Xxxxx)

![image](https://github.com/user-attachments/assets/35943b2e-8b6d-4b2a-bfd6-ac482b61769e)

After clicking on the "$7000" link we'll be taken to a .pdf file that will show customer information.

![image](https://github.com/user-attachments/assets/a55fcbd1-edf2-484f-a6d7-b5eda5ead038)

- The Customers full name, email address, and the purpose of the transaction is Frank Castle, frankcastle2093@gmail.com, Hookers and Drugs

5. It looks like the user PJ is hosting an illegal party. What city is this taking place and when? We could catch him there and shut down this entire operation. (Format: City, Month DD, YYYY)

![image](https://github.com/user-attachments/assets/f18d7236-dd07-408b-b8be-c7d6daf02e7d)

After downloading the image I used [a Steganography decoder](https://stylesuxx.github.io/steganography/) to decode the image from which we got a line of text:

![image](https://github.com/user-attachments/assets/9732a6c0-23a8-440d-8e26-1233d65c9240)

"Where the red dragon flies and the Severn meets the sea. Find the capital of Cymru, where your next adventure will be."

Interpretation:

"Where the red dragon flies"
The red dragon is a national symbol of Wales.

"Where the Severn meets the sea"
The River Severn flows into the sea near the southern coast of Wales.

"Capital of Cymru"
Cymru is the Welsh name for Wales.

So the capital of Cymru is:
Cardiff

And we could see the date below, 

![image](https://github.com/user-attachments/assets/67b26923-4db0-434d-b36b-0ec77fe8728c)

- The answer is Cardiff, February 14, 2025

6. What is the email of the user selling ‘stolen’ car parts? (Format: Email)

![image](https://github.com/user-attachments/assets/3f6c4c3f-ca23-4799-8564-473ca5ec4766)

Once again we can see hexadecimal ASCII values and using the site mentioned before we can easily find out the email address.

![image](https://github.com/user-attachments/assets/988c0c6d-8764-4329-8070-b04d2ca05aba)

- The email address is twizzerichard@gmail.com

# Tools Used:
- Rapidtables
- Cyberchef
- Tor Browser
- Stylesuxx Steganography
  
# Thanks for reading!



