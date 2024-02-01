# Volume

Program in C to scale volume of a wav file  by a given factor. CS50 Problem Set 4.

<img width="1423" alt="wav_file" src="https://github.com/cmartinezal/volume/assets/84383847/78b8e67b-4f47-4656-ba89-8824414e3143">

## Problem to Solve

WAV files are a common file format for representing audio. WAV files store audio as a sequence of “samples”: numbers that represent the value of some audio signal at a particular point in time. WAV files begin with a 44-byte “header” that contains information about the file itself, including the size of the file, the number of samples per second, and the size of each sample. After the header, the WAV file contains a sequence of samples, each a single 2-byte (16-bit) integer representing the audio signal at a particular point in time.

Scaling each sample value by a given factor has the effect of changing the volume of the audio. Multiplying each sample value by 2.0, for example, will have the effect of doubling the volume of the origin audio. Multiplying each sample by 0.5, meanwhile, will have the effect of cutting the volume in half.

<p align="left">
   <img width="400" alt="program demo" src="https://github.com/cmartinezal/volume/assets/84383847/c5879a99-f2a2-447e-9a9e-71885f2af9e2">
</p>



## Implementation Details

Complete the implementation of `volume.c`, such that it changes the volume of a sound file by a given factor.

- The program should accept three command-line arguments. The first is `input`, which represents the name of the original audio file. The second is output, which represents the name of the new audio file that should be generated. The third is `factor`, which is the amount by which the volume of the original audio file should be scaled.
- For example, if `factor` is `2.0`, then your program should double the volume of the audio file in `input` and save the newly generated audio file in `output`.
- Your program should first read the header from the input file and write the header to the output file.
- Your program should then read the rest of the data from the WAV file, one 16-bit (2-byte) sample at a time. Your program should multiply each sample by the `factor` and write the new sample to the output file.
- You may assume that the WAV file will use 16-bit signed values as samples. In practice, WAV files can have varying numbers of bits per sample, but we’ll assume 16-bit samples for this problem.
- Your program, if it uses `malloc`, must not leak any memory.

## How to Test

Your program should behave per the examples below.

`$ ./volume input.wav output.wav 2.0`

When you listen to output.wav (as by control-clicking on output.wav in the file browser, choosing Download, and then opening the file in an audio player on your computer), it should be twice as loud as input.wav!

`$ ./volume input.wav output.wav 0.5`

When you listen to output.wav, it should be half as loud as input.wav!

## Getting Started

Let's start to use this project.

## Prerequisites

A compiler for C must be installed

## Installation

To execute the project open the terminal and go to the project folder. Then compile the code with a C compiler and execute the file generated:

```sh
make volume
./volume input.wav output.wav 0.5
```
