# New Caesar

## Step by Step Solution
1. Download the files given — usually a Python script (e.g. `caesar.py`) showing the encryption logic, plus a ciphertext or output file.
2. Read the script carefully. "New Caesar" typically isn't a plain shift cipher — it combines an XOR step with a base-16 (hex) or custom arithmetic transformation on each character's ASCII value.
3. Trace through the script's `encrypt` function line by line, and write the exact inverse of each operation, in reverse order. For example, if encryption does `hex(ord(char) ^ key)`, decryption needs to reverse the hex encoding first, then XOR again with the same key (since XOR is its own inverse):
   ```python
   def decrypt(ciphertext_hex, key):
       plaintext = ""
       for pair in [ciphertext_hex[i:i+2] for i in range(0, len(ciphertext_hex), 2)]:
           byte_val = int(pair, 16)
           plaintext += chr(byte_val ^ key)
       return plaintext

   print(decrypt("YOUR_CIPHERTEXT_HEX", YOUR_KEY))
   ```
4. If the key isn't given, and you know the plaintext starts with `picoCTF{`, brute-force it by XORing the first ciphertext byte against `p` (0x70) to recover the key, then verify against the rest.
5. Run your reverse script against the full ciphertext to recover the flag.

## Concept
Custom/obfuscated ciphers built from XOR + encoding layers — the fix is always the same: read the source, and undo each transformation in exact reverse order. XOR is always self-inverting, which makes it the easiest layer to reverse once identified.
