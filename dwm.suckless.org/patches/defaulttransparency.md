# defaulttransparency

## Description

This patch adds a default transparency parameter to config.h, which specifies the
transparency, all windows are started with.

Additionally it adds some shortcuts:

 * MOD + Shift + s -> decrease transparency of current focused window
 * MOD + Shift + d -> increase transparency of current focused window
 * MOD + Shift + f -> set window to default opacity (.75)

It is based on the transparency patch of Stefan Mark.

## Download

 * [dwm.defaultopacity.patch](http://dwm.suckless.org/patches/dwm.defaultopacity.patch)
   latest patch (against r1521)

## Author

 * Christoph Lohmann - <20h@r-36.net>

