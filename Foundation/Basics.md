Må raskt dokumentere og forklare kort de forskjellige komamndoene brukt her:

# Lecture 1

philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes test.pcap
philipef@networksecuritylab:~$ ls /
bin lib root sys
bin.usr-is-merged lib.usr-is-merged run tmp
boot lost+found sbin usr
cdrom media sbin.usr-is-merged var
dev mnt snap
etc opt srv
home proc swap.img
philipef@networksecuritylab:~$ ls /home
philipef
philipef@networksecuritylab:~$ #clear
philipef@networksecuritylab:~$ ls -l /
total 3998804
lrwxrwxrwx 1 root root 7 Apr 22 2024 bin -> usr/bin
drwxr-xr-x 2 root root 4096 Feb 26 2024 bin.usr-is-merged
drwxr-xr-x 5 root root 4096 Dec 20 17:13 boot
dr-xr-xr-x 2 root root 4096 Aug 6 15:52 cdrom
drwxr-xr-x 20 root root 4020 Dec 20 22:20 dev
drwxr-xr-x 115 root root 4096 Dec 20 22:14 etc
drwxr-xr-x 3 root root 4096 Dec 20 16:26 home
lrwxrwxrwx 1 root root 7 Apr 22 2024 lib -> usr/lib
drwxr-xr-x 2 root root 4096 Feb 26 2024 lib.usr-is-merged
drwx------ 2 root root 16384 Dec 20 16:14 lost+found
drwxr-xr-x 3 root root 4096 Dec 20 17:04 media
drwxr-xr-x 2 root root 4096 Aug 6 15:18 mnt
drwxr-xr-x 3 root root 4096 Dec 20 17:13 opt
dr-xr-xr-x 194 root root 0 Dec 20 22:20 proc
drwx------ 3 root root 4096 Dec 20 16:57 root
drwxr-xr-x 31 root root 960 Dec 22 16:13 run
lrwxrwxrwx 1 root root 8 Apr 22 2024 sbin -> usr/sbin
drwxr-xr-x 2 root root 4096 Jul 10 14:46 sbin.usr-is-merged
drwxr-xr-x 2 root root 4096 Dec 20 16:26 snap
drwxr-xr-x 2 root root 4096 Aug 6 15:18 srv
-rw------- 1 root root 4094689280 Dec 20 16:16 swap.img
dr-xr-xr-x 13 root root 0 Dec 20 22:20 sys
drwxrwxrwt 12 root root 4096 Dec 22 19:58 tmp
drwxr-xr-x 11 root root 4096 Aug 6 15:18 usr
drwxr-xr-x 13 root root 4096 Dec 20 16:25 var
philipef@networksecuritylab:~$ ll
total 100
drwxr-x--- 6 philipef philipef 4096 Dec 22 20:05 ./
drwxr-xr-x 3 root root 4096 Dec 20 16:26 ../
-rw------- 1 philipef philipef 17820 Dec 22 17:12 .bash_history
-rw-r--r-- 1 philipef philipef 220 Mar 31 2024 .bash_logout
-rw-r--r-- 1 philipef philipef 3771 Mar 31 2024 .bashrc
drwx------ 2 philipef philipef 4096 Dec 20 16:27 .cache/
-rw-r--r-- 1 philipef philipef 807 Mar 31 2024 .profile
drwx------ 2 philipef philipef 4096 Dec 20 17:43 .ssh/
-rw-r--r-- 1 philipef philipef 0 Dec 20 16:57 .sudo_as_admin_successful
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab/
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes/
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ ls -l /home
total 4
drwxr-x--- 6 philipef philipef 4096 Dec 22 20:05 philipef
philipef@networksecuritylab:~$ ls -l /home/philipef/
total 52
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ pwd
/home/philipef
philipef@networksecuritylab:~$ #cd
philipef@networksecuritylab:~$ #cd tilde
philipef@networksecuritylab:~$ #ls -l /etc
philipef@networksecuritylab:~$ # Blue-directory, White-file, Green-binary
philipef@networksecuritylab:~$ # permission string: drwr-xr-x
philipef@networksecuritylab:~$ # file: -rwxr-xr-x
philipef@networksecuritylab:~$ # link: lrwxrwxrwx
philipef@networksecuritylab:~$

# Lecture 2

philipef@networksecuritylab:~$ touch testfile.txt
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes test.pcap testfile.txt
philipef@networksecuritylab:~$ ls -l
total 52
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 0 Dec 22 20:34 testfile.txt
philipef@networksecuritylab:~$ touch testfile.txt
philipef@networksecuritylab:~$ ls -l
total 52
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 0 Dec 22 20:36 testfile.txt
philipef@networksecuritylab:~$

philipef@networksecuritylab:~$ nano
philipef@networksecuritylab:~$ ls -l
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 0 Dec 22 20:36 testfile.txt
philipef@networksecuritylab:~$ cat test2.txt
learninglinux.tv
philipef@networksecuritylab:~$

philipef@networksecuritylab:~$ nano
philipef@networksecuritylab:~$ ls -l
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 0 Dec 22 20:36 testfile.txt
philipef@networksecuritylab:~$ cat test2.txt
learninglinux.tv
philipef@networksecuritylab:~$ nano test3.txt
philipef@networksecuritylab:~$ ls -
ls: cannot access '-': No such file or directory
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
-rw-rw-r-- 1 philipef philipef 0 Dec 22 20:36 testfile.txt
philipef@networksecuritylab:~$ nano testfile.txt
philipef@networksecuritylab:~$
philipef@networksecuritylab:~$ ls -l
total 64
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
-rw-rw-r-- 1 philipef philipef 29 Dec 22 20:39 testfile.txt
philipef@networksecuritylab:~$ which nano
/usr/bin/nano

philipef@networksecuritylab:~$ which vim
/usr/bin/vim
philipef@networksecuritylab:~$ vim
philipef@networksecuritylab:~$ vim
philipef@networksecuritylab:~$ ls -l
total 68
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
-rw-rw-r-- 1 philipef philipef 26 Dec 22 20:43 test4.txt
-rw-rw-r-- 1 philipef philipef 29 Dec 22 20:39 testfile.txt
philipef@networksecuritylab:~$ cat test4.txt
Learingin Linux right now
philipef@networksecuritylab:~$ vim test4.txt
philipef@networksecuritylab:~$ cat test4.txt
Learingin Linux right now.

Use I to start INSERT-ing.

Use :W filename.txt to write and create a new file.

Use :w to write to an existing file.

Use :q to quit VIM.

Use dd to delete a line:

delete1
delete3

Can type shift + a to go into INSERT mode at the end of the file, to immediately start typing.

Can
philipef@networksecuritylab:~$

# Lecture 3

philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab test.pcap test3.txt testfile.txt
Linux_Lab_Notes test2.txt test4.txt
philipef@networksecuritylab:~$ cat test2.txt
learninglinux.tv
philipef@networksecuritylab:~$ ls -l
total 68
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
-rw-rw-r-- 1 philipef philipef 312 Dec 22 20:48 test4.txt
-rw-rw-r-- 1 philipef philipef 29 Dec 22 20:39 testfile.txt
philipef@networksecuritylab:~$ cp test2.txt newfile.txt
philipef@networksecuritylab:~$ ls -l
total 72
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 17 Dec 24 13:00 newfile.txt
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 17 Dec 22 20:37 test2.txt
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
-rw-rw-r-- 1 philipef philipef 312 Dec 22 20:48 test4.txt
-rw-rw-r-- 1 philipef philipef 29 Dec 22 20:39 testfile.txt
philipef@networksecuritylab:~$ cat newfile.txt
learninglinux.tv
philipef@networksecuritylab:~$ cat test2.txt
learninglinux.tv
philipef@networksecuritylab:~$ diff newfile.txt test2.txt
philipef@networksecuritylab:~$ rm newfile.txt
philipef@networksecuritylab:~$ rm test2.txt
philipef@networksecuritylab:~$ mkdir notes
philipef@networksecuritylab:~$ mv test3.txt notes
philipef@networksecuritylab:~$ ls -l notes
total 4
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test3.txt
philipef@networksecuritylab:~$ mv \*.txt notes
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes notes test.pcap
philipef@networksecuritylab:~$ ls /notes
ls: cannot access '/notes': No such file or directory
philipef@networksecuritylab:~$ ls notes
test3.txt test4.txt testfile.txt
philipef@networksecuritylab:~$ cd notes/
philipef@networksecuritylab:~/notes$ #move back
philipef@networksecuritylab:~/notes$ mv testfile.txt ..
philipef@networksecuritylab:~/notes$ ls
test3.txt test4.txt
philipef@networksecuritylab:~/notes$ cd ..
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab notes testfile.txt
Linux_Lab_Notes test.pcap
philipef@networksecuritylab:~$ mv testfile.txt notes
philipef@networksecuritylab:~$ cd notes/
philipef@networksecuritylab:~/notes$ ls -l ..
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:04 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~/notes$ pwd
/home/philipef/notes
philipef@networksecuritylab:~/notes$ mv testfile.txt ..
philipef@networksecuritylab:~/notes$ mv ../testfile.txt notes
philipef@networksecuritylab:~/notes$ ls
notes test3.txt test4.txt
philipef@networksecuritylab:~/notes$ mv ../testfile.txt .
mv: cannot stat '../testfile.txt': No such file or directory
philipef@networksecuritylab:~/notes$ ls .
notes test3.txt test4.txt
philipef@networksecuritylab:~/notes$ cd ..
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes notes test.pcap
philipef@networksecuritylab:~$ #rename file
philipef@networksecuritylab:~$ cd notes/
philipef@networksecuritylab:~/notes$ mv test3.txt renamed_test3.txt
philipef@networksecuritylab:~/notes$ ls
notes renamed_test3.txt test4.txt
philipef@networksecuritylab:~/notes$ mv renamed_test3.txt test4.txt
philipef@networksecuritylab:~/notes$ ls
notes test4.txt
philipef@networksecuritylab:~/notes$ ls
notes test4.txt
philipef@networksecuritylab:~/notes$ cd ..
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes notes test.pcap
philipef@networksecuritylab:~$ cd notes/
philipef@networksecuritylab:~/notes$ ls
notes test4.txt
philipef@networksecuritylab:~/notes$ cat notes

Linux is quite easy so far!
philipef@networksecuritylab:~/notes$ cat test4.txt
test
philipef@networksecuritylab:~/notes$

# Lecture 4

philipef@networksecuritylab:~/notes$ ls -l
total 8
-rw-rw-r-- 1 philipef philipef 29 Dec 22 20:39 notes
-rw-rw-r-- 1 philipef philipef 5 Dec 22 20:38 test4.txt
philipef@networksecuritylab:~/notes$ cd ..
philipef@networksecuritylab:~$ ls -l
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ alias ls
alias ls='ls --color=auto'
philipef@networksecuritylab:~$ nano myscript.sh
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab myscript.sh test.pcap
Linux_Lab_Notes notes
philipef@networksecuritylab:~$ ./myscript.sh
-bash: ./myscript.sh: Permission denied
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ #-rw-, altså ikke x for execute der
philipef@networksecuritylab:~$ chmod +x myscript.sh
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rwxrwxr-x 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ ./myscript.sh
Enterprise-Network-Lab myscript.sh test.pcap
Linux_Lab_Notes notes
philipef@networksecuritylab:~$ chmod -x myscript.sh
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ chmod u+x myscript.sh
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab myscript.sh test.pcap
Linux_Lab_Notes notes
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rwxrw-r-- 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ chmod a+rwx myscript.sh
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rwxrwxrwx 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ chmod g-rwx myscript.sh
philipef@networksecuritylab:~$ ls-l
ls-l: command not found
philipef@networksecuritylab:~$ ls -l myscript.sh
-rwx---rwx 1 philipef philipef 16 Dec 24 16:47 myscript.sh
philipef@networksecuritylab:~$ chmod o-rwx myscript.sh
philipef@networksecuritylab:~$ ls -l myscript.sh
-rwx------ 1 philipef philipef 16 Dec 24 16:47 myscript.sh
philipef@networksecuritylab:~$ mkdir testdir
philipef@networksecuritylab:~$ ls -l testdir/
total 0
philipef@networksecuritylab:~$ chmod -x testdir/
philipef@networksecuritylab:~$ cd testdir/
-bash: cd: testdir/: Permission denied
philipef@networksecuritylab:~$ ls -l testdir/
total 0
philipef@networksecuritylab:~$ ls -l
total 64
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rwx------ 1 philipef philipef 16 Dec 24 16:47 myscript.sh
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
drw-rw-r-- 2 philipef philipef 4096 Dec 24 17:01 testdir
philipef@networksecuritylab:~$ chmod u+x testdir/
philipef@networksecuritylab:~$ cd testdir/
philipef@networksecuritylab:~/testdir$ cd ..
philipef@networksecuritylab:~$ rm myscript.sh
philipef@networksecuritylab:~$ rm testdir/
rm: cannot remove 'testdir/': Is a directory
philipef@networksecuritylab:~$ rm -r testdir/
philipef@networksecuritylab:~$ ls -l
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$

# Lecture 5

philipef@networksecuritylab:~$ free
total used free shared buff/cache available
Mem: 3998692 427308 2754840 9228 984660 3571384
Swap: 3998716 0 3998716
philipef@networksecuritylab:~$ free -m
total used free shared buff/cache available
Mem: 3904 417 2690 9 961 3487
Swap: 3904 0 3904
philipef@networksecuritylab:~$ df
Filesystem 1K-blocks Used Available Use% Mounted on
tmpfs 399872 1308 398564 1% /run
efivarfs 56 3 54 5% /sys/firmware/efi/efivars
/dev/mapper/ubuntu--vg-ubuntu--lv 31270768 8202556 21454184 28% /
tmpfs 1999344 0 1999344 0% /dev/shm
tmpfs 5120 0 5120 0% /run/lock
/dev/vda2 1992552 103728 1767584 6% /boot
/dev/vda1 1098632 6516 1092116 1% /boot/efi
tmpfs 399868 16 399852 1% /run/user/1000
philipef@networksecuritylab:~$ df -h
Filesystem Size Used Avail Use% Mounted on
tmpfs 391M 1.3M 390M 1% /run
efivarfs 56K 2.6K 54K 5% /sys/firmware/efi/efivars
/dev/mapper/ubuntu--vg-ubuntu--lv 30G 7.9G 21G 28% /
tmpfs 2.0G 0 2.0G 0% /dev/shm
tmpfs 5.0M 0 5.0M 0% /run/lock
/dev/vda2 2.0G 102M 1.7G 6% /boot
/dev/vda1 1.1G 6.4M 1.1G 1% /boot/efi
tmpfs 391M 16K 391M 1% /run/user/1000
philipef@networksecuritylab:~$ df -i
Filesystem Inodes IUsed IFree IUse% Mounted on
tmpfs 499836 885 498951 1% /run
efivarfs 0 0 0 - /sys/firmware/efi/efivars
/dev/mapper/ubuntu--vg-ubuntu--lv 1998848 130242 1868606 7% /
tmpfs 499836 1 499835 1% /dev/shm
tmpfs 499836 3 499833 1% /run/lock
/dev/vda2 131072 260 130812 1% /boot
/dev/vda1 0 0 0 - /boot/efi
tmpfs 99967 34 99933 1% /run/user/1000
philipef@networksecuritylab:~$ htop

philipef@networksecuritylab:~$ # for example: We can select CPU% and then select a process, then we can call SIGPIPE and many other system calls, which gives us a lot of options and control over the copmuter.
philipef@networksecuritylab:~$ uptime
21:17:56 up 18:49, 1 user, load average: 0.07, 0.02, 0.00
philipef@networksecuritylab:~$ # uptime: how long the system has been up and the load average
philipef@networksecuritylab:~$ # In htop, we can also see the number of cores and their loads, the memory used and othe statistics
philipef@networksecuritylab:~$ # If we had 8 cores and the load average for the first minute was 0.77, it would mean we would have 7.23 cores that are available for use
philipef@networksecuritylab:~$ # Load Average gives us three values [Last minute, Last 5 minutes, Last 15 minutes].
philipef@networksecuritylab:~$ # I wrote wrong, if the core is e.g. 4.5, then the core would be oversaturated to do 450% its total capacity
philipef@networksecuritylab:~$

# Lecture 6

