# SSD_Smilulator
An SSD firmware simulator for debug and test the SSD firmware.

本项目用于固态硬盘（SSD）固件Firmware代码的开发和调试。

## 项目介绍
本项目由三部分组成，Firmware，Simulator和Test Program。

Firmware是固件原生代码，尽量不做修改，只用于被Simulator程序调用。

Simulator是模拟器部分，用于模拟SSD硬件，例如Nand，Dram，FIFO，中断这些硬件资源。

Test Program包含一些测试case，用于对Firmware进行测试。

## 环境要求
* 支持多平台开发Windows，Mac，Linux
* 使用Codeblocks作为前台调试工具，GDB进行编译。
* 内存推荐使用大内存，最低内存要求为8G，32G或者64G更佳。

## Firmware
被测试的Firmware代码，最好做好分层，将硬件资源使用HAL层进行包装，方便移植和模拟。

## Simulator
对SSD硬件环境进行模拟，Nand，中断，DRAM，FIFO。使Firmware code可以运行在模拟环境中，方便调试。

## Test Program
使用测试Case对Firmware code进行测试。
