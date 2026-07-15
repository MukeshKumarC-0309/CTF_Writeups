# 1.Mod 26
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_MAZyqFQj}          

## Solve
So i researched what ROT 13 and found an online decoder that converts the plaintext to ciphertext using the ROT-13 logic.I applied the given ciphertext and it converted it into plaintext.                 

## Flag
picoCTF{next_time_I'll_try_2_rounds_of_rot13_ZNMldSDw}        


# 2.13
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}

## Solve
Similar to the previous problem,i used the same decoder to get the flag.      

## Flag
picoCTF{not_too_bad_of_a_problem}

# 3.Interendec
Can you get the real meaning from this file.

## Solve
So,on first glance it seemed similar to a encoded base 64 string.Hence i use a decoder to convert it which gave another string under b''.Since it still looked like base64,i used the decoder again and then it seemed like caeser cipher was used.Hence I used a decoder to gauge possible interpretations and found the right one.      

## Flag
picoCTF{caesar_d3cr9pt3d_78250afc}            

# 4.Unminify
I don't like scrolling down to read the code of my website, so I've squished it. As a bonus, my pages load faster!
Additional details will be available after launching your challenge instance.

## Solve
As i saw the website,there was no clues given on the homepage,since it mentioned that it was squished,i used the curl command to see the details and i saw that the flag was hidden there.        

## Flag
picoCTF{pr3tty_c0d3_b99eb82e}

# 5.Format String 0
Can you use your knowledge of format strings to make the customers happy?
Download the binary here.
Download the source here.
Additional details will be available after launching your challenge instance.

## Solve
This involves the use of binary exploitation,hence i look through the source code and find the buffers which can be exploitated using various tricks.In the first part,it asks us to choose between 3 items,i chose the grilled cheese one because it has '%114d' which when used gives us a number of 114 characters which exceeds the buffer breaking it.In the next step,i choose the Cla%sic_Che%s%steak becuse mentioning '%s' without giving the string causes an error thereby breaking the buffer which gives us the final flag value.        

## Flag
picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_dc0f36c4}

# 5.Fantasy CTF
Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.        

## Solve
On establishing the netcat connection,it takes us through a story stimulation which tells us on how a ctf works and asks us to choose the right options.It also teaches us some basics about the terminal and in the end we get the flag.        

## Flag
picoCTF{m1113n1um_3d1710n_3b6c6fab}        

# 6.Binary Search
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
You can download the challenge files here:
challenge.zip        

## Solve
So,upon setting the netcat connection,we see that it’s a game where we have to find the correct number.We can use the process of binary search where we keep moving between two halfs of numbers depending on if it's higher or lower.Doing so helped us find the right number,thereby giving us the flag.          

## Flag
picoCTF{g00d_gu355_1597707f}
