# XOR Starter

## Step by Step Solution
1. Read the challenge — you're given a hex-encoded ciphertext and a single repeating XOR key (often given directly, e.g. as an integer or short string).
2. XOR each byte of the ciphertext with the corresponding byte of the key, repeating the key as needed:
   ```python
   ciphertext = bytes.fromhex("YOUR_HEX_CIPHERTEXT")
   key = b"YOUR_KEY"  # or a single repeated byte, depending on the challenge
   plaintext = bytes(c ^ key[i % len(key)] for i, c in enumerate(ciphertext))
   print(plaintext.decode())
   ```
3. If the key is a single byte (not a string), XOR every ciphertext byte with that same value instead.
4. The decoded output is the flag.

## Concept
XOR encryption — the core operation behind stream ciphers. XORing a byte with the same key byte twice returns the original byte (`c ^ k ^ k == c`), which is why XOR is reversible and used as the foundation for more complex crypto.
