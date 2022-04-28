# Getting Start

```sh
gcc -c liba.c
gcc -c libb.c
gcc -c libd.c

ar rs libx.a liba.o libb.o libd.o
# link libx.a with whole archive, other archive with no whole archive
gcc main.o -static -Wl,--whole-archive,-lx -L . -Wl,--nowhole-archive,-Ma
```
