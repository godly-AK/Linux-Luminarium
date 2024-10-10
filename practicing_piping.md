# **practicing piping**

 ## redirecting output
 ### using '>' to redirecet output'echo PWN' to file 'COLLEGE'
 1. `echo PWN > COLLEGE`

 ## redirecting more output
 ### using '>' to redirect ouput of /challeng/run command to /myflag
 ### then reading myflag file
 1. `/challenge/run > myflag`
 2. `cat myflag`

 ## appending output
 ### we need to append the second half of the flag the fil the-flag as it contians first half of flag
 ### if not appended the we will only see second half as it overwrites the first galf of flag
 1. `/challenge/run >> ~/the-flag`
 2. `cat the-flag`

 ## redirecting errors
 ### we need to redirect stdout to 'myflag' and stderr to 'instructions' using '>' and '2>' respectively
 ### then we need to open myflag using cat 
 1. `/challenge/run > myflag 2> instructions`
 2. ` cat instructions `
 3. `cat myflag`

 ## redirecting input
 ### we need to give the value 'COLLEGE' to PWN
 ### we will use echo and redirect output to PWN
 ### then we will redirect input 'COLLEGE' to /challenge/run
 1. `echo COLLEGE > PWN`
 2. `/challenge/run < PWN`

 ## grepping stored results
 ### first we need to redirect output of /challenge/run to /tmp/data.txt
 ### then we need to use 'grep' cmd with argument 'pwn.college'(as every flag has this ) and path /tmp/data.txt
 1. `/challenge/run > /tmp/data.txt`
 2. `grep pwn.college /tmp/data.txt`

 ## grepping live outputs
 ### we need to use '|' operator to skip the process of storing the ouptput
 ### we can directly grep the output without storing it 
 1. `/challenge/run | grep pwn.college`

 ## grepping errors
 ### first we need to redirect the stderr of /challenge/run to stdout using '>&'
 ### then pipe it with grep 
 1.`/challenge/run 2>&1 | grep pwn.college`

 ## duplicating piped data with tee
 ### piping /challenge/pwn to /challenge/college will not give us the flag as we are missig something
 ### so will use 'tee" to check output pwn program and store it in a file called 'info'
 ### upon reading the file we can see we need to use a secret argument with /challenge/pwn and then pipe it to /challenge/college to get the flag
 1. `/challenge/pwn | tee info | /challenge/college`
 2. `cat info`
 3. `/challenge/pwn --secret 03eyZPX8 | /challenge/college`

 ## writing to multiple programs
 ### pipe operator can give input to one command or file only
 ### we need to use tee to send output from cmd /challenge/hack to cmds /challenge/the and /challenge/planet as input
 ### tee can only send input to files only thus we will use named pipe >(/challenge/the) and >(/challenge/planet) which will act as files and give input to respective cmds
 1. `/challenge/hack | tee  >(/challenge/the) >(/challenge/planet)`

 ## split-piping stderr and stdout
 ### we cannot use | tee as it won't separate stderr and stdout
 ### we must use normal rediection that we learned in the beggining in this module
 1.`/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)`
