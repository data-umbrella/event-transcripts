# Pablo Duboue: RAGged Edge Box: A Personal AI-Powered Document Search System

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2024/106-pablo-rag.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/303430325/
- Video: https://youtu.be/_fJFuL2pLvw
- Transcriber:  ? [needs a transcriber]

## Resources
- Slides: https://github.com/data-umbrella/event-transcripts/blob/main/resources/RAGged_Edge_Box.pdf
- Project: https://textualization.com/ragged/
- GitHub project: https://github.com/Textualization/the-ragged-edge-box
- Pablo's other talk on LLMs:  https://youtu.be/gP2gr0d0Q28, Solving NLP (Natural Language Processing) Tasks Using LLMs (Large Language Models) (Pablo Duboue)
- This was Marc Laporte's talk, Build Your First Database Web App with Tiki: https://youtu.be/Jz0rXFnY05U

## About the Event
One of the most popular embodiments of Generative AI are information retrieval (IR) augmented generation (RAG). Such systems use an information retrieval engine (based on semantic embeddings or keyword search) and then use a Large Language Model (LLM) to extract answers to a given query.

These systems require a large amount of computation and are usually implemented in the cloud which presents data privacy issues.

In this talk we will present The RAGged Edge Box project in which basic embedding systems and small local LLMs are packaged inside a multi-platform virtual machine (VirtualBox). The system provides a Web interface that runs locally and allows access to the RAG functionality in a completely private manner. The neural networks run on a ONNX runtime and do not require a GPU. RAG code is implemented in PHP and is easy to modify, requiring a much smaller execution environment than a Python alternative.

```
## Timestamps
00:00 Introduction by Reshama
04:40 Pablo begins presentation
05:00 RAGged project page
05:54 An overview of The RAGged Edge Box
08:40 Attendee Personas
10:59 Talk agenda
11:40 AI concepts in RAGged
11:52 What is Retrieval Augmented Generation (RAG)?
13:15 What are Large Language Models (LLMs)?
14:34 What are embeddings?
15:23 Embedding issues
17:28 Retrieval Augmented Generation(RAG) concepts
17:36 Answer extraction using LLMs
20:02 Information retrieval
21:35 Informational retrieval SOTA (State-of-the-Art)
22:36 Use of chunks in LLMs
23:36 Chunk issues: Chunk size and Multi-chunk processing
24:35 Using prompts with LLMs
26:10 RAGged Edge Box
28:28 Privacy in RAGged 
28:58 Technical sovereignty
29:47 Against planned obsolescence
32:40 RAGged Edge Box Architecture (GitHub walkthrough)
41:55 What is enabling technologies become RAGged Edge Box
42:00 Open Neural Network Exchange
43:52 LLAMA.CPP
45:00 Why RAGged Edge Box uses PHP
47:16 PHP semantic search classes
48:37 Sentence Transformers (Embeddings)
48:59 Q: How are the model updates done?
49:05 A: there are no current model updates at the moment. The model should run offline so no automatic online downloads of updates is supported but it is in the roadmap.
50:11 Q: Which vector database is used?
50:18 A: SQLite is the vector database used and the embedding search is done using SQLite3 vector Search (FAISS) extension.
51:32 Reverse engineering Hugging Face components
52:45 Extending RAGged Edge Box
53:53 Virtual machine packaging: generating virtual box images programmatically
57:56 RAGged Edge Box as a platform
58:38 Current status of the system
1:00:31 Contributing to the project
1:01:00 Other announcements and conclusion
1:04:20 Thank you!
```

https://github.com/data-umbrella/event-transcripts/issues/92


## About the Speaker
Dr. Duboue is an independent language technologist. His work focuses on applied language technology and natural language generation. He received a Licenciatura en Computacion degree from Cordoba University (Argentina) in 1998 and M.S., M.Phil and Ph.D. degrees in Computer Science from Columbia University in the City of New York in 2001, 2003 and 2005. He is passionate about improving society through language technology and splits his time between teaching, doing research and contributing to free software projects. He has taught at Cordoba University, Columbia University, Siglo21 University and has worked for IBM TJ Watson Research as a Research Staff Member.

- LinkedIn: https://www.linkedin.com/in/pabloduboue/

#NaturalLanguageProcessing #Machinelearning #GenAI #RAG


## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=_fJFuL2pLvw" target="_blank"><img src="http://img.youtube.com/vi/_fJFuL2pLvw/0.jpg"
alt="RAGged Edge Box: A Personal AI-Powered Document Search System" width="50%" /></a>

## Transcript
