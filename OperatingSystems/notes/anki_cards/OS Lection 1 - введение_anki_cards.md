№
1
Question;
Which CPU mode allows any instruction and any memory address, including I/O?
Answer;
kernel mode
Explanation
Kernel (supervisor) mode is a CPU bit, often in the PSW. While it is set, code may touch all hardware and memory. The kernel runs here. A crash here takes down the whole PC: nothing sits below to catch it.

---
№
2
Question;
Which CPU mode may execute only a subset of instructions?
Answer;
user mode
Explanation
Everything except the OS runs in user mode. I/O and machine-control instructions are illegal here. Isolation is enforced by the hardware, not by a polite library.

---
№
3
Question;
Who refuses I/O from user mode: the C library or the CPU hardware?
Answer;
the CPU hardware
Explanation
IN/OUT and similar privileged ops are trapped by the processor. The library cannot grant a right the CPU withholds. The legal path is a system call (TRAP).

---
№
4
Question;
A crash in kernel mode takes down what?
Answer;
the whole PC
Explanation
The kernel is the most trusted code. There is no lower layer to isolate a kernel bug, so the machine stops. Contrast a user-process crash, which is recoverable.

---
№
5
Question;
Is a crash in user mode recoverable?
Answer;
yes
Explanation
The kernel is still up, so the OS can kill the process and continue. That is why untrusted apps must not run in kernel mode.

---
№
6
Question;
Legal way for a user program to request an OS service?
Answer;
system call (TRAP)
Explanation
The program does not jump into kernel addresses. TRAP switches the CPU to kernel mode and vectors to a fixed OS entry. After the service, control returns to user mode.

---
№
7
Question;
OS viewed top-down (from the program toward hardware) is called?
Answer;
extended machine
Explanation
The programmer sees files and disk blocks, not controller registers. Top-down is a direction of thinking, not a floor in the PC case. The other view is resource manager.

---
№
8
Question;
OS viewed bottom-up (from scarce hardware toward many programs) is called?
Answer;
resource manager
Explanation
CPU, RAM, and devices are limited; many programs want them. The OS does orderly, controlled allocation so programs do not overwrite each other. Opposite view: extended machine.

---
№
9
Question;
Top-down vs bottom-up for an OS: what is the axis?
Answer;
direction of thinking (not two binaries)
Explanation
Same OS layer. Top-down starts from the programmer's API. Bottom-up starts from finite iron. Do not read it as two modules or as floors in the chassis.

---
№
10
Question;
Time multiplexing: what do programs do with the resource?
Answer;
take turns
Explanation
The whole resource goes to one user/program, then another. Lecture examples: CPU and printers. Contrast space multiplexing (each gets a part).

---
№
11
Question;
Space multiplexing: what does each program get?
Answer;
part of the resource
Explanation
The resource is sliced. Lecture examples: memory and disks. Contrast time multiplexing (take turns with the whole thing).

---
№
12
Question;
Lecture example of time multiplexing besides printers?
Answer;
CPU
Explanation
One core cannot be cut into simultaneous pieces for two programs in this model: they take turns. Printers are the other lecture example.

---
№
13
Question;
Lecture example of space multiplexing besides disks?
Answer;
memory
Explanation
RAM is partitioned among programs at the same time. Disks are the other lecture example. CPU/printers are time-multiplexed instead.

---
№
14
Question;
1st generation (1945–1955): what OS did those machines have?
Answer;
no OS
Explanation
Vacuum tubes, plug boards, Colossus/ENIAC. Mechanical language, huge, hot, almost no storage. Operating systems start in the 2nd generation.

---
№
15
Question;
2nd generation (1955–1965): what appeared in system software?
Answer;
first OS and batch
Explanation
Transistors, mainframes, core memory, tapes/disks. Batch: a pack of jobs with no interactive user at the console. Not yet timesharing.

---
№
16
Question;
3rd generation: several jobs in memory so the CPU need not idle on I/O?
Answer;
multiprogramming
Explanation
IBM System/360-class machines. Also spooling and timesharing on the same generation slide. Multiprogramming is about several programs, not several people.

