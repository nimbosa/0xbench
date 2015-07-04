## Current included benchmarks ##
There are currently 16 included benchmarks. Two for arithmetic performance, seven for 2D rendering, four for 3D rendering, one for Dalvik, and two native benchmarks for system performance.

### Arithmetic ###
  1. Linpack
> > The Linpack Benchmark make use of a general numerical linear algebra operation to test the device's ability to perform floating point operations (MFLOPS). For detail please refer to [Wikipedia](http://en.wikipedia.org/wiki/LINPACK), [netlib.org](http://www.netlib.org/benchmark/linpackjava/), [cs.cmu.edu](http://www.cs.cmu.edu/~jch/java/linpack.html). The original source can be found online here: [Source code](http://www.cs.cmu.edu/~jch/java/LinpackLoop.java).
  1. Scimark2
> > The Scimark2 Benchmark Suite includes several scientific calculation (including FTT, MonteCarlo ..etc) for testing the device's abilitity to perform floating point operations (MFLOPS). For detail please refer to [nist.gov](http://math.nist.gov/scimark2/).

### Web ###
  1. SunSpider
> > SunSpider is a JavaScript benchmark. This benchmark tests the core JavaScript language only, not the DOM or other browser APIs. It is designed to compare different versions of the same browser, and different browsers to each other.

### 2D ###
  1. Canvas Redraw
> > Use random color to redraw canvas repeatedly, and calculate the refresh rate. Note that the refresh rate of this benchmark should (may) be bounded by the device's vertical synchronization (vsync). (60fps for many Android phones, including Nexus One, HTC Hero, HTC Desire)
  1. Draw Circle
> > A simple 2D animation program. Calculate the refresh rate.
  1. DrawRect
> > Repeatedly add random colored, size rectangles on canvas.
  1. DrawCircle2
> > Repeatedly render random colored, size circles on canvas.
  1. DrawArc
> > Simple 2D animation.
  1. DrawText
> > Calculate text rendering speed.
  1. DrawImage
> > Calculate picture rendering speed.
### 3D ###
  1. GL Cube
> > A sample program from the Android API Demo that uses OpenGL ES to render a rotating Rubik's Cube.
  1. GL Teapot
> > Use OpenGL ES to render a rotating Utah Teapot ([Wikipedia](http://en.wikipedia.org/wiki/Utah_teapot)). Adapted from [android-utah-teapot](http://code.google.com/p/android-utah-teapot/) project (which uses source code from Android SDK sample programs and iPhone SDK sample programs).
  1. NeHe Lesson08
> > A rotating 3D cube with textured applied and alpha blending enabled. For detail please refer to [nehe.gamedev.net](http://nehe.gamedev.net/lesson.asp?index=02)(blending). For source code and explanation please refer to [NeHe lesson08](http://nehe.gamedev.net/data/lessons/lesson.asp?lesson=08).
  1. NeHe Lesson16
> > A rotating 3D cube with textured applied and GLFog enabled. For detail please refer to [nehe.gamedev.net](http://nehe.gamedev.net/lesson.asp?index=04)(Cool look fog). For source code and explanation please refer to [NeHe lesson16](http://nehe.gamedev.net/data/lessons/lesson.asp?lesson=16).
### Dalvik ###
  1. Garbage Collection
> > Test the performance of the garbage collection mechanism on the Dalvik VM. For detail please refer to [hpl.hp.com](http://www.hpl.hp.com/personal/Hans_Boehm/gc/gc_bench.html).  The original source can be found online here: [GCBench.java](http://www.hpl.hp.com/personal/Hans_Boehm/gc/gc_bench/GCBench.java)
### Native ###
  1. LibMicro
> > A portable set of microbenchmarks that executes abundant system calls to measure the performance of different system and library calls (bionic). Since calling system functions directly is required,  this benchmark depends on a set of executable files that needs to be deployed in advance. (Which requires root permission of your device) More information on LibMicro can be found here: [Project LibMicro, OpenSolaris](http://hub.opensolaris.org/bin/view/Project+libmicro/)
  1. BYTE UnixBench
> > A set of benchmark cases originally started development in 1983 updated by many over the years. Byte UnixBench is intended to provide indication on the performance of unix-like system. More information on Byte UnixBench can be found on [Google Code](http://code.google.com/p/byte-unixbench/).