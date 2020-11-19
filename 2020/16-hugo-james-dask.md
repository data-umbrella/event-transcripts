# Hugo Bowne-Anderson and James Bourbeau:  Data Science and Machine Learning at Scale

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/16-hugo-james-dask.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/273593514/
- Video:   https://youtu.be/MHAjCcBfT_A
- Jupyter notebook:  https://github.com/coiled/data-science-at-scale/tree/master/notebooks/data-umbrella-2020-10-27
- GitHub repo:  https://github.com/coiled/data-science-at-scale
- Transcriber:  <a href='https://github.com/'>Cynthia Thinwa</a>

## Video

<a href="http://www.youtube.com/watch?feature=player_embedded&v=MHAjCcBfT_A" target="_blank">
  <img src="http://img.youtube.com/vi/MHAjCcBfT_A/0.jpg"
       alt="Data Science and Machine Learning at Scale" width="50%" /></a>

## Transcript

### Introduction (<a href='https://youtu.be/MHAjCcBfT_A'>0.00</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=1">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t0.00.JPG"
       alt="Notebook setup" width="50%" /></a>

**Reshama**:

Okay - hello and welcome to Data Umbrella's webinar for October; so I'm just going to go over the agenda, I'm going to do a brief introduction then there will be the workshop by Hugo and James and you can ask questions along the way in the chat or - actually the best place to ask questions is the Q&A and there's an option to upvote as well. So yeah; asking the Q&A - if you happen to post it on the chat by mistake I can also transfer it over to Q&A so that would be fine too and this webinar is being recorded.

Briefly about me: I am a statistician and data scientist and I am the founder of Data Umbrella; I am on a lot of platforms as @reshamas so feel free to follow me on Twitter and LinkedIn. We have a code of conduct; we're dedicated to providing a harassment-free experience for everyone; thank you for helping to make this a welcoming, friendly professional community for all and this code of conduct applies to the chat as well. So our mission is to provide an inclusive community for underrepresented persons in data science and we are an all-volunteer-run organization.

You can support Data Umbrella by doing the following things: you can follow our code of conduct and keep our community a place where everybody wants to keep coming to, you can donate to our open collective and that helps to pay meet-up dues and other operational costs and you can check out this link here on GitHub - we have this new initiative where all the videos are being transcribed and... so it's to make them more accessible - so we take the YouTube videos and we put the raw there and so we've had a number of volunteers help us transcribe it; so feel free to check out this link and maybe if you do this video, maybe the two speakers will follow you on Twitter; I can't promise anything but it's possible.

Data Umbrella has a job board and it's at jobs.dataumbrella.org and once this gets started I'll put some links in the chat. The job that we are highlighting today is the machine learning engineer job by Development Seed and Development Seed is based in Washington DC and Lisbon, Portugal and they do - I'm going to go to the next slide - what they do is they're doing social good work and so they're doing for instance, mapping elections from Afghanistan to the U.S, analyzing public health and economic data from Palestine to Illinois and leading the strategy and development behind data for World Bank and some other organizations and I will share a link to their job posting in the chat as well as soon as I finish this brief introduction.

Check out our website for resources - there's a lot of resources on learning Python and R, also for contributing to open source, also for guides on accessibility and responsibility and allyship. We have a monthly newsletter that goes out towards the end of the month and it has information on our upcoming events - we have two great events coming up in November and December on open source so subscribe to our newsletter to be in the know. We are on all social media platforms as Data Umbrella; Meetup is the best place to join to find out about upcoming events, our website has resources, follow us on Twitter, we also share a lot of information on LinkedIn, and if you want to subscribe to our YouTube channel we record all of our talks and post them there within about a week of the talk so it's a good way to get information.

Okay and now we are ready to get started. So I will hand it over to - put myself on mute - and I will hand it over to Hugo and James and let you take over.

**Hugo:**

Thank you all for joining I just want to thank Reshama, Christina and and everyone else who tire - all the tireless effort that - that goes into putting these meet-ups and these online sessions together. I think one thing I want to say is actually the last in-person workshop I gave - either at the end of February or early March was Data Umbrella's inaugural tutorial and meetup if I recall correctly - on Bayesian thinking and hacker statistics and simulation and that type of stuff, so it's just wonderful to be back particularly with my colleague and friend James. We're building really cool distributed data science products at Coiled - we'll say a bit about that but we'll do some introductions in a bit.

### How to access and set up notebooks used in the webinar (<a href='https://youtu.be/MHAjCcBfT_A?t=300'>05:00</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=300">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t05.00.JPG"
       alt="Notebook setup" width="50%" /></a>
       
**Hugo:**

I just wanted to get you all accustomed to - it was February, thank you Reshama. We're working with Jupyter notebooks in a GitHub repository - the repository is pinned to the top of the chat. This is what it looks like (scrolling down the repository homepage) - these are all the files; this is the file system.

Now we use something called Binder which is a project, out of and related to Project - Project Jupyter which provides infrastructure to run notebooks without any local installs. So there are two ways you can you can code along on this tutorial; the first is - and i won't get you to do this yet - is to launch Binder. The reason I won't get you to do that yet is because once you launch it we have 10 minutes to start coding or the Binder session times out - I've been burnt by that before, actually several times - I'm surprised I even remembered it this time. The other thing you can do is install everything locally by cloning the repository, downloading Anaconda, creating a Conda environment - if you haven't done that, I suggest you do not do that now - and you launch - launch the Binder. James is going to start by telling us a few things about about Dask and distributed computing in general.

My question for you James is: if we get people to launch this now, will we get to execute a cell - code cell in 10 minutes?

**James:**

I would... let's hold off for now maybe..

**Hugo:**

Yep.

**James:**

Maybe I'll indicate when we should launch Binder.

**Hugo:**

Okay, fantastic.

**James:**

Cool um and just for reference -

**Hugo:**

So -

**James:**

What I'm looking at right now is the GitHub repository on your browser...

**Hugo:**

Yes.

**James:**

Okay.

**Hugo:**
Exactly. So I will not launch Binder now - I will not get you to now... I've - I'm doing this locally... (highlights notebook located in `localhost` onscreen) and we see that I'm in notebook zero, and if you want to actually have a look at this notebook before launching Binder, it's in the (highlights notebook location in GitHub onscreen) *Notebooks Data Umbrella...* subdirectory  (clicks notebook location in GitHub onscreen) and it's (highlights notebook location in GitHub onscreen) notebook zero and we're going to hopefully make it through the overview then (highlights notebook location in GitHub onscreen) chatting about Dask - Dask *delayed* and - and (highlights notebook location onscreen) *dataframe* and (highlights notebook location onscreen) *machine learning*.

