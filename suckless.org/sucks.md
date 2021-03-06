Stuff that sucks
================
See the [philosophy](http://suckless.org/philosophy) page about what
applies to this page. 

Libraries
---------
These libraries are broken/considered harmful and should not be used if it's
possible to avoid them. If you use them, consider looking for alternatives.

* [glib][1] - implements C++ STL on top of C (because C++ sucks so much, let's
  reinvent it!), adding lots of useless data types for
  ["portability" and "readability" reasons][2].
  even worse, it is not possible to write robust applications using glib,
  since it [aborts in out-of-memory situations][8].
  glib usage is required to write gtk+ and gnome applications, but is also used
  when common functionality is needed (e.g. hashlists, base64 decoder, etc).
  it is not suited at all for static linking due to its huge size.
  
  Alternatives: [libmowgli][9], [libulz][10]

* [GMP][3] - GNU's bignum/arbitrary precision library. Quite bloated, slow and
  [calls abort() on failed malloc][4]
  
  Alternatives: [libtommath][5], [TomsFastMath][6], [MPI][7]


[1]: http://library.gnome.org/devel/glib/
[2]: http://library.gnome.org/devel/glib/unstable/glib-Basic-Types.html (glib Basic Types)
[3]: http://gmplib.org/ (The GNU Multiple Precision Arithmetic Library)
[4]: http://gmplib.org:8000/gmp/file/14cd74efb9de/memory.c#l44 "GMP calls abort() on failed malloc()"
[5]: http://libtom.org/?page=features&newsitems=5&whatfile=ltm
[6]: http://libtom.org/?page=features&newsitems=5&whatfile=tfm
[7]: http://spinning-yarns.org/michael/mpi/
[8]: https://bugzilla.gnome.org/show_bug.cgi?id=674446
[9]: https://github.com/atheme/libmowgli-2
[10]: https://github.com/rofl0r/libulz

Build Systems
-------------

* [cmake][11] - cmake is written in C++ but often used to compile C programs.
  that means (on a self-bootstrapping system) that one needs to compile a C++
  compiler and cmake just in order to be able to build some C code.
  it is so huge and bloated that compilation takes more time than compilation
  of GCC (!).
  it's not even possible to use it to create freestanding Makefiles, since
  the generated Makefiles call back into the cmake binary itself.

  Alternatives: [gnu make][14]

* [waf][12] and [scons][13] - waf/scons are both written in python but often
  used to compile C programs.
  that means (on a self-bootstrapping system) that one needs to compile python
  in order to be able to build some C code.
  waf code is dropped into the compilee's build tree, so it does not benefit
  from updated versions and bugfixes.

  Alternatives: [gnu make][14]

[11]: http://www.cmake.org/
[12]: https://code.google.com/p/waf/
[13]: http://www.scons.org/
[14]: https://www.gnu.org/software/make/

Programs
--------
There are many broken X programs. Go bug the developers of these broken
programs to fix them. Here are some of the main causes of this brokenness:

* The program assumes a specific window management model, i.e.
  assumes you are using a WIMP-window manager like those
  found in KDE or Gnome. This assumption breaks the 
  [ICCCM conventions][icccm].
* The application uses a fixed size - this limitation does not fit
  into the world of tiling window managers very well, and can also be
  seen as breaking the ICCCM conventions, because a fixed sized window
  assumes a specific window management model as well (though the ICCCM
  does not forbid fixed-size windows). In any case, the ICCCM requests
  that clients accept any size the window manager proposes to them.
* The program is based on strange non-standard window manager
  hints that only work properly with a window manager supporting these
  extensions - this simply breaks the ICCCM as well. E.g. trash icon
  programs.
* The program does not conform to ICCCM due to some missing or
  improperly set hints.

Workarounds
-----------

If you still need some program which expects a floating WM, use it in
floating mode.

The following programs are broken (see [rocking stuff](/rocks) for saner alternatives):

* XMMS (assumes fixed size, doesn't set transient\_for hint properly)
* Xchat
* [Firefox](http://www.mozilla.org/products/firefox) (doesn't set the TRANSIENT\_FOR hint correctly on its download dialog)
* beep-media-player
* gqview
* gthumb
* mplayer with GUI (assumes special window management model. It works without the GUI)
* xine (same as xmms)
* aterm (doesn't like being resized by the WM), See [aterm-ml-post][aterm-ml-post]  
	Alternatives: (u)xterm, urxvt, [st][st], [uuterm][uuterm]

See also
--------

The [list of harmful software](http://harmful.cat-v.org/software/) at [cat-v.org](http://cat-v.org).

[aterm-ml-post]: http://lists.suckless.org/dev/1102/7141.html
[st]:     http://st.suckless.org/
[uuterm]: http://etalabs.net/uuterm.html
[icccm]:  http://tronche.com/gui/x/icccm/
