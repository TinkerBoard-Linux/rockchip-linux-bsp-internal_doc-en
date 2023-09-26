# RK3399 Linux5.10 SDK Release Note

---

**Versions**

[TOC]

---
## rk3399_linux5.10_release_v1.3.0_20230920.xml Note

1 **Update Debian**

- Optimize Debian's Cheese app

1) Fixed a loop issue when the Cheese camera was turned on for recording and then turned off again
2) Add H264 encoding support, as Cheese only supports VP8 encoding by default, but many RK chips have weak or unsupported VP8 encoding So by default, support for H264 encoding is added

- Update Xserver

1) Filtering Mali DDK does not support GBM_FORMAT_R8 error issue
2) Fix the issue of the menu bar sliding and getting stuck on the top left side of the Xfce desktop
3) Fix the issue of abnormal rotation function after opening the anti tearing FlipFB

- Update rkwifibt with new script processing for more complete functionality and compatibility

- Update Chromium x11 version from 91.0.4472.164 to 111.0.5563.147

1) Drop is_official_build=false GN arg for optimization
2) Support HEVC (H265)
3) Enable VEA
4) Support AV1 in V4L2 VDA

2 **Update Buildroot**

- Update Buildroot Launcher and add status bar for configuration
- Weston adds features for closing services and restarting display services
- Increase support for ubifs size setting
- Add the archives directory structure and preset some download packages in advance
- Update lvgl_demo
- Update components (glmark2\glibc\wayland\weston...)

3 **Update Yocto**

- Implement automatic login serial port function
- Implement the automatic mounting function of USB peripherals
- Implement the automatic configuration function of wifibt

4 **Update rockit**

- update rockit version to v1.7.12

5 **Update libmali**

- Update libmali header file

6 **Update rkbin**

- Update RK3399 BL32 to V2.11

1) Fix security vulnerabilities
2) Fix memory leaks.
3) Enable efuse dependent clock

7 **Update Kernel**

- use multicodecs instead simple card for rk3399 evb
- update rk3399-sapphire-excavator-lp4-linux.dts
- Enable RT5651 for rk3399 excavator evb

8 **Update tools**

- Update SD tool to V1.76

1) Fix using empty misc size greater than 64k, SD card upgrade tool may have write errors.

- Update RKDevTool to V3.19
- Update window upgrade_tool to V2.23
- Update Rockchip_HdcpKey_Writer to V1.0.5

9 **Update documents**

- Update the SDK application process and instructions for using the Redmine system
- Update DDR related documents and integrate them into one development document
- Add Common/Secutiry document directory
- Add Rockit English documents
- Add RT performance related testing and performance analysis documents
- Add MCU_RGB and MIPI_DSI2  Display Development Document
- Update AVL/USB/PCIE/MMV/USB/NVM/SPI/PERF/WESTON/and other related development documents
- Update the relevant documents required for RK3588 release

10 **Update device/rockchip*

- Add `generate_logs` command is used to package log information.
- Compilation adds prompt SDK version information
- Default empty misc, go to resize partition in OS
- Support for clean module
- Yocto adds default desktop icon layout (synchronized with buildroot)
- Add some dependency checks and prompts for SDK compilation
- Fix AB partition packaging issue
- Fix issue with aarch64 precompiled tool not being able to use
- Yocto supports 3288w
- Ui partition supports automatic resizing
- Support command editing package file
- The yocto SDK supports automatic mounting of USB drives
- Default installation of rktoolkit for all SDKs
- Generate misc firmware from script at compile time
- Using a new wifibt script

## rk3399_linux5.10_release_v1.2.1_20230720.xml Note

1 **Update Debian**

- Filtering Mali DDK does not support GBM_FORMAT_R8 error issue
- Fix the issue of the menu bar sliding and getting stuck on the top left side of the Xfce desktop
- Fix the issue of abnormal rotation function after sretting FlipFB to always
- Add support for Cheese H264 encoding and default to using H264 encoding
- Update rkaiq to release v5.0x1.3
- Update mpp/gstreamer rockchip

2 **Update Buildroot**

- Update lvgl
- Update weston to suppor some issues
- Support pre-downloaded archives for download

3 **Update documents and tools**

- Upgrade pin_debug_tool to v1.12
- Upgrade programmer_image_tool to v1.26
- Upgrade SDDiskTool to v1.75
- Upgrade FactoryTool to v1.81
- update RKDevTool to v3.18
- Upgrade programming_image_tool to v1.26
- Upgrade Linux_Upgrade_Tool to v2.22
- Update the relevant documents required for RK3399 release

