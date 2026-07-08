# Information

## Step by Step Solution
1. Download the image file given in the challenge.
2. Install and run **exiftool**, a tool that reads hidden information (called metadata) stored inside a file, like the camera used, the date, or the author: `exiftool filename.jpg`
3. Look through the list of fields it prints out — one of them (often called "License", "Artist", or "Copyright") will contain a long, odd-looking string of letters and numbers.
4. That strange string is **Base64 encoded** text — a common way of disguising normal text so it looks scrambled.
5. Decode it, either using an online Base64 decoder or a terminal command like: `echo "the_odd_string" | base64 -d`
6. Decoding it reveals the flag.
