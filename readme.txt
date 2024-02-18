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

KSZ8081MLX
- Does not support RMII!!
- Only supports MII 
- The KSZ8081RN supports RMII

KSZ8721B might be the way to go 
- support RMII and MII
- SSOP package so easy to solder
- https://www.digikey.ca/en/products/detail/microchip-technology/KSZ8721B/771457
- but have to design custom footprint


TODO:
- add ethernet/PHY chip
- add GPIO for keyboard switches
