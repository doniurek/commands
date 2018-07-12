# [⬅ Back	to Unix commands](unix.md)
# `df`
Report free disk space

If no file name is given, the space available on all currently mounted file systems is shown.

## Options
`-h` print sizes in powers of 1024 (e.g., 1023M)
`-H` print sizes in powers of 1000 (e.g., 1.1G)

## Examples
`df -h`
>| Filesystem | Size | Used | Avail | Use% | Mounted on |
| ----- | -----| ----- | ----- | -----| ----- |
|udev|            3,9G|     0|  3,9G|   0%| /dev|
|tmpfs           |787M  |9,4M  |778M   |2% |/run|
|/dev/sda6       |105G   |98G  |1,8G  |99% |/|
|tmpfs           |3,9G   |18M  |3,9G   |1% |/dev/shm|
|tmpfs           |5,0M  |4,0K  |5,0M   |1% |/run/lock
|tmpfs           |3,9G     |0  |3,9G   |0% |/sys/fs/cgroup|
|/dev/sda2        |95M   |29M   |67M  |31% |/boot/efi|
|cgmfs           |100K     |0  |100K   |0% |/run/cgmanager/fs|
|tmpfs           |787M   |28K  |787M   |1% |/run/user/1001|

---
`df -h /home/donia/Desktop/`
>| Filesystem | Size | Used | Avail | Use% | Mounted on |
| ----- | -----| ----- | ----- | -----| ----- |
|/dev/sda2        |95M   |29M   |67M  |31% |/boot/efi|
