#Redhat #Linux 

The `rm` command removes files. By default, `rm` does not remove directories. You can use the `rm` command `-r` or the `--recursive` option to enable the `rm` command to remove directories and their contents. The `rm -r` command traverses each subdirectory first, and individually removes their files before removing each directory.

In the following example, the `rm` command removes the `thesis_chapter1.txt` file without options, but to remove the `Thesis/Chapter1` directory, you must add the `-r` option.

```sh
[user@host Documents]$  ls -l Thesis/Chapter1
-rw-r--r--. 1 user user 7100 Mar  7 14:37 thesis_chapter1.txt
[user@host Documents]$  rm Thesis/Chapter1/thesis_chapter1.txt
[user@host Documents]$  rm Thesis/Chapter1
rm: cannot remove 'Thesis/Chapter1': Is a directory
[user@host Documents]$  rm -r Thesis/Chapter1
[user@host Documents]$  ls -l Thesis
drwxr-xr-x. 2 user user 6 Mar  7 12:37 Chapter2
drwxr-xr-x. 2 user user 6 Mar  7 12:37 Chapter3
```

> [!NOTE] Important
> Red Hat Enterprise Linux does not provide a command-line undelete feature, nor a "trash bin" from which you can restore files held for deletion. A trash bin is a component of a desktop environment such as GNOME, but is not used by commands that are run from a shell.