---
№
17
Question;
3rd generation: buffer I/O (e.g. print) on disk so the CPU is not idle?
Answer;
spooling
Explanation
I/O is staged on disk instead of tying the CPU to a slow device. Same generation also introduces multiprogramming and timesharing.

---
№
18
Question;
3rd generation: many users share one machine interactively?
Answer;
timesharing
Explanation
Each user thinks the machine is theirs. Later reused as a mainframe service. Distinct from 2nd-generation batch, which has no interactive users.

---
№
19
Question;
4th generation: first disk OS named on the lecture?
Answer;
CP/M
Explanation
Personal computers after LSI; Intel 8080 and 8-inch floppy. IBM PC / Gates asking for an OS is the same era. 5th generation is mobile.

---
№
20
Question;
5th generation (1990–present) on the lecture slide?
Answer;
mobile computers
Explanation
The slide is almost empty besides the mobile era. Handheld OS (Android, iOS) lives in the OS zoo.

---
№
21
Question;
First step of the CPU instruction cycle?
Answer;
Fetch Instruction
Explanation
Read the next instruction into a buffer. Then decode, calculate operand addresses, fetch operands, execute, write the result.

---
№
22
Question;
CPU instruction cycle: after Fetch Instruction comes?
Answer;
Decode Instruction
Explanation
Decode finds the opcode and operand specifiers. Next: calculate operand addresses.

---
№
23
Question;
CPU instruction cycle: after Decode Instruction comes?
Answer;
Calculate Operands
Explanation
Compute the effective address of each source operand. Then fetch those operands from memory if they are not already in registers.

---
№
24
Question;
CPU instruction cycle: after Calculate Operands comes?
Answer;
Fetch Operands
Explanation
Load operands from memory. If they already sit in registers, this memory trip is skipped.

---
№
25
Question;
CPU instruction cycle: after Fetch Operands comes?
Answer;
Execute Instruction
Explanation
Perform the operation and obtain the result. Last step: write the operand back.

---
№
26
Question;
CPU instruction cycle: last step after Execute Instruction?
Answer;
Write Operand
Explanation
Store the result in memory (or a register, depending on the instruction). Then the cycle starts again at fetch.

---
№
27
Question;
Program counter (PC) holds the address of?
Answer;
the next instruction
Explanation
Fetch uses the PC. Distinct from the stack pointer (current stack in memory) and from the PSW (flags, priority, mode).

---
№
28
Question;
Stack pointer (SP) points to?
Answer;
the current stack in memory
Explanation
Inside the CPU, but the stack itself lives in memory. PC is the next instruction; PSW holds mode and flags.

---
№
29
Question;
Which register word holds the kernel/user mode bit?
Answer;
PSW
Explanation
Program Status Word: comparison flags, CPU priority, mode (kernel or user), other control bits. A system call must change this bit; software cannot fake kernel mode without it.

---
№
30
Question;
Three-stage instruction pipeline: the three units?
Answer;
Fetch, Decode, Execute
Explanation
Stages of different instructions overlap. This is not extra cores and not hyper-threading. Superscalar adds more execute units plus a holding buffer.

---
№
31
Question;
Superscalar CPU can start more than one instruction per cycle using?
Answer;
multiple execute units and a holding buffer
Explanation
Still one core's instruction-level parallelism. True multi-CPU parallelism is multicore. Two-thread switching on one core is hyper-threading.

---
№
32
Question;
Does multithreading / hyper-threading offer true parallelism (lecture wording)?
Answer;
no
Explanation
The CPU keeps the state of two threads and can switch in nanoseconds when one waits for memory. Logical processors share one physical core. Multicore chips do true parallelism.

---
№
33
Question;
Hyper-threading: the CPU keeps state of two threads and switches in?
Answer;
nanoseconds
Explanation
If a thread must read a word from memory (slow), the CPU switches to the other thread instead of stalling. Still not two full cores.

