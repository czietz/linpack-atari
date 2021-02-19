# LINPACK benchmark for Atari TOS

This is the [famous LINPACK benchmark](https://en.wikipedia.org/wiki/LINPACK_benchmarks) to measure the floating-point performance of Atari machines running TOS (or MiNT). It requires at least a 68020 CPU and a FPU. It solves a linear equation system and is used to evaluate the performance of computers and super-computers since 1979.

The source code for `linpack.tos` was taken verbatim from this C version of the Benchmark: http://www.netlib.org/benchmark/linpackc.new.

The original benchmark (written in FORTRAN) is also included as `linpackd.tos`. The source code was taken from here: http://www.netlib.org/benchmark/linpackd. This was compiled with [GNU Fortran 8.3.0](http://tho-otto.de/crossmint.php).

## Results

Note that to some degree the results depend on the compiler that is used and on its options. All subsequent results were obtained with the binary of the *C version* of the benchmark (`linpack.tos`) in this repository, with double precision and using the default array size (200) when prompted.

System | Result in kFLOPS | Remarks
--- | ---: | ---
ST with PAK/2 68020 and 68881 FPU @ 25 MHz | 85 | Source: https://forum.atari-home.de/index.php/topic,15025.msg249259.html#msg249259
Falcon @ 16 MHz + 68882 FPU | 111 | Source: https://forum.atari-home.de/index.php/topic,15025.msg254358.html#msg254358
PAK68/3-020 + 68881 FPU, both @ 32 MHz | 180 | Source: https://forum.atari-home.de/index.php/topic,15025.msg254546.html#msg254546
Stock TT, FPU @ 32 MHz | 217 | Source: https://forum.atari-home.de/index.php/topic,15025.msg237349.html#msg237349
TT, CPU & FPU accelerated @ 48 MHz | 281 |
PAK68/3-020 + 68882 FPU, both @ 40 MHz | 343 | Source: https://forum.atari-home.de/index.php/topic,15025.msg254585.html#msg254585
CT2A Falcon | 415 | Source: https://forum.atari-home.de/index.php/topic,15025.msg237349.html#msg237349
Milan040 under MagiC | 1695 | Source: https://forum.atari-home.de/index.php/topic,15025.msg237349.html#msg237349
Milan060 | 4144 | Source: https://forum.atari-home.de/index.php/topic,15025.msg237349.html#msg237349
CT63 @ 95 MHz under MiNT | 7590 | Source: https://forum.atari-home.de/index.php/topic,15025.msg237349.html#msg237349
Vampire V4SA @ 85 MHz (core January 2021) | 8663 | Source: https://www.atari-forum.com/viewtopic.php?p=412437#p412437

A long list of results of different systems is available in the report [“Performance of Various Computers Using Standard Linear Equations Software”](https://www.netlib.org/benchmark/performance.pdf).