Great so we have... Hashim has said you could open in VS Code as well; you could - I mean, that would require all your local installs and that type of stuff as well but we're to introduce me and James; we work at Coiled where we build products for distributed computing infrastructure. As we'll see one of the big problems with like bursting to the cloud is all the like Kubernetes, AWS, Docker stuff, so we build a one-click host of deployments for Dask but for data science and machine learning in general. James maintains Dask along with Matt - Matt Rocklin who created Dask with a team - people who were working with Continuum, Anaconda at the time - and James is a software engineer at Coiled and I run Data science evangelism, Marketing, work on a bunch of product stuff as well, wear a bunch of different hats occasionally; there are many ways to think about distributed compute and how to do it in Python. We're going to present - hey James, you're muted -

**James:**

I'm taking it I went away based on what I see in the chat...

**Hugo:**

You did, you did but now we're back; I've introduced you, I've introduced me, I've mentioned that there are many ways to do distributed compute in the Python ecosystem and we'll be
chatting about one called Dask and maybe I'll pass to you in a second but I'll say one thing that I really like about - my background isn't in distributed compute my background's in
Pythonic data science. When thinking about bursting to larger data sets and larger models, there are a variety of options. The thing that took me, attracted me to Dask - originally.
I saw Cameron's note  "The ghosts in the machine aren't playing nice tonight I think that ain't that the truth" - is that Dask plays so nicely with the entire Py data ecosystem so as we'll see if you want to write Dask code for dataframes - Dask DataFrames - it really mimics your Pandas code; same with Numpy, same with Scikit-learn - okay? And the other thing is Dask essentially runs the Python code under the hood so your mental model of what's happening is - actually corresponds to the code being executed. Okay.. now I'd like to pass over to James but it looks like he's disappeared again -

**James:**

I'm still here if you can hear me, I've just turned my camera off.

**Hugo:**

Oh yeah! Okay great.

**James:**

I'm gonna turn my camera... hopefully that will help, yeah -

**Hugo:**

And I might do, do the same for bandwidth, bandwidth issues so if you want to jump in and talk about Dask at a high level, I'm sharing my screen and we can scroll through (scrolls through notebook located at `localhost`).

### An overview of Dask (<a href='https://youtu.be/MHAjCcBfT_A?t=590'>09:50</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=590">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t09.50.JPG"
       alt="Notebook setup" width="50%" /></a>

**James:**

Yeah that sounds great. So that's sort of - a nutshell - you can think of it as being composed of two main... well, components.

<a href="https://youtu.be/MHAjCcBfT_A?t=610">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t10.10.JPG"
       alt="Dask components" width="50%" /></a>

The first we call collections; these are the user interfaces that you use to actually construct a computation you would like to compute in parallel or on distributed hardware. There are a few different interfaces that Dask implements... for instance, there's Dask Array for doing nd array computations, there's Dask DataFrame for working with tabular data... you can think of those as like - Dask Array as a parallel version of Numpy, Dask DataFrame as a parallel version of Pandas and so on. There are also a couple other interfaces that we'll be talking about; Dask delayed for instance - we'll talk about that today - we'll also talk about the Futures API; those are sort of for lower level custom algorithms, in sort of paralyzing existing - existing code. The main takeaway is that there are several sort of familiar APIs that Dask implements and that we'll use today to actually construct your computation. So that's the first part of Dask - it is these Dask collections - you then take these collections, set up your steps for your computation and then pass them off to the second component which are Dask schedulers and these will actually go through and execute your computation potentially in parallel. There are two flavors of schedulers that Dask offers. The first - is a - are called single machine schedulers and these just take advantage of your local hardware they will spin up a a local thread or process pool and start submitting tasks in your computation to to be executed in parallel either on multiple threads or multiple processes. There's also a distributed scheduler - or maybe a better term for... would actually be called the advanced scheduler because it works well on a single machine but it also scales out to multiple machines, so for instance as you'll see later we will actually spin up a  distributed scheduler that has workers on remote machines on AWS so you can actually scale out beyond your local resources like say what's on your laptop.

(Scrolls through notebook located at `localhost`) Kind of scrolling down then to the image of the cluster we can see the main components of the distributed scheduler -

**Hugo:**

And James, I might get people to spin up the Binder now because we're going to execute codes-

**James:**

Yeah... now is a good point. Yep -

**Hugo:**

So just - here's a quick break point before you know... a teaser for schedulers and what's happening there. I'll ask you to - in the repository there's also the link to the binder; click on launch binder (right-clicks the link), i'm going to open it in a new tab and what this will create is an environment in which you can just execute the code in - in the notebooks okay... (displays the opened tab at *mybinder.org* where `coiled/data-science-at-scale/master` repository is loading) so hopefully by the time we've gotten - gone through this section, this will be ready to start executing code. So if everyone wants to do that - to code along... otherwise just watch - or if you're running things locally, also cool; thanks James.

#### An illustration of a distributed scheduler (<a href='https://youtu.be/MHAjCcBfT_A?t=780'>13:00</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=780">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t13.04.JPG"
       alt="Scheduler" width="50%" /></a>

**James:**

Yeah, yeah no problem, thank you. So - so yeah, looking at the image for the distributed scheduler; we're not gonna have time to go into the... a lot of detail about the distributed scheduler in this workshop so - but we do want to provide at least a high level overview of the, the different parts and components of the distributed scheduler.

So the first part I want to talk about is in the diagram what's labeled as a client. So this is the user facing entry point to a cluster; so um wherever you are running your python session... that could be in a jupiter lab session - like we are here, that could be in a python script somewhere... you will create and instantiate a client object that connects to the second component which is the Dask scheduler.

So each Dask cluster has a single scheduler in it that sort of keeps track of all of the state - for all of the - the state of your cluster and all the tasks you'd like to compute; so from your client you might start submitting tasks to the cluster... the scheduler will receive those tasks and compute things like all the dependencies needed for that task like say you're implementing - you say you want to compute Task C, but that actually requires first you have to compute Task B and Task A - like there are some dependency structures there; it'll compute those dependencies as well as keep track of them. It'll also communicate with all the workers to understand what worker is working on which task and as space frees up on the workers it will start farming out new tasks to compute to the workers.

So in this particular diagram there are three Dask distributed workers here; however, you can have as you can have thousands of workers if you'd like. So the workers are the things that actually compute the tasks. They also store the results of your tasks and then serve them back to you in the client. The scheduler basically manages all the state needed to perform the computations and you submit tasks from the client. So that's sort of a quick whirlwind tour of the different components for the distributed scheduler and at this point I think it'd be great to actually see - see some of this in action... Hugo, would you like to take over?

### Dask in action (<a href='https://youtu.be/MHAjCcBfT_A?t=915'>15:14</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=915">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t15.23.JPG"
       alt="Dask in action" width="50%" /></a>

**Hugo:**

