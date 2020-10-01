# Liz DiLuzio:  Creating Nimble Data Processes

video:  https://youtu.be/LZuJlZIDIbo

hey everybody welcome to
data umbrella's webinar um thanks for
joining us
um i'm going to go over um
a brief introduction about data umbrella
and then liz is going to do her talk
and then um for the q a for the
questions you can feel free to post them
in chat or in the q a tab and i'll sort
of
moderate the session and ask the
questions as i can
you know find a good place to interrupt
liz as she's presenting
now this webinar will be is being
recorded actually
okay a little bit about me i am a
statistician and data scientist
um i am based in new york city i am the
founder of data umbrella
and i'm also an organizer for the new
york city chapter of
pi ladies you can find me on twitter
with at reishmaest and i'm also
on github and linkedin with um with the
same username
data umbrella our mission is to provide
a welcoming and educational space for
underrepresented persons in the field of
data science and machine learning
um and we are a volunteer run
organization
uh you can find us on twitter at data
umbrella
hi ladies is a group for um python
of gender minorities really of all
levels of programming experience
i've included the link to our home page
if you want to go to the global page
it's pi ladies.com
and you can follow us on twitter as well
i want to go over the code of conduct
we're dedicated to providing harassment
free experience for everyone
um we ask you know that our participants
be professional and respectful
and also you know just also you know
this also applies to whatever
questions are posted in chat whether in
the communal chat or
private dms and we want to thank you for
making this a welcoming friendly
community for everyone
on the data umbrella website there are a
bunch of resources that i've compiled
about open source
about conferences about learning python
and r as well as accessibility
communities
um inclusive language and you know
responsibility
allyship there's there's a lot of great
resources and so i encourage you to
check it out um
when you have time after the webinar
so i we know we have upcoming webinars
we do about two webinars
a month and so the best place to find
out about upcoming events is on our
meetup page
um we also do share it on twitter as
well
um on linkedin is where um
there are um job postings and also
there's a linkedin
page where i share um resources um
youtube
is where all of our webinars are
recorded and uploaded so you can
subscribe to our youtube channel so you
get
notifications
and so now i'm going to turn over the
screen i guess to liz
um liz and i actually um work together
in new york
um we teach intro to our stats
classes in new york and that's how i
know liz and
so i'm really excited to um see her
online it's been a while and also really
really excited to hear about um
this is top sure thank you ishmael
and hello everybody um let me just
share my screen really quickly
all right so um as rachel has said my
name is elizabeth deluzio
um and i'm here today to just talk to
you
a little bit about my area of specialty
my area of passion which is program
evaluation
and in particular program evaluation in
times of crisis and change
and so for sure we're in one of those
moments um but i do think that even
beyond
um covid and our coveted era however
long it lasts
the skills that it takes to have really
responsive data and
data feedback for um data-driven
decision-making
i think is something that's needed all
of the time
no matter what time period we're in so
i think these things can span in
importance so just a little bit about me
before i begin talking about those
things
i if you're not familiar with what
program evaluation is
i think of it as applied research it's
research that's
for a purpose and particularly help
programs
um run more efficiently run um just more
intelligently and to learn from the work
that they're doing
i've been working with non-profits
governments and foundations
for over 15 years um i started off as an
eighth grade teacher
i taught eighth grade for six years and
i always say that
you know if i can teach eighth graders i
can teach anybody
and so today not only do i do work in
evaluation i
teach these types of tools and um
just data literacy skills in general i
have an mph and an msw
um so i in terms of jobs that i do i
work in internal evaluation for a
non-profit in new york city
called good shepherd services and we
serve children youth and families
about 30 000 per year i teach
quantitative methods at nyu i've been
doing that for about a year
now and then i'm a facilitator at
evaluation and learning consulting and
so that's who i'm
speaking from and who i'm representing
today
and so when it comes to evaluation and
learning consulting
they they do consulting work that is
specifically around
um evaluation work around strategy
and and building that work for
non-profits and governments
so that's me um and just in terms of
what i hope for you to get from today
um so three different uh goals for you
the first one is my favorite
participatory method for identifying key
metrics so if you're going through the
program evaluation
cycle the first thing that needs to
happen is okay we want to assess how
we're doing we want to assess
the impact that we're having and that
first step is
okay well how will we measure that and
so i have a
method that i like to use it is
participatory
in order to get as much feedback as
possible about what is the best way of
measuring
x y and z so then from there once we
have
a way of measuring it now we move into
this data collection and and i have a
specific tool that i want to share with
you that i
i like a lot um which is forms
and and it's very similar between google
and microsoft but either way this is how
we collect the data so we've identified
how we want to measure
what it is that we want to measure and
then we can create this data collection
tool
and i'll explain to you why this is
where i
tend to go if i need to collect data
and then once it comes to the reporting
phase how do we get that information
in the hands of decision makers quickly
my
go-to tool is google data studio which
is what i want to show you today
um and microsoft power bi is the
microsoft version of that
but either of those help with real-time
analyses so gone are the days of
printing out reports and making sure it
gets emailed or handed to somebody
um this allows somebody to have the
report in front of them
real-time data and they can interact
with it which is an extremely powerful
tool so again i'm going to go through
each of these phases too but
basically i want to take you in less
than an hour from
the beginning stages of how do i even
think about what it is that i want to
measure
to how do i collect that data and how do
i report on that data and what are the
tools that can help me to get there
so before i begin i just want to get a
feel from you
about what brought you here um so i have
a poll that i want to activate
right now um hopefully that pops up on
the screen in front of you
so just curious what brought you here so
of those three things which one
interests you and this will kind of help
me to
figure out what to spend more time on
than others
customize what i'm doing a little bit
so i'm not sure if you can see the
results but
if you can't it looks like
we've got oh people are still voting um
a and b are neck and neck and then oh
c just caught up though all right so you
all are
just interested in everything it looks
like it's a tie
a and b 14 votes and then c got 10 votes
um so that's great thank you appreciate
the feedback
and i will distribute my time evenly
as reishima said if you have any
questions as i'm going through
i'm going to go through each of the the
three phases i'll stop in between for
questions
but as they come up type them in the
chat box and if reishima
you know just speaks up and inserts them
into what i'm saying that's
great and otherwise we can wait for
those question
um sections to just make sure that your
questions get answered
so when it comes to identifying key
metrics
um so the there's a stage process that i
go through and it's a short one i do try
to make sure that
one i don't take too much time these
things could take
uh you know months um but that's not the
goal the goal is to get things done
quickly
and then i really work through an
iterative process
so we we do something we start
collecting because it's important to
begin
and then we can tweak along the way so
the first step is just to identify the
evaluation question what is the question
that we want to answer
um so examples could be what services
are we
are we providing right now we think we
know we told the funder that we'd be
doing x y and z but what are we actually
doing
and then how often are we doing what
we're doing
another question or set of questions
could be which services are actually
being accessed so we have these wide
array of services
what are people actually accessing and
then to what degree
thank you for sticking with us okay
um so just to go back i'm not sure where
i lost you all however um
just to run really quickly through this
slide again so in terms of
identifying key metrics there's the
evaluation questions that we want to
figure out
exactly what it is that we want to know
so once we know what it is that we want
to know and some examples could be what
services are being provided what's being
accessed who
is accessing them then we move into
who do we need in order to answer this
question in order to
figure out what our metrics will be to
measure
and figure out the answer to the
question and so some examples of people
who we might want to invite
into this event it'll be a couple of
hour
meeting would be programs staff funders
contract managers
analysts it could be maintenance folks
or people who work at the front desk of
the program
that's being offered be creative
the more people the better in my opinion
so the more minds you have on this the
better
chances you are to figure out the
metrics that are appropriate
for answering this question so
once this sorry i just wanted is your
mic
the same as it was before i think so
okay you can test that
um okay let's give this a try
markers those are the tools that you
want with you
if you're doing it online which it looks
like for a little while at least
that's what we'll be doing there is an
online intern
alternative called jamboard and if
you're not familiar with what that is
i did record a really quick tutorial on
google jamboard
um there's a hyperlink here um
and i will send out the link to these
slides afterwards or i'll ask reishima
to do so
so you have that but google jamboard is
a free
online resource i can demo it if we have
some time at the end and essentially it
has
post-its where it's a big board people
can add post-its move post-its around
annotate um and so on so it's it
simulates this environment of a post-it
um type meeting and then when it comes
to the main activity what we're calling
people together to do
is a three-part brainstorming session
and it comes from ido's field guide to
human-centered design so this is
based in human-centered design and again
this participatory approach that they
highlight
so number one the first step is to
ideate so we provide everybody
a stack of post-its if we're doing it
online we just ask people to write that
down on their computer or on a piece of
paper in front of them
we set a timer for five minutes and we
prompt them to generate as many ideas as
possible possible so
we're going back to this question if if
our question is um
what services are being accessed and to
what degree we will ask people okay well
if we were going to measure
something like that what are some
questions that we would want to have
answered or what are some data points
that we would want to make sure that
we're collecting
so we would give everyone five minutes
to just brainstorm on their own
after that we move into a discussion
phase where we have
another five minutes set up and we group
people into small groups again if it's
in person
it's about groups of three to four if
it's online i often use zoom so i can
have folks break out into breakout rooms
of
three or four people and that's when i
move them into google jam boards
and that's when i have folks share their
ideas
and they're looking for similarities
they're looking for themes
so if they have the exact same idea we
might have them
you know write a couple of post-its and
stack them up if they're starting to see
themes they might want to cluster them
together they might want to change the
color of the post-its to all be one
certain color
and again we're just kind of starting to
generate the group's opinion
on what it those metrics are that we
want to be collecting
and then the final stage is to come back
together as a whole group
and this is where we share if i was in
person what i would do is just ask folks
okay what was one of the more popular
metrics that you thought in your
group needed to be collected i'd collect
their post-its
i'd ask the rest of the room who else
had this idea i'd collect all those
post-its and i'd stick them up on that
big piece of poster paper
and i'd continue in this way for again
another five to ten minutes and i
i make sure it's time just that way the
best ideas the most popular ideas will
come to the surface during that
shortened period of time
and i am again looking for trends
looking for similarities looking for
what it is that the group is in general
saying
and the reason that i like this pattern
again it's it's um
consolidated we really make sure we
stick to those
that time period because these types of
meetings and again coming up with just
metrics can take a really
long time if we let it but what's
important is making sure that we begin
and so again making sure that we have
many people in the room many voices many
perspectives
we give each person their own time on
their own
so that you know the the person with um
the highest credentialing in the room or
the person with the most power the
highest position
is not the one whose voice makes all the
decisions everyone gets a chance to come
up with their own thoughts collect them
and then everybody you have your
post-its so
everybody is able to share what their
ideas are and each idea counts equally
and then that's how we cultivate where
um
what those metrics are all together so
that's
that in a nutshell do we have any
questions reishima from the group
just about that technique
there's so much more i could say about
it okay i don't see any questions in the
chat
okay so there's so much more that could
be said and you're more than welcome to
reach out if you have any questions
about it but that's in general
the method that i use to come up with
what those metrics are
so once i have those metrics it's time
to create this data collection tool
um and then let's do another really
quick poll
because i'm curious what it is that you
use
so when you're working whether you have
a job or whether you do consulting
do you typically use google microsoft
both or neither
okay great so i'm seeing a majority
google
which is great um and then i'm seeing so
that's six people at google
two microsoft three both
and two neither so google wins this this
round um
which is actually really great to see oh
i see more both coming in
great okay in the chat i'm just curious
those who use neither
or if you use something else please feel
free to share
it's also just a really great
opportunity for all of us to learn from
each other
so that's good to know um just to
understand where you're coming from
as i shared a little bit at the
beginning i tend towards
form if i can um
and here's the reasons why i use forms
because it's an easy way to collect data
um it's online it's free it's
collaborative so many people can get in
and edit it at the same time
i think it's extremely intuitive it's
very user friendly
it has a lot of features it can do the
basics for sure
um and then why i use this in particular
is if
in the end i know that my audience my
decision makers who need this data
are friendly to online live
visualization tools so if they're
familiar with dashboards and true
dashboards
then i try my hardest to make sure that
i use
forms whether it's google forms or
microsoft forms so that it can feed into
that live dashboard
and if that doesn't quite make sense
i'll explain more and i'll show you what
i'm talking about
but there are some drawbacks and i think
that's worth noting so again it's
i really believe there's no one solution
for everything it's just
for those of you who use both right it's
understanding
what the needs are to figure out what
the tool is that's best for what you
want to do
so there are some drawbacks to keep in
mind one of them is that you need a
google account to create a form honestly
that's not a huge drawback but if you're
not
into signing up for a new anything or
trying to remember a new password that
might be a deterrent
google accounts are free for those of
you who are not familiar
um what i will say a true drawback is
that there are not as many features
something like surveymonkey
so if you're looking for something that
has a really um
one polished look to it or two has
pretty advanced features you won't find
it in forms it's it's a basic
go-to it cannot branch questions
um only sections so that's worth noting
we're in surveymonkey
you know if if you answer a jump to
question nine if you answer b
jump to question 13 um
that is not the case for either forms
microsoft or google
what you do need to do instead is branch
sections and i'll show you what that
means so it has to be a little bit more
simple
one thing i particularly don't like is
that the templates and design options
are pretty limited so again it's a
really
basic thing it's not going to
be completely customizable so just
really quickly i'll show you what i'm
talking about
um so if you do have a google account or
when you sign up for your google account
there's something called the drive so
that's drive.google.com
so you can see my drive here um the menu
for all the google apps is right up here
in the top
um right hand corner and so you can see
all of the different
features here one thing i will point out
is jamboards is here
so it's hidden there and i didn't even
know i don't know how long it's been
around
i only learned about it maybe four
months ago and i love
it it has spread like wildfire among me
and my peers
but that's there for you to play around
with um
and then forms is also here and i think
yep it's on the same line
so if you click on forms it will take
you to the landing page of google forms
this is what that looks like up here you
can see some templates
and then down here you can see forms
that i myself have created
so i'll show you a demo um form that i
just
use exactly for purposes like this so
let's say that this is an evaluation
form
you can see um just you know basics
around
these sections that i was talking about
you create sections
and questions here in the toolbar
here's how you add a section here's how
you add questions
each of your sections can be their own
page so i just like to think of it
when you're chunking the questions maybe
by theme or by complexity of the
question
itself when it comes to adding questions
there are so many options which i think
is really
excellent um so for more qualitative
questions you have short answer and
paragraph options
for more quant you have multiple choice
check boxes
drop down menus um you know i've created
forms for hr departments
and sometimes they need documentation
uploaded there is a file upload which is
incredible and it can put it right in
your drive which is the first place that
we looked
um so it'll go right in there and it'll
keep it all in one folder for you
linear scale so that's your leicard
scale you can do that
multiple choice grids and checkbox grids
and then we have date and time
options there's lots of different
features
and it's pretty intuitive in how you you
enter your questions so questions go
here
the options all go here you can make the
question required
if you like or it can be optional
um a lot of customization that can take
place once you create your questions and
your sections
you can just click and drag to move
things around
and then you know there's some features
up here
you can change what it looks like you
can change this header image you can
change your color scheme
there really is a lot that you can do
with just this
free version of forms um
and then you can preview it so you click
on that button and you can play around
to see how it looks
you can see as i said each section
becomes its own page which is nice for
chunking
to not have people
get fatigued when completing your survey
and then in particular when it comes to
pulling out the data
there's this tab here for responses and
you can see
there are no responses yet but what it
will do is create
a summary some an aggregation of the
responses that you get for each of the
questions and then if you want to do
your own analysis
you can click on this button here the
create spreadsheet and that will allow
you to
download a spreadsheet or open it up in
google forms
sorry google sheets and do your own
analysis and create your own reports
and so as i said you could just end
there and you can do whatever reporting
it is that you like to do what i love
about this
particularly if you open it in google
sheets is that that sheet now becomes
live
so any time that somebody enters a new
form and they
they complete it they submit it it adds
a new line
a new row into your sheet and so anytime
you go back there it's got
you can see updated information being
put in um immediately which i think is
just really
helpful and so why in particular that's
helpful
is this idea of live dashboarding
so i'm just going to pause here before i
segue into live dashboarding and just
see if anybody has any questions again
this is a really
quick overview of forms so if you have
any questions about
what this is what it looks like how to
do something please feel free to
ask um there was a question from
about um can you provide an example
where you
did the key metrics identification how
was its reception maybe you might want
to answer that at the end of the
presentation since we're passing that
out
sure i can do that any other questions
about the
data collection tool um
i don't see any other questions
okay okay um and
you know i might as well just answer um
when it comes to the key metrics i
that is my go-to um i i teach this
methods to people so they can go out and
do it themselves
and it is my go-to whenever i'm helping
folks create
an evaluation system um
i can't say that i've ever had a bad
reception to it
although i can imagine there's some
anxiety that people hide because
they need to be involved right like
often we come to meetings and we expect
to just be talked to
and people to do the work for you
especially as a consultant coming in
they often expect me to just come up
with
everything um and so there is the
conversation of
it really it's an honoring of you have
the knowledge
i'm just helping to facilitate and pull
all of that out um and so in that space
i always ask for line level staff to be
involved so they're not necessarily the
one who pulled me into this program
um to do the work but now they're
involved and engaged in it
and quite honestly i think they love it
um i find that people really get
into these conversations because we're
talking about things that they're
passionate about this is their job this
is their life work
and so to be able to have me ask them
questions
and truly treat them as the expert
because they are the expert in their
content
then i i find that there's a really
hearty conversation i almost get
overwhelmed with how much information i
i receive
and need to sift through and find some
solutions too so i
i find it goes over very well please
feel free to ask follow-up questions so
that if you
you want to know more and or if i didn't
answer your question as you you hoped i
would
okay so then let me jump into
dashboarding and what that looks like um
and so i'll just
start by just a quick note about
automation
um because if anybody's even tried to
automate anything
whether it's you know live dashboarding
or something completely different
you know that this it can go very well
and it can also not go very well
um and so you know i love this this
um cartoon that just kind of
demonstrates
what not very well can look like um
which is
hey you know this quote i spent a lot of
time on this task i should write a
program to automate it
and at the top is what we imagine our
life is going to be like right so we
have our level of work which is right in
the middle
we know there's going to be an uptick
when it comes to writing the code or
creating this automation but then once
the automation kicks in
we're going to have all of the spare
time to do all these other amazing
things to enrich ourselves to
professionally
develop and then often
if not really thought through or it
doesn't have the support it needs
what can happen is what's down below
which is we have that
that level of work we write our code but
then we need to debug and then we need
to rethink and then we have ongoing
development
and updates and upgrades and it turns
out that you no longer have
the time in fact you feel more
overwhelmed than you did when you began
and so i say this not to scare and not
to scare you away from automation for
sure
but i do say make your decisions with
eyes wide open
and so as i've said i've i've tried
automation
that has not worked and then i've done
automation that has
truly saved me so much time and in fact
that automation
did take the form of forms into for me
it was for an organization that uses
microsoft so it was microsoft forums
to microsoft power bi and it saved me
an infinite amount of time and and folks
truly like
it is collaborative it is everything
that i'm telling you
and it has worked tremendously
so when it comes to dashboarding i also
like to just clarify what i mean by
dashboarding because i think that term
gets
used loosely and is not always
um true to what dashboarding is
so dashboarding is a tool and it
contains real-time information
and it that information is directed
towards decision makers that they
are equipped with what they need in
order to make
decisions it is directly connected to
one or more
database it automatically updates itself
and the information is shared via
visualizations
so sometimes people will call a printed
out report a dashboard
that is not a true dashboard it really
is this real time
information that people have access to
so when it comes to creating interactive
dashboards
when it comes to google if you're using
google
that is called data studio and if you're
using
microsoft it's called microsoft power bi
um and what i love about data studio in
particular
is that it is extremely similar to
tableau and power bi
tableau being one of the more famous
more popular
data visualization tools i would say
that if you know how to use one you know
how to use the other i've worked in all
three
and they are extremely similar
interfaces so i think that's a great
option and i
always encourage people that if
dashboarding is the way that you want to
go
if you either one are dashboarding
already with folks or that's in a place
that you want to take your organization
or your clients that i would always
recommend starting with google data
studio just because it's free
before you make this financial
investment in one of these other
two things i encourage you to start with
google if at all possible
mostly because um it's free and it gives
you the opportunity to bail out if you
if it's not working for whatever reason
um so free being another highlight i do
behind it easy to
learn i think there is the learning
curve i think it is generally
intuitive um so i say that
for it i think it's extremely easy to
share um you can share not only
you can create pdfs if you want to i
think that beats the point but
if you need to archive a certain amount
of data for a certain day
you can download pdfs and save them or
email them out
but you can also send a link so that
folks can just see the live data
at any time you can also um it has
the html code so that you can insert it
into a web page or somewhere else
it is collaborative just like any google
platform and it can draw from many types
of data sources which i think is really
powerful tools
um also so it can
pull from google sheets as i shared
already but it can also pull from any
database where you can obtain
a url and so it's very powerful in that
regard it can pull from sql databases as
well
there are some drawbacks though of
course again this is what i was speaking
to when
make your decisions with eyes wide open
you need a google
account to use i should just get rid of
that bullet i think that's silly but
it's worth knowing you need to make a
google account
um it does not have as many features as
tableau or power bi
so again i i don't i i think it's not
fair to call it training wheels because
it is its own
true full system but
i often think of it as training wheels
you start with
google data studio i encourage folks to
and then if you need more features
that might be the time to invest in
tableau or power bi
but i've seen organizations stick with
google data studio for all of their
needs
for extended periods of time and you
don't necessarily need to upgrade
it can vary security issues and that's
worth noting if you have
any sort of private data you want to
make sure that you de-identify before
you start
putting anything in google and i always
recommend that folks just speak to the
i.t
department of whatever organization
you're working with
to make sure that they don't have a hard
and fast
no google policy um and see if they have
any recommendations on how to keep the
data more secure
and actually i do think somebody told me
that if you have
a paid version of google um so for the
company actually uses google as their
their platform then it is within the
firewall
often of an organization so that too is
worth knowing
so a really quick demo for you um
so unfortunately and i have a feeling i
know why but i won't go into the history
lesson
um in your drive there is not an
app for google data studio
and so you would just need to type into
your
toolbar datastudio.google.com
and again this is free if you have a
google account you have data studio
so this is what this home page looks
like it's very similar to google forms
um so you see some uh
templates up here and then you can see a
couple of reports that i
had created here so i just want to look
at
the accident data with you um so what
this is
is accident data for
the northeast united states and it was
for
i think july to december of 2019 this is
just
open data that's out there on the web
and i had created a
dashboard just to demo what the
different features are
so you can see it looks beautiful it
really
can have a very professional appearance
to it this is what folks would look like
look at if they clicked into your
dashboard
so you can see five different tools just
here we have the ability to make pie
charts
we have the ability to make bar charts
line graphs
um and then over here too we have
so stacked bar is here and then um
just a single number so you can see our
record count the number of
accidents from july to december in these
four states
was almost 34 000.
and then if we the reason that this is
so powerful and that i love
using live dashboards so much
is that if we had somebody who wanted to
dig down and understand
more so say they wanted to understand
what the
monthly breakdown of accidents are for
new york only it's as simple as clicking
on the pie
slice for new york city and then pausing
and waiting and you can see when i hover
over it there are 20
000 almost 21 000 accidents that took
place so of the 34
21 occurred in new york city or new york
state alone
now there are a lot of pieces of data um
so it takes a moment to think about
but what you'll see as soon as it's it's
done
is that these bars will all adjust to
show new york city only
it's filtering right now so it's going
into the spreadsheet it's finding
only the new york city and new york
state accidents
and it's pulling out that data that's
related to it for these other categories
so now we can see
which um it looks like june had the most
accidents followed by october and then
closely followed by november
and we can see the change over time and
we can hover over and see exact details
um so it's it's this is the interactive
piece that i'm speaking to and you can
click on multiple pies at the same time
i can drill down further so if i wanted
to look at new york in june i could do
that
the the story goes on and on you can
also drill down
so um you can see here circumstantial
factors this is broken down
accidents that happened during the day
and happened at night and if i wanted to
dig deeper so
underneath that is okay well i want to
understand
uh the morning hours versus
full daytime versus evening versus
sunset um you can click on
say the day bar and it'll show you a
breakdown of more specific time periods
during
daytime hours and so that's called drill
down
versus filtering which is what i did up
here
so there's that and then the other thing
that i love
to show and it might take a moment to
load
um but um there are lots of features
i'll show you just the back end of how
to develop
this really quickly but um what we have
here is the ability to create a map
also and it is so easy so those of you
who really respect and understand
how challenging it can be to develop a
map um
not so much when you're working with
data studio it's as easy
as dropping in an app and you can see
here now what a story this tells
when we're looking at accident data you
can tell where the major highways are
it's so clear and
new york city is clearly a hot spot as
are the
what is that one the turnpike and the
parkway no this one's the turnpike that
one's the parkway coming out in new
jersey
boston area is a hot spot so
anyway that's the data visually
now if i wanted to show you the back end
really quickly
i'm going to click on edit again it
might just take a moment
to load and again if any of you are
familiar with tableau
or you're familiar with power bi this is
going to look
so familiar to you they worked very hard
to make sure that it's a very
interactive platform
um it has a lot of drag and drop
features
just going to go back to page one really
quickly and just show you
so up here is the main command area
when you begin you start with just a
blank
a blank screen um and you would
select add data so the very first thing
is obviously you need
to get your data um here's the option
for google sheets and what
happens is you'll click on that it will
take you to your drive
and you'll just find that sheet that is
the output from your google forms
once you have it connected the two are
connected forever i think this updates
every 15 minutes
so anytime a new form is put in within
15 minutes this data will be reflecting
that information
and then once you've got your data
connected and again you can connect
multiple data
data sets at the same time
there's this add chart feature and you
can see
how many visualization options there are
i've shown you most of them but there
are more
so you can insert just a general table
if you think that that's the
most valuable way to share information
sometimes it is
you can do donut charts you can do
different types of line charts and area
charts
scatter plots tree maps which is a
personal favorite of mine
so there are lots of options and then
once you decide let's say you wanted to
do a pie chart
let's say this was the one that i was
working on
this is where we edit it and make it
look the way that we want it to
so this list of available fields are all
of the
columns inside of my data set from the
accident data
and it's as simple as taking whatever it
is that you want to visualize so let's
say we wanted to create this
accident by states i would just find
state down here
and i click and drag it into the
dimension and then when it comes to
metric that's just asking you how is it
quantified so we'll represent the states
but how do you want me to quantify that
and then that is through the record
counts i want to know the number of
accidents for each of those states
and so again i would find record count
and i would insert it here
you can do lots of things after
you have done the basics so you can find
a different sorting method if you don't
like the way it's sorted
and then the style is where we make this
look
really professional so once you've got
the chart um
with the information that you wanted to
have you can come in here you can change
the number of pie slices you can change
the coloring
um you can add your data labels you can
change
uh the size of your font the font type
the
the font color you can just go on and on
and it's the same for all of these
charts
and so you know all of these things that
you see here from
the month the way it's spelled out
that's not the way it is in the data set
i wrote over
my data labels here you can specify
where you want them located um
it's just there's there's endless maybe
not endless but
a lot of possibilities about how you can
make this look
um so that you can get something that
looks really professional and is
something that
folks are excited quite honestly to
click into and explore
so that's my spiel for this any
questions for me
about data studio
there's obviously so much more to say
about it but i just wanted to give you a
little teaser
any questions reishima
i don't see any questions now okay great
thank you
um okay so that's those are all those
tools um i see we have a couple of
minutes left
i do just want to um do a quick close
out and then
i'll be here for questions um as long as
you are
um just in terms of you know what we
went over today we talked about
oh my favorite way of identifying key
metrics like how do we
capture the what it is that we need to
measure in order to answer our question
then i went over forms which is how
my preferred way of collecting data and
in particular if i want to have this
interactive reporting platform and so
that's google data studio
so just some final thoughts and tips oh
sure
there's one question from rose does the
dashboard access work the same way as
permissions to regular google drive apps
i if i understand your question
correctly rose yes it does
um it it interacts with
everything on your drive in just the
same way and
um if your question is around people and
their permissions
that is the same as well so you can
limit who can see what
who has access to edit versus who has
viewing access
but when it comes to pulling the data
it needs to be within your drive
or you need to have a hyperlink to
that that sql database or that
you know other platforms database
so just in terms of you know final
thoughts um
words of advice despite any types of
limitations
i think that google forms and data
studio are quick they're flexible
as i've said i've had tremendous success
i had to help organizations
set up just really quick just covet
data um around who was being affected
and where and when and
all sorts of things and and these
platforms made everything
so easy to communicate at real time
they're excellent training wheels for
other paid programs as i went over
uh i do think that m e is as much an art
as it is a science so we love to think
of research and data
and data analysis as so scientific and
just
100 logical linear but there's an art to
it and anybody who is a true
um math person will admit that
that there is art too and so with that
in mind
it is really important to have a nimble
and iterative design
so not something that takes months and
months and months to develop and lots of
money
only to find out that it's not working
for you i really
am an advocate of getting started
getting something going your most viable
product right
minimum viable product and then going
from there and building on it from there
make any creation process as
participatory as possible i think that
too
helps to eliminate later down the road
when you realize this is not working the
way that we planned on it
too um and then
yeah those are my my big questions or
pointers
for you and then just one more question
for you i just activated the poll
which is what do you want to learn more
about is there anything you want to know
more about
so identifying key evaluation metrics
there's so much more to talk about when
it comes to that data collection
methodology and tools
creating interactive dashboards other
data related skills
and other evaluation related skills
good so rachel this is good feedback for
you too for future
um webinars but it looks like
um creating interactive dashboards is
winning
with three votes other data related
skills is high too
oh there's a three-way tie at the moment
as well as identifying evaluation
metrics
um creating interactive dashboards okay
great so creating interactive dashboards
is the most popular
followed very very closely by
identifying evaluation metrics
and other data related skills but
somebody wants
everything so that's good to know too
um so in terms of how
i can help and would love to help with
all of these things i'm going to close
this poll really quickly
um in terms of continuing your learning
if it was
identifying key evaluation metrics that
is of interest to you
i do so during this coveted time i
normally teach all these classes
in person particularly in the city of
new york but i'm leveraging the internet
um and this time that i have to
develop more so as i said evaluation and
consulting
learning consulting is about teaching as
well
and so we're developing self-paced
online classes
as i shared earlier it's it's micro
learning so we focus on having classes
that are five to seven minutes
long at most um and they're just little
little um skills that we teach
and then the class just is just made up
of that so you can direct yourself you
can
pick and choose what it is that you want
to learn and and just move at your own
pace
so we're developing um a class that we
teach in person
to be an online platform you can
pre-order um
and then we have live online classes too
so you can sign up for the next
live one same thing goes for data
collection
same thing goes for interactive
dashboards what i will say is we have
both the um data collection and
interactive dashboards online already
and there's safe
self-paced version and i have this
discount code for people who attend our
webinars as a way of just saying thank
you and we want to
to empower you to learn more so if you
use
web50 it'll give you 50 off anything
whether it's a live class or whether
it's the self-paced model
so then when it comes to other data
related skills as rachman
shared we've met each other through
teaching excel
or i'm sorry r but we also teach excel
python sql qgis so if you're interested
in any of those
let us know we're creating that content
again
recorded and then we have live sessions
periodically
and then when it comes to other
evaluation related skills or really
anything if you just want to
talk i'm so happy if you can click on
that hyperlink there
to just look at my calendar find a good
time that works for you and we can just
talk i've had people who want to
troubleshoot things who
just want to know more about you know
the way that i
um find key evaluation metrics whatever
it might be
i'm more than happy to have conversation
and we can go from there so please do
that
um again i'll i can ask reishima to send
out a link to this powerpoint so you
have
all of these hyperlinks easily
accessible to you and then just for me
the the website is here it's avalarn.com
that's our company
my email is right there and my twitter
please come find me
please reach out i'm so happy to engage
with you more these i'm so passionate
about all these topics and
excited to find a community that is too
so
thank you for your time i so appreciate
it and
um i hope all of you have a good day and
if you have any questions
i'll be here for a few more minutes
liz thanks so much um what i will do is
once the recording is available
i'll upload uploaded to youtube and i
typically um include a link to the
slides in the description of the video
so that's the best place for people to
find it
um and yeah we can hang on for a couple
minutes and see if anybody has any
questions
before we close it out
okay
it is on the hour and people depending
on if they're taking their lunch break
for east coast time they may be um
heading out
but yeah if anybody has any questions um
feel free to post them in the chat
um this thank you so much for the
presentation it was really great
i um i personally love google data
sodium i put it i love the interactive
um
dashboard i love being able to see what
the data point numbers are and just
putting together um you know a dashboard
very quickly
agreed and it is it is that easy to put
it together quickly
you can get something in the hands of
people as quickly as they want it
right all right everybody so there are
no questions so we
are going i'm going to um sign off
and um thank you for joining us and the
recording will be available soon
thanks

