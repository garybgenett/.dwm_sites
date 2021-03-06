# gapless grid layout

## Description

This patch is an altered [gridmode](historical/gridmode) layout for dwm,
which arranges the windows in a grid.
Instead of using a regular grid, which might leave empty cells when there are
not enough windows to fill the grid, it adjusts the number of windows in the
first few columns to avoid empty cells.

## Usage

Download `gaplessgrid.c` and add the gapless layout to your `config.h`:

	#include "gaplessgrid.c"
	
	static const Layout layouts[] = {
		/* symbol     arrange function */
		{ "###",      gaplessgrid },
	...
	
	static Key keys[] = {
		/* modifier                     key        function        argument */
		{ MODKEY,                       XK_g,      setlayout,      {.v = &layouts[0] } },
	...

## Download

* [dwm-6.1-gaplessgrid.diff](dwm-6.1-gaplessgrid.diff) (1180b) (20140209)
* [gaplessgrid.c](gaplessgrid.c) (dwm 5.6.1) (20090908)
* [dwm-r1437-gaplessgrid.diff](historical/dwm-r1437-gaplessgrid.diff) (1.9k) (20090704)
* [dwm-5.2-gaplessgrid.diff](historical/dwm-5.2-gaplessgrid.diff) (1.9k) (20081020)
