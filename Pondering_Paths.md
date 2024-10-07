# Pondering Paths
   ## The Root
   1. `/pwn`
   ### we were supposed to type the path to run 'pwn' using root directory '/'
   
   ## program and absoulte path
   1. `/challenge/run`
   ### type absolute path of program run  

   ## position thy self
   1. `/challenge/run`
   ### got hint that in order to run the program i need to be in /etc/apt/sources.list.d directory
   2 `cd /etc/apt/sources.list.d`
   3.`/challenge/run'

   ## position elsewhere
   1. `/challenge/run`
   ### got hint that in order to run the program i need to be in  /proc/84 directory
   2. ` cd /proc/84 `
   3. `/challenge/run'
    
   ## position yet elsewhere
   1. `/challenge/run`
   ### got hint that in order to run the program i need to be in  /var directory
   2.`cd /var`
   3. `/challenge/run`

   ## implicit relative paths, from /
   1.`cd /`
   ### since we need to use relative paths we need to be in / and then run challenge/run
   2.`challenge/run`

   ## explicit relative paths, from /
   1.`cd /`
   ## this time we first need to change cwd to / then write relative path starting with .
   2. `./challenge/run`

   ## implicit relative path
   ### we need to be in /challenge
   1.`cd /chalenge`
   ### we need to run the "run" program using relative path
   2. `./run`

   ## home sweet home
   ### we are supposed to write an argument with /challenge/run
   ### should be under constraints as per question
   ### the argument should be an absolute path in home with less than 3 characters
   1.`/challenge/run ~/n
