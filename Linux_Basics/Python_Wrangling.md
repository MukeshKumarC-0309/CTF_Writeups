# Python Wrangling

## Step by Step Solution
1. Download the three files given: a Python script (e.g. `ende.py`), a password file (`pw.txt`), and an encoded flag file (`flag.txt.en`).
2. Open a terminal and try running the script with no options: `python3 ende.py`
3. It will show you a "Usage" message explaining how to use it, something like: `Usage: ende.py (-e/-d) [file]` — meaning `-e` encodes and `-d` decodes.
4. Since you want to decode the flag, run: `python3 ende.py -d flag.txt.en`
5. It will ask you for a password. Open the password file to see it: `cat pw.txt`
6. Copy the password and paste it in when prompted.
7. The script decodes the file and prints the flag directly to your screen.
