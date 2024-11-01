#Redhat #Linux 

The `mv` command moves files from one location to another. If you think of the absolute path to a file as its full name, then moving a file is effectively the same as renaming a file. The contents of the files that are moved remain unchanged.

Use the `mv` command to _rename_ a file. In the following example, the `mv thesis_chapter2.txt` command renames the `thesis_chapter2.txt` file to `thesis_chapter2_reviewed.txt` in the same directory.

```sh
[user@host Documents]$  ls -l
-rw-r--r--. 1 user user  7100 Mar  7 14:37 thesis_chapter1.txt
-rw-r--r--. 1 user user 11431 Mar  7 14:39 thesis_chapter2.txt
_...output omitted..._
[user@host Documents]$  mv thesis_chapter2.txt thesis_chapter2_reviewed.txt
[user@host Documents]$  ls -l
-rw-r--r--. 1 user user  7100 Mar  7 14:37 thesis_chapter1.txt
-rw-r--r--. 1 user user 11431 Mar  7 14:39 thesis_chapter2_reviewed.txt
_...output omitted..._
```

Use the `mv` command to _move_ a file to a different directory. In the next example, the `thesis_chapter1.txt` file is moved from the `~/Documents` directory to the `~/Documents/Thesis/Chapter1` directory. You can use the `mv` command `-v` option to display a detailed output of the command operations.

```sh
[user@host Documents]$ ls Thesis/Chapter1
[user@host Documents]$
[user@host Documents]$ mv -v thesis_chapter1.txt Thesis/Chapter1
renamed 'thesis_chapter1.txt' -> 'Thesis/Chapter1/thesis_chapter1.txt'
[user@host Documents]$ ls Thesis/Chapter1
thesis_chapter1.txt
[user@host Documents]$ ls -l
-rw-r--r--. 1 user user 11431 Mar  7 14:39 thesis_chapter2_reviewed.txt
_...output omitted..._
```
