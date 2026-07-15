# 6.Binary Search

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
You can download the challenge files here:
challenge.zip        

## Solve
So,upon setting the netcat connection,we see that it’s a game where we have to find the correct number.We can use the process of binary search where we keep moving between two halfs of numbers depending on if it's higher or lower.Doing so helped us find the right number,thereby giving us the flag.          

## Flag
picoCTF{g00d_gu355_1597707f}
