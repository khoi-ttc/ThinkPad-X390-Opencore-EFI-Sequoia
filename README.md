# ThinkPad-X390-Opencore-EFI-Sequoia (OC 1.0.2)

## Table of Contents

- [Device Information](#device-information)
- [Usage](#usage)
- [Detailed-Device-Drivers](#detailed-device-drivers)
  - [CPU](#cpu)
  - [Battery](#battery)
  - [USB](#usb)
  - [Ethernet](#ethernet)
  - [Display](#display)
  - [Audio](#audio)
  - [Keyboard](#keyboard)
  - [SSD](#ssd)
  - [Bluetooth](#bluetooth)
  - [Trackpad-Trackpoint](#trackpad-trackpoint)
  - [Wireless-Card](#wireless-card)
  - [Integrated-Camera](#integrated-camera)
  - [Thunderbolt 3](#thunderbolt-3)
  - [Headphone/mic combo](#headphonemic-combo)   

  - [SD Card reader](#sd-card-reader)
- [What-is-not-working](#what-is-not-working)
- [Recommended-BIOS-Config](#recommended-bios-config)
- [Questions-and-Issues](#questions-and-issues)
- [Hibernation](#hibernation)
- [Support](#support)
- [Credits](#credits)

## Device Information
| Specifications | Details |
|:---|:---|
| Computer Model | ThinkPad X390 |
| CPU | Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz |
| Model |  Lenevo 20Q1|
| Displayer | Lenevo LEN4094 ( 13.3 inch  ) |
| Memory | 8 GB ( 1x8 Samsung DDR4 2400 MHz ) |
| NVMe SSD | NVME WD Blue SN570 256GB |
| Integrated Graphics | Intel UHD Graphics 620 (Mobile) |
| Ethernet |  Intel(R) Ethernet Connection (6) I219-V |
| Sound Card | Intel Intel Smart Sound Technology Audio Controller (layout-id: 11) |
| Wireless Card |  Intel(R) Wireless-AC 9560 160MHz |
| I/O |  2xUSB3.1, USB-C Thunderbolt 3, MicroSD card reader, HDMI 1.4, Headphone/mic combo |


## Usage

If you have the same computer as me, you just need to replace your EFI with the EFI in the current directory. Don't forget to update your serial via GenSMBIOS

## Detailed-Device-Drivers

## CPU

Functioning normally. Patched with CPUFriend.kext: 1.6 GHz (Min) - 3.9 GHz(Max)

#### Battery

The power display is functioning normally.

#### USB

USB Ports Patching with USBMap.kext.

#### Ethernet

Functioning normally.

#### Display

Built-in HDMI dosent work, Thunderbolt port works and is attached with `Intel UHD Graphics 630` and is functioning normally. `2K@60Hz` & `4K@30Hz` are supported. Fixes coming soon

#### Audio

Driven by AppleALC with `layout-id: 90`. Everything is working normally. Support Dolby Audio.

#### Keyboard

Functioning normally except the <kbd>Insert</kbd> , which is not presented on Magic Keyboard.

#### SSD

NVMe is functioning normally.

#### Bluetooth

Bluetooth functioning partially (Successfully connected to AirPods but failed on iPhone)

#### Trackpad-Trackpoint

Functioning normally.

#### Wireless-Card

AirportItlwm works normally via OCLP root patch, thanks OC-simplify

#### Integrated-Camera

Functioning normally.

#### Thunderbolt 3

Functioning normally.
Tested with USB-C hub works fine

#### Headphone/mic combo

Functioning normally.

#### SD Card reader

Works properly

## What-is-not-working

- Biometrics not working(T2 security chip required)

## Recommended-BIOS-Config

- Security
  - Intel SGX: Software Controlled
- Boot
  - Boot Mode: UEFI Only (CSM Yes) 

### Hibernation

Hibernation is supported. No serious issue found after wake-up. However for some reason, the headphone jack audio become weird. If this didn't happen to you then you are lucky then

## Support
**Ventura**
- 13.x
**Sonoma**
- 14.x
**Sequoia**
- 15.x

## Credits
- [@mendax1234](https://github.com/mendax1234) for [ThinkpadX390-Opencore-EFI](https://github.com/mendax1234/ThinkpadX390-Opencore-EFI)
- [@VGEAREN](https://github.com/VGEAREN) for [Lenovo-X390-Big-Sur-OC-EFI](https://github.com/VGEAREN/Lenovo-X390-Big-Sur-OC-EFI)
- [@bayukp](https://github.com/bayukp) for [Thinkpad-X390-Opencore](https://github.com/bayukp/Thinkpad-X390-Opencore)
- [@mahronid](https://github.com/mahronid) for [thinkpad-x390-hackintosh](https://github.com/mahronid/thinkpad-x390-hackintosh)
- [@ayaya114514](https://github.com/ayaya114514) for [thinkpad-X390-hackintosh](https://github.com/ayaya114514/thinkpad-X390-hackintosh)
