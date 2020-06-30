Disclaimer: All ideas and concepts presented here are my own.

## Creation of BlenderProc

### Part 1

In May 2019 I had a personal need for the generation of synthetic images for the training of CNNs.
After extensive research and getting to the conclusion, that there are no easy to use frameworks out there to help with this procedure, I decided that we need our own framework.
The main reasons for this was that I wanted a pipeline, which builds on top of a raytracer and not a rasterizer. 
If you don't know the differences check out this amazing blog post by [nvidia](https://blogs.nvidia.com/blog/2018/03/19/whats-difference-between-ray-tracing-rasterization/).
In my view the worst part about rasterizer are that they have been designed to fool humans into believing that an image is real.
However, this means that they use extensively faults in our own vision system. A good example for this is that human vision has problems predicting the correct reflection in a spoon. So, while implementing a game engine, a game engineer would use that fact and reduce the realisim on such things.

But, and this is a big but, we don't know if these tricks to make the game run faster are hindering the general sim2real transfer.

To avoid all of this we are using Blender with its raytracer named Cycles. It is Open Source and has been in active development for years, which gives BlenderProc its name.

In the beginning this project was named differently though, our first working title was BlenderPipeline. As our main goal was to generate a pipeline to easily generate enough data. We later changed to Proc for procedural to make it a bit more snappy and not so long.
