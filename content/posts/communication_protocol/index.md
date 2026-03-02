---
title: "Communication Protocol"
date: 2026-02-03T06:00:20+06:00
hero: /images/posts/writing-posts/git.svg
menu:
  sidebar:
    name: Communication Protocol
    identifier: comm-pro
    weight: 30
---

## Data Communication
Data transfers can happen either serially or parallely. In serial communication,data bits are transmitted one by one whereas in parallel commuication, all bits are transmitted simultaneously.

Serial Communication can be asynchronous or synchronous.
In asynchronous serial communication, a single byte is transferred at a time. It does not require a clock signal. Eg: UART
In Synchronous coommunication,a block of data is transferred at a time. It requires a clock signal. Eg: I2C, SPI

## Some Terms
#### Simplex
Data is transmitted only in one direction.
#### Duplex
Data can be transmitted and received
##### Half Duplex 
Data is transmitted in both direction but only one eay at a time
##### Full Duplex
Data is transmitted in both direction at the same time

## UART

UART is a two wired Asynchronous serial communication protocol

For UART Communication, we need to configure both devices with same speeed, i.e. baud rate.

_Baud Rate is the data transfer rate on bits per sec._

UART Protocol requires a start bit and a stop bit. Data length can vary froom 5 bits to 9 bits. These should be configured before using UART. It uses NRZ (Non Return to zero) encoding for transmission. UART uses little endian bit ordering, which means the least significant bit is transmitted first. 


### Full Post Coming Soon!!!