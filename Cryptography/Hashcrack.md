# Hashcrack

## Step by Step Solution
1. Connect to the challenge server using netcat: `nc server-address port`
2. The server shows you a **hash** — a scrambled, one-way fingerprint of a password (you can't reverse it with math, but you can guess-and-check common passwords against it).
3. Copy the hash it gives you.
4. Go to a free online hash-cracking site like **crackstation.net**, paste the hash in, and let it search its huge database of common passwords for a match.
5. If it finds a match, it gives you the original password in plain text. Copy that password.
6. Go back to your terminal (where you're still connected to the server) and type in that password.
7. The server will confirm it's correct and then give you a **new** hash (a different type this time, so check the length of the hash to guess which type — 32 characters is usually MD5, 40 is usually SHA-1, 64 is usually SHA-256).
8. Repeat the same steps — paste each new hash into CrackStation, get the password, type it back into the server.
9. After cracking all the hashes it gives you, the server reveals the flag.
