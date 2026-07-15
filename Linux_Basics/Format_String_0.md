# 5.Format String 0

Can you use your knowledge of format strings to make the customers happy?
Download the binary here.
Download the source here.
Additional details will be available after launching your challenge instance.

## Solve
This involves the use of binary exploitation,hence i look through the source code and find the buffers which can be exploitated using various tricks.In the first part,it asks us to choose between 3 items,i chose the grilled cheese one because it has '%114d' which when used gives us a number of 114 characters which exceeds the buffer breaking it.In the next step,i choose the Cla%sic_Che%s%steak becuse mentioning '%s' without giving the string causes an error thereby breaking the buffer which gives us the final flag value.        

## Flag
picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_dc0f36c4}
