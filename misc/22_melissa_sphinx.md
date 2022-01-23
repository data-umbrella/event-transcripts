
```text
## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

Melissa Weber:  Intro to Sphinx for Python Documentation

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2021/22-melissa-sphinx.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/275518677/
- Video:   https://youtu.be/tXWscUSYdBs 
- GitHub repo:  https://github.com/melissawm/minimalsphinx
- Slides:  https://hackmd.io/@melissawm/SkjCa3OkO#/

## Resources
- NumPy Documentation: https://numpy.org/doc/stable
- docstrings: https://numpydoc.readthedocs.io/en/latest/format.html#docstring-standard
- Sphinx themes: https://sphinxthemes.com/themes/read-the-docs

## Talk outline
- PART 1: About Sphinx, how it is built and how it works 
- PART 2: Application: an example pull request, fix something small in the NumPy documentation

## Agenda
00:00:00 Reshama introduces Data Umbrella
00:05:21 Reshama introduces Melissa
00:06:50 Melissa begins talk
00:07:38 Tutorial Introduction
00:09:01 How Melissa got involved with NumPy /  Invitation to collaborate with numpy documentation
00:10:01 Impostor Syndrome explanation
00:12:08 What is documentation? (Tutorials, How-to Guides, Explanation, Reference)
00:16:54 What is Sphinx?
00:18:00 configuration file: conf.py
00:19:00 Getting started with sphinx (installation) (conf.py, index.rst, _build/html)
00:20:43 What is reStructuredText? (rst files)
00:22:21 demo of MinimalSphinx Project: https://github.com/melissawm/minimalsphinx
00:22:55 pokemon
00:24:05 What is reStructuredText?
00:24:25 comparing reStructuredText (reST) to Markdown (md)
00:25:51 reStructuredText format II (directives are blocks of explicit markup)
00:27:44 Auto-documenting a python package (autodoc)
00:28:45 Q&A: Do the docstrings have to be in rst?
00:29:30 ":members:" options
00:29:58 Other extensions (sphinx.ext.doctest, sphinx.ext.intersphinx)
00:33:08 Minimal sphinx, example
00:35:00 run "make html" command
00:39:50 Q&A: Should we consider doctest vs pytest? (They are complementary. Use both.)
00:40:30 Example: NumPy docs (how to contribute) (https://numpy.org/doc/stable/dev/)
00:43:20 Getting involved with NumPy, Communicating: https://numpy.org/contribute/
00:43:27 A pull request to the NumPy documentation
00:44:20 Fixing a Typo in NumPy Docs
00:46:20 Fork numpy repo on GitHub
00:47:15 Clone repo
00:47:55 Add remote: git remote add upstream
00:49:05 Branch: git checkout -b doc_fix
00:49:43 Find file: cd doc/source/user/
00:52:30 Set up virtual environment
00:53:40 pip install cython (numpy dependency)
00:56:00 build the docs: "cd doc", "make html"
01:00:30 Q&A: Can sphinx be used for other languages? (yes)
01:00:55 Q&A: Why did we build NumPy? (we want to generate doc with latest version of numpy)
01:03:33 Jupyter notebooks
01:04:15 Final thoughts by Melissa
01:06:15 Q&A: Why do we build from source?



## Event
This webinar will focus on a high-level explanation of how the Sphinx tool for generating documentation automatically works for Python packages, using NumPy as an example (but won't be restricted to the NumPy use case). We'll talk about advantages and disadvantages of choosing different documentation systems and how to integrate other types of documents (for example, Jupyter Notebooks) in the documentation for a given package.

## About the Speaker
Melissa is an applied mathematician and former university professor turned software enginneer. Nowadays she works at Quansight, developing open-source software and leading the Documentation Team for NumPy. She is also a LaTeX, Fortran and free software enthusiast.

GitHub: https://github.com/melissawm
LinkedIn: https://www.linkedin.com/in/axequalsb/
Twitter: https://twitter.com/melissawm

```
