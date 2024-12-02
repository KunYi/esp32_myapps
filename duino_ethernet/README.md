# W32-ETH01 Arduino Ethernet Test Project

This project demonstrates the Ethernet functionality on the W32-ETH01 development board using Arduino framework for ESP32.

## Hardware Requirements

- W32-ETH01 Development Board
  - LAN8720 Ethernet PHY (Address: 0x1)
  - Pin Configuration:
    - MDIO: IO18
    - MDC: IO23
    - EN_ETH_CLK: IO16

## Software Requirements

- Arduino IDE with ESP32 board support
- Required Libraries:
  - ETH.h (included in ESP32 Arduino core)

### Log Output
```
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:1
load:0x3fff0030,len:4832
load:0x40078000,len:16460
load:0x40080400,len:4
load:0x40080404,len:3504
entry 0x400805cc
ETH Started
ETH Connected
ETH Disconnected
ETH Connected
ETH Got IP
*eth0: <UP,10M,FULL_DUPLEX,AUTO,ADDR:0x1> (DHCPC,GARP,IP_MOD)
      ether AC:15:18:E9:F1:FB
      inet 10.42.0.227 netmask 255.255.255.0 broadcast 10.42.0.255
      gateway 10.42.0.1 dns 10.42.0.1


connecting to google.com
HTTP/1.1 301 Moved Permanently
Location: http://www.google.com/
Content-Type: text/html; charset=UTF-8
Content-Security-Policy-Report-Only: object-src 'none';base-uri 'self';script-src 'nonce-NmMKWnFm8ApcWypYYv2nwA' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
Date: Mon, 02 Dec 2024 09:34:41 GMT
Expires: Wed, 01 Jan 2025 09:34:41 GMT
Cache-Control: public, max-age=2592000
Server: gws
Content-Length: 219
X-XSS-Protection: 0
X-Frame-Options: SAMEORIGIN

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
closing connection
```

## Important Notes

- IO16 is used to enable the 50MHz clock required for Ethernet operation
- The project initializes the Ethernet PHY and establishes network connectivity
- Arduino framework provides a simpler interface compared to ESP-IDF version

## Features

- Basic Ethernet connectivity test
- DHCP client implementation
- Network status monitoring
- Simple and straightforward Arduino implementation

## Pin Configuration Details

| Function    | GPIO Pin |
|------------|----------|
| MDIO       | IO18     |
| MDC        | IO23     |
| EN_ETH_CLK | IO16     |

## Usage

1. Install ESP32 board support in Arduino IDE
2. Open the ETH_LAN8720.ino sketch
3. Select the appropriate board and port
4. Upload the sketch
5. Monitor the serial output for connection status

## References

- [Unofficial guide to the WT32-ETH01](https://github.com/egnor/wt32-eth01)
- [ESP32 Arduino Core Documentation](https://docs.espressif.com/projects/arduino-esp32/en/latest/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
