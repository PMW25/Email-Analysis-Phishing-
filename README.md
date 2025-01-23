# Email-Analysis-Phishing-

In The Planet’s Prestige, a fake scenario is presented where a planetary president’s daughter has went missing. Amidst a multi-planet revolution, a ransom note is sent via email with a pricy task request. With clues throughout the email I did some investagation to determine a lead to the the President’s daughter. 

What is the email service used by the malicious actor?
Email headers contain information about the source of the email, and where it has traveled in order to land in your inbox. It is important to note that some headers can be faked if an environment is set correctly. To view the email header information, The email can be opened in a text editor such as Notepad++. Line 28 shows that the email was sent from IP 93.99.104.210, with the sending domain.

Answer: emkei.cz

![Screenshot 2025-01-22 001521](https://github.com/user-attachments/assets/72edc799-d952-4cb5-a180-725a206ccecc)

Did a little research from google and found out the email service is actually a fake email service.

![Screenshot 2025-01-22 001615](https://github.com/user-attachments/assets/ad38dec8-c3de-4140-8196-6b206cce8fe5)



What is the Reply-To email address?
The reply-to field shows where any response to this email will be sent to. The email address domain is the service being used by the malicious actor. This can be found on line 44 in a text editor, or by searching for the Reply-To field.

Answer: negeja3921@phashter.com

What is the filetype of the received attachment which helped to continue the investigation?
The email attachment arrived as a pdf file, however a browser cannot properly view the PDF. This is because the PDF is actually a zip file. This could be discovered if the file is opened in a text editor, names of contained files will appear, implying that this is a zip file. 7-zip can also “open inside” the file, revealing all contained files.

![Screenshot 2025-01-21 232857](https://github.com/user-attachments/assets/05feb175-fcbd-488e-a371-c6b1b84519b8)
![Screenshot 2025-01-21 233341](https://github.com/user-attachments/assets/2a4538cb-2c6a-4c78-b98c-4d5c3f01b7cb)

Answer: .zip

What is the name of the malicious actor?
By using exiftool, metadata about the PDF can be discovered, where other tools might only identify anticipated metadata fields based on the file type. One of the metadata fields includes the author of this document.

Answer: Pestero Negeja






What is the location of the attacker in this Universe?
The previously analyzed PDF specifies which file to look at, Money.xlsx. This file can be discovered by a number of ways, but ultimately can be made visible in the same directory as the PDF by selecting “show hidden files”.

Screenshot of excel spreadsheet showing sheet 3 with a highlighted cell containing the encrypted location of the malicious actor.

![Screenshot 2025-01-22 000749](https://github.com/user-attachments/assets/e83c1bdc-e2d6-4de8-ba51-8ff5482e3ecc)
![Screenshot 2025-01-22 001415](https://github.com/user-attachments/assets/0fbbf8af-ca39-45bd-a9c1-8df90ca35b53)


There are two pages with text. While there are numerous ways the answer can be located, I created a conditional formatting rule to highlight all cells that contains any text. The text is in the second page. Using Cyberchef to decode this, the location of the malicious actor was revealed.


![Screenshot 2025-01-22 001429](https://github.com/user-attachments/assets/c043c280-6f51-484a-90a1-3a797bc2cc43)

Answer: The Martian Colony, Beside Interplanetary Spaceport




What could be the probable C&C domain to control the attacker’s autonomous bots?
Since all mail that responds to this email goes to the listed Reply-To, it is probable that the autonomous bots are controlled under the same domain, and are listening for events sent by that domain.

Answer: phashter.com
