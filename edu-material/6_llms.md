# Large Language Models

Goddamn, there is so much that has been developed in LLMs in such a short amount of time. 
So far, you will have found that neural networks are quite "regular". A bunch of nodes and edges. 
Convolutions shook this up a bit by adding more structure to those nodes and edges.
Transformers have a far more irregular structure, with more weird stuff going on. 
They also scale up to insane sizes, and are trained across multiple stages (e.g., pre-training, mid-training, post-training) with ridiculous datasets of 10s of trillions of tokens. A huge amount of content below. 


## LLMs: High-Level Overview
Andrej Karpathy is a beautiful man with beautiful lectures. Here is a small sample, but roam free and watch others too. 

* [Andrej Karpathy: A generalist intro to LLMs](https://youtu.be/zjkBMFhNj_g?si=yOw8U-5hXhHBNPHK)
* [Andrej Karpathy: State of GPT](https://youtu.be/bZQun8Y4L2A?si=6AsLUMS_ct8Mg2Tw) - This one doesn't overly fixate on architecture, but rather, the full training pipeline
* [Andrej Karpathy: Introduction to Transformers](https://youtu.be/XfpMkf4rD6E?si=EWtzNGjRTpBNbqNJ)

## LLMs: A Slightly Deeper Dive (Week 6: Essential)
* [3Blue1Brown Videos: Videos 5-8](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) - Teardown of GPT-3

I gave my own tutorial on LLMs below, too. Given the wide variety of architectures out there, I try to synthesize much of the field (as of June 2025).

* [My tutorial on LLMs: Part 1](https://youtu.be/acSIdUxku4w?si=84qjmnw4u3lidQMB) - LLMs 101.
* [My tutorial on LLMs: Part 2](https://youtu.be/C0R-V11elkY?si=ZdryEtF377rAvxIs) - This taps into some of the lab's research topics. 

### Coding, HuggingFace, and Fine-Tuning (Week 6: Essential)
If you're shaky on code, this is a good time to enhance your skills and try the following.
* [Build a Transformer from Scratch](https://youtu.be/kCc8FmEb1nY?si=-2GL87MZp-gkZ3V3)

The reality is you'll very rarely build an LLM from total scratch, though. It's more likely you'll take pre-existing blocks, do some fine-tuning.
For that, you should absolutely learn how to work with HuggingFace. HuggingFace hosts many Transformers and is a great library to make a lot of the things you might want to do with Transformers far easier. You can generally look up most open-source LLMs and play with them, modify them, etc.

* [SmolLM3 on HuggingFace](https://huggingface.co/HuggingFaceTB/SmolLM3-3B) - see if you can download the model (e.g., on Google Colab) and run inference with it. Use the documentation on the page to figure this one out yourself.

Now's a good time to figure out how to fine-tune an LLM. 
* [LoRA: Low-Rank Adaptation: YouTube Video](https://youtu.be/t1caDsMzWBk?si=KS5AEx33ZaP8n6ru)
* [LoRA: Interactive Code: YouTube Video](https://youtu.be/Us5ZFp16PaU?si=M--5kcr3tox_wtnC)

## Language Model Architectures (Optional, but super useful)
With the basics out of the way, let's look at some of the modern (as of September 2025) architectures out there. 

* [Gemini Technical Report](https://arxiv.org/abs/2312.11805) - Architectural details aren't there; it's a closed-source model and much of it is secret sauce.

The following models are all open-source and provide more details. However, reproducibility is still a pain in the ass because datasets have not been released (this could be for both logistical and legal reasons - i.e., training on data without a license to use it is a grey area of law).

* [Llama3 Technical Report](https://arxiv.org/abs/2407.21783) - Llama was the OG open-source LLM developed by Meta. This technical report gives you an insane amount of detail on the logistics behind training LLMs.
* [Llama4: YouTube Tutorial](https://youtu.be/Lqj69tZkPiE?si=h71I9JN8TsTqiYHL) 
* [DeepSeek: YouTube Tutorial](https://www.youtube.com/watch?v=0VLAoVGf_74&ab_channel=WelchLabs) - China released a highly performant open-source model that, for a moment, dominated a bunch of benchmarks and had a wild impact on NVIDIA stock prices lmao
* [DeepSeek Technical Report](https://arxiv.org/abs/2412.19437)
* [Qwen Technical Report](https://arxiv.org/abs/2309.16609) - Another high-performant open-source model from China. You can self-explore Qwen2.5/3 for more recent updates.
* [SmolLM3: Blogpost](https://huggingface.co/blog/smollm3) - An incredible resource on another high-performant open-source model. They released all the checkpoints of their model from various phases of training. This also digs deeper into pretraining, midtraining, post-training. 
* [KimiK2](https://youtu.be/LSfpwaujqLQ?si=QblPkri50gjwWFPY) - A more recent, trillion parameter-scale open-source model from China.

## Specific Techniques that Boost Performance (Week 7: Essential)
These are all YouTube lectures, but I encourage you to search up the research papers that presented these. 
Research papers are naturally harder to understand than bite-sized YouTube videos, but there is plenty of detail missed in these videos. You will want to learn what it takes to write a compelling, meaningful paper.

Many of these ideas came out of research labs, rather than big fancy companies. 
While it helps, you do not need a ton of GPUs to come up with and validate these ideas on a mid-sized LLM. 

* [RoPE: YouTube Video](https://youtu.be/o29P0Kpobz0?si=WCUiYo8KkvxkYLZl)
* [Mixture of Experts: YouTube Video](https://youtu.be/7yR5ScbK1qk?si=Qjv9gt0n6pHtLv7a)
* [Sliding Window Attention: Paper teardown by Yannick Kilcher](https://youtu.be/_8KNb5iqblE?si=RgZME1BVpTYH4qR6)
* [Speculative Decoding: YouTube Video](https://youtu.be/S-8yr_RibJ4?si=mdWyd62X84Qokjsc) 
* [Attention Sinks: YouTube Video](https://www.youtube.com/live/RnM84Sv9WpA?si=DMvS-k_y19yKe8eM)
* [Knowledge Distillation](https://youtu.be/jrJKRYAdh7I?si=gC518kQjPrRHaD_3)

## Post-Training (Week 7: Essential)
Pre-training/mid-training an LLM is fixated on predicting the next token.
ChatGPT didn't stop there; they finished up their training of GPT-3 with "post-training", where they paid humans to rank outputs and use those as signals to reward/punish a model.

* [Reinforcement Learning with Human Feedback: 4-min YouTube Video](https://youtu.be/vJ4SsfmeQlk?si=qqCQLif0yNLKOLEY) - Sebastian also has wonderful educational material. Strongly recommend looking deeper into his stuff.

It turns out that this process is extremely brittle. It worked for OpenAI, but many other companies had a hard time elevating performance with more human rewards. Humans are super subjective and inconsistent, so the reward signal was likewise inconsistent. We have seen alternative forms of fine-tuning and reward modeling come up as a result.  

* [Post-training from OpenAI: YouTube Video](https://youtu.be/JfaLQqfXqPA?si=s5csYtjmHIk5Jufa)
* [PPO: Proximal Policy Optimization: YouTube Video](https://youtu.be/8jtAzxUwDj0?si=jHYgb73j9mUkmb1T)
* [GRPO: Group Relative Policy Optimization: YouTube Video](https://youtu.be/xT4jxQUl0X8?si=DbMPTPOBdy5ySBpl)

## Reasoning in LLMs (Optional)
By now, you would have seen that the best performance in LLMs isn't obtained from just one forward-pass, but by letting the model "reason", or do multiple forward-passes before giving its response to the user. In one study from Stanford, simply by adding the prompt "Wait..." to the end of your input would bias your LLM to spend a bit more time ruminating on the output response. A very rudimentary form of reasoning, but it works pretty damn well.

Here is a high-level video on reasoning in LLMs by Danny Zhou of Google Deepmind:
* [Reasoning in LLMs: YouTube Lecture](https://youtu.be/ebnX5Ur1hBk?si=cjZ2cejUmbxMh02E)

You should also look into Chain of Thought Reasoning. If anyone finds a robust resource, feel free to make a PR as I'm yet to find something I like.

* [Latent Reasoning Models](https://arxiv.org/abs/2507.06203) - A review paper led by Ruijie Zhu, a PhD student in my lab.

## Low Precision LLMs (Optional, but highly relevant to my lab's work)
Computers work with floating point numerical formats. Each weight will contribute to 16 or 32 bits of memory (plus the bits required to define the location of that weight, and any additional tags). A thoroughly active area of research is in low-precision LLMs, which aim to reduce the memory (and therefore inference time/computational cost) of LLMs. 

* [Low Precision LLMs](https://www.youtube.com/playlist?list=PL4bm2lr9UVG0HvePBXvsceO4yuLC8HhUh)
* [BitNet: 1-bit LLMs by Microsoft](https://arxiv.org/abs/2310.11453)
* [1.58-bit / Ternary LLMs by Microsoft](https://arxiv.org/abs/2402.17764)
* [MatMul-free Language Model](https://arxiv.org/abs/2406.02528) - Our own fancy paper which uses ternary weights

## Advanced Concepts in Language Modeling
* [Flash Attention from Scratch](https://www.youtube.com/watch?v=zy8ChVd_oTM&t=6304s&ab_channel=UmarJamil) - Not a new architecture, but rather, an efficient implementation of Transformers. This introduces a new language called *Triton*, which is sort of like a Python-CUDA hybrid. It lets you have more control over a GPU, and therefore, can squeeze better performance.
* [Small Language Models in the Era of Agentic AI](https://arxiv.org/abs/2506.02153) - a hype paper by NVIDIA that looks into the value of specialized, small language models that work together instead of huge, overparameterized LLMs.



The field of LLMs moves incredibly fast and requires some serious grit to 1) catch up on, 2) to keep up with, and 3) if you're doing research, executing your ideas fast enough before getting scooped.  

Some more advice: when reading papers in LLMs, don't hyperfixate purely on new architectures. 

For example, a question you might want to ask is: how do they validate their architectures? 
Look into what they do to convince the reader/reviewer that their model is better.
They will often run ablation studies to show how much each component of their new innovation contributes to better performance. 
There are a set of different evaluations that are suitable at different phases of model training. 