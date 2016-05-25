# Recycle-Bin-Bash-Script
A bash script which simulates a recycle bin. CSC 460 - Operating Systems homework 2


Write a BASH script called junk that simulates use of a recycle bin and satisfies the following specifications.  Its synopsis is:  


    junk	[ -l | -p ]	[ fileName1	fileName2	... ]  


This means there are four options to execute the script from a command line:  

1) Enter	

    junk  

It displays a message including the synopsis of this “command” to show the user what the command does and how to use it correctly.  

2) Enter	

    junk	-l	[ fileName1	fileName2	... ]  

It displays the current contents of the directory ~/RecycleBin, recursively, if it exists; otherwise, it displays a message “Directory RecycleBin does not exist.”. (Note, the optional arguments following the option “-l” have no effect to the execution in this case.)  

3) Enter	

    junk	-p	[ fileName1	fileName2	... ] 
    
It deletes all the contents of the directory ~/RecycleBin if it exists; otherwise, it displays a message “Directory RecycleBin does not exist.”. (Again, the optional arguments following the option “-p” have no effect to the execution in this case.)   

4) Enter	
    
    junk	fileName1	fileName2	...  

  Case I. If ~/RecycleBin exists and it is a directory, the script checks each file in the file name list: if a file exists, the script moves it (with all its contents if it is a directory) from its current place to the RecycleBin; if a file does not exist, the script displays an appropriate error message with the file name.  

  Case II. If ~/RecycleBin does not exist, the script creates the directory first, then moves the files as described in Case I.  

  Case III. If ~/RecycleBin exists but it is not a directory, the script displays an appropriate error message.  
