# Nidhin Pattaniyil and Vishal Rathi: Serving PyTorch Models in Production


## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2022/59-nidhin-vishal-pytorch.md 
- Meetup Event: https://www.meetup.com/data-umbrella/events/286639683/
- Video: https://youtu.be/fx_NaKwFYbg
- GitHub repo:  
- Transcriber:  ? [needs a transcriber]

## Resources
- Repo: https://github.com/npatta01/pytorch-serving-workshop
- Launch this using GitHub authentication to follow along:  https://hub.np.training/

## About the Event
This talk is for a data scientist or ML engineer looking to serve their PyTorch models in production. It will cover post training steps that should be taken to optimize the model such as quantization and torch script. It will also walk the user in packaging and serving the model through Facebook's TorchServe.

## About the Speaker
Nidhin Pattaniyil is a Machine Learning Engineer in Walmart Search.

- LinkedIn: https://www.linkedin.com/in/nidhinpattaniyil/
- GitHub: https://github.com/npatta01

Vishal Rathi is a Software Engineer in Walmart Search.

- LinkedIn: https://www.linkedin.com/in/vishalkumarrathi

## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=fx_NaKwFYbg" target="_blank"><img src="http://img.youtube.com/vi/fx_NaKwFYbg/0.jpg"
alt="Nidhin Pattaniyil: Serving PyTorch Models in Production" width="50%" /></a>

```
## Timestamps
00:22 About session
00:47 About Data Umbrella
04:18 Introduction
05:16 Session agenda
06:01 Machine learning at Walmart Search
12:11 Review of some deep learning concepts
15:24 BERT: Different architectures
16:07 Bi-LSTM vs BERT
21:59 Model inference
24:21 Load the model
25:21 Test prediction
28:01 Inference review (Inference time vs accuracy tradeoff)
29:17 BERT large
29:36 BERT base
30:03 Distilled-BERT
33:54 Optimizing model for production
34:03 Post training optimization: Quantization
35:50 Types of Quantization
37:35 Quantization results
38:23 Post training optimization: Distillation
39:44 Distillation results
40:35 Eager execution vs Script mode
42:02 TorchScript JIT: Tracing vs Scripting
43:11 TorchScript Timing
45:21 Optimizing the model (Hands On)
47:36 Quantization (Hands On)
52:00 TorchScript (Hands On)
56:33 Deploying the model
57:13 Options for deploying PyTorch model
57:42 Benefits of TorchServe
59:41 Packaging a model/MAR
01:00:00 Pytorch BaseHandler
01:03:00 Built in handlers
01:04:15 Serving
01:05:10 APIS
01:05:32 Deploying the Model (Hands On)
01:22:11 Lessons learned
01:23:50 Q/A
```
## Transcript
