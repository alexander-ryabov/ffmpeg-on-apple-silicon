# FFmpeg for ARM-based Apple Silicon Macs

I've successfully built FFmpeg on my M1 Mac Mini with the build script included in this repository which is based on [OSXExperts.NET Guide](https://www.osxexperts.net).

```bash
$ ./ffmpeg
ffmpeg version git-2020-12-09-8d19b3c Copyright (c) 2000-2020 the FFmpeg developers
  built with Apple clang version 12.0.0 (clang-1200.0.32.27)
  configuration: --prefix=/Volumes/tempdisk/sw --extra-cflags=-fno-stack-check --arch=arm64 --cc=/usr/bin/clang --enable-fontconfig --enable-gpl --enable-libopus --enable-libtheora --enable-libvorbis --enable-libmp3lame --enable-libfreetype --enable-libx264 --enable-libx265 --enable-libvpx --enable-libaom --enable-libvidstab --enable-version3 --pkg-config-flags=--static --disable-ffplay --enable-postproc --enable-nonfree --enable-runtime-cpudetect --enable-cross-compile --cc=/usr/bin/clang
  libavutil      56. 62.100 / 56. 62.100
  libavcodec     58.115.102 / 58.115.102
  libavformat    58. 65.100 / 58. 65.100
  libavdevice    58. 11.103 / 58. 11.103
  libavfilter     7. 92.100 /  7. 92.100
  libswscale      5.  8.100 /  5.  8.100
  libswresample   3.  8.100 /  3.  8.100
  libpostproc    55.  8.100 / 55.  8.100
Hyper fast Audio and Video encoder
usage: ffmpeg [options] [[infile options] -i infile]... {[outfile options] outfile}...

Use -h to get full help or, even better, run 'man ffmpeg'
$ lipo -archs ffmpeg
arm64
```

## Guide

Before you start you must install arm64-based Homebrew to `/opt/homebrew`.

1. Clone this repository.
2. Run `./build.bash`.
