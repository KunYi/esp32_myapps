# W32-ETH01 Test Project

This project demonstrates the Ethernet functionality on the W32-ETH01 development board using ESP-IDF framework.

## Hardware Requirements

- W32-ETH01 Development Board
  - LAN8720 Ethernet PHY (Address: 0x1)
  - Pin Configuration:
    - MDIO: IO18
    - MDC: IO23
    - EN_ETH_CLK: IO16

## Software Requirements

- Based on ESP-IDF examples/ethernet/B=basic
- ESP-IDF development framework

## Important Notes

- IO16 is used to enable the 50MHz clock required for Ethernet operation
- The project initializes the Ethernet PHY and establishes network connectivity


### Log Output
```
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:7176
load:0x40078000,len:15564
ho 0 tail 12 room 4
load:0x40080400,len:4
--- 0x40080400: _init at ??:?

load:0x40080404,len:3904
entry 0x40080640
I (31) boot: ESP-IDF v5.3.1 2nd stage bootloader
I (31) boot: compile time Dec  2 2024 16:09:32
I (31) boot: Multicore bootloader
I (35) boot: chip revision: v3.1
I (39) boot.esp32: SPI Speed      : 40MHz
I (44) boot.esp32: SPI Mode       : DIO
I (48) boot.esp32: SPI Flash Size : 8MB
I (53) boot: Enabling RNG early entropy source...
I (58) boot: Partition Table:
I (62) boot: ## Label            Usage          Type ST Offset   Length
I (69) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (77) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (84) boot:  2 factory          factory app      00 00 00010000 00100000
I (92) boot: End of partition table
I (96) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=12d80h ( 77184) map
I (131) esp_image: segment 1: paddr=00022da8 vaddr=3ffb0000 size=02494h (  9364) load
I (134) esp_image: segment 2: paddr=00025244 vaddr=40080000 size=0add4h ( 44500) load
I (154) esp_image: segment 3: paddr=00030020 vaddr=400d0020 size=31188h (201096) map
I (223) esp_image: segment 4: paddr=000611b0 vaddr=4008add4 size=02a58h ( 10840) load
I (235) boot: Loaded app from partition at offset 0x10000
I (235) boot: Disabling RNG early entropy source...
I (247) cpu_start: Multicore app
I (255) cpu_start: Pro cpu start user code
I (255) cpu_start: cpu freq: 160000000 Hz
I (255) app_init: Application information:
I (258) app_init: Project name:     ethernet_basic
I (263) app_init: App version:      4fd7f1e
I (268) app_init: Compile time:     Dec  2 2024 16:09:27
I (274) app_init: ELF file SHA256:  55569087c...
I (280) app_init: ESP-IDF:          v5.3.1
I (284) efuse_init: Min chip rev:     v0.0
I (289) efuse_init: Max chip rev:     v3.99
I (294) efuse_init: Chip rev:         v3.1
I (299) heap_init: Initializing. RAM available for dynamic allocation:
I (306) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (312) heap_init: At 3FFB3768 len 0002C898 (178 KiB): DRAM
I (318) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (325) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (331) heap_init: At 4008D82C len 000127D4 (73 KiB): IRAM
I (339) spi_flash: detected chip: generic
I (342) spi_flash: flash io: dio
I (347) main_task: Started on CPU0
I (357) main_task: Calling app_main()
I (357) gpio: GPIO[16]| InputEn: 0| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0
I (1377) esp_eth.netif.netif_glue: ac:15:18:e9:f1:fb
I (1377) esp_eth.netif.netif_glue: ethernet attached to netif
I (2877) eth_example: Ethernet Started
I (2877) main_task: Returned from app_main()
I (2877) eth_example: Ethernet Link Up
I (2877) eth_example: Ethernet HW Addr ac:15:18:e9:f1:fb
I (4877) eth_example: Ethernet Link Down
I (6877) eth_example: Ethernet Link Up
I (6877) eth_example: Ethernet HW Addr ac:15:18:e9:f1:fb
I (8877) eth_example: Ethernet Link Down
I (16877) eth_example: Ethernet Link Up
I (16877) eth_example: Ethernet HW Addr ac:15:18:e9:f1:fb
I (18877) eth_example: Ethernet Link Down
I (24877) eth_example: Ethernet Link Up
I (24877) eth_example: Ethernet HW Addr ac:15:18:e9:f1:fb
I (26877) eth_example: Ethernet Link Down
I (32877) eth_example: Ethernet Link Up
I (32877) eth_example: Ethernet HW Addr ac:15:18:e9:f1:fb
I (33877) esp_netif_handlers: eth ip: 10.42.0.227, mask: 255.255.255.0, gw: 10.42.0.1
I (33877) eth_example: Ethernet Got IP Address
I (33877) eth_example: ~~~~~~~~~~~
I (33877) eth_example: ETHIP:10.42.0.227
I (33887) eth_example: ETHMASK:255.255.255.0
I (33887) eth_example: ETHGW:10.42.0.1
I (33897) eth_example: ~~~~~~~~~~~
I (42877) eth_example: Ethernet Link Down
I (48877) eth_example: Ethernet Link Up
```

## Pin Configuration Details

| Function    | GPIO Pin |
|------------|----------|
| MDIO       | IO18     |
| MDC        | IO23     |
| EN_ETH_CLK | IO16     |

## References

- [Unofficial guide to the WT32-ETH01](https://github.com/egnor/wt32-eth01)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
