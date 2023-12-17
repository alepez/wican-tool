# wican-tool

I've created this simple tool to help me setup a [*MeatPi
WiCAN*](https://www.meatpi.com/products/wican) device.

## Install

Copy the `wican` script in `/usr/local/bin` or another directory in your `PATH`
environment variable.

## Usage

If your *WiCAN* has the default configuration and your computer is connected
to *WiCAN* access point, this command will create a `can0` device and set the
bitrate to 1000000:

```sh
wican tcp 0 192.168.80.1
```

You can also set the bitrate:

```sh
wican tcp 0 192.168.80.1 250000
```

If your *WiCAN* has another network configuration, just change the ip address:

```sh
wican tcp 0 192.168.1.217 250000
```

If you have a second *WiCAN* device, just change the `<id>` parameter, it will
create a second can device: `can1`

```sh
wican tcp 1 192.168.1.218 250000
```
