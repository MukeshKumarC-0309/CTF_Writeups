# 2.I like logic

We are required to analyse a sal file to get the right flag.                  

## Solution
So in the google drive we have been given a .sal file and a description which says 'i like logic and i like files, apparently, they have something in common, what should my next step be.'So I searched up what a .sal file is and learnt that it's a saleae logic analyser file.Hence i open up the logic analyser and run this code.We get 4 channels wherein only 1 channel has a thick bandwith of signals.Hence i zoom in and i see that it's pulsating square wave function.Hence i figured that analysing it would give me some kind of data.So i tried to put in a analyser.The async serial seemed to be the best fit for the analyser.Hence I chose that,applied default setting and set it.It showed some random values,hence i went to the analyser settings and set the data type to ascii and i got a huge rush of words.I copy pasted all of them in a notepad and went through it.In the middle the flag was hidden,hence finishing the challenge.                

<img width="1439" height="900" alt="Screenshot 2025-10-29 at 6 27 31 PM" src="https://github.com/user-attachments/assets/e9cf389c-7803-43ae-b774-1e1c8c248f92" />            


<img width="1439" height="900" alt="Screenshot 2025-10-29 at 6 27 45 PM" src="https://github.com/user-attachments/assets/c715a3d2-fa7d-44fe-8256-6ab0e1d722b8" />                      


<img width="574" height="839" alt="Screenshot 2025-10-29 at 6 28 03 PM" src="https://github.com/user-attachments/assets/3409bf5f-07c1-48ef-a925-fa777a9c7c5f" />                


## Flag
FCSC{b1dee4eeadf6c4e60aeb142b0b486344e64b12b40d1046de95c89ba5e23a9925}            

## Concepts Learnt
I learnt what a logic analyser is and how it can be used to record the digital and analog signals used to transmit information.        

## Resources Used
Saleae Logic 2 Analyser