philipef@networksecuritylab:~$ # sudo apt update
philipef@networksecuritylab:~$ # apt search firefox
philipef@networksecuritylab:~$ # sudo apt install vim-nox
philipef@networksecuritylab:~$ # sudo apt install apache2
philipef@networksecuritylab:~$ sudo apt remove apache2
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
apache2-bin apache2-data apache2-utils libapr1t64
libaprutil1-dbd-sqlite3 libaprutil1-ldap libaprutil1t64
liblua5.4-0 ssl-cert
Use 'sudo apt autoremove' to remove them.
The following packages will be REMOVED:
apache2
0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.
After this operation, 465 kB disk space will be freed.
Do you want to continue? [Y/n] y
(Reading database ... 110875 files and directories currently installed.)
Removing apache2 (2.4.58-1ubuntu8.8) ...
Processing triggers for man-db (2.12.0-4build2) ...
Processing triggers for ufw (0.36.2-6) ...
philipef@networksecuritylab:~$ sudo apt autoremove
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages will be REMOVED:
apache2-bin apache2-data apache2-utils libapr1t64
libaprutil1-dbd-sqlite3 libaprutil1-ldap libaprutil1t64
liblua5.4-0 ssl-cert
0 upgraded, 0 newly installed, 9 to remove and 0 not upgraded.
After this operation, 13.5 MB disk space will be freed.
Do you want to continue? [Y/n] y
(Reading database ... 110825 files and directories currently installed.)
Removing apache2-bin (2.4.58-1ubuntu8.8) ...
dpkg: warning: while removing apache2-bin, directory '/var/lib/apache2' not empty so not removed
Removing apache2-data (2.4.58-1ubuntu8.8) ...
Removing apache2-utils (2.4.58-1ubuntu8.8) ...
Removing libaprutil1-dbd-sqlite3:arm64 (1.6.3-1.1ubuntu7) ...
Removing libaprutil1-ldap:arm64 (1.6.3-1.1ubuntu7) ...
Removing libaprutil1t64:arm64 (1.6.3-1.1ubuntu7) ...
Removing libapr1t64:arm64 (1.7.2-3.1ubuntu0.1) ...
Removing liblua5.4-0:arm64 (5.4.6-3build2) ...
Removing ssl-cert (1.1.2ubuntu1) ...
Processing triggers for man-db (2.12.0-4build2) ...
Processing triggers for libc-bin (2.39-0ubuntu8.6) ...
philipef@networksecuritylab:~$ sudo apt update
Hit:1 https://download.docker.com/linux/ubuntu noble InRelease
Hit:2 http://ports.ubuntu.com/ubuntu-ports noble InRelease
Hit:3 http://ports.ubuntu.com/ubuntu-ports noble-updates InRelease
Hit:4 http://ports.ubuntu.com/ubuntu-ports noble-backports InRelease
Hit:5 http://ports.ubuntu.com/ubuntu-ports noble-security InRelease
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
All packages are up to date.
philipef@networksecuritylab:~$ sudo apt upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
Get more security updates through Ubuntu Pro with 'esm-apps' enabled:
libzvbi-common libcjson1 libavcodec60 libzvbi0t64 libavutil58 libswscale7
libswresample4 libavformat60
Learn more about Ubuntu Pro at https://ubuntu.com/pro
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
philipef@networksecuritylab:~$ # sudo apt dist-upgrade
philipef@networksecuritylab:~$

# Lecture 7

