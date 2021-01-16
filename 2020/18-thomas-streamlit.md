# Thomas Fan: Streamlit for Data Science

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/18-thomas-streamlit.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/274110563/
- Video:   https://youtu.be/5TCdoWemSXI  
- GitHub repo:  https://github.com/thomasjpfan/data-umbrella-2020-streamlit-ml
- Slides:  N/A
- Transcriber:  ? [needs a transcriber]


## Video

<a href="http://www.youtube.com/watch?feature=player_embedded&v=5TCdoWemSXI" target="_blank"><img src="http://   .jpg" 
alt="Thomas Fan: Using Streamlit for Data Science" width="50%" /></a>

## Transcript

hello everyone and welcome to data
umbrella's webinar
i'm going to do a brief presentation um
i'm going to do a quick introduction um
the talk is going to be there and we are
going to have a q a at the end this talk
is being recorded if you have any
questions there's a q a tab on this
platform so if you could post questions
there that's a good place to aggregate
them
if you happen to place them in the chat
i can also easily you know transfer them
over to
q a but it is easier if you post them in
the q a tab
this webinar is being recorded a little
bit about me briefly i'm a statistician
data scientist i'm a founder
i am the founder of data umbrella and i
am on twitter linkedin and github as
reishima
so feel free to follow me um if you
would like
we have a code of conduct uh we're quite
strict with our code of conduct because
one of the reasons that this community
was created is to provide
a safe and inclusive environment for
people from underrepresented groups
we take our code of conduct very
seriously in fact
at our last session somebody posted
something quite inappropriate in the
chat
and um they're you know they're no
longer um
part of the group so please um please
you know really take this seriously
and you know this may not be for
everybody but this is sort of
the agreements that we have as a
community um
to make it professional and inclusive
and welcoming for people
we are also a volunteer-run organization
there are numerous ways that you can
support data umbrella the first and
foremost one is to follow
our code of conduct and contribute to
making it welcoming collaborative and
professional
the second is we have a discord
community chat it's on our website so
feel free to join there and
ask and answer questions there we have
an open collective
of for data umbrella so if you would
like to donate to
support us uh to pay our meet up dues
and other expenses that would be great
and we have uh an initiative an open
source initiative for editing
transcripts for these webinars
to make them accessible
this is the github url for that
and feel free to check it out and email
us and ask any questions
we have we have a bunch of people that
are working on transcripts
as well we have a job board as well
which is jobs.org so if you are in the
market looking for a job feel free to
check it out and also there's an option
to subscribe to a weekly digest
our website has a plethora of resources
on accessibility
diversity responsibility ally ship
please check it out at your convenience
we also have a newsletter which goes out
once a month it's
you can find it at
dataumbrella.stopstack.com
we promise not to spam you we only send
the newsletter out once a month
so it's a it's another way to get
information about
our group we are on all social media
platforms as data umbrella
meetup is the best place to find out
about upcoming events
our website has resources we have
twitter linkedin
and youtube if you want to subscribe to
youtube we record
all of our webinars and um post them on
youtube so that's a good place to check
out our previous webinars
this webinar and upcoming ones
so in december we have two events
contributing to numpy and
contributing to pandas they have not yet
been posted on meetup but they will be
soon and the best way as i said before
join our meetup group to receive updates
today's speaker is thomas fan who is a
core developer of scikit-learn
he is also a staff associate at the data
science institute at columbia university
and thomas maintains scorch which is a
scikit-learn compatible
neural network library that wraps around
pie charts
um i also want to say that you know
thomas
is um with the meetup group there's a
new york python meetup group in fact
that's where thomas introduced
me and others to streamline and i
reached out and asked him well this is
really great would you present for us
and he said yes
so thank you um and with that
i will keep my fingers crossed and hope
that
can share his screen and um
get started thank you i'm gonna press
this button
and see what happens
wow all right hi everyone good rasheen
reishima can you see the slides
yes i can i just turned up mike but yes
okay good
all right welcome everyone today i want
to talk to you about
streamlets using streamlight for data
science
most of this is going to be
a demo of many demos and i'm going to
showcase how
one could use streamlets to make
dashboards
so what is streamlit um streamlets
the way i see streamla is that it's a it
makes it so that you could quickly
create dashboards or applications
while staying in python so the workflow
looks kind of
something like this where you have code
on one side and then you have something
that
auto updates when you
save your code on the left so this is
i'm going to showcase how this works in
in this talk
um so most of this talk is demo so i'm
gonna
provide three demos um they get
progressively more
um advanced um the first one will be
something
uh it will showcase uh streamlight as a
library and how it interacts with pac um
plotting libraries
and then i'm gonna get into some data
science i'm gonna
train a model on the data set that we
looked at from the first demo
and then we're gonna train a model in
jupiter notebook in my case jupiter lab
and at the end i'm gonna build a
dashboard that explains that does local
explanations
for the predictions of the model i've
trained in step two
in streamlit so as a like as a sample
um you could so the first thing we're
going to build looks
it's going to look like this you're
going to have you know buttons
show me penguins and then um
there's gonna be some graphs plots and
yeah that we're gonna see how to how we
could integrate
streamlight with matplotlib seaborn
and plotly if you're so and it also
integrates with other planning libraries
but in this talk we're going to we're
going to look at those three
and afterwards we're going to do
we're going to have a dashboard we're
going to create a dashboard that does
explanations of predictions
in this case predicting the penguin
species these cute little penguins
we're going to make a model to predict
them based on um
features of the penguin and we're going
to have explanations about them
so let's jump into it
so um it's
most of all the material for this is
gonna be
in the link i'm gonna we're gonna
provide it i'm gonna write it in the
chat
and we're gonna and
i'm going to private in the description
video i'm hoping
so the first thing you do to start this
up
is that i'm going to start from from
scratch there's going to be nothing in
my editor
and i'm gonna have a terminal window
that's that's also here
all i have in this folder is some images
of the penguins
and um yeah so
i'm gonna follow them as an instruction
while starting any python project
i'm going to
i'm going to create a environment i will
erase that one up
huh okay cool so i want to build that
the the penguins thing that we have
before and i'll show you how to do it
from the beginning
i'm going to have some imports okay
cool that's good i'm going to have some
imports and then like
every time i save
would update by itself so in this case
if i have a title
that is something that is
show me the penguins
what
i see all right so to run okay so the
first thing is
all right let me start from the
beginning the first thing is to run
streamlets
you need to install the install the
libraries that i had in my
repo and then you run this command
called streamlight run
and i'm going to put an extra command
that says run on save which tells
streamlight to rerun the application
reload
every time i save so i'm going to go
quickly through this because
we had some technical issues but we
could we'll make it together
all right so in this case i want to show
me the penguins so
when i saved it it was it updates
the title if i if i don't say sum and i
save
you see that auto updates as well so
this is very interactive
and um i find this very powerful because
now i could um
interactively create
um interactions such as like let's say i
want to create a
dialog box a radio box i
input this i put this in the code and
then i could
when i save it it it auto updates the
dashboard in the web
in the application so in this case
it allows me to select a penguin so this
is sc.radio
and if i print out this species
you see that this radio when when i set
the radio
through the ui it auto updates the
species
in the program itself so in this case i
am outputting the species
so in this case um i have images
of the species so i could showcase the
images
like this using python's
f strings and so if when i click on this
thing it auto-updates to these cute
little penguins
and so it's very
cool so i'm writing pure python and it
auto updates the dashboard without
um without me writing any javascript or
any
yeah so i can stay in pure python
so here i'm going to create a dictionary
and i want to link it
i want to link my species to
um to the wikipedia page and i could
write peer markdown
so i could write some markdown and i'd
use f strings and then it'll give me
this um
this header
this header that links to different
that links to different penguins and so
off so if i if i click
if i click on ghetto and i click on
wikipedia page it will link to the
wikipedia page for the penguin so that's
pretty cool
now if i try to do eda i have a data set
in this folder
that loads the data set that loads the
data i could look at the data
like if i want to see the data i could
just write penguins
it would show me the panel's data frame
as a rendered html
so which is so you can see the different
features you can see the species
you can see how big the beef the beak is
or the
or the flipper length is and so forth so
you can look at the data
so if we have any questions we want to
ask about the data set
because let's say you have a question
about the inside they say how many how
many species are there in our data set
um so you see that i i i put the
question
in the as a header and then it shows me
in the dashboard
now so
one way to answer this is to use
use pandas so you could do
you could say the value counts so i
could have a penguin's value count here
and then so this will give me the value
count for each species
so so it will show me the panel um the
data frame
and if i ever want to plot if i want to
plot this
i could use the pandas api to plot
like so so this will this
this will help me plot
but there's no access so i'm going to
create an axis
because so this is for those who are
familiar with the matplotlib api
this will help plot and then for
streamlit
i have to create i use the map api to
create a figure i pass the access to the
plotting api
in pandas and this will quickly so
in three lines of code i could create a
bar plot
showing how many species are there per
data set
now
uh if i want to answer questions like uh
can what's the flipper length could the
fibonacci be used to distinguish between
the species
and in the aspects just so we could get
to the next
in the we could we could use uh like
we could use in this case cborn
and seabourn uses the map pilot bpi
so in this case i could use
this um which is this is a new function
called the
disk plot which plus distributions and i
could um give it
it it's very you i could give it
different
features in the data set and it will
help plot it i could give the hue in
this case species
in this case you can see that there's
difference that
the flipper length could distinguish
between the blue species and then the
green one
so so this is an example of using
streamlights but with
the streamlight api with the streamlab
api with matplotlib
for those who like uh plotly
for those who like plotly we we could
have
something we can answer another question
is the human
which is the the length of the the beak
could that you use to classify species
we could do a scatter plot
and plotly um where in this case i plus
i could place
x and x and y as the lengths
um okay so if i comment these out you
see that auto updates so that the
marginals disappear
and if i if i add these marginals back
in you can see that it auto updates and
adds a marginal back into my dashboard
so this is this allows us to very
quickly iterate on our visualizations
such that um
yeah so it allows you very quickly early
on iteration
on our visualizations
another way another question you asked
is how is the body mass for each species
distribute it you could use the box plot
and same thing for those familiar with
the plot api
this would help
in this case i'm applying the species on
the
x-axis and then the body mass on the
y-axis and the colors are the gender
um you can see that if i um
like yeah so i could remove the the
gender piece and
it will plot a box plot with the with
the genders combined
um and if i wanted to separate by the
gender
we could separate by just having the
color be gender so this is very
i'm so this talk is about some
streamline so if you remember the plot
api you could do this with the
box and plotting so
so this first example showcases how
you could you extremely could interact
with your deploying libraries that
you're used to
in this case if you use a plot
matplotlib
seaborn or plotly you could use
streamlight to
showcase your images without and while
you're staying in python
so you see that this is i'm just writing
python code and it's outputting me a
dashboard
interactively which is very powerful
so this is um the big thing about this
is that you see that every time i create
a figure um for me to output it
to output the figure in the dashboard i
have to
uh i i'm just i'm placed i'm placing the
item on its own line so in this case
scatter created an object called scat
and then i'm
to for it to be outputted into the
dashboard i
write scat by itself in this case so
that would
so streamlab will know to um
render this object in the dashboard
so that that's that is like
the basic it's very a fairly basic way
to use
streamlit just for data visual editions
um
me personally i like having questions
before a visualization because the
the question the visualization should
answer a question
so having its question driven
visualizations in my mind okay
in the interest of time i want to look
at the
data science piece so the first part of
data science is to visualize here to do
some
exploratory data analysis and this is
something we've done this
on the penguin data set the goal of the
the model i'm going to create in the
jupyter notebook
would be to use the features that we
looked at
to predict the species of the penguin so
i'm going to
create a very quick model using
scikit-learn and
i'm going to showcase how to create a
dashboard around this model
so um this is uh so i'm so i'm a data
scientist i'm in my jubilee notebook
uh i i launched my junior notebook
i'm gonna load the i'm gonna load the
data the same penguins data set we had
before
um i'm gonna have my x values which is
my features
and my y which is my labels in this case
the labels are the penguin species
i know i'm going to create a pipeline a
cycle and pipeline
where i'm going to encode the
categorical features and i'm going to
do nothing to the miracle features i do
nothing to numerical features in this
case because i know i'm going to push
this into a random forest
which doesn't require your numerical
features to be scaled so it could just
take in the miracle features
as is so if i create this pipeline
you see that in the juvenile notebook
this is a
newish feature in cycle learn it it
outputs the visualization of the
pipeline
so you can see how the data flows
through a cycle and pipeline
and this is enabled by
by setting this configuration set config
where display equals to diagram um all
this material will be in the repo so you
can follow this um
in when you have time to look over the
the
material for this talk
so in this case it will output this
visualization in the jubilee notebook
now um to we're going to train and value
the model so
in this case we're going to do a train
that split because
we are good data scientists and we're
going to train on a training set and
evaluate on a test set so in this case
this model is pretty good
um it's it's has 98 accuracy uh
if accuracy is a good metric in this
case for um
for time being accuracy accuracy is okay
in our case
and now we're going to serialize the
model so this is going to create
a serialized version of the model we
just trained
now so i don't wanna this talk doesn't
revolve around cycle learn so let's jump
back into
streamlit um so we create so we use
jupiter notebook
now we have to build the machine
learning model
now we want to as a we want to build
this thing like this like this thing
looks supe
like very complicated there's two
libraries there's two separate libraries
in here
there's a shaft value there's a shaft i
use the shaft library to crack
the shaft values and i use the anchors
library to calculate the anchors
the shaft values is like a game theory
concept where
when you have many players trying to
accomplish a task
you want to see how much credit you
allocate to each player
in this case the players are the
features and the task
is to make is the prediction so how much
does each feature contribute
to each prediction and that's chat
values in a nutshell
um we're gonna and anchors
is we're just we're talking about
anchors when we get to the
dashboard and when we develop the
dashboard um the surprising thing about
this dashboard
is that it this this this whole
dashboard takes around
a hundred ish lines of code so
like it's so because stream allows like
extremely allows
us to create these very interactive
dashboards with very few lines of code
and you get to stay in python so i'm
going to start this from scratch as well
let's let's try it alright so that was
my intro
so my intro was this thing it's very
quick um let's try another one so in
this case i'm going to stop that server
in this case i'm going to run streamlit
on the explain
so in this case it will run it will open
a new thing
and and of course it's empty because
there's nothing in my file
so let's start this off
so in this case i'm gonna have imports
we're gonna use a bunch of these things
and um just like before um i'm gonna
have some
categories i'm gonna have the features
just
so this is similar in the juvenile
notebook and i'm gonna have
my data my penguin data so
just to see some output if i output x
you see that the
the penguins data set is here if i if i
output y
it's it's the species names so it's all
here um
so um for this specific
um dashboard i'm going to need some
i want the user to as you can see before
i want to i want the user to specify the
island
and the gender and then and i wanted the
user to specify
some pieces about um the i want
the user to give me an instance and i
want my
dashboard to explain um why
my model made this prediction
so remember this is x this is explaining
the machine learning model
so i'm going to go through how to build
this in
streamlit so in the future
i'm going to need some of these
these metadata metadata about my
uh my data set um in this case it's very
these are very
simple um the metadata is just um
the the categories for the island
category and then the gen the categories
for the gender and also i wanted
i want the min max of each of my
numerical features which i'm going to
use later
when i set up this this
this um this interactive
selector because i don't want i don't
want the user to input
a number that is outside the bounds of
what
what's outside the bounds of
i want i don't usually put things
outside the balance of the the data set
so so i've saved the minimum vaccine
values for the miracle features
so to create the video i the radio item
the radio
the thing on the radio selector
i'm going to try i'm going to do one
first so sidebar that radius
i don't want to create let me let's
let's not do the sidebar yet let's do
the radio
and here i want to do select and let's
say i want to select
all right so i want to select let's say
the cumin length
uh all right actually let's do the
island
the island first select island so if i
do this i could
since i have the metadata i could
do something like this and this will
create this
select item thing but as you can see
from here i put this in the sidebar
so if i wanted it to be in the sidebar i
could do
instead of sc.radio i do sc.bar
sidebar and this will place it on a
sidebar
so so all all the interactions you could
place on a sidebar by
by preferencing the call by
with the word sidebar so in this
and um this this is normal python and if
i want to do
many of these let's say i have two of
them in this case i could use normal
python
to write a loop and um
in this case i want to store the user
input into a list
so i'm writing normal python on the left
and it's outputting java's
interactive javascript on the right so
in this case at this point
if i output the user input i could see
that
when i move the metadata i could see
that if i change this to male
you can see that the user input changed
to male if i change this island to
this island the use input changes so the
python is
updating every time i
interact with the ui which is pretty
neat
in the interest of time i'm going to
quickly look at also look at the
numerical features
in this case the numeric features i have
a number input
and i'm going to i want these step
boxes to give me
to go up and down in this case so
in this case i'm using a sidebar
numerical input and which allows me to
have numerical boxes for the
for the user to put in their numerical
values
and in this case um so then you see how
the input changes
as i update these values you see that
now it's 202
202 while this is chosen to 202
and i'm going to place this in a data
frame so if i output the data frame
it also also outputs the data frame and
i could change this
and you see how i change it to the
female and this change to female
okay so this is loading in the data from
the user
now remember we have a a model that we
trained
it's called penguin underscore clt.job
lib
so this is the model we could use this
to make a prediction
in the interest of time i will
showcase um pieces of this um in this
case on cycle learn you call predict to
get the prediction of your classifier
um and and i also want which clash is
predicted so
this code will help me grab what class
this my model predicted for this
specific instance in this case i picked
this
species i could also get the probability
by calling predict prabha
oh i already did that and then at the
end over here you can see that
i have the probabilities of each species
for my classifier in this case you see
that
chin trap has the highest probability so
that's the prediction made by the
made by the the model so
remember if you go back you see that i
have all this the sharp value stuff here
let's quickly look at that as well in
this case i want to create
i want to i want to create some ui some
headings for
what is what is i make what explanation
i'm explaining
i have the sharp values and
since um the library doesn't interact
well with
pipelines there's we have to
encode our data in
um using a piece of my of the pipeline
so this is
cycler and esque but it's still python
and and the way so i'm
in this case i'm in this case i'm
importing the
shaft library with tree explainer and if
i
uh okay so this is fairly involved
and i don't have too much time so i'm
gonna
try to get through this in this case
i know i call force plot which expects
the expected value
the shaft values um using coded
which is the encoding of the this data
by the pipeline and the thing about this
is that this library was built in such a
way that it wants the javascript to be
loaded first
so one way to do this is to grab the
javascript first and then directly place
it into the html
so like this is like because stream it
doesn't understand this library directly
like um there's there's ways to get
around this by
inputting the javascript yourself which
allows us to
write python like so what this took what
this took to embed this shap values into
the javas
into the dashboard was
20-ish lines of 50 lines of python which
is
i i still find very cool so
yeah so let's get to the anchors um
anchors is
even semi-simpler um anchors also
doesn't ex
um anchors is built in such a way that
it
expects numpy arrays so in this case
um i'm gonna create this angular explain
object and um they have this interface
where you want to explain an instance
and and if i want the html version of
this
i call as html and then it will output
this
this anchor explanation um the cool
thing about
the anchor explanation is
is that
a good thing about the angry explanation
is that
um it could
explains your instance in a very
specific way using anchors
where an anchor explanation is a rule
that sufficiently
anchors the prediction locally such that
the changes to the rest of the future
values of the instance
do not matter so in this case
in this case you could see that for this
instance
this is the anchor so it's trying to say
that if these conditions hold
the ai will the in this case the mixture
the model would predict
this species 97 of the time so
um if you had if we had domain knowledge
about
penguin species um
you could say that um is
is this counter-intuitive does this make
sense and um we could
we could um debug the model this way um
because this is what the model is trying
to
tell you about how it
it got to this prediction this chin chin
shot prediction
if i tried another model let's say if i
try another um
data data point let's say i try using
this island
and i use male and if i set
this to 49 and then sister 16
you see how every time i'm changing the
body
the data points the the application
updates automatically
in this case you can see that the shaft
values
in for the first two species change up
and
add the line go to zero while the the
last species again
gentle go to one and
um so in this case the shaft values is
telling us that
um these are the features so
these are the features and these
features push
um how much each feature pushes the
probability to zero and in this case how
much these features push the probability
to one
and the anchor explanation is telling us
that if the def
the cubeman def is lower than 17.3 and
the body mass is
greater than this then at 99.6 percent
of the time it predicts this species
so um that's not
so this is a gist of anchors it tries to
give
an explanation with some with
it tries to give an anchor explanation
about your
specific instance and
if it allows you to debug your model and
it
gives you a view into the machine
learning model
um okay so that's anchors
so you see that like the code
written here was all in python and it
allows me to create this dashboard
to have which i could ship to
someone i could ship so that anyone
could use this to explain the
predictions
so the penguins is a very low stakes
prediction but if this was a medical
prediction like if this was um
if you have cancer or not cancer a
doctor with domain knowledge about
cancer could look at these anchors
or look at these features to see if this
model is making sense
or that if this model makes sense in his
domain
or his or her domain and so this
is very useful in that aspect so
yeah so streamlet um there's a bit i
didn't get into
today about streamlets there's um
performance aspects
um there's alright so the streamlight
website
and there's a performance there's a
performance aspect where we have
caching and laying out which i didn't
explain where you could lay out your
dashboard how
how you want and caching increases
performance of your
your dashboard there's also a stream
that sharing
which you can sign up for which allows
you to create these stream
applications and they will help host the
shop app
the application for you to stream the
application for you and you could share
these
with your with others um
so all the links to slides and
everything and how they reproduce
everything i've
mentioned in this talk it's in this repo
um and
yeah so and the slides which i have also
resources on
the shaft values and the anchors and the
slides so this is
the streamline it's very cool it's it
allows
i've loved staying in python and then
creating dashboards and not having to
write too much javascript
and it's very powerful in that matter
and
thanks for listening everyone
thank you so much thomas um i have to
say that
when i used to see these dashboards in r
i was very very envious and i'm so happy
that
there's a way to make them in python
if anybody has any questions uh feel
free to post them
on on the q a thomas is here
with us for the next 10 or so minutes so
it's a great
opportunity to ask him any questions
so i do have a question for you thomas
how did you get started using it
it appeared on my radar
it's weird i could hear you just fine
and maybe it's my mic sometimes when
there's two mics going
i don't know do you you know i'll go on
mute do you want to check the q
a and just if it's if you can see the
tab and just answer the questions there
yeah yeah i could do that okay i could
read the question too all right
all right um so i i i
i use streamlets i got my radar because
i'm always looking at
different visualization tools um and
this
they just got seed funding and it seems
very exciting
um when this this
this this goes into the next question in
the q a like what are the key
differences between streamline and dash
dash so i was using dash for a while
to create dashboards
just and um
dash you have to very carefully you have
to
specify the html
um and like that you have to connect the
pieces together manually
and which takes time well my end goal is
to create the dashboard without thinking
too much about the layout
and or like and connecting pieces
together
in this case um you see how when i
connect the pieces together
they auto they automatically connect um
so when i store this input into python
variables
and i put the python variables as input
into other objects
it just automatically updates so like
when i click female here
it automatically connects this component
with components um with an anchor
with a shaft shaft value component and
anchors components
so it's very um flexible in this way
um what are other alternatives to
streamlets um
there's a few there's
there's um dash which
is heavily used there's also
vala where it converts a jupiter
notebook
to a dashboard um
those are the two that i hear about the
most
uh when it comes to writing python first
and then converting it to a dashboard in
that space
um the next question is is there a time
limit for the external api
does this stand up for as long as i keep
the
server running um as you keep this
as long as this this this is running it
will
it'll be okay and as long as your
machine can run it
so so yes only keep the server running
everyone so in this case remember this
this needs a server component
to serve the material because there is
python running in the background so when
you update these inputs
python is running on a server somewhere
and in this case my local machine and um
and updates the ui reactively
next question is there is a progress bar
in
the streamlit but i was thinking if
there was an async way
a way with async io i don't think
streamlight currently interacts with
python async io
currently
i'm and look at chat what are
the next question is what challenges
are missing features have you found from
streamlet
the biggest mixing feature has recently
been added which is the layout
which it's a beta feature so that's so i
didn't include it in this talk
because it could change but it was
it was for a while it was extremely
hacky
to get like two columns in streamlit
but now they made it easier with um
something called beta columns and
because it's a beta feature
which allows you to um so if you see
here it allows you to write
python like instead in this case i want
three columns
and it uses python's context manager in
such a way
where you could specify in this case
three images to be side by side in three
columns
so this i i felt that this was the
biggest feature missing
for a long time but they recently added
this feature
and so i'm happy
um so yeah
i i can't think of any more features
for myself that i will want from
shameless after they have added
layouts
another question is what is the easiest
best way to deploy a streamlet app to
make it accessible on the web
there are two ways the one way i i've
i didn't show directly in my
presentation but
in the repo is that you could deploy
using heroku
and heroku deployment is pretty simple
you just need a profile
and a runtime file
that specifies the python version and
the proc file to specify how to run it
and okay of course and a requirements
file to specify what other requirements
you run it
that's one way to run it the other way
to run it and shoemake is providing the
service
for now it's providing a service to
share
your streamic application so there's um
if you look at my the slides
there's a sharing stream of sharing you
can sign up ashima sharing
and allows it allows you to share your
application with others and they'll host
a service for you
for now for free
okay
i visited the external ip i external ip
port but i don't see the dashboard it's
a positive share dashboard as i'm
developing it
oh i haven't used that workflow before
where you could i think it's possible
but you you would have to them into the
server
and then edit the file direct like on
server
i could see other ways to do it but um
you have to have the server watching the
file as you develop
and i can see that working as long as
you
do the correct networking to make sure
you have access to the server
the question was um i visited the
external ip port but i don't see the
dashboard is it possible to share the
dashboard as i'm developing it
so there is yes as long as you can
access the server
and you can and the other person has
access to the ip
next question is is it response is it
responsive
um okay let's so if i
if i it's as sponsored as it could be
for a dashboard that takes
this much space you see that how the
sidebar closes
so that so if i was on the phone i would
see this
which is okay but you see that the
dashboard takes up a lot of space
in itself the visualization takes up a
lot of space but it is
responsive and
as i yeah
okay and
um i think it's i think that's all the
questions
thomas thank you so much and thank you
so much for your patience with our
technical difficulties as well
i'm glad um i'm glad the presentation
the show
did go on so thank you
