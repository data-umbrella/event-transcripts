# Rebecca Kelly:  kdb Time Series Database

- Speaker: Rebecca Kelly
- Video:  https://youtu.be/92YticvZzCM
- Transcriber: Coretta Johnson

### Intro

Hi everybody, welcome to Data Umbrellas
webinar. I'm just gonna go over a brief
introduction. So I'm gonna introduce Data
Umbrella of Rebecca Kelly is going to do
her talk and then you can ask questions
in the Q&A tab or you can ask in the
chat and I'll just loop the questions
over to the Q&A tab and depending on how
the questions come in we can sort of I
might interrupt Rebecca if it's a
good time to interrupt her but we'll get
the questions answered and this webinar
is being recorded. About me I am the
founder of Data Umbrella. I'm a
statistician by training and a data
scientist and I also organize for the
New York City chapter of Py ladies and
I'm on Twitter @reshamas. The mission of
Data Umbrella is to provide a welcoming
education inclusive space for
underrepresented persons in data science
and we are a volunteer run organization.
Py ladies is a international group of
Python ladies and gender minorities
and you know it's basically got Python
and all all things related to Python
check up check out our homepage and
follow us on Twitter. I just want to go
over our code of conduct we're dedicated
to providing harassment free
professional experience for everybody
and please keep that in mind any of the
chat messages as well. I took a
screenshot of some of the the website
for Data Umbrella and it has a lot of
resources and those resources include on
open source on sources for learning
Python and are about accessibility and
responsibility and data science and I
encourage you to check it out so for any
upcoming event or data umbrella the best
place to find them is on the meetup page
so if you just want to become a member
that's really the best place. We do also
share them on Twitter and LinkedIn
and Facebook so depending on the
platform the choice that's the if you
find out what we're up to
via those social media avenues and
I'm going to turn this over to Rebecca
and let Rebecca sort of introduce
herself and provide information about
her background as well. Great. Thank you,
very much. Well I just take over the
screen there okay okay so can everyone
see my screen? Here let me just.
Oh actually have lost the questions now
that I'm in this view. Let me think.
Is there a way?
Oh maybe I can pop this out. Okay we'll
do that. Can you see this on my screen?
Okay okay because I can. I can read the 
questions and that will be fine. Okay.
Maybe if you can interrupt me if there's any questions
just because I don't think I'll be able to see them.
Apologies. Okay no problem.
Thank you. Thanks appreciate it.
Um so hello everybody I'm Rebecca. I'm
very happy to be here talking to you all
today about Kdb+. I work in New
York myself so I thought there was a lot
of people in from from local to me so so
that's great.
You can you can find me on LinkedIn.
After this if you'd like if maybe we can
grab a coffee whenever that's socially
acceptable again so I'm based in New
York and I work as a Technical
Evangelist 4kx.
I've worked with the company for I was
just actually chatting with this work
company for about five years started as
a developer and Kdb+ worked my way up to
a Solutions Architect left went back to
college did a master's in machine
learning in the University of Edinburgh
in Scotland which was great and then I
came back to work in New York as the
Technical Evangelist so I've had a bit
of a journey kind of in between then
with the with the company I worked in a
few different places
location-wise which was which was fun
and I'll actually get into that a little
bit when I talk about some more about
tech so the way I've approached it today.
I did obviously you know look around and
I saw that the mission statement for
Data Umbrella is to provide a welcoming
and educational space so really tried to
focus on putting as much educational
content as I can in into this
presentation. So I'm hoping to provide a
very good grounding on you know what is
Kx as a company. What does the technology
look like? Who uses this. What's the user
for? And then what does that mean for you?
Before I jump into the demo and the demonstration will
do my absolute best to cover as much as
I possibly can of this language which is
quite quite broad.
So hopefully you'll come away with a
very good understanding and knowing
where to go for more resources so Kx is
a division of First Derivatives Kx is a
software company and are the software
that we produced is a high-performance
time series database. So we've actually
been around for quite a number of years
now we started in the finance space. So
kind of you know FinTech and really kind
of focused on the problem of how to deal
with big data. So when people talk about
big data they tend to kind of split it
into these the V's so the the four V's
there's a volume, velocity, variety and
veracity is typically the the kind of
primary four that I think IBM force
product and if it helps you to think
about big data in that way.
Then you know the place that we work in
would be the the high volume and high
velocity space so anywhere where there's
huge amounts of data coming at you
very very quickly is where we would
typically where our technology is most
commonly used. 

### Other Verticals (6:54)

