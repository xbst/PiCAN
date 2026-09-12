# PiCAN
[YouTube Video](https://youtu.be/SH-faxCCbi8)
![PCB](./Images/PCB.jpg)

A compact, USB drive shaped USB to CAN adapter, primarily intended for 3D printers running Klipper firmware.

## Purchasing a PiCAN
#### United States
[Isik's Tech Store](https://store.isiks.tech/products/pican-usb-to-can-bus-adapter)
- [Amazon - Prime Shipping](https://www.amazon.com/Isiks-Tech-PiCAN-Adapter-Printers/dp/B0CGLC87S5?maas=maas_adg_67FD4409E83516E2C5BBA977580D0B6B_afap_abs&ref_=aa_maas&tag=maas)
- [West3D](https://west3d.com/products/pican-a-tiny-usb-to-can-bus-adapter-by-isikstech)
#### Canada
- [Amazon - Ships from the US](https://www.amazon.ca/dp/B0CGLC87S5)
#### European Union
- [Lab4450 - Portugal](https://lab4450.com/product/pican-usb-to-can-adapter/)
#### Australia
- [Unique Prints](https://uniqueprints.shop/shop/electronics-electrical/pcb/pican-usb-to-can-adaptor-for-klipper/)
- [DREMC](https://store.dremc.com.au/products/pican-usb-to-can-bus-adapter)

## Instructions
Depending on how you sourced your PiCAN, your PiCAN might already have the firmware pre-flashed (units sold by me are pre-flashed). If yours doesn't have the firmware or if you need/want to reflash it, you can follow the instructions below. 
<details>
  <summary>Firmware Flashing</summary>

1. Download the [firmware](https://github.com/bigtreetech/U2C/blob/master/firmware/U2C_V1_STM32F072.bin).
2. Connect the PiCAN to your PC while holding down the BOOT button on the PiCAN.
3. Download and install [STM32Cube Programmer](https://www.st.com/en/development-tools/stm32cubeprog.html). (Do not download the latest version, it is buggy)
4. Select `USB` on the selecor in top right of the program (below `Not connected`). Click the refresh button next to the port selector. Select `USB1` and click connect.
5. Click `+` next to `Device Memory`, and select `Open File`. Select the downloaded firmware file. Click `Download`. Firmware will be flashed.
</details>

Wire the CAN cables according to this diagram:
![Wiring](./Images/Wiring.png)

For Klipper CAN instructions, follow [the official Klipper docs](https://www.klipper3d.org/CANBUS.html).

**Make sure your Raspberry Pi and your CAN devices have the GNDs connected. If they are powered from the same source, they should already be connected. If unsure use your multimeter's continuity mode to test.**

## Notes
- Readme files in this repo may contain Amazon Associate, Aliexpress affiliate, PCBWay affiliate links. I make a comission on qualifying purchases.
- This project does not come with any warranty, if you choose to build/use a PCB manufactured using published files in this repository, you are doing this at your own risk!
- If you want to sell PCBs manufactured using published files in this repository, you are allowed to, and you will not owe me any royalties. **You cannot claim that I endorse the sale**. You can check the license file for more information. However, if you **wish** to give me a share you can sponsor me on [GitHub](https://github.com/sponsors/xbst), subscribe on [Patreon](https://l.isiks.tech/patreon) or [YouTube](https://l.isiks.tech/member).
