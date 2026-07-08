# Tab, Tab, Attack

## Step by Step Solution
1. Download the zip file given in the challenge.
2. Unzip it in your terminal: `unzip filename.zip`
3. You'll see a folder with a long, strange, hard-to-type name. Instead of typing it out, just type the first letter and press the **Tab** key — the terminal will auto-complete the rest of the name for you.
4. Move into that folder with `cd`, then press Tab again to find and enter the next folder inside it.
5. Keep repeating `cd` + Tab until you reach a file at the very bottom of the folder chain (there are no more folders left, just a single file).
6. Check what kind of file it is: `file filename`
7. If it turns out to be a program, give yourself permission to run it: `chmod +x filename`
8. Run it: `./filename`
9. The flag will be printed straight to your screen.
