# 1.Trivial Flag Transfer Protocol

Figure out how they moved the flag.                            

## Solution
Here,We are given a pcapng file which contains some clue about the data.Hence we open the file in wireshark to inspect the network and we see that some files have been send through the tftp protocol.Hence we use the export files option and take the files from tftp.They include 3 bmp pictures,a debian package and 2 files named plan and instructions.txt.When I open instructions.txt.On opening them i found out that i had to use the ROT-13 decoder to get both the messages.Hence I got 'TFTP DOESNT ENCRYPT OUR TRAFFIC SO WE MUST DISGUISE OUR FLAG TRANSFER.FIGURE OUT AWAY TO HIDE THE FLAG AND I WILL CHECK BACK FOR THE PLAN' and 'I USED THE PROGRAM AND HID IT WITH-DUEDILIGENCE.CHECK OUT THE PHOTOS'.Hence i assume that the debian package might have something to help us out with.Hence when i open it using an installer i found an exe file called steghide.Steghide is a steganography tool which can be used to find hidden text or details in images.So i load up the exe file in terminal give the necessary arguments such as 'extract','-sf',and checked all the files one at a time giving the passphrase as 'DUEDILIGENCE'.In the 3rd picture it found some text which was then sent to flag.txt.When opened it showed us the flag value.                                    

![WhatsApp Image 2025-10-24 at 9 18 17 PM](https://github.com/user-attachments/assets/af84d699-5801-4b07-8838-cf912a3d590a)         

<img width="757" height="33" alt="Screenshot 2025-10-25 at 6 37 38 PM" src="https://github.com/user-attachments/assets/84422ae7-9168-4c17-af90-251554f0f335" />      

<img width="429" height="33" alt="Screenshot 2025-10-25 at 6 37 06 PM" src="https://github.com/user-attachments/assets/ab685a50-65fc-49a8-bcd3-2a33dc80bd22" />         

<img width="1440" height="586" alt="Screenshot 2025-10-25 at 7 12 30 PM" src="https://github.com/user-attachments/assets/44f15516-a879-4a13-ac37-f753cdf056b1" />     

<img width="1440" height="586" alt="Screenshot 2025-10-25 at 7 12 24 PM" src="https://github.com/user-attachments/assets/3bd1328a-5b8c-4949-8211-6ffb4aeee559" />       

![WhatsApp Image 2025-10-25 at 6 22 40 PM](https://github.com/user-attachments/assets/86ca6c60-2d36-488f-ba40-db366850575d)        

![WhatsApp Image 2025-10-25 at 6 23 01 PM](https://github.com/user-attachments/assets/cb8e1283-78d6-46fa-b38f-d9d04c651674)                                    

## Concepts Learnt
I learnt to read the pcapng file with the help of wireshark that can help us analyse networks and export files according to the protocol they were sent with.I learnt how to deal with debian packages,use stenography tools to find hidden details in images in this case bmp files.                            

## Resources Used
https://cryptii.com/pipes/rot13-decoder