philipef@networksecuritylab:~$ systemctl status apache2
● apache2.service - The Apache HTTP Server
Loaded: loaded (/usr/lib/systemd/system/apache2.service; enable>
Active: active (running) since Wed 2025-12-24 21:42:10 UTC; 34s>
Docs: https://httpd.apache.org/docs/2.4/
Main PID: 12390 (apache2)
Tasks: 55 (limit: 4549)
Memory: 5.4M (peak: 6.1M)
CPU: 18ms
CGroup: /system.slice/apache2.service
├─12390 /usr/sbin/apache2 -k start
├─12393 /usr/sbin/apache2 -k start
└─12394 /usr/sbin/apache2 -k start

Dec 24 21:42:10 networksecuritylab systemd[1]: Starting apache2.serv>
Dec 24 21:42:10 networksecuritylab apachectl[12389]: AH00558: apache>
Dec 24 21:42:10 networksecuritylab systemd[1]: Started apache2.servi>

philipef@networksecuritylab:~$ sudo systemctl disable apache2
Synchronizing state of apache2.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install disable apache2
Removed "/etc/systemd/system/multi-user.target.wants/apache2.service".
philipef@networksecuritylab:~$ systemctl status apache2
● apache2.service - The Apache HTTP Server
Loaded: loaded (/usr/lib/systemd/system/apache2.service; disabl>
Active: active (running) since Wed 2025-12-24 21:42:10 UTC; 2mi>
Docs: https://httpd.apache.org/docs/2.4/
Main PID: 12390 (apache2)
Tasks: 55 (limit: 4549)
Memory: 5.4M (peak: 6.1M)
CPU: 35ms
CGroup: /system.slice/apache2.service
├─12390 /usr/sbin/apache2 -k start
├─12393 /usr/sbin/apache2 -k start
└─12394 /usr/sbin/apache2 -k start

Dec 24 21:42:10 networksecuritylab systemd[1]: Starting apache2.serv>
Dec 24 21:42:10 networksecuritylab apachectl[12389]: AH00558: apache>
Dec 24 21:42:10 networksecuritylab systemd[1]: Started apache2.servi>
...skipping...
● apache2.service - The Apache HTTP Server
Loaded: loaded (/usr/lib/systemd/system/apache2.service; disabl>
Active: active (running) since Wed 2025-12-24 21:42:10 UTC; 2mi>
Docs: https://httpd.apache.org/docs/2.4/
Main PID: 12390 (apache2)
Tasks: 55 (limit: 4549)
Memory: 5.4M (peak: 6.1M)
CPU: 35ms
CGroup: /system.slice/apache2.service
├─12390 /usr/sbin/apache2 -k start
├─12393 /usr/sbin/apache2 -k start
└─12394 /usr/sbin/apache2 -k start

Dec 24 21:42:10 networksecuritylab systemd[1]: Starting apache2.serv>
Dec 24 21:42:10 networksecuritylab apachectl[12389]: AH00558: apache>
Dec 24 21:42:10 networksecuritylab systemd[1]: Started apache2.servi>

philipef@networksecuritylab:~$ sudo systemctl stop apache2
philipef@networksecuritylab:~$ systemctl status apache2
○ apache2.service - The Apache HTTP Server
Loaded: loaded (/usr/lib/systemd/system/apache2.service; disabl>
Active: inactive (dead)
Docs: https://httpd.apache.org/docs/2.4/

Dec 24 21:36:25 networksecuritylab apachectl[11376]: AH00558: apache>
Dec 24 21:36:25 networksecuritylab systemd[1]: apache2.service: Deac>
Dec 24 21:36:25 networksecuritylab systemd[1]: Stopped apache2.servi>
Dec 24 21:42:10 networksecuritylab systemd[1]: Starting apache2.serv>
Dec 24 21:42:10 networksecuritylab apachectl[12389]: AH00558: apache>
Dec 24 21:42:10 networksecuritylab systemd[1]: Started apache2.servi>
Dec 24 21:45:38 networksecuritylab systemd[1]: Stopping apache2.serv>
Dec 24 21:45:38 networksecuritylab apachectl[12750]: AH00558: apache>
Dec 24 21:45:38 networksecuritylab systemd[1]: apache2.service: Deac>
Dec 24 21:45:38 networksecuritylab systemd[1]: Stopped apache2.servi>

philipef@networksecuritylab:~$ sudo systemctl start apache2
philipef@networksecuritylab:~$ systemctl status apache2
● apache2.service - The Apache HTTP Server
Loaded: loaded (/usr/lib/systemd/system/apache2.service; disabl>
Active: active (running) since Wed 2025-12-24 21:45:58 UTC; 4s >
Docs: https://httpd.apache.org/docs/2.4/
Process: 12762 ExecStart=/usr/sbin/apachectl start (code=exited,>
Main PID: 12765 (apache2)
Tasks: 55 (limit: 4549)
Memory: 5.2M (peak: 5.7M)
CPU: 29ms
CGroup: /system.slice/apache2.service
├─12765 /usr/sbin/apache2 -k start
├─12767 /usr/sbin/apache2 -k start
└─12768 /usr/sbin/apache2 -k start

Dec 24 21:45:58 networksecuritylab systemd[1]: Starting apache2.serv>
Dec 24 21:45:58 networksecuritylab apachectl[12764]: AH00558: apache>
Dec 24 21:45:58 networksecuritylab systemd[1]: Started apache2.servi>

philipef@networksecuritylab:~$ sudo systemctl restart apache2
philipef@networksecuritylab:~$

# Lecture 8 Viewing Logs

philipef@networksecuritylab:~$ #cat /var/log/syslog
philipef@networksecuritylab:~$ cd /var/log
philipef@networksecuritylab:/var/log$ ls -l
total 3488
lrwxrwxrwx 1 root root 39 Aug 6 15:27 README -> ../../usr/share/doc/systemd/README.logs
-rw-r--r-- 1 root root 39351 Dec 24 21:31 alternatives.log
drwxr-x--- 2 root adm 4096 Dec 24 21:32 apache2
-rw-r----- 1 root adm 0 Dec 20 16:26 apport.log
drwxr-xr-x 2 root root 4096 Dec 24 21:42 apt
-rw-r----- 1 syslog adm 118857 Dec 24 22:05 auth.log
-rw-r--r-- 1 root root 61237 Aug 6 15:18 bootstrap.log
-rw-rw---- 1 root utmp 800 Dec 20 21:43 btmp
-rw-r----- 1 root adm 4363 Dec 20 16:26 cloud-init-output.log
-rw-r----- 1 syslog adm 71900 Dec 20 16:26 cloud-init.log
drwxr-xr-x 2 root root 4096 Jul 25 16:08 dist-upgrade
-rw-r----- 1 root adm 46465 Dec 20 22:20 dmesg
-rw-r----- 1 root adm 45854 Dec 20 16:49 dmesg.0
-rw-r----- 1 root adm 13360 Dec 20 16:30 dmesg.1.gz
-rw-r----- 1 root adm 13460 Dec 20 16:26 dmesg.2.gz
-rw-r--r-- 1 root root 859726 Dec 24 21:42 dpkg.log
-rw-r--r-- 1 root root 0 Aug 6 15:18 faillog
-rw-r--r-- 1 root root 813 Dec 24 21:31 fontconfig.log
drwxrwx--- 4 root adm 4096 Dec 20 16:23 installer
drwxr-sr-x+ 3 root systemd-journal 4096 Dec 20 16:25 journal
-rw-r----- 1 syslog adm 783864 Dec 22 16:36 kern.log
drwxr-xr-x 2 landscape landscape 4096 Aug 6 15:36 landscape
-rw-rw-r-- 1 root utmp 296296 Dec 24 12:58 lastlog
drwx------ 2 root root 4096 Aug 6 15:27 private
-rw-r----- 1 syslog adm 1397170 Dec 24 22:05 syslog
drwxr-xr-x 2 root root 4096 Dec 24 00:07 sysstat
-rw-r--r-- 1 root root 0 Dec 20 17:12 ubuntu-advantage-apt-hook.log
drwxr-x--- 2 root adm 4096 Dec 20 16:26 unattended-upgrades
-rw-rw-r-- 1 root utmp 22000 Dec 24 12:58 wtmp
philipef@networksecuritylab:/var/log$ ls -l apache2
total 8
-rw-r----- 1 root adm 853 Dec 24 21:42 access.log
-rw-r----- 1 root adm 1532 Dec 24 21:46 error.log
-rw-r----- 1 root adm 0 Dec 24 21:32 other_vhosts_access.log
philipef@networksecuritylab:/var/log$ cat apache2/error.log
[Wed Dec 24 21:32:30.038305 2025] [mpm_event:notice] [pid 11007:tid 266148046585888] AH00489: Apache/2.4.58 (Ubuntu) configured -- resuming normal operations
[Wed Dec 24 21:32:30.038342 2025] [core:notice] [pid 11007:tid 266148046585888] AH00094: Command line: '/usr/sbin/apache2'
[Wed Dec 24 21:36:25.226398 2025] [mpm_event:notice] [pid 11007:tid 266148046585888] AH00492: caught SIGWINCH, shutting down gracefully
[Wed Dec 24 21:42:10.526719 2025] [mpm_event:notice] [pid 12390:tid 258017810243616] AH00489: Apache/2.4.58 (Ubuntu) configured -- resuming normal operations
[Wed Dec 24 21:42:10.526760 2025] [core:notice] [pid 12390:tid 258017810243616] AH00094: Command line: '/usr/sbin/apache2'
[Wed Dec 24 21:45:38.188020 2025] [mpm_event:notice] [pid 12390:tid 258017810243616] AH00492: caught SIGWINCH, shutting down gracefully
[Wed Dec 24 21:45:58.096618 2025] [mpm_event:notice] [pid 12765:tid 249734559014944] AH00489: Apache/2.4.58 (Ubuntu) configured -- resuming normal operations
[Wed Dec 24 21:45:58.096721 2025] [core:notice] [pid 12765:tid 249734559014944] AH00094: Command line: '/usr/sbin/apache2'
[Wed Dec 24 21:46:22.361934 2025] [mpm_event:notice] [pid 12765:tid 249734559014944] AH00492: caught SIGWINCH, shutting down gracefully
[Wed Dec 24 21:46:22.425449 2025] [mpm_event:notice] [pid 12856:tid 258428584034336] AH00489: Apache/2.4.58 (Ubuntu) configured -- resuming normal operations
[Wed Dec 24 21:46:22.425535 2025] [core:notice] [pid 12856:tid 258428584034336] AH00094: Command line: '/usr/sbin/apache2'
philipef@networksecuritylab:/var/log$ #If this was a server, we could check here to narrow down the problem.
philipef@networksecuritylab:/var/log$ cat dmesg
philipef@networksecuritylab:/$ dmesg
philipef@networksecuritylab:/$ head /var/log/syslog
2025-12-20T16:26:01.960830+00:00 networksecuritylab systemd-modules-load[328]: Inserted module 'dm_multipath'
2025-12-20T16:26:01.961127+00:00 networksecuritylab lvm[316]: 1 logical volume(s) in volume group "ubuntu-vg" monitored
2025-12-20T16:26:01.961130+00:00 networksecuritylab systemd[1]: Mounted sys-fs-fuse-connections.mount - FUSE Control File System.
2025-12-20T16:26:01.961132+00:00 networksecuritylab systemd[1]: Mounted sys-kernel-config.mount - Kernel Configuration File System.
2025-12-20T16:26:01.961134+00:00 networksecuritylab systemd[1]: Finished systemd-random-seed.service - Load/Save OS Random Seed.
2025-12-20T16:26:01.961135+00:00 networksecuritylab systemd[1]: Finished systemd-sysctl.service - Apply Kernel Variables.
2025-12-20T16:26:01.961136+00:00 networksecuritylab systemd[1]: Finished systemd-tmpfiles-setup-dev-early.service - Create Static Device Nodes in /dev gracefully.
2025-12-20T16:26:01.961138+00:00 networksecuritylab systemd[1]: Reached target swap.target - Swaps.
2025-12-20T16:26:01.961140+00:00 networksecuritylab multipathd[346]: multipathd v0.9.4: start up
2025-12-20T16:26:01.961141+00:00 networksecuritylab multipathd[346]: reconfigure: setting up paths and maps
philipef@networksecuritylab:/$ tail /var/log/syslog
2025-12-24T21:50:03.966282+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T21:50:03.966568+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2025-12-24T21:55:01.247261+00:00 networksecuritylab CRON[12926]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
2025-12-24T22:00:20.144761+00:00 networksecuritylab systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2025-12-24T22:00:20.153293+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T22:00:20.153453+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2025-12-24T22:05:01.311219+00:00 networksecuritylab CRON[12939]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
2025-12-24T22:10:10.454135+00:00 networksecuritylab systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2025-12-24T22:10:10.463171+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T22:10:10.463420+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
philipef@networksecuritylab:/$ tail -50 /var/log/syslog
philipef@networksecuritylab:/$ tail -f /var/log/syslog
2025-12-24T21:50:03.966282+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T21:50:03.966568+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2025-12-24T21:55:01.247261+00:00 networksecuritylab CRON[12926]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
2025-12-24T22:00:20.144761+00:00 networksecuritylab systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2025-12-24T22:00:20.153293+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T22:00:20.153453+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2025-12-24T22:05:01.311219+00:00 networksecuritylab CRON[12939]: (root) CMD (command -v debian-sa1 > /dev/null && debian-sa1 1 1)
2025-12-24T22:10:10.454135+00:00 networksecuritylab systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2025-12-24T22:10:10.463171+00:00 networksecuritylab systemd[1]: sysstat-collect.service: Deactivated successfully.
2025-12-24T22:10:10.463420+00:00 networksecuritylab systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
^C
philipef@networksecuritylab:/$ journalctl -u ssh
philipef@networksecuritylab:/$ cat /var/log/syslog -u apache2
philipef@networksecuritylab:/$ cat /var/log/syslog |grep apache2
philipef@networksecuritylab:/$ journalctl -fu apache2

# Lecture 9 Managing Users

philipef@networksecuritylab:/$ cat etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
\_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
systemd-timesync:x:997:997:systemd Time Synchronization:/:/usr/sbin/nologin
dhcpcd:x:100:65534:DHCP Client Daemon,,,:/usr/lib/dhcpcd:/bin/false
messagebus:x:101:102::/nonexistent:/usr/sbin/nologin
systemd-resolve:x:992:992:systemd Resolver:/:/usr/sbin/nologin
pollinate:x:102:1::/var/cache/pollinate:/bin/false
polkitd:x:991:991:User for polkitd:/:/usr/sbin/nologin
syslog:x:103:104::/nonexistent:/usr/sbin/nologin
uuidd:x:104:105::/run/uuidd:/usr/sbin/nologin
tcpdump:x:105:107::/nonexistent:/usr/sbin/nologin
landscape:x:106:108::/var/lib/landscape:/usr/sbin/nologin
fwupd-refresh:x:989:989:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
sshd:x:107:65534::/run/sshd:/usr/sbin/nologin
philipef:x:1000:1000:Philip Fleischer:/home/philipef:/bin/bash
philipef@networksecuritylab:/$ cat /etc/shadow
cat: /etc/shadow: Permission denied
philipef@networksecuritylab:/$ sudo cat /etc/shadow
[sudo] password for philipef:
root:_:20306:0:99999:7:::
daemon:_:20306:0:99999:7:::
bin:_:20306:0:99999:7:::
sys:_:20306:0:99999:7:::
sync:_:20306:0:99999:7:::
games:_:20306:0:99999:7:::
man:_:20306:0:99999:7:::
lp:_:20306:0:99999:7:::
mail:_:20306:0:99999:7:::
news:_:20306:0:99999:7:::
uucp:_:20306:0:99999:7:::
proxy:_:20306:0:99999:7:::
www-data:_:20306:0:99999:7:::
backup:_:20306:0:99999:7:::
list:_:20306:0:99999:7:::
irc:_:20306:0:99999:7:::
\_apt:_:20306:0:99999:7:::
nobody:_:20306:0:99999:7:::
systemd-network:!_:20306::::::
systemd-timesync:!_:20306::::::
dhcpcd:!:20306::::::
messagebus:!:20306::::::
systemd-resolve:!_:20306::::::
pollinate:!:20306::::::
polkitd:!_:20306::::::
syslog:!:20306::::::
uuidd:!:20306::::::
tcpdump:!:20306::::::
landscape:!:20306::::::
fwupd-refresh:!\*:20306::::::
sshd:!:20442::::::
philipef:$6$uLd/7kh3TcOk3BaU$THCCvLFyVN8o6KyVSCs6N4JHAeodm/vDLy6B/8WE7p/XcqQQDpmmBNn.1zW1Tlp2bcft2OnCxUiVhxnhVS6nw0:20442:0:99999:7:::
philipef@networksecuritylab:/$ cat /etc/group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:syslog,philipef
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
fax:x:21:
voice:x:22:
cdrom:x:24:philipef
floppy:x:25:
tape:x:26:
sudo:x:27:philipef
audio:x:29:
dip:x:30:philipef
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
shadow:x:42:
utmp:x:43:
video:x:44:
sasl:x:45:
plugdev:x:46:philipef
staff:x:50:
games:x:60:
users:x:100:
nogroup:x:65534:
systemd-journal:x:999:
systemd-network:x:998:
systemd-timesync:x:997:
input:x:996:
sgx:x:995:
kvm:x:994:
render:x:993:
lxd:x:101:philipef
messagebus:x:102:
systemd-resolve:x:992:
\_ssh:x:103:
polkitd:x:991:
crontab:x:990:
syslog:x:104:
uuidd:x:105:
rdma:x:106:
tcpdump:x:107:
landscape:x:108:
fwupd-refresh:x:989:
philipef:x:1000:
docker:x:988:philipef
wireshark:x:109:philipef
ssl-cert:x:110:
philipef@networksecuritylab:/$ cat etc/p
pam.conf passwd- plymouth/ pollinate/ protocols python3.12/
pam.d/ perl/ pm/ profile pulse/
passwd pki/ polkit-1/ profile.d/ python3/
philipef@networksecuritylab:/$ cat etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
\_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
systemd-timesync:x:997:997:systemd Time Synchronization:/:/usr/sbin/nologin
dhcpcd:x:100:65534:DHCP Client Daemon,,,:/usr/lib/dhcpcd:/bin/false
messagebus:x:101:102::/nonexistent:/usr/sbin/nologin
systemd-resolve:x:992:992:systemd Resolver:/:/usr/sbin/nologin
pollinate:x:102:1::/var/cache/pollinate:/bin/false
polkitd:x:991:991:User for polkitd:/:/usr/sbin/nologin
syslog:x:103:104::/nonexistent:/usr/sbin/nologin
uuidd:x:104:105::/run/uuidd:/usr/sbin/nologin
tcpdump:x:105:107::/nonexistent:/usr/sbin/nologin
landscape:x:106:108::/var/lib/landscape:/usr/sbin/nologin
fwupd-refresh:x:989:989:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
sshd:x:107:65534::/run/sshd:/usr/sbin/nologin
philipef:x:1000:1000:Philip Fleischer:/home/philipef:/bin/bash
philipef@networksecuritylab:/$ groups
philipef adm cdrom sudo dip plugdev lxd wireshark docker
philipef@networksecuritylab:/$ groups p
philipef polkitd pollinate proxy
philipef@networksecuritylab:/$ groups philipef
philipef : philipef adm cdrom sudo dip plugdev lxd docker wireshark
philipef@networksecuritylab:/$ adduser dragon
fatal: Only root may add a user or group to the system.
philipef@networksecuritylab:/$ sudo adduser dragontamer
info: Adding user `dragontamer' ...
info: Selecting UID/GID from range 1000 to 59999 ...
info: Adding new group `dragontamer' (1001) ...
info: Adding new user `dragontamer' (1001) with group `dragontamer (1001)' ...
info: Creating home directory `/home/dragontamer' ...
info: Copying files from `/etc/skel' ...
New password:
Retype new password:
passwd: password updated successfully
Changing the user information for dragontamer
Enter the new value, or press ENTER for the default
Full Name []:
Room Number []:
Work Phone []:
Home Phone []:
Other []:
Is the information correct? [Y/n] y
info: Adding new user `dragontamer' to supplemental / extra groups `users' ...
info: Adding user `dragontamer' to group `users' ...
philipef@networksecuritylab:/$ cat etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
\_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
systemd-timesync:x:997:997:systemd Time Synchronization:/:/usr/sbin/nologin
dhcpcd:x:100:65534:DHCP Client Daemon,,,:/usr/lib/dhcpcd:/bin/false
messagebus:x:101:102::/nonexistent:/usr/sbin/nologin
systemd-resolve:x:992:992:systemd Resolver:/:/usr/sbin/nologin
pollinate:x:102:1::/var/cache/pollinate:/bin/false
polkitd:x:991:991:User for polkitd:/:/usr/sbin/nologin
syslog:x:103:104::/nonexistent:/usr/sbin/nologin
uuidd:x:104:105::/run/uuidd:/usr/sbin/nologin
tcpdump:x:105:107::/nonexistent:/usr/sbin/nologin
landscape:x:106:108::/var/lib/landscape:/usr/sbin/nologin
fwupd-refresh:x:989:989:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
sshd:x:107:65534::/run/sshd:/usr/sbin/nologin
philipef:x:1000:1000:Philip Fleischer:/home/philipef:/bin/bash
dragontamer:x:1001:1001:,,,:/home/dragontamer:/bin/bash
philipef@networksecuritylab:/$ groups
philipef adm cdrom sudo dip plugdev lxd wireshark docker
philipef@networksecuritylab:/$ su -dragontamer
su: invalid option -- 'd'
Try 'su --help' for more information.
philipef@networksecuritylab:/$ su - dragontamer
Password:
dragontamer@networksecuritylab:~$ passwd
Changing password for dragontamer.
Current password:
New password:
Retype new password:
passwd: password updated successfully
dragontamer@networksecuritylab:~$ sudo passwd
[sudo] password for dragontamer:
ThSorry, try again.
[sudo] password for dragontamer:
sudo: 1 incorrect password attempt
dragontamer@networksecuritylab:~$ sudo su - dragontamer
[sudo] password for dragontamer:
Sorry, try again.
[sudo] password for dragontamer:
dragontamer is not in the sudoers file.
dragontamer@networksecuritylab:~$
logout
philipef@networksecuritylab:/$ sudo userdel -r dragontamer
userdel: dragontamer mail spool (/var/mail/dragontamer) not found
philipef@networksecuritylab:/$ sudo groupadd reptiles
philipef@networksecuritylab:/$ groups
philipef adm cdrom sudo dip plugdev lxd wireshark docker
philipef@networksecuritylab:/$ sudo usermod -aG reptiles philipef
philipef@networksecuritylab:/$ groups
philipef adm cdrom sudo dip plugdev lxd wireshark docker
philipef@networksecuritylab:/$ groups philipef
philipef : philipef adm cdrom sudo dip plugdev lxd docker wireshark reptiles
philipef@networksecuritylab:/$ gpasswd -d philipef reptiles
gpasswd: Permission denied.
philipef@networksecuritylab:/$ sudo !!
sudo gpasswd -d philipef reptiles
Removing user philipef from group reptiles
philipef@networksecuritylab:/$ tail /etc/group
uuidd:x:105:
rdma:x:106:
tcpdump:x:107:
landscape:x:108:
fwupd-refresh:x:989:
philipef:x:1000:
docker:x:988:philipef
wireshark:x:109:philipef
ssl-cert:x:110:
reptiles:x:1001:
philipef@networksecuritylab:/$ sudo groupdel reptiles
philipef@networksecuritylab:/$ tail /etc/group
syslog:x:104:
uuidd:x:105:
rdma:x:106:
tcpdump:x:107:
landscape:x:108:
fwupd-refresh:x:989:
philipef:x:1000:
docker:x:988:philipef
wireshark:x:109:philipef
ssl-cert:x:110:
philipef@networksecuritylab:/$

# Lecture 10 Bash History

philipef@networksecuritylab:/$ history
1 quit
2 exit
.
.
.
623 groups
624 groups philipef
625 gpasswd -d philipef reptiles
626 sudo gpasswd -d philipef reptiles
627 tail /etc/group
628 sudo groupdel reptiles
629 tail /etc/group
630 celar
631 clear
632 history
philipef@networksecuritylab:/$ !624
groups philipef
philipef : philipef adm cdrom sudo dip plugdev lxd docker wireshark
philipef@networksecuritylab:/$ groups philipef
philipef : philipef adm cdrom sudo dip plugdev lxd docker wireshark
philipef@networksecuritylab:/$ cat etc/passwd
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
\_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
systemd-timesync:x:997:997:systemd Time Synchronization:/:/usr/sbin/nologin
dhcpcd:x:100:65534:DHCP Client Daemon,,,:/usr/lib/dhcpcd:/bin/false
messagebus:x:101:102::/nonexistent:/usr/sbin/nologin
systemd-resolve:x:992:992:systemd Resolver:/:/usr/sbin/nologin
pollinate:x:102:1::/var/cache/pollinate:/bin/false
polkitd:x:991:991:User for polkitd:/:/usr/sbin/nologin
syslog:x:103:104::/nonexistent:/usr/sbin/nologin
uuidd:x:104:105::/run/uuidd:/usr/sbin/nologin
tcpdump:x:105:107::/nonexistent:/usr/sbin/nologin
landscape:x:106:108::/var/lib/landscape:/usr/sbin/nologin
fwupd-refresh:x:989:989:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
sshd:x:107:65534::/run/sshd:/usr/sbin/nologin
philipef:x:1000:1000:Philip Fleischer:/home/philipef:/bin/bash
philipef@networksecuritylab:/$ history
1 quit
2 exit
.
.
.
623 groups
624 groups philipef
625 gpasswd -d philipef reptiles
626 sudo gpasswd -d philipef reptiles
627 tail /etc/group
628 sudo groupdel reptiles
629 tail /etc/group
630 celar
631 clear
632 history
633 groups philipef
634 groups philipef
635 cat etc/passwd
636 history
philipef@networksecuritylab:/$ sudo apt update
Hit:1 https://download.docker.com/linux/ubuntu noble InRelease
Hit:2 http://ports.ubuntu.com/ubuntu-ports noble InRelease
Get:3 http://ports.ubuntu.com/ubuntu-ports noble-updates InRelease [126 kB]
Get:4 http://ports.ubuntu.com/ubuntu-ports noble-backports InRelease [126 kB]
Get:5 http://ports.ubuntu.com/ubuntu-ports noble-security InRelease [126 kB]
Get:6 http://ports.ubuntu.com/ubuntu-ports noble-updates/main arm64 Components [172 kB]
Get:7 http://ports.ubuntu.com/ubuntu-ports noble-updates/restricted arm64 Components [212 B]
Get:8 http://ports.ubuntu.com/ubuntu-ports noble-updates/universe arm64 Components [377 kB]
Get:9 http://ports.ubuntu.com/ubuntu-ports noble-updates/multiverse arm64 Components [212 B]
Get:10 http://ports.ubuntu.com/ubuntu-ports noble-backports/main arm64 Components [3572 B]
Get:11 http://ports.ubuntu.com/ubuntu-ports noble-backports/restricted arm64 Components [216 B]
Get:12 http://ports.ubuntu.com/ubuntu-ports noble-backports/universe arm64 Components [10.5 kB]
Get:13 http://ports.ubuntu.com/ubuntu-ports noble-backports/multiverse arm64 Components [212 B]
Get:14 http://ports.ubuntu.com/ubuntu-ports noble-security/main arm64 Components [18.4 kB]
Get:15 http://ports.ubuntu.com/ubuntu-ports noble-security/restricted arm64 Components [212 B]
Get:16 http://ports.ubuntu.com/ubuntu-ports noble-security/universe arm64 Components [71.4 kB]
Get:17 http://ports.ubuntu.com/ubuntu-ports noble-security/multiverse arm64 Components [212 B]
Fetched 1032 kB in 1s (1827 kB/s)
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
All packages are up to date.
philipef@networksecuritylab:/$ history
1 quit
2 exit
.
.
.
623 groups
624 groups philipef
625 gpasswd -d philipef reptiles
626 sudo gpasswd -d philipef reptiles
627 tail /etc/group
628 sudo groupdel reptiles
629 tail /etc/group
630 celar
631 clear
632 history
633 groups philipef
634 groups philipef
635 cat etc/passwd
636 history
philipef@networksecuritylab:/$ # Command with space in front will be omitted from history, can be good for security - Confidentiality

# Lecture 11 Output Redirection

philipef@networksecuritylab:/$ ls
bin etc media run swap.img
bin.usr-is-merged home mnt sbin sys
boot lib opt sbin.usr-is-merged tmp
cdrom lib.usr-is-merged proc snap usr
dev lost+found root srv var
philipef@networksecuritylab:/$ ls -l > file.txt
-bash: file.txt: Permission denied
philipef@networksecuritylab:/$ cd home/philipef/
philipef@networksecuritylab:~$ ls -l > file.txt
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab Linux_Lab_Notes file.txt notes test.pcap
philipef@networksecuritylab:~$ cat file.txt
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 0 Dec 25 10:45 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ # We just saved the output into a file!
philipef@networksecuritylab:~$ ls -l > file.txt
philipef@networksecuritylab:~$ ls -l > file.txt
philipef@networksecuritylab:~$ # Overwrote it two times, which can be dangerous
philipef@networksecuritylab:~$ ls -l >> file.txt
philipef@networksecuritylab:~$ # Now we appended it, in other words duplicated the output
philipef@networksecuritylab:~$ ls -l
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ cat file.txt
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 0 Dec 25 10:47 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 323 Dec 25 10:47 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ ls -l | grep file
-rw-rw-r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ # We just got the output for all files starting with file, if we had document and desktop in our current directory, then |grep do, would give us both
philipef@networksecuritylab:~$ cat file.txt | sort
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 0 Dec 25 10:47 file.txt
-rw-rw-r-- 1 philipef philipef 323 Dec 25 10:47 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
total 56
total 60
philipef@networksecuritylab:~$ cat file.txt | sort | uniq
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
-rw-rw-r-- 1 philipef philipef 0 Dec 25 10:47 file.txt
-rw-rw-r-- 1 philipef philipef 323 Dec 25 10:47 file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
total 56
total 60
philipef@networksecuritylab:~$ # file.txt occurs twice since it got increased twice
philipef@networksecuritylab:~$ cat file.txt | grep -v file.txt
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ cat file.txt | grep -v file.txt > new_file.txt
philipef@networksecuritylab:~$ cat new_file.txt
total 56
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
total 60
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ cat new_file.txt | sort | uniq
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
total 56
total 60
philipef@networksecuritylab:~$ ls -l | wc -l
7
philipef@networksecuritylab:~$ ls -l | wc
7 56 386
philipef@networksecuritylab:~$ ls -l /etc | wc -l
207
philipef@networksecuritylab:~$ # We got number of lines or items in the directory
philipef@networksecuritylab:~$

# Lecture 12 Streams

philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab file.txt notes
Linux*Lab_Notes new_file.txt test.pcap
philipef@networksecuritylab:~$ #Standard output
philipef@networksecuritylab:~$ #Standard Error:
philipef@networksecuritylab:~$ ls Turtles
ls: cannot access 'Turtles': No such file or directory
philipef@networksecuritylab:~$ ls -l /home/philipef
total 64
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
-rw-rw-r-- 1 philipef philipef 528 Dec 25 10:52 new_file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ echo $?
0
philipef@networksecuritylab:~$ #The echo $? command prints out the exit coe of the previous command
philipef@networksecuritylab:~$ ls Turtles
ls: cannot access 'Turtles': No such file or directory
philipef@networksecuritylab:~$ echo $?
2
philipef@networksecuritylab:~$ # Everything not 0 is an error
philipef@networksecuritylab:~$ find / -name *.log
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
.
.
.
/run/cloud-init/ds-identify.log
/run/cloud-init/cloud-init-generator.log
philipef@networksecuritylab:~$ # stdin 0 stdout 1 stderr 2
philipef@networksecuritylab:~$ find / -name _.log 2> errors.txt
/var/log/dpkg.log
/var/log/auth.log
.
.
.
/run/cloud-init/cloud-init-generator.log
philipef@networksecuritylab:~$ find / -name _.log 1> errors.txt
find: ‘/proc/tty/driver’: Permission denied
.
.
.
.service-S7VrUi’: Permission denied
philipef@networksecuritylab:~$ find / -name \_.log 2> errors.txt
/var/log/dpkg.log
.
.
.
/run/cloud-init/cloud-init-generator.log
philipef@networksecuritylab:~$ find / -name \*.log 1> success.txt
find: ‘/proc/tty/driver’: Permission denied
.
.
.
.service-S7VrUi’: Permission denied
philipef@networksecuritylab:~$ cat success.txt
/var/log/dpkg.log
.
.
.
/run/cloud-init/cloud-init-generator.log
philipef@networksecuritylab:~$ echo "hello World"
hello World
philipef@networksecuritylab:~$ echo $?
0

# Lecture 13 Variables

philipef@networksecuritylab:~$ echo "Hel"
Hel
philipef@networksecuritylab:~$ HELLOMSG="Hello World"
philipef@networksecuritylab:~$ echo HELLOMSG
HELLOMSG
philipef@networksecuritylab:~$ echo $HELLOMSG
Hello World
philipef@networksecuritylab:~$ echo $?
0
philipef@networksecuritylab:~$ MY_NUM=3
philipef@networksecuritylab:~$ MY_NUM2=10
philipef@networksecuritylab:~$ echo $MY_NUM
3
philipef@networksecuritylab:~$ echo $MY_NUM2
10
philipef@networksecuritylab:~$ MY_NAME="Philip"
philipef@networksecuritylab:~$ echo "My name is $MY_NAME"
My name is Philip
philipef@networksecuritylab:~$ MY_DIR="/etc"
philipef@networksecuritylab:~$ ls $MY_DIR
ModemManager            initramfs-tools      python3.12
PackageKit              inputrc              rc0.d
X11                     iproute2             rc1.d
adduser.conf            iscsi                rc2.d
alternatives            issue                rc3.d
apache2                 issue.net            rc4.d
apparmor                kernel               rc5.d
apparmor.d              landscape            rc6.d
apport                  ld.so.cache          rcS.d
apt                     ld.so.conf           resolv.conf
bash.bashrc             ld.so.conf.d         rmt
bash_completion         ldap                 rpc
bash_completion.d       legal                rsyslog.conf
bindresvport.blacklist  libaudit.conf        rsyslog.d
binfmt.d                libblockdev          screenrc
byobu                   libibverbs.d         security
ca-certificates         libnl-3              selinux
ca-certificates.conf    lighttpd             sensors.d
cloud                   locale.alias         sensors3.conf
console-setup           locale.conf          services
containerd              locale.gen           sgml
credstore               localtime            shadow
credstore.encrypted     logcheck             shadow-
cron.d                  login.defs           shells
cron.daily              logrotate.conf       skel
cron.hourly             logrotate.d          smi.conf
cron.monthly            lsb-release          sos
cron.weekly             lvm                  ssh
cron.yearly             machine-id           ssl
crontab                 magic                subgid
cryptsetup-initramfs    magic.mime           subgid-
crypttab                manpath.config       subuid
dbus-1                  mdadm                subuid-
dconf                   mime.types           sudo.conf
debconf.conf            mke2fs.conf          sudo_logsrvd.conf
debian_version          modprobe.d           sudoers
default                 modules              sudoers.d
deluser.conf            modules-load.d       supercat
depmod.d                mtab                 sysctl.conf
dhcp                    multipath            sysctl.d
dhcpcd.conf             multipath.conf       sysstat
docker                  nanorc               systemd
dpkg                    needrestart          terminfo
e2scrub.conf            netconfig            timezone
environment             netplan              tmpfiles.d
environment.d           network              ts.conf
ethertypes              networkd-dispatcher  ubuntu-advantage
fonts                   networks             ucf.conf
fstab                   newt                 udev
fuse.conf               nftables.conf        udisks2
fwupd                   nsswitch.conf        ufw
gai.conf                opt                  update-manager
glvnd                   os-release           update-motd.d
gnutls                  overlayroot.conf     update-notifier
groff                   pam.conf             usb_modeswitch.conf
group                   pam.d                usb_modeswitch.d
group-                  passwd               vconsole.conf
grub.d                  passwd-              vdpau_wrapper.cfg
gshadow                 perl                 vim
gshadow-                pki                  vmware-tools
gss                     plymouth             vtrgb
gtk-3.0                 pm                   vulkan
hdparm.conf             polkit-1             wgetrc
host.conf               pollinate            wireshark
hostname                profile              xattr.conf
hosts                   profile.d            xdg
hosts.allow             protocols            xml
hosts.deny              pulse                zsh_command_not_found
init.d                  python3
philipef@networksecuritylab:~$ pwd
/home/philipef
philipef@networksecuritylab:~$ MY_PATH="/home/philipef"
philipef@networksecuritylab:~$ cd MY_PATH
-bash: cd: MY_PATH: No such file or directory
philipef@networksecuritylab:~$ cd $MY_PATH
philipef@networksecuritylab:~$ cd ..
philipef@networksecuritylab:/home$ cd $MY_PATH
philipef@networksecuritylab:~$ # This is especially useful for bash scripts
philipef@networksecuritylab:~$ ls $MY_PATH
Enterprise-Network-Lab  errors.txt  new_file.txt  success.txt
Linux_Lab_Notes         file.txt    notes         test.pcap
philipef@networksecuritylab:~$ echo $user

philipef@networksecuritylab:~$ myvar="linux"
philipef@networksecuritylab:~$ echo $myvar
linux
philipef@networksecuritylab:~$ env
SHELL=/bin/bash
PWD=/home/philipef
LOGNAME=philipef
XDG*SESSION_TYPE=tty
HOME=/home/philipef
.
.
.
LESSOPEN=| /usr/bin/lesspipe %s
USER=philipef
SHLVL=1
XDG_SESSION_ID=144
LC_CTYPE=C.UTF-8
XDG_RUNTIME_DIR=/run/user/1000
SSH_CLIENT=192.168.64.1 63684 22
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
SSH_TTY=/dev/pts/0
OLDPWD=/home
*=/usr/bin/env
philipef@networksecuritylab:~$ export myvar="linux"
philipef@networksecuritylab:~$ echo $myvar
linux
philipef@networksecuritylab:~$ env
SHELL=/bin/bash
PWD=/home/philipef
LOGNAME=philipef
XDG*SESSION_TYPE=tty
HOME=/home/philipef
.
.
.
LESSOPEN=| /usr/bin/lesspipe %s
USER=philipef
myvar=linux
SHLVL=1
XDG_SESSION_ID=144
LC_CTYPE=C.UTF-8
XDG_RUNTIME_DIR=/run/user/1000
SSH_CLIENT=192.168.64.1 63684 22
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
SSH_TTY=/dev/pts/0
OLDPWD=/home
*=/usr/bin/env
philipef@networksecuritylab:~$

# Lecture 14 The find command

philipef@networksecuritylab:~$ pwd
/home/philipef
philipef@networksecuritylab:~$ find -name Music
philipef@networksecuritylab:~$ ls
Enterprise-Network-Lab errors.txt new_file.txt success.txt
Linux_Lab_Notes file.txt notes test.pcap
philipef@networksecuritylab:~$ find test
find: ‘test’: No such file or directory
philipef@networksecuritylab:~$ find test.pcap
test.pcap
philipef@networksecuritylab:~$ find -name log
philipef@networksecuritylab:~$ find -type -d -name log
find: Unknown argument to -type: -
philipef@networksecuritylab:~$ find -type f -name log
philipef@networksecuritylab:~$ # d for directory and f for file
philipef@networksecuritylab:~$ find -type d -name log
philipef@networksecuritylab:~$ find /var -type f -name "*log" 2> /dev/null
/var/lib/xml-core/catalog
/var/lib/dpkg/triggers/update-sgmlcatalog
/var/lib/apache2/conf/enabled_by_maint/other-vhosts-access-log
/var/lib/sgml-base/supercatalog
/var/log/dpkg.log
/var/log/auth.log
/var/log/ubuntu-advantage-apt-hook.log
/var/log/lastlog
/var/log/kern.log
/var/log/apport.log
/var/log/unattended-upgrades/unattended-upgrades.log
/var/log/unattended-upgrades/unattended-upgrades-shutdown.log
/var/log/unattended-upgrades/unattended-upgrades-dpkg.log
/var/log/apache2/other_vhosts_access.log
/var/log/apache2/access.log
/var/log/apache2/error.log
/var/log/landscape/sysinfo.log
/var/log/syslog
/var/log/fontconfig.log
/var/log/cloud-init-output.log
/var/log/alternatives.log
/var/log/cloud-init.log
/var/log/faillog
/var/log/installer/block/discover.log
/var/log/installer/cloud-init-output.log
/var/log/installer/curtin-install.log
/var/log/installer/cloud-init.log
/var/log/apt/term.log
/var/log/apt/history.log
/var/log/bootstrap.log
philipef@networksecuritylab:~$ find /var -type f -name "*log*" 2> /dev/null
/var/lib/xml-core/catalog
/var/lib/dpkg/triggers/update-sgmlcatalog
/var/lib/dpkg/info/login.prerm
/var/lib/dpkg/info/login.preinst
/var/lib/dpkg/info/logrotate.list
/var/lib/dpkg/info/rsyslog.postrm
/var/lib/dpkg/info/logrotate.postrm
/var/lib/dpkg/info/logrotate.postinst
/var/lib/dpkg/info/rsyslog.preinst
/var/lib/dpkg/info/rsyslog.prerm
/var/lib/dpkg/info/login.postinst
/var/lib/dpkg/info/logrotate.conffiles
/var/lib/dpkg/info/login.md5sums
/var/lib/dpkg/info/login.conffiles
/var/lib/dpkg/info/rsyslog.conffiles
/var/lib/dpkg/info/rsyslog.list
/var/lib/dpkg/info/logsave.list
/var/lib/dpkg/info/logsave.md5sums
/var/lib/dpkg/info/logrotate.prerm
/var/lib/dpkg/info/login.postrm
/var/lib/dpkg/info/rsyslog.triggers
/var/lib/dpkg/info/rsyslog.md5sums
/var/lib/dpkg/info/rsyslog.postinst
/var/lib/dpkg/info/login.list
/var/lib/dpkg/info/logrotate.md5sums
/var/lib/apache2/conf/enabled_by_maint/other-vhosts-access-log
/var/lib/ucf/cache/:etc:rsyslog.d:50-default.conf
/var/lib/systemd/deb-systemd-helper-enabled/multi-user.target.wants/rsyslog.service
/var/lib/systemd/deb-systemd-helper-enabled/rsyslog.service.dsh-also
/var/lib/systemd/deb-systemd-helper-enabled/syslog.service
/var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants/logrotate.timer
/var/lib/systemd/deb-systemd-helper-enabled/logrotate.timer.dsh-also
/var/lib/systemd/timers/stamp-logrotate.timer
/var/lib/sgml-base/supercatalog.old
/var/lib/sgml-base/supercatalog
/var/cache/swcatalog/cache/C-os-catalog.xb
/var/cache/swcatalog/cache/en-US-os-catalog.xb
/var/log/dpkg.log
/var/log/auth.log
/var/log/ubuntu-advantage-apt-hook.log
/var/log/lastlog
/var/log/kern.log
/var/log/apport.log
/var/log/unattended-upgrades/unattended-upgrades.log
/var/log/unattended-upgrades/unattended-upgrades-shutdown.log
/var/log/unattended-upgrades/unattended-upgrades-dpkg.log
/var/log/apache2/other_vhosts_access.log
/var/log/apache2/access.log
/var/log/apache2/error.log
/var/log/landscape/sysinfo.log
/var/log/syslog
/var/log/fontconfig.log
/var/log/cloud-init-output.log
/var/log/alternatives.log
/var/log/cloud-init.log
/var/log/faillog
/var/log/installer/subiquity-client-info.log.1645
/var/log/installer/subiquity-client-debug.log.1645
/var/log/installer/block/discover.log
/var/log/installer/subiquity-server-debug.log.1693
/var/log/installer/cloud-init-output.log
/var/log/installer/curtin-install.log
/var/log/installer/cloud-init.log
/var/log/installer/subiquity-server-info.log.1693
/var/log/apt/eipp.log.xz
/var/log/apt/term.log
/var/log/apt/history.log
/var/log/bootstrap.log
philipef@networksecuritylab:~$ find /var/log -type f -name *.log -mtime -7
/var/log/dpkg.log
/var/log/auth.log
/var/log/ubuntu-advantage-apt-hook.log
find: ‘/var/log/private’: Permission denied
/var/log/kern.log
/var/log/apport.log
/var/log/unattended-upgrades/unattended-upgrades.log
/var/log/unattended-upgrades/unattended-upgrades-shutdown.log
/var/log/unattended-upgrades/unattended-upgrades-dpkg.log
/var/log/apache2/other_vhosts_access.log
/var/log/apache2/access.log
/var/log/apache2/error.log
/var/log/fontconfig.log
/var/log/cloud-init-output.log
/var/log/alternatives.log
/var/log/cloud-init.log
/var/log/installer/block/discover.log
/var/log/installer/cloud-init-output.log
/var/log/installer/curtin-install.log
/var/log/installer/cloud-init.log
/var/log/apt/term.log
/var/log/apt/history.log
philipef@networksecuritylab:~$ #find /var/log -type f -name \*.log -mtime -30 -exec rm {} \;
philipef@networksecuritylab:~$

# Lecture 15 changing Perminssions Numerically

philipef@networksecuritylab:~$ ls -l
total 140
drwxrwxr-x 4 philipef philipef 4096 Dec 22 16:35 Enterprise-Network-Lab
drwxrwxr-x 3 philipef philipef 4096 Dec 22 20:05 Linux_Lab_Notes
-rw-rw-r-- 1 philipef philipef 73567 Dec 25 11:01 errors.txt
-rw-rw-r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
-rw-rw-r-- 1 philipef philipef 528 Dec 25 10:52 new_file.txt
drwxrwxr-x 2 philipef philipef 4096 Dec 24 13:08 notes
-rw-rw-r-- 1 philipef philipef 994 Dec 25 11:01 success.txt
-rw-r--r-- 1 tcpdump tcpdump 42872 Dec 20 17:20 test.pcap
philipef@networksecuritylab:~$ # r=4 w=2 x=1
philipef@networksecuritylab:~$ chmod 400 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-r-------- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 444 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-r--r--r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 004 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-------r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 200 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
--w------- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 002 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
--------w- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 700 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-rwx------ 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 600 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-rw------- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 655 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-rw-r-xr-x 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 644 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-rw-r--r-- 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$ chmod 777 file.txt
philipef@networksecuritylab:~$ ls -l file.txt
-rwxrwxrwx 1 philipef philipef 646 Dec 25 10:47 file.txt
philipef@networksecuritylab:~$
