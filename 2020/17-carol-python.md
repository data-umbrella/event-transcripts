# Carol Willing: Contributing to Core Python

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2020/17-carol-python.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/273988042/
- Video:   https://youtu.be/Pkg-DKkObKs 
- Jupyter notebook:  N/A
- GitHub repo:  N/A
- Slides:  https://speakerdeck.com/willingc/contributing-to-core-python
- Transcriber:  ? [needs a transcriber]

## Reference Links
- Python on Discourse:  https://discuss.python.org/c/welcome/12
- Carol's PyCon 2015 talk: https://www.youtube.com/watch?v=szeo1XgmuEk
- Contributing to scikit-learn: https://www.dataumbrella.org/open-source/contributing-to-scikit-learn
- Book recommendation, High Performance Python:  https://www.oreilly.com/library/view/high-performance-python/9781492055013/


## Video


<a href="http://www.youtube.com/watch?feature=player_embedded&v=Pkg-DKkObKs" target="_blank"><img src="http://img.youtube.com/vi/Pkg-DKkObKs/0.jpg" 
alt="Carol Willing: Contributing to Core Python" width="50%" /></a>

## Transcript

hello everyone thank you for joining
our webinar for today uh thanks for
joining data umbrella
i'm gonna do a quick introduction uh
carol willing is going to do her talk
and we'll have a q a
session at the end and and this webinar
is being recorded
a little bit about me i'm a statistician
data scientist i'm the founder of data
umbrella
and i am on twitter linkedin github has
raised my s
feel free to follow me
we have a code of conduct we're
dedicated to providing harassment free
professional
respectful experience for everyone this
applies to the chat
as well um thank you for helping make
this
a welcoming and friendly community for
all of us
about data umbrella we're an inclusive
community for underrepresented persons
in data science
we welcome allies to join us and we are
a volunteer run organization
so how can you support data umbrella the
first and foremost is to follow our code
of conduct
um the second is we have a discord
community chat so
feel free to join it the link is on our
website and there you can ask questions
and answer questions as well for the
community we have an open collective
feel free to also if you want to donate
there to cover our meetup dues and other
operational costs
and we have a new initiative called you
know we're
doing transcripts for all of our talks
and
it is um the transcripts are on github
and it requires knowing some mark down
and how to submit a pr either via
terminal or github
um so check out this link github.com
data umbrella event transcripts for more
information
we also have a job board which is under
jobs.dataumbrella.org
if you are looking for a position or
just curious feel free to check it out
we have two highlighted jobs today the
first is a software engineer position at
oscar health which is based in new york
city
it's a health insurance company and
they are developing seamless technology
and provide personalized support to
members to navigate their health care
and they have some other roles open as
well so
but check it out our next job that we're
highlighting is a
machine learning engineer by development
c that they are based
in washington dc or lisbon portugal or
it can be a remote position for now and
um what they do is they're mapping
elections from afghanistan to the us
analyzing public data and economic data
and leading strategy and development
behind data.world bank
and other um other
social enterprise initiatives
um these are just uh um
just a sprinkling of what we have
available on our website there's a lot
of resources on responsibility on
accessibility on open source so
check that out on your own
we have a monthly newsletter it is
dataumbrella.substack.com so feel free
to sign up for it we only send it out
once a month so
we promise not to spam you with too much
email
we are on date umbrella is on a bunch of
different platforms under data umbrella
so depending on what your preference is
um the best place to actually be a
member is
the meetup group because that's where
all the events are posted
our website has resources we are on
twitter
we are on linkedin we are on youtube if
you want to subscribe to our channel
i will post some of these links once i
finish this
intro presentation on the chat so you
can follow it
and before we begin i just want to let
you know that next week where our
upcoming event is using streamlit for
data science with thomas fan
thomas is also a core contributor to
scikit learn
and streamlit is a way to build and
share
data apps in python and i think it's
going to be a great presentation
and i'm so glad that um thomas said yes
when i invited him and asked him
a little bit about today's speaker carol
willing
carol has an msn management from mit and
a bsc in electrical engineering from
duke university
she is a core developer of core python
she is a member of python's steering
council
for project jupiter jupiter notebook um
as
many of us have used she's on the
steering council and works as a core
developer on jupiter health and mybinder
she is also co-editor of the journal of
open source education
and she co-authored an open source book
teaching and learning with jupiter
there's a lot more that carol has
accomplished but i was running out of
space
so i will let um carol
take it over from here oh and and just
just one more thing we have a q a tab on
this platform so if you have any
questions just post them there
if you do post them on the chat it's not
a problem i can easily move them over to
q
a and if you want to upvote them um you
know
i think we'll have time to answer
everyone's questions but
feel free to upload to see what's really
um exciting and important for you
and i will hand it over to carol thanks
russian
thank you all for being here and thank
you for the sponsors
and everybody who organizes groups um
it's really important and it helps us as
an ecosystem gets stronger
i am going to start sharing my screen
hopefully and
once roshama lets me know that you guys
can see everything
then i will start
there was a little bit of a lag before
but
um okay well i'm going to assume you can
see my slide deck otherwise
um somebody please shout um so today
i'm going to talk about contributing to
core python
but i'm going to do it from the lens of
a scientist or a data scientist so it's
going to be my opinionated view
of working in all of these communities
and for those that are advanced users
you will find something useful in this
for those of you that have never
contributed to open source
you should also find a lot of really
useful stuff
as roshama went through my bio
the ending part talked about education
and using tools and that is really where
my heart
and passion is less about the technology
and more about building tools that
empower other people to do good things
in the world
and um i think our
science and data science ecosystem helps
us do that really well
so let's get started so
um yes core python and c python
are the same thing you will hear them
used interchangeably
and for all intents and purposes you can
just assume that they are actually the
same
um so for today's talk
we're going to look at this from a data
and science perspective so the primary
audience is data scientists scientists
data engineers
but other folks that might get value out
of this
are computer science compiler engineers
operating system experts language
geeks but that won't be the focus of the
talk
it will be the data folks and science
fics
okay
so contributing to core python today
i'm going to walk a little bit through
how core python is organized today
then i'm going to compare it to other
open source projects in our ecosystem of
data and science
scikit-learn is a great example of that
and then we'll talk about getting
started
and how you can go further with your
contributions to either see python
open source your local community and
more
so we had an interesting thing happened
a couple of years ago
gita van rossum who had been the
benevolent dictator for life of python
stepped down and we were faced with
having to
create a new governance for core python
and what we came up with was a small
steering council
these are the members currently who sit
on the steering council
and really we are
to sort of do and set the direction of
things that guido did
by himself in terms of organization in
the project
and direction of the project and
in specific we are tasked with
ensuring the quality and stability of
the language
moving towards contributions that are
accessible
inclusive and sustainable fostering a
stronger relationship
with the python software foundation
um continuing to facilitate the
decision-making process for
peps which are python enhancement
proposals those are
when there are large changes made to the
language or proposed to the language or
workflow
that's something that um is open for
everybody to read
and comment on and our goal is
to seek consensus both with each other
but
also the community at large because we
don't want to be
a dictator of the direction of python
so as we look at core python
what kinds of contributions are needed
lots um but i want to first step back
and look at the python software
foundation
which is a sister organization to
the core python developers
yeah and yeah sorry just we don't
we see you but we don't see your slides
uh-oh
so um maybe if you can just share again
maybe let me stop sharing and re-sharing
yeah that might that might work
ah that might work
let's see if escape will do it worked in
practice
right let's do it again
okay now you should see my whole desktop
is that correct
okay it takes just a couple of seconds
for the lag it is loading which is
good and now we can see your whole
desktop yep
and now you should be able to see the
talk yep now we can see the talk and we
can see you
okay so speed version the title of the
talk
core python opinionated guide for
scientists and data scientists yes core
python is the same thing as see
python i'm targeting this to the
scientists and data scientists and data
folks in the audience
we're going to go through a few
different ways of contributing to core
python
and beyond i started with a quick
discussion of governance or introduced
the steering council
what the steering council is responsible
for
and now back to you which contributions
does see python need and
looking at the mission of the python
software foundation
is a good place to start the python
software foundation
is a sister organization to the core
python group
and its goal is to promote protect and
advance
python the language as well as to grow
a diverse and international community of
python programmers
so as you think of making contributions
keep that in the back of your head
because those are really going to be the
most
valuable contributions
some ways you can contribute and
oftentimes people look at writing new
code as the only way to contribute
and it is a great way to contribute but
in many ways a lot of these other ways
to contribute
are equally if not more important um
when you're adding new code it's got to
be with backward compatibility
we're a 30 year old language you know
people don't are using this in
production they don't want things
breaking
maintaining security anything that you
can do to maintain the security of the
language
or improve core development workflows so
mariada has put together a lot of bots
that make our core development workflow
much easier for folks to get started
and also for github and the power of
technology to kind of help with some of
the
more tedious tasks writing and running
tests writing and editing documentation
both of those are absolutely critical to
the success of
any open source project python as well
um one huge need we have is folks to
triage
bugs for reproducibility
and um in addition to that
people to review open prs um
right now we're split um our code base
is on github
but our bug issue tracker is on
bugs.python.org
so um there's sort of an extra step
between the two
so um it it's helpful um
with uh decreasing the backlog of
uh prs and bugs for people to help
um triage and review prs and
in the last year we've actually started
a triaging team
which is in many ways a stepping stone
to core development
um and then really anything that you
do to share your knowledge with the
community
maintain projects give talks write blog
posts attend meetups
that is a contribution to core python
so congratulations you've all made your
first contribution to core python
or at least the python ecosystem
so i'm going to spend a minute comparing
the different projects and comparing and
contrasting
python versus other projects that are
younger
like jupiter matplotlibs scikit-learn
and more
so what's similar well most of these
projects
use a github workflow and with that i
mean
we host our source code on github or
gitlab and
we operate with a pull request
mindset and what that means is a pull
request is
hey i would like you to take my
code and add it to your code base
and then a maintainer will either say
yes that sounds like a great idea i
accept it
or gee could you make these um changes
and then resubmit it or in some cases
when
it's just not an appropriate
contribution we might say you know what
this would be better as a third party
project
or um another project
all projects have code review and that's
when
maintainers and core developers look
through code that's being submitted or
documentation that's being submitted
and make suggestions hopefully very
kindly
about what could be changed or improved
and many strong projects have
automated testing and continuous
integration
and it's really valuable to have that as
part of your project
because it provides sort of an
independent
view of what's going on so as a
contributor
it sort of provides you guidance okay
i've done like the correct syntax or
formatting if i'm submitting
code or documentation and
one thing that i forgot to mention but
is really important
is healthy open source projects have
not only a code of conduct but also
an onboarding guide or a developer guide
that helps
new contributors get started and helps
existing contributors build their skills
so what differs well there's a fair
amount of stuff that
differs between see python and other
data science projects like jupiter
and jupiter hub and binder that i've
been involved with
um and one of the most important or
biggest ones
is the velocity at which new features
are
added to the project python's a 30-year
language
has a long history and a lot of code
out in the wild that are being used in
production
in scientific research and as such
we can't just go and change things
as quickly as we could in
a newer project because we have more
embedded users
the other thing that's different about
core python
is it's a language that's used far
beyond just data and science so
not only do we have to status the data
satisfy the data and science community
but we also have communities around web
development sys admin
devops embedded systems
teaching and so forth
so when we look at python
we're looking at okay how do we keep
stability
and backward compatibility and security
while adding new features and in many of
these
other scientific projects it's a bit
flipped
we're looking for adding new features
while also creating you know a stable
um though often changing environment we
might
uh deprecate things which is stop
using things or offering things in a
two-year window
where python it would be much longer
could be five years could be ten years
um and then the context in which these
projects are used is also different
um see python is a tool that we use
to build things and it's a
tool that is used as a foundation
for many of these projects like jupiter
or matplotlib
to create their own project
so the stability of c python is critical
to the stability of our entire data and
science
ecosystem because what we don't want to
do when we make a new python release
is break a whole bunch of other projects
and so um yeah so that should give you a
sense
of the fact that python's going to move
a little slower
really emphasize code and quality and
security whereas some of these
scientific
and data science projects are going to
move much quicker and
you'll see a lot of change in even a
year or two years
so how do you get started contributing
or if you're already contributing how do
you continue
and perhaps grow your skills
well if you're a first time contributor
to open source
i want to strongly encourage you to
consider making your first contribution
be a contribution to a project in the
scientific
data science community and i'm going to
go
so far since it's my opinionated talk to
say
i would encourage you to do that
over making c python your first
contribution and the reason why is
you will find going back to the
differences between
the projects and python language the
velocity of change is much higher
in these projects like scikit-learn so
it actually winds up
being a way to learn
while doing and make an impact
while you're learning which is much
harder to do
in see python and i
highly encourage you to go watch both of
these or read the transcripts
they're excellent so
as you get ready to contribute
to see python and this would apply to
most open source projects as well
you want to kind of get into a mindset
that will set you up for success
and one of the first things you can do
is sort of
check your intent or
really identify why you want to
contribute
um and the reason i say that is when
things get bumpy
along the way um it's easier to
persist in the process when you
have clear goals of what you're trying
to accomplish
and why and i would
encourage you to think about your
initial impact
and initial scope keep it small
it's much easier to start small and then
work up to big
and i want to also say that
patience is probably one of the best
things that
you can have along with communication
skills
in open source most projects
are run by volunteers the vast majority
of core developers foresee python
are volunteers all the stuff i do is
as a volunteer on my time notable gives
me
a lot more latitude than most companies
to work on open source but it's not my
primary
job and there's less than
a handful of folks within the core
development team where it is their
primary job
all right so you've got the right
mindset you're setting yourself up for
success
what are some of the common reasons that
people contribute to open
source and these are just a few of many
you're using a project whether it's a
scientific python project
and you hit a bug and that bug possibly
is related to something in c python so
you might want to fix
something in c python to make your other
project
run better you might
have come across something that
perplexed you
or was complicated to learn so you might
want to improve the documentation so the
next person doesn't have to go through
the same
process a lot of people just think it
would be cool to contribute to python
which is
a totally valid reason um
many people want to just understand more
about how things work
and um to strengthen
their development skills so this is just
a small subset
but um some things that come up time and
again
so your most important research
resource when contributing to core
python is what we call the dev guide
um and it's located at
devguidepython.org
it is a comprehensive
guide to contributing to python um
and it's maintained by the core
developers that also maintain the
language
it is pretty much everything you ever
wanted to know about contributing
to python and then some as
such there is a quick reference guide
which
is really a great place to start and
we'll talk about it um
in a little bit but there's also things
about
how to submit a pull request how to get
help
how to run tests and many other
resources so
this is sort of your one stop if you
will um
towards getting started and many other
projects have something
similar perhaps not as long but um yeah
so some other helpful prerequisites
that will improve your contribution
experience to see python
is to take a little time to understand
see python's culture
and
that can be um
there are there's different aspects of
the culture
because we have people that have
you know been with the python language
for 30 years
versus are relatively new in the last
five years to
core python you're going to have people
with different perspectives
and different work styles within the
language
personally i spend a lot of time
looking at discourse which is
discussed.python.org
and less time looking at mailing lists
partially because i find more value in
discourse than in the mailing list
but there's a lot of core developers
that do the reverse so
um and then i also spend a lot of time
looking at
the pull requests and the code itself
so understanding the culture and where
to find information
and how the pace at which things
happen is really important
also understanding the difference
between the core
language and the standard library
the core language is a smaller subset of
what
you would think of as core python and
then the standard library is
actually many other smaller libraries
that provide additional functions that
gave python the batteries included um
name and um core python core lang the
core language is really things like data
types
and really the fundamentals that you
would have in any
software development language again
i can't reiterate enough that core
developers
are volunteers and um
be kind um many of us are wearing many
different hats
on the flip side the core developers
should be kind to you
as well so we do have a code of conduct
and
you know i encourage you if you're
seeing behavior that is not
professional please let folks know
um understanding git and github workflow
is i think very important for
contributing to
core python at the point where people
are contributing to core python
the general assumption in the community
is that you have
um basic git and github workflow
experience and understanding
and if you jump back to where i said
oh i i am encouraging you to
also consider contributing to other data
science and science libraries
partially it's because those projects
tend to be a little bit
gentler with new contributors that are
still learning git
and github and there's
lots of information out there about
doing it um
software carpentry or the carpentries
have a great guide
and um there's a talk which maybe we can
link to
in the future unfortunately it wasn't
recorded but a slide deck
that i put together gosh probably 2016
for complete beginners at writespeak
code
who are learning git and github and it
really
is a very gentle introduction to both
but um
has been very popular and then
the other prerequisite is some
familiarity of python
um it's not necessary to know c it's not
necessarily to know c
plus so most of the language is written
in python
so you can be very effective without
really understanding much if at all
from c or c plus plus
so that's a lot to digest
and i wanna um for those of you that
want a great exercise um later
or when you're ready um i wanna
just give you the brief directions on
how to build
core python from source and
um people often think it's a really
super complicated process and
um the quick reference guide in the dev
guide
actually runs through these steps
there may be some subtleties based on
the operating system that you're running
but essentially what you're going to do
is
fork and clone the source code from
github which is at python c python
then you're going to use a c compiler
and most of the time c compiler is kind
of available with your operating system
to configure and build python um
it's one command to configure and build
it
with unix linux and mac
um make is what will actually
do the actual building
and then windows there's a
bat file that combines those same steps
so
to configure and build python is one
step
so what would you want to do as you're
starting well
a good place is just to run the tests
and
again like building and config
and configuring python it's one
line of code and there are
this should look pretty familiar with
folks that have done python
it's just basically executing the test
library so um
there you go you have now learned how to
build
configure and run tests for python
um the dev guide will definitely give
you
additional questions and answers on how
to
contribute um again remember
changes to the language are submitted as
github pull requests
our continuous integration will run
the automated tests just like you're
running them locally
it will run them in an automated way
across all
operating systems and a number of
different versions of python
the next step in the process if you
submit a pr
would be to wait for some review from a
core developer or
a contributor address the feedback
as appropriate and hopefully then
you will have a final core developer
review
and if luck will have it um it'll be
merged into the code base
and um folks can use it from then on
for those of you that want to go deeper
in your understanding of see python
there is a wonderful blog post
which is now a book by anthony shaw
about a guide to see python source code
it is the most accessible yet highly
technical
um explanation of how see python
works um you know down to the
lowest levels um in fact it was so good
that when it first came out
i took the entire uh blog post
copied it all had it bound
um in a spiral you know thing
so that i could refer to it on a
day-to-day basis and
i encouraged anthony to write a book
based on it and he did
so we're very lucky that there's many
ways of accessing his materials and he's
also
a very prolific speaker
so there's lots of stuff on youtube as
well
another great resource um
for learning about python i don't know
if you can see
me or if you're just seeing my slides
but there is a book
called high performance python by misha
gorlach
and ian oswald and it is um
i think an outstanding book for
uh both learning python and how it
is built and comes together but also
the things you can do to improve
the performance of python um
one of the things you might hear in the
media is python is slow
python you know isn't performant because
there is this global interpreter lock or
gill
and the global interpreter lock or gill
what it does is it
limits at certain points the
processing to one
thread if you will at a time and
that tends to be a bottleneck because
right now we have many multi-core
processors and things like that
you'd want to use all that and not have
to bottleneck
into things but this high performance
python it runs through things like
how to profile your code how to
use multi-processing how to use cython
which is a great project in our
ecosystem
in terms of that allows us to do a lot
of more
cpu intensive stuff i believe it also
covers number
which is also another great project that
kind of
uh uses just entire time compilation
to get around the gill
so yeah there's lots of ways you can
improve your performance
and these two resources are just some of
the many that are out there
in addition to those resources um there
are
many core developers keep websites that
have a lot of um
technical content victor stinner brett
cannon and
guido a lot of historical information
from guido as well
much like the sprints that have been
held for scikit-learn
see python typically runs sprints when
we have
in-person conferences which sadly um
2020 but you know
the hope is that there will be some
being done
virtually and um you know if anybody
wants to run the c python sprint let me
know i'd be happy to kind of help
guide you with that um many of the
python
python talks both um from pycon us
and beyond um explain how to contribute
to core python
i think my python talk from 2015 was how
to contribute to core python when you're
not a core developer
mariada's given great talks about
contributing
both to the language and to the workflow
of victor stinner
and for those of you that have any
interest in
asynchronous programming lucas has
a great series on youtube about async io
i think it's about seven parts and um
it's a really great introduction so
we can always use help from folks that
are interested in asynchronous
and this is just a small subset maybe a
third of the core developers
as volunteers our time is limited
but the community is key and it's what
lets python both as a language
and ecosystem thrive
so i want to encourage you to go forward
and contribute join the discussion on
discourse which is discuss
python.org and whether you're
contributing to python
or any of the projects in the ecosystem
you are creating real change
and helping others solve important
progress
problems in the world so i want to thank
you for listening to me
and um thank you to roshama and the
organizers and
i'm going to shut off my screen
this is already available on speaker
deck
and it will be available through data
umbrella
as well
and i am happy
to take any questions that
might have come up okay so um there's a
question about the slide so i will find
all right
speaker deck for that um
speaker deck okay um
so the next question is is the need to
reproduce
old bugs against the newest version of
three nine in need
of the project
depends on how old the bug is um if the
bug is like within two years old
i'd say yeah it's probably useful to
reproduce those if
in general my view and it's strictly my
view it's not a
official view in any way or shape or
form personally
i would close the vast majority of
issues
that are over let's say three years old
and because they're still accessible
to people to find if needed
but the likelihood of them being worked
on i think is fairly low
um uh we are going
to move the issue tracker to github um
there is work in process to do so
um and that should make
the whole process more streamlined and
it will let us do some things
with notebooks and some of the tools
that we have in our
ecosystem to help surface issues that
haven't been looked at to help recognize
contributors there's many different
things we can do
with the data that is available within
the repo
hopefully that answers the question
okay uh the next question is g-i-l is a
problem but the advice i've seen is
avoid being limited to one core is to
use
multi-processing over threads
okay so there's a lot of different
perspectives
and um the gil or gill
which is the global interpreter lock
there are different ways of
getting performance that um
gets around the limitations of the
global interpreter lock
multi-processing is a great way
i would say threads would not be my
first choice
in how to do that but things like cython
number you know depending on the use
case
async io but yeah it's a great question
and the resources that i mention
particularly high performance python
will give you excellent advice on how to
get the most
out of your deployments in a safe and
efficient way
okay and the next question is what is
the best way to attract a mentor from
the core
team does the project have a formal
process for being mentored
so there is a core mentorship
mailing list which used to be more
active right now
mentors you know because we're all
volunteers
people mentor as they are able to
i typically my mentoring is basically
being welcoming and answering questions
that people directly ask me
um i just don't have the time and
bandwidth to mentor individuals
but um one of the things that
we do have is the triage team so if
you've been involved for a while
somebody may ask you hey do you want to
join the triage team
and the triage team you know it has some
additional
capabilities they can do things like um
make comments uh or attach labels to
different issues
and that's really a great way that
recently folks have found mentors
as a result of the work that they were
doing within triage
and then victor stenner has been really
great at mentoring folks
as well as you know barry raymond hedger
you know there's a lot of people that do
eric snow
um pablo salgado who's our
release manager for 310 and 311 have
also mentored fix
and victor's got a lot of writing on it
so hopefully that helps
and feel free to reach out to me
directly and
i can probably provide additional
resource what's the best way to reach
you carol
uh reshma knows this
i stink at email um
github is really the best way to at
mention me on something
but um you know my dms are open
on twitter and you know i will get to it
when i can get to it
um it's not that i don't want to respond
but the volume of stuff that comes in is
i could spend my whole day doing email
and nothing else
so um you know i
tell folks that i meet you know be
persistent
if you don't hear from me once or twice
do not hesitate to email me a third time
and i will do my best to
answer okay the next question is from
your viewpoint
what does the future hold for python for
instance for the next
30 years wow
that's 30 years i hope
that python is as vibrant today as
30 years 30 years from now as it is
today
i think in many ways
you know the whole data science
scientific
python ecosystem has been one way that
has really revitalized the language
over the last five years another place
that we're seeing
a lot of growth is in embedded systems
things like
micro python and circuit python and
uh you know that's really exciting to me
from an open hardware and education
standpoint
and and getting young folks or
folks that maybe aren't computer
scientists to start with involved
i would love to see us um
can improve the performance of the
language
um and what that will look like i'm not
entirely certain
um there's definitely going to be
efforts over the next five years to do
that
some of it is time some of it is funding
um
but i
the one thing i hope stays the same 30
years from now
is the readability of the language
and i think because python is so
readable
that actually makes it much more
accessible for folks
as well as um tools like the notebook
kind of break down and provide a good
education tool for learning more about
python so
the community is going to be the one
though that drives where python goes
and truth be told there's another
language that i also find really
interesting
that probably is relevant to many
members in this community
and that is julia it's still a very
young language
but i think it has a lot of potential
and promise
and um is very similar to python in a
lot of ways
um but gets around
issues like the gill and relies more on
c
c plus and should you ever want to
compare
julia code with python code tom
sargent's
quant econ website is excellent for
doing that
because even if you're not an economics
person it has economics code
written in python and then similar
economics code written in julia and it's
a good compare and contrast when you're
learning
so i don't know that's about all i can
say
for the future that's there's been a lot
of discussion i see going on because
o'reilly published a report too about
python and i guess speed is the thing
that's most under discussion right
um it these days you know it it's
interesting
because
oftentimes and and this has been
historically
you know i'm 54 i've been in this
industry a long time
speed has always been at the key like is
this faster than the other
is vim faster than emacs is emacs faster
than vim
um you know speed is relative
and it depends on what you're measuring
i would say one of the things that is
not often discussed and really should be
is
the speed to create
a project and python
is a really efficient language for going
from
no code to prototype to production
and there's value in that
beyond just pure processing power and
now that said there are you know
certain things that if you're cpu bound
um like high cpu operations versus io
operations and you know web is going to
be different than pure number crunching
you know your performance is going to
vary
and one of the things i think that would
be
really useful is to try out like profile
your code
look at the other tools for increasing
the speed
you know there's trade-offs regardless
of what language you use
and i encourage you to try
other languages as well there's another
question about um you mentioned the
global reach of the tech community aside
from events like this what is the role
of the python steering committee in
making the community more
inclusive so
um the steering council
has been
a part of some of the code of conduct
um decisions and discussions related to
core developers and we have this year
taking some
actions to
redirect or remove uh folks that
were probably not contributing
constructively to the community
um the so you know adopting the code of
conduct throughout the project was one
way
uh the steering council also
looks at efforts um
whether it is the
core language summit or the core
developer sprints
those used to be exclusive to only core
developers
and in more recent years we've um
invited more people to it that
to both increase the diversity on a
number of
dimensions as well as just even use
cases
my hope has long been that
diversity will benefit
from the move to github i was an early
proponent
of moving the code base to github and
have been a strong advocate for moving
the bug tracker to github
or or it could have been gitlab but
something where
the tooling is modern and is more
accessible
to more people because one of the things
i personally feel when you're an
underrepresented group
your time is more limited than if you
are in the majority so you have to pick
and choose what you work on
much more carefully and
by having a roadblock like having to
learn an
issue tracker versus using uh tooling
that you're used to from your day-to-day
work
i think that adds a barrier
to inclusion so um
[Music]
yeah so it's really trying to
shift the culture towards more inclusive
culture
mariata has done an amazing job with
that and
you know the steering council is really
there to support the efforts within the
community
and the core developers that are
interested in
moving that effort forward
also just to add you know pi ladies
which is
um you know under python software
foundation is also
connected to um
improving inclusivity in the python
space yes yes that's a great
suggestion or comment because we also
have
um within pi ladies there's the ability
to ask questions
um just like with our ladies there's an
ability to ask questions on
core development within those channels
another question here is what will be
the impact of the new
peg parser in future python tools and
libraries and maybe you could explain
what peg means to
someone like me who doesn't know um so
it's we affectionately call it the peg
parser
and when you're creating a language um
you have a grammar you know your syntax
and the language has to have a way
to sort of know okay this is a keyword
this is a variable this is an operation
things like that
and that is the job of the parser
um i believe
that the peg parser will give us more
flexibility over time
it is probably equally as performant as
the prior parser and there was a lot of
extensive testing
done during an entire release cycle to
make sure
that you know
it wasn't introducing weird regressions
and things like that
but one of the things it is much easier
to write grammar
rules now with the peg parser than it
was
with um the old parser that we have
so hopefully that ans answered a little
bit what it is
and uh why it is and
and someone who can provide far more
answers than i would be pablo salgado
and um do reach out to him he's probably
got some talks on the peg parser as well
and one last question which is i heard a
talk that is a twist
on the speed demand instead of focusing
developer time
expertise on on optimizing to a
capital o one go with n squared
performance because developer time is
more expensive than ram is what are your
thoughts on that
um i i think it really
comes back to use cases and
um i think the difficulty with python is
because we serve so many different
communities
what is optimal for one community may
not
be optimal for other communities um
so you know it's an approach
is it the approach i don't know
to be really honest it wouldn't be my
first approach
i guess is what i'm saying okay
so with that we are reaching the top of
the hour
and so um thank you so much carol for
taking the time to join us and sharing
about core python
um i have a link to the slides i put
them in the chat and i'll include them
in the video when it's uploaded to
youtube
and there's a bunch of links to
that you've mentioned which i've been
putting in chat and i will link to it in
the
you know youtube description or
somewhere very convenient
um yeah thank you so much great thank
you and thank you everybody for
attending i hope you learned
something about contributing to open
source and i hope you
you do so as you're ready to do it
thank you
