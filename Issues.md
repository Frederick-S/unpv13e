# Build error when building the library under libfree folder
Detail:
```
inet_ntop.c:56:1: error: conflicting types for 'inet_ntop'
inet_ntop(af, src, dst, size)
```

Because `arpa/inet.h` already defines a method with the same name. `inet_ntop` is renamed to `my_inet_ntop`.