Well we did start in
finance and that's not that's not the only
place we operate now we've actually been
doing a lot of work in other verticals.
So some of the ones that we've probably
gotten the most traction with would be
IOT and manufacturing so I've kind of
kept the focus on finance for a lot of
this presentation because it being New
York certainly for all of the people
that I work with in this in this place
and this time zone it tends to be a lot
of finance related stuff but like I said
we are kind of working in these other
verticals and it's actually really
interesting to see the the difference and
the similarity between the datasets. So
if you think about finance
in one way in which it will be very
different from something like IOT or
manufacturing is the the pickiness of
the data if that makes sense
you know if the markets are busy you get
a very busy day you have very very high
data volumes.
Whereas in IOT or manufacturing you tend
not to encounter that same distribution
let's say of the data. The way in which
they might be very different is that
with finance you can get downtime you
know there's those times when you're not
you know so like on weekends the markets
might not be open
whereas in IOT or manufacturing it's
pretty much 24/7 but they are united in
that they have tend to have you know
huge volumes of data and very fast
velocities. So you're talking about
sensor readings every every like
millisecond coming off multiple multiple
devices and kind of aggregating that
together which is not so dissimilar to
capturing all of the the data from the
markets and trying to action that in the
in the finance space. So just to lay a
little bit of the scene the technology
so anybody who might already be familiar
with a little bit the technology will be
may have heard people refer to it as
either kdb+, kdb or q so this is my
little infographic you'll see I'm quite
fond of pictures to tell to to tell
stories.
It is this and this to me represents how
you can think of the software. So Kdb+
is the database layer that's where the
data is stored on disk and then q is the
interface around it. So that's a
turing-complete programming language
that you use to actually query and
retrieve the data from the database and
that's the language that I'll be showing
you in the demo in a moment. Again more
effective because pictures tell a
thousand words. I'm gonna break down I
suppose some of the key features of the
language and in a way that I hope will
help
understand how it might be different to
or similar to other languages that
people have worked with before. So it's a
functional language. That means that you
know there's no it's not right compile
test you're you're actually working
interactively with the data similar to
Python in that sense and that you're you
know you can start with the problem you
can code around this you can work your
way through it and it's certainly I
spend a lot of my time talking to the
developers who actually use the language
and this is one of the things that I'm
that that they most kind of appreciate
about it because you know if you're
talking about working with big data and
trying to work through a problem it's
actually quite beneficial that the the
speed of execution is it's short you
don't have to go and take a big tea
break every time you want to to run some
code for example it's a columnar
base to database so if you're familiar
with other databases like MySQL for
example those are typically although
it's becoming more common but they're
columnar base but those are often row
based databases. The main difference I
suppose is how the data is retrieved so
if you're working with a row based
database and anytime you want any piece
of information in that row you have to
pull the entire row back into memory but
if you think about big data and how
people normally work with or use big
data you're not you know it's rare that
you would say give me all of the data
often you you're you know you're trying
to filter is you're trying to work with
a subset you're trying to kind of
aggregate it to all those things. So it's
very common that you would do something
like I would like all the data on this
day's for the Apple stock for example. So
what they columnar new database that means
you can kind of go to so that you know
you can go to the particular date that
you care about you can go to the you
know the the the stock name and you can
kind of filter based off of those
criteria and then only pull back the
rest of the data for the rows where
where it's actually met your filter. So
it's a much more
memory efficient way of trying to work
with these bigger data sets. It's very
fast and yeah I like to throw this one
and I upgraded my car from the first
version because we actually do work with
awesome marks marking Red Bull Racing. So
if you kind of think about the analogy
between the the two cars that's kind of
the the performance scale that we're
looking at it's concise of a language. So
that's what this little target is trying
to indicate that doesn't really that
sounds kind of like a throwaway comment
at first but I suppose the difference is
you're not writing pages and pages pages
of code to achieve a particular result
it's often a case of you might write one
or two lines and that means that you
know you you spend more time thinking
about what it is you're trying to do and
when it comes back to you know
supporting it or actually maintaining
that code you're working with a much
smaller kind of code sash which is often
quite beneficial for for for these kind
of systems. This is the table. Sometimes
people don't know what this is. Tables
are first-order data type in the
language. So it's a valid statement to
say table 1 plus table 2 and that will
depending on what you have in your
tables work but this is really to
emphasize the fact that the language and
the software grew up being focused on
the problem of data as not just kind of
a secondary consideration but as the
the primary motivation for the software.
So so tables are really front and entered.
This is time and this is this is really
about I suppose the fluidity of it and being
able to kind of work between different
times so you know data is is a difficult
and complicated but but things don't
tend not to necessarily coincide a lot
of the time if we're talking about fine
to markets you know like when you get a
trade you don't necessarily have a quote
for that trade at the exact time of that
trade. So you need to do you need to kind
of recreate the market context by by by
by retrieving the the quote that was
present in the market at the time of
that trade they've gotta be very common.
For example for a lot of the people that
use our software they might use it for
quality of execution reporting that's a
very big one. So they'll they'll they'll
need to know you know did was this the
best possible trade price that could
have been achieved have we done the best
that we possibly could do for our for a
customer that we're executing on behalf
of so there are a number of joins in the
in the language that are specific to
time that are based around that. I will
show you the As of join when we get to
the demo but I suppose to kind of go the
more generalized side of things there
there is a window join in there that
would let you say for every row that you
have in one of your tables you can
define a specific period of time around
each of those records and join that
original table with information from
another table so for example if you had
a sensor reading you could set a window
of time maybe you know ten minutes after
if maybe five minutes before and seven
minutes after whatever you like and
retrieve from another table let's say
like the temperature that that was
present in the room at the time for that
for that sensor during that time period.
So it's really all about kind of context
and time is I think the the ultimate
context without without running the risk
of sounding far to um introspective
but a but that's that's the idea. When
doing is the you know bread and butter
working with big data you know 
you have so much data you need to
oftentimes you know work with it and
these in these kind of smaller time
periods being able to kind of
chop and slice and dice all the data
that you're working with. So when doing
is important this is about aggregation
data aggregation data filtering all of
those good things again Big Data so you
know if you're talking about petabytes
of data you're not going to have
somebody there looking at it row after
row because that's just not feasible.
It's not a good spend of anybody's
time. So it's all about being able to cut
to roll it off into the format that you
that you want to see it in the kind of
one of the statistics that you care
about on the on the subsets of data that
you care about and and kind of continue
from there. So this is actually a little
bit of an older reference maybe then
then people might be familiar with but
this is a lambda here and it refers to
kind of the original concept of a lambda
architecture. So that's being able to
take the the data from very first kind
of point of ingest to being able to work
with it in real time and then finally
being able to work with it in its wider
historical stage. So that whole kind of
idea of being able to to seamlessly deal
with the data in whatever format it
comes in and that's something that I'll
that I'll show to you in the in the demo
how as a language it allows the
flexibility to to do that to work with
the data and kind of whatever format it
is you're getting it in. The benefit of
this as well is that you know you're not
writing three different sets of code if
you have a particular function that you
want to use with data that you want to
apply to the data you don't have to
write something special for for if you
if you're working in in real time
another for in memory another for on
disk and maybe another for streaming but
that's not something that that you have
to to worry about. This is it looks like
a waterfall. It's supposed to be
stream. I wanted to highlight the the
streaming capabilities because I think
for people who already have a good range
and breadth of languages as I imagine
may well be the case with this with this
group of people here it is certainly
worth highlighting the the streaming
capabilities of the language because I
think it's a it's really a place where
we Excel and where maybe there's not
always a great fit with some other
languages. So I've said a few times about
how great it is and obviously I would. So
this is just to say you don't have to
take my word for it and we do
participate in benchmarks so to
contextualize the benchmarks if you if
you recall I was saying that the the
that we started in finance so that I
suppose as a software we're a little
over I think we celebrated our
25 years maybe a few years ago so that
whereby we kind of came in to the the
market as I suppose high frequency
trading and all that stuff was on the
rise and the situation that a lot of the
financial institutions at the time faced
was how do I decide what software to use
for this problem that I have and
particularly when everyone is going to
tell me that their software is the right
software to use so stack is a if it's a
group an independent body that kind of
sat down with all these financial
institutions and said well what do you
care about we'll define appropriate
tests to to to track all of these things
and then that will help you be able to
decide which you know which which
software fits your needs the best. So for
us the ones that we tend to really
dominate in and where we I suppose see
the most use both in our customers as
well is in the in-memory compute and
mass of data at rest so I've kind of
expected. So that so that's that's just
to say you don't have to just trust me
here's a quick a little bit of a
whistle-stop tour of some of our clients
partners. I whoops go back. It's running
away from me. um I've had the fortunate
benefit of working with a few of these
so up on the top right hand corner there
ASIC
that's the Australian Securities and
Investment Commission and it was
actually one of the first projects I got
to work on when I joined the company. It
was great. They sent me to Sydney. I loved
it.
The weather was amazing all the time
everyone was lovely but but yeah. So so
that was a project where it was the
Australian Securities and Investment
Commission who are charged with
overseeing the entire market really. So
they guess all the market data it's such
a great place to be. If you're if you are
you know if you're someone like me who
just enjoy seeing that full picture
and we were working on market
surveillance. So the company chaox we
built we brought in a um and built a market
surveillance system. So we would take all
the data in real time and we were
looking for abusive market practices. So
there's a number of different the standard 
kind of alerts that you
care about in that space. So whether
people are layering insider trading all
of those things had to be kind of
codified and then um and then applied to
the data. So that was great.
I've also gotten to work with the
awesome Martin Red Bull racing when that
was first kicking off I was involved in
the proof-of-concept which was which was
very fun. I got to go out and actually
see the car in the wind tunnel and work
with work with some of the team there
and that was that was very very
interesting. There is an awful lot that
actually goes on. In in in the in the
Formula One racing world and a lot more.
I suppose there's not really regulation
because it's not a government body
regulating them but they kind of group
of all the people that work in that
space or the different Formula One teams
kind of bands together and put a little
bit of
they set their own regulations on and
it's very it's very interesting. Like
like for example they have a limit to
how much compute time they can run. So so
they can gather the information from the
wind tunnel but then they're limited
with how much time they can spend
punching those numbers because they all
brought together and decided that this
was the good number that they were going
to say. So however many hours um
so being able to run things faster
obviously meant that they could get more
actionable insights and it was just an
it was an interesting case that we. I
don't know that on paper anyone would
really have expected as a good as a you
know a potential vertical but now we're
very active in the automotive space and
then I know a lot of these others from
from just my work kind of going around
and talking to the different teams that
are based here in New York and and just
checking in on them and how they're how
their systems are running and keeping
them up-to-date with all the latest
features and all that. 

