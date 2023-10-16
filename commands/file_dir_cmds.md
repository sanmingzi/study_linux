# File directory commands

```
touch 用于创建空白文件或者修改文件的时间
touch [参数] filename
-a 仅修改访问时间 (Atime)
-m 仅修改修改时间 (Mtime)
-d 同时修改 Atime 和 Mtime

touch test # 创建一个名称为 test 的空白文件

touch -d "2023-01-01 00:00:00" test # 黑客的小妙招
```

```
mkdir，make directory，创建空白目录
mkdir [参数] directory_name
-p 可递归创建文件目录

mkdir a

mkdir -p a/b/c
```

```
cp，copy，复制文件或目录
cp [参数] source_name target_name
-p 保留原始文件的属性
-d 保留链接文件的属性
-r 用于目录复制
-i 若目标文件存在询问是否覆盖
-a 相当于 -pdr

如果 target 是目录，则会把 source 复制到该目录中
如果 target 是普通文件，则会覆盖
如果 target 不存在，则执行正常的复制操作

cp source_file target_file # 将 source_file 复制为 target_file

cp -i source_file target_file # 如果 target_file 存在会询问是否覆盖

cp source_file target_dir # source_file 被复制到 target_dir

cp -r source_dir target_id # source_dir 被复制到 target_dir
```

```
mv，move，用于剪切或重命名文件
mv [参数] source_name target_name
-i 若目标文件存在询问是否覆盖

如果 target 是目录，则会把 source 剪切到该目录中
如果 target 是普通文件，则会覆盖
如果 target 不存在，则执行正常的剪切操作
```