Absolutely. Thank you for that wonderful introduction to Dask and and the schedulers in particular and we are going to see that with Dask in action. I'll just note that this tab in which I launched the binder, is up and running - if you're going to execute code here, click on *notebooks*, click on *data umbrella* and then go to the *overview* notebook and you can drag around (drags one of the three dashboards displayed). We'll see the utility of these - these dashboards in a second but you can, you know drag your stuff around to - to make - you know, however you want to - want to structure it and then you can execute code in here. I'm not going to do that,  I'm going to do this locally at the moment (opens notebook at `localhost`); but just to see Dask in action to begin with, I'm going to - I'm actually going to restart kernel and clear my outputs - so I'm going to import from Dask distributed, the client, the - sorry the other thing I wanted to mention is we made a decision around content for this. We do have a notebook that we - we love to teach on schedulers but we decided to switch it out for machine learning for this workshop in particular; we are teaching a similar although distinct workshop at PyData Global so we may see some of you there in which we'll be going more in depth into schedulers as well, so if you want to check that out definitely do so. We instantiate the client which as James mentioned is kind of what we work with as the user to submit our code. So that will take - take a few seconds... okay it's got a port in use so it's going - going elsewhere. What I'll just first get you to notice is that it tells us where our dashboard is - and we'll see those tools in a second - tells us about our cluster that we have four workers, eight cores, between eight and nine gigs(gigabytes) of - of RAM... okay?

Now this is something I really love about Dask, all the diagnostic tools - if I click on the little Dask thing here (clicks on the Dask icon in the leftmost panel) and (navigates to the binder) we've modified the binder so that - that exists there as well. We can see (clicks on the Dask icon) - i'll hit search (clicks on search icon within the pop-up menu from the Dask icon) and it should - (search result displays the same port as the port that is the output from the scheduler on the notebook) that now corresponds to the - the scheduler. Now i want to look at the task stream (clicks on the `TASK STREAM` button within the pop-up menu from the Dask icon, placing the Dask Task Stream dashboard to the right) which will tell us in real time what's happening; i also want to look at the (clicks on the `CLUSTER MAP` button within the pop-up menu from the Dask icon, placing the Dask Cluster Map dashboard just below the Dask Task Stream dashboard that is positioned to the right) cluster map. So we see here - this is already really cool - we've got all of our workers around here (moves cursor around a small dashboard below the Dask icon pop-up menu) and our scheduler - scheduler there and when we start doing some compute we'll actually see information flowing between these... and the other thing maybe... I'll yeah... I'll include a little progress (clicks on the `PROGRESS` button within the pop-up menu from the Dask icon, placing the Dask Progress dashboard to the right of the Dask Cluster Map dashboard) and that can be an alternate tab to... ask... I'm wondering perhaps I also want to include something about the workers (clicks on the `WORKERS` button within the pop-up menu from the Dask icon, placing the Dask Workers dashboard between the Dask Cluster Map and the Dask Progress dashboards).

Yeah, okay... great. So we've got a bunch of stuff that's - that's pretty interesting there and so the next thing I'm going to do... we've got a little utility file (highlights code cell containing `%run prep.py -d flights`) which downloads some of the data and this is - what it does is if you're in Binder it downloads a subset of the data; if you're anywhere else it downloads a larger set. For this particular example we're dealing with a small data set - you see the utility of Dask and distributed compute when it generalizes to larger data sets, but for pedagogical purposes we're going to sit with a smaller data set so that we can actually run - run the code: there's a trade-off there. So actually, that was already downloaded it seems but you should all see it download... I'm actually going to run that in the binder just to - you should start seeing `Downloading nyc flights dataset... done`, `Extracting`... `Creating json data` etc. Okay now what we're going to do is we're going to read in this data as a Dask DataFrame - and what I want you to notice is that it - really, the Dask code mimics Pandas code,  so instead of `pd.read_csv()` we've got `dd.read_csv()`. We've got, you know, this is the file path - the first argument; we're doing some parse date, setting some data types... okay? We've got a little  wild card regular expression there to - to join - to do a bunch of them... and then we're performing a `groupby`... okay? So we're grouping by the origin of these flights - flight data, we're looking at the the mean departure delay group(ed) by origin... the - the one difference i want to make clear is that in Dask we need a `.compute()` method; that's because Dask performs lazy computation - it won't actually do anything, because you don't want it to do anything on really large data sets until you explicitly tell it - tell it to compute.

So i'm going to execute this now (runs code cell) and we should see some information transfer between the scheduler and the workers and we should see tasks starting - starting to be done, okay? So moment of truth... fantastic (code cell displays output, the clusters show lines moving among them, the task stream creates a sort of bar graph and the code cell stops running) so we call this a pew pew plot because we see pew! pew! pew! We saw a bunch of data transfer happening between them (the clusters)... these are all our calls and we can see tasks happening... it tells us what tasks there are. We can see that most of the time was spent reading reading CSVs (highlights `read csv` in task graph), then we have some groupbys on chunks and - and that type of stuff (highlights task in task graph). So that's a really nice diagnostic tool to see what most of your work is - is actually doing under Dask Workers you can see memory used, `CPU use`, more fine-grained examples there. So I - I'd love to know if, in the Q&A, I'm going to ask... Were you able to execute this code?... and if you were in Binder just a thumb up, a vote would be - no - would be fantastic; much appreciated.

So as we've mentioned I just wanted to say a few things about tutorial goals: the goal is to cover the basics of Dask and distributed compute; we'd love for you to walk away with an understanding of when to use it, when to not, what it has to offer; we're going to be covering the basics of Dask Delayed, which, although not immediately applicable to data science, provides a wonderful framework for thinking about Dask - how Dask works and understanding how it works under the hood; then we're going to go into Dask DataFrames and then machine learning hopefully. Due to the technical considerations with... we've got less time than - than we thought we would but we'll definitely do the best we can. We may have less time to do exercises - so we've had two people who were able to execute this code... if you - if you tried to execute it in Binder and were not able to, perhaps post that in the Q&A - but we also have several exercises and I'd like you to take a minute just to do this exercise. The i- I'm not asking you to do this because i want to know if you're able to print     `hello world` i'm essentially asking you to do it so you get a sense of how these exercises work. So if you can take 30 seconds to print `hello world` then we'll - we'll move on after that, so just take 30 seconds now - and it seems like we have a few more people who were able to execute code which - which was great... okay, fantastic. So you will put your solution there for some reason I have an extra cell here so i'm just going to clip that (deletes blank code cell) and to see a solution uh i'll just get you to execute this cell (highlights a code cell containing `%load solutions/overview.py`) and it provides the solution and then we can execute it and compare it to the the output of what you had, okay? 'Hello world.'

### Working directly from the cloud with Coiled (<a href='https://youtu.be/MHAjCcBfT_A?t=1401'>23:21</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=1401">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t23.23.JPG"
       alt="Working with Coiled" width="50%" /></a>

