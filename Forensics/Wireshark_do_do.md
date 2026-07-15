# Wireshark do dooo


## Step-by-Step Solution
We have been given a pcap file which we open using wireshark.We pick the first tcp packet and use the 'follow tcp stream' to see the data being transferred.We go through each stream but don't find anything useful until stream 5 which something similar to the format of the challenge but seemed to be base64 encoded.Decoding the string gave us the string.
