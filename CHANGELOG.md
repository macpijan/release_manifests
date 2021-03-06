Change log for PC Engines binary releases
=========================================

This document contain changelog for binary releases that contain all below
components:

* [coreboot (with all required blobs)](https://github.com/pcengines/coreboot)
* [SeaBIOS](https://github.com/pcengines/seabios)
* [sortbootorder](https://github.com/pcengines/sortbootorder)
* [ipxe](https://github.com/pcengines/ipxe)
* [memtest86+](https://github.com/pcengines/memtest86plus)

To see recent changes for legacy and mainline branch:
* [Releases 4.0.x](#unreleased-40x) are based on PC Engines 20160304 release.
* [Releases 4.5.x](#unreleased-45x) are based on mainline support merged in
[this gerrit ref](https://review.coreboot.org/#/c/14138/).

## [Unreleased 4.5.x]
## [v4.5.5.2] - 2017-03-03
- [coreboot v4.5.5.2](https://github.com/pcengines/coreboot/blob/coreboot-4.5.x/CHANGELOG.md#v4552---2017-03-03)
- [SeaBIOS rel-1.10.0.1](https://github.com/pcengines/seabios/blob/coreboot-4.0.x/CHANGELOG.md#rel-11001---2017-02-23)
- [sortbootorder v4.5.4](https://github.com/pcengines/sortbootorder/blob/master/CHANGELOG.md#v454---2017-02-23)
- [ipxe v1.0.0](https://github.com/pcengines/ipxe)
- [memtest86+ v4.0.1](https://github.com/pcengines/memtest86plus/blob/coreboot-4.0.x/CHANGELOG.md#v401---2016-05-11)

### Changed
- (APU3 only) set GPIO33 as output/low by default

## [v4.5.5.1] - 2017-03-02
- [coreboot v4.5.5.1](https://github.com/pcengines/coreboot/blob/coreboot-4.5.x/CHANGELOG.md#v4551---2017-03-02)
- [SeaBIOS rel-1.10.0.1](https://github.com/pcengines/seabios/blob/coreboot-4.0.x/CHANGELOG.md#rel-11001---2017-02-23)
- [sortbootorder v4.5.4](https://github.com/pcengines/sortbootorder/blob/master/CHANGELOG.md#v454---2017-02-23)
- [ipxe v1.0.0](https://github.com/pcengines/ipxe)
- [memtest86+ v4.0.1](https://github.com/pcengines/memtest86plus/blob/coreboot-4.0.x/CHANGELOG.md#v401---2016-05-11)

### Changed
- (APU3 only) set GPIO33 as output/high by default

## [v4.5.5] - 2017-02-24
- [coreboot v4.5.5](https://github.com/pcengines/coreboot/blob/coreboot-4.5.x/CHANGELOG.md#v455---2017-02-24)
- [SeaBIOS rel-1.10.0.1](https://github.com/pcengines/seabios/blob/coreboot-4.0.x/CHANGELOG.md#rel-11001---2017-02-23)
- [sortbootorder v4.5.4](https://github.com/pcengines/sortbootorder/blob/master/CHANGELOG.md#v454---2017-02-23)
- [ipxe v1.0.0](https://github.com/pcengines/ipxe)
- [memtest86+ v4.0.1](https://github.com/pcengines/memtest86plus/blob/coreboot-4.0.x/CHANGELOG.md#v401---2016-05-11)

### Added

- sgabios video oprom is added by default (v.1.0.0 pcengines version)
- added setup option to turn on legacy console to serial redirect using sgabios

### Changed

- SeaBIOS up to 1.10.0.1
- sortbootorder up to 4.5.4
- coreboot rebased to the latest mainline
- removed setup option to disable serial console, as it was not working in
  mainline

### Fixed

- Asmedia ASM106x controllers work in the mPCIe1 slot
- Memory size shown during boot corrected in 2GB SKU devices

### Known issues

- Asmedia ASM106x controllers are not working in the mPCIe2 slot
- Some XHCI USB booting stability issues after soft-reset

## [v4.5.4] - 2017-01-24
- [coreboot v4.5.4](https://github.com/pcengines/coreboot/blob/coreboot-4.5.x/CHANGELOG.md#v454---2017-01-24)
- [SeaBIOS rel-1.9.2.4](https://github.com/pcengines/seabios/blob/coreboot-4.0.x/CHANGELOG.md#rel-1924---2016-01-23)
- [sortbootorder v4.5.3](https://github.com/pcengines/sortbootorder/blob/master/CHANGELOG.md#v453---2017-01-12)
- [ipxe v1.0.0](https://github.com/pcengines/ipxe)
- [memtest86+ v4.0.1](https://github.com/pcengines/memtest86plus/blob/coreboot-4.0.x/CHANGELOG.md#v401---2016-05-11)

## [v4.5.3]
### coreboot
#### Added
- support for legacy LEDs behavior
- legacy logs at boot
- 4k alignment for bootorder in CBFS

#### Changed
- enabled memtest86+ by default

#### Fixed
- incorrect GPIO implementation

### sortbootorder
#### Fixed
- problem with saving configuration

### SeaBIOS
#### Changed
- limit level 1 logs to minimum

## [v4.5.2]
### coreboot
#### Added
- port of clock settings from legacy implementation
- support for getting sku and serial number
- sortbootorder as secondary payload
- PXE ROM based on 2016.7 release

#### Changed
- log level to ALERT
- enable UART C and UART D by default

#### Fixed
OSes tested: Debian testing (Linux kernel 4.8) and Voyage Linux (APU2 image
builder)
- booting from start works fine (Seagete SSHD 1TB ST1000LM014)
- USB booting works fine (USB MSC Drive UFD 3.0 Silicon-Power16G 1100)
- iPXE works fine (tested with Debian netboot pxelinux.0)
- HDD warm and cold boot works (Seagete SSHD 1TB ST1000LM014)
- USB warm and cold boot works (USB MSC Drive UFD 3.0 Silicon-Power16G 1100)
- iPXE works fine (tested with Debian netboot pxelinux.0)

### sortbootorder
#### Fixed
- compilation fixes to build with mainline coreboot

## [v4.5.1]
#### Added
- mainline support for APU2

[Unreleased 4.5.x]: https://github.com/pcengines/coreboot/compare/v4.5.5.2...coreboot-4.5.x
[v4.5.5.2]: https://github.com/pcengines/coreboot/compare/v4.5.5.1...v4.5.5.2
[v4.5.5.1]: https://github.com/pcengines/coreboot/compare/v4.5.5...v4.5.5.1
[v4.5.5]: https://github.com/pcengines/coreboot/compare/v4.5.4...v4.5.5
[v4.5.4]: https://github.com/pcengines/coreboot/compare/v4.5.3...v4.5.4
[v4.5.3]: https://github.com/pcengines/coreboot/compare/v4.5.2...v4.5.3
[v4.5.2]: https://github.com/pcengines/coreboot/compare/v4.5.1...v4.5.2
[v4.5.1]: https://github.com/pcengines/coreboot/compare/65a9462a73bd9c5e1054ea315b51574b4bf2f270...v4.5.1
