# Find

http://www.cnblogs.com/skynet/archive/2010/12/25/1916873.html

find [path...] [expression]

## path

```
. represent the current path, / represent the root path.
```

## expression

- -name (find by name)

```
find . -name filename
find /opt -name filename
```

- -perm (find the file by permission)

```
find . -perm 755
```

- -prune (filter the special folder)

```
Do not find in the special folder.
find /opt -path "/opt/deploy" -prune
```

- -user

```
Find file by user.
find . -user laxino
```

- -group

```
Find file by group.
find . -group laxino_rnd
```

- -mtine -n +n

```
Find file by change time.
-n, the file changed in n days.
+n, the file changed n days ago.
find . -mtime -5
```

- nogroup / nouser

```
find . -nogroup
find . -nouser
```

- -type

```
b: Block device file
d: Dir
c: Character device file
p: Pipeline file
l: Link file
f: General file
```

- -size

```
Find file by size (default measure 1 block = 512 bytes = 0.5 KB).
find . -size -1000
find . -size 1000
find . -size +1000
```

## xargs

```
After find file, through the parameters by xargs to next command.

find . -type f | xargs file
find . | xargs echo > /tmp/file_list.txt
find . -type f | xargs grep "hostname"
find . -type f -mtime +3 | xargs rm -rf
find . -type f -size 0 | grep xargs rm -rf
```

## Example

```
find . -type f -size +10240 -name '*.log'
Find log file size > 5M
```
