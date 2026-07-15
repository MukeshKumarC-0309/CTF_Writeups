# Factoring

## Step by Step Solution
1. Read the challenge — you're given RSA public key values: a modulus `n`, public exponent `e`, and a ciphertext `c`. The challenge hints that `n` is small enough to factor directly.
2. Factor `n` into its two prime factors `p` and `q`. For small `n`, the easiest approach is FactorDB:
   - Go to http://factordb.com
   - Paste in the value of `n`
   - It will usually already have the factorization on record for small/known values
3. Alternatively, factor it programmatically with `sympy`:
   ```python
   from sympy import factorint
   n = YOUR_N
   print(factorint(n))
   ```
4. Once you have `p` and `q`, compute the totient and private exponent:
   ```python
   from sympy import mod_inverse
   p, q = YOUR_P, YOUR_Q
   n = p * q
   e = YOUR_E
   phi = (p - 1) * (q - 1)
   d = mod_inverse(e, phi)
   ```
5. Decrypt the ciphertext using the private exponent:
   ```python
   c = YOUR_CIPHERTEXT_INT
   m = pow(c, d, n)
   from Crypto.Util.number import long_to_bytes  # or a manual int-to-bytes conversion
   print(long_to_bytes(m).decode())
   ```
6. The decoded output is the flag.

## Concept
RSA's security depends entirely on `n` being computationally infeasible to factor. When `n` is small (a toy/teaching example), factoring is trivial, and once you have `p` and `q` you can derive the private key and decrypt directly — this is the whole point of the challenge: showing what breaks when the "hard problem" isn't actually hard.
