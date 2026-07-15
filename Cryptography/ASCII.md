# ASCII

## Step by Step Solution
1. Read the challenge — you're given a Python list of decimal numbers representing ASCII character codes.
2. Each number maps directly to a character via the ASCII table (e.g. 99 → 'c').
3. Convert the list to a string using Python's `chr()`:
   ```python
   nums = [99, 114, 121, 112, 116, 111, ...]  # replace with the actual list given
   flag = ''.join(chr(n) for n in nums)
   print(flag)
   ```
4. The printed string is the flag — submit it as-is.

## Concept
ASCII encoding — every printable character has a corresponding decimal (and hex) code. `chr()` and `ord()` are the two functions used constantly throughout CryptoHack to move between characters and their numeric codes.
