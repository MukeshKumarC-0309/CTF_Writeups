# Corrupted File




## Step-by-Step Solution

So we first receive a file that seems to not open because of some issues.Hence we use the 'file' command to gather more information about it but it just returns 'data' which means the header is broken and the system is not able to recognize the file.Hence we open a hex editor to fix the header.We see that it closesly resemles a JPEG image.Hence we fix the headers and save the new file which gives us the flag.    