### Finance Use Cases (24:19)

So how is it used.
I figured. I put together a little word
cloud to hopefully kind of highlight
some of the ways that these clients are
using else. Um so let me see strategy
back testing for example would be a very
common one for people who are who are
using us as a very big historical
database so the you know you have
petabytes of data you have a new trading
strategy but you need to test it before
you deploy it so this is that'd be
fairly common a lot of analytics around
you know a post trade pre-trade quality
of execution and just just in general
for kind of ad-hoc analysis and and and
database to database things. 

### What about you? (25:07)

So I thought
about what you know who all of you are
in this audience and what might what
might make you interested in learning
this software and I suppose the the one
thing that I would highlight is that it
is so frequently used in the investment
banks
and we have a lot of big hedge fund
clients. So if you're somebody who's
looking to try and get more like
maneuver into a position where you're at
quant or strat or financial analyst this
is a great technology to pick up to try
and differentiate yourself from maybe
maybe other people that are also
applying. It's also like I said I find it
particularly useful with streaming data
and again in terms of the effort being
worthwhile for you rather than just
picking up another language where you
can write hello world. Here's something
that might actually help you be able to
address different kinds of problems and
yeah it's it's very interval. We have a
whole team called our fusion team who
are dedicated to putting together these
different adapters so that we play
nicely with other technologies. Look the
world is a big wide interesting place
and there's so much technology and and
really it's used the best tools for the
job. You know for you know we're not
going to rewrite backprop in our
software you should keep using probably
Python and and and and and you should
have our freedom that should be
something that you get to decide. So it's
really it's really about you know doors
open come on in and and the
democratization of data really and then
finally I think time. The most important
well in my opinion the most important
resource that that I think we have as
people is our time and you know you want
to make the most of it. So this is this a
little infographic I got from Forbes
that kind of breaks down what data
scientists typically spend their most
I'm doing and this three percent all the
way around to the end of this nineteen
percent so a little over 80 something
percent quick math is spent on working
with the data getting the data into the
format that you wants but so then you
can kind of do the quote unquote
interesting
work of you know building building your
model testing algorithms doing whatever
it is the kind of the value-added step
of your processes. So the faster you can
get through that in theory the the more
value you can be kind of continuing to
produce. So it's a it's certainly
something that's I like to you know try
and try and speed up as much as possible.

