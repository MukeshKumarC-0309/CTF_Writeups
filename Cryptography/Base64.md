# Base64

## Step by Step Solution
1. Read the challenge — you're given a hex-encoded string and asked to convert it to Base64.
2. First decode the hex string into raw bytes:
   ```python
   import base64
   hex_string = "YOUR_HEX_STRING"
   raw_bytes = bytes.fromhex(hex_string)
   ```
3. Then encode those raw bytes into Base64:
   ```python
   b64 = base64.b64encode(raw_bytes)
   print(b64.decode())
   ```
4. Submit the resulting Base64 string as the flag (it will already be in `crypto{...}` form once decoded correctly, since the underlying bytes spell out the flag).

## Concept
Base64 encoding — represents binary data using a 64-character alphabet (A-Z, a-z, 0-9, +, /), commonly used to safely transmit binary data as text (e.g. in URLs, JSON, email). Different from hex: hex is 2 chars/byte, Base64 is roughly 4 chars per 3 bytes, making it more compact.
