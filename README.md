Foxconn T99W175 flash utility 
---

## Compile for Windows
* Install MinGW64.
* Install `mman` and `libusb`
```
pacman -S mingw-w64-x86_64-mman-win32 mingw-w64-x86_64-libusb
```
* Compile
```
git clone https://github.com/pccr10001/flash_fox
cd flash_fox
make
```

### Flash Firmwares
* Enter `fastboot`
```
AT^FASTBOOT
```
* Install `libusbK` from Zadig.
  * Enable `List All Devices` in `Options` menu.
  * Select `Android` in device list.
  * Make sure `USB ID` is `18d1:d00d`
  * Select `libusbK (v3.1.0.0)` in driver list
  * Click `Replace Driver`
* Flash firmwares
```
flash_fox.exe ota.bin
```
