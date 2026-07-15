# You either know, XOR you don't

## Step by Step Solution
1. Read the challenge — you're given a hex-encoded ciphertext XORed with a repeating multi-byte key, and you're told (or it's a safe assumption) the plaintext starts with `crypto{`.
2. Since XOR is its own inverse, XOR the first 7 bytes of ciphertext with the known plaintext `crypto{` to recover the first 7 bytes of the key:
   ```python
   ciphertext = bytes.fromhex("YOUR_HEX_CIPHERTEXT")
   known_plaintext = b"crypto{"
   key_fragment = bytes(c ^ p for c, p in zip(ciphertext, known_plaintext))
   print(key_fragment)
   ```
3. If the key is shorter than or equal to 7 bytes, this fragment IS the full repeating key (possibly with repetition visible in the output). If longer, you may need to also guess the closing `}` at the end of the ciphertext to recover more key bytes.
4. Once you have the full key, XOR the entire ciphertext with it (repeating the key as needed):
   ```python
   key = key_fragment  # extended/repeated as needed
   plaintext = bytes(c ^ key[i % len(key)] for i, c in enumerate(ciphertext))
   print(plaintext.decode())
   ```
5. Submit the fully decoded flag.

## Concept
Known-plaintext attack against repeating-key XOR — if you know (or can guess) even a small part of the plaintext, you can XOR it against the matching ciphertext bytes to recover that portion of the key directly, then use the recovered key to decrypt everything.
