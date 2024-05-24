# Email_Phish_Analysis_Lab

## Objective
The phish email analysis lab project aimed to gain experience on reviewing an email and the different parts of the headers to respond to a possible phishing email. detecting cyber attacks.
### Skills Learned
- Reviewing different components within the email headers.
- Interpreting information from the headers to investigate the content of the email.
- Proficiency in analyzing an email for a potential phishing attack
### Tools Used
- Cyberchef was used in order to convert base64 so that we can review the content
- Gary Kesslers signatures (garykessler.net)
## Steps 
- Review the email in a text editor
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/d225bcc2-2505-4e81-910e-aff8c78d92ae)
- We notice that SPF = failed and the domain Microapple.com does not permit 93.99.104.210 as a sender
![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/670d6351-39be-418b-999d-d4346d3baf90)
- We can also see that the malicious actor is using emkei.cz as a service
![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/4020f8fb-c8c2-4d66-b17d-6e4dd45a7cc6)
- Notice that the 'Reply-to' field is different than the 'from' field
![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/4f35d4f7-51d8-4e56-bd3e-c1177b03ad52)
- Now the content is using plain text formatting with an encoding of base64
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/3356d10d-037b-442e-ad6c-011a79821031)
- Cyber chef will be used in order to decode the Base 64 and this is the message that is decoded
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/82d230f3-e12c-4b40-8d7d-38ff7c12aee2)
- Now we can see that there was an attachment after the message named puzzletococanda.pdf 
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/39d2f515-1435-4c50-9ddd-d8dde4627d0e)
- After decoding this is what we receive in cyber chef
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/8e92685f-d97c-4eb6-9935-e7985c01c866)
- Converting this file to Hex to use the first 4 bytes in order to get the file signature
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/ad3854cb-e243-4d67-8020-2c445ec05e52)
- We'll be using Gary Kesslers signatures. Do a ctrl + f and paste in the first 4 bytes to search for the file signature
- ![image](https://github.com/Brandencampos/Email_Phish_Analysis_Lab/assets/62733055/259c9d30-6d02-4330-bf77-5feb0f74327a)
- Even though the email said that the file was a PDF it is really a .zip