### My Pet Peeve (28:11)

This is this is because I have a forum
so this is where I normally take the
time to talk about it just kind of a
little bit what annoys me and mostly
it's something that I see a lot and that
I think you know whatever software
you're using whatever it is you're
working with you know they're very kind
of good and bad practices and something
I see is that people will go to the
database it you tend to gathered a lot
in these kind of fractured environments.
So in the top panel here what I see
sometimes is that there is a database
administration team and then there is
the data analytics team and they
maybe you know I mean they talk to each
other they're fine everyone gets along
but if you want data to use for your
data analytics what happens is you get
your extract from the database but
that's a database administration team
gives to you they put it somewhere on
disk and you work with that you work
with that extract and that's that's kind
of just what you have but as a data
scientist I find that very frustrating
because I'll you know you like to be
able to test against other conditions
against other edge cases and in other
situations. So like I might have taken
all the information for Apple but now I
want to check for Microsoft and now I'm
caught in that in a two-week
request/response
situation and it it it annoys me and
also from from a database administration
perspective this isn't great either
because you're you know you're losing as
soon as you take the day that out of the
database and you put it somewhere else
using data governance you know that that
audit trail for who access that data is
gone.
So my recommendation and though it
doesn't have to be our database but you
know the best thing you possibly do to
really empower people to do the best job
they can is to give people that freedom
to to work directly with the data and to
to be there with it. So I will get off my
podium now and just move on. 

### Python (30:26)

So I'm aware
the audience here is is quite familiar
with Python so I wanted to particularly
highlight the Python interfaces that we
have. So we have two and the one that I'm
gonna show you in the demo is going to
be this one on the left-hand sides that
we call embed py so that's where it's
kind of what it looks like you'll see I
reuse this pictographic technique of
putting putting the thing in but but in
fact but that's what it is it's a it's a
q process that's running that has a
Python process in better than to it. So
they share the same memory space and
it's really very efficient and then py q
is the flip side so it's a Python
process that's got q embedded in the
same memory space. So the difference
would be the prompt that you're working
with.
So with embed py the base language is q
and with py q did the said language is py q 
and that's the main difference.

### Questions (31:22)

Rebecca. Yes. This may be a good time to
ask this question from.
Yeah go for it.(Questions)
Would love to know the reason why q was written.
Were there some time series data access not supported
by SQL.
Yeah that's a great question and yeah I
think that was effectively it. I think
people got tired of trying to figure out
how to how to stitch the data back
together to get that context so I I'd
mentioned the half of join. I'll show it in
the demo but the idea is that you can
have one table like your tray table and
have all of those different times I wish
all those trades occurred and you can
just say oh give me the quote table as
of the time in the tray table now I know
there have been
that some of these capabilities have
been subsequently added to some of these
row based ones but but that you know
performance wise you know it just wasn't the same
if you're trying to make a decision
about you know how much credit do you
want to extend somewhere that's not
something that you really want to to
leave waiting for too long you know.
These are the kinds of things that can
end up hurting you financially that
the time horizon of when you can get
those answers and as well at the ability
to to to chop up the data and bucket it
appropriately is is also very kind of
fundamental to the language as well and
I think that that has been one of the
real drivers too but yeah it was it was
kind of a two-pronged thing it was being
able to provide the kind of common
analysis techniques that that that that
are native in the language now such as
the the bidding the aggregating the the
time contextualized joins and then also
it's the the speed at which you could
perform those operations we're kind of
the two driving factors behind it so how
can we do these things firstly and
secondly how can we do it at a speed at
which this will be valuable you know
information still because any
information has a has a maybe not maybe
not may not all information now that I
think about it
but a lot of information has a has a
finite value horizon and certainly in
finance that's stuff that can be quite
short hopefully that answers the
question. Are there anymore while
actually well well we're kind of pause?
No that was the only question.
Okay okay well hopefully that answers
and all continue on yeah 

### Machine Learning (34:06)

So python has
been in each place that we've
particularly focused on because of the
huge growth in machine learning and AI.
We have a team ourselves in London that
are exclusively dedicated to machine
learning and AI and how how
we as a software can you know provide I
suppose the most utilities and guidance
and and benefit to to the users of our
software in that space
like I said we're not planning on
rewriting backprop and and really the
the most fundamental step I think in in
terms of making that available to our
customers was you know let's let's get
an easy way for people to work with
Python and actually you'll see when I
get to the demo now I think in a second
that I'm going to use the Jupyter
notebook can a format that hopefully a
lot of people here will be familiar with
and this is me.

### Live Demo (35:07)

Live Demo hopefully hopefully not everything.
Here we go.
So okay. I've got a Jupyter instance
running and I actually have the ability
to to run q you so there's a q kernel
available for Jupyter for those people
that are interested in maybe getting
this set up after and when I when I go
back to the slide I'll talk a little bit
more about that but we're available on
an Anaconda Anaconda or Anaconda and I
call it the comic-con is the conference but yeah
we're available via Anaconda and I think
actually in the resources that I that I
sent on that that I think was linked in
the United States is the the link to
embed py and it goes through the
installation and setup and there's an
and yeah hopefully that'll arm help you
after this if you want to try reproduce
some of this so the demo that I'm gonna
go through I'm gonna try and give you
the biggest whistle software I possibly
can of the language. So I'm going to show
you, I suppose the basics of it other as
kind of a column based language and
really being kind of fact oriented it's
quite like numpy or an umpire whatever
way people want to say it and then you
know when it comes to the table querying
I suppose again with the kind of Python
analogy it's it
you know I I actually do a comparison
between a query and in pandas versus in
in our language we actually have an
sql-like syntax that we refer to as q
SQL for for that.
I'll show real time so data that like
working with data and memory working
data on disk and streaming data and then
finally the pipe and interoperability. So
it's very ambitious but what but
hopefully it'll be a good introduction.
So I was saying that it's like numpy it
is it's it's very much vector based so
in this cell here all I'm doing is
creating a vector or an array that I'm
calling a and then I'm just adding 10
and you can see that all the operations
are are kind of pairwise out of the out
of the box in this case I'm taking the
the kind of the vector b and the vector
a and I'm adding them together and
that's just kind of automatically
working pairwise so that's that's pretty
neat and useful in a lot of ways but
moving on actually getting our hands on
some data. I have pre-loaded some
simulated trade and quote data. So this
is what my quote table looks like. I've
got my symbols the time and the
standards kind of quote information and
similarly I have my my trades. They're a
paradigm version because we don't we
don't need a lot to kind of go through
this. So in terms of how much data I'm
working with I've got my 5 million in
quotes and 1 million in trades. I also
because I'm running this with embed py
I've also got that same data in Python
so that I can hopefully show a little
bit of the the kind of side-by-side
direct comparisons. So just to prove
they're the same here we go.
The good thing is because we're working
in this Jupyter notebook environment we
can actually we can run some cells in q and
some cells in Python
by using these neat little magic
commands. So I'm going to recreate a very
common requirement for for financial
data which is to create a volume
weighted average price referred to as a
vwap broken down for each of my different
stocks so normally people would kind of
create this at the end of the day as an
indicator to use for some for some
different models. So if I do that in
Python you can see it looks like this.
Now obviously, I'm very aware I'm talking
to a group of people who are quite
Python literate so any suggestions on on
refactoring this are very welcome but
this was this was my attempt at doing
this in in pandas and here is the
equivalent in q. So you can see the
sql-like syntax. So select the columns
we care about broken down by the
columns we want to break down by from
the table we care about and to show some
of the. So these items that are
highlighted in green are some of the key
words and the language. So they kind of
do as you as you would expect. I don't
think there's anything here that I
thought that people are struggling with
but if there's any questions do you just
chat wavg is weighted average. So yeah
so it's very easy to kind of get that
same breakdown and just to prove that
those are the same and a more
complicated thing that I didn't even
honestly attempt to do in Python but it
but if somebody knows this please do
send me on the code is a time weighted
average price. So this is where we search
to kind of again just highlight that
area earlier questions that somebody had
like why why was through the need for
this. This is an example of something
that be very common to do that's using
time that maybe isn't as easy to do in
other languages. So what we're getting or
generating here is a time weighted well
this is actually a spread but it could
be it could be on thing is but its time
weighted and it's broken down by
and by stock and here's an
example of some of the aggregations so
this xbar function here is actually
performing pocketing so it's breaking
out all the times into 30-minute
buckets and then this is the the time
weighted average spread so so hopefully
that helps to kind of highlight or make
it clear how kind of time focused the
the language in the syntax is but we do
have the the standard joints that you'd
expect. So if we do have this kind of
reference table like this info is just
giving us the full company names we can
use a left join and append that
information on but more interestingly we
have this outer join so let me show you
what this looks like, what I'm doing here
is I'm joining the trade table with the
quote table and I'm doing it where this
symbol is match exactly. So if I'm
looking at a trade and Apple I only care
about quotes and Apple and then my time
column is gonna serve as like a soft
lookup. So I'll see if I can find an
example here in the in the in the like
directly in the things okay. So if for
example here there was a trade that
happened in Apple at 9:30 and then
all of these milliseconds later actually
that's another thing that we have native
to the language that maybe not a lot of
other databases support. It's just the
granularity of time that we support but
yes so it happened at this time and
you'll see that this quote information
that has been joined on is actually from
a quote that occurred just like that one
one increment beforehand. So while this
was obviously very close in time that
could be much much earlier in the day if
you're looking at something that's maybe
particularly liquid and that's that's
kind of the idea behind it being able to
kind of bring that context in and say
well this was the quote and therefore
therefore this this works like that.
So just to show the tables. The benefit
of being able to do this kind of
analysis. So now that I've made this
table tack that has my contextualized
trade data I can use that to perform
different analysis so like like I said a
very common one is around the quality of
execution. So I'm gonna go and I'm gonna
pull out all the cases where where that
price that I traded out wasn't within
the better ask. So this is something
unusual that really should be justified
because you know if if it's outside the
better ask it you know there's a very
good chance that this wasn't optimal in
terms of its execution so that needs to
be addressed for the clients. The neat
thing about it being a programming
language is that you can put code kind
of directly into your break downs. So if
you're used to maybe some other
languages you know that the break downs
often have to be kind of existing
columns. So this would be maybe a
two-step process you'd have to make the
column and then break down then do your
break down on the kind of the next line
working with a new table but because
it's a full programming language you can
put kind of whatever you you want in
here to kind of get your breakdowns. So
here I'm deciding if it was a valid
trade or not by deciding by checking if
the price was within that bidder asked
from the quotes. So these cases here
where it's zero this is a boolean value
are telling me that that's not true.
So there was 84 cases where trades
happens that were outside of the quote
in this in this stock. So that is where
if I'm the person charged with you know
ensuring quality execution that's where
I would be starting to to look as my
kind of basis. So this was a quick
example of the syntax I was working with
in-memory data but now we're going to
jump to on disk data. 

