# Matti Picus: Contributing to NumPy

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/19-matti-numpy.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/274689815/
- Video:   https://youtu.be/lHJqOE5j6xE 
- GitHub repo:  
- Slides:  https://github.com/numpy/archive/blob/master/content/data_umbrella_dec_2_2020/data_umbrella.ipynb
- Transcriber:  ? [needs a transcriber]

## Resources
- NumPy Slack: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A
- Documentation:   https://numpy.org/devdocs/dev/development_environment.html?highlight=gdb#debugging


## Video

<a href="http://www.youtube.com/watch?feature=player_embedded&v=lHJqOE5j6xE" target="_blank"><img src="http://img.youtube.com/vi/lHJqOE5j6xE/0.jpg"
alt="Matti Picus:Contributing to NumPy" width="50%" /></a>



## Transcript

Hello everybody,
welcome to Data Umbrella's Webinar.
so our processes usually, I do a
quick introduction.
Matti will do his talk and we'll have a Q&A;
If you have questions you can post them on chat
or you can post them in the Q&A tab; I can easily move questions from
the chat over to the Q&A,
so that's fine um and this webinar is
being recorded
and will be available on youtube um
usually within a couple of days but
sometimes a week depending on
how much editing has to be done.
A quick introduction about myself, i'm
the founder of Data Umbrella
i'm a Statistician/ Data scientist by
training and
I am available on Twitter, Linkedin and
Github @reshamas, so
feel free to follow me if you'd like.
We have a code of conduct here uh; we're
dedicated to providing harassment free
experience for everyone this applies to
the chat of this webinar
as well. Our code of conduct,
you can link to it on this link to the
sticky pad if you want to go to it.
Thanks for making this a welcoming
and friendly community for all.
If anybody does sort of put something
inappropriate in the chat,
we will remove that person from our
community.
uh and to let you know that we are a
volunteer run organization.
There are various ways that you can
um support our community.
The very first way is to follow our code
of conduct we want to make it a
welcoming and inclusive space for
underrepresented persons and so
um following our code of conduct and
contributing to making a professional is
like our top priority otherwise you know
it could be like
any other community. We have a Discord
community chat so feel free to join it
it's on our website;
um it's a it's a place to ask and answer
questions there.
We have an open collective where people
can donate to
um cover our operational expenses
expenses
and we also have an initiative this
video
um to do a transcript that will be
available for people
to read later.
The location of the transcript is on
github.com/data-umbrella/event-transcripts
You can also find transcripts for past
events there.
We have a job board which is at
jobs.dataumbrella.org/
Check it out just if you're curious or
if you're on the market.
On our website which is dataumbrella.org
we have a lot of resources for open
source, for accessibility,
for responsibility, social impact of ai...
so please check it out later at your
convenience.
We also have a monthly newsletter which
is dataumbrella.substack.com, i'll
copy the link and put it in the chat
later. We send out a newsletter once a
month so feel free to subscribe we
promise not to send you
spam.
We are on all social media platforms as
data umbrella; the best place to join
really is our Meetup
group because that's that has our events
in it
um and then there's you know we're on
Twitter and Linkedin and
also Youtube so this is being recorded
and it'll be uploaded to Youtube so you
can check out our past
events there as well and if you
subscribe to Youtube you get this
notification on your phone uh which is
useful.
um
We have uh two upcoming events we're
gonna have a Contributing to pandas
webinar on December 15,
so you can find it on our Meetup page; we
also have a Command Line
setup Environment which is on January so,
you know, there's more information on the
Meetup group about these events and
signing up for it.
Today's speaker is Matti Picus. I hope
i'm pronouncing it that right.
um Matti is an active computer
contributor to numpy and a member of the
steering council.
He's also a core developer and release
manager for PyPy. He also contributes to maintaining
the scientific python stack across the
ecosystem of packaging, CI which is Continuous
Integration and documentation.
Since april of 2020 and this year he has
worked at Quansight Labs and you can find
him on Github at mattip;
and with that I will turn off my video
and
I will hand it the floor over to Matti.
Great uh okay here we go
so my talk today is how to get involved
in numpy
um as Reshama said my name is Matti Picus.
This presentation is in the Jupyter
Notebook
and when we put up the youtube video
we'll actually link to that
notebook as well.
I'll be tabbing around my web browser a
bit hopefully the lag won't be too bad
and won't make you too dizzy.
Use the chat and the Q&A. There's some
ringers in the uh
in the audience, some other numpy
contributors and they'll be happy to
answer your questions
um as we're going along um
and my goal and the goal the the reason
that
we'd like to talk to you today is to get
help with
to get you started with helping us with
documentation,
tutorials, code and devops. So numpy is
much more than just the code itself.
We have other ways you can contribute.
So what are we going to do? First of all,
don't panic the project itself is huge
it has lots of different corners
and i'm gonna talk about some stuff and
if it doesn't make sense,
that's okay i'm gonna have a brief
history of numpy.
When was it started? By whom and what? for
what drives numpy? what are the goals and
how do we decide on those goals?
who are the who decides what happens in
the community?
We're going to talk about communication
channels and ways you can get in touch
with us
and the different repos there are in
github and then we'll
demonstrate how to build and test numpy
and then we'll take a look at
some how to find issues and prs that
contributors can work on
and then at the end we'll take some
questions if there's still time;
but first me my name is Matti. As I said
i'm a Quansight developer. Quansight is a
company of about 80-90 developers working both in open source
and for contracted work.
I was previously employed by the
Berkeley Institute of Data Science to
work full-time on numpy
I did that for two years before i joined
Quansight and i'll talk a bit more about
that
later. I'm an avid open source evangelist;
I believe in open source. I think that's
the best way to produce
quality code and software.
PyPy is a project to implement Python but not via C, actually
via Python. So it's python that
implements Python just like
the C compiler is written in C um
If you want to know more about that you
can find out about it on pypy.org
I believe deeply in the power of
community that's why
i'm doing this talk. That's why i've been
working on open source for the past
couple of years.
I spent a long time in an intentional
community in Israel called Kibbutz,
spent over 10 years there and i think
that community is
is the way that society should be
organizing itself;
and i also believe in diversion and
inclusion.
I was lucky enough to have a very uh
smooth
course in my life not everybody else
does and i'd like to help others
move on and become able to contribute to society tech and
open source in particular.
Okay so back to the talk about Numpy.
Numpy, as you can see here in 2006
uh it was started by Travis Oliphant. It
grew out of two other libraries: Numeric
and Numarray
as a way to synthesize those two
libraries together
and it was the cornerstone of what
Travis actually wanted to build which
was Scipy.
So Numpy sits under Scipy and it turns
out
Numpy sits under a lot of other things
as well. As time went, on the Numpy API
and the Numpy way of looking at
a chunk of memory and dividing it up
into
items became very popula,r was adopted by
the deep learning
frameworks by a library called CuPy,
which allows you to
do Numpy-like operations
on data on your gpu. Dask and Sparse also use it.
Also use the the API and the ideas behind
numpy as well as numpy itself.
Numpy's quite popular pretty much it's
the first thing that people will install
if they're doing data science
and they want to they're building a
python environment.
We estimate that it's got tens of
millions of downloads and users
worldwide
and uh it's maintained now by about
10 people that's a bit of a stretch
maybe six people
actively uh maybe full-time
equivalents of about two and a half or
two people.
It's over its lifetime it's had 1.4
million
dollars u.s dollars in lifetime funding
about
over a million of that was uh donated by
the Moore and Sloan Foundation in a
joint grant
that I was lucky enough to participate
in. It started about
two and a half years ago they hired
about
three developers to work on numpy
full-time for two years
along with some other things and that
really gave the library a boost.
The infographic below shows how Numpy
is used pretty much everywhere,
but of course you all know that.
Okay, that was a brief history of Numpy.
Now, we'll talk about
what actually is Numpy, how do the
core people who push Numpy forward
what do they think the goals of it are.
So as I said, this is all a Jupyter
Notebook,
um i'm just using the the website here
because i'm too lazy to actually write stuff by
myself
so if you go to the website you can read
about what
Numpy is. Numpy is run by a steering
council.
There's about a dozen people on the
steering council.
The steering council is a loose uh
loosely appointed
self-appointed group of people who are
the currently the
active contributors to numpy and they're
the ones who will decide
what uh direction the the the
project will take. Numpy is made up of a
bunch of overlapping teams. We have teams for
might be a bit small here to see this
but we have teams for code
documentation, the website, for triaging
bugs and issues
and a small team for getting funding and
grants and administrating the project
and we also have a small number of
sponsors I already mentioned the Moore
and Stone Foundation,
Chan Zuckerberg Institute initiative
has been active in the past couple years
giving us some grants
and Tidelift gives us monthly support
and uh both of these industrial uh
partners institutional partners i've
been working i've been lucky enough to
work at
over the past couple years.
So how how do we decide what not where
we're going to go with Numpy?
so if you look at it from the top down
we can look at it from the bottom up
we're going to do that as well
but if we look at it from the top down
Numpy is
it's higher level goals and when we look
for funding
what we're trying to do is to get
actually
funding for our roadmap. The roadmap
describes the scope of Numpy
and our wish list of features we'd like
to work on and then
enhancements, large chunks of future work
on Numpy
will be done through Numpy Enhancement
Proposals or NEPs N-E-Ps. These are proposals to change
things like the dtype um system
underlying the the array object or the
random number module that was in Numpy or one of the
latest ones that's uh to put
uh to make all the functions in Numpy
use processor intrinsics.
Okay, so that's kind of a higher level
view, but
what does Numpy think about itself? Numpy
is a very nice way to work with a chunk
of memory on CPU with strides, shape and dtype
and one of the most important things
that we as developers take to heart
while developing Numpy is not to break
anything. We have a strong commitment to be backward
compatible and not to break
people's workflows we realize that Numpy
is is a basic
uh core piece of the data science stack
in in python and we're trying to be
careful not to break things.
While performance is important
interoperability beats performance
as I said before Numpy was started as an
initiative
to be one piece in a larger puzzle we
realize that that
that is a is a deep commitment and
that's part of
what numpy views itself is as doing as
being the
being at the forefront and at the base
of a large number of
python array type
objects and driving that forward so that
people can do things with numpy
that uh that may uh
that that aren't built into numpy but
enable interoperability with other
libraries.
So what do I mean about interoperability?
Don't worry if this is a bit of a deep
dive and you miss a bit of this
uh it's more of a higher view of of
how just trying to in um trying to
emphasize
how Numpy wants to work nicely with
other
libraries and to interact with other
libraries in a nice way.
What goes into Numpy is actually
very tightly controlled we try to keep
many things
out of Numpy provide only the minimum
tools needed to work with the basic
library that Numpy
is and would rather delegate
other tasks to other libraries that can
move a lot faster
and maybe break things where Numpy has
to be careful not to break anything
so one of the things that's in Numpy is
an is an extension to distutils which is a tool to build
libraries but things like optimizations which are
in Scipy or loading images which are in
Scikit-image and pillow
or working on the GPU which are in
Cupy and JAX,
they won't ever hopefully come into
Numpy.
It's hard to say never but they they're
probably will never come into Numpy
there are pieces of of code that are in
Numpy for historical reasons and
probably shouldn't be
one is a is a minimal fft implementation
the one in scipy is much nicer
as is the linear algebra routines that
are in sci-fi they're much well
better thought out polynomial and f2 pi
were two
pieces of code that uh kind of orphans
no one really wants to take care of them
so they've stayed in numpy
and the random module that's in numpy is
a best of brand
random number generator um that we're
very proud of
and it would it is in Numpy but
you might think that it doesn't actually
um
belong in Numpy it doesn't actually go
with the core mission of Numpy
in addition numpy provides throughout
its code
a way to take this ndarray object that
I talked about that
that has the chunk of memory on the uh
on the CPU with strides and shape and
allows you to
subclass it via different protocols the
array of the __array__ protocol, __array_wrap__ protocol, __array_struct__
protocol, __array_priority__ protocol.
All these are useful for subclassing ndarray
in a way that doesn't actually um
it overrides the behavior of the ndarray but it doesn't
uh affect the code in numpy itself so
it's another way we can interact with
others then we determined that these were not
enough we need
more ways for people to be able to
override things in Numpy
and so we provided three new protocols
the: __array_ufunc__ protocol, the __array_function__ protocol and the
__array_module__ protocol
to also make overriding functions transparent
so all those protocols are the reason
that you can do something like the code
that's on this page
you can do import numpy as np
import cupy which as I said was the
library that allows you to work on a
GPU. You can create a cupy zero
array by 10 by 10 of the dtype
np.int and then you can
call sum on that now when you call sum
on that that's actually calling the sum
method on this a
object but if you call np.sum
that's calling a procedure from the
numpy array
but because we have protocols you can
override that and that actually calls
back out
to cupy to provide their
their function. As well, you can
override functions okay sum is a u-func
if that means anything to anyone mean is
a function
you can also override that with array
function
and lately our last step in this
procedure and one that will be out in
the late
in the in the next release of Numpy
hopefully next month
will be uh the like keyword
which allows you to actually create a
new
array just with the same
device type and same kind of format as a
so all this needs a lot of fun working
underneath the hood in Numpy to make all
these things work.
Even that is not enough so numpy
together with
the other data libraries and together
with some industrial partners
have started to set up what we're
calling a common api for arrays and
tensor Python libraries, so this will cover both
numpy and pandas type objects the pandas data
frame and the idea is to
create a common api so that anyone who
wants to create
something that can be that can
one for one replace numpy will be able
to do it
so rather than import numpy you may do
import my_fancy library
and as long as it implements all of
these api functions
you will know that it is numpy
compatible.
Okay so I hope i've convinced you that
Numpy tries to
uh be uh interoperable with a lot of
other
um libraries and tries to be a good
member of the community
and now let's actually talk about
contributing to numpy
and working with numpy.
Like most of the world numpy has moved
to Github
most of our our our activity takes place
on Github
we also have a mailing list
numpy-discussion
for bigger topics ones that can't be
neatly packaged into an issue or pull
request.
So how does that look let's take a look
at the
numpy organization on Github we have
three or four different repos we'll go
through them really quickly to see
which ones do what. So
the top um repo on in the
in the hierarchy is the actual numpy/numpy
repo. That's where the code and the
documentation for the Numpy library
live. The archive; the reason it's on top
is because that's where i put my uh
my talk just now that's where it's been
archived and that's where it's uh you
can find it
so that's why it was updated half an
hour ago um
that's an archive of all kinds of
presentations and talks and logos and
branding about numpy
numpy tutorials is a new repo that we've
started in the past six months to
actually
aggregate uh best of brand tutorials on
how to work with numpy
things we recommend and ways we
recommend that it all work.
numpy.org is the numpy website
repo and then the only other one that I
want to call out in this long list is the numpydoc
repo which holds a an extension for
sphinx.
sphinx is a way to document python
libraries. It builds a lot of the
documentation that you'll see.
If you go into Python package
documentation websites you'll see
documentations that have been built
using sphinx. numpydoc is a way to
turn docstrings from python functions
into nicely formatted  documentation.
Right, got it.
Okay, so that's how you can that's how
you kind of wander around the Github
NumPys.
How do you actually build and test and
get involved
in uh in working with numpy the library
itself
not import numpy and then working with
it but actually building it
and testing it
so numpy has a nice long contributors
guide
okay uh
it goes through the whole development
process with a summary of how to
actually create a pull request,
how to build, how to test, what kind of
stylistic things you can use, how to
build the documentations,
and then even more detail in subsequent
web pages.
But you guys are lucky i'm here so
we're going to do this together. We're
going to go through and
create a directory to work to to uh
actually build Numpy, we're going to
create a conda environment
to build Numpy, we're going to clone the
repo and we're going to actually build
Numpy.
so let's start let's start
now i've got a terminal it's a bit small
let me try and copy paste the commands
from here
because copy paste is a is a developer's
dream
and we'll copy
mkdir /tmp/dm_test
cd /tmp/dm_test.
They always say never live code,
right?
and then i want to actually create a
conda environment,
so i'm going to create a new conda
environment
called data_umbrella using python 3.8
and the paste didn't quite work this is
why they say don't live code.
It's going to take a second to actually
resolve all that
and we'll tell it to go ahead and create
that environment.
I like working in a virtual environment,
that sets my makes my code uh
makes my python environment clean
I know exactly what's in it and now
activate that environment
[Music]
okay now we've got a conda environment
activated you can see that it's called
data_umbrella
and we're gonna clone the um
the the Numpy repo git clone https://github.com/numpy/numpy
[Music]
Okay and while that clones let's go back
and look a bit at the repo
what we're actually pulling down into
this uh directory.
So if we go into Numpy this is the
director we're cloning right now
you'll see that there's a lot of
different files here
um starting with the readme itself
that asks that ask for contributions
um so among these directories
the two that are really where we like to
work in
are the doc directory and the numpy
directory
because we're going to try and build
numpy let's take a look at the
numpy directory itself. We'll dive in and
and see what it looks like
oh my goodness there's way too much here.
So, there's a whole bunch of directories
here this is a mixture of Python
and C code within it
within the uh within one one
directory structure you'll see things
like f2py which i talked about which is
a library that allows you to use Fortran
in python or random
or distutils which is a collection of
improvements
distutils so that it compiles better.
The one we care about is where the C
code actually lives because Numpy is
built in C underneath the Python a lot of it
is python but much of the
code is C and that's in the core
directory
in the source directory this is where
the actual code itself lives that we'll be
working with as numpy contributors.
Originally, Numpy had two different
structures two different uh two
different extensions that were built
they've been unified together
one is multiarray and one is umath
multiarray is the thing that holds the ndarray
so this is this is the actual code that
builds that ndarray object
It looks a bit scary but as we'll see as
we try and work through an issue,
it's not that horrible.
Okay, so we've successfully cloned Numpy
now we'll cd into the into the Github
checkout and the next thing we want to
do is build and test our new checkout of
Numpy so we do python the
the way you can build a that people
traditionally build a C extension
project within python within
the python world is with
python setup.py
Numpy has a convenience function called
runtests
that surprise surprise runs all the tests
so it builds and runs the
the tests of numpy there's different
ways you can run it this is all
documented on the website under that
contributor guideline
if you just run runtests which is what
we're going to do in just a minute
it will build and run all of the tests
that Numpy has probably around
12,000-14,000 different tests. If you run
it with a -s, it will only test
this module and if you run it with a
-t it will only test this
particular test.
Because as I said, Numpy is a C extension
module there's problems there's problems
there's
challenges when you want to build it and
test it in place. When you want to run
the actual code that you've built. So you
have this directory
and when you build the project not
necessarily
Python knows how to import it from that
directory so runtest sets everything up
in a way that you can do
runtest --ipython or runtest --python
and then it will import it will set up
your environment
so that you can import the newly built
numpy every time you build it from or
build it from build it in you
we also have benchmarks within the uh
test suite
and uh you can run the benchmarks to see
how your code has affect the performance
of Numpy.
Okay i won't go through everything that
that's in the runtest it's way too much
to go through
but let's try running it
the only argument i'll give it is show
[Music]
build and build
log which will show the compilation
as it's going ah I didn't do something, I
didn't read the instructions.
Let's go back to the instructions, what
didn't I do? I didn't install everything
we need to actually
build Numpy in our conda environment.
So let's paste that command.
There's a file that has all the
requirements, we'll install that
and now we should be ready to go.
Okay, so the first thing it does is
process Cython, which is a library that
takes python-like code and turns it into
C
and now it begins to compile the pipe
the
numpy extensions you can see it does a
lot of compiling things
while it does that we'll take one more
look at the at the uh
at the directory structure okay i said
there were two
main uh pieces of the of the code
itself of the numpy uh repo
there's the numpy code and then there's
the documentation
we take our documentation seriously we
like to have
clear and concise documentation about
everything that numpy
does this is where the documentation
lives
just like in numpy where there was a
source directory here there's also a
source directory
and the the documentation is written in a format called rst
restructured text
um and the restructured test
heavily uses
the sphinx tool to automate
a lot of the building things so if you
look at for instance uh
the index page of the of the whole
library
all you'll see is that it's got a toctree, which is a table of contents
and then it refers to other pages and
these other pages
will actually be pulled in and uh sphinx
will help us
create from this a nice html
library. So let's see how we're doing
still compiling
okay
Let's move on a bit and we'll come back
to the tests we'll come back to see how
the run run went in a little bit.
So it all looked very clean and very
easy for linux.
That's usually the way world works but
if you're on a mac os and windows
there's a few things you might have to
look out for when you're
starting to build Numpy. mac os
is pretty close to linux so it's pretty
smooth.
You may have some problems with the
accelerate library which is linear
algebra library
that Numpy by mistake will pick up. It
has bugs and Numpy won't let you let you
use it in its uh compilation so you'll have to
find a way to
neutralize that that library there's
some tips in our
developer guide. On Windows you're going
to have to install a compiler
once you've done that it should just
work
hopefully um
okay much of the code base is written in
C and it's not we don't use c++ basically because we support
some very old compilers.
As I said we try not to break things uh
that means that
because it's written in c you need to
know something about
the Python C api and how ref counting
works
ref counting is a way around
is a way around the the uh the
problem that Python has an  object
initialization and throwing things away
so objects in python live in a scope if
you're writing a python code
you'll see that the the object lives
within your little
local scope of your code and when the
object goes out
out of scope python is very clever about
destroying it.
In C, we don't have that option once you
create something in C you have to you're
the one who are responsible for destroying it or for
deleting it. Another trick that we use in
Numpy is that a lot of the C
code is actually generated either from
Python or from other code in a
templating kind of way.
If you hit that, then you'll have to
learn about it.
Building documentation; we talked about
documentation how important it is to the
Numpy ecosystem.
Because our code is self-documenting you
have to have
the version of numpy that you want to
use.
we want to actually document installed
in order to use it.
So this might be a little bit of there's
some tricks you have to learn to work
around this when you're
when you're compiling numpy and then
trying to work on the
documentation itself; the two versions
have to agree with each other.
As I said, the docstrings the the code
is self documenting so the docstrings for C extension they're injected
from Python
let's see how that works we have a
Python file oops not that one
this one we have a Python file called
add_newdocs
that adds the documentation to the C
extension modules when you import
Numpy. So let's go down see how some of
these look
if nditer probably it's not a function
most a lot of people use
but here's the documentation for nditer.
It's written in rst in this restructured text
within Python so it's got the triple
quotes to turn it into a doc string the
first line is the
high or is the one line summary of what
the function actually does
and then there's a longer summary and
then the documentation is written in
this very special
format that that numpy docstrings use
and then is parsed and turned into
pretty documentation.
Okay, let's go back and see how our test
run went
went pretty well okay it finished
compiling i'll go back i'll
scroll back up this is the end of the
compilation
and then immediately it started to run
the tests
people who have used pytest before this is
a pytest
output of all the tests that numpy is
running
and everything was green there's some
tests that are skipped
on different platforms and different
operating systems we'll use the
different testing strategies but everything ran
that that could run here and all the
test pass it just skipped out a bit on the
screen here let me see if i can
get that. There we go, pops up a bit.
We had about 13,000 tests pass in
a little over a minute 85 seconds
Okay great so
we've moved on we've looked at a bit of
code we've seen how we build numpy
now let's take a look at how you can
actually
dig out a issue or a pull request we
have about
10 minutes left to before we'll take
some questions
answers to try and look through and
find some issues you can work on.
Typical workflow in Numpy is much
like the other lectures you've heard in
in this or the other talks you've heard
in this uh series.
You want to add a failing test we do
test-driven development.
The idea behind the failing test is you
probably just take it right from the
issue, put that failing code into a test in the
proper place in the test structure,
run the test as I did and your test
should fail.
The next thing you need to do is find
out where that function is implemented
and then you have to start from there to
figure out what's wrong,
what's going on in that function that
trips the test.
Then of course you want to try and fix
it then run all the tests not just that one to make
sure you didn't break anything else.
Very important not to break things then
you can push a pr and interact with
people.
So the work doesn't end when you push
the pr, that's only really the beginning.
That's when the actual work itself
starts. Your work will get a review, a very careful
review.
Some people would call it nitpicky and
then you need to
react to the comments on that review and
push it forward until it gets through.
If it's a simple pull request maybe the
whole process could take a week or two.
If they're complicated pull requests
well, let's take a look at what happens to
complicated pull requests.
It's not easy to find good first issues
in Numpy and i'll just let's open that
up and take a look
at that while i talk about why it's not
so easy.
We have over 2,000 issues in Numpy
and about 290 open pull requests.
Now we'd be very happy to get that down
to zero on both ends
but there's a lot of reasons we don't.
If we take a look at some of these issues
and if we sort them by
at least recently updated let's say and
we look at
something that some of these issues from
six years ago or from
or from for from quite a long time ago
the reason that we haven't solved these
issues is we don't really know how.
As I said, we're very careful about not
breaking things in Numpy and a lot of
these issues
are good ideas but they would change the
way Numpy works and so we can't do them.
Same thing with the pull requests we
have pull requests that have been opened
for way too long
if I sort them by least recently updated
we can see there are pull requests from
five four years ago
that can't be done because they're
enhancements that will break things that
currently work in Numpy
or that we don't know how to do so a
good place to look for issues
is either to go to the center of the
issue
stack not the ones that are a week old
because people
jump on those pretty quick and not the
ones that are very old because the
reason they're there is there are two
that we can't fix them
but to look at ones that are maybe three
or four months old or maybe a year old.
Okay let's take a look at how if you're
the one who jumps on the issue first
how that all might how you might
actually attack it
and try and fix it
and this actually happened now we had a
new contributor come along
and pick up this issue that someone
posted
a little about three weeks ago and the
uh and we'll try and take a look at what
this person did to
push this issue and and try and fix it
so this is how an issue looks when it
first comes
through the the pipeline uh new user
user comes up and says hey something's
wrong
uh and they're trying to their best to
give a description of actually what's
wrong
so one of the first things you have to
do when you when you're triaging an
issue
is look at it and try and figure out
what's going on here
what is the person actually trying to
convey to the Numpy developers,
and one thing you might notice in this
issue is that it
it's not quite formatted correctly.
The user doesn't
actually didn't actually use the
Github markdown
code formatting format to format their
issue and so let's help them out that's
something we can do as a triage is to
reformat their comments and now
we can actually see what what the
problem is what's going on here.
Okay, they do import numpy as np
that's pretty clear
print out the version
that's one eighteen five
and then they do arr3=np.arange(start=5) 
and they print out array3
so that would be this lin.e
Anybody see anything strange here? See
what the problem is?
Okay, we asked for start=5
what Numpy did was stop=5.
Well that looks bad. Okay, if I ask for
stop=8,
then Numpy will um output an error
that the required argument start is
missing.
If you don't put anything in arange, if
we go over to the documentation look at
it I don't want to do that because i
don't want to make you guys dizzy with
flipping all my tabs around all the time,
you'll see that you can do arange open
parentheses close parentheses with
nothing in the middle
and it will um also yell at you that
that the
uh that the start argument is missing
but if you put in one number
arange(8) for instance that we will get
that will get translated to stop
and that will print out 0 1 2 3 4 5 6 7, eight values.
Okay, so we've kind of understood what
this issue is about there's two problems
here. One
is that for some reason start is being
interpreted as stop
and the other less critical problem is
that
stop is is when stop alone is put in
there is no start equals zero.
Okay so people started commenting you'll
see how long it took for someone to
start commenting was
actually no time at all on the same day
someone had already commented and the
person
came back and and uh commented again
and then someone actually tried to look
through the code to see when this
when this broke and then uh
we discovered that actually it's not a
regression this code has been that way
for 20 years and no one's ever
discovered
so um because of this comment here that
might be a nice thing for some newcomer
to work on a newcomer actually
picked this code up and started working
on it
and we can see that because later on in
the uh issue
in the flow of the issue there's
actually a pull request here
that comes to fix this so let's take a
look at the pull request
the first thing we see in the pull
request is that it says it links back to
the
actual issue itself that's the way that
nice little link showed up in the issue
was because this
pull request actually said I fix issue
i'm related to issue 17764.
So that's pretty important when you
create a pull request,
it kind of marks your territory. It says
i'm working on this issue
please don't also submit a pull request
to fix it
okay um and what does
the pull request
actually comprise? What's in it? There are
two files that changed. Okay, we'll not
look at the let's look
first at the second file that changed,
which was the test so the first thing
that this person did was write a very
nice test
of all the different things that are
currently untested in arange.
For instance there was no test that
arange without any values
comes out clean, there was no test for
step=3 which is also an error and
uh and and so forth and so this is the
actual test for the issue that the uh
that the reporter raised um
and if you would run if we would
actually uh check out this branch
with only these tests in our in our uh
in our repo
and run the tests we would see that they
would fail. So the next thing
the person had to do was find out
where actually is arange implemented?
And i'll just go into that in two
minutes because i'm kind of running out
of time here.
But um if we go back to the code,
let's go back into the code into the
core/src/multiarray
which I said was
where most of the code lives,
there's one file that's called
multiarray module
and if we look in this file,
for arange with
double quotes around it, we'll see
that somewhere along the line way deep
in the 4,000 lines of this file there is a
dictionary that maps um names
like arange to functions uh like a
array_arange nested in theirs is
another function it's mapped to
Npyiter_nestedIters,
so let's try and see how this function
actually looks.
Is this where we want to be and i'll
just finish out this
this piece quickly by not by confusing
you too much with the c
code but by saying that well this looks
like the right place because this is
has a function in it called parse tuple
and keywords
so that's probably what's handling the
input of this function
this is the place we want to start
looking around digging around to see
where the actual bug might be.
Okay and as I said, it got complicated
quickly.
That's pretty much what i want to talk
about um
I'd like to take uh some Q&A now let's
see what we can do with that just to
summarize my goal here was hopefully not to scare
you off too much
to convince you that numpy is a nice
place to to help out with
we could use help with documentation,
tutorials, code and devops.
Anything you contribute would be welcome
and we don't have any questions so
now would be the time to ask questions
or actually have another poll i'm going
to put up another poll
where is it the cued start polling
to see how i did here if you could fill
out the poll and
tell me if you think you're interested
in contributing
if you need help contributing we can
help you out you can reach out to us
either open an issue
or comment on an issue or reach out to
us on the mailing list or in some other
way
and say i'd like to get involved i need
a little bit of help to get started
we're happy to mentor people at the
beginning and
get them started with with the project.
Yeah so that's pretty much what i wanted
to say. If there's no questions and there's uh
no comments on the chat that i missed,
Reshama, I think i'll 
uh send it back to you.
question about GDB. Could you go over
briefly ways to use GDB with numpy?
So Brian are you using windows or linux?
other
other
I can show you in Linux I can't really
show you in Windows
so did my
uh my screen made itself
smaller let me make this font bigger.
The best way to work with GDB
in linux is you actually need to build a
debug build of of Numpy.
So the way to do that
is to clean it all out
git clean xfd
that cleans out all the files that
we built
and when we where we ran build tests
before and now we're going to set up
some C
flags to do now this works on my
computer
um i've heard it doesn't work in other
places
o0 -g3
so these flags are that's a capital o
capital o and then a zero that means
don't do any optimizations
g3 means take care of all the macros
um that you want don't turn any of them
don't
inline any of the macros and show me all
of the values for
C macros so now I can I don't want to
actually
run the tests I just want to build Numpy,
so i will do
runtests.py -b
which is build only.
This will build a debug version
of Numpy and i'll answer some other
questions and i'll show you
before i show you how to get into it
while it's building.
Do we need to be familiar with C
language in order to contribute to Numpy?
You don't. It helps.
A lot of the code is written in C
and a lot of the a lot of the
kind of bent of the code reflects C
up in the python language so things like
dtypes really take a C kind of mind in
order to understand
why all of a sudden my dtype is
overflowing or my dtype isn't behaving
the way I want it to
but like I said we could use help with
documentation with tutorials
with devop kind of things as well
as uh code itself.
Would be very happy to to help people
work around i'll be
very happy also to work with people who
don't know C
and to improve our documentation and our
onboarding system so that we'll be more
friendly to people who don't know C.
Okay so but i'll go back to C
because of to answer Brian's question so
the next thing you need to do is do
gdb --args python runtests py --python
which is what i said
before is a way you can
get this whole thing to run under python
and now we've opened up a gdb
session we can tell it to run
it's now running python
under gdb okay so we've got a python
prompt we can do import numpy as np
a3=arange(start=3)
to get back to the bug
that we were looking at
never live code okay
and now we can stop if we i'm going to
hit ctrl+c
ctrl+c will bring me into the debugger
and i'll say
break at array_arange(b array_arange)
I did a tab to complete the the
line
it sets a breakpoint because I compiled
with the debug
version and now if I tell it to continue
running
no until to continue
and i'll hit that code again I have now
stopped in the debugger
at the uh array_arange function
I think that's enough with GDB for
people who know GDB,
this is enough to get you going for
people who don't they were really bored
from the past three minutes
so good
More questions...
chats i'm on linux
uh so okay someone says they use GDB
from CLion
yep and there's some other good answers
in the chat about uh
pure Python things that could be
improved
great
any more questions anymore?
Matti, this was such a great talk I
can't overstate like how informative and
useful it is
on so many levels not just for Numpy but
for Python, for
debugging, for open source, for the
history
of it all it was really just um amazing
really. Thank you so much.
Thank you i'll stop sharing my screen.
and um you know that this has actually
gotten me excited about
possibly doing a sprint with you
Great yeah like I said we really love to
to onboard new people you know even if
you on board and and you
uh go somewhere else and work on some
other library,
that's fine you know that's great yeah
that is great.
um that's sort of the you know the same
thought I have with scikit-learn where
I have organized a bunch of sprints
which is like you know this is like for
open source if you go and contribute to
another library it's still a success
so um and a lot of this information is
transferrable
with you know from one python library to
another with like slight you know
specific
tweaks um
Okay so with that i will um
I will end this. This recording um
will be made available within the next
two to five days
um there's a comment here: if you look at
our docs for contributing and find them
confusing or incomplete we would also
appreciate help there, that's from
Melissa.
um yes and actually what i will do also
is there's a bunch of links in this chat
which I have access to later so I will
copy all those links
over to you know our transcript area so
it's available for people
um when they're viewing this recording
later.
Again, thank you
MAtti and also thank you to the whole
Numpy team, I know
there were you know there were a lot of
other people um
that that you had um collaborated with
as well so thank you so much.
Yeah bunch of them were in the chat so
thanks guys for handling all the chat
during the talk.
