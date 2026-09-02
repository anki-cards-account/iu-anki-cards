№
1
Question;
Multiprogramming: what several things reside on one computer at once?
Answer;
programs
Explanation
Goal: while one waits for disk, the CPU runs another. There need not be interactive users — a batch of jobs is enough. Time-sharing is about several users, not this axis.

---
№
2
Question;
Time-sharing: computing resources are shared among several what at the same time?
Answer;
users
Explanation
Usually interactive: each user thinks the machine is theirs. Several users imply several programs, so every TS system is multiprogramming. The converse is false.

---
№
3
Question;
Every timesharing system is a multiprogramming system. Is every MP system timesharing?
Answer;
no
Explanation
A batch machine can keep several jobs in memory with nobody at a terminal. That is MP without TS. Do not confuse either term with multiplexing (time vs space for one resource).

---
№
4
Question;
Time-sharing vs multiplexing: multiplexing's axis is time vs space for?
Answer;
one resource
Explanation
CPU take-turns vs RAM sliced. Time-sharing is sharing a computer among people. Different question from MP (several programs) vs TS (several users).

---
№
5
Question;
2 physical CPUs × 2 hyperthreads each: how many physical packages?
Answer;
2
Explanation
Four logical processors, still two packages. Logical threads on one package share ALU and cache. HT is not four full cores and not multicore true parallelism.

---
№
6
Question;
HT scheduling when programs do not migrate: finish time is the load on the busiest?
Answer;
physical CPU
Explanation
Two threads on one package serialize CPU-bound work. Best case ~20 msec if P2=20 runs alone; worst ~35 if 5+10+20 share one package.

---
№
7
Question;
Average access: RAM hit rate 99% is measured among what, not among all references?
Answer;
cache misses
Explanation
Cache already hits 95% of all references. RAM's 99% applies to the remaining 5%. Disk gets 0.05×0.01 of references. Do not treat 99% as 99% of everything.

---
№
8
Question;
Average access time over cache/RAM/disk is a weighted sum, not?
Answer;
the mean of the three latencies
Explanation
Do not compute (1 ns + 10 ns + 10 ms)/3. Almost all of 5001.445 ns comes from the rare disk term (5000 ns).

---
№
9
Question;
What are the two main functions of an operating system?
Answer;
resource management and fine abstractions from the bare metal
Explanation
Two views of the same OS, not two programs. Top-down (program toward hardware): extended machine — disk blocks instead of controller registers. Bottom-up (scarce hardware toward many programs): resource manager — orderly allocation so programs do not overwrite each other. Top/bottom is a thinking axis, not a floor in the case.

---
№
10
Question;
Define multiprogramming (not time-sharing).
Answer;
several programs on one computer at the same time
Explanation
While one waits for disk, the CPU runs another. Interactive users are optional (batch jobs still count as MP). Time-sharing instead means several users at once.

---
№
11
Question;
Define time-sharing (not multiprogramming).
Answer;
sharing resources among several users at the same time
Explanation
Usually interactive. Several users imply several programs, so every TS system is MP. Not every MP system is TS.

---
№
12
Question;
Are all multiprogramming systems also time-sharing systems?
Answer;
no
Explanation
Every TS system is MP; the converse is false. Counterexample: a batch system with several jobs in memory and no interactive users.

---
№
13
Question;
Monochrome text 25×80: how much video RAM for one frame?
Answer;
2000 bytes
Explanation
One cell = 1 byte (character code, no color). 25×80 = 2000 bytes ≈ 2 KiB. At $5/KiB in 1980 that is $10. Count the framebuffer, not GPU power.

---
№
14
Question;
Bitmap 1200×900, 24-bit color: framebuffer size?
Answer;
3240000 bytes
Explanation
24 bits = 3 bytes per pixel. 1200×900×24 bit = 3,240,000 bytes. The 1980 price on the slide uses KB→KiB via 1.024 and gets $15,820.

---
№
15
Question;
25×80 text RAM cost at 1980 prices ($5/KiB)?
Answer;
$10
Explanation
2000 bytes ≈ 2 KiB × $5/KiB = $10 on the tutorial slide. The bitmap of the same problem is ~$15,820 — GUIs were luxury because RAM was expensive.

---
№
16
Question;
1200×900×24-bit RAM cost at 1980 prices ($5/KiB, slide formula)?
Answer;
$15820
Explanation
3240 KB / 1.024 × $5/KiB = $15,820. Text was $10. Present-day cost is not computed on the answer slide.

---
№
17
Question;
Tutorial 1.8: present-day cost of that video RAM on the answer slide?
Answer;
not computed
Explanation
The source has no number for 'how much now'. Do not invent a 2026 price. The exam point is 1980 text vs bitmap cost.

---
№
18
Question;
What is kernel mode?
Answer;
any instruction, any address, including I/O
Explanation
A CPU bit (often in the PSW). The kernel runs here. A crash takes down the whole PC. User mode is only a subset of instructions; I/O is refused by the hardware.

---
№
19
Question;
Kernel mode vs user mode: who may perform I/O?
Answer;
only kernel mode
Explanation
User mode: subset of instructions; machine control and I/O forbidden by the CPU. Process crash is recoverable. Kernel crash is not.

---
№
20
Question;
How do two CPU modes aid OS design?
Answer;
apps cannot take down the kernel; entry only via TRAP
Explanation
Applications must not get the full key, or a browser tab could wipe OS tables. The kernel stays trusted. Without TRAP the two modes are useless: user mode has no legal way to ask for the disk.

---
№
21
Question;
2 CPU × 2 HT; P0,P1,P2 = 5,10,20 msec; CPU-bound, no migrate. Completion time?
Answer;
20 to 35 msec
Explanation
Four logical processors ≠ four full cores. Finish time = load on the busiest physical CPU. 20 msec if P2 is alone and P0+P1 share the other package; 25 if 5+20; 30 if 10+20; up to 35 if 5+10+20 share one package. HT is not true parallelism.

---
№
22
Question;
Cache 95% @ 1 ns, RAM 99% after miss @ 10 ns, disk 10 ms. Average access time?
Answer;
5001.445 nsec
Explanation
T = 0.95×1 + 0.05×0.99×10 + 0.05×0.01×10,000,000 = 0.95 + 0.495 + 5000 = 5001.445 ns ≈ 5.001 µs. The 99% is among cache misses. Almost all of T is the disk term.

