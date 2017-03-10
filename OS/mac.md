# Mac

## Terminal
### Terminal Commands
`ps -acx` : display all of the programs and processes being run by all of the users, this command returns:
* PID : process identification number 
* TTY : the terminal the process is running in. If you see two question marks (??), that means the process isn’t associated with a specific Terminal window or display: typically it’s a system-level command or utility
* TIME : Tells you the amount of time it took to run that particular process, or how long that process has been running, in minutes and seconds.
* CMD : the specific command that’s being run. 

`grep` : a Unix search tool that you use to search for words or, as numbers in files, or in this case, the output of a command:  
Kill Word Process
```
$ ps -ax | grep Word
 1634 ??         0:02.50 /Applications/Microsoft Office 2011/Microsoft
                 Word.app/Contents/MacOS/Microsoft Word -psn_0_766139
 1645 ttys002    0:00.00 grep Word
$ kill 1634
```

#### Batch Renames and Extracting File Lists
Suppose you just received a thumb drive from a client with hundreds of files in a single folder. Now let’s say that you only need those files that have the sequence `-nt-` or `-dt-` as part of their filenames, and that you want to copy them from the thumb drive to your home directory.
```
$ cd /Volumes/Thumb
$ cp *-dt-* *-nt-* ~
```

`ls -aF` you can figure out the items are files or directories with `-F` 

#### FTP 
For example, if you wanted to download the cover image for this book from O’Reilly’s website, you could use the following commands:  
```
$ ftp ftp.oreilly.com
Connected to ftp.oreilly.com.
220 ProFTPD 1.3.1rc3 Server (ftp.oreilly.com) [172.17.107.51]
Name (ftp.oreilly.com:taylor): anonymous
331 Anonymous login ok, send your complete email address as your password
Password:
230-Welcome to the O'Reilly Media, Inc. FTP Archive.

 Local date and time: Sat Oct 03 20;00:16 2015

 --> Hello 71.237.2.63 <--
 --> There are 2 users out of 100 allowed in your usage class. <--

 Check us out on the web at http://oreilly.com
230 Anonymous access granted, restrictions apply
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> cd /pub/graphics/book-covers/low-res
250 CWD command successful
ftp> get 9781449332310.gif
local: 0596009151.gif remote: 0596009151.gif
229 Entering Extended Passive Mode (|||62244|)
150 Opening BINARY mode data connection for 0596009151.gif (27259 bytes)
100% |*******************************************************|   261 KiB
     430.20 KiB/s    00:00 ETA
226 Transfer complete
267646 bytes received in 00:00 (389.56 KiB/s)
ftp> bye
221 Goodbye.
```

### Terminal Button Commands
jump to the begining of the line : `Ctrl + A`  
jump to the end of the line : `Ctrl + E`  


## System Button Commands
`Command-Option-Escape` : open Force Quit Applications window  

## File Structure
**.profile** : in your home directory you probably have a file called *.profile* that contains specific instructions on how you want your command shell set up when it’s launched.
