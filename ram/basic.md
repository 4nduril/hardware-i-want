# RAM

## Characteristics

### Size

### Generation

### ECC

ECC-RAM can detect 2-Bit errors and correct 1-Bit errors (generally). So it adds reliability to the data which is stored in RAM. Although it’s standard to use ECC-RAM in servers, there is some reason to question that need (see [To ECC or Not To ECC on Coding Horror](https://blog.codinghorror.com/to-ecc-or-not-to-ecc/)).

To be able to use ECC-DIMMs you have to have a CPU and a motherboard that suppport ECC. Note: It's the board itself (BIOS and maybe also wiring from CPU to DIMMs) not the chipset that is involved here. To have a ordered starting point for the check bits in memory the BIOS has to initialize, i.e. write to, the complete RAM range. If it doesn't, no ECC. Also, be careful when the board specs say “compatible”. Sometimes that only means you can use ECC-DIMMs but they will operate without ECC. When in doubt, ask the manufactorer.

Yes, the internet is full of articles and forums which either vague or explicitly say it would be chipset-dependent. Yes, even newer articles (2016/17). But they are wrong. The memory controller is built into modern CPUs. Historically though, it sat in a chip called Northbridge which was part of the, well, chipset. Not anymore. It’s dead, Jim. See e.g. [my own question on superuser](https://superuser.com/questions/1224573/why-is-memory-still-dependent-on-the-chipset).

### Registered

### Clockspeed

### Latency
