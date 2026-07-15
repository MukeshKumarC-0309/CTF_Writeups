# rsa-pop-quiz

## Step by Step Solution
1. Read the challenge — it gives you a `nc` (netcat) connection string to reach an interactive quiz server.
2. Connect to it:
   ```bash
   nc HOST PORT
   ```
3. The server will ask a series of RSA-related conceptual questions, one at a time, waiting for your text answer before showing the next one. Typical questions and answers include:
   - "What do we call the numbers `p` and `q`?" → **primes** (the two large prime numbers multiplied to form `n`)
   - "What is `n` called?" → **modulus**
   - "What is `e` called?" → **public exponent**
   - "What is `d` called?" → **private exponent**
   - "What is `(p-1)(q-1)` called?" → **totient** (Euler's totient of `n`, often written `φ(n)`)
   - "What must `e` and `φ(n)` satisfy?" → they must be **coprime** (gcd(e, φ(n)) = 1)
   - "What operation is used to encrypt?" → **modular exponentiation**
4. Answer each question exactly as prompted — the server usually expects a single lowercase word or short phrase, so match its expected format precisely (check for trailing punctuation or capitalization hints in the prompt).
5. After answering all questions correctly, the server prints the flag directly in the terminal.

## Concept
This challenge isn't a cryptographic attack — it's testing whether you actually understand RSA's building blocks (primes, modulus, totient, exponents) rather than just knowing how to run an attack script. Useful as a self-check before tackling the harder RSA challenges in this list.
