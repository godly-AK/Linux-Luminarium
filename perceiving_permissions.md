# perceiving permissions

 ## changing file permissions
 ### 'chown' cmd is used to change ownership of a file while being root user
 1. `chown hacker /flag`
 2. `cat /flag`

 ## groups and files
 ### groups have many users
 ### users can be in many groups
 ### 'ls -l' with file as arg tells about files perms
 ### 'chgrp' allows to change group ownership of a file
 ### 'id' cmd tells which grp we belong to
 1. `chgrp hacker /flag`
 2. `cat /flag`

 ## fun with group names
 ### every user has their own group as per linux convention
 1. `id`
 2. `chgrp grp27217 /flag`
 3. `cat /flag`

 ## changing permissions
 ### 'chmod' alllows to change perms of a file 
 1. `chmod o+r /flag`
 2. `cat /flag`

 ## executable files
 ### we need to make '/challenge/run' executable by others
 1.`chmod a+x /challenge/run`
 2. `/challenge/run`

 ## permission tweaking pratice
  1 `/challenge/run`
  2 `chmod ug+x /challenge/pwn`
  3 `chmod go+w /challenge/pwn`
  4 `chmod ug-rw /challenge/pwn`
  5 `chmod uo-rx /challenge/pwn`
  6 `chmod o+r /challenge/pwn`
  7 `chmod o-w /challenge/pwn`
  8 `chmod g-x /challenge/pwn`
  9 `chmod ug+rw /challenge/pwn`
 10 `chmod a+r /flag`
 11 `cat /flag`
 
 ## permission setting pratice
 ### we can use '=' to directly assign the perms bit and ',' to do for users/grp/others in one arg
 ### this challenge is similiar to previous one

 ## the suid bit 
 ### the s bit denotes that the program will be executed as owner irrespective of user
 1. `chmod u+s /challenge/getroot`
 2. `cat /flag`
