# Entwicklung eines Bare-Metal-Bootloaders für den Raspberry Pi 5

## 1. Ziel
Der Bootloader soll Multiboot unterstützen und in der Lage sein, Betriebssysteme über das Netzwerk herunterzuladen und zu installieren.

## 2. Programmiersprache
Nach Abwägung der Optionen wurde **C** mit etwas **Assembler** gewählt, da es einfacher einzurichten ist und viele existierende Beispiele für den Raspberry Pi gibt.