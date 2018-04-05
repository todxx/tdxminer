# tdxminer v0.1.0.0

This software is in an alpha stage and may be unstable.

Download is available in the [releases section](https://github.com/todxx/tdxminer/releases).

Currently only AMD Polaris and Vega GPUs are supported and must be running with the ROCm 1.7.1 OpenCL stack.

This miner currently only supports the lyra2z algorithm.  Its only configuration is via command line to set the basic parameters for connecting to a stratum pool and selecting which platforms/devices to use.  Invoking the miner with the --help option will print a short help message for how to use the options.  I have tried to make the options similar to other miners to keep confusion to a minimum.

NOTE: This miner does NOT monitor GPU temperatures.  It is up to the user to ensure that GPU(s) are functioning within safe power and temperature limits.

Software Requirements:
- [ROCm 1.7.1](https://github.com/RadeonOpenCompute/ROCm)
- libjansson4

This miner includes a dev fee.  The hash rates reported by the miner are the user hash rates.  (I.E. the hash rates reported should be the average hash rate that your pool reports.)

Some rough lyra2z performance numbers with this version:

| GPU        | SCLK (MHz) | MCLK (MHz) | Hash Rate (Mh/s) |
|------------|-----------:|-----------:|-----------------:|
| RX 580     | 1167       | 2000       |  2.91            |
| RX Vega 64 | 1401       | 945        |  5.81            |

For reporting bugs and/or for features requests, please open an issue on this repository.

Happy hashing ;)