**Hugo:**

So as as we saw, I've done all this locally, you may have done it on Binder... there is an option to work directly from the cloud and I'll - I'll take you through this - there are many ways to do this. As I mentioned we're working on one way with Coiled and I'll explain the rationale behind that in - in a second but I'll show you how easy it is to get a cluster up and running on - on AWS without even interacting with AWS for free, for example; you can follow along by signing into Coiled cloud. To be clear, this is not a necessity and it does involve you signing up to our product, so i just wanted to be absolutely transparent about that; it does not involve any credit card information or anything along those lines and in my opinion it does give a really nice example of how to run stuff on the cloud. To do so you can sign in at <a href='https://cloud.coiled.io/'>cloud.coiled.io</a> you can also `pip install coiled` and then do authentication; you can also spin up this - this hosted Coiled notebook (clicks <a href='https://cloud.coiled.io/jobs/coiled/quickstart'>link</a> on notebook), so I'm going to spin that up now and I'm going to post that here... actually yep, I'm gonna post that in the chat if you - let me get this right - if you've - if you've never logged in to Coiled before it'll ask you to sign up using Gmail or GitHub so feel free to do that if you'd like; if not that's also also cool, but I just wanted to be explicit uh about that.

The reason I want to do this is to show how Dask can be leveraged to do work on really large data sets; so you will recall that i had between eight and nine gigs of RAM on my local system - oh wow Anthony says, "On iPad, unable to execute on Binder," incredible... I don't have a strong sense of how Binder works on iPad; I do know that I was able to - to check - to use a binder on my iPhone several years ago on my way to Scipy doing code review for someone - for Eric Maher i think, for what that - that's worth... but back to this, we have this NYC taxi dataset which is over 10 gigs - it won't even - I can't even store that in local memory - I don't have enough RAM to store that. So we do need, either to do it locally in an out of core mode of some sort or we can we can burst to the cloud - and we're actually going to burst to the cloud using - using coiled; so the notebook is running here (navigates to the Coiled page) for me and - but - I'm actually gonna do it from my local - local notebook (navigates to JupyterLab loading the notebook hosted in Coiled) but you'll see... and once again feel free to code along here... it's spinning up a notebook and James who is - is my co-instructor here is to be - I'm, I'm so grateful all the work is done on our notebooks in Coiled - you can launch the cluster here and then analyze the entire... over 10 gigs of data there... I'm going to do it here (navigates to the notebbok in `localhost`).

So to do that, I import Coiled and then I import the Dask distributed stuff (highlights code cell) and then I can create my own software environment (highlights next code cell), cluster configuration (highlights next code cell) - I'm not going to do that because the standard Coiled cluster configuration software environment (highlights next code cell) works. Now i'm going to spin up a cluster (highlights and runs next code cell) and instantiate a client.

Now because we're spinning up a cluster in - in the cloud, it'll take - it'll take - a minute - a minute or two... enough time to make a cup of coffee but it's also enough time for me to just talk a bit about why this is important and there are a lot of a lot of good - good people working on - on similar things... but part of the motivation here is that if you want to... you don't always want to do distributed data science, okay? First I'd ask you to look at - instead of using Dask, if you can optimize your Pandas code, right? Second I'd ask, if you've got big datasets - it's a good question - do you actually need all the data? So I would - if you're doing machine learning, plot your learning curve; see how accurate... see how your accuracy or whatever your metric of interest is improves as you increase the amount of data - right? - and if it plateaus before you get to a large data size then you may as well, most of the time, use your small data; see if sub-sampling can actually give you the results you need. See if you can get a bigger, bigger - access to a bigger machine so you don't have to burst to the cloud; but after all these things if you do need to burst - burst to the cloud, until recently you've had to get an AWS account, you've had to, you know, set up containers with Docker and/or Kubernetes and do all of these kind of - I suppose - DevOpsy software engineering foo stuff which, which if you're into that I - I absolutely encourage you - encourage you to do that... but a lot of working data scientists aren't paid to do that and don't necessarily want to. So that's something we're working on, is thinking about these kind of one-click hosted deployments so you don't have to do all of that; having said that I very much encourage you to try doing that stuff if - if you're interested.

We'll see that the - the cluster has just been created and what I'm going to do, we see that - oh I'm sorry, I've done something funny here... I'm - I'm referencing the previous client, aren't I James?

**James:**

Yeah it looks like you should go ahead and connect a new client to the Coiled cluster -

**Hugo:**

and... 

**James:**

making sure not to re-execute the cluster creation because -

**Hugo:**

Yeah, exactly. So, would that be... how would I... what's the call here?

**James:**

I would just open up a new cell and say `client = Client` and then pass in the cluster, like `(cluster)` (typing the code `client = Client(cluster)` in a new cell)... yeah -

**Hugo:**

Great... okay, fantastic - and what we're seeing is a slight version... this (highlights code cell output) - we don't need to worry about this; this is essentially saying that
the environment on the cloud mis- is there's a slight mismatch with my, with my local environment; we're fine with that. I'm going to look here - for a certain reason the - the dashboard isn't quite working here at the moment. James would you suggest i just click on this and open a new

**James:**

Yeah... click on the ecs dashboard link (in the code output)

**Hugo:**

Oh yes, fantastic... so... yep, there's some bug with the local dashboards that we're - we're currently - currently working on but what we'll see now... just a sec, I'm going to remove all of this (closes all previously opened dashboards and the Dask icon popup menu) - we'll see now that I have access to 10 workers, I have access to 40 cores and I have access to over 170 gigs of memory (resizes window containing notebook on `localhost` to show Dask dashboards at the ecs link mentioned earlier lying to the right)... okay, so now I'm actually going to import this data set (highlights and runs code cell in notebook on `localhost`) and it's the entire year of data from 2019, and we'll start seeing on - on the diagnostics all the, all the processing happening, okay? So... actually, not yet because we haven't called compute (i.e. added `.compute()` to the `dd.read_csv()` function)... okay, so it's done this lazily, we've imported it - it shows kind of like Pandas when you show a dataframe, the column names and data types - but it doesn't show the data because we haven't loaded it yet; it does tell you how many partitions it is. So essentially - and we'll see this soon - Dask DataFrames correspond to collections of Pandas DataFrames so there are really 127 Pandas DataFrames underlying this Dask DataFrame.

So now i'm going to do the compute - well I'm going to set myself up for the computation to do a group by passenger count and look at the mean tip (runs code cell) - now that took a very small amount of time; we see the ipython magic timing there because we haven't computed it - now we're actually going to compute (runs next code cell) - and James if you'll see in the chat, Eliana said her Coil-Coiled authentication failed; I don't know if you're able to to help with that but if you are, that would be great... and it may be difficult to debug in - but look; as we see, we have the task stream now and we see how many - you know we've got 40 cores working together, we saw the processing, we saw the bytes stored - it's over 10 gigs as I said - and we see we were able to do our basic analytics. We were able to do it on a 10 plus gig dataset in - in 21.3 seconds which is pretty - pretty exceptional. If any - any code-based issues come up and they're correlated in particular... so if you have questions about the code execution please ask in the Q&A not in the chat because others cannot vote it and I will definitively prioritize questions on technical stuff particularly ones that up- that are upvoted; but yeah, I totally agree thanks - thanks very much.

