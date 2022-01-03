# 二进制编辑器

hexedit（命令行）

ghex(客户端)



都可以直接通过 apt install 安装



# qemu 模拟软盘

需要安装 qemu-system-i386、qemu-system-x86

```sh
qemu-system-i386 -drive file=helloos.img,if=floppy,format=raw
```

其中，

-drive 定义了一个新的驱动，后面的 file=helloos.img,if=floppy,format=raw 是 -drive 的选项，file 是驱动使用的文件，if 是驱动类型，有 ide, scsi, sd, mtd, floppy, pflash, virtio, none 这几种类型，format 可以是 raw, base64等



