# useless gap

## Description

This patch adds useless gap between windows and removes everything (gap and border) in monocle mode for aesthetic purpose. 
The size of the gap is configured in config.def.h.

## Example

	Original look :
	+-----------------+-------+
	|                 |       |
	|                 |       |
	|                 |       |
	|                 +-------|
	|                 |       |
	|                 |       |
	|                 |       |
	+-----------------+-------+


	New look :
	+----------------++-------+
	|                ||       |
	|                ||   N   |
	|                ||       |
	|                |+-------+
	|                |+-------+
	|                ||       |
	|                ||       |
	|                ||       |
	+----------------++-------+

## Download

 * [dwm-5.9-uselessgap.diff](dwm-5.9-uselessgap.diff) (1.8k) (20110107 updated. Thanks Jordan for your bug report)
   
	Update to use the new resizeclient() function instead of resize()
 
 * [dwm-uselessgap-5.8.diff](historical/dwm-uselessgap-5.8.diff) (1.7k) (20100225 updated. Thanks Guillaume for your bug report)
   
	Fix floating clients bug and remove all borders in monocle mode.
 
 * [dwm-gap-5.7.2.diff](historical/dwm-gap-5.7.2.diff) (0.7k) (20091215)

## Author

 * Jerome Andrieux - <jerome@gcu.info>
