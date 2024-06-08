# Hey! I'm Filing Here

In this lab, I successfully implemented an ext2 file system image which contains a root directory with one directory, one regular file, and one symbolic link inside of it.

## Building

Run the following command to build the executable
```shell
make
```
Then run the following command to create the filesystem image
```shell
./ext2-create
```

## Running

Can view filesystem contents and check image validity with the following commands:
```shell
dumpe2fs cs111-base.img
fsck.ext2 cs111-base.img
```

To mount and view the filesystem, run
```shell
mkdir mnt
sudo mount -o loop cs111-base.img mnt
```
(now you can navigate the filesystem image)

```shell
sudo unmount mnt
rmdir mnt
```
unmount


## Cleaning up

```shell
make clean
```
