zoomswap
========

Description
-----------
This patch swaps the current window (C) with the previous master (P) when zooming.

	Original behaviour :
	+-----------------+-------+
	|                 |       |
	|                 |       |
	|                 |       |
	|        P        +-------|
	|                 |       |
	|                 |   C   |
	|                 |       |
	+-----------------+-------+

	+-----------------+-------+
	|                 |       |
	|                 |   P   |
	|                 |       |
	|        C        +-------|
	|                 |       |
	|                 |       |
	|                 |       |
	+-----------------+-------+


	New Behaviour :
	+-----------------+-------+
	|                 |       |
	|                 |       |
	|                 |       |
	|        C        +-------+
	|                 |       |
	|                 |   P   |
	|                 |       |
	+-----------------+-------+

Download
--------
Patches against different versions of dwm are available at
[dwm-clean-patches](https://github.com/jceb/dwm-clean-patches).

 * [dwm-6.1-zoomswap.diff](dwm-6.1-zoomswap.diff) (2585b) (20120406)
 * [dwm-10e232f9ace7-attachabove.diff](dwm-10e232f9ace7-attachabove.diff) (1.7K) (20120406)
 * [dwm-6.0-zoomswap.diff](dwm-6.0-zoomswap.diff) (1.6K) (20120406)

Author
------
 * Jan Christoph Ebersbach - `<jceb at e-jc dot de>`
