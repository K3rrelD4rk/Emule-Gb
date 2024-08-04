# Emule-Gb

Emulatore GameBoy in C

Notes on Gb Hardware:
CPU:
 - Mix between Z80 and Intel 8080
 - runs at ~4.19 MHz
 - I/O ports are not available. Components need to be completly memory-mapped.
 - Only 7 general purpose registers
 - includes Z80's extended bit manipulation istructions
 - LDH istruction to operate last 256 bytes with start adrr '$ff00' and fits in one fewer byte
BUS:
 - 8bit data bus and 16bit addr bus
MEMORY MAP:
 - Game Pak space ( Game Cartridge)
 - Work RAM, High RAM, Display RAM
 - I/O (joypad, audio, graphics and LCD)
 - Interrupt controls
RAMs:
 - Work RAM (8Kb of RAM)
 - High RAM (127B of RAM) has a small space for faster access thru LDH istructions ( Generally Slower, only for CPU )
 - VRAM (32Kb ) uses a bank switcher ( same as NES ), the last 4 KB can be swapped using 7 different banks. extra register (SVBK) acting as bank switche, used to examine ext mem
 
