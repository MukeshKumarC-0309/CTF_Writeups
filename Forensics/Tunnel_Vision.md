# Tunnel Vision (tunn3l v1s10n)

## Step by Step Solution
1. Download the file given in the challenge and check what type of file it actually is: `file filename`
2. Open it in a **hex editor** (a tool that shows you the raw bytes of a file). You'll notice the very first two bytes are `42 4D`, which is the "signature" that identifies a BMP image file.
3. Rename the file so it ends in `.bmp` and try opening it in an image viewer. It will either refuse to open or look cut off / broken.
4. Every BMP file has a "header" at the very start — a small block of bytes that tells the computer the image's width, height, and other details. In this challenge, one of those numbers has been deliberately changed to a wrong value, which is why the image won't display properly.
5. In the hex editor, find the width and height values in the header (they sit a short distance in from the beginning of the file).
6. Fix the incorrect value so the header makes sense again — for example, matching the height to the width, since the image was clearly stretched or cut off in one direction.
7. Save the file and open it again. The image will now display correctly, and the flag is written directly in the picture.
