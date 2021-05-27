# Everything (I know) about Linux Terminal

## Commands

```shell
cd /path/to/directory
```
changes current directory, if no path is specified will bring to the current user' home directory.

```shell
cp /origin/directory/file /destination/directory
```
copies the file into another directory.

```shell
kill <PID>
```
kills the process with that specific PID.

```shell
mkdir new_directory
```
creates a new directory.

```shell
move /origin/directory/file /destination/directory
move old_file_name new_file_name
```
moves the file into another directory, changes the name of a file.

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
removes a file, removes a directory with all its content (usually super user is required).

```shell
su
su <user>
```
changes the current user to be the super user, changes back the super user into the specified user.

```shell
touch new_file
```
creates a new file without any content.

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