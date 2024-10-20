# pondering PATH
 
 ## the PATH variable
 ### the PATH variable stores bunch of directories of cmds
 ### by emptying path var , rm cmd will not work
 1. `PATH=''`
 2. `/challenge/run`

 ## setting PATH
 ###  we can add a path to PATH var to be able to use our own cmd just by its name 
 1. `PATH='/challenge/more_commands'`
 2. `/challenge/run`

 ## adding commands
 ### we will read the flag using variable as read is a part of bash
 1. `echo 'read X < /flag' > win`
 2. `echo 'echo $X' >> win
 3. `chmod a+x win`
 4. `PATH=/home/hacker`
 5. `/challenge/run`

 ## hijacking commands
 ###  similiar to prev one , we will trick by creating rm of our own which will read the file
 1. `echo 'read X < /flag' > rm`
 2. `echo 'echo $X' >> rm`
 3. `chmod a+x rm`
 4. `PATH=/home/hacker`
 5. `/challenge/run`