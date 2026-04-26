# Project README

## Overview
This project is a C-based application that implements Fourier series transformations using a graphical user interface. The application provides visualizations of the transformation process and supports running on multiple platforms including Linux, Windows, wine, and web assembly.

## Features
- **Fourier Series Visualization**: Displays the Fourier transform of input signals graphically.
- **Interactive User Interface**: Allows users to interact with the visualization through a graphical window.
- **Cross-Platform Compatibility**: Supports compilation and execution on Linux, Windows, via Wine, and WebAssembly.

## Project Structure
```
<project>/
├── build/              # Compiled executable files (.exe)
├── src/                # Source code directory
│   ├── Main.c          # Entry point of the application
│   └── *.h             # Header files containing function declarations
├── Makefile.linux      # Linux specific build configuration
├── Makefile.windows    # Windows specific build configuration
├── Makefile.wine       # Wine specific build configuration for cross-compiling to Windows
└── README.md           # This file
```

### Prerequisites
- **C/C++ Compiler**: GCC (GNU Compiler Collection) is used for compiling the C code.
- **Development Tools**: Standard development tools are required, including make and any necessary libraries like X11 for Linux or WINAPI for Windows.
- **Libraries**: The project depends on libraries such as libpng and libjpeg for image processing, and user32 and gdi32 for graphical output.

## Build & Run
To build the project, navigate to the project directory and run:

### Building on Linux:
```bash
make -f Makefile.linux all
```

### Building on Windows (using MinGW):
```bash
make -f Makefile.windows all
```

### Building using Wine for Windows Cross-Compilation:
```bash
make -f Makefile.wine all
```

### Building WebAssembly for the Web:
```bash
make -f Makefile.web all
```

To execute the built application, use:

### Running on Linux:
```bash
make -f Makefile.linux exe
```

### Running on Windows (from build directory):
```bash
./build/Main.exe
```

### Running using Wine for Windows Cross-Compilation:
```bash
WINEPREFIX=~/wine64 WINEARCH=win64 wine ./build/Main.exe
```

### Running WebAssembly:
Open the `index.html` file in a web browser to run the application.

To clean and rebuild the project, use:

```bash
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

This README provides a clear guide on how to build, run, and understand the project structure.