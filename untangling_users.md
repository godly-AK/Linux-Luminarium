# untangling users

 ## becoming root with su
 ### using ' su' we will access the root shell 
 1. `su`
 2. `hack-the-planet`
 3. `cat flag`

 ## other users with su
 ### using username as arg with su we can root shell of ther users
 1. `su zardus`
 2. `dont-hack-me`
 3. `/challenge/run`

 ## cracking passwords
 ### all passwords are stored in **'/etc/shadow'**
  1. `john /challenge/shadow-leak`
  2. `su zardus`
  3. `aardvark`
  4. `/challenge/run`

 ## using sudo
 ### sudo allows to run commands as root user
 1. `sudo cat flag`