# cs344-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [CS344 Assignment 1 Solved](https://www.ankitcodinghub.com/product/cs344-assignment-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;63242&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS344 Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
This assignment is split into three parts. The first part concentrates on getting familiarized with x86 assembly language, the QEMU x86 emulator, and the PC’s power-on bootstrap procedure. The second part examines the boot loader for our kernel. Finally, you will add a system call in a toy operating system named xv6, which fills a buffer with an ASCII art drawing of Wolfie.

<strong>Part1: PC BootStrap</strong>

The purpose of this exercise is to introduce you to x86 assembly language and the PC bootstrap process, and to get you started with QEMU and QEMU/GDB debugging. You do not have to write any code for this part of the lab, but you should go through it anyway for your own understanding and be prepared to answer the questions posed below.

<strong>X86 Assembly</strong>

If you are not already familiar with x86 assembly language, you will quickly become familiar with it during this course! The <a href="http://pacman128.github.io/static/pcasm-book.pdf">PC Assembly Language Book</a> is an excellent place to start. Hopefully, the book contains mixture of new and old material for you.

<em>Warning: </em>Unfortunately the examples in the book are written for the NASM assembler, whereas we will be using the GNU assembler. NASM uses the so-called <em>Intel </em>syntax while GNU uses the <em>AT&amp;T </em>syntax. While semantically equivalent, an assembly file will differ quite a lot, at least superficially, depending on which syntax is used. Luckily the conversion between the two is pretty simple, and is covered in <a href="http://www.delorie.com/djgpp/doc/brennan/brennan_att_inline_djgpp.html">Brennan’s Guide to Inline Assembly</a> .

<strong>Exercise 1. </strong>

Become familiar with inline assembly by writing a simple program. Modify the program ex1.c (at end of this file) to include inline assembly that increments the value of x by 1.

*You should read the recommended chapters of the PC Assembly book and “The Syntax” section in Brennan’s Guide. Save the Intel/AMD architecture manuals for later or use them for reference when you want to look up the definitive explanation of a particular processor feature or instruction.

<strong>Simulating x86</strong>

Instead of developing the operating system on a real, physical personal computer (PC), we use a program that faithfully emulates a complete PC: the code you write for the emulator will boot on a real PC too. Using an emulator simplifies debugging; you can, for example, set break points inside of the emulated x86, which is difficult to do with the silicon-version of an x86.

In this course, we will use the QEMU Emulator , a modern and relatively fast emulator. While QEMU’s built-in monitor provides only limited debugging support, QEMU can act as a remote debugging target for the GNU debugger (GDB), which we’ll use in this lab to step through the early boot process.

To get started, you have to first built a toolchain to use QEMU and GNU debugger and then clone the xv6 OS and as following:

For Linux users:

<table width="494">
<tbody>
<tr>
<td width="331"><em>$ sudo apt-get update</em></td>
<td width="163"><em>//updates package information</em></td>
</tr>
<tr>
<td width="331"><em>$ sudo apt-get install build-essential</em></td>
<td width="163"><em>//installs GNU tools</em></td>
</tr>
<tr>
<td width="331"><em>$ sudo apt-get install qemu</em></td>
<td width="163"><em>//installs QEMU</em></td>
</tr>
<tr>
<td width="331"><em>$ git clone git://github.com/mit-pdos/xv6-public.git</em></td>
<td width="163"><em>//clones xv6</em></td>
</tr>
</tbody>
</table>
<strong>For Windows users:</strong>

<ol>
<li>Install Linux subsystem for Windows.</li>
<li>After successful installation, open a “bash on Ubuntu VM”.</li>
<li>Follow the same steps for Linux installation after this.</li>
</ol>
Now you’re ready to boot xv6 OS with QEMU, but it requires an image file of the OS that you want to boot. So you need to issue <strong><em>make </em></strong><em>inside xv6 directory</em> to compile the OS. This will supply the file <strong>xv6.img</strong>, as the contents of the emulated PC’s first “virtual hard disk”. This hard disk image contains both our boot loader (bootblock), and our kernel (kernel). Now to boot you can issue following command inside xv6 directory:

