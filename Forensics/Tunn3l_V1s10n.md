# 2.Tunn3l_V1s10n

We found this file. Recover the flag.          

## Solution
We receive a file which has random gibberish when catted out.But on top it said 'BM' which could mean it’s a bitmap file.Hence i use exiftool to get more details and it's indeed a bitmap file but it is not opening which could indicate that the file is corrupted.Hence i open it in a hex editor and compare it with a working bmp file which indicates that the header was changed wantedly.Hence i change it and when i open it,i successfully get the image,but it shows a small image saying 'not a flag sorry'.Hence that was not the intended flag.But when examining the flag,it felt like it was cut out.So I had the idea of tampering with the size of the image.Also i analysed the way the sizes are mentioned.So i tampered with the length of the file changing to 800,which showed the flag.        

<img width="1242" height="465" alt="Screenshot 2025-10-24 at 9 02 04 PM" src="https://github.com/user-attachments/assets/2af0552b-6eb1-495c-8351-e82830e38b80" />       


![WhatsApp Image 2025-10-24 at 8 57 49 PM](https://github.com/user-attachments/assets/7c8281f0-1ebc-462a-bea3-9a49337754d4)        


![WhatsApp Image 2025-10-24 at 8 57 22 PM](https://github.com/user-attachments/assets/ad34fe37-b08f-4e0c-8cc3-b8ad8d2fd02f)         


![WhatsApp Image 2025-10-24 at 9 01 19 PM](https://github.com/user-attachments/assets/e7e2ce83-142a-424f-bbd8-6f58d52ffee6)        


![WhatsApp Image 2025-10-24 at 9 02 35 PM](https://github.com/user-attachments/assets/6f2b2dfa-2100-4690-85e7-317fe71e8fe4)         
    
        


## Flag
picoCTF{qu1t3_a_v13w_2020}        
    
## Concepts Learnt
I learnt about a new kind of file ie.BitMap File and how we can mess around with the details of the file to get the desired output.I learnt how to use a hex editor to change certain details of a file.       

## Resources Used
Neo,A hex editor                 
A sample bmp file which i sourced from the internet     
https://www.filesampleshub.com/format/image/bmp
