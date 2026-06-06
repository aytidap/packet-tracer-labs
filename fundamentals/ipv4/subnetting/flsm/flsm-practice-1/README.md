## Network Address

```txt id="69rwv7"
10.10.10.0/27
```

## End Devices

| Device | IP Address  | Subnet Mask     |
| ------ | ----------- | --------------- |
| PC1    | 10.10.10.10 | 255.255.255.224 |
| PC2    | 10.10.10.11 | 255.255.255.224 |
| PC3    | 10.10.10.33 | 255.255.255.224 |
| PC4    | 10.10.10.34 | 255.255.255.224 |
| PC5    | 10.10.10.35 | 255.255.255.224 |

## Router Configuration

```bash id="vgpq09"
enable
configure terminal

interface fa0/0
 no shutdown
 ip address 10.10.10.1 255.255.255.224
exit

interface fa0/1
 no shutdown
 ip address 10.10.10.36 255.255.255.224
exit
```

## Connections

* Switch ↔ Router: Copper Straight-Through
* PC ↔ Switch: Copper Straight-Through

## Verification

### PC1 → PC4

```bash id="31axfr"
PC1> ping 10.10.10.34

Reply from 10.10.10.34: bytes=32 time<1ms TTL=128
Reply from 10.10.10.34: bytes=32 time<1ms TTL=128
Reply from 10.10.10.34: bytes=32 time<1ms TTL=128
Reply from 10.10.10.34: bytes=32 time<1ms TTL=128

Ping statistics for 10.10.10.34:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
```

Result: Success

### PC3 → PC2

```bash id="jkf9zf"
PC3> ping 10.10.10.11

Reply from 10.10.10.11: bytes=32 time<1ms TTL=128
Reply from 10.10.10.11: bytes=32 time<1ms TTL=128
Reply from 10.10.10.11: bytes=32 time<1ms TTL=128
Reply from 10.10.10.11: bytes=32 time<1ms TTL=128

Ping statistics for 10.10.10.11:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
```

Result: Success

### PC5 → PC1

```bash id="x2dkh7"
PC5> ping 10.10.10.10

Reply from 10.10.10.10: bytes=32 time<1ms TTL=128
Reply from 10.10.10.10: bytes=32 time<1ms TTL=128
Reply from 10.10.10.10: bytes=32 time<1ms TTL=128
Reply from 10.10.10.10: bytes=32 time<1ms TTL=128

Ping statistics for 10.10.10.10:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
```

Result: Success