<em>$ make qemu&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; //boot OS</em>

This executes QEMU with the options required to set the hard disk and direct serial port output to the terminal. (You could also use <strong>make qemu-nox </strong>to run QEMU in the current terminal instead of opening a new one.)

Everything after ‘Booting from Hard Disk…’ was printed by xv6 kernel; the $ is the prompt printed by the small <em>shell </em>included in our OS. These lines printed by the kernel will also appear in the regular shell window from which you ran QEMU. This is because we have set up the xv6 kernel to write its console output not only to the virtual VGA display (as seen in the QEMU window), but also to the simulated PC’s virtual serial port, which QEMU outputs to its own standard output because of the -serial argument. Likewise, the xv6 kernel will take input from both the keyboard and the serial port, so you can give it commands in either the VGA display window or the terminal running QEMU.

If you type <strong>ls</strong> at the $ prompt, it will list all the files that are included in the file system of our xv6 OS. These files are included in the second virtual hard disk created when you made xv6, namely, <strong>fs.img</strong>. Similarly, you can execute the other programs included in fs.img by typing their names at the command prompt. Of course, we could have combined fs.img and xv6.img into one disk image but we’ve decided to keep them separate for simplicity.

It is important to note that our OS is running “directly” on the “raw (virtual) hardware” of the simulated PC. This means that you should be able to copy the contents of xv6.img onto the first few sectors of a <em>real </em>hard disk, and the contents of fs.img onto another hard disk, insert the disks into a real PC, turn it on, and see exactly the same thing on the PC’s real screen as you did above in the

QEMU window.

NB: We don’t recommend you do this on a real machine with useful information on its hard disk, though, because copying the images onto the beginning of its hard disk will trash the master boot record and the beginning of the first partition, effectively causing everything previously on the hard disk to be lost!

<strong>The PC’s Physical Address</strong>

We will now dive into a bit more detail about how a PC starts up. A PC’s physical address space is hard-wired to have the following general layout:

The first PCs, which were based on the 16-bit Intel 8088 processor, were only capable of addressing 1MB of physical memory. The physical address space of an early PC would therefore start at 0x00000000 but end at 0x000FFFFF instead of 0xFFFFFFFF. The 640KB area marked “Low Memory” was the <em>only </em>random-access memory (RAM) that an early PC could use; in fact the very earliest PCs only could be configured with 16KB, 32KB, or 64KB of RAM!

The 384KB area from 0x000A0000 through 0x000FFFFF was reserved by the hardware for special uses such as video display buffers and firmware held in non-volatile memory. The most important part of this reserved area is the Basic Input/Output System (BIOS), which occupies the 64KB region from 0x000F0000 through 0x000FFFFF.

In early PCs, the BIOS was held in true read-only memory (ROM), but current PCs store the BIOS in updateable flash memory. The BIOS is responsible for performing basic system initialization such as activating the video card and checking the amount of memory installed. After performing this initialization, the BIOS loads the operating system from some appropriate location such as floppy disk, hard disk, CD-ROM, or the network, and passes control of the machine to the operating system.

When Intel finally “broke the one megabyte barrier” with the 80286 and 80386 processors, which supported 16MB and 4GB physical address spaces respectively, the PC architects nevertheless preserved the original layout for the low 1MB of physical address space in order to ensure backward compatibility with existing software. Modern PCs, therefore, have a “hole” in physical memory from 0x000A0000 to 0x00100000, dividing RAM into “low” or “conventional memory”

(the first 640KB) and “extended memory” (everything else). In addition, some space at the very top of the PC’s 32-bit physical address space, above all physical RAM, is now commonly reserved by the BIOS for use by 32-bit PCI devices.

Recent x86 processors can support more than 4GB of physical RAM, so RAM can extend further above 0xFFFFFFFF. In this case the BIOS must arrange to leave a second hole in the system’s RAM at the top of the 32-bit addressable region, to leave room for these 32-bit devices to be mapped. xv6 is a 32-bit operating system so we need not worry about this issue.

