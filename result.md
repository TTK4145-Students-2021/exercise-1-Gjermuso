First in go, I ran the program spawning the functions as goroutines three times, and got these results:  
The magic number is: -347180.  
The magic number is: 158854.  
The magic number is: -807214.  

Then I ran the program not using goroutines and got:  
The magic number is: 0  

In C, I ran the executable three times also, and got these results:  
The magic number is: -83504  
The magic number is: 148673  
The magic number is: -155355  

My explanation for these results is the conccurrency causing write-write conflicts. The functions run at the same time, sharing memory and using the same memory space at once. This causes, let's say the incrementing function to get the value for i in memory, counting up once and store it. But at the same time the decrementing function gets the same value for i and decreases it, to then save the value. The sum of this will then be that i = i-1. This happens up to 1e6 times and therefore gives us a random value between -1e6 and 1e6.
