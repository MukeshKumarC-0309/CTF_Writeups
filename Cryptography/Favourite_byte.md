# Favourite byte

## Step by Step Solution
1. Read the challenge — you're given a hex-encoded ciphertext that's been XORed with a single, unknown byte (0-255).
2. Since there are only 256 possible keys, brute-force all of them:
   ```python
   ciphertext = bytes.fromhex("YOUR_HEX_CIPHERTEXT")
   for key in range(256):
       plaintext = bytes(c ^ key for c in ciphertext)
       if b"crypto{" in plaintext:
           print(key, plaintext.decode())
   ```
3. The loop will print the byte value and decoded flag when it hits the correct key — recognizable because the output contains `crypto{`.
4. Submit the decoded flag.

## Concept
Single-byte XOR brute force — with only 256 possible keys, you don't need to be clever, you can just try them all and filter for readable/expected output. This is the simplest form of a known-plaintext-style attack (you're not told the key, but you know part of the expected result).
