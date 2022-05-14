```text
## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

[53a] Sebastian Raschka: Introduction to PyTorch
Video 1/3: https://youtu.be/B5GHmm3KN2A

[53b] Adrian Wälchli: Scaling Up with LightningLite
Video 2/3: https://youtu.be/AEMU92KOq1U

[53c] Q&A: Sebastian Raschka & Adrian Wälchli (PyTorch, LightningLite)
Video 3/3: https://youtu.be/HaXK4Os5mdo

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2022/
- Meetup Event: https://www.meetup.com/data-umbrella/events/285079424/

## Resources
- DevCon 2022: https://www.pytorchlightning.ai/events/devcon2022nyc
- Sebastian's slides: https://github.com/PyTorchLightning/dataumbrella22-intro-pytorch
- Adrian's slides: https://github.com/data-umbrella/event-transcripts/blob/main/resources/intro-lightninglite.pdf
- 30% book discount:  https://www.amazon.com/gp/mpc/A2MFJW51D7YHHN
- Suggested resource: https://github.com/rasbt/deeplearning-models/blob/master/pytorch-lightning_ipynb/kfold/kfold-light-cnn-mnist.ipynb
- https://github.com/rasbt/deeplearning-models/blob/master/pytorch-lightning_ipynb/kfold/kfold-light-cnn-mnist.ipynb
- Sebastian's book: https://sebastianraschka.com/books/#machine-learning-with-pytorch-and-scikit-learn
- kfold: https://github.com/rasbt/deeplearning-models/blob/master/pytorch-lightning_ipynb/kfold/kfold-light-cnn-mnist.ipynb
- model inspection:  https://pytorch.org/tutorials/intermediate/tensorboard_tutorial.html#inspect-the-model-using-tensorboard
- Link to code examples: https://github.com/PyTorchLightning/dataumbrella22-intro-pytorch

## Community Announcements
- Adding timestamps: https://github.com/data-umbrella/event-transcripts/issues/92


[53a] Video 1: Intro to PyTorch
## Agenda
00:00 Reshama introduces Data Umbrella
08:25 Sebastian begins 
09:50 What is PyTorch? (tensor library, automatic differentiation engine, deep learning library)
10:50 TensorFlow vs PyTorch: why PyTorch is so popular
12:55 PyTorch: tensor library (rank-x tensor: scalar, vector, matrix, 3D tensor, 4D tensor
15:40 tensor library, torch.tensor ~= numpy.array)
17:19 PyTorch: automatic differentiation support
25:28 automatic differentiation in PyTorch
26:30 autograd
28:12 PyTorch: deep learning library 
28:30 3 Steps in Neural Network Training
29:39 Defining the Model
33:50 Step 1: Define forward method
37:28 Step 2: Defining the training loop (initialize the model and optimizer)
41:10 Iterating over the training examples
42:52 Computing the predictions
45:10 Computing the backward pass (backpropagation)
optimizer.zero_grad() (remember to reset the gradients for each iteration)
46:41 Updating the model weights
47:14 Tracking the performance
47:52 no_grad() (we don't care about gradients here, we don't need to construct the computation graph)
48:52 Why do I like PyTorch?
50:38 Live Demo
51:10 Developer conference: Lightning DevCon
52:26 demo in Jupyter Notebook

[53b] Video 2: Scaling Up with LightningLite

## Agenda
00:00 Sebastian finishes up, introduces Adrian: scaling the code to multiple GPUs
01:26 Adrian begins
02:05 Intro to LightningLite
06:55 pip install pytorch-lightning
08:15 The LightningLite Skeleton
09:22 Step 1: Initializing the model and optimizer
10:37 Step 2: Setting up the data loaders
11:22 Step 3: Iterating over the training examples
12:15 Step 4: Updating the model weights
13:32 Why did we make these changes to the code?
13:38 Accelerate your PyTorch code
15:50 Mixed precision saves you memory
17:22 Try different strategies for best performance
20:10 docs.pytorchlightning.ai
    
[53c] Video 3: Q&A with Sebastian and Adrian
00:00 Getting started with Q&A 
00:40 Q: Which activations functions have we used and why?
02:50 Q: When and based on what criteria do we use nn.Module and nn.Sequential?
04:10 Q: When do we use nn.Sequential?
05:54 Q: More info on the  Developer conference: Lightning DevCon? 
07:14 Q: Why do we have a static dataset instead of cross-validation?
09:35 Q: Is reducing precision to 16-bit the same as quantization? (Quantization is mainly for speeding up inference. Mixed precision is more for training.)
11:46 Q: After creating multiple models, we define them in the run method of lite, and we get our experiment results at lightning speed?
12:42 Q: How do we measure and validate PyTorch performance?
14:36 Q: Computational graphs seem like a practical way to look at modeling. Can you recommend resources to learn more about creating these graphs?



 
## Event
This talk will introduce attendees to using PyTorch for deep learning. We will start by covering PyTorch from the ground up and learn how it can be both powerful and convenient. At times, Machine learning models can become so large that they can't be trained on a notebook anymore. Being able to take advantage AI-optimized accelerators such as GPU or TPU and scaling the training of models to hundreds of these devices is essential to the researcher and data scientist.
However, adding support for one or several of these in the source code can be complex, time consuming and error-prone. What starts as a fun research project ends up being an engineering problem with hard to debug code. This talk will introduce LightningLite, an open source library that removes this burden completely. You will learn how you can accelerate your PyTorch training script in just under ten lines of code to take advantage of multi-GPU, TPU, multi-node, mixed-precision training and more.

## About the Speaker: Sebastian Raschka
Sebastian is a machine learning and AI researcher with a strong passion for education. As Lead AI Educator at Grid.ai, he is excited about making AI & deep learning more accessible and teaching people how to utilize AI & deep learning at scale. Sebastian is also an Assistant Professor of Statistics at the University of Wisconsin-Madison and the author of the Machine Learning with PyTorch and Scikit-Learn book.
- LinkedIn: https://www.linkedin.com/in/sebastianraschka/
- Twitter: https://twitter.com/rasbt
- GitHub: https://github.com/rasbt

## About the Speaker: Adrian Waelchli
Adrian is a research engineer at Grid.ai developing and maintaining PyTorch Lightning, a library for researchers and deep learning practitioners built on top of PyTorch, minus the boilerplate. Previously, Adrian graduated with a BSc and MSc in Computer Science at University of Bern, Switzerland. Before joining Grid in 2021, he worked for three years as a PhD student in the Computer Vision Group at the Institute of Computer Science, University of Bern, under the supervision of Prof. Dr. Paolo Favaro. The topics he is passionate about are machine learning at scale, computer vision, computer graphics and mathematics.
- LinkedIn: https://www.linkedin.com/in/adrian-waelchli/
- GitHub: https://github.com/awaelchli
- Twitter: https://twitter.com/adrianwaelchli


```
