# Bootrom

This is a simple bootrom that runs when a PC boots up. It looks for a file called "init.elf" at the root of any attached drive and loads it.

## Building

Assuming that you have a compiler for the target triplet `mipsel-unknown-elf`:

```shell
make
```

The bootrom doesn't get rebuilt automatically, so you'll have to rebuild it manually before compiling the mod if you changed it.
