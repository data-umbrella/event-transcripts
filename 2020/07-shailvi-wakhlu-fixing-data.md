# Shailvi Wakhlu:  Fixing Bad Data

video:  https://youtu.be/O5Z1-9Ohoro


okay so it's it's really great
my name is Rashmi Shaikh and I am the
founder of data umbrella I am also an
organizer for NYC hi ladies and I am
based out of New York City welcome to
our welcome to our session the mission
of data umbrella is to provide a
welcoming and educational space for
underrepresented persons in data science
we welcome allies to help us in our
mission and we welcome all different
skill levels we are on twitter at theta
umbrella so feel free to tweet and share
about the event and follow us also
there's a LinkedIn page for us where I
usually share job posting so you're
welcome to join there and there's
information on the website about a
discord for community I just want to go
over the code of conduct that you know
we're dedicated to providing harassment
free experience for everyone be kind to
others be professional and respectful we
really want to build a friendly
community here our Twitter is just to be
P at data umbrella and also at NYC PI
ladies and this is our meetup page so
we'll be posting I'll be posting any
upcoming events on the meetup page even
though this is webinar and it's
available to anybody around the world
its meetup pages like the central page
where the events are posted oh I want to
thank our speaker she'll be from joining
from San Francisco and I want to thank
our sponsor for providing this webinar
platform which is neo4j and I'm just
going to introduce Shelley I actually
met Shelby back in August in San
Francisco when I was there for the right
speak code conference Shelby is the head
of analytics at Komodo health and as an
analyst professional and former software
engineer Shelby has been involved in
shaping great products or companies big
and small for the last 13 plus years
she's worked on various analyses
previously she worked at Salesforce and
she I guess the really impressive thing
here
additionally is that she has worked with
a really large data a data at scale um
40 million plus users and then I think
you should be able to screen share now
don't get perfect Oh give me a second
goal all right can you see my screen
hey I equal to see my screen yes okay
perfect um okay thank you yeah all right
anyways thank you all so much for
joining in today
my name is shall give a clue thanks
again Reshma for the introduction and
today I am going to walk you all through
how I think that Sherlock Holmes would
have fixed back data and I hope you're
all as excited about investigating data
anomalies as I am so just to pick a
little bit about me so this is me as a
child I used to spend a lot of time
reading detective novels and after I had
finished reading one I used to go around
hunting in my backyard for cues I have
no idea what I was what mystery I was
trying to solve but one day I found this
big huge lemon as you can see it's
almost the size of my face
and I didn't even know we had a lemon
tree so for my five-year-old for my 11
year old self this was actually the most
important discovery I had ever made at
that point and it just convinced me that
I'm gonna go on to do very exciting
things in my future and I don't think I
ended up doing some exciting things I
worked with a lot of different companies
of different sizes mostly in analytics
which I've been involved in for almost a
decade but even though I started as an
engineer and now I am the head of
analytics at Komodo health where I lead
a team of eight data scientists so today
we're gonna talk about three things one
what is
bad data and why should you care about
it and how do we actually fix it so
sorry bad data is essentially my
definition is that it's inaccurate
incomplete or misleading data and
essentially what that encompasses is
anything that's wrong anytime there is
missing information or there's duplicate
information but it's not actually tagged
as such or there's some information or
data that's low quality that's
incorrectly transformed that can imply
something different than what what it
really means all of that comes under the
umbrella of bad data now this is
obviously just my definition I'm sure
what you really want is a scientific
definition and this is this is the best
that I came up with bad data is anything
that makes you want to throw your
computer across the room because it just
makes everything terrible so I would
like to call out that what bad data is
it is just if it's not something that
you want to see or if it's not something
that you feel good about like that
doesn't make it bad data it's it still
has to fit the requirement of it being
inaccurate
in some way and just because you don't
like what it tells you it doesn't make
it bad so with that distinction
you know let's actually walk through a
couple of quick examples of how I think
bad data actually manifests so one of
the most common things that I have seen
is that you know you're trying to pull
up revenue numbers because revenue is
important and you have a sales force
table that says you made 32 million
dollars last year and you have an
internal table that says you made 35
million dollars so automatically the
question is well which one is right and
you know that three million dollar gap
that is going to decide whether your
company invests in more snacks for your
kitchen for example so it's a really
important thing to sort of solve for and
you want to make sure that you trust the
data that you have and if you don't
trust it like you have some caveats
attached to it and things like that
the other really common thing that shows
up is just you know something where the
analysis just looks really suspicious so
in the in you know in this new chart you
can see that you it shows you revenue by
country and it shows you you have twenty
five million dollars that you made in UK
and then you note that you're actually a
company that's located in North America
you haven't even ever marketed in Europe
see all the North American countries
make sense so you know who are all these
people in UK who are buying your product
it just doesn't make sense that it would
be the biggest country where you'd have
revenue from so things like this they
basically you know are a starting point
where you start wondering what's going
on and you know what is this bad data or
like where is all this information
coming from and the next logical
question that comes up is you know where
where is this bad data getting created
created in the first place so for me
like the way I think about it there is
essentially a life cycle of data that
has many phases and each of those phases
has some inherent risks that are
associated with it where bad data can be
introduced so I know there's a lot of
information on this slide and I'm going
to try to break it down I put it as one
visual because I actually personally
have this printed out on my desk because
I like to refer to it just to sort of
fact check you know any investigation
that I'm struggling with I try to make
sure I'm covering my bases
so say let me let me walk you through
what's actually in here so on the on the
left you see the the five different
phases of introducing bad data so the
first one that we start off is is just
the definition this is where you know
the data team and the product team are
reconciling and they're saying what are
the features that we even want to
consider as one coherent unit and then
what data requirements do we sort of
associated with it
after that you go on to login where you
actually translate some of those
definitions that
you had created in the previous step and
turn them into actual code that you can
use to log and store that data after
that you are transforming that data in
some way and what you're essentially
looking at is you're looking at your
business rules and you're applying those
rules to do that tracked data so that
you can convert it into a format that
actually makes sense that is actually
usable after that comes the fun part
you're actually analyzing it so data
scientists typically they have to
interpret the data based on you know
actual business questions that they're
trying to solve for and that is that is
where a lot of the action happens
and finally after this you actually
share out your results and it can happen
in a bunch of different ways it can
happen in the way of an ad hoc analysis
or some some self-service reports things
like that and all of these these things
are shared directly with stakeholders so
during all of these phases I've you know
on the on the right I've kind of
highlighted a few common things that I
observe in each of the phases like which
are just according to me they're the
most they're the most logical places
where something goes wrong
so I actually look at all of these
things just as a as a sanity check when
I'm trying to investigate what happened
I'm going to walk you through a couple
of them I won't walk you through all but
because some of them I'll be discussing
later when I'm talking about fixes so
you know some of the most obvious ones
all most common ones that I see is
actually in the definition stage so you
know when we when we think about
features anything that we are trying to
track it has some sort of a definition
associated with it and how we define
that feature can make a lot of
difference in to what insights they're
able to get from it at a later stage so
if you don't evenly apply the same you
know same sort of intention behind some
of these feature definitions it can get
quite confusing later on so an example
here is that let's say you
you know your product team says I want
to track all clicks on this page any
click that happens I want to check it so
that's so pretty
like it's a pretty all-encompassing
definition but you also have you know as
a team that's dedicated to tracking
things that occur on mobile and so in
mobile environment they'll be like yeah
I want to track the chicks there too so
initially you logically think that all
my all my clicks on the on the website
are being tracked and some some subset
of them would have happened on the
mobile but if mobile team decides to not
track all the clicks and only like three
of the buttons that you can possibly
click then you have definitions that are
not evenly aligned because you'd assume
that you know the the website clicks are
still kind of the superset of everything
but you'd expect that the mobile subset
is a full subset for all mobile clicks
but it's actually only tracking three
three types of clicks so that can cause
issues because anybody who's done this
long enough knows that they'll always be
that one person who'll say I want that
one click on mobile that nobody's
tracking like give me information on
that like you know you're giving me
information about everything else what
about that one so the more thoughtful
you are upfront about like making sure
you're tracking everything evenly it'll
it'll just be easier in the in the long
run the other example is at the analysis
phase so you know I think that's again
one of the most common things that
happen that you just don't define the
problem it's it's very ambiguous because
especially when we're you know one human
talking to another human you know you're
two separate humans so you're always
gonna have some things that you're not
where you're not aligned where you don't
understand each other and you know if
you're talking to a product manager they
can make certain assumptions that like
oh I'm sure they already know this and
then you can make certain assumptions
like oh I already like of course they
know that this can't happen so if you
don't actually clarify some of those
that can result in some very tough
consequences you know you may end up
spending a lot of time doing some work
which has to be redone because there was
an incorrect assumption in the first
place or worse
maybe the error never gets discovered
because you are all you're both calling
in the same thing but you're actually
doing something that's completely
different so these type of examples you
know you can you can kind of look
through the remaining ones later but
these are some common things that kind
of show up all right so why should
organizations or you know anybody even
care about all this bad data now that
we've seen a couple of ways it showed up
so I think inherently the big takeaway
that I have seen over the years is that
bad data is just costly it's costly at
every single level across the company I
think you know to start with the people
who are working who have to deal with it
it is it hampers their productivity
if you don't upfront spend that time and
effort in trying to keep things clean
and it affects our morale because they
feel that you know this is this is just
I spend so much time doing something I
don't want to do it can also affect it
can cause liabilities you can sometimes
end up sharing information that you had
you're not supposed to or you shared
incorrect information that's specially a
problem if if you're a public traded
publicly traded company and you had an
earnings call where you said I have you
know X number of monthly active users
and then the next earnings call you're
like well just kidding it's actually 20%
lower because I made a mistake that's
not gonna look good and you might your
company might actually get sued for for
misleading shareholders so bias of
course is a big problem you know if you
if you have some if you have some data
that's inherently biased and that's not
known to you like that's just it's it's
it's a it's it's a it's a issue because
it can cause harm to people based on
whatever decisions are being made with
that data
and overall you know you can also just
straight-up lose revenue so if you have
a bad data pipeline and data goes
missing maybe your marketing team
doesn't have leads to follow up on and
that can lead to material revenue
revenue costs overall I think the
biggest the biggest reason that I think
this is important is also because it
lowers trust the minute your customers
find out that there is something sketchy
going on with your data that can often
be just game over for you because if
they do if they don't trust your data
they don't it had a really trust you the
one thing that I again like to sort of
highlight a little bit more is that I
think you know besides all those other
reasons which have a cost attached to it
I think just the fact that data
scientists have no moral because it's
something like this is reason enough for
people to care about it you know data
scientists have to find the error find
the source validate cross checking it so
it's a lot of work that goes into
resolving some of these issues and I
think inherently it very much is a part
of a data scientist job to do this but
inherently they feel well my skills are
so much you know there's so much other
cool stuff that I can be doing and so
everyone wants to be they everyone wants
their talents to be used in an optimal
way and you don't want people leaving
leaving a job just because they're
always dealing with dirty data issues so
good so next you know how do we actually
solve it my my thought here is I think I
think we solve it by thinking like
Sherlock Holmes and for for those of you
who are not familiar with him Sherlock
Holmes is a fictitious character created
by Sir Arthur Conan Doyle he is arguably
one of the most famous fictional
detectives and there's a lot of books
and movies about like that character so
check it out if you haven't had the
chance to so why did I actually pick
Sherlock Holmes
for you know why did I pick that we
should emulate his his style so I
actually think that his style of solving
crimes is very relevant to data
scientists even though hopefully we're
not solving crimes just data issues but
I think inherently we're doing
investigations and I think a lot of his
personality traits are very good if you
think of a philosophy of how data
scientist should think I think it's very
it's it's it's a it's very relevant and
inherently Sherlock Holmes is always
presented as a very very data-driven
character so I think his methodologies
are actually extremely relevant and the
three sort of traits of his that I
picked which are sort of you know larger
bucketing of of some of his personality
are deep observation scientific method
and pattern matching so let's dive into
a little bit of each of these and see
how they sort of manifest so his deep
observation is so there's a very famous
quote that Sherlock Holmes says in one
of the books he says he says you see but
you do not observe and that's a that's a
that's a very interesting difference
distinction to call out that if
essentially when we have data in front
of us our default is to look at it and
absorb the information ances but when we
actually start observing it more closely
we gain more nuance by just interacting
with that information as an active
participant and that is a skill that I
think is worth building on so some of
the ways that you can build on that
skill is to just be fully present and
very mindful so when you're mindfully
interacting with not just the person who
you know your stakeholder your your
business partner like people like that
like when you're mindfully interacting
with them you're more engaged you are
not going to be distracted and that will
mean that
don't you don't miss out on something
that's critical for you to you know be
able to solve the problem at hand and I
think it's one of the best ways to have
impact the other way to improve your
observation is to be an active
participant in with whatever you're
doing so you know one of the you know
one of the fun examples that they called
out is that you know when Sherlock
Holmes was given you know he said they
said oh here we found this note and this
is a clue so he didn't actually just
read it
he didn't just like you know look at it
he he actually smelt it too because he
said you know smelling it is gonna give
me some extra insight and I just reading
it doesn't doesn't gave me and that is a
very interesting thing because you're
you know you're actively participating
with the information in front of you
you're you're being inclusive you're not
just saying well this is how I normally
look at data but like you're trying to
be you're trying to be thoughtful and
getting into the weeds of how you can
use use information in in in to tell you
different insights the next thing again
about improving your observation is to
structure your thinking so this one is
you know I think like all good engineers
have to do it you have to just be
structured you have to keep good
documentation I think for data
scientists it's especially relevant
because you know sometimes during our
analysis we'll make some assumptions and
if it's not or we'll make some decisions
rather and if it's not an intuitive
decision like why did we make that
decision
maybe we made it because we spoke to a
colleague who pointed something out and
if two months later we'd forget why we
why we decided to go this direction with
our analysis it will be really helpful
to you if you have actually sort of
documented that somewhere so that even
you yourself are not struggling with
figuring out why you why you did
something specific so you know and and
like being structured also means that
you you try to look at information and
sift through it and say like you know
let me step back and
what is actually useful to me what is
just a red herring or something that's
kind of taking me away from what I'm
actually trying to do here the next
character trait was scientific method
and here again you know the famous quote
here is when you have eliminated the
impossible whatever remains however
improbable must be the truth it's a very
it's a very scientific way of thinking
about it cuz we you know we have to
regard facts as truth even if we can't
see it and if the most likely answer is
not the answer and the impossible answer
is not the answer
we have to give the improbable answer a
chance to prove itself and we have to be
truthful saying that if this is where
things are pointing me I have to give it
a shot
to sort of see if that's actually true
or not so here again you know you can
build on this scale by just generally
avoided avoiding the trap of bias and I
think you know a lot of times it's it's
very easy like it's human nature that we
are the if we're given if you're given
something that makes our life easier so
someone States an opinion which sounds
kind of correct like it makes our brain
is programmed to just attach to it
because it makes our life easier so but
we should we should you know
purposefully step away from that because
a lot of times opinions are stated as
facts and people then there must have
been tons of companies that you know
said hey our monthly active users just
never go down like we're a growing
company and then coronavirus hit and of
course a lot of companies lost lost
users and if they had treated that as a
fact that like there's just no way that
we can ever have less people coming to
our site you know they would have just
found it way harder to be like well you
know why is this happening now of course
in this example I'm assuming people
weren't living under a rock and they
kind of heard about the covert situation
so hopefully they would have been able
to piece things together but you know
there could be some situations there you
just don't know what's going on
and the other thing sharer is you know
we tend to the information that is
available to us like the information
that's in front of us that we can see we
tend to weigh that more heavily than
what we don't have access to so for
example if I have access to the signups
that occurred on my website but I don't
have access to the actual you know
volume of people who came to my site and
bounced out without signing up I will
just look at my signups and be like yeah
it's going really well
you know I'm I have so many people
coming to my site but the fact is while
that singularly might be true if you
just have had a lot more people come and
yes overall your signups are going going
higher but your rate of conversion is
actually lowering your you're missing
out on key information by like just
being biased towards the information
that's available to you at that point
and then you know the last way to build
this skill is to you know regular
science facts like build a hypothesis
test it out if you have multiple
multiple options to go with you rank
them pick the most likely one first to
test out and keep kind of validating
each of them until you find something
that fully explains what issues you
might be having the last skill was about
pattern matching so you know there is
nothing more deceptive that an obvious
fact as Sherlock Holmes said and it's
it's it's because you know the
interesting thing was Holmes was
actually considered to be very good at
understanding human behavior and
predicting human behavior even though he
was considered someone who wasn't
actually very good at empathizing and I
and that may seem you know not very
aligned but the sheer fact is that when
you understand when you understand
situations people all of that better you
are much more easily able to find
patterns and you know that hey this may
present as an obvious fact but it's very
common for people to sort of you know
stated as a fact but
it's not it's not true so like let me
dig into it a little bit more so a good
way to improve on this skill is just to
be very objective when you're trying to
parse information you know understand
the people that you're dealing with
understand their motivations understand
that fears those things could be very
different than yours
so if you have stakeholders you know if
you have a product person and a
marketing person for both coming and
telling you this data looks wrong they
might have very different opinions on
where they think the problem occurs and
you have to still separate yourself from
you know from from sort of those two
conflicting conflicting directions and
pick what what makes the most sense for
you to investigate first because you
because you know otherwise you won't be
objective and you won't you won't stay
focused on the truth say as you hear as
you hear opinions and ideas I guess
always good to understand that also for
future reference but try to sort of like
parse the right information from it the
last way to sort of improve on that
skill is to just in general widen your
knowledge base so you know as as a data
scientist I think it's extremely
important that like obviously we have to
get really good at understanding the
data appreciating what it does but the
other part is like if you if you do an
equally good job at also understanding
the product understanding the users
understanding how your marketing channel
works and things like that it can
actually allow you to make a hypothesis
much more easily when you sees things
that are going wrong and you'd be in a
better position because you would have
seen some odd things that happen which
if you just focused on the data you
wouldn't have access to so it it
basically allows you to consider you
know factors outside of just just what's
in what's in front of you all right so
hopefully they're all made sense so far
now we are actually going to walk
through an example so you know we
hopefully we understand a little bit how
Sherlock Holmes
and how we can apply his mindset to our
own problem-solving techniques so now
I'm going to walk through a simple
example where we will try to use some of
those philosophies that I kind of just
highlighted and for the sake of
simplicity I am going to go with the
assumption that we eventually have one
warehouse where we store all our data
regardless of where it comes from
so whether it's initially coming from
Salesforce heap website logs whatever
all of it comes and it sits in one data
warehouses I want to make life my life
easier and just compare two data sets in
the same place so this is this is
typically how they how the question
starts and I I hope a lot of you can
relate to this specific example which is
you know you have a colleague maybe
they're in marketing or something and
they come to you with the question they
say the number of sales in May I pulled
one number from Salesforce report and
today they reported something else in
all hands and you know what's the deal
why they why they're not matching so
obviously a lot of things could have
gone wrong and for the purpose of this
example we are actually going to pretend
everything that could go wrong did
indeed go wrong and yeah I like that you
know of course if you've been at a
company for a while or if you've
interacted with that same data set for a
long time you'd probably have you'd
probably start building out a good idea
of where the problem might be but for
this example yeah for this example I am
going to assume that you just joined two
hours ago you know no one you know
nothing all you know is your snowflake
warehouse password and what the
offending data sets are so before we
begin actual coding some simple sanity
check lists to just examine the facts we
are talking about two different numbers
basic questions are they even supposed
to represent the same information
sometimes numbers may be called the same
thing but they're actually not supposed
to
represent the same thing at all so an
example would be that you know people
may be just saying sign ups but maybe
the sign ups that are stored on sales
force on the Salesforce platform are
referring to sign ups that need a
customer success person to reach out
whereas the sign ups that would be
stored in your internal table would be
all sign ups ever so you know you're
both calling it sign ups but is it
actually all sign ups and the same
amount the other thing to think about is
I think this is actually super super
common but you know are they from the
same time frame and is your refresh data
refresh cadence for the two places that
you're looking for information similar
and that is I mean hands down
one of the most common things that
happens that like one report could be
set to begin at the first of the month
the other report is set for the first
Monday of the month or like you know
they're set to different time zones just
just things like that like they're all
time frame related things and those
things you know again get it out of the
way quick because that is that is
usually a very common reason for
misalignment to occur and the last thing
here are sanity checklist wise is just
human error
you know there's I mean I think all of
us no matter how foolproof we make
something there's always gonna be some
unintended use there could be some typos
there could be some extra filters
there's just like basic things that are
unintended how you intention for them to
be used and then the last sort of
checklist before we get into the coding
is you know just understand understand
the data set and understand what the
problem is before you fully begin so
here again the basic questions to ask
you know what rules where each of the
data sets built way like is it just
purely raw data and presented as is or
were there some transformations applied
were there some business rules applied
on top of it a lot of this information
is unfortunately tribal knowledge and
you again as a good data scientist
and as a good citizen you have to you
have to actually start documenting some
of these things so that other detectives
have an easier time and it's um it's
totally worth the time the other common
thing is the drain off the data set so
you could very often have something
where again they looked like they have
the same number of columns but maybe
they're both aggregated at a completely
different Lane and that could also
result in some unintended things that
you can't see and finally is there a
pipeline issue again that's also very
common that like you know the pipeline
just breaks for a couple of hours or
something like that and you're missing
data from a specific like chunk of time
or or something weird is going on so now
let's sorry I just have some more okay
so now let's actually let's actually get
into some code so here's what a dataset
looks like it has an ID column and
obviously there might be other columns
as well but these are the relevant ones
we look at there's an odd order date
there's a region and there's a sales
amount and that's sort of the basic
thing that we're dealing with so the
most obvious check to start with when
you're comparing two different data sets
to see what's going on with them you
know are they the same or not
after answering all those sanity checks
that we just did the first thing is do
they have the same number of rows that
can usually tell you a lot of what's
going on and so you know the simple
thing there is just select count from
from both of them compare that number of
course you might decide to add like a
where clause if you're looking for a
specific month or a specific region or
whatever the difference is showing up
but this is your absolute bare minimum
starting point after that if they if
they don't actually have the same number
of rows first thing is let's look for
missing information so in this example
the ID was a unique column so we're
basically gonna look for we're gonna
find the missing ids and we're gonna say
you know which eye
we're going to do a full full join of
the two tables and if the ID is null in
one of the tables that's the table that
it's missing from so this you know the
second query should essentially give you
a list of all the missing IDs and which
ID which table they're missing from and
once you have that information we will
discuss few different ways you can go
about it but that should give you some
information the next step you know I
think even if you did find some missing
information I think it's still as long
as like I think it's still useful to
look for duplicates anyways because
again pipelines do weird things and
funky stuff can happen so here again
you're simply you know getting all the
all the I all the IDS you know grouping
the IDs to get a count and you're
basically looking for any ID that has a
count greater than one from each table
and you're unioning those two those two
sub-queries and getting your final
result that gives you the final answer
so this way again you'll have one one
result that will give you all the
duplicate IDs that are that are missing
so that are that are duplicates and and
which table there are duplicate in so
these these queries that we have so far
like of course there could be a lot of
like extra clauses that you can build
into it but just kind of sharing it as
examples of life starting points of how
to start even thinking about some of
these issues next and you know sort of
the last sequel level check that I
talked about is just doing a check at
the dimension level so here is where it
gets interesting and where your
familiarity with the data can really
help but again in this example you're
new to the companies you have no idea
what's going on once you've sort of
eliminated some of the basic things you
want to start breaking things down by
you know one dimension at a time and
seeing you know is there a case where
things are consistently off across
dimensions or it's only one dimension
where there's something
gone wrong so like for example in this
query I am looking essentially for
regions there the region the sales the
sum of the sales for a region in table
one is different from the sum of the
sales in region two and in the same in
table 2 for the same region and this so
that's why I'm only doing like I'm only
looking for I'm only gonna it's only
gonna result in the rows that have that
have a difference and that is
immediately gonna tell me like if I see
all the regions then the problem is
either on a different dimension or
there's something else going on but if
this data shows me that oh only region
that has a problem is say the East
region or something then that
immediately tells me that the rest of my
pipeline is probably fine or my rest of
my feature definition is fine but at
least I know to narrow down that I have
to go do something about the East region
because that's where my problem is
showing up and like you like I said like
if if the if all the regions are equally
off then you break it down by a
different dimension maybe it's the
product or something else but the point
is to keep doing those cuts until you
find something where you have a step to
dig further so this is you know these
are obviously I mean these examples have
this example has been simplified to sort
of give you a give you a taste of what
what what this looks like but you know I
I expect that people will as they become
more familiar with datasets they will
build their own scripts and write their
own queries to resolve common problems
and I think you know you should ideally
make these things modular so that you
can convert those code snippets easily
and share them with the you know share
them save them converted into reusable
modules so that you can like change
change things and and kind of go around
it and you can also convert some of
these things to visualizations to help
you spot errors faster so for example
like in my you know in in in one of the
places I used to work at like I had
these
like just kind of ready to go cuz Elvis
knew where the pipeline would break and
it was a different team that had to fix
the pipeline so I just had to provide
them the proof that the pipeline was
broken so I had these scripts is ready
to go and when it wasn't a pipeline
issue when it was a feature definition
issue I would have like I would go
through this because that was the most
common thing and then I would have
something else to go through those I
knew that okay for feature stuff I write
different scripts or I have different
filters or some or something like that
and yeah you can you can kind of like
build on these as you as you get more
comfortable with the data so to wrap it
up I think one of the things to keep in
mind is that you know as as we saw
through a bit of the examples like
prevention is a lot better than cure and
you know a lot of the sanity checks that
we do before we before we do anything
before we look into stuff like a lot of
it comes into things that are easy to
prevent if you do it in the beginning so
if you're as a company committed to
reconciling on terminologies documenting
stuff making sure everybody is data
literate it makes your life and
everybody's life a whole lot easier and
I also think like automating stuff is
extremely important like you should not
have to do anything manually if you're
if you're doing it more than once then
by all means be absolutely lazy and just
do it once then never do it again
and automate it because I think I think
that those that actually allows you to
be be more efficient in what's going on
the other thing is just simplify your
curated data sets so anything that has
way too much information that you don't
use is going to be very hard to debug
when a problem occurs because you just
have so many different things to look at
so keep it extremely simple keep it
aggregated to a level that you expect it
to work at and that way also specially
like like at my company we use snowflake
which is which is super fast but like
you know some of the old data warehouses
it takes a while to run some queries so
it makes sense
if you have something that's you know
simple and aggregated so that you only
go up one level if you if you pinpointed
the problem to like one one section and
yeah I think again like it's very
important to have an actual governance
standard and you know some sort of a
philosophy about who owns ooh art who
owns which part getting broken who's in
charge of reporting things things like
that I think are extremely are extremely
required and you should also have an
audit process so at some point you
should do some kind of a quality or you
know a data cleanup hackathon that that
is that is able to sort of address some
of these some of these issues so yeah I
guess you know overall like I think sort
of wrapping up the philosophy and the
methodology like you know keep keep
breaking down the problem into smaller
parts until you are able to fully
isolate where differences are occurring
and bad bad data is creeping up and you
know the the the truth is out there
somewhere like you just you just have to
sort of like keep finding a way to get
to it and yeah with that I I just wanted
to leave you all with some additional
research and reference material I think
there are some great thoughts that
people shared about like bad data and
also how to think like Sherlock Holmes
which you can apply for other things as
well and I also linked my own talk about
thoughtful analytics in case anybody is
interested it is also on my website and
yeah that's that's that's that's it for
today thanks so much for attending a
special thank you for asthma and data
umbrella for hosting me this is this is
extremely fun I haven't actually done a
technical webinar ever so this is
solving in-person services 10 fun for me
I hope you found the content useful I
will be taking some questions now but
also keep in mind that data umbrella is
going to publish a recording of this on
their website as well as on their
YouTube channel and I'll be doing the
same as well in about a month's time so
you know feel free to stay in touch with
me on Twitter and also if you have any
questions
I can answer them too right now yeah you
can hear me right yeah great yeah if
anybody has any questions if you just
want to post it on chat um we have about
ten minutes left in the hour so we could
answer any questions any questions or
any observations anything else that
you've noticed that helps you do we have
Rene Phillips here who is like she's
like very very involved in Postgres
women SQL and in the conference
organizing the conference as well and do
you show me do you want to put in the
chat the link to the careers page for
Komodo health yeah let me let me quickly
grab that thank you
what's the hardest data quality problem
I have faced um that's to be very very
frank it's so I go with the hardest one
first
honestly it's convincing people that
it's important which which should not be
a thing but you know I think I think
some organizations have very good data
hygiene and they know sort of all the
downstream issues that it can cause if
you don't notice these things up front
but I did work in an organization once
where it was just it was you know there
was just absolutely like there was a
wild wild west of like everybody just
kind of do whatever and you'll figure it
out later and it caught it cause it was
so costly because it took so many people
so much time to try to like you know
reset some of the things that were just
very very bad and yeah that was that was
pretty hard the most fun one I would say
is yeah I you know I I just I like I
like investigating stuff like
i i like having an analysis that I trust
so if there's something that comes up
which you know which I'm confused like
oh my why'd you know why does this seem
odd sometimes that entire investigation
is because I think there's bad data and
maybe at the end of it I prove that it's
not like this is legitimately what our
what our data is telling us that's I
think that's still a good outcome for me
because I think that whole process makes
me understand the data a lot better
makes me trust different parts of it a
lot better so I I do find it fun to have
these challenges every once in a while
because I think it allows me to engage
with things more Ruchika us how do you
take care of bias in the data when
historically there has been a lot so
that's an interesting that's an
interesting question I guess my first
question to that would be like how do
you know there is there is bias or is it
just that you're trying to make sure
that there is there is no bias so Arouca
I don't know if you had a specific sort
of thing in mind but I guess I'll just
give you I guess I'll just give you a
general making sure that there's no bias
okay yeah I guess I guess for me I am
always trying to look at the use case I
think you know whatever I'm trying to do
whatever I'm trying to get to as an
answer like I think honestly for me it
really comes down to talking to a lot of
people and kind of almost poking holes
at a problem like what are the what are
the ways this could go wrong well you
know we're we're doing something
unintended I actually in one of the
companies I used to actually sit go and
sit with the customer support teams
occasionally and like get them to tell
me like you know just show me examples
of what people are complaining about
about our software and you know that
actually started an initiative where we
would we would flag things which
seem like people just didn't trust
something that was happening like they
didn't they didn't think it made sense
and some of those things were I mean
there was like it was just there was no
reason for them to not trust it but
other things like it made sense and we
did actually do some investigations
where they're like yeah the reason why
this person said this looks suspicious
makes sense because there is there is
something odd happening there and that
doesn't make sense
milena what tools you use to clean up
the data so I think that for me depends
on what what I'm actually using so I
typically access most of my data in a
sequel warehouse and I end up doing a
lot of it there if I have exported it
out then I usually use art but again
that's just my preference my my entire
team is very much on the Pythian
bandwagon and that's that's what they
use yeah what additional functionality
and unique capabilities does snowflake
provide oh I have to tell you I'm very
biased towards snowflake I am a huge
huge snowflake fan girl when I was
joining Komodo health actually one of
the first question I ask them is do you
have snowflake and they said yes and so
I joined because my previous company did
not have snowflake and I was very
annoyed by that for the two and a half
years that I work there
snowflake is just really fast it's it's
it's such a it's I mean yeah I I'm like
I said I am amazingly I like to spend
less time doing stuff so I was on
hurting for awhile and those things used
to take me like 20 minutes to run a
query and then in snowflake that same
query would take a less than a minute
say I I I'm not paid by them but I do
like their to me quite a bit I have a
question for you I was thinking when
you're working with that many millions
of Records
do you often find those cases that are
you know just a handful that are
problematic and heavy it's is it like
finding a needle in a haystack or is it
something that really just sort of
breaks all your programs because it's
that exception yeah that's a that's a
great question so
you know some of the so some of the most
like often that I did these
investigations that actually at
Salesforce where the platform that I
worked on had 340 million users so it
was obviously yeah it was it was just a
ton of junk data that was generated
for Ford the stuff that we were using
and that was the time I did not have
snowflake so my queries would actually
take longer and then like that's the
thing that I got to like I think like we
had a little bit of an understanding of
like I think when I was a kissed able to
explain like here's why this data is
always gonna be slightly shifted from
this other data then people have less of
a problem like if they if I if I've done
that true once where it's like you know
we expect there to be a 1% difference
when you're pulling it from this source
versus this source because you know
they're they're out of sync they're
never gonna be insane there's always
gonna be a little bit of lag here or
something like that like then people
have then if people understand it
they're okay with it but if that shift
ever like really changes like suddenly
even from 1% it goes to 1.5 like if it's
crossed a threshold that we have
established as unknown then it warrants
investigation like what's what's going
on like is this something that's
breaking or is this really my data
changing and I think in that like again
the more time I spent with that data the
more sort of checks I built in one thing
I forgot to mention but like some of
these queries that I had pulled put out
I actually you know got some of the data
engineers to convert them into alerts so
that if some of those checks didn't pass
it would actually like things that I
knew were to be true like I would have
them coded into the things so that
before that data was even published it
would go through all of those checks and
if something failed it would not publish
that data set so that then I could go
and look at it and be like does this
look fine or does this not does this
require extra investigation and I think
that was really helpful because then
you're not on a totally by goose chase
you're actually you know you're saying
like sure here's what went wrong in here
that's what in pharma we used to call
those edit chicks yeah the same thing
yeah yeah cuz we have another couple of
minutes does anybody else have any
questions
awesome so thank you so much for joining
us I'm from San Fran's an Francisco
right your that's where you are I'm in
New York and the recording will be
available soon I'll send a message the
meetup group it's on our data umbrella
events page and Renee is asking if you
would like to do a webinar for Postgres
women New York City yes absolutely thank
you all right um thank you everybody and
watch our meetup page for upcoming
events have a good night awesome thank
you so much it's