---
№
34
Question;
Do multicore chips do true parallelism (lecture wording)?
Answer;
yes
Explanation
Several complete processors on one chip. The OS must be a multiprocessor OS. GPU is different: thousands of tiny cores for small parallel work.

---
№
35
Question;
Lecture GPU: how many cores, of what kind?
Answer;
thousands of tiny cores
Explanation
Good for many small computations in parallel (e.g. rendering polygons). Not a substitute for two fat CPU cores, and not hyper-threading.

---
№
36
Question;
Typical register access time on the lecture slide?
Answer;
1 nsec
Explanation
Top of the hierarchy: fastest, tiniest, most dollars per bit. Cache ~2 nsec, main memory ~10 nsec, disk ~10 msec. Slide typical values, not 2026 datasheets.

---
№
37
Question;
Typical cache access time on the lecture slide?
Answer;
2 nsec
Explanation
Between registers (1 nsec) and main memory (10 nsec). Capacity on the slide ~4 MB. Hit in cache also described as about 2 clock cycles.

---
№
38
Question;
Typical main-memory access time on the lecture slide?
Answer;
10 nsec
Explanation
RAM layer: 1–8 GB on the slide. Disk is ~10 msec — a million times slower than this RAM figure.

---
№
39
Question;
Typical magnetic-disk access time on the lecture slide?
Answer;
10 msec
Explanation
Seek + rotation delay + transfer. In nanoseconds this is 10,000,000 ns, which dominates average-access formulas if virtual memory hits disk.

---
№
40
Question;
Typical cache line size?
Answer;
64 bytes
Explanation
Main memory is cut into lines; the hottest lines live in high-speed cache inside the CPU. A hit does not send a request over the bus to RAM.

---
№
41
Question;
On a cache hit, is a main-memory request sent on the bus?
Answer;
no
Explanation
Hardware finds the line in cache and answers locally, usually in about 2 clock cycles. Misses go to RAM, then maybe disk if using virtual memory.

---
№
42
Question;
Cache hit latency in the lecture (clock cycles)?
Answer;
about 2 clock cycles
Explanation
That is why the hierarchy slide can say ~2 nsec for cache. Two or three cache levels: each next level is slower and larger.

---
№
43
Question;
Each next cache level compared with the previous is?
Answer;
slower and larger
Explanation
L1 is small and fast; L2/L3 grow and slow down. On multicore slides, L2 may be shared or per-core.

---
№
44
Question;
On power-off, which loses its contents: RAM or ROM?
Answer;
RAM
Explanation
RAM serves CPU requests that the cache missed. ROM is nonvolatile and programmed at the factory. EEPROM/flash are nonvolatile but rewritable.

---
№
45
Question;
Where is ROM programmed?
Answer;
at the factory
Explanation
Afterwards it does not change. Some machines keep the bootstrap loader in ROM. CMOS is a different chip: time, date, boot-device list.

---
№
46
Question;
Can EEPROM and flash be erased and rewritten (unlike factory ROM)?
Answer;
yes
Explanation
Both are nonvolatile. Flash sits between RAM and disk in speed, is used in portables, and wears out.

---
№
47
Question;
Flash memory wears out: true or false?
Answer;
true
Explanation
Rewrite cycles are limited. Speed is between RAM and disk. Do not treat flash as immortal ROM.

---
№
48
Question;
CMOS stores time, date, and which boot parameter?
Answer;
which disk to boot from
Explanation
BIOS walks that CMOS list after POST. Wrong boot device in CMOS means the machine will not find the OS. Not the same as ROM bootstrap code.

---
№
49
Question;
On some machines the bootstrap loader lives in?
Answer;
ROM
Explanation
Factory-programmed, survives power-off. Later stages come from disk: boot sector, then secondary loader from the active partition.

---
№
50
Question;
HDD access time = seek + transfer + what delay?
Answer;
rotation delay (latency)
Explanation
Seek: move the head to the track. Rotation delay: wait until the sector reaches the head. Transfer: actually read/write the bits.

---
№
51
Question;
Disk seek time is the time to?
Answer;
position the head on the track
Explanation
Mechanical. Then you still wait for rotation (latency) and pay transfer time. This is why disk is milliseconds in the memory hierarchy.

