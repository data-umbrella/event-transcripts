# Nick Janetakis:  Creating a Command Line Focused Development Environment

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2021/21-nick-command.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/274778387/
- Video:   https://youtu.be/y4fYxmE0HZM 
- GitHub repo:  https://github.com/nickjj/nyhackr-cli-dev-env
- Slides:  https://github.com/nickjj/nyhackr-cli-dev-env/blob/master/nyhackr-cli-dev-env.pdf
- Transcriber:  ? [needs a transcriber]

## Resources
- Documentation:   

## Timestamps
0:00 -- Intro
7:14 -- [Talk starts] What we're going to cover
9:44 -- A few practical demos of using tmux, vim and other tools
16:48 -- Parsing CSV sales data on the command line using a few Unix tools
23:44 -- Picking a terminal on all major operating systems
25:55 -- Comparing shells (sh vs bash vs zsh vs fish)
29:22 -- Configuring your Bash profile
32:29 -- Configuring and accessing your Bash history
33:58 -- Creating and using Bash aliases
36:48 -- Configuring your prompt (including ANSI escape codes and git branch)
43:25 -- Efficiently searching your Bash history with CTRL + r and FZF
47:39 -- Setting a Shebang and striving to be POSIX compliant
49:42 -- Using and configuring tmux
1:03:32 -- Rapid fire descriptions of a few useful Vim plugins that I use
1:08:00 -- Going over what dotfiles are and how to install + configure everything
1:13:35 -- Main takeaway of the talk
1:14:46 -- Questions and answers

## Video 

<a href="http://www.youtube.com/watch?feature=player_embedded&v=y4fYxmE0HZM" target="_blank"><img src="http://img.youtube.com/vi/y4fYxmE0HZM/0.jpg" 
alt="Nick Janetakis: Command Line Focused Development Environment" width="50%" /></a>

## Transcript

