# Hackintosh
Hackintosh ( Z390 + i7-9700K + 5700XT ) + OpenCore 0.5.9

## Hardware

- CPU: Intel Core i7-9700K
- Motherboard: Gigabyte Z390 Aourus Elite, F10c BIOS Version
- RAM: 16 GB DDR4 PC3200 * 2
- GPU: Radeon RX 5700 XT 8GB
- OSX Version : macOS Catalina 10.15.5

## BISO Setting

### CFG Unlock

```shell
# Tools -> modGRUBShell
setup_var_3 0x5C1
setup_var_3 0x5C1 0x00
```


