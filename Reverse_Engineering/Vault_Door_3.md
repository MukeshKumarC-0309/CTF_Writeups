# 3.Vault Door 3

This vault uses for-loops and byte arrays. The source code for this vault is here: VaultDoor3.java     

## Solution

Here,when i downloaded the java file.I first tried to running it directly but to no avail as i did not have the vault passcode.Then when i read between the lines of code,i realised that there was a certain block of code which could give us the flag.Since i did not have much experience in java,i tried to recreate the same logic in python.When i wrote a new block of code in python for the same logic and run it with the same arguments,we successfully obscured the flag.   
     
<img width="686" height="780" alt="image" src="https://github.com/user-attachments/assets/9a47f985-dcc1-46f0-84b7-4235495da5bc" />      

<img width="686" height="780" alt="image" src="https://github.com/user-attachments/assets/3320460c-0339-46f2-91ae-cf7c06e735c9" />      

<img width="460" height="329" alt="image" src="https://github.com/user-attachments/assets/807d9155-46ea-475a-b0eb-d14486a104b0" />
     
<img width="1104" height="62" alt="image" src="https://github.com/user-attachments/assets/4192553c-eff9-44aa-a267-82bfe02f32d0" />     

'''
password = list("................................")
sample = "jU5t_a_sna_3lpm18gb41_u_4_mfr340"

for i in range(0, 8):
    password[i] = sample[i]

for i in range(8, 16):
    password[23-i] = sample[i]

for i in range(16, 32, 2):
    password[46-i] = sample[i]

for i in range(31, 16, -2):
    password[i] = sample[i]

flag = ''.join(password)
print(f"Flag: picoCTF{{{flag}}}")
'''    
   
## Concepts Learnt     
I learnt the concept of reading in between codes to find out the right part which can be executed to get the code.    
    
## Notes    
I had some initial trouble running the code as i tried to directly run the java code which kept asking for the password,which i didn’t have.