hello everyone and welcome to our data
umbrella webinar this is our first
webinar of 2021.
i'm going to do a quick introduction and
then nick will do his talk and
we'll open it up for q a you can also
ask questions
in the question tab throughout the
presentation and we'll sort of break
whenever it's a good time to break and
this
webinar is being recorded
data umbrella is an inclusive community
for underrepresented persons in data
science and we are volunteer run
a brief couple of things about me i'm a
statistician data scientist and i have
an
ms in masters in statistics and an mba
from nyu
and i am the founder of data umbrella um
if you
are interested in learning more about
what i'm doing you can follow me
on twitter linkedin or github i have the
same handle raishma s
we have a code of conduct here and we're
really really intentional about
providing a
respectful welcoming professional
environment so please
make sure that you follow our code of
conduct it's listed on our website
and also this applies to the chat as
well so please um
you know be professional about what we
post on the chat
so the ways to support our community is
the most importantly as i said following
our code of conduct
um we have a discord channel the link is
on our website and so it's a great place
to ask and answer questions there if you
want to share events through your
community there that's a good place to
do it
and we have for all of our events we
record them and we have
a list of transcripts on our github repo
so if you would like to help us edit it
um feel free to email us and i also have
detailed instructions on how to go about
doing that
another way that you can support us is
donate to our open collective
it helps us cover operational costs such
as meetup dues
and other other operational costs and
we greatly appreciate your support
we are on all social media platforms as
data umbrella
so the best place to find out about
upcoming events is on
our meetup group all of our events are
posted
as i said on the video library on data
umbrella we have a job board as well
and a newsletter which goes out once a
month and we have resources on our
website
website related to diversity alice
allyship inclusive language and more
on our video library on youtube we have
a playlist for contributing to open
source
and so we have um for the library is
numpy
scikit-learn pandas and core python
there are some videos
so you know for those of us in data
science open source is critical and it's
a good way to figure out and learn how
you can
contribute we also have a playlist on
career advice
we have three speakers who've done a
really informed really done informative
talks about it so
if you are looking for career advice
please check those out
this is just um a small screenshot
of some of the events that we have on
our youtube so
check it out depending on what topic
you're interested in
our job board is jobs at
jobs.dataumbrella.org
if your company is hiring they can post
jobs there and we can share it with our
community
on um in our newsletter as well as in
upcoming webinars
our highlighted job that we have is um
cloud infrastructure engineer at
coiled and it
is a distributed infrastructure so feel
free to check that out to learn more
about the position
this is just a list of some of the
resources that we have on our website
open source
guides to using inclusive language how
people can be allies how to handle
burnout
and resources for ai ethics
as i mentioned before we're on all
platforms under data umbrella so
depending on your choice whichever
platform you prefer
to you prefer to use um follow us on
that platform
i want to share some upcoming events
that we have we have intro to sphinx for
python documentation
presented by melissa weber and that is
on january 28th
and the link to that to sign up is on
our meetup
page we have our flagship event for the
year which is a scikit-learn open source
sprint this
this sprint is focused on participating
getting participants from the regions of
africa and middle east and so if you're
in those regions please check out our
website it's afme2021.dataumbrella.org
if you have any questions feel free to
email
us the information about contacting us
is on the application form on the
website
there's also want to share a community
event that's coming up which is global
diversity cfp day
and the goal of this event is to provide
resources for underrepresented or
marginalized groups in tech
to submit pf cfps and get started
speaking at
meetup events and conferences and there
are live streams there are six different
live streams for different regions in
the world
and there's some great talks and
workshops coming out
the website is globaldiversitycfpday.com
um feel free to check that out
and i want to now introduce our speaker
for this event it is nick
giannitakis and nick is a developer and
cis admin
he is an independent freelancer course
creator and host of podcasts running in
production
he has hundreds of blog posts blog posts
and youtube videos focused on building
and deploying web apps
um as along with development environment
tips um i reached out to
nick because you know studying using the
command line is a really really useful
um skill for data scientists and i think
it's really going to be beneficial to
people in our community whether they're
aspiring data scientists or
experienced practicing data scientist
and you can find
nick and more information on nick's
website nick johnnytakis.com
and github is at nick jj and nick is
also on twitter
as at nick jonatakis and with that i am
going to turn the camera
and microphone over to nick
okay thank you for the introduction let
me uh just share my screen really quick
do you see anything
it shows your slides by the way just a
heads up
here we go okay
so everyone can see this now i hope
so hey everyone thanks a lot for coming
my name is nick genitakis and today
we're going to go over
creating a command line driven
development environment
by the end of this talk you'll be well
on your way to having a tricked out
terminal
along with being familiar with tools
like tmx and vim
and also being comfy using command line
tools to solve
real world problems we're also going to
go over
how you can manage your dot files these
are files that typically live in your
home directory
and are responsible for configuring a
bunch of command line tools
just a heads up everything we go over
today is going to work on all major
distros of linux
macos and windows 10. in the case of
windows it will be expected
that you're using wsl1 or wsl2 which is
the windows
windows subsystem for linux that's
because we're going to focus on shell
scripting
in a unix or unix-like environment not
so much powershell
also we're going to cover a lot of
ground in this talk
but don't worry i'm not going to leave
you hanging on installing and
configuring everything on your own from
scratch
so feel free to check out this get repo
afterwards it has a very skimmable
reference for everything we're going to
do
uh as well as this slide deck you can
just download it there as well
with that said let me quickly introduce
myself my name is nick genitakis
and i've been a freelance developer for
the last 20-ish years
and i would say for the last seven or so
years i've been doing a lot of
devops work that's mainly setting up
linux servers
working with various cloud hosting
providers deploying code
writing shell scripts and using tools
like docker ansible and terraform
now the specifics aren't too important
but i do think working with a bunch of
different technologies and projects
has led me to having a command line
focused development environment
now chances are you're not going to be
using the same exact tech stack as me
but we can all use the same command line
tools to solve
our unique problems for example i found
myself bouncing around
so many different freelance and open
source projects and i wanted a way to
quickly switch between them
to get right back into our project as if
i never left
that led me to discovering tmux and
eventually vim
and by the way if you decide you don't
want to use vim as a primary code editor
that's completely fine
i only started using vim about two years
ago mainly because the combination of
using it with tmux
really let me quickly switch between
projects on the command line
but even if you don't use vim there's so
much more to the command line
than cone editing and tmux is really
useful on its own in any case
now before we dive into the basics of
using tmx and other tools
let me quickly go over a couple of
practical examples
of how i use tmux vim and various
command line tools in my day to day
i'm going to blaze through this without
explaining everything in detail
so you can get a high level overview of
how everything fits together
and see what types of workflows you can
create this way you can start thinking
about
how all of this applies back to your end
your dev environment
then after that we'll go back and cover
how everything works and how everything
can be configured in more detail
also just a heads up for the sake of
time and avoiding silly mistakes like
typos
i decided to go with animated gifs for
demoing a few things
that means you'll occasionally see
animations that are looping indefinitely
and they may not line up exactly with
what i'm saying but i think you'll get
the gist of it
lastly feel free to ask questions if
anything isn't clear
because i am prepared to jump into a
live terminal if needed
let's do this so here's a brand new
terminal that i just opened
and let's say i want to start working on
the source code to my flask course which
is a web application
running in docker i was working on that
last night but
today is a new day instead of opening
everything from scratch
i can attach to a tmx session that's
running in the background
it already has vim open with the last
file i was editing along with the entire
app running inside of docker
it's like i never left i can immediately
get back into the deck of it
next up let's say i want to do a
project-wide search for
all the tests in the project i can do a
search for the test
underscore string in vim and it'll do a
fuzzy search and list all the matches
also instead of a string i could have
used a regular expression
after that vim will present me a way to
filter and select the matches i want
and it even shows a little preview of
the file as i cycle through the matches
my font size is massive for the sake of
this talk but normally you can see a lot
more of the file in the preview
then from here i can pick a file and it
opens in the main buffer
if i want to look at multiple files at
once vim makes it easy to open
horizontal
and vertical splits it looks a little
cramped here because the font size
is so large with my normal setup i can
fit four 80 character width files side
by side
on a 2560x1440 monitor running at one to
one scaling
also i didn't show it there but it's
really easy to switch between the
different splits using hotkeys or the
mouse
now let's say that you want to open a
different set of files but you don't
want to lose your existing layout of
files
with a vim you can open files in a new
tab and this tab becomes a bucket
to hold as many files as you want then
you can switch between tabs up top
using hotkeys or the mouse so let's say
we did some work and now it's time to
commit our changes
i can hop over to the second tmux window
on the bottom
open a split and make my git commit
message as an aside
tmux also supports horizontal and
vertical splits
i also like using vim for writing commit
messages because it helps me adhere to
best practices such as
warning me through syntax highlighting
if the first line is too long
or if i have any typos next up let's say
you have
a few tmux splits open and you really
want to view the log details in full
size but you don't want to close your
existing splits
tmux lets you zoom in and out of any
split you want
it's i'm just hitting a hotkey there to
toggle the zoom in and out
also it's worth mentioning you can do
the same thing with vim splits too
i didn't show it for the sake of time
and just as a reminder
we're going to see how to do all these
things later on when we dive into the
details
next up let's say i want to jump to a
completely different tmok session
in this case it's my podcast site and
maybe i came here to add a reference
link or something like that
after doing whatever i needed to do i
can jump over to the second tmux window
on the bottom
and deploy the site with ansible
ansible's deploy command is kind of long
and i don't want to have to hit the up
arrow 100 times to find it so
i can reverse search my history using
the same tool that we saw
in fim to fuzzy search through files in
a project this tool is called
fcf by the way lastly here's a quick
demo of doing github style markdown
previews in vim
technically it's not real time since
it's not updated on every character
press
but you can turn that option on if you
want i keep it off for performance
reasons
instead it updates every time i switch
vim modes or save the file
also on the right vim puts aaron's
exclamation points near the line count
that's to let me know that these lines
have changed based on the most recent
git commit
it'll show new lines and deleted lines
with different markers too
honestly we could spend the whole hour
looking at vim and tmux features
but there's so much more to the command
line than using vim
so let's switch gears and go over a few
practical examples
of using command line tools for example
let's say that i'm working on something
and it sparks an idea for a blog post
i can just run a custom script i created
called drafts and start typing whatever
i want
after running that command it
automatically creates a date labeled
file
in my personal website's drafts folder
if i rerun the same script
it opens the file in vim so i can start
fleshing out the draft right now
that's typically what happens in
practice this might seem like such a
minor thing but
it really helps remove friction when
starting new blog posts
because the tool i use to build the blog
expects files to be in this dated format
not having to create this file manually
means it's one less thing i need to
think about
as for the draft script it's a simple
script and don't worry if you can't read
the text
the real takeaway here is the command
line is there to help you solve
whatever unique problems you have it's
almost like a direct link to your brain
except you just have to type what you
want instead of just thinking it for now
in another example i created a script to
toggle dark and light mode for my
terminal
tmux vim and other tools i prefer using
light themes in my day to day
but after running a poll i found most
folks like seeing a dark theme in my
video tutorials
so with the script i can quickly change
between the two
it's open source and my public dot files
and we'll take a look at that later
in one more example let's say i was
heading over to new york city later
tonight and i wasn't sure if i needed a
really heavy jacket
because i live 90 minutes away and
weather is crazy like that
not a problem i can just run weather nyc
and
that's what we see here there's almost a
tool for everything
in this case the weather command is a
very simple function i set up to
curl wttr.in which is a website that
shows you the weather in a browser
but it's also optimized for displaying
the weather on the command line
there's also dozens of general purpose
unix tools that you can use
to solve problems around processing and
filtering text
i i'm trying to keep this folks talk
focused on workflows and more generally
your development environment
but besides using tmx and vim piping
together a few unix commands
and writing your own scripts to solve
your specific problems
is a huge part of using the command line
it becomes another tool at your disposal
with that said let's take a couple of
minutes and go over one example of doing
this
so imagine if you have a csv file with a
bunch of transactions in it
and you want to extract that information
like how much money you generated
but also have an ability to filter the
results on specific product names
date ranges and so on the csv file we're
looking at here
is a simplified version of a csv that my
course platform spits out
with a bit of anonymized data in
practice you'll find payment gateways
like
stripe and paypal supplying your
transaction information
in csv files so this is a real world use
case
as an aside vim has a plugin to help
view and display csv data
and we'll go over that in a little bit
but viewing this data
isn't super useful typically i want to
figure out things like
how many courses were sold this month
and have an ability to filter
the results by course name and so on and
that begins with removing
the csv headers said stands for stream
editor
and in practice it's a very useful tool
for doing a find and replace in text
but in this case we're using it to
delete the first line
in the file the 1d part stands for
delete the first line
if we swapped out the one with a two
then the first two lines would have been
deleted instead
one neat thing about the command line is
there's often more than one way to do
something
if you googled around for how to delete
the first line in a file you'll find all
sorts of different answers
and most of them will probably work for
example we could have used the tail
command and
passed in these flags to get the same
exact result technically tail is faster
than set on linux but it's also slower
on mac os by default
at least according to stack overflow
although i find the tl version
to be less readable for this type of use
case it's confusing because plus one
actually outputs the entire file so we
need to offset what we want by one
and then there's also differences
between using one and plus one
one takeaway here is you should be
mindful of performance but readability
almost always wins
especially if the performance difference
isn't worth anything considering
for example if we had thousands of rows
and the said version finished in five
milliseconds but the tail version
finished in 3 milliseconds
it doesn't really matter for a script
that i run once a month on my dev box
but i will remember what 1d does instead
3 months from now
which has way more value in the end as
an aside
tail is still a great tool if we wanted
to get the last line or last couple of
lines of the file
then tail is for sure the way to go here
you can even have tail watch a file for
changes in real time
and output new lines as they come in
that could be really useful for
monitoring web server logs
but moving on we're going to use the
said version and the next thing we'll
want to do
is filter out a specific column of data
this column is the net amount of sense
and it's the thing we want to sum up in
the end
unix was invented a long time ago but
they made some great design decisions
such as being able to pipe the output of
one program
as input into another and you'll also
find that text streams are the protocol
that most unix commands use that means
most command line tools expect text as
input
and produce text as output this is
remarkably powerful because suddenly it
means you can combine
hundreds of tools in a number of
different ways to solve
very specific problems that you might
have
and unix pipes are the secret sauce that
lets us send the output of one program
as input to another pipes are defined
with the vertical line and you can see
that they are sitting in between
said and cut that means in this case the
output of the set command is now being
fed in as
input to the cut command and this cut
command is going to delimit the output
by a comma
since this is a csv file and we want to
grab the fifth column
which is the net amount in cents if we
ever wanted to calculate the transaction
fees for
a specific payment gateway then we can
change this five to a four
and now it would get the previous column
which are those fees
and this is why command line tools are
amazing we get to break down the problem
into bite-sized chunks
and then work on only a very specific
tiny problem at hand
i think this fits the functional
programming model very nicely
speaking of which a lot of functional
programming languages also have the idea
of a pipe operator
where you can send the output of a
function as input to another function
it's a great way to break up a problem
next up
now that we have a list of amounts we'll
want to sum them up
but before we can sum them we need to
transform the list of numbers
into a math equation that adds each
value for that
there's the paste command and don't ask
me why it's name paste because i have no
idea
it has nothing to do with your clipboard
all i know is when we use these flags
it becomes what we see here if you
wanted to do something else like
subtract the values
then you can replace the plus at the end
with a hyphen and technically you can
use this paste tool for anything
it's not limited to math if we put an
underscore instead then it would delimit
them with that
by the way the dash d is the delimiter
and dash s puts everything onto one line
and now that we have our equation ready
to go we can use the
basic calculator command aka the bc
command to sum them all up
and there we go we solved our problem by
piping together a few commands
in practice when you're more familiar
with these commands you can create
pipelines like this in a few minutes
by the way there's a gacha here too with
the bc command if you ever want to
support floating point numbers you'll
need to add the lflag to it i didn't add
it here since we're dealing with summing
whole numbers
so there's never going to be a decimal
point next up let's filter the results
by a specific course by using the grep
tool
this is a tool you'll likely find
yourself using all the time
you can provided a text stream or a file
and then we can match whatever
search string we want in our case it's a
regular expression
that makes sure comma bsawf is at the
very end of the line
this is nice because it means we no
longer need to use the set command
to chop out the first line since this
grep pattern will only ever match csv
rows that have this specific text and
then from here we can use what we did
before
to sum up the net sales and suddenly we
have the total sales for a specific
course
i also decided to throw in two more
examples here at the end
the first one lets us count the number
of sales for a specific month
here we just take the output of what
grep produces and pipe it into
the word count command the l flag counts
the number of lines
instead of words alternatively grep has
a c
flag to get a count of the results
instead of returning each match on a new
line
in practice i would use this second
command if i wanted the count
it's less typing less overhead and more
straightforward to read
so that's a mini crash course in
combining a couple of commands together
to solve a real world problem the cool
thing is if you find yourself writing
scripts like this
and they start to get a bit unwieldy
then you can put them into a dedicated
script file
and run them like that we'll talk more
about shell scripts a bit later on
and that leads us into the next part of
this talk we just covered a bunch of
practical workflows
and examples of using the command line
now it's time to get into the details
about setting up your development
environment
and that begins with picking a terminal
and configuring your shell
we're going to spend quite a bit of time
on this because it's pretty core to your
environment
the interesting thing about tmux by the
way is it gives you tabs
splits and a way to search up and down a
buffer in any terminal
this allows us to pick a terminal that
focuses on speed
and having the least amount of input
latency when you press keys
you can al you can also optimize for
quality of life enhancements too
like customizable hotkeys easily being
able to zoom in and out
being able to click urls and also have
solid unicode support for displaying
icons and emojis
if you're going to be spending a lot of
time typing something in the command
line it should feel really good and make
you happy while doing it
for example i'm using windows and the
microsoft terminal has really really low
key press latency
it's like night and day compared to most
other terminals on windows
i tried a whole bunch and the other one
that came close was wsl tty
but i've gone with the microsoft
terminal because it's more integrated
with being able to easily switch between
wsl distros
as for anyone running native linux xterm
is a very lightweight terminal
and that's pretty much the lowest input
latency that i've ever encountered on
any os
also with a bit of configuration it's
all the marks for the quality of life
improvements
i do run native linux on a modified
chromebook and that always amazes me at
how nice the terminal experience is
for mac os to be honest i am not 100
sure
since i have no first hand experience
but i've heard really good things about
item 2
so i might want to start there if you
want to give it a shot in addition to
that there's cross-platform terminals
like alacrity which is something you may
want to check out too
but personally on windows and linux i've
always used the microsoft terminal
and xterm and i think the takeaway here
is
it doesn't matter too much on which
terminal you pick because tmux brings a
lot to the table
so just stack up on speed and quality of
life improvements and i wouldn't worry
about
too much about having native terminal
support for things like tabs splits and
searching
next up it's time to pick a shell and
your shell provides a command line
interface
to your operating system it's both
interactive
and it can be used as a scripting
language right now i happen to be
running bash and you can check which
shell you're currently running
by running echo dollar sign zero
there's also dollar sign shell too but
this is technically the default shell
for your system or user
not your current shell to help clarify
that another shell is sh
which is the bourne shell and it was
released way back in 1979
if you're curious its successor bash
stands for the born again
shell and that was released about 10
years later in 1989
but just because i'm running bash here
doesn't mean i can't use the original
boring shell
you can run it by running sh notice how
the prompt changed
and now running dollar sign zero returns
sh instead of bash
but dollar sign shell still returns bash
because for my nic user on the system
bash is set as the default typically in
modern systems you wouldn't use sh as
your interactive shell in your day to
day
it's missing very nice to have features
like being able to tap complete commands
or use the arrow keys to move the cursor
around however when writing shell
scripts
it's often a good idea to target your
scripts for the shell since it's the
most compatible across systems
although there's not too much harm in
targeting bash2 because it's available
on most linux systems and mac os
we'll talk about shell scripting in a
bit but for now let's focus on the
shells themselves
besides sh and bash there's also newer
shells such as z shell
which is labeled as zsh just like bash
extended the original boron shell z
shell extends bash
personally i'm not a huge fan of it but
it's not because it's bad or i have
anything against it
i'm just content with bash and i don't
really feel like i'm missing out
on anything at the moment by the way
it's worth pointing out if you're
running a modern version of mac os
if you follow along before and you ran
the echo dollar sign zero command
chances are you saw z shell as your
shell that's because mac os made it the
default shell in the catalina release
back in 2019 but even so bash is still
available to be run
on mac os next up there's fish which is
an even more recent shell
and it stands for friendly interactive
shell unlike z
shell fish is not compatible with sh or
bash because the creators
thought certain design decisions from
back in the day were poorly designed so
they went their own way
honestly this shell isn't for me mainly
due to that lack of compatibility
but it might be okay for you it has a
lot of the out of the box features like
auto suggestions but
you can also get that to work with other
shells too it just takes a bit more
effort
with that said at least now you know
these options exist
we only have so much time here so we
can't spend a ton of time
breaking down the pros and cons of each
shell but overall your shell is there to
make it a pleasant experience
to use your system from the command line
if you're curious now you can google for
things like bash versus z shell versus
fish
and you can make an informed decision uh
just be aware that this is an excellent
topic to get lost in yak shaving or bike
shedding
in other words you can spend a lot of
time here and not wind up with a lot of
games
the real gains come from learning how to
create tools that help you solve your
exact
problems and getting comfy with
workflows that let you do whatever you
need to do quickly
it's not a life or that death decision
either you can always switch your show
later on without too much fuss
so that's a basic rundown of shells
since i happen to use bash
let's go over how i have it configured
although in a lot of cases even if you
plan to use z shell or phish
most of what we're about to cover still
applies
most shells have a few config files in
your home directory
with bash you'll have at least the
bashrc file and maybe a bash under skype
underscore profile too in my case i
decided to
rename my bash profile to profile so
that it'll work with any shell
although technically this profile file
has one line in it that's specific to
bash
so it's not entirely portable across all
shells with that said
let's take a look at this file just a
heads up before we get into this i'm
only going to be showing a few lines at
a time
so it's easier to talk about this entire
file along with all of my config files
are in my dot files repo on github
and we'll cover that near the end as for
this profile file
it runs once when you log into your
system so it's a good spot to put things
that don't change very often
for example i modify my path here so
that any executable scripts or binaries
that exist in my
home directories dot local bin directory
are available to run without supplying
the entire path
that's how i ran that draft script from
before it exists in my dot local bin
directory
and i can run it like any other command
that's already on my system path
like rep ls and some other commands that
we took a look at before
this is also where i like to set system
defaults for certain tools that i use
the editor variable controls which text
editor to open
for example if a tool needs to open a
text editor it opens vim by default due
to this being
set the editor variable is a standard so
a bunch of tools know how to read from
it we saw that before when i wrote a git
commit message
get new to open vim due to this setting
you can also choose to set your own
variables here if you want
i really really like this pattern
because it means your settings are
stored in one spot
you know if 10 different tools decided
to open your default text editor
it means you only need to change this
variable in one spot if you wanted to
use something else
next up there's a bunch of configuration
to use syntax highlighting
in certain tools like less and man the
man command
opens a reference manual for many
different tools for example
if you run man grep it'll open the
manual for grep this is a good way to
learn about a specific tool
you can also see their syntax
highlighting without setting those
environment variables we just saw
this would be all one solid color which
in my opinion is a bit harder to read
lastly this line does the dollar sign
zero trick we did before
to see what shell we're running and even
if we're running bash and we have the
bashrc file present
it sources that file sourcing it
basically means running the script and
any shell-related changes will take
effect
in your current shell if you are running
a z-shell or phish
you would want to modify this for
whatever shell you're using
next up let's take a look at the rc file
for the sake of time i'm going to try to
keep things brief rather than go into
the gory details of everything
this file executes every time you start
a new terminal session
that means every time you open a new
terminal window or spawn a new tmx
window
this bashrc file is going to run top to
bottom
the first five settings control your
history basically if you want to save
the last 50 000 lines of history
ensure each line has its own time stamp
avoid adding duplicate or empty lines
and also append to the history file
instead of rewriting a new file on every
entry
your history is saved in your home
directory with bash it'll be in a bash
underscore history file
mine is nearly empty now because prior
to this talk i backed up my real history
file
so that i didn't have to worry about
showing sensitive information during the
talk
some of them contain client information
about client work and i didn't want to
leak those out by accident
speaking of history you can take a look
at your history by running
the history command that's useful to
find commands you've run in the past
and with saving 50 000 entries chances
are you'll be able to find commands
you've run months ago
but dropping through this output would
be kind of painful
so bash provides the control r keyboard
shortcut to reverse search your bash
history
we'll go over that in more detail once
we encounter a different part of this
bashrc file
the next couple of settings are default
values of the bashrc file
it's not worth spending any time on them
but i included them here anyways
although it is worth mentioning that on
a linux system you can check out what
the default
rc file is by cutting out etsy scale
that dash rc
that could come in handy if you're
tweaking your bash rc file and you want
to double check the default
value also in the scale directory
there's a few other default config files
to look at
if you're curious next up we have
aliases and these are really really
useful
the basic idea here is if an aliases
file
exists then we load it in there's two
files here because my dot files are
public on github
and i wanted the option to have a local
aliases file that's ignored from version
control
this locofile contains aliases that are
only ever going to be useful to me
and are super specific to private files
on my file system
like quickly accessing client project
and things like that
with that said let's take a look at the
regular aliases file which by the way in
bash would be named bash
underscore aliases by default i decided
to go with aliases to make it a bit more
portable
across different shells it still works
as aliases because it's tied into the
file being sourced from the bashrc file
we just looked at technically we can
name this file anything we want
as long as it matches up with what you
source the first couple of aliases are
defined by default
it's mainly for enabling colors in
popular commands like ls and grp
but it also sets up popular aliases like
ll
i use this one all the time to list
directories and files
my real aliases file has over 20
different functions and aliases
and we could legit spend the next two
hours going over it but instead
i want to focus on the big picture here
in my aliases file
you'll notice there's both functions and
aliases
and they both allow you to access your
function or alias as if it were a script
on your system path
if you plan to pass in arguments like
you see here then it would make sense to
use a function otherwise you can set up
an alias for example
with the weather command we can pass in
a city
zip code or nothing and it all works the
same the dollar sign one
ends up being the value you passed in if
it's empty then it's treated as an empty
string
but in this case we have an alias that
takes no arguments and we saw this
command being run during the demo
instead of just running the script on
its own it also sources the bachelor c
file because
it ends up changing the color of a
specific tool that depends on bash being
reloaded
that's kind of a neat trick because the
alias and script both have the same name
in this case the alias takes precedence
over the script's path
the takeaway here is don't be afraid to
create aliases that help you in your
day-to-day
you should try to mold your dev
environment to fit your exact needs
i think there's really a whole mindset
or philosophy around that
especially when it comes to using linux
with the amount of configuration you can
do
it really becomes an os that you can
customize for you
one day i'll switch to native linux and
the only reason i haven't already is
because i had some audio trouble with
some of my hardware
i bet if i were running native linux for
the last 10 years i would probably have
500 aliases and custom scripts
to help me in my day-to-day anyways that
is it for
aliases
the next part of my the next part of my
bashrc file
is related to the prompt and we haven't
really gone over that yet so
let's quickly do that before we see how
it's configured
my prompt doesn't look like the bridge
of the uss enterprise
and this really comes down to personal
preference i very much prefer a minimal
prompt that gets out of my way
and lets me focus on the commands i'm
running and the output of those commands
but i do like to see some information in
my prompt for example
as we saw earlier if you're in a git
repo it will show the branch name
which i find to be quite handy beyond
that i also like to see the current
directory of where i am
since that's important information as
well also if i ssh
into one of my production servers i like
to configure the prompt there to be read
to remind myself that i probably
shouldn't copy paste commands from the
internet here or start running a bunch
of commands without thinking
i don't drink much but if i did seeing
this red prompt would
be a last resort reminder to hopefully
prevent myself from deleting a
production database in a drunken rage
one takeaway here is all of these
command line tools are
super configurable if you don't like my
basic prompt and you'd rather have a
more busy prompt with emojis rainbows
and seeing your battery life or
hard drive space on every line that's
totally cool and you can do that
i've linked to a few resources in the
get repo on projects that help you
customize your prompt
in different ways with that said let's
see how to configure your prompt
aka your ps1 which stands for primary
prompt string
the syntax looks like total insanity and
it kinda is but there is a silver lining
once you have it set up you never have
to worry about it again until you get
bored and want to change things around
we can spend an hour here easy but let's
go after the low hanging fruit
the bash provides a bunch of special
characters such as backslash u
and slash h these are special variables
that translate to specific things
in the case of slash u that's your
username and slash
h is the host of the machine in my case
my username is nick
and i named my computer kit if you're
old enough to remember knight rider
you'll get that reference
there's also this slash w hidden amongst
a sea of backslashes
that's the current working directory
which is slash temp in this case
there's a number of other special
variables that you can use too and a lot
of them are related to dates and times
and i've dropped a link to the bash
manual in the references if you want to
check that out
now besides those special variables most
of the other characters in this ps1
are related to outputting color these
are called antsy
escape codes and it's kind of where the
insanity begins
it's not that it's a terrible system
it's just that it requires a lot of
escaping and also resetting colors back
to the default color if you've picked a
different color
that's why you see a few zero zero
entries that's the result code
as for picking colors if you google
around for an ansi color chart
you'll find a bunch of examples i
usually go to wikipedia for it but
that has too much to show in one slide
so i made a more readable chart
here we can see a list of valid colors
fg is foreground and bg is background
if you remember my username and host was
green so that would be foreground color
32 and if you go back to the previous
slide here we can see 32 being set for
the username
and host we can also see that 34 are set
for the working directory
which is blue that's the slash temp and
if we jump back to the chart again
here we can see that 34 is blue now
there is a variation of these colors
called bright mode
as far as i know there's more than one
way to set them honestly a lot of this
stuff is black magic to me and i just
copy paste things and tweak it
until i'm happy but as for bright mode
notice how
there is a zero one before the 32 and
34.
to my knowledge that flips on bright
mode for the color being set
if you set it to zero zero it would be
the regular version of the color
an alternative way to set that is to add
60 to the value
so 32 becomes 92 and 34 becomes 94.
keep in mind not all terminals and
themes are created equal so you may see
different results depending on what you
use
but here's a modified chart to show how
bright colors look using
xterm with the default theme also my
prompt only modifies the foreground
color of text
but you can set the background color too
i'm going to leave that one up to you if
you want to research it
you'll be able to find lots of
copy-pastable examples if you google
around
as for the command separator it's pretty
standard to end your prompt with a
dollar sign
this will end up being the character
that separates your prompt with whatever
command you're running
some folks like to use unicode
characters or an emoji
years ago i used a lightning bolt but
eventually grew bored of it
but don't let me talk you out of using
something else i really do encourage you
to mold your prompt and dev environment
to whatever you like if you did want to
swap out the dollar sign
it's a matter of replacing it here at
the end as
for this prompt the last component is
getting the get branch wedged in near
the end
the basic idea is we execute a function
here
and the output of that function ends up
in its place
that function is defined in the middle
here and all it does
is grab the current branch then it uses
said to replace some characters that get
usually outputs
when you want to run the get branch
command also if the command
fails we redirect all errors to dev null
which means if we're not get repo we end
up with no output which is exactly what
we want
honestly it's not too important to go
through this function in detail
i'm pretty sure i grabbed it from stack
overflow like seven years ago
and it still works great
there's other more fancy integrations
that you can add too
such as outputting specific characters
depending on the state
of staged files or if a file is
different than what's been commit
but in practice i don't really find that
to be that useful
typically that information could be
obtained in your code editor
or using get commands when you're ready
to commit something
but the branch is very nice to see
because being on the wrong branch can
cause all sorts of confusion
and typically you're launching vim or
another text editor
while you're actively looking at your
prompt so the branch is nice to see
there
okay so that's the prompt the next bit
here
updates your terminals window title
depending on which directory you're in
this only works if your terminal
supports it and it's part of the default
bashrc file
so it's not super important to go over
next up we have asdf which is a tool
that helps you manage
programming language versions in a
consistent way it's not important
to cover now since this mainly relates
to installing specific programming
languages
although the vim plugin i use for
previewing markdown files
does require having node installed and i
do use asdf to install node
we'll talk more about this later next up
there's fcf which is a command line
fuzzy finder
we saw this in action during the demo
when searching through a project in vim
as well as the command history this tool
replaces the behavior
for reverse searching your history and
makes it a lot better
searching your history is an important
part of using the command line so
let's spend a minute or two going over
how to do this and how fcf
improves the experience when you hit
ctrl r in bash without fcf you'll get a
menu that looks like this
the basic idea is you can start typing
the first few characters of any command
and it'll start showing you matching
commands you've run in the past
in this case i'm searching for the
characters bs if there's multiple
commands that start with these
characters then you can cycle through
them
by hitting control r as many times as
you want it's called a reverse search
because it returns the last command that
matches
in other words it searches your history
in reverse this is one of the most
useful things
ever it sure beats hitting the up arrow
42 times in a row to find some command
you ran three days ago
i probably use this feature 100 times a
day you can pick the command you want to
run
by hitting enter and it'll populate the
command for you
so in the above case all i did was hit
ctrl r
searched for the bs characters and then
hit enter all in all something like this
takes a second or two to use
it's really practical practical by the
way you can also
cancel your reverse search by hitting
ctrl c if you don't want to pick
anything
now when you use fcf control r is still
available to run
except now it looks like this then as
you start typing
it narrows down the search in real time
in this case only commands that contain
the c character
are returned it's also a fuzzy search
meaning if instead i searched for the l
character
it would have found the second match
since clear has an l in it
it ranks then based on what it thinks is
the best match and it's very good
i would say probably 99 of the time it
picks the command they want after typing
a few characters
and and that's even going through
thousands of files in the one percent
case where it fails it's no biggie i
just type one or two more characters
and it always finds it after hitting
enter to pick the item it'll
inject the command into your prompt and
then you can choose to run it
you can also hit control c to cancel the
selection just like the regular control
r
fcf can do a lot more than search your
history too you can use it to search
your process list and more
to be honest it deserves its own 45
minute talk it's a really really useful
tool
but now that we know how to search our
history efficiently let's go back to the
bashrc file
we saw these lines a few minutes ago
this controls enabling and configuring
fcf
the bottom line enables fcf and the two
optional lines above it configure it
fcf supports both dark and light themes
and you can also customize the colors
however you see fit but the line above
that is a bit more interesting to talk
about
it configures fcf to use a tool called
rip grep instead of the grep tool
when it searches for matches rip rep is
a much faster version of grep
although in practice i do use grep on
the command line because it's fast
enough
but fuzzy searching is pretty demanding
and i find rip grip speed boost to be
worth it
it narrows down search results pretty
much as fast as you can type
even with thousands of files this is
important because the even plugin for fc
up will use rip rep when searching for
files to open
or searching your project for specific
text during the demo i ran the rg
command which
uses rip grip under the hood and fed the
results into fcf
using a vim plugin installing rickrep is
easy because
every major operating system has a
version of it in its package manager
but i recommend holding off on
installing it right now because there's
a couple of other tools covered in my
rc file that we'll want to install and
it's going to be a lot easier to install
them
after we talk about dot files since
that's all documented in one spot
and finally there's a bit of
configuration in my bashrc file
related to wsl2 and wsl1
this mainly sets up an x server display
so you can share your clipboard or run
graphical apps between wsl and regular
windows
i don't want to spend a ton of time on
this one but if you're using wsl
the reference has a link to a video that
goes over this in more detail
so that's how i have bash configured i
know
it was a lot to take in but we just
condensed multiple months of research
in about 10 minutes or however long that
took
now before we get into using tmox i do
want to cover one last thing
that's important when writing your own
scripts
when writing shell scripts you might
have seen something like what we see
here
this is called a shebang and it's the
first line in the file
that starts with pound exclamation point
followed by a path to some type of
binary such as
sh bash or any programming runtime that
can be called from the command line you
may have also seen this style of a
shebang which technically works on most
systems but it's considered to be less
portable
it's less portable because the bash
binary might not exist in slash
bin on some systems whereas user bin env
exists almost everywhere i tend to use
this style unless i made a mistake and
use the less portable version by
accident
speaking of portability remember when we
talked about using sh instead of bash
for scripting
well the barn shell aka sh is posix
compliant
this is a standard that was created to
ensure compatibility between different
operating systems
to write a posix compliant shell script
you would reference
sh instead of bash in practice i try to
do that
but sometimes you really need the extra
features provided by bash
in which case i would use bash without
giving it a second thought
honestly we could spend two hours going
over the subtle differences between the
two
so let's just leave it at that you can
always google for the differences later
with that said i think one of the best
ways to learn something is to see fully
working examples
so i've dropped a bunch of links in the
references to a number of scripts i've
open sourced over the years
to help me in my day-to-day now i'm not
saying it's the best code ever written
but it might get your noodle cooking to
see what types of programs or problems
you can solve on the command line
all of the code is mit licensed too so
that's shells and scripting in a
nutshell on that note we covered a lot
but don't feel compelled to learn
everything upfront before you do
anything
you can slowly introduce things on a
need to know basis
what i mean by that is like any
programming language or environment
you can still be very productive without
understanding the entire language and
ecosystem in detail
next up let's go over using tmux unlike
the shell we'll spend the majority of
our time
using tmox instead of configuring it but
we will take a look at some config
settings too
first up what is tmox good question i'm
glad you asked
tmux is a terminal multiplexer and what
that means
is it lets you create and control
multiple terminals from a single screen
we saw that before in the demo when
creating windows and splits
it also lets you create sessions that
you can attach and detach from
which is amazing because it means if you
close your terminal
everything will still be running in the
background and you can connect to it
or connect to any session at any time
and it'll just resume where
you left off before you'll find tmox in
whatever package manager your operating
system uses
so it's going to be no problem to
install it but like before let's not
worry about installing it until we talk
about dot files near the end
for now let's just focus on using it one
core feature of tmux is its ability to
control
most things with hotkeys but don't worry
you can usually use the mouse for
a lot of things too like selecting text
or copying text
or clicking different windows or split
panes
but since tmox is so high key driven
they introduce the idea of a thing
called
a prefix key the basic idea is you'll
hit this key along with some other key
afterwards
to perform a specific action this helps
namespace
all of your tmx hotkeys so you don't end
up overriding hotkeys from other tools
by the way i also tend to call this a
leader key because that's what vim
defines it as
so you may hear me use both terms
interchangeably
by default it's bound to control b which
in my opinion is a bit funky to hit
so i've remapped my prefix key to be the
back tick
that's usually under the escape key or
to the left of the one
on a standard keyboard in practice
you'll find a lot of folks use this key
it's pretty easy to access and you
really type it in your day to day
and when you do need to insert a
backtick somewhere then you can just hit
the key twice it's not really a big deal
throughout the rest of this section i'll
always reference hotkeys with the word
prefix instead of using the backtick
directly
since you could in theory be using a
different key by default when you open a
terminal tmox is not going to be running
we need to run it manually by running
the tmux command
after running it you'll know you're
inside of tmux because you'll see a
status bar on the bottom of your
terminal
out of the box the status bar is going
to look different than what we see here
but we'll go over how to configure that
a bit later on i made mine pretty
minimal to maximize usable space
while giving me just enough information
i care about from here we have access to
a bunch of tmox goodies for example if
you hit prefix c
you can create a new window notice on
the bottom we have two windows now
instead of one
and both of them are named bash because
that's the shell i'm running
so let's say we opened a couple of
windows like we see here
and it starts to get confusing because
we're not sure what's running in each
window
well if you hit prefix comma tmux will
bring up its command mode
and now we can rename the window by
typing in whatever we want
with a new name you can also switch to
a different window by hitting leader 2
or whatever number you want to switch to
the window you're currently looking at
will have a star next to it which makes
it easy to identify at a glance
by default tmux will order windows
starting at zero
but in my tmux config i changed it to
start at one because in my opinion it's
a lot easier to hit backtick one
rather than backtick zero also if you
have mouse mode enabled
you can click any one of those windows
on the bottom to switch it and yep i do
have mouse mode enabled in my config
can everyone read that yeah just kidding
so as an aside i'm not trying to cover
every tmux feature here there's other
ways to switch between windows 2
but i'm trying to focus on what you
might use in your day-to-day
tmux has this help menu that you can
bring up with prefix question mark to
learn
all about its different binds and that's
kind of what we see here
the funny thing is i zoomed out to try
to fit all of this in one screenshot
but there's still five lines above this
there's also the man pages too and
plenty of cheat sheets available
if you google around with that said i
included a link to a cheat sheet
if you want to check that out in the
references so going back to our example
before
if you want to split a window in half
you can use prefix b
to open a split below you but that's not
the default bind
instead i made it match the same
bindings as my vim config
and there's really no limit to how many
times you can split a window you're
basically limited by your monitor screen
resolution
in practice i use split panes all the
time and you can switch between them
using the mouse
or if you use my tmx config you can also
use alt
and the upper down arrow depending on
which direction you want to go
alternatively you can also split your
windows vertically this time around you
can use prefix v
which also matches my vim keys binds or
bim
key bindings also while i'm not showing
it here you can combine horizontal and
vertical splits together
however you see fit you can even drag
the bar around with your mouse
to resize the panes there's resize
hotkeys for that too but
personally i don't even know what they
are off the top of my head because i
just don't use them at all
next up if you do find yourself having a
bunch of splits open
but you want to temporarily zoom into
one of them without closing the rest of
your splits then you can do that with
prefix z
you can tell if you're zoomed in because
it'll show a z next to the window name
on the bottom
this is something i do all the time as
well it's especially handy if you're
creating tutorial videos with a large
font size
and you just want to zoom into something
to explain one window but i still do use
this in my day to day with a regular
font size too
now there's a lot more we can do with
windows and paints but
this goes back to the 80 20 rule which
is basically focusing on the 80
which is going to give you the most
benefits versus how much time you spend
in other words what we just covered goes
a really really long ways for dealing
with windows
and split panes next up let's go over
another killer feature of tmux which are
sessions
if you hit prefix d that is going to
detach you from your current session
we didn't go over this yet but when we
ran tmux before
it started a session for us behind the
scenes and it named that session zero
since we didn't define a name
that means if we close our terminal we
could reattach to it and things will be
back as if we never left
if we ever forget what's running we can
also use the tmux ls command
to get a list of sessions in our case we
have just the one here
then if we run the attach command along
with a specific session name
we can attach to a specific session
right now our session is named zero but
we can choose to rename it to something
else which we'll do in a few
it's also worth pointing out that if you
run tmux attach with no arguments
it'll attach you to the last used
session which is something i do
all the time
after running that attach command we're
back to our session from before
and it's like we never left what's
really useful is that
you can have multiple sessions running
at once and switch between them at will
that's a game changer if you have a
terminal focused development environment
speaking of multiple sessions if you're
already in a team up session
you can create a new session by running
prefix colon to bring up command mode
and then you can run the new session
command i'm passing in
a custom session name of cool here but
you can name it whatever you want
technically you can make a new session
without naming it but i find in practice
that naming your sessions is totally
worth it
especially when you're dealing with a
few sessions as for this animation
right after the session is created we
can see that we're put into a new
session with only one window
but our old session is still running in
the background
also if you're curious most commands
that you can run in command mode
can also be run directly on the command
line although in this case if you try to
create a new session like this when
already in a session tmox is going to
prevent you from doing it by default
otherwise it gets too confusing with
nested sessions however
when you run new session in command mode
that doesn't nest the new session with
an existing session
it creates a completely new one i know
that's a little confusing but that's how
it works as far as i know
the takeaway here is you should always
spawn new sessions from command mode
if you're already inside a session or
you can just detach from your current
session and make a new session from the
command line
as for switching between sessions you
can hit prefix
s this gives you a list of all of your
sessions and then you can use the arrow
keys to pick the one that you want and
switch to it by hitting enter
upon doing so you'll be put into that
session immediately
what's really cool is as you cycle
through the list of sessions you'll get
to see a preview of what's running in
the lower half of the window
that could be very handy to see what's
running in a session you can even click
directly into one of those boxes and
jump straight into that sessions window
next up let's say you want to search up
and down your buffer
with the way i have things configured
you can use the mouse wheel to scroll up
in your buffer
and that puts you into tmox's copy mode
you can identify that by the orange
label in the top right
which shows the number of lines in the
buffer then you can hit the forward
slash key to begin searching
type in your term and hit enter from
here tmux will highlight all the matches
and you can press m n as a nick to jump
to the next match or
shift end to go in reverse this is what
i meant by
tmok super charging your terminal
suddenly we can do all of this with any
terminal
now with the way i have things
configured if you select any text with
the mouse and let go with the mouse
button
it'll copy that text to your clipboard
that's due to using a tmux plugin
called yank you can even use the mouse
wheel or the page or up down keys
to quickly select a bunch of text that
is multiple pages long
copy pasting text is a pretty common
thing to do so i'm sure you'll be using
that one
once in a while i know i do next up it's
worth pointing out that if you open
two separate terminals you can connect
both of them to the same session
when you do this your actions are going
to be mirrored in both terminals
that includes both typing and switching
windows
by default tmux will also resize the
viewport of both terminals
to be whatever the smaller one is to be
honest i am not sure why it does this by
default but you can change this behavior
for example if you attach to the session
like this
along with setting one config option
then you can connect to the same session
but each terminal will have its own
independent view of a specific window
this is
very very handy if you use multiple
monitors it means you can have a second
terminal open on your other monitor
and look at a different window on the
same session that's running on your main
monitor
i do this quite often when i'm working
on projects that require seeing many
things at
once lastly let's say you're detached
from tmux
and you want to stop all of your
sessions you can do that by running tmux
kill server that's going to completely
kill tmux
destroy all of your sessions and stop
any processes that were running in the
foreground
inside of tmox that could be handy if
you get busy with not naming your
sessions and after a few weeks of using
tmux
without rebooting you wind up with
having 20 unnamed sessions and 50 copies
of him running
been there done that although as for
rebooting
by default you will lose all of your
sessions after your reboot
on linux this might not be too bad
because you know you might not reboot
for six months but on windows this is
painful because windows will
reboot your machine whenever it feels
like it but there is a silver lining
there's a plugin called tmux resurrect
that will let you save and restore your
sessions after a reboot
even if the tmx server is killed with
that said let's quickly go over a few
interesting parts of my tmox config
for the sake of time we're not going to
spend as much time as we did going over
the shell related configs
my config is pretty well commented so it
should be fairly easy for you to take a
look at it in more detail on your own
like the other config files will show a
little bit at a time and this is how you
can customize your prefix key
there's not much to it if you wanted to
use something other than the backtick
then you would change it here
next up this one is super interesting
this is the setting that allows you to
get independent windows
when connecting to the same session
multiple times apparently resizing isn't
enough
you need to aggressively resize to get
your independence
these settings control the status bar i
explicitly removed everything
except showing the window number and
labels by default tmx shows a clock on
the bottom right side of the status bar
i have that disabled with comments if
you google around for
tmok status bar configuration you'll
find a bunch of examples on what you can
do
for example you can add things like your
network ip address and more
that could be handy if you're connecting
to multiple remote machines
these settings work together to make
tmox a bit more human friendly
for example if you had four windows and
you closed window 2
then tmux by default will leave a
numbered gap what i mean by that is
you would end up with windows 1 3 and 4
being available
the first setting removes the gaps so
you would end up with windows 1 2
and 3. the other settings on the bottom
make tmux start numbering windows at 1
instead of 0. next up you can quickly
reload your tmux config
by hitting prefix r that's handy to do
if you're tweaking your tmux config
and you want to see the changes without
having to kill your tmux server
this is similar to sourcing your bashrc
file to see the changes
without opening a new terminal lastly
tmux has plugins
and the tool to manage them is called
tpm that stands for
tmux plugin manager in case you're
wondering it's something you'll need to
install and it's included in my dot
files documentation
the yank plugin copies selected text to
your clipboard and the resurrect plugin
lets you save and restore tmok sessions
even if your tmux server dies
you can do that by hitting prefix
control s to save your sessions
and prefix control r to restore them
once you're inside
any existing tmx session and that's all
you have to do this plugin is awesome
especially if you're on windows
now let's talk a little bit about them
and unlike the tmx session this is going
to be more like a rapid-fire description
of a bunch of vin plug-ins that i use in
my day-to-day
that's because to really really really
get into vim would totally require its
own dedicated talk
instead of a few minutes if you're
curious i do have over 15 videos on
youtube
covering a bunch of vim topics i've
linked to them in the reference notes
lastly i do run regular vim not neovim
but all the plugins that we're about to
go over will work with vim 8.1 or above
and neovim as well speaking of plugins
we'll need to
install a tool to use them then vim has
many many different choices
for how to install plugins since it's
been around for so long
the one i use is called plug and you'll
see how to install it once we get into
the dot files section
none of these plugins are in any
specific order but let's start with the
ones that
we've seen during this talk also the
code snippets you see here are straight
from my vim config file
as for fcf it allows us to fuzzy search
files
git commits and more it's one of my
favorite plugins
fern allows you to quickly visualize
your project's directory structure
and it makes it really easy to rename
copy or delete files and directories
it even supports bulk renaming files and
even buffer for doing complex renaming
this could come in really handy if you
want to re-reorganize how you label
media files
or whatever you might be doing next up
signify is a super efficient plugin for
displaying get changes
like what we saw during the markdown
preview demo that's where we saw the
orange exclamation point
it also uses a green plus symbol for new
lines and a red dash
for deleted lines then for previewing
markdown
i use this plugin it's labeled as being
for neovim but it still works with the
vim 8.1 or above this is the plugin that
requires having node installed
also we saw this plug-in display
markdown that looks like github styles
but you can very easily change that by
swapping a css file
in case you happen to be using gitlab
bitbucket or you just want your markdown
style differently
for csv files there's not much to say
about this one
other than it works really well by the
way i have about 20 other plugins
related to syntax highlighting
for all the different tools and
languages they use on a regular basis
that's one of the reasons why i really
like vim it lets me use the same tool
for everything
multi-snips and vim snippets really help
with providing shortcuts for
inserting code most editors have some
type of snippet support
and these work really nicely in vim as
for this other plugin
it tells vim to automatically pop up its
code complete window
while you type now if you've ever used
sublime text that makes it very similar
to how you can autocomplete anything
you've typed in any open buffer
the cool thing about this one is none of
these plugins require running a language
server if you happen to know what that
is
this is more for a lightweight approach
to get useful but not hyper intelligent
autocomplete that's context aware
moving on this one lets you zoom in and
out of splits and vim just like you can
with tmox this comes in very handy if
you're someone who likes to open a bunch
of splits
now all of these plugins work together
to serve the end goal
of making it easier for you to find
search and replace text
i use these all the time especially the
visual star
and vim gripper plugins there's a 30
minute video linked in the references
that goes over how to do various find
and replace workflows in vim
it ranges from searching for a character
in one line to doing a regular
expression based find and replace across
multiple files
lastly there's two themes that i really
enjoy using
both of them have very good syntax
highlighting for many popular languages
including python and r
i used one dark for all the screenshots
in this talk and i typically use it when
recording videos
and then i switch over to one light for
personal use prior to that i used
drevbox for almost two years and i still
really like that theme
but like most developers we get bored of
themes over time so i like to mix it up
but i could see myself switching back to
it in the future
besides plugin plugins related to syntax
highlighting
there's still about 15 or so plugins
that i didn't mention which are still
worth using for very specific things
now i don't quite have 200 plugins but i
would say i have about 45 or 50
and i do use them on a regular basis i'm
very protective of which plugins i add
and i also focus on keeping things as
efficient as possible
that means not using plugins that
introduce typing delays or
other hitches with that said all the
plugins i use are listed in my vmrc file
in my dot files
with a one line comment explaining which
each one does and that's going to wrap
things up for vim
so now let's talk a little bit about dot
files
we've already seen a few such as the
profile bashrc file and tmux config
files
when it comes to configuring user
settings for command line tools
it is very common to put them into
various dot files
it's not a guaranteed role but most
command line tools will use files that
begin with a dot
for its configuration and there's three
main places where
they might exist some tools will write
out their config files into your user's
home directory
which is what we saw before with a
bashrc file tmux config and a few others
it's also quite popular for tools to
create a dot directory
in your home directory named after that
tool for example if we take a look
at my home directory there's a few tools
that do that this usually happens when a
tool has one or more config file but not
always
sometimes a tool will place a bunch of
config files unrelated to its
configuration
along with its configuration all in one
spot it's also pretty popular for tools
to place their config files
within their own directory within the
dot config directory inside of your home
directory
that's a lot of directories this is a
newer standard based on something called
the xdg-based directory specification
which is linked to in the reference
notes if you want to learn more about
conventions
around where certain files should live
and that's what we can see here
if i happen to write any scripts that
need one or more config files
i always use the config directory since
it's a standard
so that's how configuration is mainly
handled but i sort of simplified where i
store my individual dot files
to make the previous slides easier to
read in reality
most of my dot files are sim-linked to a
separate directory
that's contained within a get repo you
can see that here with the arrow pointer
which is a sim link
sim links are references to another file
or directory you can sort of think of
them as shortcuts if you're coming from
the windows world
now they're not specific to dot files
but they're often used together with
that file so that you can save your dat
files in one centralized location
and then sim link them to wherever they
need to go in your home directory
and that leads us into one way of
managing your dot files
i'm a fan of having a single directory
somewhere on my system
such as this dot files repo in my github
folder and then i can sim link the
config files to where they need to go
this keeps things simple and it makes it
easy to replicate my setup on another
machine
or share it with others all you would
have to do is clone down this repo and
then set up the sim links if all you
wanted to do is replicate my configs
but sim links are not the only way to
manage your dot files
there's dozens of tools focused on dot
files management
but honestly i never felt the need to go
that far
a really popular one is called yet
another dot files manager and i've
dropped a link to that one in the
references
it's basically an abstraction on top of
git and it comes with its own custom
command line tool to manage your dat
files
if you find yourself gravitating towards
wanting to use a dot files manager
i would start with this one i haven't
used it personally but i do know someone
who is happily using it
that someone has been working on the
command line for 15 plus years
and he looked at a lot of other tools so
i trust his recommendation
with that said let's take a look at a
few key parts of my dot files repo on
github
in addition to the config files
themselves i included screenshots and
documentation
related to installing the tools i use on
a few popular linux distros and mac os
there's not really an unwritten rule to
include installation instructions in
your dot files repo
but i decided to go the extra mile i
included them mainly because i have a
few programming courses and
i wanted a single place where i could
point folks too in case they wanted to
replicate or cherry pick a few things
for my setup
for example if you wanted to install
tmux vim and another
a number of other tools you could copy
paste one of the package installation
commands
depending on what os you're using in
this case it's the debian and ubuntu
installation instructions but in the
readme file there's copy pasteable
commands for brew
in case you're using mac os you can also
choose to add or remove anything you see
fit
for example jq is a command line tool
that lets you parse json
if you don't care about that then you
can easily remove it
then for installing the dot files
themselves it's a matter of cloning this
repo
and then setting up the sim links you
could choose to grab all of my configs
or just the ones that you care about
for example if you find yourself using z
shell instead of bash
you could remove my bashrc file or if
you're not using wsl
you can remove the last sim link since
that only applies to wsl
also if you want more control over your
setup and want a very personalized
solution
you could always skim through my
individual configs and copy paste
whatever you want
directly into your config files beyond
that there's a bunch of commands like
this where
you can pick and choose to install
whatever tools you want this quite a bit
more than what's shown here
but the rest are documented in the same
way and all of these commands will work
on linux and mac os
since it's mainly running curl get and
pip commands
there's even reminders like this in the
readme file for installing plugins for
vim and tmox
there's also a section up top to help
verify everything is set up correctly
lastly it's worth mentioning that these
dot dot files are going to evolve over
time
in the references i've linked to the
exact commits for all the files that we
went over
but i do recommend checking out the
master branch on your own because if
you're watching this talk in the future
chances are i've updated a number of
things which are probably improvements
in some way or another
so that's the tldr on dot files if you
google around for
fails github you'll find thousands of
other examples
i'm not sure how many of them will have
tons of documentation but at least now
you're familiar with the concept
and that's kind of the main takeaway of
this talk i tried my best to showcase
and go over a bunch of tools but
ultimately it's up to you to apply
as much or as little as you want in your
daily workflow
like anything that takes time to build
up muscle memory especially for hitting
hotkeys that might be foreign to you
i know it took me a long time to get
used to them and i still feel like i
have a lot to learn
in other words don't get discouraged if
you struggle for a while it definitely
gets better over time
and on that note hopefully at the very
least a couple of unknown
unknowns were discovered today usually
when i watch a talk or read a book i'm
hoping to walk away with at least one
nugget of information
then i can apply it back to my
day-to-day and that is all i have
thanks a lot for having me and if anyone
is still awake and we still have some
time i'm more than happy to answer any
questions
cue awkward silence
not really sure what i need to do beyond
this point oh can you
hear me now
okay if anybody has any questions uh
please feel free to post
um in the chat or in the q a um
i want to thank nick for his
presentation
um yeah that was um a lot of great
information um
i did have a question for you um there
are
a number of different um these are
called
vim is called the terminal editor right
um there's a number of different ones um
what are your thoughts on
um some of the other ones
okay by the way this is a little bit
weird you're actually coming through on
headphones sitting on my desk instead of
the one in my ear
so i can barely barely hear you but i'm
pretty sure you asked me
like how to compare different terminal
emulators like
what's the difference between using next
term and alacrity or kitty or like 50
other ones
uh it really comes down to preference
right like tmux really helps you out
when it comes to using different
features like splitting windows and
panes and searching
so i just try to really go for the
terminal that that is basically the
fastest and the ones listed in that
other slide
were kind of the ones that i prefer but
you can always just google around for
you know like alacrity versus kitty
versus hyper or whatever terminal that
you want and
check out its features okay great um
somebody asked
is asking a question on check can we
review the video
um if you're referring to this video yes
i will post it pretty soon on the data
umbrella
um youtube sorry to interrupt this is
crazy like i can't hear you at all so
i'm going to switch over to different
headphones
okay
yeah these are also uh a lot uglier and
bigger i use these to edit my videos but
they work very nicely can you hear me
now yeah much better
okay um all right um yeah so
reviewing the video the video will be
posted
um pretty soon um
and we'll send an announcement um
somebody else says i really enjoyed
learning about tmux as an unknown
unknown thanks for the informative talk
yes and actually um you know i
for tmux i wrote up a um i have like a
written up thing that i did when i was
taking the fastai deep learning
um best day deep learning
course and so i can share that as well
um but yeah tmux is very very
um it's really really useful i'd say
yeah
yeah it's one of those tools where it's
like until you realize that it exists
like how to live live my life without
that yeah
it is i mean i'm gonna let me just see
if i can find it
pretty quickly um it was
it certainly was very um very popular
yeah if anybody has any other questions
feel free to ask
now while nick is available
um and
um yeah yeah do you remember one
question that popped up last time was
like
well let's say i don't want to use vim
like let's say i want to use vs code
instead like is the command line still
useful and like totally for sure like
vs code if you wanted to jump between
different projects you can totally do
that as a built-in terminal
like you know the real takeaway is uh
just using the command line in general
right it's not tied to specifically
using vim
right okay
that's great um and i guess the other
thing is maybe this is a good time to
share
your um youtube channel do you want to
share that in the link nick
ah i don't even have that chat open i
can't even bring it up otherwise it's
going to like interfere with some things
here
but i can search uh youtube
is it yeah right if you just search for
my name it's there
well i hope there might be other nick
gen attackers out there but
no it's true you have 10 and a half
thousand subscribers
is that right okay
do you have a custom url for your
youtube
uh funny enough i don't remember it but
i'm pretty sure it's just youtube.com
c nicktoon attackers okay all right cool
also if you went to my home page here
then it's in the about page on the
bottom
ah okay cool yeah there's a lot of a lot
of helpful stuff there
okay so um if there are no other
questions i am going to
uh we're going to uh complete the
webinar
um once again thank you so much um
return no problem
yeah also one heads up about that
youtube channel there is a vim and tmux
playlist so if all you care about is
that then
i would check that out ah wonderful cool
all right thank you yeah no problem

