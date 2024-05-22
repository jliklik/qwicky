Following along this tutorial: https://www.youtube.com/watch?v=t5phi3nT8OU

Ethernet PHY chip: https://www.digikey.ca/en/products/detail/microchip-technology/KSZ8081MLXIA/5049431
- LQFP so hopefully easier to solder?
- also tutorial with STM32 with KSZ8081: https://www.youtube.com/watch?v=Cj9AXikFMmM
   - LAN8742 uses same register commands as KSZ8081 to set up PHY
- https://youtu.be/Cj9AXikFMmM?si=nM6vmNc-t6WU_bas

Magnetics:
- https://electronics.stackexchange.com/questions/681489/ethernet-phy-colliding-with-itself / https://www.we-online.com/components/products/datasheet/74980111211.pdf
- https://andybrown.me.uk/2014/12/27/ksz8091rna/

Decoupling capacitors required for MCU VDD inputs:
- https://www.protoexpress.com/blog/decoupling-capacitor-use/

Options:
- KSZ8081MLX - [Microchip] - Only supports MII
- KSZ8081RN - [Microchip] - Supports RMII, but no LQFP option
- KSZ8721B - [Micrel] bad datasheet, but has SSOP pattern
- DP83848 = [TI] good datasheet, LQFP-48 (STM32 eval board uses this! (but with an external oscillator))
   - people say this chip is old and power hungry https://forum.microchip.com/s/topic/a5C3l000000MRYDEA4/t335965

- KSZ8001L - [Microchip] good datasheet, LQFP-48, used by Beckhoff! (https://download.beckhoff.com/download/document/io/ethercat-development-products/an_phy_selection_guidev2.6.pdf)

Wiring RMII:
These two complement each other:
- https://www.ti.com/lit/an/snla076a/snla076a.pdf?ts=1708225671535&ref_url=https%253A%252F%252Fwww.google.com%252F#:~:text=The%20RMII%20does%20not%20provide,logically%20AND%20this%20with%20TX_EN.
- https://ww1.microchip.com/downloads/en/DeviceDoc/KSZ8001L-S-Data-Sheet-DS00003062A.pdf

Hmmm RMII needs 50Mhz
- https://community.st.com/t5/stm32-mcus-products/stm32f4-rmii-eth-external-clock-source/td-p/549453#:~:text=''In%20RMII%20mode%20the,''
- unless we use the LAN8720 (24 pin VQFN)?
- But geez this is hard to solder
- LAN8740 (32 pin VQFN)

LAN8720:
- https://electronics.stackexchange.com/questions/350088/stm32f407-lan8720a-lwip-freertos-no-received-ethernet-frames
- https://pcbartists.com/design/embedded/esp32-ethernet-phy-schematic-design/

Display:
- https://www.digikey.ca/en/products/detail/sharp-microelectronics/LS013B7DH03/5300387
- https://www.digikey.ca/en/products/detail/adafruit-industries-llc/3502/7386264 (Adafruit version of SHARP, twice as expensive :< )

TODO:
- add GPIO for keyboard switches
