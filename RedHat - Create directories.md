#Redhat #Linux 

The `mkdir` command creates one or more directories or subdirectories. It takes as an argument a list of paths to the directories that you want to create.

In the following example, files and directories are organized beneath the `/home/user/Documents` directory. Use the `mkdir` command and a space-delimited list of the directory names to create multiple directories.

```sh
[user@host ~]$ cd Documents
[user@host Documents]$ mkdir ProjectX ProjectY ProjectZ
[user@host Documents]$ ls
ProjectX  ProjectY ProjectZ
```

If the directory exists, or a parent directory of the directory that you are trying to create does not exist, then the `mkdir` command fails and it displays an error.

The `mkdir` command `-p` (_parent_) option creates any missing parent directories for the requested destination. In the following example, the `mkdir` command creates three ``Chapter_`N`_`` subdirectories with one command. The `-p` option creates the missing `Thesis` parent directory.

```bash
[user@host Documents]$  mkdir -p Thesis/Chapter1 Thesis/Chapter2 Thesis/Chapter3
[user@host Documents]$ ls -R Thesis/
Thesis/:
Chapter1  Chapter2  Chapter3

Thesis/Chapter1:

Thesis/Chapter2:

Thesis/Chapter3:
```

Use the `mkdir` command `-p` option with caution, because spelling mistakes can create unintended directories without generating error messages. In the following example, imagine that you are trying to create a `Watched` subdirectory in the `Videos` directory, but you accidentally omitted the letter "s" in `Videos` in your `mkdir` command.

```sh
[user@host ~]$ mkdir Video/Watched
mkdir: cannot create directory `Video/Watched`: No such file or directory
```

The `mkdir` command fails because the `Video` directory does not exist. If you had used the `mkdir` command with the `-p` option, then the `Video` directory would be created unintentionally. The `Watched` subdirectory would be created in that incorrect directory.