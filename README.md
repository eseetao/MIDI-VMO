# MIDI-VMO Study

We present a study to evaluate the effectiveness of generating a long-term structure using MelodyRNN. To create sequential samples of data, MelodyRNN uses three configurations: a basic RNN, lookback RNN, and attention RNN to generate MIDI samples by looking at previous events that might constitute a recurring theme or structure. We evaluate the generated samples by using information rate from a Variable Markov Oracle to allow statistical characterization of musical information dynamics and detection of motifs in the MIDI samples. 


### Prerequisites

Set up your [Magenta environment](https://github.com/tensorflow/magenta/blob/master/README.md) and [Variable Markov Oracle](https://github.com/wangsix/vmo). 

When installing Magenta 0.3.9, you may encounter a dependency error on grpcio. Doing the following will install grpcio 1.9.1 and complete the installation of Magenta 0.3.9:

```
pip3 install grpcio==1.9.1 magenta
```

### Generating melodies with Melody_RNN

```
    melody_rnn_generate
    --config=CONFIG
    --bundle_file=/Users/../attention_rnn.mag
    --output_dir=/Users/../attention_rnn
    --num_outputs=10 
    --num_steps=512
    --primer_midi=/Users/../Summer_Primer_Melody.mid
```
Where bundle_file is the absolute path to the of the .mag file of the pretrained model and config as either 'basic_rnn', 'lookback_rnn', or 'attention_rnn' that matches the bundle file. 


## Acknowledgments

I would like to thank Shlomo Dubnov and CREL members for their guidance, as well as the Google Magenta team for the technical work on music generation. 
