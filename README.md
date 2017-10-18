# ASRock-H110M-G-M2


Phân vùng EFI dùng cho mainboard ASRock H110M-G/M.2

# Cấu hình:
* Mainboard: ASRock H110M-G/M.2
* CPU: Intel i3-7100
* RAM: 8GB/DDR4/2133
* GPU: ASUS PH-GT1030-O2G
* SSD: 240GB SATA3 

# Cấu trúc phân vùng EFI


EFI

-Boot

--BOOTX64.efi (Clover Bootloader)

-Clover

--ACPI

---Patched

----SSDT-GFX0.aml (Sleep/wake fix for nvidia)

----SSDT-PM.aml (Speedstep for i3-7100)

----SSDT-UIAC.aml (USB port patch for USBInjectAll.kext, fix sleep/wake problem)

--CLOVERX64.efi (Clover Bootloader)

--config.plist (config file for ASRock H110M-G/M.2)

--drivers64UEFI

---apfs.efi (Use for APFS filesystem macOS 10.13)

---EmuVariableUefi-64.efi (Use for 100-series mainboard)

---OsxAptioFix2Drv-64.efi

--kexts

---Other

----AppleALC.kext (Audio fix for ALC887)

----FakeSMC_xxSensors.kext (Use for HWSensors)

----FakeSMC.kext

----IntelMausiEthernet.kext (Ethernet fix for Intel® I219-V)

----Lilu.kext (Help to inject AppleALC, Shiki,...)

----Shiki.kext (iTunes-DRM enable)

----USBInjectAll.kext (Inject USB port)

-Microsoft (Windows 10 Boot Manager) 