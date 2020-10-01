# Matt Brems:  Data Science with Missing Data

video:  https://youtu.be/LJKYXq3WHTw


Oh
you
you
you
you
if you have a
you can use the QA function so if you're
on zoom and you hover over the video it
should be on the bottom below the video
it looks like QA and you can ask
questions there and then we'll spend
some time to answer them we do a break
in the middle of the talk and then at
the end of the talk as well
you
hey Matt I saw you just logged in are
you good to go
yeah good to go whenever you are cool
yeah I just I'll just do a quick intro
talk about the meetup group talk about
Gao take like two minutes I'll start at
6:05 and then you can hop into your
presentation sounds good
how's the new gig it's going pretty well
week two yeah no no complaints yet it's
been dropped a little bit into the deep
end but that's okay what I was sort of
looking for yeah is it what's it like on
boarding during a pandemic so in my
current role worst of it it's
interesting secondly there wasn't a ton
of onboarding there's a there's a bunch
of stuff that I have to do kind of all
on my own time you know compliance and
all of that but there hasn't been a ton
of onboarding so I don't know if that's
just the nature of me joining in the
middle of this project or something else
but yeah I know I know about six
different people and that's about it
okay yeah that's interesting it's it's
weird because in a sense like remote
work or this environment we're in you
cut a lot of the flow cut a lot of
things and I guess some people might
think they're fluff or not but right
like a lot of the stuff you do the first
day at work or the first week it's like
meeting people you know all sorts of
meetings and things like that that may
or may not have to do with actually the
lauric you have to do but they're just
like work culture events right and so it
looks like some companies are just
cutting it out and you know it's just
like whatever
yeah it's it'll be interesting when we
have to start going back into the
officer rather if we we have to do that
what things will look like then if there
will be a like a retro onboarding or
anything like that yeah well a lot of
uncertainty there is FINRA like I don't
know like the culture at FINRA is it
like very much like when the government
opens they will
open up because I know in New York City
you know like officers opened up and
obviously companies like GA and other
tech companies are like let's let's hold
back but I have some friends that work
in investment banks they have to like
show up to work next week like full time
we we haven't gotten anything about that
yet I think we're following the to my
knowledge and what I've heard we're
following the like the schools in DC so
I didn't schedule we'll see but haven't
heard anything yet so I I would be
surprised if we go back before like
August 15 just based on where we are now
but who knows okay well we have like we
have yeah we still gonna come people
tricking in but I'll just start my intro
this can everyone can you see my whole
screen now yep okay sometimes I forget
if you go fullscreen and Google Chrome
so thanks everyone for attending during
these uncertain times I hope you'll get
as much out of this talk as I'm planning
to so the talk is called good fast cheap
how to do data science with missing data
and Matt brems will actually be leading
the talk I'm just here to do an intro
and moderate and login to my zoom
account so just a quick agenda we're
gonna do an intro I'm just gonna
introduce Matt I'm gonna introduce kind
of our sponsors and the meetup group and
then we will open up for Q&A as I
mentioned before zoom has like a
built-in Q&A function so if you hover
over this video with your mouse on the
bottom below the video you'll see a
things called Q&A so you can ask
questions directly there this will be
recorded it will send it'll be sent out
and in a couple days so so call it two
or three days automatically by the GA
team if you do not get the recording for
some reason it could be in your spam box
but otherwise just email your local GA
kind of
campus and and they'll be able to sort
it out or they'll just email me and then
I'll email them they're recording so
Matt brems is the speaker he actually
just moved to FINRA maybe like two weeks
ago but before that he was at the global
instructor for GA Zeta Science immersive
program across the United States and
before that he was working in the
political consulting realm and if you
want to follow him on Twitter his symbol
is or his tag his handle is Matthew
brems I wasn't able to figure all by oh
it was you know it's too long for the
slide and then the event is run by data
umbrella so the mission of data
umbrellas provide a welcoming and
educational space for you our G's or
underrepresented groups in the fields of
data science and machine learning you
can learn about upcoming events and the
mission at data umbrella org and you can
follow them at data umbrella on Twitter
data umbrella is running weekly events
during this time like weekly virtual
events so if you check the page there'll
be another really interesting data
science event within the next seven to
ten days call it pi ladies is also a
co-sponsor it's the New York City
chapter of a large national group so
it's a group for python ladies and nine
non-binary people of all levels of
programming experience and you can check
the home page of the national
organization pi ladies calm and then
their Twitter handle is NYC PI ladies
and then last but not least the company
where I work at and where I met Matt
brims and is letting us borrow their
webinar zoom account is General Assembly
so General Assembly is a pioneer in the
education and career transformation
space specializing in today's most
in-demand skills so the homepage is
General Assembly or General Assembly Y
and then the Twitter handle is at GA we
run a lot of cool classes and tech data
marketing product management if you're
interested in learning
the classes you can also ask questions
to me I can I can help sort that out but
without further ado we will move on to
Matt's talk awesome just stop staring my
screen and then you can yours yeah I'll
go ahead and start sharing my screen as
well good evening everybody
like liked I shared my name is Matt
friends I use he/him pronouns I'll go
ahead and share my screen here so
hopefully you'll be able to see it I
dropped in the I dropped it in the chat
box a link to github where you can find
my content so if you would like to
follow along you're certainly welcome to
I've got I'll be focusing exclusively on
slides here
however in in the repository there are
in the repository there's code and it
will clear breaks in the code show when
you can that show kind of when we'll be
shifting from one slide to the next and
where the code sort of fills in the
blank I'm seeing that this is not
sharing so let me actually tie really
quickly are you able to see my slides so
no it just says Matt brands has started
screen sharing okay well let me go ahead
and restart sharing that I appreciate
folks as patience here with this this is
my first time setting up this my first
time using this iPad I switched iPad
since they no longer I'm using my GA one
so we will let's see
yeah if everyone's wondering the slides
from this presentation are in that link
that Matt shared in the chat and that
could help others PDF right so this is
not working so what I'm gonna do I've
got the slides on Google slides so I'll
just go ahead and use the Google slides
version and edit through that instead of
instead of working on my iPad so I will
not get to use my my stylus that that is
that is okay so let me stop sharing that
and I will go ahead and reshare my
screen here again appreciate folks is
patience with this Oh were you trying to
cast your iPad into the zoom yeah I've
got a okay yeah I've got it
nice desktop thank you uh you would be
able to see my screen now my Google
slides have not pulled up can you see
him yep we can say it now okay I saw a
face light up so imagine that yeah that
that's coming through now so I won't be
able to annotate with my with my Apple
pencil but but that's okay so thank you
very much time thank you very much
everybody for for having me join like I
mentioned my name is Matt friends I use
he in pronouns and what I'm here to talk
with you about is how to do data science
with missing data this is a really
challenging problem to work within to
try and grapple with but I think it's an
important topic because if you do data
science you have inevitably run into
challenges with missing data or missing
information and the ways that we try and
handle that probably are not the ways
that we should be handling that so I've
got some stuff here you can see this in
the slides ty has already talked about
my background so I'll go ahead and skip
beyond this you're welcome to to hit me
up afterward if you'd like to talk about
any of these experiences but the lay of
the land for tonight so we're gonna
start by talking about missing data
we'll get into strategies for doing data
science with missing data and provided
that we've got time we're gonna wrap up
with some practical considerations and
warnings for you to keep in mind as this
goes on please feel free to at any
moment drop notes in the slack or in the
zoom channel so I will keep an eye on
that as well as the Q&A so at
any point feel free to do that to drop
stuff in there and I'll try and respond
kind of in real time
so how big of a problem is missing data
and this is just gonna be the the very
quick start of it it's a really
challenging question for us to answer
because what's going to happen when we
are trying to work with missing data we
try and quantify how big of a problem it
is is that from a practical point of
view and it sounds trivial to say this
we can only see what we observe so we're
only going to be able to actually see
the data that we've gathered we don't
know the value of that missing thing
itself so the only way for us to be able
to quantify or understand the magnitude
of how big of a problem missing data is
is there we can use simulated data to
try and help and answer that question
now in the interest of time we're not
going to go through actually generating
the simulated data and looking at this
but if I move forward to this slide if
you would like to check this out all of
the code is pre-written for you in the
notebook and in the so in the repository
I've got three different sets of
notebooks
there's one with a prefix 0 0 1 with a
prefix 0 1 and one with a prefix 0 2 so
you can run that on your own if you
would like but in short what you would
see at that notebook is we create some
data or we generate a complete data set
and then we take 20% of those
observations and turn them off or we set
those to be missing and we see how much
of an impact that would have on our
model if and what we notice is that if
we were to look at the slope and the
y-intercept of our simple linear
regression model there's actually a
really really really large effect and so
that is a quick way for us to try and
quantify how bad or how big of a problem
missing data is now that depends on a
whole host of factors how much data do
you have what is the type of missing
data that you're dealing with how what
type of model are you trying to fit how
many variables do you have all sorts of
things factored into that but in a very
very simple case we can see that missing
data is really going to undermine a lot
of our inferences and the conclusions
that we may try to make
so this brings me to what I want to get
into which is what is a realistic
approach for us so if you're familiar
with the good fast cheap idea in project
management what that means is that you
can come up with a project that is good
and fast and if you come up with a
project that is good and fast what's
going to end up happening is it's not
gonna be cheap that is it will be more
expensive to be able to do that project
because if somebody wants something done
quickly and wants something done well
people will probably have to pay top
dollar for that on the other hand you
can think about a good and cheap project
so sometimes people will say hey I need
a project that is high quality and they
don't want to pay a ton of money for it
and that's a very realistic scenario to
come up but the challenge is if
somebody's not willing to invest in it
and you want something that's high
quality generally that will take a large
amount of time in order to deliver that
solution so here we see the overlap
between good and cheap is that it will
take time to deliver and then finally at
the bottom here we see fast and cheap
most frequently in my personal
experience people will say hey I want to
pay this low dollar amount for a project
and I need it done tomorrow well what's
gonna happen is is that if something is
done fast and that something is done on
the cheap it's not going to be the best
quality in most cases so because of that
we need to think about how can we take
this approach and apply it to - missing
data the reason that I bring this up is
that oftentimes what clients or managers
or anybody else once they will say I
want something that is good and fast and
cheap but that's not going to be
feasible connecting this directly with
missing data we think about what missing
data means in terms of a fast and cheap
analysis that's going to be you just
drop all of your missing values or you
do a single imputation
if you want an analysis that is done
well and is fairly inexpensive then you
have to fill in your missing values or
handle missing data in what I would call
the proper way so we can talk about
proper imputation or the pattern sub
model approach and then finally and
we'll get into what those means shortly
and then finally if you want an analysis
that's good and your analysis to be very
quick then you should gather your data
in a complete manner the downside of
that of course is it's incredibly
expensive to do that you have to figure
out how can you collect complete data
without missing any data and oftentimes
you have to pay top dollar for that
something that might be a hard sell for
when you're talking with your boss or
your client or somebody else so I'm not
I what you should come away from this
evening is not this is the specific way
I need to always handle my missing data
but get a better understanding of what
are the trade-offs and missing data what
are the different challenges in are the
trade-offs if I go with one approach
versus another approach so given that
introduction what I'd like to do is talk
about what are strategies for doing data
science with missing data so the first
thing to do is let's talk about how to
avoid missing data so something that I
think is really important to note is
that it's usually going to be more
expensive up front but cheaper in the
long run to avoid missing data so as you
think and this is probably the this is
not the best way of going about best way
trying to come up with the right phrase
for it this is not the this is not the
fanciest or coolest approach to missing
data for me to spend time to talk about
avoiding missing data you're like yeah
like okay I know that it's better for us
to collect data as opposed to collect
data that is missing and I get that but
it's important to talk about this
because oftentimes in the long run it's
going to be a better thing for you to
avoid that missing data upfront
depending on the jobs you have were the
jobs you want to have if you're working
in an organization where you're
gathering survey data or you're working
to collect data in some capacity
if you have any control over that there
may be small to moderate design changes
that can be implemented there that
allowed to gather significantly more
data if you gather more data you don't
have to invest time in how to handle
that missing data later you can just use
the entirety of your data if you've got
more data your inferences and your
predictions and everything tend to be
more precise your variance is lower and
so because of all of this it's often
better for us to try and avoid missing
data upfront if we can so I want to take
a moment to talk very briefly about some
of these again you can read all of these
on your screen but some of the things
that I think about our for example
decreasing the burden on your respondent
or minimizing the number of questions
somebody has to respond I responded to
two surveys earlier today I'm Survey
Monkey a former colleague had posted
some stuff on LinkedIn and I filled
those out and they were I was willing to
do it even on my phone because they were
relatively short surveys I like the
beach Chipotle app I eat from Chipotle
quite frequently and up until actually
like last week what they would do is if
you ordered online through the app they
would follow up about an hour later with
a green smiley face or a red frowny face
and say hey how was your dinner this
evening
and you could click that smiley face or
the frowning face and if you click the
smiley face they said hey thank you so
much if you click the frowny face you
got to put a couple of checkboxes and
say this is what I this is what I didn't
like or this was this was not
satisfactory and that was it so many
other organizations there were so many
other data collection mechanisms end up
requiring you to fill out 20 30 40 50
questions and so what ends up happening
is that you often will create missing
data by the design of what you're
looking at is opposed to any anything
else
so making some changes on how you can
decrease the burden on your respondent
maybe making questions closed-ended
instead of open-ended like like a fill
in the blank question
one other note that I want to make here
is thinking about in groups thinking
about improving accessibility that's a
very very important point so there are
lots of different ways you can get into
this we can think about language
accessibility we can think about
readability we can think about
individuals who may be hard of hearing
and ways to gather data from individuals
but it's important to think about
accessibility and inclusivity when we
design that so if you are part of an
organization where you are gathering
data in some capacity is there a way to
improve that accessibility to others for
example when I was doing polling and
surveys in the context of politics we
would administer surveys in multiple
languages specifically English and
Spanish when we were calling different
populations or specifically different
states that had a a particularly large
Hispanic population or spanish-speaking
population that was something that we
wanted to do because otherwise we were
just leaving out broad swaths of the
population which would of course down
the road compromise our inferences so
you can make a compelling business case
for doing something like this it's not I
mean accessibility in my opinion is in
and of itself a valuable goal in
addition to that I think that it's
important to recognize that when
attempting to encourage other people or
share with other people that they should
take some action or invest some funds or
some energy in that that there are some
positive business effects to it as well
moving onto the next slide so we talked
about avoiding missing data how do we
ignore missing data well the very very
short summary is that we're going to
assume that any observation that we've
observed is similar to those
observations for which we are missing
data when we ignore we're making an
implicit assumption which may or may not
be a valid thing to do when I was in
grad school a professor shared that a
very general rough guideline is that if
you are missing less than five percent
of all of your data you may be okay
ignoring that data that's missing now if
you are trying to do something like
supervised learning you fit a model
where you've got a bunch of inputs and
an output your Y variable if you're
missing a ton of data from your Y
variable
then even if you're missing less than 5%
of your data overall that may compromise
your inferences too much you may not be
willing to do that or if there are
certain variables that you know were
believed to be really meaningful and
you're missing a lot of data from those
maybe ignoring missing data isn't the
right way to go now when we ignore
missing data effectively it's what most
software's are going to do by default in
our in Python in something else if you
just put your data into your model and
press GO
or dot fit or whatever it is you choose
to do if you were to do that and didn't
handle your missing data in some
capacity or in some way then you're
probably going to that's effectively
ignoring it your model or your software
is almost certainly going to drop all of
your observations that contain one or
more missing values in it and that may
be okay to do if that number is
relatively small but I want to emphasize
up here there is an assumption that you
are making with that and that may or may
not be a valid assumption to make
so the last thing that I want to talk
about is how to account for missing data
I mentioned how to avoid missing data
upfront if you can't avoid it you might
say can I ignore it well here before we
account for MIT and if we can't ignore
it then we have to account for it but
before getting into that I want to shift
our mindset a little bit because there
is a a belief that we can just plug in
those gaps in our data that you know and
perhaps you were perhaps someone
expected that you would be able to come
here tonight and I would give you a new
Python package that allows you to fill
in missing data and and you've got that
technique you can put in your work flow
and in your wallet and kind of move on
your way but the problem with that is
that you have to do this in a specific
way or we're really just making up data
and making up data has all sorts of
issues a we might be wrong be it's not a
an ethical thing to do in my opinion and
so because of this we need to be very
careful about how we would fill in some
of those gaps or how we how we tackle
missing data but I like to shift our
mindset a little bit and say in most
cases we're not really fixing missing
data it's not like we just have this as
a new step in our workflow where I fit
some some method in pandas or in
scikit-learn and then move on with the
rest of my day we're really just
learning how to cope with missing data
so given that shift in our mindset that
we're really just learning how to
effectively and in a principled way cope
with our missing data let's move beyond
this so we want to talk about how to
account for missing data and there is
code in the repository to go through
both unit missingness and item
missingness so I want to I want to share
that with you and that's again in the
repository if you'd like to take a look
one note that I want to make is please
again feel free to drop questions in the
chat if there are questions that you
have because I want to make sure that I
can answer them as we go I really want
this to be as helpful as possible for
for each so let's talk about unit and
item missingness there are a couple of
different ways that data can be missing
unit missingness is where we're missing
all of our values from one observation
so for example here index 3 if I'm
gathering data on individuals and let's
say that person 3 just did not respond
to my survey or for whatever reason I
have no information from this person if
I have n A's for all of those that would
be an example of unit missingness this
person did not share their information
with me and so I have no information
item missingness or I like to refer to
it as Swiss cheese missing this is where
there are holes in your data so indices
1 2 in 10,000 have this for example for
index 1 we do not have information on
age or income but we do have information
on sex here for individual 2 or index 2
we do not have sex but we do have access
to age and income data and then all the
way down to row 10,000 we're missing one
value here in the income
so the way that we handle unit and item
missingness is a little bit different so
in terms of unit missingness the very
very quick summary of how to handle unit
missingness and i am let me actually go
ahead and pull up this notebook just to
very quickly show what this looks like
I'm gonna go ahead and pull open this
jupiter notebook if you do not have
jupiter notebook on your computer or if
you're not familiar with python or
anything like that that's okay
i'm probably only gonna spend about two
to three minutes talking about this but
do want to pull this up as an example
so when we are that is item missing this
what I meant to do is pull up the unit
missing this one I grabbed the wrong one
so I apologize I'm gonna move back over
here I'm going to go ahead and shut that
down and open up the jupiter notebook 0
1 unit missing this
you
and I'll drop that in the chat here zero
one unit missing this IP Y and B which
can be found in that repository in my
experience the most common method of
handling unit missingness where we're
missing an entire row of data is if we
have supplemental data on that
individual to do something called weight
class adjustments where we take our
observations and we break them into
classes and then we will weight them
before doing our analysis so for example
let's say that I'm working in HR
analytics so I'm working in human
resources and I want to understand how
satisfied are individuals within our
organization let's say that to make this
simple we have two different departments
we have a finance department and an
accounting department for which I want
to study individuals and let's say that
maybe when I administer these surveys
that in the finance and accounting team
they're split perfectly evenly got 50%
of people in finance 50% of people in
accounting but let's say that maybe
people in finance had too much other
stuff to do or were less responsible or
whatever kind of motivation you want to
ascribe to that and let's say that
people in finance were less likely to
respond to my survey and let's say that
people in accounting whether it's
because they had less on their plate
they're more organized they're more
conscientious of this they just wanted
to reply whatever else let's say that
accounting people responded more to my
server and so because of this if I
scroll down here what we're going to do
is we're going to see that if I look at
all of my survey responses so let's say
I administer this survey 50% of people
are in accounting 50% of people are in
finance but when I get my surveys back I
get a disproportionate number of
responses in the accounting department
here about 77% of my responses are in
accounting meaning that only about 22 or
23 percent of my responses are in
finance well if
I was going to just take these values
and I was just gonna do a simple average
to understand on average how happy are
my employees I might be putting some
additional bias in my model here and
that bias may come in because I received
way more responses from accounting than
from Finance so what I would like to do
the strategy that we can employ is
something called a weight class
adjustment where I'm going to basically
down weight all of my people from
accounting I'm going to up weight all of
my respondents from finance and what
that's going to do is going to put them
back on an equal playing field because
again 50% of people were in finance and
50% of people were in accounting so the
way that we do that is we take our full
sample of people do all of the 100
percent of people who we administered
those surveys to both the observed and
the missing we're going to lump them all
together and we break them into
subgroups based on characteristics that
we know in this case I know accounting
and finance I'm going to give every
individual a weight as well so the
weight for people in group I is going to
be what's the true percentage of people
in that group divided by what's the
percentage of observed responses in that
group so for example in the accounting
group the true percentage of people who
were in accounting is 1/2 divided by the
percentage of responses from accounting
which was as we saw appear about 77% I
let Python do the math and so the weight
for each accounting vote is about 64
point six percent
I do the exact same thing for finance
and what that means is that each finance
though gets a weight of 2.2 so for every
finance person this is finance and this
is accounting every single finance
person who replied they get a vote
that's 2.2 times so one person submits a
survey I'm gonna up with them 2.2 times
for every accounting person who
responded instead of each person getting
one vote they effectively get point six
four five votes if we want to take the
weights in each of those groups and
multiply that by the number of responses
that we get that ends up equalizing
things so that the total weight from all
of my accounting responses and the total
weight from all of my finance responses
end up being equal or in this case
almost exactly equal once you have
created those weights what you can do is
just pass them in to SK learn so you'll
create a column of weights I've done
that here just added a column in pandas
DF bracket weights
and then what we can do is use that in
order to do more complex analyses so if
I were to just calculate for example the
raw average of employee satisfaction I
did an employee satisfaction score of
about five point seven but if I
calculate the weighted average based on
my employee satisfaction score it's
significantly lower I get here five
point four five so that that average
score went from five point seven down to
five point four five above a decent drop
and that's because people in accounting
this is based on the data I generated up
top but people in accounting were on
average happier with their jobs people
in finance were on average less
satisfied with their jobs what ends up
happening though is when accounting over
responds and Finance under responds is
that that's gonna skew our results now
if you want to take this information and
you want to build a more sophisticated
model with this you can do so by passing
DF weight if you're if you're a user of
Python and specifically scikit-learn
if you want to you can pass DF bracket
weight that column or that vector of
weights when you fit your model and it
will weight
your models results based on those those
weights that you've given it so you
could do this for a linear regression
model or you could do this for a random
forest or something else if you would
like to two quick things that I want to
call out one is that our goal with post
weighting when we do this weight class
adjustment is to decrease our bias but
what should we be concerned about well
when we decrease bias
we tend to increase variance and so
there's an article from the New York
Times back in 2016 some of you may be
familiar with this there was an
individual I believe it was the the
title of this article is how one
nineteen year old Illinois man is
distorting national polling averages and
what this ended up and so I encourage
you to take a look at this if you would
like to take a look at and read this but
effectively they created these buckets
they weren't just looking at the
accounting and Finance Department but
instead they looked at for example age
geography sex other information maybe
political party all of these different
buckets and by creating so many
different buckets and attaching a weight
to those buckets based on response rates
what ends up happening is they decrease
bias but there tends to be an increase
in variance and so what ended up
happening here I would encourage you to
perhaps take a look at that later if you
would like but what ends up happening is
that the person who had that who is
distorting national polling averages his
weight as assigned by this approach was
a was thirty times higher than the
average individuals weight and was
actually 300 times more than the person
with the smallest weight in this poll so
this one individual had an enormous li
outsized influence on these polling
averages so it's something to to keep in
mind related to this I'm making an
assumption here I'm making an assumption
and thank you Sam for for sharing that
link I'm making an assumption here that
I know that fifty percent of my people
are in accounting and fifty percent of
my people are in finance but that's not
always a realistic assumption so if I
want to understand what percentage of
people will support the Democratic
candidate in the upcoming election and I
want to look at things across age groups
eighteen to thirty four thirty five to
fifty four or fifty five and up I have
to make a guess about that as I write
here hopefully it's an educated guess
but what we see in past elections may
not be indicative of what we're going to
see in this election thinking about the
2016
kradic presidential primary my
understanding is far more young people
came out and voted in that Democratic
presidential primary largely in support
of Bernie Sanders thinking about that
that's something that we may not have
noticed in 2010 2008 2004
so if we use past data to predict the
future it can be really challenging to
do that in a way that's principled we
think about when then-senator Obama was
running in 2008 what ends up happening
was when when he was running against
secretary or then I should say
then-senator Clinton in oh wait what
ends up happening is that if you just
looked at information in 2000 and 2004
you're likely going to dramatically
underestimate the proportion of people
of color specifically black voters who
came out in support of Obama during the
2008 election so this is this weight
class adjustment method is something
that you can sometimes do but you can't
always do that and so it's important to
keep in mind some of the limitations of
this we would be assuming that we know
what the distribution of in this case
what I've highlighted the age groups are
but that's certainly not a guarantee I'm
gonna go ahead and shut this and I'm
gonna move back over to the slides
you
so to try and talk about how to pull
some of these pieces together in a work
flow we have not talked about we have
not talked about imputation 4 for unit
non-response yet but we'll get into that
here in terms of my work flow I start by
saying how much missing data do I have
and is it worth my time to try and
address it anytime I'm doing a data
science problem that's one of the first
things I look at then I say is it
reasonable to attempt deductive
imputation which we're going to talk
about momentarily then if my goal is to
generate predictions then I'm going to
use the pattern sub model approach if I
want to conduct inference that I will
use the best imputation method available
ideally proper imputation so we'll talk
about what each of these are because a
lot of those bold in terms are things we
haven't seen yet in order to get into
that though one last thing that I need
to talk about are three different types
of missing data
now you when you look at your data and
you see a bunch of na s in your data or
a handful of na s in your data they all
look the same to us but there are
actually three different types of
missing data that are important to know
so I'm taking inspiration from my friend
Allison here my friend Allison she is
getting her PhD in biology at Notre Dame
very proud of her so let's say that
she's a grad student in a lab working
late and while she's pipetting in the
lab she reaches for her pen and
accidentally knocks one petri dish off
the desk so from that petri dish my
friend Allison loses all of the data
that she otherwise would have collected
so over here I'm looking at what maybe
that might look like in terms of data
gathering so Allison was able to measure
how much bacteria or what was the width
of the bacteria in her petri dish on day
one for all of these different petri
dishes did the same thing on day two
but this here you can see 16 millimeters
but really that would be an n/a in our
data that's something that we do not
have access to we would call that
missing completely at random this data
is missing completely at random because
there's no systematic differences
between that data that's missing and the
data that we've observed
moving on to the next example there's
something called missing at random and I
apologize please do not shoot the
messenger I was not in the room when
people decided on these terms
I think these terms are silly and I wish
there was a better way to describe them
but I apologize on behalf of
statisticians here so we talked about
missing completely at random here we've
got missing at random so let's say that
we work for the Department of
Transportation and we're looking at the
Pennsylvania Turnpike a toll road that a
highway that hasn't told me with on it
so that you can understand people have
to pay whenever they go through this
toll booth in order to use the
Pennsylvania Turnpike and let's say that
there's a a sensor set up to track how
many cars go through a given gate in a
given time window
well that sensor breaks and doesn't
gather any information between 7 and 10
a.m. what we would describe that as is
data that's missing at random and the
reason that we call it missing at random
is that conditional on some data that we
do have in hand the data of interest is
not systematically different so whether
or not that data point is missing
depends on data that we have observed in
this case we have observed time that is
information that we do have and time
contributes to that missingness that
missingness is based on are contingent
upon those specific hours that data is
missing you might imagine this solution
for trying to tackle this type of
missing data is maybe we want to use the
time in order to help us fill in or
generate some value for those number of
vehicles that are that we are missing
the last type of data that's missing the
last type of missingness I should say is
data that's not missing at random let's
say that I administer a survey and that
survey includes a question about income
people who have lower incomes are less
likely to respond to that question about
income what we call that data that's not
missing at random because whether or not
something is missing depends on the
value of that missing thing itself here
for example we see that people who have
lower incomes are on average less likely
to share their incomes with me so if we
wanted to do something simple like
calculate the average of this data I can
calculate the average of income but it's
going to be skewed pretty significantly
upward we're gonna see a value that's
much higher than it should be now this
is the most complicated type of
missingness to work with because we
don't have access to these incomes here
so those are the three different types
of missingness and i want to talk about
a couple of ways that in the 15 minutes
we've got left that we can handle so
there are five different methods here
that I outline I'm going to move quickly
through them because there's a reporting
here and I want to be respectful of
folks this time and not hold folks over
but again please ask any questions that
you have in the chat
so let's start by talking about
deductive imputation deductive is it has
to do with logic we're going to deduce
values we're going to use logical rules
to understand how we can fill data in so
let's say that there was a survey that
asks if somebody was the victim of a
crime in the last 12 months and that
person says no and then of the same
survey has a later question that says
really the victim of a violent crime in
the last 12 months and that respondent
leaves the answer blank we can use logic
we don't have to make any guesses or we
don't have to do any inference we can
use logic to say given the answer to my
first question I know the answer to that
and I can fill in that missing value
through logic this requires specific
coding so you would have to as we get
new data we have to recognize how do my
variables or my columns relate to one
another you would have to code that up
that's not something that is going to be
consistent across all data sets so you
can't just download a library to do that
it can be time-consuming but it's good
because it doesn't require any inference
and it does not matter what type of
missing data you're working with whether
it's missing at random not at random
completely at random you can do this in
any of those cases the next thing that I
want to bring up is mean median and mode
imputation so I imagine that many of you
have done this at some point or another
for any n a value or any missing value
and your data you just replace your
missing value with the mean or the
median or the mode of that column it's a
quick fix it's easy to implement and it
seems reasonable but it can really
significantly distort your histogram and
it underestimates your variance and
we'll talk in a minute about why that
variance or that variability is so
important it should only be considered
if your data is missing completely at
random so if you can say based on my
understanding of my data I can truly
believe and maybe some quick analyses
that I do in my data you can say look I
believe that my data are missing
completely at random this would only be
appropriate in that case but even then
you probably shouldn't do this in their
better ways of handling missing data so
this is an example so what I have up top
and this is all in that zero two
notebook if you want to take a look at
that zero two item missingness these
visuals come directly from that movement
so here up top
this is the real histogram of data with
in blue this blue vertical bar shows us
the true average of that data down below
we're looking at the same data but in
blue I have which data I've observed and
then any value that was missing I filled
the mean in so here this orange bar
gives me the mean you'll notice that
that's a pretty dramatic difference
between the top and the bottom if you're
missing ten twenty thirty percent of
values in a column which is not the
craziest thing in the world to think
through you might get something like
this so first off you're going to
distort that histogram so that's one
challenge of working with this
the other thing that I want to run
through is why is under estimating
variance a bad thing so here I've got
the formula for your sample standard
deviation and you can go through this if
you would like but in short if you are
working with the sample standard
deviation what you'll notice is that if
you've observed your first K
observations and then observation k plus
1 all the way through n those are
missing and you try and use mean
imputation what you'll do is for K plus
1 through n you fill the meaning for
those values that formula ships instead
of dividing by K you're gonna divide by
n that denominator gets bigger but you
can rewrite this formula by breaking it
out for the first K values those values
you've observed the actual real data and
here k plus 1 through n all of those
values that were missing and you filled
in the mean for we'll notice here we've
got x-bar which is our sample mean minus
x-bar which is our sample mean that's
zero zero squared is zero and if you add
a bunch of those up that still gives you
zero so what ends up happening is that
this part of your this part of your
variance or this part of your standard
deviation remains exactly the same you
don't add anything there but your
denominator gets bigger the reason I
walk through that is by doing this your
standard deviation gets smaller your
standard deviation is used in a number
of ways one if you try and generate a
confidence interval then your standard
you're gonna get maybe a 95% confidence
interval but that's gonna get smaller I
apologize if you can you can either see
the Lightning or hear the thunder on
sign so you may see your your confidence
interval get much smaller depending on
how many of those values you move it
that's not because you're getting more
confident or that's not because you
decrease your level of confidence and
say 95
to 90% confidence that's just because we
imputed our meat so we might become
falsely confident in our results
something similar happens to p-value
where your p-value may shrink so your
p-value of point O 7 now becomes a
p-value of say point O 3 all of the
sudden we get a significant result but
even though we but that significant
result is only because we filled in this
missing data so Ramesh asks and I
apologize if I mispronounce anybody's
name thank you for your question you
mesh do you see significant gains in
model performance from imputing using
methods like Miss forests or other model
based in QT how do they compare it in
simpler imputing methods like mean
imputation so mean median and mode
imputation and if I move to the next
slide this is a write-up of that
confidence interval gets smaller the
p-value gets smaller but that's not
something that's that's not real that's
not valid if we look at mode imputation
we see a similar challenge where one
value is artificially inflated at ton
but we're still going to see in effect
where that standard deviation is almost
certainly going to get smaller and
artificially so so when it comes to
trying to impute properly what you
should do and in the interest of time
I'm gonna skip ahead if you were to try
and fit a single regression imputation
where you fit a model to your data like
Miss forests or something else you're
gonna get values that look like this
where those imputed values are all
lumped in the middle it's still not
going to work the way that you expect it
to and that's because when you generate
those predictions that deterministic
computation that you do is usually going
to fall on one line instead you imagine
that you probably want to generate
values that look more like this that
resembled a true variability that you
see in your rule
so because of that in order to properly
impute we need to impose because anytime
you fill in a value with one number
you're treating it like you know that
true number and that's not the case if
you fill in any missing value na with a
zero or a ten or a thousand you're
acting like you know that value don't so
the way to properly impute missing data
is to make like ten copies of your data
set to do imputation with some
stochastic behavior so you can add in
like a random error if you were to do a
regression model or if you were to do
miss forest you could you would be able
to maybe adding some randomness into
that you would do that on all ten of
your copies of your data sets once
you've got ten copies of your data set
that are full they've got some different
values in them then you would build like
your final model or do your final
analysis on each of those data sets then
combine your results together just like
you would aggregate results in a random
forest so if you are doing a
classification or a regression model you
can average your predictions for
classification you would do like a vote
based prediction across all ten of those
models that you constructed there's a
visual here that I think helps to drive
that point home again you start with
your data there's a bunch of pound signs
or hash tag symbols in here that
represent missing data you make a bunch
of copies of that this image has three
copies of your data and fills those in
using some sort of random imputation
method like a regression model with some
random error then you build your final
model or analysis on those three data
sets you get your results and then you
combine them together if your goal is to
do prediction you can do that if your
goal is to do inference there's
something called rubens rules we're
gonna drop that name in the channel here
Ruben's rules
in order to combine those estimates
together so I've got a little bit of
context on that on Rubens rules so
there's documentation in the repository
if that's something that you want to
explore on your
so there's content in the notebook on
that but the last thing that I want to
go through is I've talked about those
first four methods of imputation the
pattern sub-model approach is where I
want to end up for today and that
pattern sub-model approach for handling
missing data is you're gonna take your
data set and you break it into subsets
of data based on how your data is
missing then what you're going to do is
build one model on each of those subsets
creating many different models you won't
combine those models together you will
end up with many different models so a
visual example look at the data set on
the left hand side I have a Y I have an
x1 and an x2 what I can do is I can take
my first two rows what here because I've
observed the same data I'm gonna call
that pattern one my next two rows I'm
gonna call that pattern to the next two
rows our pattern 3 and then my final row
is pattern 4 I'm gonna group my data
into four chunks based on how my data
are observed in missing together and I'm
gonna fit a different model on each of
those so you would end up with four
different models here one model would be
if you wanted to do a linear regression
model y equals beta naught plus beta 1
times X 1 plus beta 2 times X 2 and that
would be fit on those first few
observations then you would fit a
separate linear regression model on
these next observations where you just
exclude any value for X 2 because you
don't have any value for x 2 so that
would be a model like y equals beta
naught plus beta 1 times X 1 so you
would based on this come up with four
different models there are a lot of
advantages to this and if your goal is
just to make predictions then you should
use the pattern sub model approach that
I described here that this will
outperform imputation methods if your
data are not missing at random
and it's gonna perform about on par with
imputation methods are filling in
methods if your data are missing at
random or missing completely at random
it does not require missingness
assumptions so that's one of in my
opinion one of the cool things about
that it is a based on my understanding a
relatively new method there was a paper
released in I think September of 2018 on
that I think it was mentioned a a long
time ago in a more esoteric paper but to
my knowledge there's not a ton of
machinery like in Python to implement
this so it has to be a little bit more
of a manual process so I know that we're
right at the end of time here and I do
want to be respectful of focus time so
first off thank you so much for for
showing up I totally understand if you
need to hop off so please feel free to
do that I'm happy to stick around and
tie you feel free to come on if you mean
to give me the hook and pull me off

