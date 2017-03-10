# UNIX

## commands
`. .bash_profile` execute .bash_profile  
`vi /etc/hosts` edit hosts (eg: 10.158.4.103 Firesniffer01)  
`grep` command : `-i` parameter is for ignore case sensetive  
`&` : put it at the end of a command, we don't have to wait until the command finish processing  
`wait` : wait until the command finish processing  
`;` : write two commands in one line  
`chmod 755 myscript` or `chmod a+x myscript` give myscript execute permission for all users  
`bash -n myscript` : use `-n` for not execute, for syntax check   
`bash -v myscript` : use `-v` for verbose, it echos every line command  
`bash -x myscript` : use `-x` echos every line being executed  
`#` is the comment sign in bash  

## Schedule Cron Jobs
`crontab -e` edit crontab  
RHEL/CentOS 5.x/6.x user:
```
service crond status --see the status of cron service  
service crond start 
service crond stop
```
You need to put `. ~/.bash_profile` inside crontab if you wanna use user environment, bacasue cron doesn't load user environment automatically.  
