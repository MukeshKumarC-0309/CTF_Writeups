# Very Very Very Hidden
## Step by Step Solution
i opened wireshark and then i analysed the pcap file.i filtered out only the http and https requests and when going through them i found 2 files which i downloaded.Among the 2 the evil-cat.png was similar to the other file but was much bigger in size hence there's a chance it could be steganography related.Hence i download powershell-stego-decode and use the required tool to extract the script hidden in the png file.It had a script which upon running delivered a file flag.txt which when opened gave us the flag.    
