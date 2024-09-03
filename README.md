# HTML_Accelerator
 A funcitoning version of the fictional PCIE card

Modeled after: https://twitter.com/_Ninji/status/1317197426449633281


# Signal Chain (new):
1. PCIE 1x (16x size)connection to PC  
2. 1x MCS9990 PCIE to USB2.0 port host controller  https://www.aliexpress.us/item/3256803035586571.html
3. 4x Alcor Micro AU6438BS USB to flash reader (order 2, make sure to choose 6438BS https://www.aliexpress.us/item/3256804567088275.html) (backup order 50x here https://www.aliexpress.us/item/2251832667577487.html)  
4. 4x Flash storage iC mimic card inserted to reader  

# Signal Chain (old):
1. PCIE 1x (16x size)connection to PC  
2. 1x VIA Technolgies VT6212 PCI USB2.0 4 port Host controller  https://www.aliexpress.us/item/2251832638752642.html  
2.5 (if using VT6212, need PCI to PCIE reversable interface iC
2b. 1x MCS9990 PCIE to USB2.0 port host controller  https://www.aliexpress.us/item/3256803035586571.html
3. 4x Alcor Micro AU6438BS USB to flash reader (order 2, make sure to choose 6438BS https://www.aliexpress.us/item/3256804567088275.html) (backup order 50x here https://www.aliexpress.us/item/2251832667577487.html)  
4. 4x Flash storage iC mimic card inserted to reader  

## Flash storage options (see readyboost notes below)
1.70ea 1gb https://www.arrow.com/en/products/mx30lf1g28ad-ti/macronix-international

## 40x40 mm black heat sink with tape
- 1.42 ea https://www.aliexpress.us/item/2251832401116531.html  
- 1.23 ea 10pack https://www.aliexpress.us/item/2251832640943503.html  
- 2.68 ea 5pk https://www.aliexpress.us/item/2251832494702724.html  
- 3.92 ea https://www.digikey.com/en/products/detail/t-global-technology/TGH-0380-03/13682115  

## PCIE 12cm full height bracket and screws
- 10.89 for 5 (mesh) https://www.aliexpress.us/item/3256804202694680.html  
- 15.83 for 5 (solid) https://www.aliexpress.us/item/3256803817602223.html  
- 10.1 for 5 mesh https://www.ebay.com/itm/374654311256  


# Notes:
VT6212 reference PCB for PCIE to USB card:  
https://www.aliexpress.us/item/3256803148283309.html
https://www.startech.com/en-us/cards-adapters/pexusb4dp

AU6438 USB to EMMC reader pcb for reference:  
https://www.aliexpress.us/item/3256805090449780.html
with schematic: https://www.pcbway.com/project/shareproject/USB_flash_drive_AU6438.html  

PCIE pinout:  
https://pinoutguide.com/Slots/pci_express_pinout.shtml

## Windows Readyboost info:
https://en.wikipedia.org/wiki/ReadyBoost  
- Must be at least 256MB  storage  
- Access time of 1ms or less  
- 2.5MB/s read 4kb rand  
- 1.75MB/s write 512kb rand  

## Order from:
dimensions 110mm X 140mm  
1.6mm thick FR4  
blue  
5/5mil trace space  
min hole size 0.25mm  
edge connector, 20* bevel, ENIG 1u"  
1oz copper  
PCBway 75$ with shipping https://www.pcbway.com/orderonline.aspx  
JLC PCB 55$ with shipping https://cart.jlcpcb.com/quote?orderType=1&stencilLayer=2&stencilWidth=100&stencilLength=100  

## Todo:
1. Wire up PCIE connection
2. Power Supplies & Decoupling caps
3. Wire up USB connection #1
4. Wire up USB connection #2,3,4

https://docs.kicad.org/7.0/en/eeschema/eeschema.html#hierarchical-schematics

USB pullup 1.5k on D+ for high speed conneciton (maybe in chip already)