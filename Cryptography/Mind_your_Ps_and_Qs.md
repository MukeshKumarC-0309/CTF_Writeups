# Mind Your P's and Q's

## Step by Step Solution
1. Download the file given in the challenge and open it: `cat values` — you'll see three numbers labeled **c** (ciphertext), **n**, and **e**. These are all part of RSA encryption.
2. Normally, N is built by multiplying two enormous secret prime numbers together, and that's what makes RSA secure — factoring N back into those two numbers is supposed to be nearly impossible.
3. The challenge hints that this particular N is small enough to actually be factored, meaning we can find the two secret numbers hiding inside it.
4. Go to an online tool like **factordb.com** or **dcode.fr**, paste in the value of N, and let it factor it into its two prime numbers (call them **p** and **q**).
5. Once you have p and q, use a short Python script to work out the private key:
   - `phi = (p - 1) * (q - 1)`
   - `d = inverse of e, mod phi` (Python's built-in `pow(e, -1, phi)` does this for you)
   - `m = pow(c, d, n)` — this decrypts the message
   - Convert the resulting number back into readable text
6. Running the script prints the flag.
