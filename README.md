# soundfont repository tool (sf2repo)

**Version 0.0.1**
---

The primary purpose of this tool is to decompose a soundfont 2 (sf2) format files so that it
can be stored and maintained within a git or other type of source control repository.
A sf2 file is a binary file that is too large to be stored in a source control repository
which then makes it difficult for different authors to collaborate on the same soundfont.

This project aims to decompose a sf2 file into many smaller text and wave files
corresponding to each of the Samples, Instruments and Presets contained in the soundfont.
These separate files can then be checked in and tracked by the source control system.


## About

This code is based on two command line tools called 'sf2dump' and 'sf2extract'
which are part of the open-source 'libgig' project available at:
 http://www.linuxsampler.org/libgig/

## Future

It is planned code will be written at some point that will allow the original
sf2 to be recreated that is an exact match of the original and has the same md5sum.
