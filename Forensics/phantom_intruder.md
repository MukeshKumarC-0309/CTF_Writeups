# Phantom Intruder


## Step-by-Step Solution
We have been given a pcap file which captures network traffic.We use a tool called wireshark to inspect it.So when we open the pcap file,we try to find the syn handshake which initiates a TCP conversation.We see that there's a part of base64 encoded string in it.Then we filter the packets on the basis of time and we get more packers with bits of encoded string.We decode each bit and place them together to find the final flag.
