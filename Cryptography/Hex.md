# Hex

## Step by Step Solution
1. Read the challenge — you're given a string encoded in hexadecimal.
2. Hex-encoded data uses two characters (0-9, a-f) to represent each byte.
3. Decode it in Python using `bytes.fromhex()`:
   ```python
   hex_string = "YOUR_HEX_STRING"
   decoded = bytes.fromhex(hex_string)
   print(decoded.decode())
   ```
4. The decoded output is the flag.

## Concept
Hex encoding — a common way to represent raw bytes as printable text. `bytes.fromhex()` converts a hex string back to raw bytes; `.decode()` then converts those bytes to a readable string (assuming it's valid ASCII/UTF-8).
