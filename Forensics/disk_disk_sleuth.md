# Disk Disk Sleuth


## Step-by-Step Solution
We make use of the sleuth kit here which provides commands related to disk images.One such file was .gz file which we had decompress to get the raw disk image.Then we used the srch_strings command to search the disk image and used a pipeline to connect it to 'grep' command which also filters out strings based on the argument given and hence in the end we get the final flag.