<strong>The ROM BIOS</strong>

In this portion of the lab, you’ll use QEMU’s debugging facilities to investigate how an IA-32 compatible computer boots.

Open two terminal windows. In one, enter <strong>make qemu-gdb </strong>(or <strong>make qemu-nox-gdb</strong>). This starts up QEMU, but QEMU stops just before the processor executes the first instruction and waits for a debugging connection from GDB. In the second terminal, from the same directory you ran <strong>make</strong>, run <strong>gdb</strong>, and type <strong>source .gdbinit </strong>at the prompt. You should see something like this:

A .gdbinit script is provided that sets up GDB to debug the 16-bit code used during early boot and directed it to attach to the listening QEMU. It should be loaded before you start debugging the kernel. You can do this by either using GDB’s source command every time you start GDB, or by adding it to the auto load path using its <strong>add-auto-load-safe-pathcommand</strong>.

The following line

[f000:fff0] 0xffff0:&nbsp;&nbsp;&nbsp; ljmp&nbsp;&nbsp; $0xf000,$0xe05b

is GDB’s disassembly of the first instruction to be executed. From this output you can conclude a few things:

<ul>
<li>The IBM PC starts executing at physical address 0x000ffff0, which is at the very top of the 64KB area reserved for the ROM BIOS.</li>
<li>The PC starts executing with CS = 0xf000 and IP = 0xfff0.</li>
<li>The first instruction to be executed is a jmp instruction, which jumps to the segmented address CS = 0xf000 and IP = 0xe05b.</li>
</ul>
Why does QEMU start like this? This is how Intel designed the 8088 processor, which IBM used in their original PC. Because the BIOS in a PC is “hard-wired” to the physical address range 0x000f0000-0x000fffff, this design ensures that the BIOS always gets control of the machine first after power-up or any system restart — which is crucial because on power-up there <em>is </em>no other software anywhere in the machine’s RAM that the processor could execute.

The QEMU emulator comes with its own BIOS, which it places at this location in the processor’s simulated physical address space. On processor reset, the (simulated) processor enters real mode and sets CS to 0xf000 and the IP to 0xfff0, so that execution begins at that (CS:IP) segment address. How does the segmented address 0xf000:fff0 turn into a physical address?

To answer that we need to know a bit about real mode addressing. In real mode (the mode that PC starts off in), address translation works according to the formula: <em>physical address </em>= 16 * <em>segment </em>+ <em>offset</em>.

So, when the PC sets CS to 0xf000 and IP to 0xfff0, the physical address referenced is:

&nbsp;

16 * 0xf000 + 0xfff0&nbsp;&nbsp; # in hex multiplication by 16 is

0xffff0 is 16 bytes before the end of the BIOS (0x100000). Therefore we shouldn’t be surprised that the first thing that the BIOS does is jmp backwards to an earlier location in the BIOS; after all how much could it accomplish in just 16 bytes?

<strong>Exercise 2. </strong>

Use GDB’s <strong>si </strong>(Step Instruction) command to trace into the ROM BIOS for a few more instructions, and try to guess what it might be doing.

When the BIOS runs, it sets up an interrupt descriptor table and initializes various devices such as the VGA display. This is where the “SeaBIOS” messages you see in the QEMU window come from.

After initializing the PCI bus and all the important devices the BIOS knows about, it searches for a bootable device such as a floppy, hard drive, or CD-ROM. Eventually, when it finds a bootable disk, the BIOS reads the <em>boot loader </em>from the disk and transfers control to it.

<strong>Part2: The Boot Loader</strong>

Floppy and hard disks for PCs are divided into 512 byte regions called <em>sectors</em>. A sector is the disk’s minimum transfer granularity: each read or write operation must be one or more sectors in size and aligned on a sector boundary.

If the disk is bootable, the first sector is called the <em>boot sector</em>, since this is where the boot loader code resides. When the BIOS finds a bootable floppy or hard disk, it loads the 512-byte boot sector into memory at physical addresses 0x7c00 through 0x7dff, and then uses a jmp instruction to set the CS:IP to 0000:7c00, passing control to the boot loader. Like the BIOS load address, these addresses are fairly arbitrary — but they are fixed and standardized for PCs.