---
№
52
Question;
Disk rotation delay (latency) waits until?
Answer;
the sector reaches the head
Explanation
The platter must spin into place after the head is already on the right track. Distinct from seek (arm motion) and from transfer (data rate).

---
№
53
Question;
Two parts of an I/O device?
Answer;
controller and the device itself
Explanation
The controller accepts OS commands. The mechanism behind it is simple and easier to standardize. The driver talks to the controller.

---
№
54
Question;
A device driver must be placed in the OS so it can run in?
Answer;
kernel mode
Explanation
Talking to controller registers needs privileged IN/OUT or mapped I/O. A user program must not get that. Drivers are loaded into the kernel at boot.

---
№
55
Question;
The set of all device registers is called?
Answer;
I/O port space
Explanation
Each controller has a small set of registers. Access is either memory-mapped (ordinary loads/stores) or special port space (IN/OUT).

---
№
56
Question;
Memory-mapped I/O: device registers are accessed as?
Answer;
ordinary memory words
Explanation
Registers are mapped into the OS address space. The other style is a separate I/O port space with IN and OUT, kernel-only.

---
№
57
Question;
I/O registers in a special port space are accessed with which instructions?
Answer;
IN and OUT
Explanation
Each register has a port address. Only kernel mode may execute these. Memory-mapped I/O instead uses ordinary memory reads/writes.

---
№
58
Question;
Busy waiting (polling) I/O: the CPU is?
Answer;
busy polling until the device finishes
Explanation
The driver starts I/O then sits in a tight loop. Simple, but the CPU cannot do other work. Interrupt and DMA free the CPU.

---
№
59
Question;
Interrupt-driven I/O: the device signals when?
Answer;
the transfer is finished
Explanation
The driver starts the device and can let the OS run something else. Device number may index an interrupt vector to the handler address.

---
№
60
Question;
An interrupt vector maps a device number to?
Answer;
the interrupt handler address
Explanation
A slice of memory: index = device number, value = handler. After the handler, control can return to the user program.

---
№
61
Question;
DMA moves bits between memory and the controller without?
Answer;
constant CPU involvement
Explanation
The CPU programs the DMA chip (what and where), then lets go. When done, DMA typically raises an interrupt, like interrupt-driven I/O.

---
№
62
Question;
When a DMA transfer completes, DMA typically?
Answer;
raises an interrupt
Explanation
Same finish path as interrupt I/O after the bytes have already been moved by the DMA chip, not by the CPU in a loop.

---
№
63
Question;
A shared bus needs who to decide the current owner?
Answer;
an arbiter
Explanation
Several devices share the same wires. Without an arbiter they collide. Parallel vs serial is a different axis (many wires vs one lane).

---
№
64
Question;
A parallel bus carries a data word how?
Answer;
on many wires at once
Explanation
Example: classic PCI, a 32-bit word on 32 wires. Serial: all bits of a message on one lane; parallelism then means many lanes.

---
№
65
Question;
A serial bus lane carries bits over how many connections?
Answer;
one
Explanation
The whole message is serialized. Throughput can still be high with many lanes (32 messages on 32 lanes). Contrast parallel PCI-style buses.

---
№
66
Question;
DDR3/DDR4 in the lecture connect which two?
Answer;
CPU and RAM
Explanation
Other lecture links: PCIe to an external graphics device; DMI between north and south bridge; SCSI/SATA to disks; USB as a polled central bus.

---
№
67
Question;
PCIe in the lecture is the bus to?
Answer;
an external graphics device
Explanation
Not the CPU–RAM path (that is DDR). Disks on the slide are SCSI/SATA. USB is a centralized bus whose root polls devices.

---
№
68
Question;
On USB, the root device does what to other I/O?
Answer;
polls them
Explanation
Centralized bus: the root asks whether each device has traffic. Distinct from a shared bus with an arbiter, and from PCIe to graphics.

