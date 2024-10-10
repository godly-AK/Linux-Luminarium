# comprehending commands

## cat : not the pet,but the command !
### we are supposed to read file flag using cat command
1.`cat flag`

## catting absolute paths
### we were supposed to use cat with absolute pah of flag in order to read the flag
1.`cat /flag`

## more catting pratice
### we were supposed to read flag with absolute path /opt/kropr/src/flag using cat command
1. `cat /opt/kropr/src/flag`

## grepping for a needle in a haystack
### we were supposed to search flag in /challenge/data.txt using grep cmd
### flag starts with pwn.college
1.`grep pwn.college /challenge/data.txt`

## listing files
### we are supposed to find the renamed run file in /challenge by viewing all the files in /challenge using ls cmd
1. ` ls /challenge`

## touching files
### we are supposed to create file two files pwn and college in /tmp using touch and then run /challenge/run
1. `cd /tmp`
2. `touch pwn`
3. `touch college`
4. `/challenge/run`

## removing files
### we need to create delete_me file using touch, delete it using rm cmd and then run /challenge/check
1. `touch delete_me`
2. `rm delete_me`
3. `/challenge/check`

## hidden files
### we need to find the flag file in / ,  which is starting with '.' thus a hidden file
### thus we need to use ls -a to view hidden files
### then we will use cat cmd to read the file 
1. `cd /`
2. `ls -a`
3. `cat  .flag-215601236318974`

## an epic filesystem quest
### we need to use cat , ls and cd comd repeatedly to find chain of clues leading to flag
 1.` ls /`
 2. `cat /REVELATION`
 3. `cd /opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/clk`
 4. `ls`
 5. `cat ALERT`
 6. `cd /opt/linux/linux-5.4/drivers/android`
 7. `ls`
 8. `cat DOSSIER`
 9. `ls  /usr/lib/python3/dist-packages/sympy/stats/tests`
10. `cat /usr/lib/python3/dist-packages/sympy/stats/tests/HINT-TRAPPED`
11. `cd  /opt/linux/linux-5.4/include/config/oid`
12. `ls -a`
13. `cat .TIP`
14. `cd  /opt/ghidra/Extensions/IDAPro`
15. `ls -a`
16. `cat .CLUE`
17. `ls  /opt/linux/linux-5.4/drivers/staging/unisys/visornic`
18. `cat  /opt/linux/linux-5.4/drivers/staging/unisys/visornic/INFO-TRAPPED`
19.`cd /opt/ghidra/Ghidra/Features/GhidraServer/data/yajsw-stable-13.09/lib/core/yajsw`
20. `ls`
21. `cat SNIPPET`
22. `cd /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Italic
23. `ls`
24. `cat CUE`
## making directories
### we need to create 'pwn' directory in /tmp using mkdir cmd and then create college file in /tmp/pwn using touch cmd
### then run /challenge/run to get flag
1. `cd /tmp`
2. `mkdir pwn`
3. `cd pwn`
4. `touch college`
5. `/challenge/run`

## finding files
### we need to the 'flag' file in the whole filesystem using find cmd
1. `find / -name flag`
2. `cat /usr/share/doc/libec5/flag`

## linking files 
 ### we are supposed to fool the link into giving us the flag
 ### /challenge/catflag should open /flag
 ### we have cannot edit /flag and /challenge/catflag
 ### thus we will remove the not-the-flag file as it is symlink to /challenge/catflag
 ### then link /flag with /not-the-flag and the run /challenge/catflag leading to opening /flag file
 ### *asked mentor for hint*
 1.`rm not-the-flag`
 2. `ln -s ~/flag ~/not-the-flag`
 3. `/challenge/catflag`
