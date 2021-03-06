# tag all #

## Description ##

Shortcut to move all (floating) windows from one tag to another.

## Download ##
Patches against different versions of dwm are available at
[dwm-clean-patches](https://github.com/jceb/dwm-clean-patches).

 * [dwm-6.1-tagall.diff](dwm-6.1-tagall.diff) (1058b) (20140209)
 * [dwm-10e232f9ace7-tagall.diff](dwm-10e232f9ace7-tagall.diff) (988b) (20120406)
 * [dwm-6.0-tagall.diff](dwm-6.0-tagall.diff) (988b) (20120406)

## Configuration ##

 * MODKEY+Shift+F1 moves all floating windows of the current tag to tag 1

    { MODKEY|ShiftMask,     XK_F1,      tagall,        "F1" }, \
    ...
    { MODKEY|ShiftMask,     XK_F9,      tagall,        "F9" }, \

 * MODKEY+Shift+F1 moves all windows of the current tag to tag 1

    { MODKEY|ShiftMask,     XK_F1,      tagall,        "1" }, \
    ...
    { MODKEY|ShiftMask,     XK_F9,      tagall,        "9" }, \

## Author ##
 * Jan Christoph Ebersbach - <jceb@e-jc.de>
