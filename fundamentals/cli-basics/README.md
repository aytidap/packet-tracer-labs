# Cisco CLI Basics

Basic Cisco IOS CLI navigation and router interface configuration.

## Basic Commands

### Set Enable Secret Password

```bash id="jlwm7v"
enable secret iloveme
```

### Show Running Configuration

```bash id="d65n6l"
do show running-config
```

### Change Hostname

```bash id="vdsp5z"
hostname R1
```

### Configure MOTD Banner

```bash id="q4m5y7"
banner motd #Unauthorized access prohibited#
```

## CLI Modes

| Mode                 | Description                  |
| -------------------- | ---------------------------- |
| `Router>`            | User EXEC Mode               |
| `Router#`            | Privileged EXEC Mode         |
| `Router(config)#`    | Global Configuration Mode    |
| `Router(config-if)#` | Interface Configuration Mode |

## Navigation Commands

| Command              | Function                                |
| -------------------- | --------------------------------------- |
| `enable`             | Enter Privileged EXEC mode              |
| `configure terminal` | Enter Global Configuration mode         |
| `interface fa0/0`    | Enter Interface Configuration mode      |
| `exit`               | Move up one level                       |
| `end`                | Return directly to Privileged EXEC mode |
| `disable`            | Return to User EXEC mode                |

## Basic Router Interface Configuration

```bash id="5r6n1v"
Router> enable
Router# configure terminal

Router(config)# interface fa0/0
Router(config-if)# ip address 10.10.10.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit

Router(config)# interface fa0/1
Router(config-if)# ip address 20.20.20.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
```
