# My Hackintosh
My hackintosh configuration

#### CPU
Intel (r) Core (tm) i7-9700K 8 core Coffee Lake-S

#### Motherbord
Asus Rog Strix Z390-E gaming

#### GPU
Sapphire Nitro+ AMD Radeon RX580 Polaris 20XTX 8Gb

#### Audio
Realtek ALC1220P / ALC S1220A

 #### Network
 Braodcom BCM943602CS 802.11ac
 Intel Ethernet Connection I219-V
 
 #### HDD
 Samsung SSD 850 Evo

##
[EFI](https://github.com/roan-droid/hackintosh/tree/main/EFI) for Opencore 0.6.5

## Fast How-to
Edit config.plist with your serials or use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
Mount you EFI partition, copy EFI folder and enjoy
Futher information on [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

### To Fix DRM issue use this commands

List of overrides:

`defaults write com.apple.AppleGVA gvaForceAMDKE -boolean yes` forces AMD DRM decoder for streaming services (like Apple TV and iTunes movie streaming)

`defaults write com.apple.AppleGVA gvaForceAMDAVCDecode -boolean yes` forces AMD AVC accelerated decoder

`defaults write com.apple.AppleGVA gvaForceAMDAVCEncode -boolean yes` forces AMD AVC accelerated encoder

`defaults write com.apple.AppleGVA gvaForceAMDHEVCDecode -boolean yes` forces AMD HEVC accelerated decoder

`defaults write com.apple.AppleGVA disableGVAEncryption -string YES` forces AMD HEVC accelerated decoder

`defaults write com.apple.coremedia hardwareVideoDecoder -string force` forces hardware accelerated video decoder (for any resolution)

`defaults write com.apple.coremedia hardwareVideoDecoder -string disable` disables hardware accelerated video decoder (in QuickTime / Apple TV)

[source](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.Chart.md)
