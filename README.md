Device Details:
K26C SOM

Approach:
Need to Convert some or all of this code to baremetal PS code
Want to first enable a few very specific settings first, then we will work on making this library a bit general

## Milestone 1

### Only Enable Encode Block

#### Requirements
- **Send Task List to MCU**
  - h.265
  - 15 Mbps
  - Other settings will be taken care of later
- **Service Interrupts on APU**
      



# VCU Control Software Source Code

## Overview

The VCU control software can be used in two ways:
- As a standalone command-line executable (details provided below).
- As a library, with entry points available in `lib_encode` and `lib_decode`.

## Libraries

### `customers`
This library allows for modification of build options, such as enabling traces, via the `config.h` file.

### `lib_app`
Miscellaneous C++ utilities.

### `lib_cfg`
C++ utilities for configuration file parsing.

### `lib_conv_yuv`
C++ utilities for YUV conversion helpers for the encoder (makes use of `lib_app`).

### `lib_preprocess`
Handles QP table management.

### `lib_rtos`
Wrapper around OS synchronization primitives.

### `lib_common`
Miscellaneous C utilities.

### `lib_common_*`
Contains structures used for communication with the firmware.

### `lib_bitstream`
High-level syntax bitstream generation, such as headers.

### `lib_encode`
Entry point for the encoding library.

### `lib_decode`
Entry point for the decoding library.

### `lib_parsing`
Contains codec specifications relevant to the decoder (HLS, DPB, etc.).

### `lib_fpga`
Handles communication with the hardware, including reading/writing registers and handling IRQs.

### `lib_ip_ctrl`
Interface for controlling the codec.

## User Manual

For more detailed information, refer to the Xilinx product guide document: **PG252 H.264/H.265 Video Codec Unit Product Guide**.