The ability to boot from a CD-ROM came much later during the evolution of the PC, and as a result the PC architects took the opportunity to rethink the boot process slightly. As a result, the way a modern BIOS boots from a CD-ROM is a bit more complicated (and more powerful). CD-ROMs use a sector size of 2048 bytes instead of 512, and the BIOS can load a much larger boot image from the disk into memory (not just one sector) before transferring control to it.

For this course, however, we will use the conventional hard drive boot mechanism, which means that the BIOS will only load the first 512 bytes. The boot loader (bootasm.S and bootmain.c) does the bootstrapping work. Look through these source files carefully and make sure you understand what’s going on. The boot loader must perform the following main functions:

<ol>
<li>After some simple initialization, the bootloader has to configure the A20 address line. This is one of the arcane x86 features the x86 architecture. If you are interested to understand it better, skim <a href="http://www.win.tue.nl/~aeb/linux/kbd/A20.html">this </a><a href="http://www.win.tue.nl/~aeb/linux/kbd/A20.html">article</a> .</li>
<li>The boot loader then switches the processor from real mode to <em>32-bit protected mode</em>, because it is only in this mode that software can access all the memory above 1MB in the processor’s physical address space. Protected mode is described briefly in sections 1.2.7 and 1.2.8 of <a href="http://pacman128.github.io/static/pcasm-book.pdf">PC Assembly Language</a> , and in great detail in the Intel architecture manuals. At this point you only have to understand that translation of segmented addresses (segment:offset pairs) into physical addresses happens differently in protected mode, and that after the transition offsets are 32 bits instead of 16.</li>
<li>The boot loader sets up the stack and starts executing the C code in bootmain.c.</li>
<li>Finally, the boot loader reads the kernel from the hard disk by directly accessing the IDE disk device registers via the x86’s special I/O instructions.</li>
</ol>
After you understand the boot loader source code, look at the files bootblock.asm. This file is a disassembly of the boot loader that our Makefile creates <em>after </em>compiling the boot loader. This disassembly file makes it easy to see exactly where in physical memory all of the boot loader’s code resides, and makes it easier to track what’s happening while stepping through the boot loader in

GDB.

You can set address breakpoints in GDB with the <strong>b </strong>command. You have to start hex numbers with 0x, so say something like <strong>b *0x7c00 </strong>sets a breakpoint at address 0x7C00. Once at a breakpoint, you can continue execution using the <strong>c </strong>and<strong>si </strong>commands: <strong>c </strong>causes QEMU to continue execution until the next breakpoint (or until you press <strong>Ctrl-C </strong>in GDB), and <strong>si <em>N </em></strong>steps through the instructions <em>N </em>at a time.

To examine instructions in memory (besides the immediate next one to be executed, which GDB prints automatically), you use the <strong>x/i </strong>command. This command has the syntax <strong>x/<em>N</em>i <em>ADDR</em></strong>, where <em>N </em>is the number of consecutive instructions to disassemble and <em>ADDR </em>is the memory address at which to start disassembling.

<strong>Exercise 3. </strong>

Take a look at the lab tools guide(refer last page of assignment) on GDB commands. Even if you’re familiar with GDB, this includes some esoteric GDB commands that are useful for OS work.

Set a breakpoint at address 0x7c00, which is where the boot sector will be loaded. Continue execution until that break point. Trace through the code in bootasm.S, using the source code and the disassembly file bootblock.asm to keep track of where you are. Also use the x/i command in GDB to disassemble sequences of instructions in the boot loader, and compare the original boot loader source code with both the disassembly in bootblock.asm and GDB.

Trace into bootmain() in bootmain.c, and then into readsect(). Identify the exact assembly instructions that correspond to each of the statements in readsect(). Trace through the rest of readsect() and back out into bootmain(), and identify the begin and end of the for loop that reads the remaining sectors of the kernel from the disk. Find out what code will run when the loop is finished, set a breakpoint there, and continue to that breakpoint. Then step through the remainder of the boot loader.

