Goals
=====

This page is to discuss and maybe add comments on the future of st.

TODO
----
* see the TODO file in the [repository](http://git.suckless.org/st/plain/TODO)

Theoretical features
--------------------
* st should keep a pointer to the beginning of the oldest line, because we
  would like to keep lines and not part of them (pancake)
* Edit previous text in the terminal like in Plan 9 and 9term (jt_)
* add your feature request here

Goals
-----
- have a working graphical terminal for terminal applications
- do no reimplement tmux and his comrades

Non-goals
---------
- filters that change colour (should be done by tmux or something doing the
  higher layers *in* st)
- server to save sessions in case of X crash (should be done by dtach)
- unlimited scrollback buffer (done by dvtm) 
- URL selecting/launching in browser similiar to vimperator's mark mode and the
  urxvt script (patch?) (possibly piped through something like plumb to
  	- This one is done by a simple shortcut in dwm which will launch your
	  plumber on the current select buffer. St has easy select through
	  double-click. This keeps the complex logic out of the st context.

Links
-----
* [Repository](http://git.suckless.org/st)

