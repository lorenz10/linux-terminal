# Everything (I know) about Linux Terminal

## Commands

`cd /path/to/directory`
opens a given directory. If no path is specified will lead to the current user' home directory.
When tiping a directory name, if we press the `Tab` button the terminal will automatically complete its name, given that a direcotry starting with such characters exists and there is only one candidate.

```shell
cp /origin/directory/file /destination/directory
```
copies the file into another directory.

```shell
kill PID #Process ID
```
kills the process with a given PID.

```shell
mkdir new_directory
```
creates a new directory.

```shell
move /origin/directory/file /destination/directory
move old_file_name new_file_name #TRICK changes the name of a file
```
moves the file into another directory.

```shell
ps -ef
```
shows all running processes with detailed info.

```shell
pwd
```
gets the current directory path.

```shell
rm /path/to/file
rm -r /path/to/directory
```
removes a file, the second instead removes a directory with all its content (usually super user will be required).

```shell
su #super user
su <user>
```
switches the current user into the super user, the second switches back the SU into the specified user.

```shell
touch new_file
```
creates a new empty file.

-------------
## Useful packages

* netstat: display network-related information such as open connections and socket ports. 
`apt-get install net-tools`
`netstat -ant`
`netstat -pant`

-------------
## Philosophy

#### Copy and paste / cut and paste
It is possible to use them inside the terminal, but you need to press `ctrl` + `shift` + `c` or `v`.