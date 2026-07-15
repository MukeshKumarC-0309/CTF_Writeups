# 2Warm

## Step by Step Solution
1. Read the challenge — it gives you a number in decimal (base 10) and asks for its binary (base 2) equivalent.
2. Open a terminal and use Python to convert it:
   ```bash
   python3 -c "print(bin(YOUR_NUMBER))"
   ```
3. `bin()` returns a string prefixed with `0b` — that prefix is usually part of the expected flag format, so don't strip it unless the challenge says otherwise.
4. Wrap the binary string in the flag format given by the challenge, e.g. `picoCTF{...}`.

## Concept
Number base conversion — decimal to binary. This is the same core idea as Warmed Up (hex to decimal), just a different base pair.
