# Everything (I know) about Linux Terminal

## Commands

#### IMPORTANT -> to show all the options available for a specific command write it follwed by -h or --help <-

```shell
cd /path/to/directory
```
opens a given directory. 

`cd` alone leads to the current user' home directory.

`cd ..` alone leads to the previouse level of directories.
For example `cd ../../data` bring us two levels back in the tree and opens the directory named "data".

When tiping a directory name, if we press the `Tab` button the terminal will automatically complete its name, given that a direcotry starting with such characters exists and there is only one candidate.

```shell
cat > new_file_name
```
creates a new file. Then the cursor will be on a new line giving the possibility to write inside the new file. Once terminated typing can press `Ctrl + D` to finish editing.

```shell
clear
```
clear the terminal UI from previous commands.

```shell
cp /origin/directory/file /destination/directory
```
copies the file into another directory.

```shell
kill PID1 PID2 PID3 # PID = Process ID
```
kills the processes with a given PID. Can kill as many PIDs as you want.

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
move old_file_name new_file_name
```
changes the name of a file.

```shell
ping IP_address
```
ping the specific IP.

```shell
ps -ef
```
shows all running processes with detailed info.

```shell
pwd
```
gets the current directory path.

```shell
rm /path/to/file1
rm -r /path/to/directory # -r is needed to remove recursively all the content of the directory
```
removes a file or a directory (with all its content).

```shell
su #super user
```
switches the current user into the super user.

```shell
su user_name
```
switches back the super user into the specified user.

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