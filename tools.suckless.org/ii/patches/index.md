Patches
=======

diff generation
---------------
For git users:

    cd ii-directory
    git diff > ii-X.Y-yourpatchname.diff

For tarballs:

    cd modified-ii-directory/..
    diff -up original-ii-directory modified-ii-directory > ii-X.Y-yourpatchname.diff

where `X.Y` is an ii tag name or version number.


patch application
-----------------
For git users:

    cd ii-directory
    git apply path/to/patch.diff

For tarballs:

    cd ii-directory
    patch -p1 < path/to/patch.diff
