# Trivial Flag Transfer Protocol

## Step by Step Solution
1. Download the `.pcapng` file given — this is a recording of network traffic.
2. Open it in **Wireshark**.
3. Go to **File > Export Objects > TFTP** (TFTP is a simple, unencrypted method of sending files over a network, and it's what was used in this capture).
4. You'll see a list of files that were transferred. Save/export all of them to your computer.
5. Open the text files first. Their content will look like scrambled nonsense — this is a simple substitution cipher called **ROT13** (every letter is just shifted 13 places in the alphabet).
6. Paste the scrambled text into any online ROT13 decoder to read the real message.
7. The decoded message tells you that a program was used to hide the flag inside one of the picture files, and gives you a password.
8. That "program" turns out to be **steghide**, a tool that hides secret data inside image files. Install it if you don't already have it.
9. Use steghide with the password you found to try extracting hidden data from each image, one at a time: `steghide extract -sf picture1.bmp -p PASSWORD`
10. One of the images will successfully extract a text file — open it, and there's your flag.
