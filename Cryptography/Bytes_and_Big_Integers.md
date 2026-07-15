# Bytes and Big Integers

## Step by Step Solution
1. Read the challenge — you're given a large integer and asked to convert it into a byte string (which spells out the flag).
2. Python's `int.to_bytes()` handles this directly, but you need to know the byte length first. You can compute it from the integer's bit length:
   ```python
   n = YOUR_BIG_INTEGER
   length = (n.bit_length() + 7) // 8
   flag_bytes = n.to_bytes(length, byteorder='big')
   print(flag_bytes.decode())
   ```
3. Alternatively, if `pwntools` is available, use its `long_to_bytes()` helper:
   ```python
   from pwn import long_to_bytes
   print(long_to_bytes(YOUR_BIG_INTEGER).decode())
   ```
4. The decoded string is the flag.

## Concept
Integers and bytes are two representations of the same underlying data — this conversion (`bytes ↔ int`) is foundational for RSA, since RSA operates on integers but plaintext/ciphertext are conceptually byte strings.
