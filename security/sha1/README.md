SHA1 Example
===============================

This is an optimized implementation of SHA1 secure hash algorithm targeting
execution on an SDAccel supported FPGA acceleration card.



Changelog
----------
1/29/2016 - Initial Release
7/5/2016  - Conversion to Makefile based execution

Compiling the Application
---------------------------
This application is compiled using the SDAccel Makefile flow

To compile the application for execution on x86 servers/cloud:

```
make all
```

To compile the application for execution on POWER8 servers/cloud:
```
make sv_all
```

The target board and platforms are available in the utility/boards.mk file. The utility directory is located at the root of this repository.


Executing the Application
---------------------------
```
sha1_example.exe --platform Xilinx --device fpga0 --kernel bin_sha1.xclbin
```

Files in the Example
---------------------
Application code is located in the src directory.
Accelerator binary files are located in the xclbin directory. This directory is required by the Makefile. The contents of the directory are generated during compilation.