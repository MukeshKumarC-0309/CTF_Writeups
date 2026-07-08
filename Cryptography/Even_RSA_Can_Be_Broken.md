# Even RSA Can Be Broken

## Step by Step Solution
1. Connect to the challenge server using netcat (a tool for talking directly to a server over the network): `nc server-address port`
2. The server sends you three values: **N** (a big number), **e** (a small number), and a **ciphertext** (the encrypted flag).
3. Normally, RSA encryption is unbreakable because N is made by multiplying two huge, secret prime numbers together, and figuring out those two numbers is extremely hard.
4. Here's the twist: check if N is an **even number** (ends in 0, 2, 4, 6, or 8). If it is, that's a big mistake by whoever set up the encryption — it means one of the two secret numbers is simply **2** (the only even prime number).
5. Since one of the numbers is already known (2), finding the other one is easy: just divide N by 2. `q = N / 2`
6. With both secret numbers known, you can now work out the private "key" needed to decrypt the message, using a small Python script (using the `pycryptodome` library) that:
   - Calculates `phi = q - 1`
   - Calculates `d = inverse of e, mod phi`
   - Decrypts using `m = pow(ciphertext, d, N)`
   - Converts the resulting number back into readable text
7. Running the script prints the flag directly.
