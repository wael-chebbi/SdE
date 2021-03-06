<b>Pentru TD1:</b>
* cerinta acestui laborator a fost crearea unui cont GitHub + o lista de studenti. 
 
<b>Pentru TD2:</b>
*Patron de conception producer-consumer: https://github.com/UPB-FILS/SE/blob/2013/2013/TD2/TD2.pdf
-fisierele aferente temei sunt incarcate in folderul TD2 si testate pe codeenv.com
- pasii realizarii temei au fost facuti in ordinea descrisa si in enuntul temei : citirea datelor dintr-un fisier, crearea de threaduri sincronizate.


<b>Pentru TD3:</b>
*Gestion FCFS des processus: https://github.com/UPB-FILS/SE/blob/2013/2013/TD3/TD3.pdf
- fisierele aferente temei sunt incarcate in folderul TD3 si testate pe codeenv.com

<b>Pentru TD6:</b>

*Virtual Memory Management Simulator
In this mini project you write a Java program that simulates translation from a virtual address to a physical address. The program will read from a file containing virtual addresses. It uses a page table as well as a TLB to translate the virtual address to the phyiscal address and outputs the physical address and the byte stored at that address. Let the phyiscal address space have a size of 65536 (=2**16) bytes. 
Your program will read a file containing several 32-bit integer numbers that represent the virtual addresses. You need only be concerned with 16-bit addresses. Thus take the 16 LSB into account. The 16-bit virtual address is divided into (1) an 8-bit page number and (2) 8-bit page offset. 
Other specifics include:

The page size is 256 (2**8) bytes
The number of entries in the page table is 256 (2**8)
The number of entries in the TLB is 16
The number of frames in the physical memory is 256 (Thus the memory size is 256*256=64K bytes)
Address Translation
Your program will translage the virtual address to the physical address using a TLB and a page table as outlined in section 8.4.2 (Figure 8.11) of the text book.

Test File The text file InputFile.txt provides integer values representing virtual addresses ranging from 0 through 65366. The value 65366 corresponds with the size of the virtual address space. Your program will open this file, read each virtual address, and translate it to the corresponding physical address. Then it will read and output the (signed) byte at the physical address.

How to Run your Program
If you adopt the package structure of the software distribution below your program should run like this:

    java opsys1.addressTranslationSim.VMsim InputFile.txt
Perhaps you may want to store the results of your program in a text file:
    java opsys1.addressTranslationSim.VMsim InputFile.txt > vmsim.out
Your program is to output the following values:
The virtual address being translated (read from InputFile.txt)
The corresponding physical address
The signed byte value stored at the translated physical address
Statistics
Whenever the program encounters an invalid virtual address (the corresponding valid bit in the page table is off) then it counts as a page fault. Second, the program should count the TLB hits and report the TLB hit ratio.

Resources
Package: opsys1.addressTranslationSim:
A template file for the simulator: VMsim.java.templ
Package: opsys1.vmm:
A page frame: Frame.java
A page table entry: PageTableEntry.java
A TLB (translation lookaside buffer) entry: TLBEntry.java
