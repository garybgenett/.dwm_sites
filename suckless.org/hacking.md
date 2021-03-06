Hacking
=======

Debugging
---------
If you find any crashes, please send a full backtrace to the dedicated mailing list.
You can create backtraces with `gdb`:

Before starting a program, you may have to allow core file creation. It is
recommended that you put this in your profile:

    $ ulimit -c unlimited

Then start the program as usual.

After the program crashes, do the following:

    $ gdb -q `which program` /path/to/core
    gdb> bt full

If you encounter freezes (no crash at all) of the program, you can debug as follows:

    $ gdb -q `which program` --attach `pgrep -o  program`
    gdb> bt full

Send the output of that command to the mailing list along with the output of
`program -v`! Thank you!


Patches
-------

diff generation
---------------
For git users:

    cd program-directory
    git diff > program-X.Y-yourpatchname.diff

For tarballs:

    cd modified-program-directory/..
    diff -up original-program-directory modified-program-directory > program-X.Y-yourpatchname.diff

where `X.Y` is a dwm tag name or version number.

patch program
-------------
For git users:

    cd program-directory
    git apply path/to/patch.diff

For tarballs:

    cd program-directory
    patch -p1 < path/to/patch.diff

