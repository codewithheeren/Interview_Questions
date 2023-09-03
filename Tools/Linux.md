Q. What are some commands of Linux ?
mkdir 
Pwd 
ls/ll
touch
rm
cp/scp
cat
sudo su 
chmod
Ping

create

1.create file
touch filename - will create an empty file
cat > filename
hello
ctrl+z (to save file with data)

2.create directory
mkdir foldername1 foldername2

3.Read file and also in running mode
cat filename
less filename  use q to exit and shift + F to start file executable mode.
tail -f dgHDFSAgent.log   (open file in running mode)
VI Editor commands:
open- vi hello.txt
Insert- i
quit- :q!
:wq! - Save the file and quit
search-   /searchtext


4.read dir
ls,ll,cd dirname/ tab 2 times

5.remove file and directory
rm filenmae
rm -r dirname
rm -r f1 f2 f3

6.change file/dir name
mv file1 file2
mv dirname1 dirname2

move one dir/file to another dir
mv folderfilename /todir

7.copy commands
copy a file 
cp filename newfilename   (file will be copy to newly created file newfilename)
sudo cp filename /dir  (will copy file in to a dir) (in case permission dinied use sudo)

scp filename.txt dataguise@192.168.0.119:/home/dataguise
scp filename.txt dataguise@192.168.0.119:~  copy to the home dir

8.search command:-
ls -ltr Ing*
find hell*
find . search filename*

to uncompress logs file -
gzip -d file.gz
unzip source_code.zip


to make empty a file.
> filename
Sudo su
The sudo command lets us use our account and password to execute system commands with root privileges

 • Directory Commands
 1. pwd
 2. cd
 3. cd ..
 4. ls
 5. mkdir name1 name2
 6. rmdir name1

 • File commands
 1. cat > intro.txt
        My name is Heerendra.
        Ctrl+D
 2. cat intro.txt (to see the content of file)
 3. rm intro.txt
 4. cp existing_file_name new _file_name
 5. mv file_name directory_path

 • File content commands
 1. head file_name
 2. tail file_name
 3. tac file_name
 4. more file_name