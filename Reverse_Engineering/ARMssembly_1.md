# 2.ARMssembly 1

For what argument does this program print `win` with variables 83, 0 and 3? File: chall_1.S Flag format: picoCTF{XXXXXXXX} -> (hex, lowercase, no 0x, and 32 bits. ex. 5614267 would be picoCTF{0055aabb})             

## Solution
The file given is an assembly file which was orginally written in C.Hence we look through the file to find some code which prints you win.We find that under .LC0.Hence when we read the main block we find that the value must be 0 for it run 'you win'.Hence,we go through the global func which results in giving the final variable.We see that it’s just a sequence of storing,loading,basic mathematics formulae.ldr stands for loading certain data onto a stack and str means to store a data onto the stack.mov puts the value into the variable.lsl refers to left bitwise shift.sdiv stands for division and sub stands for subtraction.As we go through the steps one by one,we find ourselves in the stage 'sub' wherein 27-w0(at 12)(initial argument) should result in the final value which we want it to be 0.Hence the value that we want is 27 which when converted to hex is 1B.Hence to match the format we put it as '0000001b' which is the answer.str and load has the stack position as argument.       

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/6fd60d95-41e1-4132-8327-161e6bf5a187" />      

<img width="1440" height="390" alt="image" src="https://github.com/user-attachments/assets/a677c56c-80ea-4351-b1ac-550d656bf239" />


## Flag
picoCTF{0000001b}         

## Concepts Learnt
I learnt how to read assembly files and what certain commands stands for and how they work such as mov,str,ldr,lsl and much more.It also helped me run through the code quickly to find the blocks of code which could actually help us.
