XBOMB Version 2.3
=================

A program that looks superficially like the minesweeper program that
comes supplied with MS Windows (and is also available in other
versions). Runs under X Windows on the UNIX operating system.

Screenshot
--------
![Screenshot](Screenshot_20210810_145906.png?raw=true "Screenshot")

Features
--------

There are a number of features that make this version different from
the others available (that I have seen).

3 Grid Tile options

        Hexagonal      - Easy (the endgame can be difficult).
        Square         - Traditional.
        Triangular     - Difficult.

3 Grid sizes

        Small          - 8x8 with 10 bombs
        Medium         - 16x16 with 40 bombs
        Large          - 30x16 with 99 bombs

Cipher mode

        The numbers have been encrypted with a substitution cipher.
        Blank still means zero.

Highscore table

        10 entries for the fastest times for each of the 3 levels of
        each of the 3 grid shapes.

Playing the game
----------------

Located under the tiles of the grid are a number of unexploded
bombs. The target of the game is detect the location of the bombs
given only the number of bombs neighbouring each of the locations
known to have no bomb. Locations known to contain bombs, are marked
and the game finishes when all locations are uncovered or marked.

Left mouse button

                      Uncover the current location if not already done.
                      Else, same as the middle mouse button.
Middle mouse button

                      Uncover all adjacent cells not marked as bombs if the
                      number of marked cells equals the displayed number.
                      Disabled in cipher mode as the player may not know which
                      number is which.
Right mouse button

                      Mark a cell as being known to contain a bomb (toggles).

's' key             - Start a new game

'c' key             - Toggle cipher mode

'q' key             - Quit the game

'h' key             - Print the high score table for the current grid shape.

'1','2' or '3' key  - Select game level 1, 2 or 3.

'H','S' or 'T' key  - Select game type Hexagon, Square or Triangle grid.

Installation
------------

Edit the Makefile to set the paths for installation (INSTDIR), X
windows libraries (XLIB) and the compiler options (CC, CFLAGS).

make xbomb

make install

And all should be OK.

On Ubuntu, compile.sh installs the needed libraries and makes the xbomb executable.

This program has been tested on the following systems:

Linux 1.x, 2.x
SunOS 4.1.x
Solaris 2.x

Author & Copyright
------------------

Andrew M. Bishop  (XBomb first written late 1994/early 1995)

This program is Copyright Andrew M. Bishop 1995-2014 and distributed under GPL.

More information: http://www.gedanken.org.uk/software/xbomb/
