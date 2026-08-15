# Windows Setup Guide

This document explains how to configure and run the DPI Engine on Windows.

---

# 1. Install Required Tools

## Install C++ Compiler

Install **MSYS2**:

Download:

https://www.msys2.org/

After installation open:

```
MSYS2 UCRT64 Terminal
```

Update packages:

```bash
pacman -Syu
```

Restart terminal and run:

```bash
pacman -Su
```

---

# 2. Install Development Packages

Install GCC compiler:

```bash
pacman -S mingw-w64-ucrt-x86_64-gcc
```

Install CMake:

```bash
pacman -S mingw-w64-ucrt-x86_64-cmake
```

Install Make:

```bash
pacman -S make
```

---

# 3. Install Libpcap / WinPcap

The project requires packet capture libraries.

Install:

- Npcap
- Npcap SDK

Download:

https://npcap.com/

During installation enable:

```
Install Npcap in WinPcap API-compatible Mode
```

---

# 4. Clone Repository

Clone the project:

```bash
git clone <repository-url>
```

Navigate:

```bash
cd PacketAnalyzer
```

---

# 5. Build Project

Create build directory:

```bash
mkdir build
cd build
```

Generate build files:

```bash
cmake ..
```

Compile:

```bash
cmake --build .
```

---

# 6. Run Application

After successful compilation:

```bash
./dpi_engine.exe
```

---

# Troubleshooting

## CMake cannot find compiler

Check GCC installation:

```bash
g++ --version
```

If not detected, add MSYS2 UCRT64 bin path:

```
C:\msys64\ucrt64\bin
```

to Windows Environment Variables.

---

## Packet capture permission issue

Run terminal as:

```
Administrator
```

---

## Missing pcap.h error

Verify Npcap SDK installation and include paths.

---

## Build clean

Remove build folder:

```bash
rm -rf build
```

Create again:

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

---

# Development Environment

Recommended:

- Visual Studio Code
- C/C++ Extension
- CMake Tools Extension
- MSYS2 UCRT64 Compiler
