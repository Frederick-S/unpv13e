[![Build Status](https://travis-ci.org/Frederick-S/unpv13e.svg?branch=master)](https://travis-ci.org/Frederick-S/unpv13e)
# Issues
## Build error when building the library under libfree folder
Detail:
```
inet_ntop.c:56:1: error: conflicting types for 'inet_ntop'
inet_ntop(af, src, dst, size)
```

Here is the [solution](https://stackoverflow.com/questions/7947960/unix-network-programming-book-code-has-bugs-due-to-old-os-how-to-solve-this-or).

## `daytimetcpcli` connect error: Connection refused
The daytime service might be not enabled.

The following steps enable the daytime service on Ubuntu:

```
sudo apt-get update
sudo apt-get install xinetd
cd /etc/xinetd.d
sudo vim daytime // change disable to no in both tcp and udp version
sudo service xinetd reload
```
