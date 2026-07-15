# Glory of the Garden

## Step by Step Solution
1. Download the file given in the challenge — it's usually an image (e.g. `garden.png`).
2. Don't just open it in an image viewer — the flag is hidden as extra text appended after the actual image data, which viewers ignore.
3. Use the `strings` command to pull out readable text from the binary file:
   ```bash
   strings garden.png | grep picoCTF
   ```
4. If `strings` doesn't catch it cleanly, try looking at the raw end of the file instead:
   ```bash
   tail -c 500 garden.png
   ```
5. The flag will appear as plain text mixed in with (or right after) the binary image data.

## Concept
Files can have extra data appended after their "logical" end (e.g. after the PNG end-of-file marker) without corrupting the file itself. `strings` and manual byte inspection are the standard first move whenever a challenge says "hidden in a file."
