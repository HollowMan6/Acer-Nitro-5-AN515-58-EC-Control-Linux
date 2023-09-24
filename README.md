# Acer-Nitro-5-AN515-58-EC-Control-Linux

Implementation of basic EC registers that NitroSense Modifies, as a Bash Script

Support running under secure boot mode or a lockdowned kernel with the help of [acpi_ec](https://github.com/MusiKid/acpi_ec)

# Requirements

1. Install the kernel module `acpi_ec` according to the instructions [here](https://github.com/MusiKid/acpi_ec?tab=readme-ov-file#installation).
2. Reboot.

# Usage

To show available switches

```
./nitrosense
```

Available Switches

```
PWR: [q]uiet [d]efault [p]erformance
FAN: [a]uto  [c]ustom  [m]ax
DBG: [r]ead from ec
DBG: [e]nergy data from intel_rapl
DBG: [n]vidia-powerd restart
```

Example: Default Power with Auto Fan

```
./nitrosense da
```

Example: Performance Power with Max Fan

```
./nitrosense pm
```

Example: Performance Power with Custom Fan at 50%

```
./nitrosense pc 50
```

# Notes
To dump current EC registers

```
./nitrosense r
```
