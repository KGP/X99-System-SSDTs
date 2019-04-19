
# X99-System-SSDTs

## Instructions

This X99 System SSDT Github repository constitutes a set of motherboard and PCIe-Slot specific system SSDTs for the ASUS X99-A II. Users of different motherboards and/or different PCIe-Slot populations have to adopt at least the ACPI path and ACPI replacments implemented in each specfic file. 

How to do so, is explained wihtin this small and basic guideline:
http://kgp-hackintosh-corner.com/how-to-create-or-modify-a-simple-system-ssdt-aml-by-means-of-dsdt-and-ioreg-acpi-information
 
## SSDTs

Collection of X99 System `SSDTs` for the ASUS X99-A II.

| AML File | Description |
| :------- | :---------- |
| `SSDT-X99-HDEF.aml` | On-board Realtek ALC 1150 Audio controller HDEF PCI implementation |
| `SSDT-X99-ANS1.aml` | On-board NVME controller ANS1 PCI implementation |
| `SSDT-X99-SAT1.aml` | On-board AHCI SATA controller SAT1 PCI implementation |
| `SSDT-X99-EVSS.aml` | On-board AHCI SATA controller EVSS PCI implementation |
| `SSDT-X99-USBX.aml` | Fixes USB Power Errors during system boot |
| `SSDT-X99-XHCI.aml` | Intel X99-A II Chipset USB3.0 extensible Host Controller XHCI PCI implementation |
| `SSDT-X99-XHC.aml` | On-board ASMedia ASM1142 USB 3.1 Type-A & Type-C extensible Host Controller XHC2 PCI implementation |
| `SSDT-X99-ETH0.aml` | On-board Intel i218-V 1GB NIC controlller ETH0 PCI implementation |
| `SSDT-X99-Vega-Frontier.aml` | AMD Radeon RX Vega Frontier PCIe Slot-1 GFX0 and HDAU PCI implementation |
| `SSDT-X99-Vega64.aml` | AMD Radeon RX Vega 64 PCIe Slot-1 GFX0 and HDAU PCI implementation (Sapphire Nitro+ RX Vega 64)  |
| `SSDT-X99-Vega56.aml` | AMD Radeon RX Vega 56 PCIe Slot-1 GFX0 and HDAU PCI implementation (MSI RX VEGA 56 Air Boost OC |
| `SSDT-X99-RX580.aml` | AMD Radeon RX 580 PCIe Slot-1 GFX0 and HDAU PCI implementation |
| `SSDT-X99-RX560.aml` | AMD Radeon RX 560 PCIe Slot-1 GFX0 and HDAU PCI implementation |
| `SSDT-X99-Radeon-VII.aml` | AMD Radeon VII PCIe Slot-1 GFX0 and HDAU PCI implementation for use with modified Whatevergreen Source Code distrubution also considering Radeon VII|
| `SSDT-X99-Nvidia.aml` | Nvidia PCIe Slot-1 GFX0 and HDAU PCI implementation |
| `SSDT-X99-ARPT.aml` | OSXWIFI Broadcom BCM94360CD BT/WIFI PCIe Slot-5 ARPT PCI implementation |
| `SSDT-X99-TB3HP.aml` | GC-Titan Ridge/GC-Alpine Ridge/ASUS TBEX 3 TB3/USB-C Hotplug Injector Slot-4 PCI implementation |
| `SSDT-X99-ACQU.aml` | Acquantia AQC107-AFW 10GB NIC PCIe Slot-6 XGBE PCI implementation |
| `SSDT-X99-X540-T1.aml` | Intel X540-T1 10GB NIC PCIe Slot-6 XGBE PCI implementation |
| `SSDT-X99-P2EI0G-2T.aml` | Small-Tree P2EI0G-2T 10GB NIC PCIe Slot-6 XGBE and XGBF PCI implementations |
| `SSDT-DTPG.aml` | DTPG PCI implementation (required for all `SSDTs` listed above) |

## Required Patches

The `SSDTs` above require the following `config.plist` ACPI DSDT patch replacements.

| Comment | Find [HEX] | Replace [Hex] |
| :------ | :--------- | :----------- |
| `_OSI` &rarr; `XOSI` | `5F4F5349` | `584F5349` |
| `EC0_` &rarr; `EC__` | `4543305F` | `45435F5F` |
| `H_EC` &rarr; `EC__` | `485F4543` | `45435F5F` |
| `HEC1` &rarr; `IMEI` | `48454331` | `494D4549` |
| `IDER` &rarr; `MEID` | `49444552` | `4D454944` |
| `LPC0` &rarr; `LPCB` | `4C504330` | `4C504342` |
| `FPU_` &rarr; `MATH` | `4650555F` | `4D415448` |
| `TMR_` &rarr; `TIMR` | `544D525F` | `54494D52` |
| `PIC_` &rarr; `IPIC` | `5049435F` | `49504943` |
| `_DSM` &rarr; `XDSM` | `5F44534D` | `5844534D` |

## Acknowledgements

Special thanks to Apfelnico and NMano for all substantial and always kind contributions.

Partial contributions of Mork vom Ork, Matthew82, Maleorderbridge, TheRacerMaster, Crismac2013 and LeleTuratti to `SSDT-X299-TB3HP.aml` might also be mentioned in addition.