### On-disk data (45:32)

So I have much bigger tables on disk now having
said that I am just running off of this
let me see about this Mac this will tell you
yeah so this is what I'm working off in
terms of my system spec I'm not
connected to anything else in the
backend here.
It's just my own laptop and I have some
some data in a database that I have that
I've generated that that's running
locally and in fact I've got about 95
million quotes and 19 million trade
records. So I can show you what they look
like you'll notice that these are schema
wise this table is the same as it was in
when we were working within a memory
with the exception of this new column
here which is the date which signifies
the date. So normally in a kind of a
stock standard take capture system using
the technology people would typically
accumulate the data intraday in the in
the in memory table and then when it
comes to the next day they will they'll
basically purge that right that I disc
and then start fresh. So just to to add a
little bit of architectural context to
it but we can do the same things with
this data that we have on disk as we did
with the in-memory data so we can get a
breakdown of of how many this count i is
just going to tell us how many records
we have for each day you see the syntax
isn't really any different and we can
actually run let's run a so another
thing that people would normally do at
the end of the day is you kind of create
some summary statistics or you know from
the from the trading day that just
occurred and it's very common for for
candlesticks to just create the they
open high the low and the close along
with this vwap here so we can just
bill that on the fly. So just a reminder
again that we're working off of the I
think 19 million records or something
and it doesn't you can see it doesn't
really take an awful lot of time to to
work with this which is which is nice so
now that we have
this data in a daily format this is
exactly the kind of data that we might
want to feed in to a model if you were
trying to to have a look at you know
beginning to understand the the market
behavior and where things are. So I can
take the actual the series so the the
the end of day vwap for each stock and
extracted from that table and get us so
this is a dictionary so it's a key value
pairing of of the the key being the
stock and then the value being the the
price series for each day from the daily
table if I want to just see it for one I
can do that so this is what the Apple
price series looks like getting again to
the statistics of it we can look at how
that correlates with Microsoft.
We can also I'm missing bit of a
line we can check Apple against every
one with less code. This is actually this
this is kind of our version of a it's
one of our versions we have a few
different ways to do this but it's what
we call an iterator in the language and
it's kind of it's our way of doing loops
you know you don't really write for
loops in the language you you iterate over
things so I'm so what we're doing here
is we're we're court we're checking the
correlation of Apple with each item to
the right that's what that's doing which
is our price series for each to the
different stocks and then finally we can
actually go even further and check the.
So this is looking a little funny
because of my formatting but this is a
this is the table if I see my for a
second. Oops.
Yeah so there you can see it looking a
little bit more like the table but I
will I will go back in for free ease of
readability now but just a highlight
that this is less code than when I want
to just do it for for the two individual
ones but yet I'm doing more so it's
hopefully a little bit of a peek
the kind of elegance of the language so
to speak. Hmm if there's no questions or
nothing so far I'm gonna jump into
streaming and this were. Oh sorry.
There is one question. Oh great. Okay.
A question from Aditi is q couples
with Kdb or can we possibly configure a
relational database we already have to
work with q. So there are different you might
have seen the kind of fusion piece I
mean you can use it just as a
programming language if that's all you
want to use it for for sure we have a
number of different drivers so there's
like an ODBC driver there might even be
like one or two different versions of
flash so there's one by Simba there's
another ODBC three one there's a JDBC
driver. So like if you're trying to work
with relational databases yeah you can
you can do that you can you can do your
extract from those and bring it in to
kind of to this space and actually the
the working in Jupyter has been quite um
quite great for a lot of our of our
developers really because the so I'm
currently got the q kernel running here
with embed py which means that I can
kind of swap in these different code
cells between the two different
languages we also have an interface
embed or so that's my accent can be a
little heavy but that's or for Romeo if
we're going to go fanatic with it. So I
mean the programming language. So if you
have both loaded into your q
environment and you're working in
Jupyter you actually kind of have this
this great kind of polyglot environment
where you can have a cell and or and
have a cell in Python and then swap back
to q and I mean maybe maybe someones
worst nightmare but but it's quite it's
quite helpful if you're if you kind of
like to use a few different things like
I said best tool for the job and all
that.
A question. So q is a language and Kdb
is a database. Is that right? Yeah. 
I mean people tend to use them kind of
interchangeably but but technically yes.
So Kdb+ is the is the database
kind of so that historical data
that I was looking at would be written
down in in kind of that format. Okay.
So I'm going to let you go back to the
presentation but I just want to add that
JupyterCon is coming up. So if you want to
submit a CFP on how you use Jupyter for your
work feel free to. We can talk about it later.
Oh cool. Thank you.
Yeah no. I do. I do enjoy it. I think I
think I think it's great it's a yep. I'm
gonna start in a tangent now so I'll stop but
yeah we should chat about it.

