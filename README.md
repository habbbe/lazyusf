lazyusf
=======

Converter for Ultra 64 Sound Format (usf and miniusf) by Josh W (http://joshw.info) based on 64th Note.

This tool is based on JoshW's audacious plugin "lazyusf". It was rewritten to a standalone commandline tool.

## Build
```bash
cmake .
```
```bash
make
```
#### Build Dependencies
* cmake
* make
* gcc
* gcc-c++
* [optional] flac-devel: needed if you wish to write directly to .flac files
* [optional] libao-devel: needed if you want support for on-the-fly playback

## Usage
```bash
lazyusf [OPTIONS] "soundtrack name.miniusf"
```
By default the PCM output is written to "soundtrack name.miniusf.au". For more help run lazyusf without any parameters.



## FAQ
Q: The output of Donkey Kong 64 is slower than in the original game.

A: DK64 internally samples at 21617 Hz; the output of the game was at 22050 Hz. Enable rounding the samplerate by using the -r option.

## TODO
* be able to specify multiple files to play sequentially
* be able to switch between those files
* adapt usage function
* adapt SIGINT and SIGTERM
