# OpenWrt WHW03 (ASUS RT-ACRH17) Patches

Local patches for IPQ4019 WHW03 hardware on top of OpenWrt 24.10.

## Changes

- **Kernel config**: Enable CSR8811 Bluetooth (BT, BT_LE, RFCOMM, BNEP, HIDP, HCIUART) + RFKILL_FULL/GPIO/INPUT/LEDS
- **DTS whw03.dts**: Fix SD card pinmux (remove gpio32 from SD pins, add bus-width=4 + non-removable)
- **DTS whw03.dtsi**: Remove bluetooth-enable gpio-hog for CSR8811 recovery experiment (GPIO32 VREG_EN_RST# driven from userspace)
- **generic.mk**: Fix WHW03 image entry

## Base

OpenWrt 24.10 branch, commit `25920e84` (kernel bump 6.6 to 6.6.144).
