# Easy1

## Step by Step Solution
1. Read the challenge — you're given ciphertext and a lookup table (a table mapping letters/bytes to encoded values), which represents a one-time pad (OTP).
2. A one-time pad XORs each plaintext character with a key character of equal length. With the table provided, this is done via lookup instead of manual XOR math.
3. Download the files given (ciphertext + key table, or a `.py` script that performs the encoding).
4. If a table is given, reverse the lookup: for each ciphertext value, find which plaintext letter maps to it under the corresponding key letter.
5. If it's a script-based OTP (XOR-based), decrypt in Python:
   ```python
   ciphertext = bytes.fromhex("YOUR_HEX_CIPHERTEXT")
   key = bytes.fromhex("YOUR_HEX_KEY")  # same length as ciphertext for a true OTP
   plaintext = bytes(c ^ k for c, k in zip(ciphertext, key))
   print(plaintext.decode())
   ```
6. Assemble the flag from the decoded plaintext.

## Concept
One-time pad — theoretically unbreakable *if* the key is truly random, used only once, and kept secret. This challenge is a bridge into XOR-based crypto, since OTP encryption/decryption is just XOR with a key of matching length.
