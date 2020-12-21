# File Link

## mount & umount

```
sudo mount --bind source target
该命令会将 source 的内容挂载到 target 目录上。
经过 mount 之后，target 和 source 的内容会一摸一样，我们操作 target 实际上操作的就是 source。
我们在 source 中的修改同样也会改变 target。
那原来 target 的内容哪里去了呢？原来 target 的内容被系统隐藏起来，暂时无法访问了，但并为删除。

sudo umount target
通过 umount 命令可以解除挂载，同时 target 里面的内容会恢复到和 mount 之前一样。

sudo mount --bind /workspace/vendor/ /workspace/sso/vendor/

sudo umount /workspace/sso/vendor
```