Answer the following questions:

<ul>
<li>At what point does the processor start executing 32-bit code? What exactly causes the switch from 16- to 32-bit mode?</li>
<li>What is the <em>last </em>instruction of the boot loader executed, and what is the <em>first </em>instruction of the kernel it just loaded?</li>
<li>How does the boot loader decide how many sectors it must read in order to fetch the entire kernel from disk? Where does it find this information?</li>
</ul>
<strong>Loading the Kernel</strong>

We will now look in further detail at the C language portion of the boot loader, in bootmain.c. But before doing so, this is a good time to stop and review some of the basics of C programming.

<strong>Exercise 4. </strong>

Read about programming with pointers in C. Then download the code for <a href="https://compas.cs.stonybrook.edu/~nhonarmand/courses/fa17/cse306/pointers.c">pointers.c</a> , run it, and make sure you understand where all of the printed values come from. In particular, make sure you understand where the pointer addresses in lines 1 and 6 come from, how all the values in lines 2 through 4 get there, and why the values printed in line 5 are seemingly corrupted.

We also recommend reading the <a href="https://blogs.oracle.com/ksplice/entry/the_ksplice_pointer_challenge">Ksplice pointer challenge</a> as a way to test that you understand how pointer arithmetic and arrays work in C.

<strong>Warning: </strong>Unless you are already thoroughly versed in C, do not skip or even skim this reading exercise. If you do not really understand pointers in C, you will suffer untold pain and misery in subsequent labs, and then eventually come to understand them the hard way.

To make sense out of bootmain.c you’ll need to know what an ELF binary is. When you compile and link a C program such as the xv6 kernel, the compiler transforms each C source (‘.c’) file into an <em>object </em>(‘.o’) file containing processor instructions encoded in the binary format expected by the hardware. The linker then combines all of the compiled object files into a single <em>binary image </em>such as kernel, which in this case is a binary in the ELF format, which stands for “Executable and Linkable Format”.

For our purposes, you can consider an ELF executable to be a header with loading information, followed by several <em>program sections</em>, each of which is a contiguous chunk of code or data intended to be loaded into memory at a specified address. The boot loader does not modify the code or data; it loads it into memory and starts executing it.

An ELF binary starts with a fixed-length <em>ELF header</em>, followed by a variable-length <em>program header </em>listing each of the program sections to be loaded. The C definitions for these ELF headers are in elf.h. The program sections we’re interested in are:

<ul>
<li>.text: The program’s executable instructions.</li>
<li>.rodata: Read-only data, such as ASCII string constants produced by the C compiler. (We will not bother setting up the hardware to prohibit writing, however.)</li>
<li>.data: The data section holds the program’s initialized data, such as global variables declared with initializers like int x = 5;.</li>
</ul>
When the linker computes the memory layout of a program, it reserves space for <em>uninitialized </em>global variables, such as int x;, in a section called .bss that immediately follows .data in memory. C requires that “uninitialized” global variables start with a value of zero. Thus there is no need to store contents for .bss in the ELF binary; instead, the linker records just the address and size of the .bss section. The loader or the program itself must arrange to zero the .bss section.

You can display a full list of the names, sizes, and link addresses of all the sections in the kernel executable by typing: $ <strong>objdump -h kernel</strong>

You will see many more sections than the ones we listed above, but the others are not important for our purposes. Most of the others are to hold debugging information, which is typically included in the program’s executable file but not loaded into memory by the program loader.

Take particular note of the “VMA” (or <em>link address</em>) and the “LMA” (or <em>load address</em>) of the .text section. The load address of a section is the memory address at which that section should be loaded into memory. In the ELF object, this is stored in the ph-&gt;p_pa field (in this case, it really is a physical address, though the ELF specification is vague on the actual meaning of this field).

