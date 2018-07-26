# Booting process

## Why four loaders are necessary?

### First loader (bootloader in permanent memory such as ROM/NOR flash/randomly access and byte addressable)

- Processor can run but knows nothing about the whole system
- Prepared by by SoC vendors or motherboard vendors to make sure there is no problem with the whole system
- Check/initialize the hardware
- May provide basic services to other programs
- May provide shells to end‐users for basic operations
- Load/jump to the second loader (based on predefined procedures/configurations)

### Second loader (bootloader in any devices such as DISK/CD‐ROM/NAND flash/remote server/…)

- As soon as first bootloader can access the second loader(on any device), load it into memory, and can jump to the starting instruction
- Prepare by OS vendors or other third party vendors
	Stored in the correct location/in correct format)
	Must know how to loader OSs
- May provide shell to end‐users to select OSs (multi‐booting) or set configurations
- Loading OS into memory
- Optional for embedded processors

### Third loader (OS loader that loads OS)

- A program executes without OS services
- Initial and prepare OS services

### Fourth loader (processes replies on OS to fork/exec other processes)

- OS is now ready and can provide services
- Any process calls OS services to fork/execute other processes










