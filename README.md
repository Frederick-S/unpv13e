[![Build Status](https://travis-ci.org/Frederick-S/unpv13e.svg?branch=master)](https://travis-ci.org/Frederick-S/unpv13e)
# Issues
## Build error when building the library under libfree folder
Detail:
```
inet_ntop.c:56:1: error: conflicting types for 'inet_ntop'
inet_ntop(af, src, dst, size)
```

Change `size_t` to `socklen_t` can fix the issue. ([reference](https://stackoverflow.com/questions/7947960/unix-network-programming-book-code-has-bugs-due-to-old-os-how-to-solve-this-or))

## `./daytimetcpcli 127.0.0.1` connect error: Connection refused
The daytime service might be not enabled.

The following steps enable the daytime service on Ubuntu:

```
sudo apt-get update
sudo apt-get install xinetd
cd /etc/xinetd.d
sudo vim daytime // change disable to no in both tcp and udp version
sudo service xinetd reload
```

## `./daytimetcpsrv` bind error: Permission denied
> Ports below 1024 are considered "privileged" and can only be bound to with an equally privileged user (read: root). ([reference](https://stackoverflow.com/questions/20396820/socket-programing-permission-denied))

Try to run it with root.
