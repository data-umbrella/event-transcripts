# Marco Gorelli:  Contributing to pandas

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/20-marco-pandas.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/273988776/
- Video:   https://youtu.be/TVe-uT_So6c  
- GitHub repo:  N/A
- Slides:  N/A
- Transcriber:  ? [needs a transcriber]

## Resources
- Documentation:   https://pandas.pydata.org/pandas-docs/dev/development/contributing.html
- Installing Conda:  https://conda.io/miniconda.html

## Video

<a href="http://www.youtube.com/watch?feature=player_embedded&v=TVe-uT_So6c" target="_blank"><img src="http://img.youtube.com/vi/TVe-uT_So6c/0.jpg" 
alt="Marco Gorelli: Contributing to pandas" width="50%" /></a>


## Transcript

hello everyone and welcome to
data umbrella's webinar
our our agenda is going to be i'm going
to do a quick introduction
and then marco will be doing his talk
and we have q a at the end
this is actually a special webinar
because what we will do
after marco's presentation is we're
going to go over to discord and if
anybody wants to set up their
environment
we have somebody to help
people who are viewing this reporting
after today is tuesday december 15th
a little bit about data umbrella we are
an inclusive community for
underrepresented persons in data science
and we are a volunteer run
organization
a little bit about me i'm a statistician
data scientist i have a master's in
statistics
and um let me just get my slides back
i'm going to uh okay
for some reason i think we're both
sharing at the same time or something
sorry i didn't realize i was sharing
yeah
[Music]
there we go thank you okay um yeah i
have a master's in statistics in the mba
from nyu
in technology and management and
business analytics
i'm the founder of data umbrella and um
if you'd like to connect with me feel
free to follow me on either twitter
linkedin or exactly
but we have a code of conduct uh we are
very uh
serious about our code of grondik
because we want to continue to provide a
professional inclusive community
and that applies to the chat as well and
also for this because it's a special
session and some people will be joining
us on this board please keep in mind
that when you join this board
make sure your username is something
that is professional
welcoming and inclusive
uh because we're a volunteer
organization there are various ways that
you can support us
the you know the most important one is
to follow our code of conduct and make
our community
uh what we want it to be um on discord
if you have any questions you can ask or
answer them with the community
i will post the link to discord in the
chat it's also available on our website
we have an uh open collective where
people can donate to help support us
and cover our operational costs and we
also have
transcripts of our webinars available on
github and if you'd like more
information there
you can look there or email us and
see how you can contribute and
participate
um we have uh our meet-up events are
posted on meetup.com
our videos our webinars are all recorded
and placed
on youtube we have a job board as well
as a monthly newsletter and we have a
lot of resources available
on our website
on our video library on youtube we have
a couple of playlists and one of them is
open source
and we have a recent one about numpy
there's one for
learn and we will be adding this canvas
video
to that list as well
but we also have and i think i
mentioned that we have a career track as
well
it takes like i tasted the wrong thing
and here's a
um a collection of some of our videos so
check them out
depending on what topics you're
interested in
our job board is jobs at
dataumbrella.org
our highlighted job today is cloud
infrastructure engineer at
coils um it is a remote friendly
position
a coil connects data scientists and
researchers to distributed
infrastructure
using the python data science stack
which is numpy pandas that could learn
and ask a popular open source library
for parallel analytics
um the founders of coil come from the
open source python community and they're
very familiar with python and das in
particular
so if you're interested in a position
just check out jobs.dataumbrella.org
on our website we have a lot of
resources at dataumbrella.org
we have a list of conferences open
source um
documents on how to contribute we have
guides to using inclusive language in
your work
we have guides for allyship and how to
deal with burnout and prevent burnout
and aifix and a whole lot more
so um please check out our website
um you can also connect with us aside
from meetup on twitter
linkedin and subscribe to our youtube
channel
um that's the best way to get
notifications on when the videos are up
and i will share
some of these links in the chat as well
our upcoming event for january is
creating a command line focus
development environment which
i'm really looking forward to it's an
essential tool
for data scientists um new
and experienced so um posted on our
meetup page so
we hope you will join us for that
today's speaker is marco guerrelli he's
a data scientist at samsung
joining us all the way from the uk
outside
of work he's a maintainer of candice
data wrangling platform for python
um he's author of mdqa code quality for
jupiter notebook
and marco holds a masters of science in
mathematics and foundations of computer
science from the university of oxford
and you can find marco on github
marco gorilla
so with that i am going to put myself on
mute and hand it over
to
[Music]
hello uh thanks rashama
all right i believe i'm now sharing my
screen if i'm not please do let me know
so hello friends we are here to talk
about
pandas and in particular how to
contribute to it
with me marco e him
your screen sharing has been
disconnected
whoops my screen sharing has been
disconnected
what's just happened
uh is this still going
start screen sharing sharing on
hello
okay you can see it now yeah it was just
a delay but it's now
there okay yeah sure sorry my upload
speed isn't uh
as fast as would be desirable but it's
it's what i've got to work so i was
saying
i'll start by telling you a bit about
the team and governance
then i'll go over what kinds of issues
you could work on
if you decided you wanted to contribute
to pandas
after that i'll walk you through how to
set up your own development environment
so you can start contributing and then
i'll walk you through what it looks like
to open a pull request
after that we'll have a live five
minutes q a
we'll then take a break and we can head
over to discourse
so that if there are any keem bees who
want to start contributing
straight away then i can offer them some
assistance in setting up their
development environment
great let's uh dive in
pandas was first released to the public
in 2008
after being created by west mckinney
now this is the part of the story
uh this is where the story of pandas
usually ends
which is unfortunate because it's now
led by someone called jeff
ryback and the reason i think it's
important to highlight this is because
otherwise
wes gets all of the compliments and all
of the credit
and jeff gets all of the complaints and
all of the bug reports
so let's show a bit of appreciation for
the excellent work that jeff is now
doing
if you look on the pandas website you'll
see that as well as these two figures
there's another 24 who who are listed
under the maintainers section
and this is the part that i'm a bit more
embarrassed about because
we have a nice diversity and inclusion
statement about how open we are to
uh people from diverse backgrounds and
all we have a code of conduct and the
code of conduct committee
but then if you scroll up you see that
we're all just a bunch of blokes
so how can we fix this well ideally
society wouldn't be such that women do
most of the unpaid labor
but in the meanwhile i believe we have
some kind of a duty to take part in
sessions like this one that are
specifically targeted towards
underrepresented minorities so thanks
reshamma for putting this together
although i'm i certainly i'm not kidding
myself i don't think this is going to be
enough to solve the problem
but you know pandas has done events like
these in the past i just hope that
i can learn something from it and we can
and this can inform our future
steps speaking of maintainers
why might someone be interested in
becoming a maintainer
well first it's a really nice community
you'll meet some lovely people and
you'll make some nice friends
next you'll gain loads of new skills
not just technical skills even
interpersonal skills
and finally even if you don't get
directly paid for your work on pandas
it'll probably help you in your career
so if uh if that's motivated you
let's say something about how to become
a maintainer
this is all highlighted outlined in the
governance document on
on the website but the summary of the
summary
is if you're helpful on the issue
tracker and reviewing pull requests and
making contributions
and you carry this out for and you
sustain this for
about a year or so then you might be
invited
to become a maintainer so
seeing as i'm here i'll also say a word
or two about how i got involved in the
project
and this started in august 2019 when i
first opened an issue
in which i was asking about some error
message which
i didn't think was very clear and i got
the response
hey marco are you interested in
submitting a pull request
now at the time i only had a vague
understanding of what a pull request was
i didn't really know how to contribute
to open source
nor did i know that i could but it
seemed like
a fun thing to try giving a go at
so i found on the pandas website there
was a contributing guide document
i read through it it actually explained
everything that i needed
very clearly so i followed the steps i
was able to open my first pull request
and found the response from the
community to be very friendly and very
encouraging
and i got a huge adrenaline rush when
they finally approved and merged my pull
request
so i continued doing this for a bit and
after about four months
was given triage access and then after
about a year
i was given right access anyway that's
enough about me let's talk about you
and more specifically what could you
do if you started contributing to pandas
if you look at the pandas page on github
you'll see that there are more than 3000
open issues
there's all kinds of things that need
attention
and a lot of these are not actually very
easy to work on if you're a beginner
however what you can do is you can
filter the issues on the
good first issue label and you'll find
ones that
we think are good for beginners or
people who maybe are experienced with
python but are not
don't have an in-depth knowledge of the
pandas codebase
so let's look at what kinds of
contributions people make
these are in the these are of
different levels of difficulty so one
type is to make an enhancement
so adding a new feature now adding a new
feature
isn't that easy in pandas pandas already
does a lot of things
and so we're a bit hesitant to make it
do
even more things so before spending
hours
implementing some new feature which you
think needs to be in pandas
perhaps first check with the current set
of maintainers if they would be welcome
if they would welcome such an addition
other types of contributions include bug
fixes
now pandas is quite serious about
promoting test driven development
so if you submit a bug fix you should
typically also submit a test
which proves that the bug was fixed and
also prevents the bug from being
reintroduced
in the future next documentation
if you find that the documentation isn't
clear
or if someone else complains that the
documentation isn't clear
and you have an idea for how to make it
clearer then certainly
a contribution a pull request to
clarify the documentation would be
welcome
next you can add or update tests
sometimes we
find that some areas of the code lack
sufficient
test coverage and so we will typically
mark these
issues with the needs tests label
so if you submit a pull request for
those that's always welcome
and finally if you're familiar with type
hints
then any new development
should have type ins but also there's a
general
move towards adding type hints to the
existing
code based so if you're familiar with
type ins this can be a great way
to to really get familiar with the
project
if you're new to open source then i
think documentation
fixes and test fixes are probably
the easiest way to get started
but if you want to get started you'll
need to have set up a development
environment
now i mentioned earlier that when i
started i read through the contributing
guide
and that explained everything i needed
to know
nonetheless today i'll walk through it
with you
so that you can see what it looks like
and it won't all be a complete mystery
when you're just reading through this
really long document
so the first thing we'll want to do is
to fork the repository
so to do that we're gonna want to go to
github.com
pandas dev slash pandas and we will
click
the fork button i've already done this
but
you will get the option to fork it to
your account
once in there you'll want to clone it so
you'll copy the link you find here
you'll open up a terminal and you'll
write git clone
and then you'll put the folder in which
you want
to clone it i've called it pandas
marco typically we advise people to put
pandas dash and then their name it
doesn't have to be your name you could
put pandas dev if you want but what we
don't recommend
is to just put pandas because otherwise
you might
start a python rebel in this directory
you'll try to import pandas
and you'll accidentally be importing the
wrong thing so let's call it pandas
marco
now if i try doing this it doesn't
actually work because
i've already done it but for you it
should start downloading all of the code
once you've done that you can go into
your
repository and you can set up a mini
conda environment
uh you don't have to use mini conda
there are other ways to set up a
development environment
but in my humble opinion this is
probably the easiest
so the the command to do that is conda
and
create f environment
now this isn't going to work for me
because i've already done it
but for you it'll start downloading all
of the requirements
to build python to build pandas
once you've done that you can activate
your environment
conda activate pandas dev and then
there's another two things we need to do
before we can start contributing so
first
we'll be uh building the psyphon
extensions
so that'll be python setup.pi build x
in place and then j4 or you can pass a
higher number if you have like a really
powerful computer
with lots of cores for me this has run
really quickly because i already
did it but you can expect it to take
some time
if it's the first time you're doing it
and then finally
you want to make a local editable
install
so the command for that is in the
contributing guide
uh i think it's pyth
pip install dashi dot no build isolation
and then no
use pep 517
which will be very fast for me because
i've already done it again for you it
might take a bit longer
finally let's check that the
installation worked correctly
so we'll start by typing ipython or just
python and then let's try importing
pandas
we get no error that's already a good
sign
and then let's type pandas dunder
version
and if you get something that looks a
bit messy like this
it means you've probably done it
correctly great
so now that we've got our development
environment
set up actually we haven't quite got it
set up there's one more thing we need to
do
and that is pre-commit install
so this will enable a tool called
pre-commit inside our environment
i'll i'll show you how what pre-commit
actually does a bit later
when we try making a pull request
so we've set up our environment now
let's try actually working on an issue
and opening a pull request the issue
will be that i've chosen will be this
one here which was reported
a few months ago in which someone
noticed
that a certain command was working
in version 1.0.3 but then stopped
working
in version 1.1.3 this is something we
call a regression
so let's check that this is true
let's try reproducing their example
they've told us that this should raise a
key error
and indeed we can reproduce it
so it is a bug we need to fix it
so let's see how we can go about fixing
it
something we advocate for in pandas is
test driven development
and that roughly has got
three phases red green refactor
red means you should start by writing a
test which should initially fail
green means fix up your code such that
the test passes
and then refactor optionally clean up
your code
and it's important that you only do this
once you've got your tests in place
because otherwise how do you know that
your attempts to clean up your code
are actually cleaning it up rather than
introducing extra bugs
so let's start with the first phase and
that was
to um to do to write a failing test
now pandas already has a file called
test underscore info
so seeing as this bug has to do with
the dot info method let's put it in
there
so first before we actually write any
code let's make a new branch for this
i'm gonna call it bug info integer
call names just so i can remember what
it's about when i refer to it in the
future
it's not too important what you call it
next let's put in here
the issue which this person reported to
us on github
now i will warn you what i'm about to do
is
probably going to be a bit too fast for
anyone who's trying to follow along um
however as i mentioned earlier the steps
to contributing all described
meticulously in the contributing guide
this is just to show you what it looks
like to get to
so so you can see what it looks like
don't worry about following all of the
steps
live so let's try to test i'm going to
call it test
info integer call
column let's be explicit names next in
here i'll paste
the example which this person has
uh reported to us on github
then i don't need to do pd.data frame
we've already got that in here
okay great now if you remember from test
driven development
the first step was red that is to say
write a failing test
so let's check that this test actually
fails
and we'll do that by running it using pi
test
and indeed
it's red it's failing great
so now we can go in and fix our source
code to make the test pass
and after a bit of
inspecting the source code and uh git
log
to see when the bug was introduced it
turned out that the fix was simply to do
dot i lock
here and here
and you'll see that now if we if we try
running the test again
it passes so we've gone from red to
green
and i am proud to say that i am the
person who fixed
this bug in pandas however
uh i am less proud to admit that i am
also the person who introduced the bug
in the first place so maybe i shouldn't
have brought attention to this fact
anyway now that we've gone from red to
green
the last thing we'll want to do is
refactor before
pushing up to our fork
so something we ask contributors to do
is when they make a new test they add
the issue number
so that uh future contributors can more
easily
find what issue each test
refers to so let's put that in here
next we will also want to write a note
in the release notes
so let's put that here let's write fixed
regression in math
data frame dot info
throwing exception
key error when called on a
data frame with integer
column names and then we'll put the
issue
number awesome
now that you now that we've done that we
can
stage our changes we can commit them and
then we can push them
and finally we can open a pull request
so let's go through those steps one by
one
we will stage our changes with git add
hue then we will commit them and
let's write a message such as a fix
bug in dataframe.info
when called with integer column
names now earlier i mentioned
that we had done this command pre-commit
install
so now if you press enter you'll see
what that actually does
it'll run a whole series of automated
checks on
the code which we've changed and
it will block the commit if any of these
automated checks fails one of these
checks which has failed is an auto
formatter called black
so it's black as fixed has formatted our
code for us
so now we will have to
repeat the last two steps we will have
to stage our
changes run git commit again and now
now that the auto formatter has already
fixed our
code then it will all pass so the final
thing we can do
is we can push to our
fork and then we can open a pull request
you'll see that we get a link here
if you follow that in your browser
you'll be able to open the pull request
i'm not going to do that now i already
made a pull request for this
but if i was doing it anew then i would
do it either from there
or if if you go directly
to the pandas page yeah you see it
it'll actually tell you um hey you just
uh
pushed to this branch a few minutes ago
do you want to open a pull request so
you can just press that
and create it easy
cool so that's uh yeah that's a little
walkthrough of what's involved in making
a pull request
so now that we've done that let's go
over what we've gone over
so in confusion we've seen that pandas
is a friendly community
and it offers you a great chance to
learn all kinds of different skills
we also saw that regrettably the current
dev team is totally male dominated and
hence
there needs to be an active effort on
our side to address this
we saw that there are many many open
issues which you can work on
such as enhancements bug fixes
documentation tests
typings build and
i mentioned that if you're new to this
then documentation
and adding tests are probably a good
place to start
and finally i mentioned that the
contributing guide
tells you everything you need to know
about how to start contributing
and i also went through the process of
setting up the development environment
for you as well as
opening a pull request but again both of
these are meticulously documented in the
contributing guide
so that's it from me i hope you go out
and make a contribution to pandas
so let's uh let's open this up to some
live q and a
or it'll either be an engaging q a or an
awkward silence it
depends on you and after that we can
head over to discourse
and any keem bees can get started
either in the chat for the q a um this
is a great time because we have
um canvas cord developers
right now well okay yeah lots of
comments i wasn't
noticing while i was talking okay some
missions about uh screen sharing i hope
it wasn't
too bad but i guess i'll see you later
if i've got the courage to watch myself
on youtube it's okay i think what
happens is when you change screens
there's a delay so it goes online
um but you know it's fine uh you're
speaking so we have
what you're saying so asked about the
documentation and it looks like it is
available as well so
that's good yeah okay so
i hope the step-by-step guide set at the
end will also be shared later yeah
that's all in the contributing guide
i mean if you just search pandas
contributing guide you should find it
but
let's let's put it in the chat anyway
here you go
uh next
um yeah that's it okay
any other questions we should answer on
air
there is a question in the q a that says
how much level of python knowledge is
required for contributing
to canvas um well
sorry oh q a sorry i i didn't see that
there was this extra
um tab i could go to okay cool this
really depends on what kind of issue you
want
to contribute to so something like
fixing a bug might require
you to be familiar with pi test and with
debugging but uh
clarifying the clarifying what a
parameter does in a document
in a docs string in the documentation um
i i wouldn't think that requires
much experience with with uh with python
um but really we need all we need uh
contributions
of of all kinds it's not like some kind
of contribution is uh
um way more valuable than some others
you know
the documentation needs improving bugs
needs need fixing so
um please please do try contributing uh
if you're interested in contributing
please try doing so regardless of how
good or bad you think your python skills
might be
i can assure you you'll learn a lot by
making any kind of contribution i feel
like
almost every time i open a pull request
i'm learning something new
so could you explain again what the
setup that pi
script did when building the environment
yeah so that one
uh builds the syphon extensions so these
are
these um so uh so
some of the faster parts in pandas are
written in syphon
rather than in pure python so for those
you'll need to
you need to run this uh python setup.pi
dashi text
and you'll you need to do this anytime
the c extensions
have changed so it's
it's a it's a command we're running
periodically so
uh if if i make a pull request and then
uh a week later someone else has made
uh commits to the master branch which
have changed some of the psyphon files
and then i pull uh i will probably again
have to
run the python setup.pi
build.xt command in order to get
my pandas build working again
all right if anyone has any more
questions
uh this is a good time to ask and then
we'll go over
to discord um where people can you know
set up their environments and ask
questions
one one going twice okay
so with that i will end the recording of
this webinar and we're gonna head over
to um this um
so see you over there and i want to
thank marco
so much for joining us all the way from
london and
putting on this great presentation thank
you rashma