The link address of a section is the memory address from which the section expects to execute. The linker encodes the link address in the binary in various ways, such as when the code needs the address of a global variable, with the result that a binary usually won’t work if it is executing from an address that it is not linked for. (It is possible to generate <em>position-independent </em>code that does not contain any such absolute addresses. This is used extensively by modern shared libraries, but it has performance and complexity costs, so we won’t be using it in this course.)

Typically, the link and load addresses are the same. For example, look at the .text section of the boot loader:

$ <strong>objdump -h bootblock.o</strong>

The BIOS loads the boot sector into memory starting at address 0x7c00, so this is the boot sector’s load address. This is also where the boot sector executes from, so this is also its link address. We set the link address by passing -Ttext 0x7C00 to the linker in Makefile, so the linker will produce the correct memory addresses in the generated code.

<strong>Exercise 5. </strong>

Trace through the first few instructions of the boot loader again and identify the first instruction that would “break” or otherwise do the wrong thing if you were to get the boot loader’s link address wrong. Then change the link address in Makefile to something wrong, run <strong>make clean</strong>, recompile the lab with <strong>make</strong>, and trace into the boot loader again to see what happens. <strong>Don’t forget to change the link address back and make clean again afterwards!</strong>

Look back at the load and link addresses for the kernel. Unlike the boot loader, these two addresses aren’t the same: the kernel is telling the boot loader to load it into memory at a low address (1 MB), but it expects to execute from a high address. We’ll dig in to how we make this work in the next section.

Besides the section information, there is one more field in the ELF header that is important to us, named e_entry. This field holds the link address of the <em>entry point </em>in the program: the memory address in the program’s text section at which the program should begin executing. You can see the entry point:

$ <strong>objdump -f kernel</strong>

You should now be able to understand the minimal ELF loader in bootmain.c. It reads each section of the kernel from disk into memory at the section’s load address and then jumps to the kernel’s entry point.

<strong>Exercise 6. </strong>

We can examine memory using GDB’s <strong>x </strong>command. The <a href="https://sourceware.org/gdb/onlinedocs/gdb/">GDB manual</a> has full details, but for now, it is enough to know that the command <strong>x/<em>N</em>x <em>ADDR </em></strong>prints <em>N </em>words of memory at <em>ADDR</em>. (Note that both ‘x’s in the command are lowercase.) <em>Warning</em>: The size of a word is not a universal standard. In GNU assembly, a word is two bytes (the ‘w’ in xorw, which stands for word, means 2 bytes).

Restart the machine (exit QEMU/GDB and start them again). Examine the 8 words of memory at 0x00100000 at the point the BIOS enters the boot loader, and then again at the point the boot loader enters the kernel. Why are they different? What is there at the second breakpoint? (You do not really need to use QEMU to answer this question. Just think.)

<strong>Link vs Load Address</strong>

The <em>load address </em>of a binary is the memory address at which a binary is <em>actually </em>loaded. For example, the BIOS is loaded by the PC hardware at address 0xf0000. So this is the BIOS’s load address. Similarly, the BIOS loads the boot sector at address 0x7c00. So this is the boot sector’s load address.

The <em>link address </em>of a binary is the memory address for which the binary is linked. Linking a binary for a given link address prepares it to be loaded at that address. The linker encodes the link address in the binary in various ways, for example when the code needs the address of a global variable, with the result that a binary usually won’t work if it is not loaded at the address that it is linked for.

In one sentence: the link address is the location where a binary <em>assumes </em>it is going to be loaded, while the load address is the location where a binary <em>is </em>loaded. It’s up to us to make sure that they turn out to be the same.

Look at the -Ttext linker option in Makefile, and at the address mentioned early in the linker script in kernel.ld. These set the link address for the boot loader and kernel respectively.

When object code contains no absolute addresses that encode the link address in this fashion, we say that the code is <em>position-independent</em>: it will behave correctly no matter where it is loaded. GCC can generate position-independent code using the -fpic option, and this feature is used extensively in modern shared libraries that use the ELF executable format. Position independence typically has some performance cost, however, because it restricts the ways in which the compiler may choose instructions to access the program’s data. We will not use -fpic in this course.

<strong>Part3: Adding a System Call</strong>