### Working with Dask DataFrames (<a href='https://youtu.be/MHAjCcBfT_A?t=1963'>32:43</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=1963">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t32.49.JPG"
       alt="Working with Dask DataFrames" width="50%" /></a>

**Hugo:**

So yeah... let's jump into - into Dask DataFrames (opens notebook two at `localhost`). So of course we write here that in the last exercise we used Dask Delayed to parallelize loading multiple csv files into a Pandas DataFrame. We're not - we - we haven't done that but you can definitely go through and have a look at that - but I think perhaps even more immediately relevant for a data science crowd and an analytics crowd is - which is what I see here from the reasons people - people have joined - is jumping into Dask DataFrames, and as I said before a Dask dataframe really feels like a Pandas dataframe, but internally it's composed of many different - different dataframes. This is one - one way to think about it, that we have all these Pandas dataframes and the collection of them is a Dask dataframe - and as we saw before they're partitioned. We saw when we loaded the taxi dataset in the Dask dataframe was 127 partitions right? Where each partition was a normal Panda - Pandas dataframe and they can live on disk as they did, early in the first example - Dask in action - or they can live on other machines as when I spun up a coiled cluster and and did it on - on AWS.

Something I love about Dask's dataframes - I mean I rant about this all the time - it's how... it's the Pandas API and - and Matt -Matt Rocklin actually has a post on - on the blog called "A brief history of Dask" in which he talks about the technical goals of Dask but also talks about a social goal of Dask which in Matt's words is to "invent nothing"; he wanted and the team wanted the Dask API to be as comfortable and familiar for users as possible and that's something  really appreciate about it.

So we see we have element - *elementwise operations*, we have the - our favorite - *row-wise selections*, we have *loc*, we have the *common aggregations*, we saw *groupby*s before, we have *is in*s, we have *datetime string accessors*. Oh James! We forgot to - I forgot to edit this and I -it should be *groupby* - I don't know what - what a *froupby* is but that's something... we'll make sure the next iteration to - to get it right; at least we've got it right there and in the code but have a look at the Dask dataframe API docs to check out what's happening and a lot of the time Dask dataframes can serve as drop in replacements for Pandas dataframes. The one thing that I just want to make clear as I did before, is that you need to call `compute()` because of the lazy - lazy compute property of Dask. So this is wonderful to talk about when to use Dask dataframes. So if your data fits in memory use Pandas; if your data fits in memory and your code doesn't run super quickly I wouldn't go to Dask, I'd try to - I'd do my best to optimize my Pandas code before trying to get gains - gains and efficiency; but Dask itself becomes useful when the dataset you want to analyze is larger than your machine's RAM, where you normally run into memory errors and that's what we saw with the taxicab example. The other example that we'll see when we get to machine learning is you can do machine learning on a small dataset that fits in memory but if you're building big models or training over like a lot of different hyperparameters or different types of models, you can you can parallelize that using - using Dask. So there is, you know - you want to use Dask perhaps in the big data or medium to big data limit as we see here, or in the medium to big model limit where training, for example, takes and takes a lot of time, okay?

So without further ado let's get started with Dask dataframes; (highlights a code cell) you likely ran this preparation file to get the data in the previous notebook but if you didn't execute that... now we're going to (highlights a code cell) get our file names by doing - doing a few joins and we see our file is a string `data/nycflights/*` - to access all of them - `.csv` and we're going to import our Dask dust.dataframe and read in (highlights a code cell containing `dd.read_csv()`) our dataframe, parsing some dates, setting some - setting some data types, okay? I'll execute that (runs all cells above together with the current cell) we'll see we have 10 partitions... as we noted before, if this was a Pandas dataframe we'd see a bunch of entries here; we don't, we see only the column names and the data types of the columns and the reason is, as we've said it explicitly here, is the representation of the dataframe object contains no data, it's done - Dask has done enough work to read the start of the file so that we know a bit about it, some of the important stuff and then infer the column types and column names and data types, okay?... but we don't - once again we don't - let's say we've got 100 gigs of data, we don't want to like do this call and suddenly it's reading all that stuff in and doing a whole bunch of compute until we explicitly tell it to, okay?

(Highlights a code cell containing `df.columns`) Now this is really cool... if you know a bit of Pandas you'll know that you can there's an attribute `columns` which (runs code cell) prints out - it's well... it's actually the columns form an index, right?... the pandas index object - and we get the - we get the column names there... cool! Pandas in Dask form. (Highlights a code cell containing `df.dtypes`) We can check out the data types as well as we would in Pandas we see we've got some *int*s for the day of the week, we've got some *float*s for departure time, - maybe we'd actually prefer that to be, you know, a date time at some point - we've got some objects which generally are the most general o-objects so generally strings... so that's all Pandas-y type stuff. In addition Dask dataframes have an attribute, `npartitions`  (highlights a code cell containing `df.npartitions`) which tells us the number of partitions and we saw before that that's 10, so i'd expect to see 10 here... (runs code cell) Hey, look at that.

Now this is something that we talk about a lot in the *delayed* notebook is really the task graph (highlights a code cell containing `df.visualize()`) - and i don't want to say too much about that - but really it's a visual schematic of - of the order in which different types of compute happen, okay? (runs code cell) ... and so the task graph for `read.csv` tells us what happens when we call compute and essentially it reads csv 10 ten times, zero indexed of course - because Python, reads csv ten different times into these ten different Pandas - Pandas dataframes and if there were `groupby`s or stuff after that we'd see them happen in - in the - in the graph there and we may see an example of this in a second. So once again (highlights a code cell containing `df.head()`) as with Pandas um we're going to view the the head of the dataframe, great, and we see a bunch of stuff... you know we - we see the first - first five rows. I'm actually (changes code in cell from `df.head()` to `df.tail()`) also gonna - gonna have a look at the - the tail, (re-runs code cell) the final five rows. That may take longer, because it's accessing the the final - I - I - there's a joke and it may not even be a joke, how much data analytics is actually biased by people looking at the first five rows before actually, you know interrogating the data more - more seriously. So how would all of our results look different if... if our files were ordered in - in a different way that's another conversation for - a more philosophical conversation - for another time.

### Computations with Dask DataFrames (<a href='https://youtu.be/MHAjCcBfT_A?t=2437'>40:37</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=2437">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t40.37.JPG"
       alt="Computations with Dask DataFrames" width="50%" /></a>

