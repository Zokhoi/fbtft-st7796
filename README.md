# FBTFT driver for ST7796 (?)

Tested with linux kernel 5.10.160

**Caution**: The store I bought the display from lists the panel as ST7796U, but when I try to use [initialization sequence for ST7796](https://github.com/birdtechstep/tinydrm/blob/master/st7796.c#L112-L196) it didn't work. However I used the sequence for ST7789 and it worked, but I still had to use [ST7796's screen orientation settings](https://github.com/birdtechstep/tinydrm/blob/master/st7796.c#L179-L196), so I'm not sure which controller it actually is. If it doesn't work for you, you can override it in `init` property.

## Usage
```sh
make
make install
depmod -A
```

