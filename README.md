# pyserial_boot_time

## Environment:
- Local machine:
-   cygwin on Windows
-   Python 3.9.16
- Target machine:
  - Linux 5.4
  - U-boot 2019.04
  - Aspeed AST2600

## Introduction
This is used for Aspeed AST2600 board.
Measureing the boot up time for every boot stage.

- Initialization sequence:
  - FSBL: U-boot SPL
  - SSBL: U-Boot
  - Linux: kernel
  - init: Filesystem

### Expected output log_file contains:
FSBL:2.480000000039581s
SSBL:13.419999999983702s
Linux:5.599999999976717s
init:29.570000000006985s
Total time:51.070000000006985s

### Step 1: check the connected device name.
### Step 2: pexpect.expect() to read the specific values as beakpoints for boot up
