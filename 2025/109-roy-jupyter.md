# Make Your Own JupyterLab Extension

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2024/109-roy-jupyter.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/304917194/
- Video: https://youtu.be/ERbe2yfXmFY
- Transcriber:  ? [needs a transcriber]

## Resources
- https://jupyterlab.readthedocs.io/en/latest/extension/extension_dev.html
- slides: https://slides.com/invisibleroads/make-your-own-jupyterlab-extension

We have some other Jupyter presentations that complement this well:  
- a) Jupyter Notebook and Data Analysis with Python:
https://youtu.be/hc8-AhYBu08
- b) Debugging in Python, in Jupyter Notebook:
https://youtu.be/1b9fq7-xesI

## About the Event
Make your own JupyterLab extension in this tutorial. JupyterLab is a free and open source, browser based integrated development environment (IDE) that is the successor to Jupyter Notebook. Designed from the core to be extensible, JupyterLab is itself an extension of the Jupyter framework. Since its release, open source developers have contributed hundreds of third party extensions (652 third-party extensions as of 2024-10-15).

JupyterLab extensions can customize or enhance any part of JupyterLab. They can provide new themes, file viewers and editors, or renderers for rich outputs in notebooks. Extensions can add items to the menu or command palette, keyboard shortcuts, or settings in the settings system.

JupyterLab began in 2015 thanks to a $6 million grant from the Leona M. and Harry B. Helmsley Charitable Trust, the Gordon and Betty Moore Foundation and the Alfred P. Sloan Foundation. The first stable release was in 2018. Real time collaboration was added in 2021.

