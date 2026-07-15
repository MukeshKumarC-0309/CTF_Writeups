# 2.Custom Encryption

Can you get sense of this code file and write the function that will decode the given encrypted file content.        
Find the encrypted file here flag_info and code file might be good to analyze and get the flag.        

## Solution
So,in this challenge we have been given two files,one with flag information and another python file which holds some certain program/algorithm which can be used for encryption.So,in a way we have to reverse the process to get the flag.So,instead of writing another program from scratch i decided to take the bits and pieces of the program that i need from the original program and reprogrammed it according to the goal.Then i created a loop to switch the ciphers back to the original decipher which is used as the plaintext.Then i meddle with the main program,the XOR program which can be used to find the ciphertext if the plain text and key is given.Hence i add an extra variable 'k' there that prints the key also just to view it.Then i run the program with 'picoCTF{' as the key as i thought that since it’s present in the flag it might be the clue or you know part of the clue.But it just printed some random output.But there was one part of the the ouput that intrigued me.Something like aedurtu.....         
This is because i remember seeing something similar to this in the main program under the __main__ variable,so that was my next guess as key.Fortunately,it was the right key and i managed to unlock the flag.            

<img width="957" height="593" alt="Screenshot 2025-10-27 at 8 38 59 PM" src="https://github.com/user-attachments/assets/b390feaa-6f1c-4e62-94c7-4d3d592c5ed0" />           

<img width="1090" height="130" alt="Screenshot 2025-10-27 at 8 39 29 PM" src="https://github.com/user-attachments/assets/08f452fc-77a4-4cec-93dd-6024c1e33d6c" />          

<img width="957" height="593" alt="Screenshot 2025-10-27 at 8 38 43 PM" src="https://github.com/user-attachments/assets/df9752b1-f046-4816-8a42-e4bdaf13a996" />          

<img width="1090" height="150" alt="Screenshot 2025-10-27 at 8 39 46 PM" src="https://github.com/user-attachments/assets/666dddf8-95d1-47e2-add1-2d2f8b01e0c4" />          

## Flag
picoCTF{custom_d2cr0pt6d_019c831c}            

## Concepts Learnt 
I learnt how to reverse a program to trace back the process that had already been completed with the given output and code structure as reference.
