## AN4 example database for SphinxTrain

This directory contains the Census (AN4) database audio files. Some
files from the original database were excluded, namely those
with filenames starting with "cen9".

The AN4 database was recorded at Carnegie Mellon University circa
1991. For more detailes, please see "Acoustical and environmental
robustness in automatic speech recognition", by Alex Acero, published
by Kluwer Academic Publishers, 1993.

The files have been converted to RIFF (a.k.a. Microsoft WAV) format
for ease of use.

The directories contain:

-wav/an4_clstk: training data set recorded on close talking microphone.

-wav/an4test_clstk: test data set recorded on close talking microphone.

-etc: directory containing the transcriptions, control files,
dictionaries, and a basic unigram language model for evaluation.

This database is mostly interesting for quickly testing the training
scripts, as it is quite small and simplistic.

To run basic training:

    docker run -t dhdaines/sphinxtrain -t an4 setup
    docker run -v $PWD:/st -t dhdaines/sphinxtrain run

See [LICENSE](./LICENSE) for terms of use.
