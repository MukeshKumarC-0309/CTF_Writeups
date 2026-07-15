# XOR Properties

## Step by Step Solution
1. Read the challenge — you're given four files/values, typically representing:
   - `KEY1 ^ KEY2`
   - `KEY2 ^ KEY3`
   - `KEY3 ^ KEY4`
   - `KEY1 ^ KEY2 ^ KEY3 ^ KEY4` XORed with the flag (the "FLAG" file)
2. The key insight is the property `A ^ B ^ B = A` — XORing a value with itself cancels it out.
3. Combine the first three known values to recover `KEY1 ^ KEY2 ^ KEY3 ^ KEY4`:
   ```python
   part1 = bytes.fromhex("KEY1_XOR_KEY2_HEX")
   part2 = bytes.fromhex("KEY2_XOR_KEY3_HEX")
   part3 = bytes.fromhex("KEY3_XOR_KEY4_HEX")

   # KEY1^KEY2 ^ KEY2^KEY3 ^ KEY3^KEY4 = KEY1^KEY4 (KEY2, KEY3 cancel out)
   combined = bytes(a ^ b ^ c for a, b, c in zip(part1, part2, part3))
   ```
4. Work through which combination of the given parts cancels down to match what's needed to XOR against the flag file — the exact combination depends on which parts are given, but the cancellation principle (`X ^ X = 0`) is always the tool.
5. XOR that recovered value against the flag file's ciphertext to get the plaintext flag:
   ```python
   flag_enc = bytes.fromhex("FLAG_XOR_HEX")
   flag = bytes(a ^ b for a, b in zip(flag_enc, combined))
   print(flag.decode())
   ```

## Concept
XOR is commutative and associative, and any value XORed with itself is zero. This lets you cancel out unknown intermediate keys just by combining the right set of XOR results — a technique that shows up constantly in stream cipher attacks.
