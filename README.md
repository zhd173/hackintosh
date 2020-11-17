# Hackintosh
Hackintosh ( Z390 + i7-9700K + 5700XT ) + OpenCore 0.6.3

## Hardware

- CPU: Intel Core i7-9700K
- Motherboard: Gigabyte Z390 Aourus Elite, F10c BIOS Version
- RAM: 16 GB DDR4 PC3200 * 2
- GPU: Radeon RX 5700 XT 8GB
- OSX Version : macOS Big Sur 11.0.1

[1](./images/1.png)
[2](./images/2.png)
[3](./images/3.png)
[4](./images/4.png)

## BISO Setting

### Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option then enable AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

How to disable CFG Lock:

```shell
# Tools -> modGRUBShell
setup_var_3 0x5C1
setup_var_3 0x5C1 0x00
```
### Enable

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI
