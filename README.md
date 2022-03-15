## PS2 C++20/CMake Primer

Primer for using modern tools wto build software for the PlayStation 2 console.

This project can be used as a template for building C++20 software on the PS2.

## Building from source

You need PS2SDK installed (the PS2DEV/open source one, not the Sony one).

It can be gathered [here](https://github.com/ps2dev/ps2toolchain) if you do not have it installed.

To build:

```bash
$ cmake -Bbuild -GNinja --toolchain cmake/toolchain/ps2.cmake
$ cmake --build build
```
