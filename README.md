# batch-remove-tool
#### Bash script to make removing a large amount of files easier, but also safer from potential catastrophes. 
--
Have yet to master the command line?    

Scared of using ```rm``` to remove more than one file at a time?  

Feel like ```rm -i``` is overkill?  

**This tool may be for you!**

--
The goal here is to make a tool that is both easy and safe to use for file removal jobs.  

The user first enters the name of a directory, followed by a file name.  
This uses the ```find -iname```  

The user is then presented with a list of the files matching that directory and file name.  
Below the list is a set of options:

1. Select files to keep:  
  * Uses the ```grep -v```
  * Returns a list with the matching files removed from the list of files to be deleted
2. Remove only files:
  * Asks user for confirmation
  * Uses the ```sudo rm```
3. Remove files and directories:
  * Asks user for confirmation
  * Uses the ```sudo rm -r```
4. Change search parameters:
  * Prompts user to enter directory and file name
  * Uses the ```find -iname```
5. Cancel:
  * Ends the script
  
