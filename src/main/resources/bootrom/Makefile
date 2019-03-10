CC=mipsel-unknown-elf-gcc
OBJCOPY=mipsel-unknown-elf-objcopy

boot.bin: bootrom.c bootrom.ld
	$(CC) -G0 -g -Os -fno-toplevel-reorder -mhard-float -fomit-frame-pointer -Wl,-T,bootrom.ld -nostdlib -o boot.elf bootrom.c
	$(OBJCOPY) -Obinary boot.elf boot.bin

.PHONY: clean

clean:
	rm -f boot.elf boot.bin