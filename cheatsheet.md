# Cheatsheet

## Webapps

* Check for headers when accesing website

### Strings manipulation :
* base64 encoded ?
  ```
  # echo $STRING | base64 --decode
  # openssl enc -base64 -d <<< $STRING
  ```
  
### Scan all files in a website root folder : 
  `# dirb http://$WEBSITE$ (-p $PROXY)`
  
  
  
 Try a dictionnary on a password :
  Set Burp as INTRUDER, and set the ¨POST request and then the payload as a list of words
  
  
 Brute force a wp-login
  * Create the dictionnary
  `# wpscan -u $SITE --proxy $PROXY --username=*USERNAME --wordlist=$DICTIONNARY`
  
  
  Fidn a directory where the current user has write access : 
  `# find / -writable -type d 2>/dev/null`
  
  
  In a program, always chec that the commands are mentionned from the base name : /bin/bash/CAT and not simply cat.
  Otherwise, write a file containig only "/bin/sh" and add it in first to the PATH : 
   export PATH=FILE:$OLD_PATH
   
   `# strings $FILE` will display printable string of a file (useful when executables)

