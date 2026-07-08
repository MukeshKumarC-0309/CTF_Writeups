# Inspect Me

## Step by Step Solution
1. Open the challenge website in your browser.
2. Right-click anywhere on the page and select **"View Page Source"** (or press `Ctrl+U`).
3. Read through the HTML code carefully. Look for anything wrapped inside `<!-- -->` — this is called a comment, and it's not normally shown on the page itself.
4. You'll find one piece of the flag sitting inside a comment in the HTML.
5. The page also loads a CSS file and a JavaScript file (you'll see them linked near the top of the HTML, like `mycss.css` and `myjs.js`).
6. Visit those two files directly in your browser (just type their file name after the website's link) and look through them the same way.
7. Each file has a comment hiding one part of the flag.
8. Put all three parts together in the right order to get the complete flag.
