# processes and jobs

 ## listing processes
 ###  'ps' is used to list all ongoing processes
 ### -ef and -aux args are used to get all processes
 ### diff
    - -ef gives parent pid
    - -aux gives cpu and ram %s
 1.`ps -aux`
 2. `/challenge/32345-run-17551`
 
 ## killing processes
 ### 'kill' cmd allows to kill processes using pid as arg 
 1. `ps -ef | grep dont_run`
 2. `kill 74`
 3. `/challenge/run`

 ## interrupting processes
 ### ctrl + c is used to interrupt processes
 1. `/challenge/run`
 2. press ctrl + c

 ## suspending processes
 ### ctrl + z is used to suspend command
 1. `/challenge/run`
 2. press ctrl + z
 3. `/challenge/run`

 ## resuming processes 
 ### we use 'fg' cmd to resume suspended processes
 1. `/challenge/run`
 2. press ctrl + z
 3. `fg`

 ## backgrounding processes
 ### in order to resume suspended processes in background we use 'bg'
 ### -o arg in ps allows to view stat
 ### some exmaple are:
    T: suspended   
    S: sleeping while waiting for input
    R: running
    +: in foreground

 1. `/challenge/run`
 2. ctrl +z
 3. `bg`
 4. `/challenge/run`

 ## foregrounding processes
 ### we can also use 'fg' to foreground a background processes
 1. `/challenge/run`
 2. ctrl +z
 3. `bg`
 4. `fg`

 ## starting backgrounded processes
 ### by appending '&' to  the cmd we can directly start a cmd in bckgrnd
 1. `/challenge/run &`

 ## process exit code
 ### '?' var stores exit code and '$' allows to read it 
 1. `/challenge/get-code`
 2. `echo $?`
 3. `/challenge/submit-code 108`
  