Now that we know how the kernel is compiled and loaded and gained basic familiarity with QEMU and GDB, it’s time to get our hands dirty with some kernel coding. Your task is to add a new system call to xv6. It will help to start by reading syscall.c (the kernel side of the system call table), user.h(the user-level header for the system calls), and usys.S (the user-level system call definitions).

You may add additional files to xv6 to implement this call.

<strong>Exercise 7. </strong>

Create a system call int sys_wolfie(void *buf, uint size), which copies an <a href="https://en.wikipedia.org/wiki/ASCII_art">ASCII art</a> image (Use a buffer of a wolf picture, google it for more information) of Wolfie to a user-supplied buffer, provided that the buffer is large enough. You are welcome to use an ASCII art generator, or draw your own by hand.

If the buffer is too small, or not valid, return a negative value. If the call succeeds, return the number of bytes copied.

You may find it helpful to review how other system calls are implemented and compiled into the kernel, such as read.

<strong>Exercise 8. </strong>

Write a user-level application, called wolfietest.c, that gets the Wolfie image from the kernel, and prints it to the console.

When the OS runs, your program’s binary should be included in fs.img and listed if someone runs <strong>ls </strong>at the xv6 shell’s command prompt. Study Makefile to figure out how to compile a user-mode program and add it tofs.img.

<strong>*This completes the lab assignment.</strong>

<strong>ex1.c</strong>

// Simple inline assembly example

// #include &lt;stdio.h&gt;

int

main(int argc, char **argv)

{&nbsp;&nbsp; int x = 1;

printf(“Hello x = %d\n”, x);

&nbsp;

//

// Put in-line assembly here to increment

// the value of x by 1 using in-line assembly

//&nbsp;&nbsp; printf(“Hello x = %d after increment\n”, x);

if(x == 2){&nbsp;&nbsp;&nbsp;&nbsp; printf(“OK\n”);

}&nbsp;&nbsp; else{&nbsp;&nbsp;&nbsp;&nbsp; printf(“ERROR\n”);

}

}

<strong>GDB Tool guide</strong>

See the <a href="http://sourceware.org/gdb/current/onlinedocs/gdb/">GDB manual</a> for a full guide to GDB commands. Here are some particularly useful commands for this course, some of which don’t typically come up outside of OS development.

<strong>Ctrl-c</strong>

Halt the machine and break in to GDB at the current instruction. If QEMU has multiple virtual CPUs, this halts all of them.

<strong>c </strong>(or <strong>continue</strong>)

Continue execution until the next breakpoint or Ctrl-c.

<strong>si </strong>(or <strong>stepi</strong>)

Execute one machine instruction.

<strong>b function </strong>or <strong>b file:line </strong>(or <strong>breakpoint</strong>)

Set a breakpoint at the given function or line.

<strong>b *<em>addr </em></strong>(or <strong>breakpoint</strong>)

Set a breakpoint at the EIP <em>addr</em>.

<strong>set print pretty</strong>

Enable pretty-printing of arrays and structs.

<strong>info registers</strong>

Print the general purpose registers, eip, eflags, and the segment selectors. For a much more thorough dump of the machine register state, see QEMU’s own info registers command. <strong>x/<em>N</em>x <em>addr</em></strong>

Display a hex dump of <em>N </em>words starting at virtual address <em>addr</em>. If <em>N </em>is omitted, it defaults to 1. <em>addr </em>can be any expression.

<strong>x/<em>N</em>i <em>addr</em></strong>

Display the <em>N </em>assembly instructions starting at <em>addr</em>. Using $eip as <em>addr </em>will display the instructions at the current instruction pointer.

<strong>Symbol-file <em>file</em></strong>

(Lab 3+) Switch to symbol file f<em>ile</em>. When GDB attaches to QEMU, it has no notion of the process boundaries within the virtual machine, so we have to tell it which symbols to use. By default, we configure GDB to use the kernel symbol file, obj/kern/kernel. If the machine is running user code, say hello.c, you can switch to the hello symbol file using symbol-file obj/user/hello.
