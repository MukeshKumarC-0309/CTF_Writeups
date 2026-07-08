# Caesar

## Step by Step Solution
1. Download the file given in the challenge and open it: `cat ciphertext` — you'll see a string of scrambled letters.
2. The challenge name tells you exactly what's used here: a **Caesar cipher**, where every letter is shifted forward by the same fixed number of places in the alphabet (for example, shifting by 3 turns A into D).
3. Since there are only 26 possible shift amounts, you don't need to guess randomly — just try every single one.
4. Paste the scrambled text into an online Caesar cipher tool (like the one on dcode.fr or CyberChef), and either let it auto-detect the shift or manually try shifts 1 through 25.
5. Look through the results for the one that actually turns into readable English words.
6. That readable version is your flag.
