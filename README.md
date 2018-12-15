# MIDI-VMO Study

We present a study to evaluate the effectiveness of generating a long-term structure using MelodyRNN. To create sequential samples of data, MelodyRNN uses three configurations: a basic RNN, lookback RNN, and attention RNN to generate MIDI samples by looking at previous events that might constitute a recurring theme or structure. We evaluate the generated samples by using information rate from a Variable Markov Oracle to allow statistical characterization of musical information dynamics and detection of motifs in the MIDI samples. 


### Prerequisites

Set up your [Magenta environment](https://github.com/tensorflow/magenta/blob/master/README.md) and [Variable Markov Oracle](https://github.com/wangsix/vmo). 

When installing Magenta 0.3.9, you may encounter a dependency error on grpcio. Doing the following will install grpcio 1.9.1 and complete the installation of magenta 0.3.9:

```
pip3 install grpcio==1.9.1 magenta
```


### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo


## Acknowledgments


