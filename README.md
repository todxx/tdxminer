# tdxminer v0.2.2.1

This software is in a beta stage and may be unstable on some hardware.

Download is available in the [releases section](https://github.com/todxx/tdxminer/releases).

GPUs Supported:
- RX 580/570/480/470 with amdgpu-pro or ROCm 1.7.1 drivers
- RX Vega 64/56, Vega FE with ROCm 1.7.1 drivers

Software Requirements:
- libjansson4
- A supported driver version (see GPUs Supported above)

This miner currently only supports the lyra2z algorithm.  Its only configuration is via command line to set the basic parameters for connecting to a stratum pool and selecting which platforms/devices to use.  Invoking the miner with the --help option will print a short help message for how to use the options.

NOTE: This miner does NOT monitor GPU temperatures.  It is up to the user to ensure that GPU(s) are functioning within safe power and temperature limits.

This miner includes a 3% dev fee.

The miner reports user hash rates every 60 seconds.  These are the hash rates after dev fee deduction.  (I.E. the hash rates reported should be the average hash rate that your pool reports.)

Some rough lyra2z performance numbers with this version:

| GPU           | SCLK (MHz) | MCLK (MHz) | Hash Rate (Mh/s) |
|---------------|-----------:|-----------:|-----------------:|
| RX 580        | 1167       | 2000       |  3.27            |
| RX Vega 64    | 1401       | 945        |  6.66            |
| RX Vega 64 LC | 1408       | 945        |  7.07            |

For reporting bugs and/or for features requests, please open an issue on this project's github [issue tracker](https://github.com/todxx/tdxminer/issues).

Happy hashing ;)

----------------
Changes in v0.2.2.1
- Added better/faster handling of non-responding pool connections.
- More network bug fixes.

Changes in v0.2.2.0
- More network bug fixes for pool connection.

Changes in v0.2.1.1
- Fixed bug with handling network errors in dev pool connection.

Changes in v0.2.1.0
- Fixed bug with handling network errors in pool connection.

Changes in v0.2.0.0
- Improved lyra2z performance
- Support for Ellesmere GPUs under amdgpu-pro drivers
- Dev fee set to 3%
