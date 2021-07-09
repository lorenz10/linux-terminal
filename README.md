# Everything (I know) about Linux Terminal

## 1. Commands

#### *File system*

-> **cd**

`cd /path/to/directory` opens a given directory. 

`cd` alone leads to the current user' home directory.

`cd ..` leads to the parent directory.
For example `cd ../../data` bring us two levels back in the tree and opens the directory named "data".

`cd -` leads to the previous working directory.

When tiping a directory name, if we press the `Tab` button the terminal will automatically complete its name, given that a direcotry starting with such characters exists and there is only one candidate.

-> **cp**

`cp /origin/directory/file /destination/directory`
copies the file into another directory.

`cp -r /origin/directory1 /destination/directory2` copies direcory1 and all its content into directory2.

`cp -r /origin/directory1 .` copies direcory1 and all its content into current directory.

-> **ls**

`ls /path/to/directory`
shows the content of the specidic directory, if no forlder is specified show the current one. Use `-a` to show also hidden files.

-> **mkdir**

`mkdir new_directory`
creates a new directory.

-> **mv**

`mv /origin/directory/file /destination/directory` moves the file into another directory.

-> **pwd**

gets the current directory path.

-> **rm**

`rm /path/to/file1`
removes file1.

`rm -r /path/to/directory` removes directory and all its content (-r is used to consider recursively the content).

-> **tree**

shows the contents of the working directory recursively showing sub-directories and files. Use `-a` to show also hidden files.

#### *Files*

```shell
cat
```

`cat file_name`
shows the content of the file.

`cat > new_file_name`
creates a new file. Then the cursor will be on a new line giving the possibility to write inside the new file. Once terminated typing can press `Ctrl + c` to finish editing.

```shell
echo
```

`echo 'Text to be placed in the file' > new_file.txt`
creates a new file containing the provided text.

-> **mv**

`mv old_file_name new_file_name` changes the name of a file. Works with directories too.

```shell
tail
```

`tail -n 100 new_file`
shows the last 100 lines of a file, shows the last 10 if -n option is not specified.

```shell
touch
```

`touch new_file_name`
creates a new empty file.

```shell
wget
```

`wget -O new_file_name.zip https://github.com/path/to/archive/master.zip`
downloads a file from the web, renaming it.

#### *Other*

```shell
clear
```
clear the view from previous commands.

```shell
date
```
shows the current timestamp. If followed by `+%s` it is shown in unix format.

```shell
kill PID1 PID2 PID3 # PID = Process ID
```
kills the processes with a given PID. Can kill as many PIDs as you want.

```shell
ping IP_address
```
ping the specific IP.

```shell
ps -ef
```
shows all running processes with detailed info.

```shell
su #super user
```
switches the current user into the super user.

```shell
su user_name
```
switches back the super user into the specified user.

-------------

## 2. Packages

#### netstat
display network-related information such as open connections and socket ports. 
* `apt-get install net-tools`
* `netstat -ant` or `netstat -pant`

#### Simple HTTP server (Python)
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
