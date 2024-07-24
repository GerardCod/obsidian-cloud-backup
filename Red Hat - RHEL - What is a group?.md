#Redhat #RHEL #Linux 

A group is a collection of users that need to share access to files and other system resources. Groups can grant access to files to a set of users instead of to a single user.

Like users, groups have _group names_ for easier recognition. Internally, the system distinguishes groups by the unique identification number, the _group ID_ or _GID_, which is assigned to them. The mapping of group names to GIDs is defined in identity management databases of group account information. By default, systems use the `/etc/group` file to store information about local groups.

Each line in the `/etc/group` file contains information about one group. Each group entry is divided into four colon-separated fields. An example of a line from `/etc/group` follows:

```bash
[user01@host ~]$ cat /etc/group
_...output omitted..._
group01:x:10000:user01,user02,user03
```

Consider each part of the code block, separated by a colon:

- **`group01`** : Name for this group.
- **`x`** : Obsolete group password field; it is now a placeholder.
- **`10000`** : The GID number for this group (`10000`).
- **`user01,user02,user03`** : A list of users that are members of this group as a supplementary group.