### Streaming Analytics (52:53)

So yeah finally moving on to streaming.
So you we've already looked at this and
I had the the five million quote 1
million in trade. So I can do you know
the syntax that you saw before but what
I'm going to do now is I'm going to
subscribe to some data in on the back
end and you'll see that this is now
changing the number of rows I have in my
data is is changing as I get new data in
to the system. So I can still work with
that live data even though it's it's
streaming and calculate these kind of
metrics on the fly. So I think that my
total count broken down by each stock
from my quote table and you can see that
those aren't changing. This is where I
normally go into my architect mode and
talk a little bit about it good system
design.
So there's a very big difference between
streaming analytics and kind of these ad
hoc api's when it comes to what effect
it has on the system. So I'll try clarify.
The quote table here that we have is
going to be increasing as the day goes
on so every time you get a new set of
data that's appended on to the end of
your code table and that continues to
grow.
So that means that when you're running
this query that's going to take
different times to complete depending on
what time of the day it is and even
though obviously it's a very fast very
performant language like you know this
doesn't take really any time to do if
you have a lot of people working on the
same system and I'm wanting to kind of
do these queries then you know that can
sometimes become non significant and you
don't like that if you if you're
designing systems you don't like
unknowns you don't like not being able
to you know have things behave in a very
expected way. So what we do in the kind of
Kdb world is we we use
streaming analytics. So streaming
analytics are really just getting to
decide what you want to do with each bit
of information you get. So if I get a new
a new quote message what I'm going to
get I'm going to get a little mini table
that will have some amount of quotes so
that could be one row or it could be
many many rows it depends on kind of the
upstream system but I decide what I want
to do every time I get that message. So
that means that well actually I'll just
show you here so I'm gonna make a new
streaming function and it's going to
happen every time I get a quote message
so this here the curly brackets are the
is how you write a function in in in kdb
/q and then this here is the
parameter so I'm saying that this is a
function that takes a parameter q and
then I'm writing the code for what I
wanted to do. So I'm gonna create a new
table called qtotal that's going to for
every kind of message I get in for the
quote table so that'll be a series of
rows or one row or whatever I'm going to
calculate this so I'm going to get the
total count broken down by each stock in
just that message so that could be like
three Microsoft messages and one Oracle
and to IBM that might be what came in in
a bundle and I'm going to them
add that on. So this is an example of
kind of adding two tables really but
that I kind of talked about before I'm
going to add that on to this qtotal
table so that every time I get a new
message this is updated so the benefit
of doing that just to show those two
things are the same now and they will
continue to be the same is that this
table here that I've created this
qtotal table is small it's got you know a
finite number of records because it's
just based off the stocks I have it's
got a pretty well understood execution
time you know because I'm it's it's
pretty small it's not really going to to
hold up anything but yes if everybody
wanted to come and retrieve that from my
process that's you know this is this is
this is going to take take the same
amout of time no matter what time of the
day they put this in as opposed to the
first query which will have you know
different different runtimes at the end
of day versus the beginning so streaming
analytics are just very very powerful in
that sense and that you can control the
system in a very in a very I suppose
discrete fashion and it does mean that
then you can that this is kind of a
whole framework that we use for for
leveraging action and responses so if I
you know I can have something in here
that would check if you know if the
stock is Microsoft and if the price is
below this then I'd like you to go and
make a trade or or or do something else.
It's this whole kind of event trigger
kind of paradigm that's that but that
you can then use which is which is
really kind of the powerful thing with
with streaming analytics in my opinion
and I'm also just going to do something
else here I'm gonna I'm gonna add to the
tray table a summary that's going to cut
keep a running vwap so keeping a
running vwap actually kind of tricky
because you're you know you've got to
constantly be carry carrying forward
that waiting and that's that's pretty
easy to do in a streaming fashion believe
it or not some things are obviously
harder than others
but but it's it's it's really very
powerful to be able to work with things
incrementally. So if you're interested at
all in kind of capturing real-time data
and maybe driving analytics or decisions
off of it you know I it is very fun to
play with and it's pretty easy to kind
of set up different different
connections. The audience being what it
is. I thought I'd also show some Python
integration because we because we all
like Python here so that's great
so I'm gonna build a time series this is
a little bit more complicated than the
one I did before so rather than getting
just the end of day price from my
historical trades table for e or my
volume way to price over the day for
each day I'm getting an even more
granular time series I'm going to get
the the kind of opening price in
15-minute time buckets for each stock
across all the days in my in my database
So this is built a 15-minute bucketed
time series for for each of my stocks
and then I can import map Bartlett
So this dot p dot import is is is is
doing that so I'm just saying dot p
dot import whatever the library is I
want from from Python and if I. I'll show
you what that looks like that just says that
it's this module here and then I can use
this kind of a syntax to to to to to use
it so I'm saying I want to go into plush
on the function I care about it is this figure
and then this pykw is
saying it's a Python keyword and I'm
saying that associate the Python keyword
of figsize with with this input so I'm
kind of meshing the the q the q
variables into the in but leveraging the
Python library and then I just extract
the time series for Adele and I plot my
my
my figure so that's obviously pretty
straightforward the nice thing about
this is that I can then use the very q
like syntax of of wrapping things up in
functions and iterating to to kind of go
a little bit further so I start with
making my my um my kind of basic plot
said I'd the the size and all last and
then I wrap all of this into a pipe into
into a little function so this is going
to take each of my time series and like
I said they're at dictionary. So I'm
pulling out the I'm pulling out the
price and I'm pulling out the the symbol
for for each of my sorry for each of my
rows of my of my table and plot them
kind of all at once. So that's the this
this each year is the is is another
iterator in in in in Kdb. So it'll take
any function and it will apply it to
each of these and this time series here
is the the table up above where I've got
this sym and the price for each of the
different rows that and the those
basically get passed through as a kind
of a dictionary structure into into this
and you can plot them all so that's
that's a very quick whistle stop tour
of the technology. I'll flick back to
slides now if I can yes and just say
that if it's available for a
non-commercial use so if you want to use
it for your own projects doing whatever
it is you would like knock yourselves
out if you want to use it for academia
absolutely we have the citation page and
everything feel free to play around with
it and in the resources that that were
linked with the talk that you'll see
that there are some guides on on
doing this installation and for those
people who might be interested in
knowing more about this or any getting
getting more hands-on
I understand that with the best will in
the world it's not always easy to
motivate it's certainly something I
struggle with so just to say that we do
have free one-day workshops that we run
at least once a month in in pretty much
at least three major time zones but
certainly in America. We have at least
one a month in the U.S. time zone so for
people that do want to just come along
they're free. The the one-day workshops
the Kx introductory workshops are free
and so you'd all be very welcome if
you'd like to come and get get more
hands-on with it in in a one day
training. So that was me.
This is a picture of me if anybody wants
to stay in touch please do find me I'm
on you can you can email me here rebecca@kx if you have any questions about
anything today or if you just want to
know any more I'd be very happy to talk
with you and I hope that you find it you
know interesting and even if it's not
something you want to pursue hopefully
it'll it has helped you know broaden
your horizons. So certain so certain bit.
Rebecca would you be able to put the link
to the training in the chat.
Oh yes I'll do that now. Yeah. That would
be great. Yeah. So I might stop my screen share if that's okay because I'm getting a little bit of Inception and where I'll find
this little oh I popped out my chat
that's my problem. Okay. Okay. That's fine.
Alright, yeah. I actually popped out my chat
and I don't remember how to get to it.
I'm struggling a bit.
It's okay you know what I can do. I'm going
to upload the video later and so I'll put the link to the training in there so people will be able to get it. Okay.
There is one more question which is are
q and Kdb+ open source and how are the requests for feature enhancements handled.
They're not open source. No it's actually a very very very
small code base and the so it's it's
free for non-commercial use so
definitely do whatever you like in your
own time but yeah it's not an
open-source software it's written in C
and it's all very very terse I think
even I don't know I've seen the glimpse
of it before and it did not look like
any C code I've ever seen but in terms
of feature requests it comes through us
here on the evangelism team anytime
people say or we'd like to see exploits
edge we feedback back in to our core
development team and we also have a we
have a number of kind of support groups
so there's a a support group makes the
time very dramatic but there is a Google
group for for people that you know are
involved with it or want to use it or
how many questions in the usage where a
lot of our more expert engineers will
kind of respond back and there's also we
have a number of meetups and stuff so we
well in in in different times they would
have been a much more frequent and
person thing but yeah we have a we have
different email groups for for those and
a number of different tools and I didn't
want to kind of get into too much today
but like an IDE tool and a front-end
dashboarding tool that are that are also
worth checking out. That is it for question.

### Thank You

So I want to thank you first of
all for turning off your air conditioning to
reduce the sound. Thank you so much. No problem. Thank you for joining us tonight and your presentation it was really great. No thank you all for joining and thank you
very much for having me I was delighted
to come and hope I hope it was helpful.
