# virtual-threads

I have used the jdk-19 with loom preview. The --enable-preview flag hsa to be enabled
for both Java Compiler and for java execution (jvm argument).

* **StructuredConcurrency**  This example demonstrates Project Loom structured concurrency
features, which enables a main task to split into several
concurrent sub-tasks that run concurrently to completion before the
main task can complete.


* **CompareParallelFuturesAndLoomStructuredConcurrency**
  This example compares and contrasts the programming models and
performance results of Java parallel streams, completable futures,
and Project Loom structured concurrency when applied to download,
transform, and store many images from a remote web server.

Execution results:

Entering the program with 8 cores available 

  utils.OptionsImages: Parallel streams reduce()/concat() test downloaded and stored 105 images

  utils.OptionsImages: Completable futures test downloaded and stored 105 images

  utils.OptionsImages: Structured concurrency test downloaded and stored 105 images

Printing 3 results from fastest to slowest

Completable futures runFineGrained() test executed in 22129 msecs

Structured concurrency runFineGrained() test executed in 27668 msecs

Parallel streams run() test executed in 28578 msecs
