Reading and Writing Audio Files in Python
=========================================

[back to main page](http://github.com/mgeier/python-audio/blob/master/README.md)

There are several libraries for reading and writing audio files with Python but
it's often not clear which is the best one. That's mostly because there is no
single best one. Each one has a different set of features and limitations,
different availability on different platforms and different ease of use.

This directory shows a few of the available libraries along with some advantages
and disadvantages as well as some usage examples.

Most of the mentioned libraries can be used on multiple platforms.

File Formats
------------

There are a lot of digital audio formats available, but each one of them falls
into one of two categories: either it's a lossless or a lossy format.  Files in
lossy formats (e.g. Ogg-Vorbis, MP3) are normally much smaller because
information which is contained in the original signal but is (ideally) not
audible is thrown away. When using a lossless format, the original signal can be
perfectly restored, either because no compression is used at all (e.g. WAV) or
the compression doesn't loose information (e.g. FLAC).

If you want to distibute your latest song on the internet you might want to use
a lossy format to save some bandwidth, if you plan to further process your data
(or if you are aiming at a high-end crowd) you should choose a lossless format.

The lowest common denominator for exchanging audio files is probably the MS WAV
format. But although it is widely supported, only few programs support all
variants of this format. WAV files support both fixed point and floating point
numbers. Very popular are 16-bit fixed point (PCM) values, as this is the format
of Audio CDs.
Some professional recordings use 24-bit PCM data. 32-bit PCM data is also
possible, but this practically never used.

32-bit floating-point data, however, are widely used by digital audio
workstations (DAWs), so you may encounter those.
As most audio processing applications use 32-bit floating-point data internally,
this is also a meaningful data type for file exchange between applications.

TODO: `WAV_PCM` vs. `WAVEX`

TODO: range of values, e.g. 16-bit: -32768 to 32767

Conversion to Other Formats
---------------------------

For most cases it should be sufficient to support the various variants of WAV
files. There are many conversion programs which allow to convert to and from
many other formats.
Probably the most powerful is [SoX](http://sox.sf.net/) -- highly recommended!
To create `.ogg` and `.mp3` files, for example, [oggenc](http://www.vorbis.com/)
and [LAME](http://lame.sourceforge.net/) can be used, respectively.

Example Files
-------------

Example WAV files with different encodings are available in the directory
[data/](data/). These files were generated with the script
[`generate_example_wav_files.py`](data/generate_example_wav_files.py).

Python Sound File Libraries
---------------------------

TODO: nbviewer link!
[scipy.io](http://nbviewer.ipython.org/)

TODO: more!

<!--
vim:textwidth=80
-->