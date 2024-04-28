## Executable template
### Overview

This repository contains the standard template for the executable with linked static library. This repository depends on `cmake` build automation tool and `ninja` build system. 

### Building

In order to build the executable and the library it is necessary to configure the project and perform the actual build. The first one is performed with

    cmake -G "Ninja" -B build

which results in the project configuration files for `ninja` generator being generated in the directory `build`. The second action is performed with

    ninja -C build

which performs out-of-source build in `build` directory.

### Running

After performing the build, the example application can be launched by calling

    cd build
    ./executable_template

### Debugging

TODO



