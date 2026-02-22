# Modbus Setup Guide

## Hardware Example

Waveshare TCP to RS485 converter.

## Settings

- TCP Mode
- Port 502
- 9600 baud
- 8N1
- RTU mode

## Node-RED Settings

- node-red-contrib-modbus
- Modbus Flex Write
- FC6 single register writes
- 200ms delay between writes
- Timeout 2000ms
