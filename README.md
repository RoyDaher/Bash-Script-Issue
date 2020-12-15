# Bash-Script-Issue
Issue in adduser debian bash scripting



I am asked to add some users with all their info (password , id ,group id ...) present in a given file. Whenever I run my bash "gedit" script , it gives me a message that the "useradd command not found". If anyone could help me please , this is my code :

 FILE="user"
   USERNAME=$(cut -d " " -f 1 $FILE)
   PASSWORD=$(cut -d " " -f 2 $FILE)
   USER_ID=$(cut -d " " -f 3 $FILE)
   GROUP_ID=$(cut -d " " -f 4 $FILE)
   USER_INFO=$(cut -d " " -f 5 $FILE)
   HOME_DIRECTORY=$(cut -d " " -f 6 $FILE)
   SHELL=$(cut -d " " -f 7 $FILE)
   MIN=$(cut -d " " -f 8 $FILE)
   MAX=$(cut -d " " -f 9 $FILE)
   INACTIVE=$(cut -d " " -f 10 $FILE)
   WARNING=$(cut -d " " -f 11 $FILE)
   
   useradd -m -c "${USERNAME}" "${PASSWORD}" "${USER_ID}" "${GROUP_ID}" "${USER_INFO}" "${HOME_DIRECTORY}" "${SHELL}" "${MIN}" "${MAX}" "${INACTIVE}" "${WARNING}"
   
   
This is the content of the input file "user" :
charbel:password:1001:1001:Charbel Haddad:/home/charbel:/bin/bash:0:30:15:7:y
assil:p@ssw0rd:1002:1002:Assil:/home/assel:/bin/bash:0:30:10:5:n
marwan:p@ssw0rd:1003:1003:Marwan Ghantous:/home/marwan:/bin/bash:0:50:30:7:n 
michel:password:1004:1004:Michel:/home/michel:/bin/bash:1:30:10:5:y
