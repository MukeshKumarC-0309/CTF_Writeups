# Vigenere

## Step by Step Solution
1. Read the challenge — you're given ciphertext encoded with a Vigenère cipher, and usually a hint about the key or a known plaintext fragment (often the flag starts with `picoCTF{`, which you can use to derive the key).
2. The Vigenère cipher shifts each letter of the plaintext by an amount determined by the corresponding letter of a repeating key (like a Caesar cipher where the shift changes every letter).
3. If you know the key already, decrypt directly:
   ```python
   def vigenere_decrypt(ciphertext, key):
       result = []
       key = key.upper()
       ki = 0
       for c in ciphertext:
           if c.isalpha():
               shift = ord(key[ki % len(key)]) - ord('A')
               base = ord('A') if c.isupper() else ord('a')
               result.append(chr((ord(c) - base - shift) % 26 + base))
               ki += 1
           else:
               result.append(c)
       return ''.join(result)

   print(vigenere_decrypt("YOUR_CIPHERTEXT", "YOUR_KEY"))
   ```
4. If you don't have the key but know the plaintext starts with `picoCTF{`, you can derive the key from the first several characters of ciphertext by reversing the shift, then use that key to decrypt the rest.
5. Assemble the result into the flag format.

## Concept
Vigenère is a polyalphabetic substitution cipher — it defeats simple frequency analysis (unlike Caesar) because the shift changes per letter, but it's broken instantly once the key length or key itself is known.
