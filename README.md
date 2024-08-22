# Benchmark for noir-rsa

This repository includes the source code used for the benchmarking of the RSA verification using the Noir programming language. 

## Description of the benchmark

We ran a benchmark to measure the number of gates of the circuit, the proving time and the verification time of the RSA verification. The benchmark includes two main scenarios: the signature verification of one signature and 10 different signatures. For both scenarios, we reported all the metrics mentioned above.

On the one hand, the number of gates is measured using the `bb gates` command. On the other hand, the timing measures are taken using the `hyperfine` command line tool which takes the average of ten executions of the proving and verification commands. These averages are the ones reported in the results presented here.

The benchmarks were executed using a laptop with Intel(R) Core(TM) i7-13700H CPU and 32 GB of RAM.

## Results

The results for the verification of one signature are the following:

| **Bit length** | **Circuit size** | **Avg. proving time (BB) [ms]**  | **Avg. proving time (UH) [ms]** | 
|----------------|------------------|---------------------------------|--------------------------------------|
|           1024 |             2204 |                           234.8 |                             181 |
|           2048 |             7131 |                           345.6 |                           261.9 |

The results for the verification of 10 signatures are the following:

| **Bit length** | **Circuit size** | **Avg. proving time (BB) [ms]** | **Avg. proving time (UH) [ms]** |
|----------------|------------------|---------------------------------|--------------------------------------|
|           1024 |            21516 |                           970.9 |                           514.4 | 
|           2048 |            63821 |                          1801.7 |                           964.2 |

