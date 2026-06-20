# OnePlus 15T fairlady OrangeFox device tree

## Working

- [x] Display
- [x] Touch 
- [x] Decryption
- [x] Flashing
- [x] Backup & Restore
- [x] KernelSU, KernelSU Next & SukiSU Ultra Installer
- [x] MTP/OTG Storage
- [x] ADB/FastbootD
- [x] Factory Reset
- [x] Vibrator
- [x] Display & Vibration Settings
- [x] Flashlight

## Not working

- [ ] ???????

# How To Build

### Clone & Sync Source
```
mkdir -p ~/android/OrangeFox_14
cd ~/android/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/android/fox_14.1
```
### Clone Device-tree And Prebuilt Kernel
```
cd ~/android/fox_14.1/device
mkdir -p oneplus
cd oneplus
git clone https://github.com/iliaoke/android_device_oneplus_fairlady-orangefox fairlady
git clone https://github.com/OnePlus-SM8850-Development/android_device_oneplus_fairlady-kernel fairlady-kernel
```
### BUILD!
```
cd ~/android/fox_14.1
source build/envsetup.sh
lunch twrp_fairlady-ap2a-eng
mka adbd recoveryimage
```
