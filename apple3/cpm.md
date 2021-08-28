---
title: "CP/M on the Apple ///"
author: "Kirk Jackson"

---

CP/M was an operating system created by Gary Kildall during 1974, and during the 1970's and early 80's was a prominent operating system for Intel 8080 and Z80-based micro-computers.

After the Apple II was released Microsoft created a Z-80 SoftCard, and it successfully let business users run their CP/M applications on the Apple II.[^softcard] The SoftCard included a Z-80 CPU and when running CP/M the Z-80 took over the operation of the computer from the 6502.

Microsoft later released an Apple III version called the SoftCard III. This provided similar ability to run CP/M programs on a Z-80 coprocessor.

As-of August 2021, Joe's Computer Museum is selling a [SoftCard III Reproduction](https://jcm-1.com/product/softcard-iii-reproduction/).

[^softcard]: See [Z-80 SoftCard on Wikipedia](https://en.wikipedia.org/wiki/Z-80_SoftCard), [Coprocessors on a2history.org](https://apple2history.org/history/ah13/#07)

## Using CP/M

Apple included 4 manuals with the SoftCard III product:

- [Apple III - SoftCard III Installation and Operation Manual](Apple_III_Softcard_III_Installation_and_Operation_Manual.pdf) ([archive.org](https://archive.org/details/Apple_III_Softcard_III_Installation_and_Operation_Manual.PDF))
- [Apple III - Microsoft BASIC Reference Manual](Apple_III_Microsoft_BASIC_Reference_Manual_(CP-M).pdf) ([apple3.org](https://www.apple3.org/iiimanuals.html#cpm))
- Osborne CP/M User Guide ([archive.org](https://archive.org/details/osborne-cpm-users-guide_2nd-ed))
- [Apple III - The CP/M Reference Manual](Apple_III_CP-M_Reference_Manual.pdf) ([apple3.org](https://www.apple3.org/iiimanuals.html#cpm))


There were some III-specific quirks to setting up and using CP/M, and the Installation and Operation Manual detailed those differences. The other three manuals are general CP/M and BASIC references.

### CP/M Boot

To check that your SoftCard is installed properly, you can boot from the CP/M Master disk:

- [Apple SoftCard III CP/M Master](APPLEIIICPM.DSK) ([apple3.org](https://www.apple3.org/iiisoftware.html#os) [asimov](https://mirrors.apple2.org.za/ftp.apple.asimov.net/images/apple3/system/os/Apple%20Softcard%20III%20CPM%20Master%20Diskette%20%28076-0002%29%20Apple%201982.dsk))

If the disk boots into CP/M successfully, then your SoftCard works!

The Apple III requires you to boot from the built-in drive, and the same rule applies for using CP/M. 

### CP/M Setup

The Apple III's SOS requires drivers to be loaded on the boot disk in order to access each device. This is different to the behaviour of the Apple II, and more like modern operating systems.

Getting the drivers onto your CP/M boot disk is... quirky. You need to follow the following steps:

1. Use the SOS System Configuration Program (SCP) to create a regular SOS boot disk with the drivers you need.
2. Boot into CP/M and use `SOSXFER` to copy the drivers from your SOS boot disk to your CP/M boot disk.
3. Run the `CONFIG` program to map the SOS devices to CP/M devices.
4. Reboot

