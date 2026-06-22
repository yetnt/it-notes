# Start-up and boot software pg 37

When the computer is switched on, and before the OS is loaded, the hardware devices that will be used need to be checked.

Once they are deemed to be correct, the OS on the main drive gets loaded in RAM together with drivers for the hardware devices.

A **_`boot sequence`_** is the initial set of operations that the computer performs when it's turned on.

The program that performs the boot sequence and ends in the entire OS being loaded is the **_`boot loader`_** (or **_`bootstrap loader`_**)

## BIOS

The **B**asic **I**nput **O**utput **S**ystem is low-level software that lives in a non-volatile ROM chip on the motherboard.

Software that lives on the ROM permanently is known as **_`Firmware`_**

When the computer turns on the following happens

```mermaid
---
title: Process that the BIOS follows
---
graph TD;

    bios[[BIOS]]
    post[Power-On Self-Test]
    cmos[[CMOS]]
    test[Test]
    mbr[["Master Boot Record(MBR)"]]

    bios -->|begins| post
    post -->|An inventory of hardware is connected, obtained from the|cmos
    cmos -->|runs tests to determine if its functioning properly| test
    test -->|bios locates| mbr


```

-   MBR - **M**aster **B**oot **R**ecord, which is a seciton of code usually stored on the hard disk drive. Its responsible for loading and exeucting the OS's **[`kernel`](#kernel)** which continues the start up procedure

### Kernel

The core of the computer's OS which remains in RAM. It's responsible for I/O requests from software, translating them into instructions for the CPU. It also handles memory and peripherals like keyboards, monitors, printers and speakers.

## CMOS

**C**omplementary **M**etal-**O**xide **S**emiconductor
A battery-backed, volatile memory that stores:

-   hardware settings
-   user settings

CMOS is referred to by the BIOS in the boot up process to obtain data about the system.

CMOS memory needs to be volatile since users can install different hardware devices and change user settings.

## UEFI

**U**nified **E**xtended **F**irmware **I**nterface is also low-level firmware
which is a faster more efficient system than BIOS.

UEFI supports BIOS emulation for older PCs, but you cannot switch from BIOS
to UEFI on an existing PC, you'd need a new one.

Advantages:

- UEFI firmware can boot from drives of 2.2TB or larger
- UEFI can run in 32-bit mode or 64-bit mode which has more address space
than BIOS; meaning that the boot process is faster.
- UEFI setup screens are more user-friendly than BIOS, featuring graphics and 
mouse cursor support.

Other features:

- Supports Secure Boot. (validity to ensure no malware has tampered with the
boot process)
- Support networking features right into the UEFI firmware itself, aiding in
remote troubleshooting and config.
- UEFi is more than a BIOS replacement, it's a tiny operating system
that runs on top of a computer's firmware and can do alot more than BIOS
- It may be stored in flash memory on the motherboard or it may be loaded from
a hard drive or network share at boot.

