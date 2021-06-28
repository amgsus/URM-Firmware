# URM HID Protocol

The device implements several modes.

### Report ID 1 (IN)

The device sends Report 1 when the state of input channels are changed.

| Offset | Field Size | Description |
| ------ | ---------- | ----------- |
| 0 | 8 | Bits 0:3 indicate the state of inputs. |

### Report ID 1 (OUT)

The host sends Report 1 to the device to set the state of output channels (relays).

| Offset | Field Size | Description |
| ------ | ---------- | ----------- |
| 0 | 8 | Bits 0:3 indicate the desired state of outputs. |

### Report ID 2 (OUT)

The host sends Report 2 to the device to turn OFF and ON outputs with atomic operation, or does not perform any change. 

| Offset | Field Size | Description |
| ------ | ---------- | ----------- |
| 0 | 8 | Bits 0:3 set the respective outputs to OFF state. Bits 4:7 set the outputs to ON state.  |

| Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| Set output 4 to ON | Set output 3 to ON | Set output 2 to ON | Set output 1 to ON | Set output 4 to OFF | Set output 3 to OFF | Set output 2 to OFF| Set output 1 to OFF |