## Timestamps
```
00:00 About Data Umbrella
03:15 About the presentation and presenter
04:00 CrossCompute
04:25 CrossCompute Product History
05:33 Sandbox Tools for Testing JupyterLab Extensions and Extension Development
06:12 Overview
06:50 Brief History of the Jupyter Project
07:40 Jupyter Notebook vs JupyterLab
08:41 Cool Features of JupyterLab that You Might Not Know
10:25 JupyterLab Basics: Installation, Essential Keyboard Shortcuts
12:20 JupyterLab Basics: Notebook Pre-Commit Hooks for Clearing Outputs
13:39 JupyterLab Basics: Notebook Pre-Commit Hooks for Linting using nbqa
14:28 JupyterLab Basics: Notebook Diffs to Compare Changes using nbdime
15:12 JupyterLab Basics: Activating the JupyterLab Debugger kernel using xeus-python
16:22 JupyterLab Basics: Try Untrusted JupyterLab Extensions in a Sandbox Environment
17:05 JupyterLab Basics: Vim Key Bindings for JupyterLab with jupyterlab-vim
17:33 JupyterLab Basics: Interactive Matplotlib Plots for JupyterLab with ipympl
18:21 JupyterLab Extensions: Plotting (ipympl, ipydatagrid, ipywidgets, pythreejs, mapboxgl-jupyter, ipyleaflet, pydeck, jupyter_bokeh)
18:31 JupyterLab Extensions: Plotting spreadsheet data with ipydatagrid
19:47 JupyterLab Extensions: Publishing (spellchecker, jupyterlab-latex, jupyterbook, jupyterlab-crosscompute)
20:15 JupyterLab Extensions: Publishing web-based tools with jupyterlab-crosscompute
21:07 JupyterLab Extensions: Code (jupyterlab-lsp, nbdime, jupytext, nbqa, search-replace, jupyterlab-vim, jupyterlab-variableInspector, jupyter-resource-usage, gather, jupyter-ai)
21:15 JupyterLab Extensions: Code using Supercharged Tooltips with jupyterlab-lsp
22:27 JupyterLab Extensions: Code Collection with gather
22:50 JupyterLab Extensions: Code Block Completion with jupyter-ai
23:00 JupyterLab Extensions: Repository (jupyterlab-git, jupyterlab-gitlab, jupyterlab-github)
23:05 JupyterLab Extensions: Repository Clickable Git Commands with jupyterlab-git
23:38 JupyterLab Extensions: Data (jupyterlab-spreadsheet, jupyterlab-spreadsheet-editor, jupyterlab-sql, jupyter-archive, jupyter-fs)
23:48 JupyterLab Extensions: Data Spreadsheet Editing using jupyterlab-spreadsheet-editor
24:09 JupyterLab Extensions: Data from Compressed Archives using jupyter-archive
24:22 JupyterLab Extensions: Data from Networked File Systems like S3 using jupyter-fs
24:36 JupyterLab Extensions: Deployment (jupyter-scheduler, jupyterlite)
24:39 JupyterLab Extensions: Deployment via Scheduled Jobs using jupyter-scheduler
25:00 JupyterLab Extensions: Deployment using WASM in the Browser using jupyterlite
25:18 Make a JupyterLab Extension: Overview
25:50 Make a JupyterLab Extension: Documentation Highlights (Common Extension Points, Extension Examples README)
26:45 Make a JupyterLab Extension: How to Experiment with Example Extensions
27:20 Make a JupyterLab Extension: How to Read the Code of a JupyterLab Extension by Examining Entrypoints
28:25 Make a JupyterLab Extension: How to Start a Sandbox Pair Programming Session Restricted to Specific IP Addresses and SSH Keys
30:13 Make a JupyterLab Extension: How to Install and Test Example Extensions in a Remote Sandbox
30:50 Make a JupyterLab Extension: Examining the Entrypoint for the Front End of a JupyterLab Extension
31:30 Make a JupyterLab Extension: How to Start Your Extension from a Template
32:48 Make a JupyterLab Extension: Walkthrough - Add Right Sidebar
33:26 Make a JupyterLab Extension: Walkthrough - Listen for Events in Shell and Show Events with console.log
33:55 Make a JupyterLab Extension: Walkthrough - Listen for Events in Shell and Show Events in a React Widget
34:30 Make a JupyterLab Extension: Walkthrough - Use Signals to Connect Your Widget with Events from Other Widgets
35:57 Make a JupyterLab Extension: Walkthrough - Listen for Events in the File Browser
36:17 Make a JupyterLab Extension: Walkthrough - How to Handle Module Not Found Error by Adding Dependencies
37:03 Make a JupyterLab Extension: Walkthrough - Open File in Shell (or How to Cause Changes in Other Widgets)
38:10 Make a JupyterLab Extension: Walkthrough - Add CSS Styling to Your Extension Components
38:47 Make a JupyterLab Extension: Walkthrough - Add Button to Call the Server (or How to Get the Front End to Call the Back End API)
39:05 Make a JupyterLab Extension: Walkthrough - How to Write a View for the Server Extension (or How to Make the Back End API for Your Extension)
39:43 Make a JupyterLab Extension: Walkthrough - Where to Find the Code for the Walkthrough in https://github.com/crosscompute/jupyterlab-crosscompute
40:55 Make a JupyterLab Extension: How to Search the Standard Extensions for Hints using vim $(grep -InR "YOUR QUERY" * -l)
42:06 Make a JupyterLab Extension: Standard Extensions Overview
42:50 More Resources
```
https://github.com/data-umbrella/event-transcripts/issues/92

## About the Speaker: Roy Hyunjin Han
For the past several years, Roy has been working on CrossCompute, a distributed computing platform for deploying decision support tools. He is interested in infrastructure planning and hazard mitigation.

- LinkedIn: https://www.linkedin.com/in/invisibleroads/

#OpenSource #Jupyter #JupyterLab


## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=ERbe2yfXmFY" target="_blank"><img src="http://img.youtube.com/vi/ERbe2yfXmFY/0.jpg"
alt="Make Your Own JupyterLab Extension" width="50%" /></a>

## Transcript
