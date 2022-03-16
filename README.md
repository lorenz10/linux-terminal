# About Linux Terminal

```man any_command``` 
shows the manual of a given command.

## File system :open_file_folder:

#### basename

extracts the filename from a complete path.

#### cd

`cd /path/to/directory` opens a given directory. 

`cd` alone leads to the home directory of the current user.

`cd ..` leads to the parent directory. For example `cd ../../data` bring us two levels back in the tree and opens the directory named "data".

`cd -` leads to the previous working directory.

When tiping a directory name, if we press the `Tab` button the terminal will automatically complete its name.

#### cp

`cp /origin/directory/file /destination/directory` copies the file into another directory.

Use `-r` option to copy a directory with all its content.

#### du

`du -sh any_directory` returns the size of a directory in human-readable format.

#### ls

`ls /path/to/directory` shows the content of the specidic directory, if no forlder is specified show the current one. 

Use `-a` option to show also hidden files.

Use `-l` option to show the permissions of each file or directory.

Use `-R` option to show recursively all sub-dirctories and files.

#### mkdir

`mkdir new_directory` creates a new directory.

#### mv

`mv /origin/directory/file /destination/directory` moves the file into another directory.

#### pwd

gets the path to the current directory.

#### rm

`rm /path/to/file1` removes file1.

Use `-r` option to remove a directory and all its content.

#### tree

shows the contents of the working directory recursively showing sub-directories and files. 

Use `-a` option to show also all hidden files.

## Files :bookmark_tabs:

#### cat

`cat file_name` shows the content of a file.

`cat > new_file_name` creates a new file. The cursor will be prompted on a new line giving the possibility to write inside it. Once terminated typing can press `Ctrl` + `c` to terminate.

#### echo

`echo "New text" > new_file.txt` creates a new file containing the provided text.

`echo -e 'New text' >> /path/to/existing_file.txt` adds a new line of text at the end of an existing file.

#### grep

`grep any_word any_file` searches for a string on a given file and return the line with the resulting match.

Use `-i` option to ignore case sensitivity.

Use `-o` option to print only the matching part of the line and not the whole line.

#### mv

`mv old_file_name new_file_name` changes the name of a file or directory.

#### sed

`sed -i 's/apple/pie/g' file_name` replaces all occurrencies of the word "apple" with the word "pie" inside a file.

#### tail

`tail -n 100 new_file` shows the last 100 lines of a file, shows the last 10 if -n option is not specified.

#### touch

`touch new_file_name` creates a new empty file.

#### unzip

`unzip file.zip` extracts the content of a zip file.

#### wc

`wc -l` counts the number of lines printed on standart output.

## Internet :satellite:

#### ifconfig

if used alone shows all network interfaces.

#### netstat

`netstat -ant` or `netstat -pant` display network information such as open connections and socket ports.

#### ping

`ping <IP>` ping the specific IP. Press `ctrl` + `c` to stop and show the resume of the attempts so far.

#### scp

`scp -P 2222 file_name username@ip_address:/path/to/destination` uploads a file through SSH into the destination folder through port 2222. Use `-r` to upload a directory. 

#### wget

`wget -O new_file_name.zip https://github.com/path/to/archive/master.zip` downloads a file from the web, renaming it.

## Users :bust_in_silhouette:

#### passwd

changes the password of the current user.

#### su

switches the current user into the super user.

#### whoami

returns the name of the current user.

## Processes

#### kill

`kill <PID>` kills the processes with a given PID (process ID). Can specify as many PIDs as you want.

#### pidof

`pidof <process_name>` returns the PID (process ID) given the name of the process.

#### ps

`ps -ef` shows all running processes with detailed info.

## Others

#### clear

clears the view from previous commands.

#### date

shows the current timestamp. If followed by `+%s` it is shown in unix format.

#### lsblk

shows all disks and partitions of the machine.

#### watch

`watch -n 100 any_command` executes every 100 seconds any specified command.

#### top

shows an auto-updated table with all running processes.

-------------

## 2. Packages



#### simpleHTTPserver (Python)
creates a simple HTTP server on your machine.

1. create a new directory
2. inside it create a new `index.html` file with the following content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <h3>Python SimpleHTTPServer</h3>
    <p style="margin-left: 30px; color: rebeccapurple">Python 3 Web Server</p> 
</body>
</html>
```

3. move into the directory and type: `python -m SimpleHTTPServer [PORT]`, optionally specifing the port where to start listening.

#### vim
a highly configurable text editor built to make creating and changing any kind of text very efficient.
* `vi file_name` to open a specific file.
* press `i` to switch into "insert mode" and be able to edit the file, then `esc` when finished editing.
* `:wq` to enter in command mode, write changes and quit the file.

-------------

## 3. Philosophy

#### Copy and paste / cut and paste
It is possible to use them inside the terminal, but you need to press `ctrl` + `shift` + `c` or `v`.

#### ~ symbol
This symbol represents the path of the home directory of the current user.

#### Commands concatenation
`command1 ; command2` executes the first and then the second command. \
`command1 && command2` executes the first command. Executes the second if the first ends successfully. \
`command1 || command2` executes the first command. Executes the second if the first fails.

#### Typing commands
Press `ctrl` + `w` to delete the last word typed. \
Press `ctrl` + `u` to clear everything you just typed in.

#### Processes
Press `ctrl` + `c` to interrupt an executing process. 