## rk3399_linux5.10_release_v1.2.0_20230620.xml Note

1 **Update device/rockchip**

- Fix Secureboot

2 **Update Debian**

- Update Blueman to resolve abnormal Bluetooth power management issues after sleep wake-up
- Update alsa to address audio issues after sleep wake-up
- Update mpp/gstreamer rockchip

3 **Update Buildroot**

- Resolve task - c command line exception issues
- Add Weston alpha channel support
- Add Gstreamer NV16_10LE40 format support
- Increase the use of domestic kgithub image sources for DL packages

4 **Update rkbin**

- Fixed sometime tool read efuse fail after efuse program

5 **Update Kernel**

- Update RK817/RK809 driver to address sleep wake-up issues

6 **Update documents and tools**

- Update Rockdev to resolve address resolution exceptions
- Update the relevant documents required for RK3399 release

## rk3399_linux5.10_release_v1.1.1_20230520.xml Note

The main update list is as follows:

1 **Update device/rockchip**

- buildroot/yocto installs Chinese fonts by default
- recovery does not install additional overlay
- Fixed hostname exception after dynamically switching rootfs
- Add dependency check and installation prompt
- Add repair owner permission
- Fix the problem that repeated compilation of yocto post-rootfs does not execute

2 **Update recovery**

- Repair press the recovery button to reset to enter the system, nothing is displayed
- U disk upgrade startup support
- Solve the problem that the first upgrade of the SD card starts abnormally
- Fix userdata partition unmount failure

3 **Update Debian**

- Solve the problem of cheese app recording screen freeze
- Support xfce4 power management configuration
- There are hidden problems in updating system permissions
- Update rkwifibt to solve problems related to switch or sleep wake-up
- Update adb to add some feature support
- Update mpp and gstreamer-rockchip
- Update rockchip-test to V2.1
- Solve the abnormal double-click problem of Debian desktop icons

4 **Update Buildroot**

- Add support for setting the location of Gstreamer glimagesink/xvimagesink plugin
- Fixed crash when Weston destroys dmabuf
- Add power/dictionary pen/sweeping machine and other product configurations
- Added support for external toolchains
- Add support for GCC8.X
- Fix the problem that the video source size may overflow after Gstreamer kmssink scaling
- Add Chromium 111.0.5563.147, support video H265 decoding
- Update Frecon, solve zoom and switch VT1 support
- Update rockit to v1.7.4
- Add support for lvgl demo

5 **Update rkbin**

- Fixed LP3 reboot error

6 **Update Kernel**

- Solve isp switch abnormal error
- RK3399 EDP low temperature power-on probability is not displayed, PLL lost lock
- System panic after opening KASAN with Logo buf non-PAGE aligned

7 **Update Uboot**

- fastboot: Burning more than 4G firmware causes the system to fail to start
- System panic after opening KASAN with Logo buf non-PAGE aligned

## rk3399_linux5.10_release_v1.1.0_20230420.xml Note

The main update list is as follows:

### SDK update main core component versions

- Kernel upgrade from 5.10.110 to 5.10.160
- Update Debian to 11.6
- Update Yocto to 4.0.9
- Update Buildroot to November 2021
- Weston updated to 11.0.1
- Gstreamer updated to 1.22

### SDK optimization and adjustment

- Reconstruct SDK configuration compilation mechanism
- Adjusting the compilation mechanism of the wifibt module
- Import a new version of Camera rkaiq to optimize its functionality and performance

### SDK New features

- Added Linux headers support, making it convenient for third-party applications without the need for kernel compilation and debugging
- Added yocto support for x11
- Added gst mpp support for av1
- Added gst mpp support for afbc encoding
- New support for OTA differential function
- Added adaptation support for libcamera

### SDK main fix issues

- Fix ubi format partition packaging and mounting issues
- Fix recovery mount partition exception
- Fixed the issue of resetting the time to 0 after standby wake-up
- Fix fiq debugger driver, serial port RX interference, resulting in system stuck
- Fixed a low probability of error after starting KASAN: KASAN: use after free in rga_ job_ next
- Support for addressing Weston touch related configurations
- Solve HDMI/MIPI plug and display issues
- Solve the problem of PDM recording channel confusion
- Resolve the issue of playback noise caused by RK809 · RK817-pdm recording
- Fixed LP3 reboot error
- Fixed single channel loop at "advanced training done"
- Fixed LP3 dbw detect bug

## rk3399_linux5.10_release_v1.0.0_20220920.xml Release Note

```
- The first release version
```
