# Permission

## 修改文件权限

```bash
chown [OPTIONS] USER[:GROUP] FILE(s)
USER 可以是 username 可以是 UID
GROUP 可以是 group name 也可以是 GID，该字段可以为空
如果 GROUP 为空，有两种情况：
1. USER 的形式为 USER，后面没有 :，那么文件只是修改 USER，但是 GROUP 未变
2. USER 的形式为 USER:，后面有 :，那么文件 owner 变成 USER，同时 GROUP 也变成该用户登录时的 GROUP
```

```bash
sudo chown windmill_knight:windmill_knight /workspace

sudo chown -R windmill_knight:windmill_knight /workspace
-R 选项可以让递归的修改该目录下所有文件的权限
```
