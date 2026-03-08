# CoCoBASIC - a bunch of BASIC programs for the Tandy Color Computer (CoCo)

## colordle

A wordle clone for the CoCo1/2/3. A disk image can be [downloaded](https://colorcomputerarchive.com/repo/Disks/Games/Colordle%20(Paul%20Ripke).zip) from colorcomputerarchive.com, or even [play](https://colorcomputerarchive.com/xroar-online/?machine=cocous&basic=RUN%22COLORDLE%22%5cr&cart=rsdos&disk0=/unzip%3Ffile%3DDisks/Games/Colordle%20(Paul%20Ripke).zip/colordle.dsk) online!

* `colordle.bas`: The game in BASIC.
* `makeidx.bas`: Rebuild the `guesses.idx` file from `guesses.dat`. This is used to shortcut the binary search when validating guesses.
* `guesses.dat`: Full 5-letter word list based on Collins Scrabble List, 2019, all words concatenated with no separators.
* `words.dat`: List of "common" words, concatenated.

Amusingly, I tripped over a 40-year old ROM bug while writing this - you can read more about that [here](https://www.stix.id.au/wiki/2022-03-01_Retro_Computing_Microsoft%27s_BASIC_%22ST_ERROR%22).

## utils

A bunch of simple utilities I have written over the years.

* `benchmrk.bas`: Simple BASIC program that benchmarks a bunch of BASIC functions and operations. See also my [blog post](https://www.stix.id.au/wiki/2023-05-06_Benchmarking_BASIC_on_a_Tandy_CoCo1).
* `benchmrk.txt`: Output of `benchmrk.bas` when run under [xroar](https://www.6809.org.uk/xroar/).
* `bininfo.bas`: Dump the binary preamble and postamble for a `BIN` file; the load address and length of each segment, and the execution address.
* `cat.bas`: Efficiently dump a disk file to the screen.
* `fsck.bas`: Check the integrity of the RDOS filestructures for the given disk. Note: unlike `fsck` on Unix, no repair operation is offered; that's up to you.
* `hexdump.bas`: Dump the contents of a disk file out in hexadecimal and ASCII to the screen, and allow paging around the file (" " or <enter> to advance, "-" or "B" to go back, "Q" to quit).