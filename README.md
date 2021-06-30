# Everything (I know) about Linux Terminal

## 1. Commands

#### 1.a File system

```shell
cd /path/to/directory
```
opens a given directory. 

`cd` alone leads to the current user' home directory.

`cd ..` leads to the parent directory.
For example `cd ../../data` bring us two levels back in the tree and opens the directory named "data".

`cd -` leads to the previous working directory.

When tiping a directory name, if we press the `Tab` button the terminal will automatically complete its name, given that a direcotry starting with such characters exists and there is only one candidate.

```shell
cp /origin/directory/file /destination/directory
```
copies the file into another directory.

```shell
ls /path/to/directory
```
shows the content of the specidic directory, if no forlder is specified show the current one.

```shell
mkdir new_directory
```
creates a new directory.

```shell
move /origin/directory/file /destination/directory
```
moves the file into another directory.

```shell
pwd
```
gets the current directory path.

```shell
rm /path/to/file1
rm -r /path/to/directory # -r is needed to remove recursively all the content of the directory
```
removes a file or a directory (with all its content).

#### 1.b Files

```shell
cat > new_file_name
```
creates a new file. Then the cursor will be on a new line giving the possibility to write inside the new file. Once terminated typing can press `Ctrl + D` to finish editing.

```shell
echo 'Text to be placed in the file' > new_file.txt
```
creates a new file containing the provided text.

```shell
move old_file_name new_file_name
```
changes the name of a file.

```shell
tail -n 100 new_file
```
shows the last 100 lines of a file, shows the last 10 if -n option is not specified.

```shell
touch new_file
```
creates a new empty file.

#### 1.c Other

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
python -m SimpleHTTPServer [PORT]
```
creates a simple server in the current directory, listening on the specified, optional port.

```shell
su #super user
```
switches the current user into the super user.

```shell
su user_name
```
switches back the super user into the specified user.

#### _IMPORTANT: to show the options available for a specific command, type it followed by -h or --help_

-------------

## 2. Packages

#### netstat
display network-related information such as open connections and socket ports. 
* `apt-get install net-tools`
* `netstat -ant` or `netstat -pant`

#### vim
a highly configurable text editor built to make creating and changing any kind of text very efficient.
* `vi file_name` to open a specific file.
* press `i` to switch into "insert mode" and be able to edit the file, then `esc` when finished editing.
* `:wq` to enter in command mode, write changes and quit the file.

-------------

## 3. Philosophy

#### Copy and paste / cut and paste
It is possible to use them inside the terminal, but you need to press `ctrl` + `shift` + `c` or `v`.

#### ~ 
This symbol represents the path of the home directory of the current user.