---
title: "UART: Universal Asynchronous Receiver and Transmitter"
date: 2026-01-08T06:00:20+06:00
hero: /images/posts/writing-posts/git.svg
menu:
  sidebar:
    name: UART
    identifier: uart
    parent: communication-protocol
    weight: 20
---

UART is a two wired Asynchronous serial communication protocol

For UART Communication, we need to configure both devices with same speeed, i.e. baud rate.

_Baud Rate is the data transfer rate on bits per sec._

UART Protocol requires a start bit and a stop bit. Data length can vary froom 5 bits to 9 bits. These should be configured before using UART. It uses NRZ (Non Return to zero) encoding for transmission. UART uses little endian bit ordering, which means the least significant bit is transmitted first. 

### UART via ESP32

### Complete Post Coming Soon...