**Hugo:**

So now i want to show you some computations with Dask dataframes, okay? So since Dask dataframes implement a Pandas-like API, we can just write our familiar Pandas codes. So, I want to look at the column,(highlights a code ceell containing `max_delay`) departure delay and look at the maximum of that column; I'm going to call that `max_delay`. So you can see we're selecting the column and then applying the max method as we would (runs code cell) with Pandas. Oh what happened there? Gives us some Dask scalar series... and what's happened is we haven't called compute, right? So it hasn't actually done the compute yet. We're going to do compute but first we're going to visualize the task graph like we did here (highlights a previous code cell) and let's try to reason what the task graph would look like, right? So the task graph first is going to read in all of these things, and then it'll probably perform this selector on each of these different pandas data frames comprising the Dask dataframe, and then it will compute the max of each of those and then do a max on all those maxes, I think (runs current code cell) - that's what I would assume is happening here... great. So that's what we're - what we're doing we're reading this; so we read the first - perform the first *read-csv* get this Dask dataframe, *getitem* i think is that selection, then we're taking the *max* - we're doing the same for all of them, then we take all of these *max*s and aggregate them and then take the max of that, okay? So that - that's essentially what's happening when I call compute (highlights a code cell containing `%time max_delay.compute()`) which i'm going to do now (runs code cell). Moment of truth... okay! So that took around eight seconds and it tells us the max and I-I'm sorry? (Clicks on the Dask icon) Let's - let's just get out some of our dashboards up as well... (scrolls up the notebook)

**James:**

I think in this notebook we are using the single machine scheduler, Hugo. So i don't think there is a dashboard to be seen.

**Hugo:**

Exactly. Yeah thank you for that - that - that catch, James... great. It's even better. James, we have a question around using Dask for reinforcement learning. Can you - can you speak to that?

**James:**

Yeah so it depends on... this - I mean yeah, short answer yes you can use Dask to train reinforcement learning models. So there's a package that Hugo will talk about called Dask-ML that we'll see in the next notebook, for distributing machine learning, that parallelizes and and distributes some existing models using Dask. So for instance things like random forces - forest inside Scikit-Learn... so - so yes you can use Dask to do distributed training for models. I'm not actually sure if Dask-ML implements any reinforcement learning models in particular, but that is certainly something that - that can be done.

**Hugo:**

Yeah and I'll - I'll build on that by saying we are about to jump into machine learning... I don't think - as James said I don't think there's reinforcement learning, explicitly, that - that one can do, but you of course can use the Dask scheduler yourself to, you know, to distribute any reinforcement learning stuff you - you have as well... and that's actually another - another point to make, that maybe James can speak to a bit more. It's that the Dask team of course built all of these high-level collections and Dask arrays and Dask dataframes and were pleasantly surprised when you know, maybe even up to half the people using Dask came in all like, we love all that but we're going to use the scheduler for our own bespoke use cases, right?

**James:**

Yeah, exactly. Yeah... the original intention was to like make basically a numpy - like a parallel numpy, so that was like the Dask array stuff like run - run numpy in parallel on your laptop... and - and yeah. So in order to do that we ended up building a distributed scheduler which sort of does arbitrary Dask computations; so not just things like, you know, parallel numpy, but really whatever you'd like to throw at it and it turns out that ended up being really useful for people... and so yeah, now people use that sort of on their own, just using the distributed scheduler to do totally custom algorithms (Hugo opens the machine learning notebook at `localhost`) in parallel. In addition to these like nice collections, like you saw, Hugo presents the Dask dataframe API - is, you know, the same as the Pandas API... so there is this like familiar space you can use things, like the high-level collections, but you can also run whatever custom - like Hugo said, bespoke computations - you might have.

**Hugo:**

Exactly, and it's - it's been wonderful to see so many people - so many people do that and the first thing, as we'll see here, the first thing to think about is if - if you're doing lifestyle compute, if there's anything you can, you know, parallelize embarrassingly, as they say, right? So just - if you're doing a hyperparameter search, you just run some on one worker and some on the other, and there there's no interaction effect; so you don't need to worry about that as opposed to, if you're trying to do - you know, train on streaming data where you may require it all to happen on on on the same worker, okay? Yeah so even think about trying to compute the standard deviation of a - of a-a univariate data set, right? In - in that case um you can't just send - you can't just compute the standard deviation on two workers and then combine the result in some - some way; you need to do something slightly - slightly more nuanced and slightly - slightly clever - more clever, I mean you still can actually in - in that case, but you can't just do it as naively as that... but - so, now we're talking about parallel and distributed machine learning, we have 20 minutes left so this is kind of going to be a whirlwind tour, but... you know, whirlwinds when safe, exciting and informative. I just want to make clear, the material in this notebook is based on the open source content from Dask's tutorial repository as there's a bunch of stuff we've shown you today. The reason we've done that is because they did it so well, so i just want to give a shout out to all the Dask contributors, okay?

### Parallel and Distributed Machine Learning (<a href='https://youtu.be/MHAjCcBfT_A?t=2834'>47:14</a>)

<a href="https://youtu.be/MHAjCcBfT_A?t=2834">
  <img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t47.11.JPG"
       alt="Parallel and Distributed Machine Learning" width="50%" /></a>

**Hugo:**

So what we're going to do now is just break down machine learning scaling problems into two categories; just review a bit of Scikit-Learn in passing, solve a machine learning problem with single michelle - single Michelle? I don't know who she is but single michelle - wow. Single machine and parallelism with Scikit-Learn and Joblib then solve an l problem with - an ml problem with multiple machines and parallelism using Dask as well... and we won't have time to burst through the cloud - I don't think - but you can also play - play around with that, okay?

So as I mentioned before, when thinking about distributed compute, a lot of people do it when they have large data, they don't necessarily think about the large model limit and this schematic kind of speaks to that.

<img src="https://github.com/CeeThinwa/event-transcripts/blob/patch-1/images/v16/v16t48.24.JPG" alt="Scaling Problems Visualization" width="50%" />

