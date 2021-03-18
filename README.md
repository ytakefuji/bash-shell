# problems
1. Show your bash script on how many files and how many directories in the current directory respectively.

Hint: ls command

2. Delete blank lines in text
Hint: sed -i '/^$/d'

3. Show your script on how many commas in the first line of new_deaths.csv:

https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/jhu/new_deaths.csv

Hints: 
A. head -1
B. tr -cd ,
C. wc -c
or
A. awk -F ',' '{print NF-1}'

4. Show only mounted column from result of df:
<pre>
$ df
Filesystem     1K-blocks      Used Available Use% Mounted on
rootfs         233465860 105665500 127800360  46% /
none           233465860 105665500 127800360  46% /dev
none           233465860 105665500 127800360  46% /run
none           233465860 105665500 127800360  46% /run/lock
none           233465860 105665500 127800360  46% /run/shm
none           233465860 105665500 127800360  46% /run/user
tmpfs          233465860 105665500 127800360  46% /sys/fs/cgroup
C:\            233465860 105665500 127800360  46% /mnt/c
Hints: 
A. reduce multiple spaces to a single space per line using "tr -s ' '"
B. cut -d ' ' -f 6

5. Convert minus numbers to positive numbers in csv file.
https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/jhu/new_deaths.csv

6. Explain "history|grep wget"

7. Explain $  ls -d \.[a-z]|grep /

</pre>

# shell
<pre>
Operating systems including Windows, Mac, and Linux have a default shell.
WSL (Windows Subsystem for Linux) and Linux (Ubuntu, Debian,...) have 
a default bash shell.
Mac has a default zsh. zsh is similar to bash.

In order to run shell, open terminal on your operating system.
Whenever starting shell, terminal window will be opened with 
the following prompt:
</pre>
<img src='wsl.png' width=260 height=66>
<img src='cygwin.png' width=180 height=80>
<pre>
We can run any line commands (bash, apt, Python, Firefox,...).
The followings are basic bash commands:

cd: to change directory
ls: to list files or directories (folders)
pwd: to print working directory
touch: to create a file
vi: screen editor 
ps: to provide information about the currently running processes 
mkdir: to make directory
cat: to read and concatenate files and give their content as output
sed: stream editor
  sed -n '3,4p' <bs
tr -s : to transform string or delete characters from the string
  echo "my     is  432234" | tr -s ' '
  my is 432234
  echo "my username is 432234" | tr -cd ' a-z'
  my username is 
head -x: reads first x lines of the file
  head -1 new_deaths.csv
awk: a scripting language used for manipulating data and generating reports
  head -1 new_deaths.csv |awk -F ',' '{print NF-1}'
cut: a command for cutting out the sections from each line of files and writing the result to standard output
  cut -d ' ' -f 6

echo: to display line of text/string that are passed as an argument
crontab -e: an editor creating cron jobs
export DISPLAY=:0: to export a display to remote client
df -h: to display information related to file systems about total space and available space
uniq: to report or filter out repeated lines in a file
ssh:
ifconfig:
iwconfig:
wget:
sudo apt install:
apt cache search:
openssl:
tar xvf xxx.tar:
tar cvf xxx.tar dir:
unzip:
make:
top:
gcc:
cmake
hcitool scan:
scp:
bc:
pkill –f xxx:
kill -9:
sshfs:
expect:
ntp:
sort:
nmap:
while:
rm:
wc:
grep -rn:
dpkg -l:
xargs: to read items from standard input as separated by blanks and execute a command once for each argument
find:
nslookup:
</pre>
