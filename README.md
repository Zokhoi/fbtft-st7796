# FBTFT driver for ST7796 (?)

Tested with linux kernel 5.10.160

**Caution**: The store I bought the display from lists the panel as ST7796U, but when I try to use [initialization sequence for ST7796](https://github.com/birdtechstep/tinydrm/blob/master/st7796.c#L112-L196) it didn't work. However I used the sequence for ST7789 and it worked. Thus this driver contains ST7789 init sequence, and you can override it in `init` property if it doesn't work for you.

## Usage
```sh
make
make install
depmod -A
```

