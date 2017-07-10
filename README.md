[![Build Status](https://travis-ci.org/Frederick-S/unpv13e.svg?branch=master)](https://travis-ci.org/Frederick-S/unpv13e)
# Issues
## Build error when building the library under libfree folder
Detail:
```
inet_ntop.c:56:1: error: conflicting types for 'inet_ntop'
inet_ntop(af, src, dst, size)
```

Here is the [solution](https://stackoverflow.com/questions/7947960/unix-network-programming-book-code-has-bugs-due-to-old-os-how-to-solve-this-or).
