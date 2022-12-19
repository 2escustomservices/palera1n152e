# 
![palera1n-Header](https://user-images.githubusercontent.com/104146035/204871654-854b47a5-866b-41e1-aaab-8059cbfc4b9a.jpg)






# This is a work in progress. by [pwnd2e@Twitter](https://twitter.com/pwnd2e) for this modified version of [palera1n](https://github.com/palera1n/palera1n)
Read this throughly, feel free to ask questions, know the risks. 

- 1. [open](https://discord.gg/5pWry9wn6p) Ask in r/jailbreak Discord #palera1n channel
- 2. [open](https://discord.gg/4S3yUMxuQH) Ask in palera1n Discord
- 3. [open](https://discord.gg/kKJmDDaZrB) Ask in 2escustomservices Discord #palera1n channel
- 4. Or open a GitHub issue

Please, please, please, provide necessary info:

- iOS version and device (eg. iPhone 7+ 15.1, iPhone 6s 15.3.1)
- Computer's OS and version (eg. Ubuntu 22.04, macOS 12.0 and up)
- The command you ran
- Debug logs with `--debug`



# palera1n

iOS 15.0-15.7.1 **work in progress, tethered** checkm8 "jailbreak" 

# What does this do?

It boots the device with AMFI patches. On first run, it'll boot a ramdisk which dumps your onboard blob, and installs Sileo and Substitute.

**WARNING 1**: I am NOT responsible for any data loss. The user of this program accepts responsibility should something happen to their device. While nothing should happen, jailbreaking has risks in itself. If your device is stuck in recovery, please run `futurerestore --exit-recovery`, or use `irecovery -n`. Using this on iOS 16 has a higher chance of bootlooping you.

On A10 and A11, you **must disable your passcode while in the jailbroken state**. On A10, this can be fixed in the future by implementing blackbird. On A11, we don't have a SEP exploit yet.

# Linux issues
Linux has some weird usbmuxd issues. We have tried our best to fix them, but there stil are issues. We highly recommend to compile and install [usbmuxd2](https://github.com/tihmstar/usbmuxd2).

Stop making issues about Linux not being able to connect, we are aware. This includes being stuck on waiting for ramdisk to finish booting.

# Prerequisites
- 1. checkm8 vulnerable iOS device on iOS 15 (A8X-A11)
    - You must install the Tips app from the App Store before running the script
- 2. Linux or macOS computer
    - Python 3 is required
- 3. iOS 15.0-15.7.1
- 4. A brain
    - Remember, this is mainly for developers.

# How to use
- 1. Clone this repo with `git clone --recursive https://github.com/2escustomservices/palera1n152e && cd palera1n152e`
    - \[A10+\] Before running, you **must** disable your passcode
    - Put your device in DFU Mode before running.
- 2. - For rootless Run `./palera1n.sh --tweaks <ios version youre on atm>`   
   _for fakefs run `./palera1n.sh --tweaks <ios version youre on atm> --semi-tethered` 
   - With semi-tether after first install and re-jailbreaking just hit activate tweaks then respring
- 3. Let it ra1n







# Repos
All repos work because it uses normal Procursus and not rootless.
- [pwnd2e](https://www.2escustomservices.com/iOS15) You can add this repo for tweaks that wont bork your idevice

# Credits


- [pwnd2e](https://github.com/pwnd2e) for this modified fork

- [Nathan](https://github.com/verygenericname)
    - The ramdisk that dumps blobs, copies files, and duplicates rootfs is a slimmed down version of [SSHRD_Script](https://github.com/verygenericname/SSHRD_Script)
    - For modified [restored_external](https://github.com/verygenericname/sshrd_SSHRD_Script)
    - Also helped Mineek getting the kernel up and running and with the patches
    - Helping with adding multiple device support
    - Fixing issues relating to camera.. etc by switching to fsboot
    - [iBoot64Patcher fork](https://github.com/verygenericname/iBoot64Patcher)
- [Mineek](https://github.com/mineek)
    - For the patching and booting commands
    - Adding tweak support
    - For patchfinders for RELEASE kernels
    - [Kernel15Patcher](https://github.com/mineek/PongoOS/tree/iOS15/checkra1n/Kernel15Patcher)
    - [Kernel64Patcher](https://github.com/mineek/Kernel64Patcher)
- [Amy](https://github.com/elihwyma) for the [Pogo](https://github.com/elihwyma/Pogo) app
- [checkra1n](https://github.com/checkra1n) for the base of the kpf
- [nyuszika7h](https://github.com/nyuszika7h) for the script to help get into DFU
- [the Procursus Team](https://github.com/ProcursusTeam) for the amazing [bootstrap](https://github.com/ProcursusTeam/Procursus)
- [F121](https://github.com/F121Live) for helping test
- [m1sta](https://github.com/m1stadev) for [pyimg4](https://github.com/m1stadev/PyIMG4)
