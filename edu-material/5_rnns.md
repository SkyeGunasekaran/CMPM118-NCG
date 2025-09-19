# Recurrent Neural Networks

RNNs are neural networks that process sequences and time-varying data. Think: audio signals, language, biomedical signals, etc. 

We used to use RNNs in language pre-2017. But then the Transformer architecture became popularized. 
Some people will say RNNs are totally redundant now. I disagree - they're significantly more efficient than Transformers, can be useful in modelling the brain (a chunky time-varying machine), and my lab is developing RNN-variants that meet Transformer-level performance under certain scenarios.

From here, this material starts becoming much more tightly related to the work in my lab.

## RNNs 101
* [Josh Starmer Lecture Series: Videos 15-18](https://www.youtube.com/playlist?list=PLblh5JKOoLUIxGDQs4LFFD--41Vzf-ME1)
* [Andrew Ng's video on Sequence Models](https://youtu.be/S7oA5C43Rbc?si=Wmd-DrbmV7wf4LW8) - Andrew actually deleted this from his main channel. My guess is it's because Transformers dominated the scene. I still think it's valuable. Pay particular attention to Backprop-Through-Time. 

## Optional viewing
Recurrent neural networks have a lot of problems with them. With some slight modifications, they become extremely powerful.
My lab has been paying a lot of attention to *State-Space Models*. 
* [Some basics of state-space models](youtube.com/watch?v=X-7rgesJaGM&ab_channel=ConferenceonLanguageModeling) - Note, state-space models are just a fancy name for recurrent networks that are linear through time.
* [A paper on hybrid linear attention](https://arxiv.org/abs/2507.06457) - This combines linear RNNs with Transformers (which you'll learn next week). This was a paper co-led by a former undergraduate at UCSC who I met through CMPM 118! 
* [HGRN2](https://arxiv.org/abs/2404.07904) - A very powerful linear recurrent neural network used in language modeling
* [Linear Attention](https://www.youtube.com/watch?v=d0HJvGSWw8A&ab_channel=SashaRush)
* [Flash Linear Attention Library](https://github.com/fla-org/flash-linear-attention)
