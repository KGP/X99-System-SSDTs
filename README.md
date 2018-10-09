# X99-System-SSDTs

# Collection of X99 System SSDTs for ASUS X99-A II:

SSDT-X99-HDEF.aml: onboard Realtek ALC 1150 Audio Controller HDEF PCI implementation

SSDT-X99-ANS1.aml: onboard NVME controller ANS1 PCI implementation

SSDT-X99-SAT1.aml: onboard AHCI SATA controller SAT1 PCI implementation

SSDT-X99-EVSS.aml: onboard AHCI SATA Controller EVSS PCI implementation

SSDT-X99-USBX.aml: Fixing USB Power Errors on system boot

SSDT-X99-XHCI.aml: onboard Intel X99-A II Chipset USB3.0 extensible Host Controller XHCI PCI implementations

SSDT-X99-XHC2.aml: onboard ASMedia ASM1142 USB 3.1 Type-A & Type-C extensible Host Controller XHC2 PCI implementations

SSDT-X99-ETH0.aml: onboard Intel i218-V 1GB NIC controlller ETH0 PCI implementation

SSDT-X99-Vega.aml: RX Radeon Vega 64 PCIe Slot-1 GFX0 and HDAU PCI implementation

SSDT-X99-Nvidia.aml: Nvidia PCIe Slot-1 GFX0 and HDAU PCI implementation

SSDT-X99-TB3HP: TB3/USB-C Hotplug Injector Slot-4 PCI implementation

SSDT-X99-ARPT.aml: OSXWIFI Broadcom BCM94360CD BT/WIFI PCIe Slot-5 ARPT PCI implementation

SSDT-X99-ACQU.aml: Acquantia AQC107-AFW 10GB NIC PCIe Slot-6 XGBE PCI implementation

SSDT-X99-X540-T1.aml: Intel X540-T1 10GB NIC PCIe Slot-6 XGBE PCI implementation

SSDT-X99-P2EI0G-2T.aml: Small-Tree P2EI0G-2T 10GB NIC PCIe Slot-6 XGBE and XGBF PCI implementations

SSDT-DTPG.aml: DTPG PCI implementation (required for all SSDTs listed above)


# Set of X99-SSDTS requires the following config.plist ACPI DSDT patch replacements:

Comment: / Find*[HEX] / Replace[Hex]

_OSI -> XOSI / 5F4F5349 / 584F5349

EC0_ -> EC__ / 4543305F / 45435F5F

H_EC -> EC__ / 485F4543 / 45435F5F

HEC1 -> IMEI / 48454331 / 494D4549

IDER -> MEID / 49444552 / 4D454944

LPC0 -> LPCB / 4C504330 / 4C504342

FPU_ -> MATH / 4650555F / 4D415448

TMR_ -> TIMR / 544D525F / 54494D52

PIC_ -> IPIC / 5049435F / 49504943

_DSM -> XDSM / 5F44534D / 5844534D


# Acknowledgements: 

Special thanks to Apfelnico and NMano for all substantial and always kind contributions. 

Partial contributions of Mork vom Ork, Matthew82, Maleorderbridge, TheRacerMaster, Crismac2013 and LeleTuratti to SSDT-X99-TB3HP.aml might also be mentioned in addition.
