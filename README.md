![CUDA](./CUDA_Logo.jpg)

# CUDA Environment is Spinning Up
## Introduction 
Accelerated computing is replacing CPU-only computing as best practice. The parade of breakthroughs driven by accelerated computing, the ever increasing demand for accelerated applications, programming conventions that ease writing them, and constant improvements in the hardware that supports them, are driving this inevitible transition.

At the center of accelerated computing's success, both in terms of its impressive performance, and its ease of use, is the [CUDA](https://developer.nvidia.com/about-cuda) compute platform. CUDA provides a coding paradigm that extends languages like C, C++, Python, and Fortran, to be capable of running accelerated, massively parallelized code on the world's most performant parallel processors: NVIDIA GPUs. CUDA accelerates applications drastically with little effort, has an ecosystem of highly optimized libraries for [DNN](https://developer.nvidia.com/cudnn), [BLAS](https://developer.nvidia.com/cublas), [graph analytics](https://developer.nvidia.com/nvgraph), [FFT](https://developer.nvidia.com/cufft), and more, and also ships with powerful [command line](http://docs.nvidia.com/cuda/profiler-users-guide/index.html#nvprof-overview) and [visual profilers](http://docs.nvidia.com/cuda/profiler-users-guide/index.html#visual).

CUDA supports many, if not most, of the [world's most performant applications](https://www.nvidia.com/en-us/gpu-accelerated-applications/) in: [Computational Fluid Dynamics](https://www.nvidia.com/en-us/gpu-accelerated-applications/), [Molecular Dynamics](https://www.nvidia.com/en-us/gpu-accelerated-applications/), [Quantum Chemistry](https://www.nvidia.com/en-us/gpu-accelerated-applications/), [Physics](https://www.nvidia.com/en-us/gpu-accelerated-applications/) and HPC.

Learning CUDA will enable you to accelerate your own applications. Accelerated applications perform much faster than their CPU-only counterparts, and make possible computations that would be otherwise prohibited given the limited performance of CPU-only applications. In this lab you will receive an introduction to programming accelerated applications with CUDA C/C++, enough to be able to begin work accelerating your own CPU-only applications for performance gains, and for moving into novel computational territory.

 
## Objectives
By the time you complete this lab, you will be able to:

- Write, compile, and run C/C++ programs that both call CPU functions and launch GPU kernels.
- Control parallel thread hierarchy using execution configuration.
- Refactor serial loops to execute their iterations in parallel on a GPU.
- Allocate and free memory available to both CPUs and GPUs.
- Handle errors generated by CUDA code.
- Accelerate CPU-only applications.



# Next Steps
With the techniques and tools that you’ve learned now at your disposal, you are almost ready to start accelerating your own real world applications. This section will provide you with details for:
- Setting up your own CUDA-enabled environment
- How best to continue your accelerated programming learning
- An additional practice problem
- Other helpful resources

## SETTING UP A CUDA-ENABLED ENVIRONMENT
**The 2 easiest ways for you to set up a CUDA-enabled environment for your own work are:**
1. Via cloud provider
2. Installing CUDA on your own system with an NVIDIA GPU

### VIA CLOUD PROVIDER
All major cloud providers provide NVIDIA GPU-enabled instances. A simple web search for “NVIDIA GPU <your cloud provider of choice>” will result in a hit for how to set one up on your cloud provider of choice. These instances will have the CUDA toolkit installed. You can simply SSH in and set to work.

### YOUR OWN SYSTEM
If you have access to a system with an NVIDIA GPU, but have not yet installed the CUDA toolkit, simply follow [the directions here for downloading and installing CUDA on your particular operating system](https://developer.nvidia.com/cuda-downloads).

## CONTINUING YOUR ACCELERATED COMPUTING DEVELOPMENT
After setting up your own accelerated system, there is one very best thing you can do to further your development as an accelerated computing programmer, work to accelerate your own applications. In addition, 

### WORK TO ACCELERATE YOUR OWN APPLICATIONS
You have learned how to approach accelerated computing iteratively, and in a profile-driven manner, so:
- Take some baseline measurements of a compute-intensive application you work on
- Make some hypotheses about where you might accelerate it
- Make some naive changes
- Profile and repeat

### READ AND APPLY THE CUDA C BEST PRACTICES GUIDE
Even though you are ready to accelerate CPU-only applications in ways that will meaningfully improve their performance, you can take the study of accelerated computing much further, and in time, you should.

The [CUDA C Best Practices Guide](http://docs.nvidia.com/cuda/cuda-c-best-practices-guide/index.html) is an essential resource for effective CUDA programming. After accelerating your own application in the ways you already know, start a study of this document, applying the techniques it describes to further improve your application’s performance. 

## GPU-ACCELERATING PRACTICE APPLICATION
By far the best practice is to accelerate your own applications, but for those of you who might not yet have a real-world use case, try your hand at accelerating the following [Mandelbrot Set](https://en.wikipedia.org/wiki/Mandelbrot_set) simulator. Per usual, take an iterative and profile-driven approach.

- [Mandelbrot Set Simulator](https://github.com/sol-prog/Mandelbrot_set): this C++ simulation includes a link to a detailed explanation of the application, and will allow you to visually see the impact of GPU-acceleration

## HELPFUL RESOURCES
A lot of highly talented programmers have used CUDA to create highly optimized libraries to be used for accelerated computing. There are many scenarios in your own applications where you will need to write your own CUDA code, but as usual in programming, there are also many scenarios where someone else has already written the code for you.

Peruse [GPU-Accelerated Libraries for Computing](https://developer.nvidia.com/gpu-accelerated-libraries) to learn where you can use highly optimized CUDA libraries for tasks like [basic linear algebra solvers](https://developer.nvidia.com/cublas) (BLAS), [graph analytics](https://developer.nvidia.com/nvgraph), [fast Fourier transforms](https://developer.nvidia.com/cufft) (FFT), [random number generation](https://developer.nvidia.com/curand) (RNG), and [image and signal processing](https://developer.nvidia.com/npp), to name a few.



# Environment Quick Start
This is a quick-start for users who just want to get going.

1. Use the nvidia AMI on AWS (10 minutes): [Deploy on Amazon EC2](https://github.com/NVIDIA/nvidia-docker/wiki/Deploy-on-Amazon-EC2)

2. Get started with nvidia-docker (5 minutes): [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)

3. Get started with the CUDA development image (5 minutes): ["docker pull nvidia/cuda:9.1-devel"](https://hub.docker.com/r/nvidia/cuda/)
