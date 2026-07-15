# No Padding, No Problem

## Step by Step Solution
1. Read the challenge — you're given RSA public key values (`n`, `e`), a ciphertext `c` you want to decrypt, and access to a service/oracle that will encrypt or decrypt values for you (but won't decrypt your exact target ciphertext directly).
2. Because there's no padding scheme (like OAEP) in use, RSA's mathematical properties become directly exploitable — specifically its **multiplicative homomorphism**: `(m1 * m2)^e mod n = (m1^e mod n) * (m2^e mod n) mod n`.
3. Pick a small multiplier, e.g. `2`, and compute a modified ciphertext:
   ```python
   n = YOUR_N
   e = YOUR_E
   c = YOUR_CIPHERTEXT
   c2 = (pow(2, e, n) * c) % n
   ```
4. Send `c2` to the oracle/service instead of the original ciphertext (since services in these challenges often refuse to decrypt the exact target ciphertext, but will decrypt anything else).
5. The oracle will return `m2 = 2 * m mod n` (i.e. the original message multiplied by 2). Recover the original message:
   ```python
   m2 = ORACLE_RESPONSE_INT
   m = m2 // 2  # only works cleanly if no modular wraparound occurred
   from Crypto.Util.number import long_to_bytes
   print(long_to_bytes(m).decode())
   ```
6. If dividing by 2 doesn't give a clean result, account for the modulus (`m = (m2 * mod_inverse(2, n)) % n` handles the general case correctly).

## Concept
RSA without padding is malleable — an attacker can transform a ciphertext into a related ciphertext (e.g. one representing `2x` the original message) without knowing the private key, purely by exploiting the math. This is exactly why real-world RSA always uses padding schemes like OAEP: padding breaks this mathematical relationship and prevents this class of attack.
