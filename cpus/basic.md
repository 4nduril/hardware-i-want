# CPU

The CPU is the heart of the computer. Or is it the brain? Whatever. All your further decisions depend on this. So you better know what to look for.

+ [Basic characteristics](#basics)
  + [Socket](#socket)
  + [Clock rate](#clock-rate)
  + [Number of cores](#core-count)
  + [Thermal Design Power](#tdp)
  + [Overclocking support](#overclocking)
  + [Memory support](#ram)
    + [Multi-channel support](#ram-multichannel)
    + [Support of ECC-RAM](#ram-ecc)
  + [PCIe lanes](#pcie-lanes)
  + [Instruction sets / extensions](#instruction-sets)
  + [Word size](#word-size)

## <a name="basics"></a>Basic characteristics

### <a name="socket"></a>Socket

The socket is the physical connection between CPU and mainboard. These are manufactorer- and CPU-generation-/-model-specific. In general, if your hardware renewal cycles are longer than two years you will have to buy both, a new CPU and a new mainboard.

### <a name="clock-rate"></a>Clock rate

The clock rate indicates the speed of a single CPU core. It is measured in clock cycles per second and uses the unit Hz (MHz, GHz …).

Along with the speed of instruction execution the power consumption and the dissipated heat increase with the clock rate. Again, for servers it is not that big of a problem (as long as they don't reside in your living room) if power cost is not a concern to you. For laptops or media PCs it could be better to choose a lower clock rate and maybe more cores (if needed). A multi-core CPU will use less power than multiple single-core CPUs with similar overall performance.

[Wikipedia on clock rate](https://en.wikipedia.org/wiki/Clock_rate)

[Clock rate in the CPU article in Wikipedia](https://en.wikipedia.org/wiki/Central_processing_unit#Clock_rate)

### <a name="core-count"></a>Number of cores

This is a measure for the ability of the CPU to execute multiple tasks *at the same time*, in parallel. Putting more cores in a CPU makes it more capable whithout all of the drawbacks of pushing clock cycles up (power consumption, heat production, see [clock rate](#clock-rate)).

However, note that a fair share of the available and often used software is not written in such a way that it utilizes multiple cores, i.e. parallel execution. So there is no simple equation like "speed = #cores * x" which means if you take a CPU that has double the cores of another it is not twice as fast in your daily usage.

It depends on the software you are going to use and the type of machine you are building. In general, for a computer that is going to be used as a server, e.g. a webserver, it totally makes sense to have as many cores as you are willing to pay. For a desktop workstation or a laptop, not so much. The current line of desktop cpus has around 2–4 cores.

[Wikipedia on multi-core-processors](https://en.wikipedia.org/wiki/Multi-core_processor)

### <a name="tdp"></a>Thermal Design Power

The TDP is a measure for the maximum amount of heat running "real" applications. It is therefore a measure for the cooling needs and of the power needs of a CPU. The smaller the better.

### <a name="overclocking"></a>Overclocking support

By manually raising the clock rate you can reach better performance—for the cost of higher temperature / power consumption. Some CPUs allow to do that, others don't.

### <a name="ram"></a>Memory support

What kind of main memory (RAM) can you use with a certain CPU? And how much of it? The current standard is DDR4-SDRAM. Current mainstream CPUs support generally 32–64GB of RAM.

#### <a name="ram-multichannel"></a>Multi-channel

Most current CPUs support Dual Channel RAM access. That means that the connection between the CPU and the main memory is doubled and so, in theory, the access rate is doubled because of parallel access. Modern high-end CPUs implement even quad-channel RAM access. To exploit these capabilities you also have to use motherboard-specific DIMM configurations. 

Anyway, there seems to be [evidence](http://www.tomshardware.com/reviews/PARALLEL-PROCESSING,1705-15.html) for the fact that the performance gain by multi-channel memory access is nowhere near double.

#### <a name="ram-ecc"></a>Support of ECC RAM

If you want to use ECC-RAM the CPU has to support it. In general, only CPUs intended for server usage are supporting this kind of memory. But there are exceptions.

### <a name="pcie-lanes"></a>PCIe lanes

PCI Express lanes are provided either by the mainboard chipset or directly by the CPU. The CPU lanes are often used for the connection of graphics cards.

### <a name="instruction-sets"></a>Instruction sets / extensions

Somewhat <del>esoteric</del> complicated topic. Each CPU generation implements a certain set of instructions ([Wikipedia](https://en.wikipedia.org/wiki/Instruction_set_architecture)). I remember back in the 90s (yes, the 1990s) Intel had a huge advertising campaign on "Pentium with MMX" where MMX was an extension to the instruction set of the Pentium CPUs of the time. It allowed new ways of calculating integer numbers which was used for 2D/3D modelling. Over the time many extensions have been added (or deliberately not added) to the x86 architecture. One of which is for example [AES-NI](https://en.wikipedia.org/wiki/AES_instruction_set) which allows for crypto calculations directly in the processor hardware. That way, cryptographic usecases such as full disc encryption or software like KeePass are much more performant than without AES-NI.

### <a name="word-size"></a>Word size

Not really worth mentioning. Get a 64 Bit CPU.

[Read what it is in Wikipedia](https://en.wikipedia.org/wiki/Central_processing_unit#Integer_range)
