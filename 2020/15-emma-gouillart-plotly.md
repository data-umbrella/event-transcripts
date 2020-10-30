# Emily Gouillart:  Data Visualization with Plotly

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/15-emma-gouillart-plotly.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/272683860/
- Video:  https://youtu.be/BxIoQ0gsxzA
- Jupyter notebook:  [plotly-code](../resources/plotly-presentation.ipynb)
- GitHub repo:  not applicable
- Transcriber:  ? [needs a transcriber]

## Transcript

welcome to data umbrella
um i'm going to just go over the agenda
of how the webinar is going to go i'm
going to do a brief introduction
emmanuelle um will do her presentation
on plotly
and you can ask questions on the q a tab
and so we'll sort of check questions
when it's a good time to stop
um but not to worry your questions will
get answered some of them might be at
the end but we will answer all questions
and this webinar is being recorded
a little bit about myself i'm a
statistician data scientist i'm the
founder of data umbrella and i'm also an
organizer for the new york city chapter
of pi ladies
you can find me on twitter github and
linkedin
as reishmas
data umbrella is our mission
is to provide inclusive and welcoming
space for underrepresented persons in
data science
machine learning and ai and we are an
all volunteer run organization
pi ladies is an international group
there
are over 125 active chapters around the
world
and it's for women and gender minorities
of all levels of programming
um and this is our website yeah you can
also
um you know go to our website and we
have links to
all of our linkedin and slack and more
information
i want to cover the code of conduct
briefly we're very strict with our code
of conduct we're dedicated to providing
harassment free experience for everyone
we ask that you make this a professional
and respectful environment
and this applies to the chat as well and
um
it's been a great experience so far and
thank you everyone in the community for
uh keeping it up
i want to share a new feature of data
umbrella which is a job board
the url is jobs.dataumbrella.org
i'll also in in just a couple of minutes
i'll put it in the chat um but you can
check it out
to see what jobs are posted and you can
also there's a weekly digest that you
can subscribe to
if you are um in the job market
we have the highlighted job of the week
which is farfetch farfetch is a
um i know they do work with fashion uh
you can read more about the um
job on our website and they're new york
city based and they're looking for a
lead data scientist
on our website which is dataumbrella.org
there are a number of resources there
there are resources
for accessibility and inclusivity there
are resources for open source
about social impact of policy about
scikit-learn
so um you know on your when you have
some time uh check out the website um
there's a lot of
helpful information there
for data umbrella the best place to find
out about
upcoming events is meetup.com nyc data
umbrella
uh the website has resources we're on
twitter feel free to tweet about it
and pretty much we're on all social
media platforms
data umbrella
and now i am going to hand it off to
emmanuel
um and uh just that you know if we could
if we could clap emanuel is joining all
the way from france
paris and i started in particular
contributing to psychic image which is a
python
image processing toolkit since i was
using it for my research
and one year and a half ago i decided to
contribute
more to open source and this is why i
joined blockley
full time and during this time at
plotley i've been lucky to receive a
grant
from the chance working bag initiative
which is a foundation
which has funded a project
uh bloodly to work on interactive image
processing i talk about it
at the end of the presentation
so the subject of my talk is a bloody
graphing library so
uh what is plot g maybe um
most of you know about it and i'll try
to share
a little just so that you can vote for
your preferred
visualization tool you don't have to say
it's bloodline it's just interesting for
me to
see which tool people are using so i
just put
solutions well just put answers in
writing
because this is the language i know the
most
uh but so plotly is an interactive
web native visualization library and
since it is developed for visualization
in the browser
it is written in javascript but it also
has
apis for languages more familiar to data
scientists
so python are and more recently
julia as well
the the python flavor of
plotly also has a high level
expressive api which is called bloody
express
and which is particularly suitable for
working with spender's data
frames like seabourn for mad bloodly
and for python plottings in fact
the most downloaded visualization
library
uh which is interactive that is uh
web-based and
very interactive matplotlib is more than
loaded but then it's not
as interactive and it's not based
plotly is open source it's mighty
licensed and during this presentation
we'll see that it has a large variety of
traces and is very customizable
and it has a strong focus on
interactivity
in the sense that charts figures are
very
interactive but also they send events
which can be listened to by
other libraries for even more
interactivity
so in order to illustrate the
capabilities of properly
i'll focus here on three different use
cases
of bloody during this talk first of all
we'll see how to explore data
by visualizing them which is something
you can do
in a jupiter notebook for example then
i'll switch to a slightly more advanced
use case where you want your
visualizations to interact with other
elements
or to publish them as a dashboard
and finally i'll combine the two first
aspects
to show tools we've been developing
recently for
interactive image annotation and
processing
so let me start with the first
use case which is interactive
exploration of
data and for this we'll work
in a notebook
so i guess most of you are familiar with
a jupyter notebook
so it's a development environment
which mixes code cells and the outputs
um so i'll be using it
uh during this presentation i hope the
the fonts are big enough i can increase
them a bit
so um plotly is open source you can
paper install it
and so we'll start by importing it
and in particular we'll import
a set package called graph objects for
it's like a collection of graphical
objects and it's
commonly imported as go
and the first object we'll be creating
is called a figure so when
we execute this in a notebook
we get a figure but then it's an empty
figure so not very interesting
but so we'll populate this figure object
in an object-oriented manner by
adding first a trace
which will be a scatter trace
with x and y coordinates
[Music]
okay and we'll
show it so here
the first race and we'll add
more elements by adding for example
a bar plot
so a second trace
[Music]
and let's say we don't
so traces are data points which you
are visualizing in some specific ways
and
um here we also want to add more
elements in particular
let's say we want to add a title so a
title
is a part of what's called the layout in
a
closely figure and
so we call the update layout method
my first figure this will be my text
okay so here is our first
figure object but what it is uh what is
it exactly
to know what is this figure object
we'll just print it
to show its structure
calling its representation
so we see that this figure object
contains an object which looks like a
dictionary
a dictionary with two keys one of them
is the data
which is a list of traces and the other
one is a layout
and so each trace or the layout is
itself a dictionary
which is a dictionary of dictionaries so
it has a nested
hierarchy structure with the different
properties and attributes of the visual
elements
and this object is in fact passed
to the javascript library as a json
string since it has this json-like
hierarchy so it's in fact a very
simple object which is just past as it
is to
uh the javascript part of
the library and once you have understood
this nested hierarchical structure
then you can modify it
like for example if
i want my
first trace which is the scatter trace
i want to modify its x coordinate
not 0 1 2 but 1 2 3.
i can modify it this way you see it has
shifted the x data points or i can also
modify
my title
[Music]
uh like
this equals 30.
okay but um so instead of
writing all those dots it's actually
nicer to call this high level
methods of the figure objects which
are archways or update traces
update layout and
also instead of writing all these dots
you see here this underscore
which is exactly uh the same
as uh putting a dot here so if i want to
modify the title font size
here i can write it like
this so using this underscores called
magic
underscores a way to navigate down
the hierarchy of attributes of the the
plotly figure
there you go okay so this was for
a crash course introduction to the
structure of bloody figures
you can create figures in this
informative way where you define the
traces you modify the layout
and you create a figure but sometimes
it's
much nicer to uh use a high level
api and this is uh what the bloody
express
um package does so now
i'll introduce bloody express
you usually import it as px
and uh so it's probably express
why express it's uh in order to create
a function figures
fast but also uh to
also to create figures in an
expressive way so it's both fast and
expressive
and so px comes with a set
of built-in data sets so we'll use one
of them which is called the gapminder
[Music]
so what it is it's it's a painless data
frame
where each line is a pair of
country in year
and there are other columns
for values such as the life expectancy
or the population
of the country for this year so to to
start with
we'll limit our data sets to
the most recent year here using some
typical pandas syntax with a query
and we'll start by asking ourselves
what is the distribution of life
expectancies through
the countries of the world so we'll call
the plotly express or px that
a histogram function in order to
plot a histogram so the syntax is
you have the data frame and then you
give the variable
on which you want you to plot the
distribution so
here i'm interested in the distribution
of
life expectancy there you go
so you've got
this figure which is
[Music]
quite interactive you can see in
particular that
i can see for each binder the count
corresponding to the number of countries
with life expectancy
in a given bin what's interesting is
that you can see that
this histogram is quite bi-modal it's
not just one peak
um you can see that uh a few countries
have a very
low life expectancy all those very high
so
can we know more about which countries
are in which to pin for this we
can add more visual elements but
first i'd like to show you that
this figure created by
the plotliexpress core the plot express
function
is not very different from
uh the figures we've been using uh in
the examples just before with graphical
object so we'll
print the figure and you can see
that so it's still a figure object with
a data key corresponding here to one
trace
this trace is a histogram so it's a
graphical object
trace it has some x data and also it has
a layout
which is populated with
some values in particular the
the the title of uh the
the access is already
[Music]
specified you don't have to to give it
yourself so
bloody express is here a fast way
to to produce a figure which is not
completely
camera ready but uh has already a lot of
useful elements
but it's exactly the same structure as a
plotline figure created with graph
objects
and so i was saying what if we want to
know more about which countries are in
each bin
then we can add facets
for a marginal view of the countries
so we add this rock plot
where each of these small bars
correspond to one country
um but we don't know
the name of the countries so we'll map
the name the country column of the data
set to
the hover name so that it appears in the
hover
[Music]
what uh i'm i'm doing here is
mapping columns of my data set to visual
elements and i can go further
in this direction by adding
a different color for
different continents
color equals continent
[Music]
so here you've got this different
stacked
histograms each one of them corresponds
to a different continent
one interesting things also is this
legend which is
interactive like if i want to select
only
um asian country
oops i should
double click on it or
i can select or
remove one of these continents so the
the legend
is uh quite quite useful
um so this was for a histogram but
in this histogram each
country has the same weight whereas we
know that some countries are
much more populated than others so if
you want
a different view what we can do is
instead to plot
a bar plot with
this time
[Music]
the x corresponding to the
the continent and the y to
the population and you get
this bar plot and um
where the height of each
bar corresponds to to the population and
this time
since i've got a different x location
for
each continent i can save the color for
a different
colon of my data set which is life
expectancy
so that it will be
color coded color coding the life
expectancy and you get this nice
hues for the life expectancy with a
color bar here
so this
chart is interesting but what if
i want to be able to select one
continent
and to do some drill down
in my data set for this i can
switch from a bar plot to a more
hierarchical plot
and i will show you this by just
looking through the plotly documentation
just to
show you an example of uh how to look
for stuff
in the plotley documentation so this is
the main plotly documentation
and let's say you're looking for a
hierarchical
plot so you see that on the left column
you have the documentation results
for different tutorials and here is a
figure reference result so it's more the
api
so you see that the first results are
treemap
and some burst charts so which are the
two kinds of hierarchical
traces which we have in bloodley so if
you go to one of these pages
you have actually quite a large number
of
examples for each chart you you can see
that there is a property express
sunburst
function that its arguments are pass
for the hierarchy of levels values
is what you want to represent the
equivalent of the y in the bar chart
uh you have more examples with scholars
and
and so on and so forth so we try to have
quite a thorough documentation for
plotly
and it's also an area where we get a lot
of help from the community of users with
a lot of
community pro requests about improving
the documentation which is absolutely
great
and i hope we continue to have a lot of
great contributions
from the community in the future but so
if i go back to
my code cell here if i want to
plot a sunburst here instead
i have to use a bus with continent
and then country
[Music]
and my values will be
the population and color
life expectancy so i get this
um circular diagram where i can drill
down
in one country and you can see
that in more details
the different countries of africa and
you can go back one level up
by double clicking exploring uh
another continent so this is a
small example of the entire activity
which you
you get with bloody and by the way the
sunburst and tree map charts are
even more useful when you have a large
number of levels like uh
three or four rather than two
um so this was
for a short introduction
uh to the plotly visualization library
um one little thing which i can
also show is um
how to yeah how to
map different columns uh to
um not
a two to facets that is
two different subplots this is something
which is very
very useful so i could do
like a live
[Music]
equals continent
[Music]
it's why
okay so in this visualization
i get one
one facet per continent
and i could also make different colors
um for
just two
[Music]
yeah this is better so it's uh also a
way to map
the values of your columns this time to
a
different subplots and this is a very
powerful way
of creating subplots and populating them
because if you had to
write all this yourself it's actually a
bit more verbose you would have to loop
through the different uh facets you can
do it of course
it's easy to write loose with python but
uh
this high-level way of making
multi-faceted
plots is quite nice
so this
was for the short not so short maybe
introduction to
uh plotline and if you want to learn
more
i recommend going to the documentation
website which has several tutorials
covering what i've been describing
and in particular how to create
figures their structure plotly express
and you can also
see in the documentation that there is a
very large number of charts
of course uh usual basic charts like pie
charts bar charts but also statistical
charts
uh heat maps geographical charts 3d
visualization is also quite interesting
so check it out if you're interested
so very nice flats a lot of different
traces
but what if you want to have more
interaction than just
user interaction in one figure for
example if you want
to have two figures which interact
together
so um this is something
which you can do with uh plotline
because
plotting figures in fact emit some
events
which can be captured by other
javascript tools
and in particular you can
capture these events using dash so i
spent just a few minutes
explaining what is dash which is another
open source library developed by plotly
also mighty license
so dash is a web framework to write
what we call analytical apps in python
we'll see examples of analytical apps
which are basically dashboards for
science and data science it's a
user interface toolkit so written in
javascript but
with a python api so that you can write
your java
your dashboards uh in pure python with
no javascript required this is really
the promise of dash
it has a large variety of interactive
components
and so we will see
uh first a few examples just to
introduce dash and then we'll see how
plot integrates with dash
so we've got this first hello world
uh script for dash
uh where you import some dash modules
and then you create
your first dash app and you declare
the layout of the app with several
elements
so one of them is an html title and the
other one
is taken from this dashboard com
components library dcc which is for
elements to be modified by the user and
here it's a text input
so what happens if
i execute this writing script
we'll go back to the notebook just in a
few minutes but just
i show you the vanilla classical way of
defining uh of dash apps
so when you run the app uh under the
hood there's a flask server running
and you can go to a url
where you have created your web page
with this
title you defined in layout and also a
text input
so far so good but we don't have
interaction
in this app so for interaction
we need to add what's called a callback
uh so a callback is a
this function decorated here
which links together
two components the here
it takes as input the the text input
when it's changed the callback will be
triggered and as output
uh the content of my title
so what if i run this time
this new app
this will this should reload my
app and now when i write hello
every time i type a keystroke
then
the values are sent to the python server
the
callback is executed and the new value
for the title is sent back to the
javascript layer
in my browser and if you want to take a
look
at the graph of callbacks in my
uh in my dash app
you can see that here there is one
callback
linking together the input
and the title components
okay so how can we
integrate this with platygraphs
so for this
i first show you an example
of what is it
it's here which is an example from the
dash gallery so in this dcc
dash core components package you have
a component called dcc.graph
which is a wrapper around the plotly
figure
and for example this is here a bloody
figure you can see here it's modbar
it's a different kind of trace which is
here a cover plate so it's one of this
geographical
uh map and so when
you change the sliders this will
modify your map because
there's a callback taking as input as a
slider
and as outputs a bloody figure the
callback creates a new plot refigure
and sends it to the browser
however uh this is only one way of
interacting and the other way works as
well
like if i make a selection like this
lasting selection here
in my figure this will
send a specific event called a selected
event
in to a callback listening to this kind
of event
and this will modify a histogram here
so the plotline figure can be interacted
with
really both ways in a dash app you can
modify it with a callback but it can
also trigger events
and callbacks and if you want to know
more about the kind of events
which you can listen to i encourage you
to take a look at
the the interactive visualizations
tutorial of the
dash documentation where you have
this app with one callback
for every kind of event so
hover over data which is the events
triggered when you hover
click data when you click selected data
and so on and so forth and the layout
data is when you change
one element of the layout so for example
here if i
zoom i will trigger
a layout data event changing the
range of the two axis or if i
click i trigger
also a click data event so this is how
you can
connect bloody figures to other parts of
a dash app
so this was for
a very short demonstration
demo of how you can
use your plotter figures in an
interactive way with other elements
in an app like a dash app and in the
last part
of my talk i'll show you how
to combine platy express with
the with dash for
image processing so image processing is
uh what's the topic which uh
maybe interests me the most in data
science
in uh in scientific writing it's
the task of processing your image data
in order to extract information from
them it's something which is done
in a very large variety of domains
in science like in biology where you
want to count cells and measure
the properties satellite imaging
it will be very useful also in
a self-driving cars
or in image classification like in
google images for example
and um last year i i've been working
on this project funded by sensody
in order to develop more tools for
interactive image processing
using several mainstream tools
from scientific python the first one
is psychic image which is
the image processing toolkit for python
so i'm a maintainer also
psyched image which is a collection of
image processing algorithms with a
functional api you call functions on
images
and the idea of this project is to
combine the algorithms
of site image with the capabilities of
plotting dash
to use plotly in order to visualize
image data
in a dash to trigger to trigger
callbacks when you annotate images
within plotline dash to call
some algorithms from psychic image like
if you
draw a rough contour like here of
this organ you want a psychic image to
segment
in a very good way uh it's exact contour
so the idea is to have
uh powerful tools to build interactive
image passing apps
so how how have we been doing this
uh let me go back to my notebook
a first step has been to
extend the bloody express api
so that it had
image visualization capabilities because
we used to have limited capabilities
for image visualization so i'll
start by just importing an image data
set
from plotly from psychic image so
sorry by calling
one of the built-in image data sets
which is the cat and
[Music]
there is one trace
which is called image trace
and which is meant to represent images
[Music]
i forgot to import plotly that's a demo
effect
[Music]
so there you go you've got this
image visualization here in this figure
where you've got
some information in the hover in
particular the the value of each pixel
is represented as z
here this is quite useful
and so that's a low level
uh go api but we've
also introduced
the corresponding property express
function
and we've got a px dot in show
[Music]
function
[Music]
and um
[Music]
which is calling um an image trace
under the hood so this the first step of
the
project was to uh implement
this interactive image
visualization function where you can
zoom
you can select some parts and
now we can build our first
image processing dash app for this i'll
reuse some code
so that you don't have to see me
copy pasting so
let's say i want to
[Music]
visualize
the histogram of some parts in
my image and i want the user to select
interactively uh some interesting parts
um so for for this since we are in the
notebook
i'd be using um a recent
let me let me use a new notebook
we'll be using a new package called
jupiter dash
[Music]
which we've been
um releasing
and oh i forgot to kill
my
my old app so i need to um
use in a new port so
[Music]
so jupiter dash is a way to
display your uh well to
to write and visualize your dash apps in
the notebook so it's very convenient
if you're used to working in the
notebook because you can start just
creating your bloody figures in the
notebook
and then adding some interactivity with
the jupiter dash app
so here i've got two figures
one of them is my image here and the
other one
is a histogram and i want to be able to
make a selection
and to see what happens
what is the histogram of my
my
my selected vision and so
when you do this usually what i start
doing is that
i i listen to the selected data event
and i look
at uh the structure of
this this events and i see
that it looks like this so i know the
syntax
of um what i should be calling i use
print
quite a lot in the dash apps and so
this will be like my next
uh
[Music]
my next callback let me update it
i see that i'm running out of time so i
will try to be fast
and just updating this
[Music]
so this time when i select
a small region then the
the graph is updated
and if i select like the nose for
example
it's very red so i can explore some
parts
of my my image like this
the white part is very bright and so on
and so forth
but um so with selection i can
have some interactivity but selections
are quite short-lived
and we wanted to have something which uh
was more persistent in user annotations
which you could
use for a longer time in the plotlife
and this is why we introduced
shapes shapes uh so
shapes which you can draw shapes have
been parts of the plotline layout for
a long time so a shape for example is
this rectangle
and um in the most recent versions of
broadly
you can draw shapes yourself like for
example you can draw
a rectangle you can draw a circle
and each time you do this this triggers
a layout event
you can also modify them just by
clicking
modifying some of them and you can
listen to the corresponding we layout
data events
uh in your your dash apps so
i just stopped the presentation by
showing you a small example of a more
advanced
dash app we've been writing using this
annotation
so this shape annotations we've got
one figure here which would like to
segment
that is to separate the different parts
of the image
in different classes and here when
i'm selecting the different colors a
callback is updating the
new shape properties of my platfigure so
that
the the color is changed i will do this
i can also modify it switch which is
another property
of this new shapes and and so on
and
so i have all my shapes which are
persistent more than selections
and then when i click on this show
segmentation
a callback uses cyclone
to compute well cyclotron and features
corresponding on local neighborhoods
to compute labels for the remaining
pixels
so this is an example combining
these plotly annotations
uh in an interactive figure where you
can also
zoom for example you can fan and
look at the details and also the power
of scientific writing libraries like
psychic image for image processing or
psychic learn for machine learning
um so i'm running a bit out of time so
conclude here by
just hoping that this presentation was
interesting for you
i hope there will be questions in the
chat i
hope you will be in touch either on
twitter or
also we have this discourse community
forum where
a lot of questions about flatly and dash
are asked
and answered too so
thank you very much and i hope we'll now
have a nice
q a session thank you
so let me go back to the chat
okay so i guess it's it's your time to
work and to ask questions in the chat
so the next question is uh is
image processing the same as neural
networks or a different process
so neural networks
are a possible tools for image
processing because
image processing is this
generic class of tasks where you want to
extract
information from images
and there are several ways of doing that
uh
you can either do somewhere
operations on uh pixel values
which is a more traditional way of doing
image processing
or you can build a neural net
to perform some image processing tasks
by uh
learning some structure out of your
images or you can also use
uh more traditional tools uh for machine
learning
like uh the the app i showed at the end
was you using a random forest classifier
for example so this is not a neural net
but this is still using machine learning
so i'd say
neural net is one of the possible tools
for image posting
and nowadays it's also the state of the
art
for a lot of image processing
tasks like image
classification or segmentation or some
objects
next question um
how is the app recognizing the classes
after
you indicate the classes this is some
kind of cnn or
other machine learning algorithm so
i went very quickly on this app because
i was running out of time so
um let me go back to the app so here
um for each pixel um
we call a circuit image function co
computing
a vector features for each pixel so
features are based on the local
intensity the local standard deviation
and texture
in different neighborhoods with
different signals
so we've got this uh vector features for
each pixel
and after we call uh random forest
classifier
uh from cyclic learn so it starts using
cnn but
the features are defined um
in um in a more specific way but of
course it would be also possible
to use a pre-trained uh neural nets here
uh which could give
very good results maybe even better
that's actually some extension i've
been wanting to to do to this ab it's to
try it out with uh
with the neural net
um
does the next question is does bloodley
dash work well with 3d volumetric images
both for visualization and image
analysis
so plotline has
a variety of traces
for 3d visualization i can
show here
the section of the documentation on the
uh 3d uh plots
like is it has a surface plots
uh which
it has uh 3d scatter plots and and so on
and so forth
uh the performance of these traces
depends uh on the size of your data sets
like if for example you want to compute
a nicer surface of
several millions of points
it can take quite a lot of time and it
can even freeze your browser
so um usually you want to limit
uh the number of data points uh which
you
you feed the browser since the browsers
are not very good
with very large
objects but for
medium sized data sets
you've got all this nice traces
which you can use so for
image processing in 3d in particular you
can use
slices or maybe i can
show this up dash
playground it's a
recent app which we've been writing so
it's not using here
a 3d uh trace but
it's using uh just slices through
a 3d volume so
it's a it's an mri data set here
so this is just a broadly image where
here i'm navigating through the the
different slices
and so here in in this interactive
dash app we want to segment here
a lesion which is
a part of the brain where there was a
problem
and so the segmentation is done so
you can see that this slicing and dicing
through the volume works quite well so
this is something
you can do with splatling and you also
have a
3d view here of the brain
where you you have here the the lesion
which has been segmented
in 3d and the contour of the brain
so this is a typical example of what
you've been doing in 3d
with splatly so that was for the vince
and as for the image analysis so
plotli does not include image processing
algorithms but
uh if you're calling uh its python api
then you can use uh other packages such
as
psycat image uh for example so
that uh you can write callbacks which
are just a few lines uh calling uh
second image
functions and this is what we've been
doing in this since that
project if you're interested i forgot to
mention that
we've got a blog
which is uh you can see it from
my twitter i've tweeted a few blog posts
with some examples uh describing how to
use
plotly dash and circuit image together
for uh image processing and one of the
next posts will be
on the 3d visualization in image
processing um
so i think i went through the whole list
of questions
uh i don't know if we still have time
for
one or two questions
it's also possible of course to reach
out after the webinar
but the nice thing here is that other
people can see the questions and hear
the answers
oh we can take a look also at the at the
results of the poll
uh but there is uh one more question
uh oh which is basically a story of my
life
could you share your career trajectory
from your phd in physics to working on
open source development full time
so during this year's
in research i've been doing
experiments where my main source of
scientific data was images
and i needed to extract
some numbers some scientific data from
this large sets of images which i was
acquiring at the
synchrotrons and
so and for for this
this is how i started contributing to
psychic image because
when i started doing image phosing a
second image was actually just
starting and
i i got more and more involved because
uh
well first of all the scientific writing
is community is a
very nice one very welcoming and i felt
very welcomed so i wanted to to spend
more time
in this community and also i
realized the importance of having open
source tools
uh available to a large community
because this was something
i was directly using for my my research
work so
i i tried to spend some time on open
source development but as a hobby
and at some point i thought
hey why don't you try to turn this hobby
into a job
and this is how i joined plotley which
is
this open core company uh
developing nice open source
tools used by very large number of users
with also a commercial offering
but i've been working on the the open
source tools
and so at the end of uh
this grant i'm going back to to research
but
uh it's been really great navigating uh
between research and software because uh
um so for the research the software
tools
are just essential you you need them to
do your science
but also when you're developing uh
software it's very useful to have ids
about
what users can do and having my
background in research having also
collaborations and contacts
students doing research has been very
useful
when developing software because it
helps developing the right tools
something which you think will be really
used
so um i would encourage really
people in research trying to spend more
time
developing open source software but also
people developing software also
trying to be in the shoes of their users
and also to
to work on applications so basically
doing more
multidisciplinary work so thank you for
for this question
and for all the questions thank you
thank you so much emma um i think that
is the most successful live
coding demo i have seen
which is really great because you never
know how these things
well yeah only a few bucks
it was really great um thank you so much
um
and for our um you know for people who
are joining i'm gonna you know
sort of um put a video up within the
next few days
and for sharing the notebook it won't be
today because it's midnight in paris so
bear with me
in wait until tomorrow please
yeah we'll definitely get that
information out i'll probably add it as
a link
to the youtube video just so it's
readily available for whoever watches
versus an email or something so yeah i
think that'll be great
thank you very much to everybody it's
been really fun
uh giving this presentation and
especially answering the question saying
thanks for having a lot of questions and
if you have more please reach out and on
twitter
or on the plotline community forum so
see you there
thanks a lot


