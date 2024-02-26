# Juan Luis Cano Rodríguez:  Into the rabbit hole: Debugging in Python

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

[89a] Debugging in Python (Juan Luis Cano Rodríguez)
Video 1/3: https://youtu.be/3qNgX3QtmuE

[89b] Debugging in Python: in Jupyter Notebook (Juan Luis Cano Rodríguez)
Video 2/3:  https://youtu.be/1b9fq7-xesI

[89c]  Debugging in Python: in Visual Studio Code (VSC)  (Juan Luis Cano Rodríguez)
Video 3/3:  https://youtu.be/Kgb7FMEg9uY

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2023/89-juan-python-debugging.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/295529919/
- Video:  
- GitHub repo:  
- Transcriber:  ? [needs a transcriber]

## Resources
- Repo:https://github.com/astrojuanlu/workshop-debugging-python
- Slides: https://github.com/astrojuanlu/workshop-debugging-python/blob/main/slides.ipynb
- structlog: https://www.structlog.org/en/stable/
- rich: https://rich.readthedocs.io/en/stable/introduction.html
- Brandon presentation: https://rhodesmill.org/brandon/slides/2015-05-pywaw/hoist/
- Example of Kedro issue: https://github.com/kedro-org/kedro/issues/3055
- Joel Grus talk : I don't like notebooks https://youtu.be/7jiPeIFXb6U
- Reduction Technique: http://sscce.org/ 
- Exercises: https://projecteuler.net/

## About the Event
Your code gives an error. Or worse: it doesn't give an error, but doesn't do what you want. Welcome to the hard part of programming! What to do now?

In this talk we will talk about debugging, which includes a broad set of techniques to identify the root causes of undesired behavior in programs and eventually fix them. We will start with a theoretical introduction of the different types of debugging, we will describe a couple of techniques that you can use, and we will apply them in practice, both in Jupyter Notebook (using its new interactive debugger) and in VSCode.

```
## Timestamps: Part 1
00:00 Intro to Data Umbrella
02:59 Speaker Introduction
04:22 Talk begins + outline
09:56 Sources of bugs
13:17 Types of debugging - tracing v. interactive
16:20 Interactive debugging
19:17 Interactive debugging - VSCode example
19:38 Debugging is problem-solving
21:13 Technique 1 - Divide and Conquer
23:13 Technique 2 - Hypothesis Testing
25:43 Technique 3 - Reduction 
27:47 Technique 4 - Reading Carefully
29:31 Traceback example + exercise
31:40 Think of your future self
32:49 Five (5) debug code tips
36:02 Q&A - Structlog library
37:11 Q&A - What is Rich formatting?
38:15 Q&A - Larger screenshot review  (ImportError, VSCode/JupyterLab debug interface)
41:02 Q&A - Stack Overflow management tips
44:04 Q&A - Template for bug reporting
45:54 Reviewing debug tips and tricks
47:17 Q&A + inspiration for debugging
49:14 Comments - get familiar with common tracebacks / errors seen to produce correct syntax
51:38 Q&A - How does unit testing factor into debugging?
```

```
## Timestamps: Part 2 (Jupyter Notebook)
00:00 Let’s talk about Jupyter
01:16 package: Language server protocol (lsp); Installation recommendations: install extra plug-ins / packages (for linting, formatting)
03:08 Jupyter ipyflow package: gives execution order and cell flow
04:01 Jupyter demo
10:40 pip install ipyflow
11:54 Jupyter debugger
14:54 import pdb, pdb_set_trace()
15:39 ipdb (interactive pdb)
20:53 example of adding the function: breakpoint()
21:00 turn on the Jupyter debugger
22:57 Q&A: What are the first 3 things you do when you cannot reproduce an error?
25:56 Q&A: Where is the breakpoint coming from? (it is a built in function)
```

```
## Timestamps: Part 3 (VSCode)
00:00 VSCode window breakdown (integrated terminal, file editor)
00:21 VSCode v. Jupyter
00:30 Navigating to example directory to run Python file 
01:05 Activating an environment (`which python` command example)
01:17 Installing dependencies with pip install numpy matplotlib scikit-learn to run the existing scripts that have imports
02:12 Running the scripts (`python plot.py`)
02:40 Beginning debug - example problem with “Gaussian process”
03:04 Introducing Debugging Configurations (How do I debug on VSCode?) 
03:13 Run & Debug Panel
03:38 Post-mortem debugging with tracebacks
04:17 Using the Debug Console (on the integrated terminal)
05:57 More sophisticated debugging - using breakpoints
07:21 Attempting different approach
08:11 Stepping into the code
08:34 Creating `launch.json` file to modify VSCode configs
10:14 Wrap-up
```

https://github.com/data-umbrella/event-transcripts/issues/92


## About the Speaker
Juan Luis (he/him/él) works as Developer Advocate at QuantumBlack, AI by McKinsey, with a focus on Kedro, an open source data science framework. He has a decade of experience as developer advocate, software engineer, and Python trainer in several industries. PSF Fellow since 2017, he has made significant contributions to the PyData stack, published several open-source packages, and organized the first seven PyCons in Spain. Currently he is the lead organizer of the PyData Madrid monthly meetups.

- LinkedIn: https://www.linkedin.com/in/juanluiscanor/
- GitHub:  https://github.com/astrojuanlu/

#python #codereview

## Video 1
<a href="http://www.youtube.com/watch?feature=player_embedded&v=3qNgX3QtmuE" target="_blank"><img src="http://img.youtube.com/vi/3qNgX3QtmuE/0.jpg"
alt="Juan Luis Cano Rodríguez:  Into the rabbit hole: Debugging in Python" width="50%" /></a>

## Video 2
<a href="http://www.youtube.com/watch?feature=player_embedded&v=1b9fq7-xesI" target="_blank"><img src="http://img.youtube.com/vi/1b9fq7-xesI/0.jpg"
alt="Juan Luis Cano Rodríguez:  Into the rabbit hole: Debugging in Python" width="50%" /></a>

## Video 3
<a href="http://www.youtube.com/watch?feature=player_embedded&v=Kgb7FMEg9uY" target="_blank"><img src="http://img.youtube.com/vi/Kgb7FMEg9uY/0.jpg"
alt="Juan Luis Cano Rodríguez:  Into the rabbit hole: Debugging in Python" width="50%" /></a>

#python #codereview

## Transcript
