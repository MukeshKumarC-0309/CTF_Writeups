# String It

## Step by Step Solution
1. Download the file given in the challenge. Do **not** try to run it — the challenge wants you to find the flag without executing the file.
2. Open a terminal and use the `strings` command, which pulls out all the readable text hidden inside a file: `strings filename`
3. This will print a huge wall of text, way too much to scroll through by hand.
4. Filter it down using `grep`, which searches for a specific word: `strings filename | grep picoCTF`
5. This single command finds the line containing the flag and prints it straight to your screen.
