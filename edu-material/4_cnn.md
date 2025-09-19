# Convolutional Neural Networks

We can make modifications to neural networks to adapt them to various data types (images, sound, language, etc.) This week, you'll be looking into convolutional neural nets (CNNs), which are *usually* optimized best for processing images and videos. These have been around since the 1980s fyi. 

The rate of research on CNNs has slowed down a little bit since LLMs became the hottest topic in research. Though given that they're quite mature now, this also means they're in a good position for applications. 

Note: it can be pretty tempting to start developing your own new convolutional architectures. And in 2013-2018, the research trend was to build out new architectures (often with trivial changes). This has stabilized a bit. Sometimes, it's best to just pull a predefined architecture using torchvision. Common architectures include:
* [ResNet](https://arxiv.org/abs/1512.03385)
* [EfficientNet](https://arxiv.org/abs/1905.11946)
* [ConvNext](https://arxiv.org/abs/2201.03545)
* [MobileNet](https://arxiv.org/abs/1704.04861)

I recommend skimming some of these research papers so you can get a vibe on how papers are written. 
More recently, 'Transformers' - the architecture to do LLMs - have been increasingly used to do image-based tasks too. 

## CNNs 101
* [Convolutional Neural Networks YouTube Playlist](https://www.youtube.com/playlist?list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF)
* I'm now going to expose you to research papers. The above playlist is pretty old school in the CNN world. So checkout this [ConvNext](https://arxiv.org/abs/2201.03545) paper from 2022.
* [3Blue1Brown video on Convolutions](https://youtu.be/KuXjwB4LzSA?si=sZjjp6N26_Q67uIx)
* [CNNs in PyTorch](https://youtu.be/pDdP0TFzsoQ?si=Vx52_i7SySBIWXrN)
* [Transfer Learning in PyTorch](https://youtu.be/K0lWSB2QoIQ?si=4rVyc91XbUZuVcAp)
* [ResNet from Scratch](https://youtu.be/DkNIBBBvcPs?si=RzipG_JPbaBLfyjW)

## Optional viewing
The above material focuses mostly on image classification. 
There are a wide variety of different tasks in computer vision, though. 
This includes object detection, segmentation, image generation, etc.

* [Object detection](https://youtu.be/svn9-xV7wjk?si=F4x_RkltMSTliec6) - the most common architecture is the YOLO family lmao
* [Image Segmentation with U-Net from scratch](https://youtu.be/IHq1t7NxS8k?si=dqK_6zrkr3x1tdU0)
* [Breast Cancer Detection using CNNs](https://www.nature.com/articles/s41586-019-1799-6) - A mate from Google worked on this paper. This is an extremely high-quality paper. CNNs are used, but a major part of the novelty is in how AI was integrated into the clinical workflow. 
* [Heart disease Detection using a 1D CNN](https://www.nature.com/articles/s41591-018-0268-3) - Andrew Ng's lab published this a while ago. They used 1D convolutions (everything above is a 2D convolution), which turns out to be useful for time-series data. Also a high-quality paper.