---
№
69
Question;
Plug and Play automatically assigns what that used to be wired on the card?
Answer;
IRQ and I/O addresses
Explanation
Old cards had fixed interrupt lines and port addresses, so two cards could clash. PnP collects device info, assigns numbers centrally, and tells the card.

---
№
70
Question;
First firmware that runs at power-on (lecture boot chain)?
Answer;
BIOS
Explanation
Low-level I/O software on the parent board. Then POST, scan buses, pick a boot device from CMOS, run the boot sector.

---
№
71
Question;
BIOS POST checks integrity, RAM size, and?
Answer;
that basic devices respond
Explanation
Power-On Self-Test. After POST the BIOS scans buses and detects devices, then chooses a boot device from the CMOS list.

---
№
72
Question;
After POST, BIOS scans what to detect devices?
Answer;
buses
Explanation
The OS later must know those buses for configuration. Boot device choice is a separate step using the CMOS list.

---
№
73
Question;
The list of candidate boot devices is stored in?
Answer;
CMOS
Explanation
Time, date, and configuration, including which disk to boot from. BIOS walks this list. ROM holds bootstrap code on some machines, not this list.

---
№
74
Question;
The boot sector is which sector of the boot device?
Answer;
the first sector
Explanation
Loaded into memory and executed. It usually looks at the partition table at the end of that sector to find the active partition.

---
№
75
Question;
The secondary boot loader is read from?
Answer;
the active partition
Explanation
Then it reads the OS from that partition and starts it. The OS queries BIOS for configuration and loads drivers into the kernel.

---
№
76
Question;
After the OS starts, device drivers are loaded into?
Answer;
the kernel
Explanation
For each device the OS checks that a driver exists. Then it initializes tables, starts background processes, and launches login or a GUI.

---
№
77
Question;
Mainframe OS is built for many jobs that do mostly?
Answer;
huge I/O
Explanation
Room-sized machines in data centers (OS/360, OS/390). Services include batch, transaction-processing, and timesharing. Not a microwave embedded OS.

---
№
78
Question;
Mainframe batch service: jobs run with what kind of user?
Answer;
no interactive user
Explanation
Routine jobs without someone at a terminal. Distinct from timesharing (many remote interactive users) and from transaction-processing (many small requests).

---
№
79
Question;
Mainframe timesharing service: many users where?
Answer;
remote, at the same time
Explanation
Example: querying a large database. This is the 3rd-generation idea reused as a mainframe service, not 2nd-generation batch.

---
№
80
Question;
Server OS: many users share hardware and software how?
Answer;
over the network
Explanation
Big PCs, workstations, even mainframes. Lecture examples: Solaris, FreeBSD, Linux, Windows Server. Distinct from embedded (no user-installed software).

---
№
81
Question;
A multiprocessor OS exists so one system can run?
Answer;
several CPUs
Explanation
Parallel computers, multicomputers, multiprocessors; today even laptops are small-scale multiprocessors. Needed to use multicore chips.

---
№
82
Question;
Embedded OS: may the user install extra software?
Answer;
no
Explanation
Computers inside appliances that are not thought of as computers: microwave, MP3, TV, cars. Examples: embedded Linux, QNX, VxWorks. Contrast a PC OS.

---
№
83
Question;
Sensor-node OS named on the lecture?
Answer;
TinyOS
Explanation
A node has CPU, RAM, ROM, and sensors; radios to peers and a base station. Smallest-power class, not a handheld phone OS.

---
№
84
Question;
Hard real-time: missing a deadline is?
Answer;
forbidden (absolute guarantee)
Explanation
The action must happen by the deadline. Soft real-time may miss occasionally with no permanent damage. Example OS on the slide: QNX.

---
№
85
Question;
Soft real-time: a rare missed deadline causes?
Answer;
no permanent damage
Explanation
Missing is bad but allowed. Hard real-time instead gives absolute guarantees. Do not mix this with 'embedded means no app store'.

---
№
86
Question;
Smart-card OS in ROM often includes which interpreter?
Answer;
JVM
Explanation
Tiniest OS class: CPU on a credit card. Java applets are downloaded and interpreted. Not a mainframe timesharing service.

