# The Numbers

## Step by Step Solution
1. Read the challenge — you're given a sequence of numbers instead of letters.
2. The encoding is the simplest possible substitution: A=1, B=2, C=3, ... Z=26.
3. Convert each number back to its corresponding letter. You can do this by hand for a short sequence, or automate it:
   ```python
   nums = [16, 9, 3, 15, ...]  # replace with the actual numbers given
   flag = ''.join(chr(n + 64) for n in nums)
   print(flag)
   ```
4. `chr(n + 64)` works because ASCII 'A' is 65, so number 1 → chr(65) → 'A'.
5. Assemble the decoded letters into the flag format given.

## Concept
Simple substitution cipher — the most basic form of encoding, one symbol per letter with a fixed 1:1 mapping.
