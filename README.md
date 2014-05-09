CE5
===

Part 1
===


addi $s0, $0, 44

addi $s1, $0, -37

addi $s2, $s0, $s1

sw $s2, 0x54($0)


Part 2
===

Conversion to hex

0x2010002C

0x2011FFDB

0x02119020

0xAC120054

Program 2 Waveform

![alt text](http://i57.tinypic.com/25jky0n.png)

Walking through teh test bench, you can see that the program works because the program stores -37 and 44 into registers 16 and 17 (both of which are dispplayed in hexidecimal) 


Part 3
===
Updated Schematic
![alt text](http://i62.tinypic.com/242bpue.jpg)


updated ALU Decoder Table and Main Decoder table
![alt text](http://i61.tinypic.com/2ljt4s8.jpg)



part 3 waveform
![alt text](http://i61.tinypic.com/w2irzk.png)

To check my waveform, I looked to see if the aluout value was 8007, which is what I was supposed to get for ori.  Looking at my waveform picture, 00008007 is in the correct place (aluout) at approximately 30 ns


Documentation: C3C Austin Bolinger explained how I needed to increase the number of bits for alusrc and create a second mux to choose between zeroext and signext.  After that, it was simply a matter of modifying the mips.vhd code using things that were already in the code.