If you've got a small model that fits in RAM, you don't need to think about distributed compute; if your data size - if your data is larger than your RAM, so your computer's RAM-bound, then you want to start going to a distributed setting or if your model is big and CPU-bound such as like large-scale hyper-parameter searches or like ensemble blended models of like machine learning algorithms... whatever it is and then of course we have the you know big data - big model limit where distributed computer desk is
incredibly handy as i'm sure
you could uh imagine okay and
that's really what i've what i've gone
through here
um a bird's-eye view of the strategies
we think about um
if it's in memory in the bottom left
quadrant just use scikit-learn or your
favorite ml library
um otherwise known as psychic learn um
for me anyway
um
i was going to make a note about xg
boost but i but i won't
um for large models
uh you can use joblib and your favorite
circuit learn estimator
for large data sets uh use our dark ml
estimators so we're gonna do a whirlwind
tour of psychic learn in
in five minutes we're going to load in
some data so we'll actually generate it
we'll import scikit-learn for our ml
algorithm create an estimator
and then check the accuracy of the model
okay so once again i'm actually going to
clear all outputs after restarting the
kernel
okay so this is a utility function of
psychic learn to create some data sets
so i'm going to make um
a classification data set with four
features and 10 000 samples and just
have a quick view
um of some of it um
so just a reminder on ml
um x is the samples matrix um the size
of x
is um the number of samples
uh in terms of rows number of features
as columns
um and then a feature or an attribute
is uh what we're trying to predict
essentially okay um so why um
is the predictor variable uh which we're
where
um which we're or the target variable
which we're trying to predict so let's
have a quick view
of why it's zeros and ones in in this
case
okay so um yep that's what i've said
here
why are the targets which are real
numbers for regression tasks or integers
for classification
or any other discrete sets of values um
no words about unsupervised learning at
the moment we're just going to support
we're going to
fit a support vector classifier for this
example
so let's just load the appropriate
scikit-learn
module we don't really need to discuss
what
support vector classifiers are at the
moment now this is one of the
very beautiful things about the
scikit-learn api
in terms of fitting the the model
we instantiate um a classifier and we
want to fit it
to the features with respect to the
target okay so the first argument is the
features second argument
is the target variable
so we've done that now i'm not going to
worry about inspecting the learn
features um i just want to see how
accurate it was okay and once we see how
accurate it was i'm not gonna do this
but then we can um make a prediction
right
using uh estimator dot predict on a new
a new data set
um so this estimator will tell us
so this score will tell us the accuracy
and essentially
that's the proportion or percentage
a fraction of um
the uh results that were that the
estimator got correct and we're doing
this on the training
data set we've just trained the model on
this so this is telling us
um the accuracy on the on the training
data set okay so it's 90
accurate on the training data set if you
dive into this a bit more you'll
recognize that
um if we we really want to know the
accuracy
on a holdout set or a test set
um and it should be probably a bit lower
because this is what we use to fit it
okay
but all that having been said i expect
um you know
if if this is all resonating with you it
means we can really move on to the
distributed stuff um um in in a second
um but the other thing that that's
important to note is that we've trained
it but
a lot of model a lot of estimators and
models have um hyper parameters that
affect the fit but you
that we need to specify up front um
instead of being learned during training
so
you know there's a c parameter here
there's a uh
are we using shrinking or not um so we
specify those
we didn't need to specify them because
there are default values but here we
specify them
okay and um
then we're going to um
look at the score now
okay this is amazing we've got 50
accuracy um
which is the worst score possible just
think about this if if you've got binary
classification task and you've got 40
accuracy then you just flip the labels
and that changes to 60 accuracy so it's
amazing that we've actually hit
50 accuracy we're to be congratulated on
that
um and what i want to note here is that
we have two sets of hyper parameters
we've used one's
created 90 actual model with 90 accuracy
another one one with 50 accuracy um
so we want to find the best hyper
parameters essentially and that's why
hyper parameter optimization
is is so important um there are several
ways to do hyper parameter optimization
one is called grid search uh cross
validation i won't talk about cross
validation
um it's essentially um a more robust
analogue of train test split where you
uh train on a subset of your data and
compute the accuracy on a test
on a holdout set or a test set um cross
validation is
a as i said a slightly more robust
analog of this
it's called grid search because we have
a grid of hyper parameters so
we have you know in this case we have a
hyper parameter c we have a hyper
parameter kernel
and we can imagine them in a in a grid
and we're performing
um we're checking out um the score
over all this gr over this entire grid
of hyper parameters okay
so to do that um i import grid search
csv
now i'm going to um
compute um the estimator over
over these train the estimator over over
this grid um
and as you see this is taking time now
okay
um and what i wanted to make clear and i
think should be becoming
clearer now is that if we have a large
hyper parameter
uh sweep we want to do on a small data
set das can be useful for that
okay because we can send some of the
parameters to
one worker some to another and they can
perform them um in parallel so that's
embarrassingly parallel because
you're you're doing the same work as you
would otherwise
um but sending it to a bunch of
different workers we saw that took 30
seconds which is in my realm of
comfort as a data scientist i'm happy to
wait 30 seconds
um if i had to wait much longer if this
grid was bigger
i'd start to get probably a bit
frustrated um
but we see that it computed um
it for c is equal to all combinations of
these
essentially okay um so that's really all
i wanted to say there um and then we can
see the best parameters
and the best score so the best score was
0.098 and it was c10 and the kernel um
rbf a radial basis function it doesn't
even matter what that is though
um for the purposes of this so we've got
10 minutes left we're going to
we're going to make it i can feel it i
have a good i have a good sense
um a good after the
i mean this demo is actually going
incredibly well given um the initial
technical hurdles so touchwood hugo um
okay so what we've done is we've really
segmented ml scaling problems into
two categories cpu bound and ram bound
um and i
i really i can't emphasize that enough
because i see so many people
like jumping in to use new cool
technologies um without
perhaps taking it being a bit mindful
and
intentional about it and reasoning about
when things are useful and and when not
um
i suppose the one point there is that
sure data science is a technical
discipline but there are a lot of other
aspects to it
um involving this type of reasoning
as well so we then carried out a typical
sklearn workflow for ml problems
um with small models and small data and
we reviewed hyper parameters and hyper
parameter
optimization um so in this section
um we'll see how job lib which is a set
of tools to provide lightweight
pipelining
um in python uh gives us parallelism on
our laptop and then we'll see how dark
ml can give us um awesome parallelism
uh on on clusters okay so essentially
um what i'm doing here is i'm doing
exactly the same as above
with a grid search but i'm using the
quark the keyword argument n
jobs which tells you how many tasks uh
to run in parallel
using the cause available on your local
workstation and specifying minus one
jobs
means the it just runs them the maximum
possible
okay so i'm going to execute that
great
so we should be done in a second feel
free to ask um any questions
in the chat oh alex
um has a great question in the q a does
das have
uh see a sequel and query optimizer
um i'm actually so excited that um
[Music]
and james maybe you can provide a couple
of links to this um
we're really excited to have seen dark
dust sql um
developments there uh recently um
so that's dark hyphen hyphen sql um
and we're actually we're working on some
some content and a blog post and maybe a
live live coding session
about that in in the near future um so
if anyone if you want updates from from
coyle feel free to go to our website and
sign up for our mailing list
and we'll let you know about all of this
type of stuff but the short answer is
yes alex and it's getting better and um
if james is able to post post a link
there that would be that would be
fantastic
um so we've done link in the chat
fantastic um
[Music]
and so we've we've seen how
we have um
[Music]
single machine parallelism here um using
the
um using the end jobs quark um and in
the final minutes
let's see multiple multi-machine
parallelism
with dusk okay um so
what i'm going to do is i'm going to
uh do my imports and create my
client incentive my client and check it
out
okay so once again i'm working locally
um i hit search and that'll
task is pretty smart in terms of like
knowing uh which which client i want to
check out
do the tasks stream
because it's my favorite i'll do the
cluster map otherwise known as the pew
pew map
um and then
i want some progress we all we all crave
progress don't we um
and
maybe my workers tab okay great so um
we've got that up and running now i'm
going to do a slightly uh
larger hyper parameter search okay um
so remember we had just a couple for c
a couple for kernel um we're going to do
more we have some for shrinking now i'm
actually
going to comment that out because i
don't know how long that's going to take
um if you're coding them on binder now
this may actually take
far far too long for you um but we'll
we'll see so i'll execute this code and
we should see
just sick no we shouldn't see any work
happening yet um
but what i'm doing here is
oh looks like okay my clusters back up
great
we're doing our grid search but we're
going to use um
dask as as the back end right and this
is a context manager where we're
asserting that um
and and we can just discuss the the
syntax there but it's not particularly
important currently i'm going to execute
this now
and
let's see
fantastic we'll see all this um data
transfer happening here we'll see our
tasks
um happening here we can see these big
batches of fit and score
fit um so fitting fitting the models
then finding um
how well they perform uh via this
k-fold cross validation
which is really cool
and
let's just yep we can see um
what's happening here we can see we
currently have 12 processing we've got
seven in memory and we have um
several more that we need to do uh our
desk workers we can see
us oh we can see our cpu usage
we can see how we can see cpu usage
across all the workers which is which is
pretty cool seeing that distribution
is uh is really nice whenever some form
of b swarm
plot if you have enough um would would
be useful there
or even um some form of cumulative
distribution function or something like
that
um not a histogram people okay um you
can go to my bayesian tutorial
um that i've taught here before to hear
me rave about um
the the horrors of histograms um
so we saw that talk a minute which is
great and we split it across
you know eight cores or whatever it is
and now we'll have a look
once again we get the same best
performer which is which is a sanity
check
um and that's pretty cool
i think um we have a we actually have a
few minutes left so i am gonna
just see if i can um
oh let me think
yeah i will see if i can burst burst to
the cloud and and
and do this um that will take uh a
minute
a minute or two to create the cluster
again um but while we're while we're
doing that i'm wondering if we have any
any questions um or if
anyone has any feedback on on this
workshop i very much welcome
welcome that um perhaps if there are any
final messages you'd
you'd like to say james while we're
spinning this up you can
you can let me know yeah sure i just
also first off wanted to say thanks
everyone for attending and like bearing
bearing with us uh with the technical
difficulties really appreciate that
um real quick i'm just yeah so if you
have if you have questions please post
in the q a section while the cold
cluster's spinning up uh
theodore posted in the last largest
example of grid search
how much performance gain did we get
from using das and not just in jobs
hmm that's a great question and we
actually
didn't see um let's see
so it took 80 seconds
ah let me get this they're actually not
comparable
um because i did the grid search over
a different set of hyper parameters i
did it over a larger set of hyper
parameters
um right so when i did um
end jobs i did it there were only um it
was a two by two grid of hyper
parameters
whereas when i did it um with with dusk
it was a
one two three four five six six by three
so let's just reason about that um this
one was
eighteen six by three is eighteen which
took eighty seconds
um and this one was two by two
uh so it was four and it took
26 seconds um
so a minor gain i think with this hyper
parameter
search if you multiply that by by four
you'll
well 4.2 4.5 you'll need that would have
taken maybe two minutes or something
something like that so we saw some
increase in efficiency
not a great deal but um james maybe you
can say more to this
part of the reason for that is that
we're doing it on kind of a very small
example so we won't necessarily see the
gains in efficiency
with a data set this size and with um a
small hyper parameter suite like this is
that right
yeah yeah and um yeah exactly and i
guess also this is more of an uh kind of
an illustrative point here
i guess uh so you're just using uh
directly using in jobs with
something like job lib um by default
we'll use local threads and processes
on like whatever machine you happen to
be running on so
like in this case on hugo's laptop um
one of the real advantages of using
uh job lib with the das back in will
actually dispatch
back to um to run tasks on a dash
cluster is that your cluster can
expand beyond what local resources you
have
so you can run um you know you can
basically scale out like for instance
using the coil cluster
uh to have many many cpus and
a large amount of ram that you wouldn't
have on your locally uh table to run and
there you'll see
both large performance gains as well as
you'll be able to expand
your the set of possible problems you
can solve uh
to larger than ram uh scenarios so
you're out of out of core training
exactly and thank you jack this was
absolutely unplanned and we didn't plan
that question but that's a wonderful
segue into
me now performing exactly the same
compute with the same code
using uh the dasc as the parallel back
end um on a
on a coiled cluster which is an aws
cluster right
um so we can i'm more currently anyway
so i will execute
this code um and it's exactly the same
as we did
um whoa
okay great um so
we see our tasks task stream here
um
you see once again we see the majority
is being batch
um uh fit and and getting the scores out
um
similarly we see the same result being
the best
i'll just notice that for this for this
small task doing it on the cloud took 20
seconds
uh doing it locally for me took um 80
seconds so that's a four-fold increase
in performance
on a very small task so imagine what
that does if you can
take the same code as you've written
here and burst to the cloud
uh with with one click or however
however you do it um
i think that that's incredibly powerful
and that the fact that your code
and what's happening in the back end
with dusk um generalizes immediately to
the new setting of working on a cluster
i personally find very exciting and if
you work with larger data sets or
building larger models or big hyper
parameter sweeps i'm pretty sure
um it's an exciting option for all of
you also um
so on that note um i'd like to reiterate
james what james said and thanking you
all so much
for joining us um for asking great
questions
and for bearing with us through some
some technical technical hurdles
but it made it even even funner when
when we got up and running uh once again
i'd love to thank
mark christina and and the rest of the
organizers for doing such a wonderful
job
um and doing such a great service to uh
the data science and machine learning
community and ecosystem worldwide so
thank you once again for having us
thank you hugo and james um i have to
say like with all the technical
difficulties i was actually giggling
because it was kind of funny um
yeah but we're very sorry and we thank
you for your patience
and sticking through it and um
i will um be editing this video
to um you know make it as efficient as
possible
and have that available tim supercard
thank you um great and i'll just ask you
if you are interested in checking out
coiled go to our website if you want to
check out our product
go to cloud.coil.io we started building
this company in february
um we're really excited about building a
new product um so if you're interested
reach out we'd love to chat with you
about what we're doing and what we're up
to
um and it's wonderful to be in the same
community as you all so thanks

