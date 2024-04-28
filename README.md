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

The project supports debugging with the use of the `vscode` editor. In order to make it work, it is necessary to set `DBG` envionmental variable to contain the path to the debugger associated with the used compiler. It is also necessary to build the executable with the `CMAKE_BUILD_TYPE` option set to `Debug`.



