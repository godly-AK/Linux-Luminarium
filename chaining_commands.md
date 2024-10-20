# chaining commands
 
 ## chaining with semicolons
 ### ';' is used to chain multiple commands
 1. `/challenge/pwn ; /challenge/college`

 ## your first shell script
 ### '.sh' files can store multiple cmd lines which can be run together
 1. `echo '/challenge/pwn ; /challenge/college' > x.sh`
 2. `bash x.sh`

 ## redirecting script output
 ### all redirection methods works for .sh file
 1. `echo '/challenge/pwn ; /challenge/college' > x.sh`
 2. `bash x.sh | /challenge/solve`

 ## executable shell scripts
 ### we can remove use of bash cmd by making file executable
 ### thus we will change perms to a+x ( all users can execute it )
 1. `echo /challenge/solve > x.sh
 2. `chmod a+x x.sh`
 3. `./x.sh`
 
