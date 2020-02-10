# ARM926EJ-S-Bare-Metal-Examples
My firsts programs written for ARM926EJ-S in Bare Metal (without operating system).
### Requirements
 - arm-none-eabi-gcc (for compiling);
 - QEMU (for simulation).
### How to compile
    $ arm-none-eabi-as -mcpu=arm926ej-s -g startup.s -o startup.o
    $ arm-none-eabi-gcc -c -mcpu=arm926ej-s -g test.c -o test.o
    $ arm-none-eabi-ld -T test.ld test.o startup.o -o test.elf
    $ arm-none-eabi-objcopy -O binary test.elf test.bin
### How to simulate
    $ qemu-system-arm -M versatilepb -m 128M -nographic -kernel test.bin
### Examples
 - return 0;
 - Hello world by an UART.
