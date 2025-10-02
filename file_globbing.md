# **file globbing**

 ## matching with *
 ### we need to change directory to /challenge using cd cmd but argument should be four char
 ### we will use *
 ### then we will run /challenge/run to get the flag
 1. `cd /ch*`
 2. `/challenge/run`

 ## matching with ?
 ### we need to use ? which is a single char wildcard  to change directory to /challenge
 ### we need replace c and l with ? in argument /challenge of cd and after that run the /run program in /challenge to get the flag
 1. `cd /?ha??enge`
 2. `./run`

## matching with []
### we need to use change directory to /challenge/files
### we need to use 'file_[bash]' as we need the bracket glob files_b, files_a, files_s,files_h
### we need to run the above argument with /challenge/run program
1. `cd /challenge/files`
2. `/challenge/run files_[bash]`

## matching paths with []
### we need to do like the previous ques but without changing cwd
### we will need to add the path '/challenge/files' to the argument 'file_[bash]'
1. `/challenge/run /challenge/files/file_[bash]`

## mixing globs
### we need glob files 'challenging','educational'and 'pwning' using less than 6 char
### in /challenge/files first char of every file is unique
1. `cd /challenge/files`
2. `/challenge/run [cep]*`

## exclusionary globbing
### we need to exclude files starting with 'p','w'and 'n' in /challenge/files using [^] argument
1. `cd /challenge/files`
2. `/challenge/run [^pwn]*`
## multiple globs
- basically what we need is every file name havin letter p
- whihc mean the name of the file shoudl have p any where in the name
- so prefix before letter p could be denoted by * and suffix after letter p could be denoted by *
- so the correct arg is \*p\*

