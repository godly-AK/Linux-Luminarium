# shell variables
 
 ## printing variables
 ### '$' is used to access data stored in variables
 ### we will use '$' to print stored flag in FLAG variable
 1. `echo $FLAG`

 ## setting variables 
 ### '=' is used to assign value to variable, ex: 'a=b'(no space after and before '=')
 1. `PWN=COLLEGE`

 ## multi word variable
 ### we use "" to assign multi word value to a variable
 1. `PWN="COLLEGE YEAH"`

 ## exporting variable
 ### **'sh' cmd creates child(simpler ver) shell inside a existing shell**
 ### export cmd allows to export var to environment variables of all child shells
 1. `export PWN=COLLEGE`
 2. `COLLEGE=PWN`
 3. `/challenge/run`

 ## printing exported variables
 ### 'env' cmd allows to see every exported var in the shell
 ### find flag 
 1. `env`

 ## storing command output
 ### using '$()' to access output of cmd and assign it to var
 1. `PWN=$(/challenge/run)`
 2. `echo $PWN`

 ## reading input
 ### we will use 'read' cmd to take input use '-p' arg to add a prompt(text to input)
 ### we need to give PWN var the value COLLEGE by input
 1.`read -p "PWN=" PWN`
 2. input 'COLLEGE' 
 
 ## reading files
 ### we can redirect content of file to a var as input,it most efficient and better
 1. `read PWN < /challenge/read_me`