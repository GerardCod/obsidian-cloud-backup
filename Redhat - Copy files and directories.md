#Redhat #Linux 

The `cp` command copies a file, and creates a file either in the current directory or in a different specified directory.

```sh
[user@host ~]$  cd Videos
[user@host Videos]$  cp blockbuster1.ogg blockbuster3.ogg
[user@host Videos]$  ls -l
total 0
-rw-rw-r--. 1 user user    0 Feb  8 16:23 blockbuster1.ogg
-rw-rw-r--. 1 user user    0 Feb  8 16:24 blockbuster2.ogg
-rw-rw-r--. 1 user user    0 Feb  8 16:34 `blockbuster3.ogg`
```

You can also use the `cp` command to copy multiple files to a directory. In this scenario, the last argument must be a directory. The copied files retain their original names in the new directory. If a file with the same name exists in the target directory, then the existing file is overwritten.

> [!NOTE] Note
> By default, the `cp` command does not copy directories; it ignores them.

In the following example, two directories are listed as arguments, the `Thesis` and `ProjectX` directories. The last argument, the `ProjectX` directory, is the target and is valid as a destination. The `Thesis` argument is ignored by the `cp` command, because it is intended to be copied and it is a directory.

```sh
[user@host Documents]$  cp thesis_chapter1.txt thesis_chapter2.txt Thesis ProjectX
cp: -r not specified; omitting directory 'Thesis'
[user@host Documents]$  ls Thesis ProjectX
ProjectX:
thesis_chapter1.txt  thesis_chapter2.txt

Thesis:
Chapter1  Chapter2  Chapter3
```

The `Thesis` directory failed to copy, but the copying of the `thesis_chapter1.txt` and `thesis_chapter2.txt` files succeeded.

You can copy directories and their contents by using the `cp` command `-r` option. Keep in mind that you can use the `.` and `..` special directories in command combinations. In the following example, the `Thesis` directory and its contents are copied to the `ProjectY` directory.

```sh
[user@host Documents]$  cd ProjectY
[user@host ProjectY]$  cp -r ../Thesis/ .
[user@host ProjectY]$  ls -lR
.:
total 0
drwxr-xr-x. 5 user user 54 Mar  7 15:08 Thesis

./Thesis:
total 0
drwxr-xr-x. 2 user user 6 Mar  7 15:08 Chapter1
drwxr-xr-x. 2 user user 6 Mar  7 15:08 Chapter2
drwxr-xr-x. 2 user user 6 Mar  7 15:08 Chapter3

./Thesis/Chapter1:
total 0

./Thesis/Chapter2:
total 0

./Thesis/Chapter3:
total 0
```