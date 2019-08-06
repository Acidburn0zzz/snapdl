# snapdl

Snapdl downloads and verifies signatures of OpenBSD snapshot releases.

The default download location is `/home/_sysupgrade`, which is the same location
used by `sysupgrade(8)`.  Make this location writable by an unprivileged user or
group to avoid running this tool as root.

To perform an unattended upgrade after placing files in the default download
location, copy `bsd.rd` to `/bsd.upgrade` and reboot.

```
$ doas sh
# install -m 0700 /home/_sysupgrade/bsd.rd /bsd.upgrade
# reboot
```
