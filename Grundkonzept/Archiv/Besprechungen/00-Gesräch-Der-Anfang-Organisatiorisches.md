# Entwicklung eines Bare-Metal-Bootloaders für den Raspberry Pi 5

## 1. Ziel
Der Bootloader soll Multiboot unterstützen und in der Lage sein, Betriebssysteme über das Netzwerk herunterzuladen und zu installieren.

## 2. Programmiersprache
Nach Abwägung der Optionen wurde **C** mit etwas **Assembler** gewählt, da es einfacher einzurichten ist und viele existierende Beispiele für den Raspberry Pi gibt.

## 3. Notwendige Tools und Programme (Windows 10 x64)
### **Compiler & Toolchain**
- **ARM GNU Toolchain** ([Download](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads))
  - AArch64 ELF (Bare-Metal) Toolchain installieren
  - `bin/`-Pfad zur **Umgebungsvariable PATH** hinzufügen
  - Test: `aarch64-none-elf-gcc --version`
- **CMake** ([Download](https://cmake.org/download/)) (optional, für Build-Management)
- **Ninja** ([Download](https://ninja-build.org/)) (Alternative zu `make`)
- **QEMU** ([Download](https://qemu.weilnetz.de/)) (für Emulator-Tests)

### **Code-Editor & IDE**
- **VS Code** ([Download](https://code.visualstudio.com/)) (empfohlen)
  - Erweiterungen:
    - **C/C++ Extension Pack**
    - **ARM Assembly (Syntax-Highlighting)**
- Alternativen: CLion, Notepad++, VSCodium

### **Debugging & Serielle Konsole**
- **PuTTY** ([Download](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html))
- Alternative: **Tera Term**

### **SD-Karten-Management & Boot-Dateien**
- **Raspberry Pi Imager** ([Download](https://www.raspberrypi.com/software/))
- **Win32DiskImager** ([Download](https://sourceforge.net/projects/win32diskimager/))
- **HxD Hex-Editor** ([Download](https://mh-nexus.de/en/hxd/))
- **Balena Etcher** ([Download](https://www.balena.io/etcher/))

### **Raspberry Pi 5 spezifische Tools & Firmware**
- **Offizielle Boot-Firmware** ([Download](https://github.com/raspberrypi/firmware))
- **RPi Boot (USB-Mode-Tests)** ([Download](https://github.com/raspberrypi/usbboot))

### **Zusätzliche nützliche Tools** (optional)
- **GCC ARM Assembly Online Compiler** ([Godbolt](https://godbolt.org/))
- **Binwalk (Boot-Dateien analysieren)** ([Download](https://github.com/ReFirmLabs/binwalk))

## 4. Nächste Schritte
1. **Installation der Toolchain und VS Code**
2. **Test der Toolchain** (`aarch64-none-elf-gcc` im Terminal ausführen)
3. **Erstellung eines ersten Bare-Metal-Programms** (LED-Blinken oder serielle Ausgabe)
4. **Schrittweise Erweiterung um Multiboot- und Netzwerk-Funktionalität**

