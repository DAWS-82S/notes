ssh -i <path-to-your-private-key> ec2-user@IP

absolute path and relative path

/c/devops/daws-82s/daws-82s.pem --> absolute path
daws-82s/daws-82s.pem --> relative path

clear

$ --> denotes normal user
sudo su --> root access
\# --> denotes admin/root user

/home/<user-name>

/root --> root user home folder
sudo su - --> lands into root user home folder /root

<command-name> <options> <inputs>

- --> we can give single char
-- --> we need to give word

/ --> root of the server

ls --> list subdirectories

ls -l --> long listing format with more details
ls -lr --> reverse alpha order
ls -lt --> new files on top
ls -ltr --> old files on top
ls -ltrh --> human readable
ls -la --> display all files including hidden files and folders

drwx------ --> d means directory
-rw-r--r-- --> - means file
lrw-r--r-- --> Link files

touch <file-name> --> creates empty file

cat > devops.txt
cat > DevSecOps.txt --> enter the text, once done Enter and press ctrl+d
>> --> append, adds to the current text

mkdir <name> --> creates directory
rmdir <name> --> removes only empty directory

cp <source-file> <destination>
cd .. --> one step back

rm -r devops --> recursively delete everything inside devops

curl and wget

wget <URL> -->  Downloads the file
curl <URL> --> Shows the content on the screen
curl <URL> -o <path> --> donwloads the file with name given

https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md

/ --> seperator/delimiter/fragments
Sivakumar Reddy M

piping

grep <word-to-search> <file>

| --> pipe

cat <file-name> | grep <word-to-search>

cut command
=============
echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | cut -d "/" -f9
session-02.md

awk command
=============
echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | awk -F "/" '{print $NF}'

echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | awk -F "/" '{print $1F}'

How can I get all the users in Linux Servers

awk -F ":" '{print $1F}' passwd

head passwd --> top 10 lines from top
tail -n 4 passwd --> last 4 lines from bottom

head -n 10 passwd  | tail -n 7

4-10

head 10, tail (10-4)+1

find <which-location> -name "<file-name>"

find / -name "passwd"

vim editor