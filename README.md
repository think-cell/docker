# think-cell/docker

This is a collection of docker container we use to test our projects on CI.
They are designed to compile a CMake project using Ninja and a specific compiler version and run the tests;
not to actually build a released executable or anything like that.

## Common Software

* curl
* git
* CMake 3.27.6
* ninja

It is designed for a basic CMake workflow:

```sh
cmake /path/to/src
cmake --build .
ctest
```

This will automatically select the specific compiler and Ninja as generator.

## Image ghcr.io/think-cell/clang:<version>

* clang 6-10 on Debian buster
* clang 11-15 on Debian bullseye
* clang 16 on Debian bookworm

## Image ghcr.io/think-cell/gcc:<version>

* GCC 7-13

