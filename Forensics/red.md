# Red


## Step-by-Step Solution
The file we got was a plain png with nothing but the colour red.Hence we use the file command to gather any hidden details but there's wasn't any.Even exiftool yielded no returns.Then we used a tool called zsteg which is a tool used for LSB steganograhy or hidding things within colours.It seperates the colours and its data.Here we get a base64 encoded string which when decoded gave us the final flag.
