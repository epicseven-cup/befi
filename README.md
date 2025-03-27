# Run (Tested on Fedora)
```bash
qemu-system-x86_64 -cpu qemu64 -drive if=pflash,format=raw,unit=0,file=/usr/share/edk2/ovmf/OVMF_CODE.fd,readonly=on   -drive if=pflash,format=raw,unit=1,file=/usr/share/edk2/ovmf/OVMF_VARS.fd   -net none
```


## Need to create a disk image for QEMU 
- https://wiki.osdev.org/UEFI

# Running the EFI Application
```bash
qemu-system-x86_64 -cpu qemu64 -bios /usr/share/edk2/ovmf/OVMF_CODE.fd -drive file=befi.img,format=raw
```