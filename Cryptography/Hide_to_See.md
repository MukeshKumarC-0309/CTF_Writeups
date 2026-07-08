# Hide to See

## Step by Step Solution
1. Download the image file given in the challenge.
2. The challenge name is a hint about **steganography** — hiding one file secretly inside another, like a picture.
3. Use a tool called **steghide** to check if anything is hidden inside the image: `steghide extract -sf imagename.jpg`
4. When it asks for a passphrase, just press Enter (leave it blank) — many of these challenges don't use a password.
5. This pulls out a hidden text file (something like `encrypted.txt`). Open it up: `cat encrypted.txt`
6. The text inside looks scrambled — since the image file was named after (or the challenge hinted at) the **Atbash cipher**, a very old cipher that simply reverses the alphabet (A becomes Z, B becomes Y, and so on).
7. Paste the scrambled text into an online Atbash decoder (or the Atbash option in CyberChef) to reverse it.
8. Decoding it reveals the flag.
