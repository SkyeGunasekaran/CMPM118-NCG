# Spiking Neural Networks
Let's now look at how the brain does its thing. 
Actually tbh, we don't really know.
But we have some different views on what makes the brain efficient.

As one example, biological neurons rely on voltage bursts known as "action potentials", or "spikes", to communicate.
Can these be used to make deep learning more efficient? 

## Spiking Neural Networks
* [Action Potentials in the Neuron](https://www.youtube.com/watch?v=oa6rvUJlg7o)
* [Training Spiking Neural Networks Using Lessons from Deep Learning: Sections 3 onwards](https://arxiv.org/abs/2109.12894)

## Coding up SNNs
* [Hands-on with snnTorch](https://youtu.be/aUjWRpisRRg?si=_i7K9oD4-S1XSkx4)
* [snnTorch Tutorial series: Tutorial 2,5,7 at least](https://snntorch.readthedocs.io/en/latest/tutorials/index.html)

I want to make it very clear that SNNs can be a pain in the ass to train compared to non-spiking neural networks.
Compressing activations to 1/0 is extremely lossy, and modern computers can do computation pretty cheaply anyway. 
For most deep learning workloads, it's memory access that is the most expensive part. 
So it's primarily sparsity that makes the most sense here. 
As a result, my opinions on what aspect of SNNs to focus on have evolved a bit in the past couple of years.

* [A talk that summarizes my take on SNNs in 2025](https://youtu.be/5tzA72tOlRw?si=abL3v3NWKcYFDzw9)

In this above talk, I start to dive deeper into state-space models. 
Spiking neural networks share a ton of similarities with SSMs. If you wish to dive deeper into SSMs, then go back to the [RNN optional material](https://github.com/SkyeGunasekaran/CMPM118-NCG/blob/main/edu-material/5_rnns.md) section.

