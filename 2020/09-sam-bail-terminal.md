# Sam Bail:  Intro to Terminal

video:  https://youtu.be/sqN0bFWrS6Q

(00:00)
There you go,okay.  Everybody welcome to Data Umbrella and PyLadies online event.  Just sort of let you know how well did
it how the event is gonna go, I'm gonna do an introduction about the meetup group. Sam Bell is going to give a talk  and we'll have Q&A will also sort of
watch the Q&A every 10 minutes or so and
answer questions along the way just to
let you know this event is being
recorded about me I'm a statistician
data scientist I founded data umbrella
and I'm also a hi ladies organizer a New
York City chapter and I am on twitter at
reached is the mission of data umbrella
is to provide a welcoming and
educational space for underrepresented
persons in the fields of data science
our website has information we're on
twitter if you'd like to share about
this event and just know that we are a
volunteer run organization
this is co-promoted with hi ladies which
is an international group of hi
foundations and gender minorities and
they are you can find up to the local
chapter New York City chapter that's our
website and on Twitter our code of
conduct to be iterated from emails we
are dedicated to providing harassment
feet experience for everyone um please
keep this experience to everyone
professional welcoming and inclusive on
the data umbrella website there are many
resources available and I took some
space there are these sources for open
source accessibility and responsibility
so if you want to check them out later
on please do so to watch for upcoming
events we have them
the meetup page but we also have them on
Twitter and we're on social media
LinkedIn YouTube and Facebook so feel
free to follow us on whichever platform
is your processed and so we're gonna get
started
Sam is in New York SMI Sam we met
through your PI ladies organizer as well
the New York Chapter and so it's really
exciting to have Sam presented terminal
I'm gonna let her introduce all right
great thanks for switching over hi
everyone welcome to this webinar my name
is Sam
I'm a at this point I'm kind of just
saying data person I do data things I'm
based in New York City
I run the partnerships team at a small
start-up called superconductive
superconductive is the team behind great
expectations the law gentleman on the
side here that's our logo and great
expectations a really cool open-source
tool for data quality so here's a very
brief plug if you're interested in data
quality and in using a Python library
that's open source and free for data
quality please do hit me up after the
talk we have really cool things going on
so the plan for today for this talk
about an inch or two terminal is to give
you some background ice talk about
terminology just explain sort of what do
we mean by terminal shell bash sea shell
all these things then second go into
some basic navigation file manipulation
some searching so just kind of like
orienting yourself around your file
system go a little bit into environment
variables and what your profile is all
about and then I will do a very brief
introduction to shell scripting in terms
of the structure which might already
mention it I'll be mostly showing slide
so this evolved from an interactive
workshop that pre kovat we actually used
to do hands-on parts on this in this
case I'll be doing most of the talking
and demoing some stuff I'll be stopping
after not quite each section but after
each major section for questions
I will feel these from the from the chat
and it will also have hopefully have
some time for FAQ at the end we Rallo
the the it might get a little tight
I might have to skip a couple of things
or Russia but but local figure it out
we'll play it by ear and most
importantly all the slides are going to
be online but please post a link to the
slides at the end and the chat so you
can also follow along and there are the
little DIY blocks or marked as DIY there
are many exercises that you can also try
out after the workshop so hopefully this
is this is going to give you sort of an
overview and an idea of how things work
and you can ask some questions and then
you can use the slides to like work
through stuff by yourself
after the workshop all right let's get
started so background on terminology
what are all these words so there's a
lot of things that are actually used
interchangeably which is very
interesting and honestly I had to look
up some of this too so what is a Shou
generally Chell is a user interface
which interestingly can be either a
command line so kind of what we
generally think of as a shell or it
could be graphically graphical so funny
enough we actually even consider a
graphical user interface GUI also a
shell but in general when we talk about
shell we kind of mean actually the
terminal those sort of black box with a
green font that runs a shell and then we
often also use the word bash which in
this case is a type of shell so it's
just one particular program there are
lots of others like Z shell cash I'll I
think there's one called fish but it
there's a lot of out there Mac OS
interestingly switched from bash to Z
shell and version 10-15 sitters around
last fall the basics between bash and Z
shell are pretty much the same I think
once you get really deep into it you'll
notice the differences but for me at my
level of like sort of navigating around
things I didn't actually notice a
difference between bash and sea shell so
just keep that in mind that a lot of
times like we're so used to saying bash
but
funny enough if you use a MacBook you're
actually now not in fashion any more
year in seashell so I hope that's given
you in just an overview of the
terminology and honestly like we use a
lot of those things interchangeably
because again unless you go super deep
into it a lot of times these are pretty
much the same if you use your terminal
that will open a shell etc etc so just
to clarify those things okay so now the
question we actually already had a
question in the chat like why use the
terminal and shell at all think there's
a lot of people at Apple and Microsoft
and Linux that just add Linux distros
that spend a lot of time on usability of
their graphical user interface why
should we even go back to the terminal
so one reason is it's often a lot faster
or more flexible than doing things sort
of by clicking my one of my lecturers
have a class called the keyboard is
mightier than the mouse and so a lot of
times it's really easy to just like
write a one-liner and do for example
both operations on files to search for
files and texts some some things that
don't work quite as well in your in your
operating system their GUI so that sort
of my preference is a lot of times
there's something that's just a little
easier to do second sometimes you have
to even just like navigating around the
file system to like run let's start say
start up a server or run some programs
run some Python code whatever like a lot
of times you just do that from from your
shell to kind of have to another good
example is if you connect to a server if
you run any kind of jobs or anything
remotely a lot of times you ask this
agent to that server have some other way
of connecting to it and you only have
your terminal you don't have a GUI that
you can click around another thing is
things like setting aliases or
environment variables so if you've ever
used Postgres for example there's an
environment variable called PG password
that you set to set a password there's
things like your Python path if you're
if you're using Python I'm kind of just
as human at a lot of people here are
data
sort of in in you work with data and are
maybe close to Python and have some
familiarity with that so I'm kind of
making a lot of Python references I
think so a lot of times you just kind of
have to you think the only way to do
things is fire your terminal so it's
very very helpful to just have some
familiarity with it and be able to kind
of navigate and find your way around
them I hope that's given you an
explanation as to like the motivation of
this so let's just dive right in
navigating the file system so some
basics to navigate the file system we
have and the way I'm going to do this is
I'm going to do the boring stuff and
actually just read these things out and
then I'm just going to pull up my
terminal and show you so we have several
commands to navigate the file system
once we're in our show we have PWD which
is the path of our current working
directory and usually your terminal will
open a shell in your home directory so
we'll see that in a second you can do an `ls` which just lists everything that's in
your directory and then pretty much
every shell command has a flag so the
flag is usually the - something in this
case LS dash L at a long format flag and
LS dash L a adds you can you can
concatenate the to flex it's a long
format Plus show all so I can show that
right now so I'm currently in my
terminal workshop directories the
workshop where I have all the content
for this I hope this is big enough for
everyone so let's just do this I do
PWD which says I'm an user Sam
co-terminal workshop so this is the
current working directory that I'm in I
can do an LS LS just like shows all the
files that are in this directory right
now going to LS dash L so I'm adding
this flag which shows me all the files
plus some additional information about
the file such as the permissions the
owner the group
those on the I'm actually not sure if
this is the last edit date or the
creation date this must be the last
modification date because I've updated
my slides recently and so this is last
modification date so this is the long
format flag and then I can also do LS
dash L hl8 sorry which lists also this
also gives me some of the hidden files
so that the all flag gives me hidden
files as you can see I have a docket
director here and an idea for mine
pycharm IDE that's created so so just to
give you kind of an idea of like this is
usually the first thing and you use it a
lot like PWD to kind of see where you
are use LS to see what's like what's in
the directory so now how do I know what
Flags are possible here right how do I
know I can use - oh la la something else
there is a command called man ma m which
stands for manual and that's built in
it's a it's a UNIX command and I can
just say man and then something like an
LS for example so the command but I want
to have the manual for do that and I get
a really cool of commands manual that
gives me all the information so this is
kind of the documentation about the
command I just typed of that LS and it
shows me that can use the spacebar here
to go through this and it shows me all
the flags that have just used so this -
a that I've just used include directory
entries whose names because with a dot
or the - L that I've just used listed
long format etc etc so just to give you
an idea ma n ran gives you the manual
for pretty much all shell commands that
are built-in it's super helpful there's
also a lot of Easter eggs in there these
been around for a few decades so there's
occasionally some fun stuff to find in
there the way you get out of ma n you
can see I have this blinking cursor
right at the bottom actually what I'm
gonna do is I'm gonna make this just
tiny bit so set below that
and this blinking cursor at the bottom
and once I I see this banking cursor all
I do is press Q obviously you couldn't
see what I just typed but I just hit the
letter Q to get out of MA and so that's
just an overview of like some of the
very basics all right cool all right so
next slide some helpful shortcuts so one
of the things that actually I teach
almost everyone I work with who I see
not using things and you don't always
have to type everything in your terminal
by hand so there are some really cool
shortcuts or some really cool helpers to
navigate just the terminal itself one
example is I can type clear and I'm
actually going to show this now so you
can see all my stuff is kind of pushed
to the bottom so I write clear and it
clears it up so it just like moves
everything everything up I can use my up
arrow so instead of typing clear again
all I can do is hit my up arrow
and you can see I didn't type anything
right it just gives me the previous
command so it can hit up up up up each
time and it shows me over all the
previous commands match will also tap
complete things which is great so if I
want to say for example if I want to
write a command anything that might
route shell knows about it will try to
autocomplete so in this case I only type
CL and then hit tab and it actually
suggested a bunch of stuff to me so I
can do this edit and it autocomplete so
it just works like a tab complete or
autocomplete let's say in your IDE for
example if you're writing code that also
works with directories which is really
helpful so there's a lot of really cool
stuff oh yeah and so Smith that just
said that I can also hit ctrl + L to
clear my screen so hang on ah yes I can
also there's also a shortcut so speaking
of shortcuts there's a bunch of
shortcuts with Khan
trol plus something so the most
important ones to use are I can do so
let's assume I just type something and I
want to go back to the beginning of the
line I can do ctrl + 8 and again you
don't see what I'm typing but just trust
me ctrl and the letter 8 takes me to the
beginning of the line and ctrl + E takes
me to the end of the line so just moves
my cursor to the end of the line one
other helpful thing is if I'm typing
multiple words and then I realize oh I'd
actually want to change this ctrl + W
removes the word that's right in front
of my cursor so which also and spaces
are also considered words so this
one-take will take me to this will take
me to the beginning of the next word
including the included space so I can
basically just like remove all the words
that I've just typed or the commands
that have just type one by one and then
also if I want to earth type of command
but I don't actually want to run it ctrl
C will basically just cancel this and
move me to the next line so there's a
bunch of stuff and again this is
something that you know it this is a
good thing to do on cheat sheets to just
look up you don't have to memorize all
this but at some point it will become
second nature oh the one really
interesting thing is control all right I
don't want to show so I've shown you
control just the arrow right which loops
to all the commands let's assume I want
to find the LS command and it just wrote
because it's like super complex one
thing that you do is hit ctrl R it takes
me to the back search and then I could
type LS for example and you can see it
searches in my in my history for this
terminal it searches all the times that
I've written anything involving LS and
then each time I hit ctrl R again it
shows me yeah you can see I don't know
I've done a lot of LS so each time it
shows me like the last time I've used LS
so this isn't really the way I always
use this is for my mark which is the
copra generates these slides that I've
just shown I can never remember the
syntax so I just ctrl ctrl R and then I
find the mark command and I don't have
to memorize it so this is super helpful
um there's a question that Chad actually
was a terrific pitcher in control and
command I think it's actually exactly
the same so on my macbook it's control
art and I think it's the same in the
terminal on Windows if you use git bash
alright cool so navigating across system
so now I wanna know where I am
one thing I want to do I don't want to
just be stuck in my file system forever
but I actually want to change where I am
so I can for example execute code in a
different directory so there's a bunch
of things I can do let's assume I open a
new directory and as I've told you oh
this is this is fun sorry okay
so I actually set my this is really
funny I actually set my terminal to open
in the same to open a new tab in the
same directory where I have my pre must
have generally all the terminals by
default are set to open in your home
directory I set mine to actually open in
the same directory but let's assume I'm
PWD I'm in this in this directory and I
actually want to go one level up for
example to see all my directories that I
have under code so I can do CD and then
I can either type in the name of the
directory that I want to go to so users
Sam code and as you can see I am now in
user Sam code or alternatively one of
the things I can do is use one of the
nice elias that we have in this case
it's dot dot to go one level up so now I
am in user Sam right so so the thought
that helps me navigate around there's
another CD change directory shortcut
that's the tilde tilde it takes me
home directory so as you can see uh this
is the same user Sam let's say I go back
into code so now I'm in in user Sam code
and I go to the CD tilde and back up in
my home directory so the key shortcuts
are or aliases say you can remember here
are put back the tilde alias for your
home directory the dot which just means
the current directory and the dot dot
which means the parent directory and one
of the things that you can also do is
just concatenate these so I can say for
example I want to let's go back to code
terminal workshop I can say and just use
the dot dot as a file path so this takes
me not just one but two levels up so in
the second the grandparent and then I'm
back to the user Sam so I skip the code
directory here so just one one thing to
keep in mind is this with CD you kind of
navigate around and you have a bunch of
aliases to take you to specific
directories all right cool basic file
operation so I'm gonna move a little bit
faster just because we're really tight
of time okay
there's a bunch of basic file operation
so you might want to use the key words
here are make dear touch and open so I
can show this real quick as an example
so let's just go back to my code
terminal workshop directory I'll do an
LS to see what's in there is clear real
quick so I can do a make deer call it
mine here and as you can see here I just
created a directory called my dirt ok so
so I can go into my dear and then I can
if I want to create an empty file
honestly touch I multi just use it to
test whether I have permissions to
create anything in there usually
obviously if I'm creating like any kind
of file I'm you know using a text
for that so touch you file dot txt and
you can see I created a new file and
then if I want to I can open your father
PEC and this will open it in my whatever
is set up as a default editor and this
case is really just by Mac OS default
text editor that opens new fado text and
I have a new file that I've just created
here so just just one example of how you
can make quickly if you want to often
like for configurations or if you want
to store anything there this is kind of
a quick way to do this and you don't
have to click around or your text editor
and navigate in your finer and stuff I
really like doing this all right
file operations number two this is where
it gets really interesting because you
can do copy you can move and rename
files and you can remove files from your
command line and this is where I think
things start getting more powerful than
if you do them in your in your finder
because you can sort of bulk modify
stuff so let's assume I have a file
hello.txt okay
Janell X I have hello detects new photo
text I can copy hello dot Tex to let's
say hello to dot Tex just making a copy
and you can see I now have hello dot Tex
and hello to dot txt and the content of
those would be identical so now I can
rename on the command line
hello to to let's say hello three for
whatever reason rename that and then if
I do LS again I have hello and hello 3
because hello to was renamed - hello 3
this is pretty straightforward so this
is this in and also if I want to I can't
remove let's say clean up me Father
Tex so I can also delete my new file dog
tags by just typing RM for remove so
this is where just gets powerful is by
using a wild cards so the wild call
upper Rader is the asterisk little
star and this is where I can do bulk
operations for example if I wanted to
remove every single file called hello
that's something in this directory
I could just say remove hello okay I'm
doing this this is let's consider it
irreversible so please do use this with
caution and but I can basically just say
remove hello dot Tex
hello anything that starts with hello
I'm never doing or less again I have
nothing in there because I just removed
hello dot Tex and hello 3 dot Tex so
this wild collar operator is really if
there is one thing you take away from
this that you don't know yet I think
this is super super helpful because that
allows it to do bulk operations and you
can also use it in a way such as hello
star for example or dot CSV to remove
all your CSV files or you can do it for
example through an LS to just list
everything to show everything that
starts with hello and as a CSV file etc
etc so you can do lots of stuff with
that
ok look at that file content so and
again like I'm picking up speed a little
bit just to get through the key stuff
here again this is all going to be on
the slides so I have a file a sample CSV
file from the New York open data website
as an example and there's a bunch of
stuff you can do to look at CSV files so
again just kind of going back to what I
said about this is a little bit aimed at
data have folks and this is the kind of
stuff that you do a lot or that I do a
lot so let's go see the up into my
directory soon LS to see I have my
permit sub CSV so that's us human I've
downloaded permits dot CSV and I want to
know what's going on with this file and
I don't know I said I want to open it
and like Excel or read into a panda's
data frame or though all that I just
want to kind of want to get an idea with
what's in that file so I have different
options one which is a little bit of the
danger zone but I can use a command
called Cat Cat really just print the
entire
file to the screen the reason why I'm
saying this is a danger zone is because
that might be a very large file and it
might just portion a lot of content to
your screen in this case I know it's
large but it's not crazy large so let's
just run it summer running a cat and it
basically just printed everything in
that file so screen and it can if I want
I'm actually able to just scroll through
this so cat was kind of cool for smaller
files in particular to just print the
whole thing to the screen immediately
and you don't have to open it separately
another really cool command is that I
actually found more useful than hat is
head and you also have a matching tails
ahead gives you the first n rows of your
file that you're looking at so in this
case if I have head permits excuse me
and I think it's the false of five or
ten ten sorry the false till the first
ten rows so in this case especially for
like things like CSV files this is
always really nice for me to see the
header row and to get a little bit of
the data so this is literally the head
if you're using pandas this is the head
for pandas and then in addition to head
will also have a tail which gives me the
bottom here Rose nice and I do actually
have two okay head if I and again just
like your pandas if I want to only see
the top something rows of this this file
I can also do - n which specifies the
end like the end number of rows that I
want to see and I can say I only want
the top two rows so now you can see
let me repeat this and just do yes now I
can only it only prints the top two rows
just keep in mind that this is a CSV
file
obviously head does not know that this
is a CSV file so it doesn't give you the
top two data rows but it gives you the
top two text rows and or text lines and
in whatever file is how you're looking
at and you can do the exact same thing
with tail boom so that gives me the
bottom two lines
pretty straightforward this is super
helpful I think if you download a file
you're getting file from somewhere and
you just want to get a quick look
without opening anywhere else like head
and tail cat head and tail is for
helpful I'll actually pause for oh I got
it yep so head gives you the the top
rows and tail gives you the bottom rows
so bottom so tail starts counting from
the bottom head starts counting from the
top actually possible quick to see if
there's any other questions yeah so a
lot of the things this is this is an
incremental workshop so I'm actually
going to talk about less to so thanks
for thanks for mentioning that it's all
coming any other questions
alright great let's keep going
so speaking of which so a nicer way to
navigate around files is to use a
comment called less less is basically an
interactive text reader that allows you
to do a little bit more navigation so
one thing that you can do is just say
less and the premise of CSV and the
reason why it's called less is because
there's also program called more less is
basically more oh my god less is more
but with more functionality UNIX things
are funny and weird and quirky and it's
been going on for a long time and this
is like read up on it it's pretty funny
so if you say less permits that CSV less
is the interactive text reader so again
it shows you it starts at the top of the
file you can navigate around really just
using the arrow keys up and down to go
through the rows you can use your
spacebar to page between whole pages
right or there's also some really cool
built-in functionality for searching
unless if you use a forward slash so
again you see the blinking cursor after
the colon at the bottom if you use a
forward slash that get
into search mode so now I can for
example say I want to find everything
that says film so I just type in film
and it shows me all the the search
results for film I can navigate through
those search results using P and N P
stands for previous result and stands
for next results so well this is the top
of the file so I keep going down and and
you can see just bumps the line that it
where it finds that search result to the
top of the screen so it just moves it up
and highlights it keep in mind the
search is case sensitive in order to
make it case insensitive okay - I wait
okay and then you ignore your pace and
searches so - I gives you case
insensitive search so now I can also
search from oh great oh this is not
found sorry I'm like getting mixed up
okay ignore cases there we go
okay so and then I can navigate through
that even though I've searched for lower
case phone and again just like with MA
and with man most of the time for a lot
of UNIX programs the way to get out of
whatever it is you're stuck in just hit
Q and I'll get you back up alright so
that was less next up
oh I've actually already explained
finding set text and files so less is a
really good way to do this there's a
bunch of other ways so this is option
one as to use less option two is he used
something called Greg grab actually I
don't know you might have hurt someone
you reading saying like oh I'll just
grab for this like grab kind of and by
that we mean gr e P not GRA V not grab
but grep so grep is also
unikz told it comes built in your shell
that allows you to search in files from
your command line so I can show this
real quick so we just type grep then you
type your search word yes sorry I get
the syntax like that sometimes you
search a certain search word in this
case I'm crapping for the word film in
my permit csv file and it doesn't give
me a result why do I not get a result
because it's case sensitive so if I grab
for film
it now prints every single line where it
finds the word film um the other way to
do this is to say crap - I and then
search for whatever case I can even do
this so - I makes a case sensitive and
again this is one thing that like occurs
in so many contacts in your shell so
many programs like the - I usually makes
things case insensitive okay and it just
found and then grep just prints all the
different all the lines where it finds
that search result
so again if you're working with data
like this is occasionally pretty helpful
to just search really quickly for a
specific word or specific lines that
contain the thing that you're looking
for you just grab for it alright one
thing one way - the way I use is a lot
to use grab a lot is if I don't want to
just print all the lines where I find
something but I want to actually see the
recurrence and Swasey I see you're
asking to go back to the slide for less
I think this is it
I would like to keep moving though but
the slides will be online and you can
totally do like look look things up
afterwards just in the interest of time
okay so sorry jump in back the pipe
operator so the pipe
operator chains any two commands and
pipes the output of command eight of the
first command into command B so I'm
going to show an example and I'm going
to clear my screen so one other tool
that's super helpful is word count WC
word count - L counts the number of
lions in a specific file so in this case
if I want to count the lines in my
permit dot CSV I do WC - L permits dot
CSV and it tells me I have 42 thousand
rows again keep in mind word count again
doesn't know that it's a CSV file and
that it has a header row so this always
includes the header row if you're
looking at data if it's CSV files
specifically it just says this is the
number of lines that I see so one way to
use this is to pipe the output of your
grep to your word count okay so I'm
going to show this by grabbing right
case-insensitive
grab so I want to see get all the lines
that contain the word film so I want to
see how often do I see the word thumb
and then pipe this pipe this - word
count and keep in mind I don't need that
argument I don't need the permit such as
the argument here because word can knows
through the pipes that it should be
counting this input it should be taking
this as the input rather than having an
argument as the input all right so what
do you think happens I'll give everyone
like a second to think what what do you
think is the output of this so so the
output of graph - iPhone permits etc etc
pipe word word count - L will be a
number oh that's a fantastic question
but I'll finish this and so be the
number of
times that the word sorry the number of
lions where the word film occurs okay
which is probably I don't know somewhat
less than the 40 mm and we have enough
file right we have exactly seven
thousand four hundred and ten Lions
where the word film occurs which means
there could be multiple occurrences in
one line this is really just to give you
an idea of this but again like if you
know your data pretty well and you know
your CSV structure pretty well this can
often be super helpful so yeah we have
7/4 out 7410 lines that contain the word
film might be multiple mentions of the
word film one thing that you could get
really sneaky is to do this and
basically be prescriptive about your CSV
structure and in this case we know it
only occurs once per line alright great
so that was um I will actually skip this
part just in the interest of time
actually no this is well we'll have time
for that quote okay so this is searching
stuff in a file that you already know is
there so I know I have my permits dot
CSV and I just want to do some like data
manipulation data searching and stuff
cool
so one thing that you also might want to
do is finding files and I think honestly
in this case I find the terminals so
much easier to use
then the Mac OS search I don't know why
but the Mac OS search to search for
specific files with a specific file tile
types just always turns into a huge pain
so one of the things you can do is use a
command called find then you always have
to specify the directory and remember in
this case in this example the directory
could just be thought right and then you
have to specify the flag
which could be in this example there's
tons and tons and tons of flags to find
this is kind of the most common one
either - name or - I name again - I is
case insensitive so - - name or - I name
and then you can basically just search
for anything in your quotes that is in
the file name somehow so I'm going to
show this correctly so in this case
where am i okay so I'm going to find in
my directory um let's say I just want to
find any CSV file right so I want to
find anything again you can use asterisk
for a wild-card I want to find anything
that says Oh cuz I did not use my -
Maine flag so I'll just do that again so
again find in this directory and
everything below fine does recursive by
default find anything that in the file
name has something matching dot CSV
something that ends in dot CSV in this
case not that exciting it's only my
permits dot CSV to show you that it was
really recursive I'm actually going one
level up and just repeating that let's
say with anything that starts with NPI
I have a lot of NPI files it's a health
care provider index files and I use this
a lot for testing so I know all my code
all my repos have a bunch of copies of
this so I can do fine dot - name
actually let's do a - I name to see if
there's anything that's also an
uppercase NPI there anything that starts
with MPI bah blah blah and instance he
asleep and it shows me a bunch of MPI
CSV files the way I use this a lot of
times which is really cool is basically
saying how often do I have this file in
my directory so thinking back to the
pipe operator and work count is I can
basically pipe the output of frying
- my word count so this instead of me
counting each line one two three four
five or I can just say this boom and it
tells me it's there nine times so this
is a really cool and this is something
that I don't even know how I would do
this using my finder or Explorer on
Windows or Mac this is something that I
think is just a really nice quick one
liner in your inner shell anything else
about find again keep in mind it's
recursive by default which is super
super helpful a lot of times for a lot
of commands you have to specify
recursiveness oh and the other thing you
can also specify a specific directory to
search and so it's not just dot as in
like this directory in anything below
but you can say okay find everything you
know let's say code
let's find everything in my code
directory which in this case is the same
that says MPI dot CSV so - so there's
ways to basically point it at a
directory to look at great any questions
so far about fine and again like find
has a lot of flags a lot of
functionality this is just sort of the
most frequently used one for me right
this one I'm going to go through real
quick environment variables and profile
files so environment variables are
system-wide global variables so your
shell knows about you can let you just
type in in and it will show you all the
environment variables I don't think I
have any passwords stored here so these
are all the up here is a password and my
Postgres connection screen I won't show
you that it's all dummy data that's all
our test databases I don't have any
concerns so M shows you all the
environment variables that your shell
Kearney knows about and you can echo a
specific variable by referring to using
the dollar
sign so this is across shells variables
are referenced by the dollar signs so I
can say echo user so user and and
everything is case sensitive in your
shell
so my user is set to Sam or I can say
this is the thing that you probably see
a lot your pythonpath oh that's
interesting my Python path is empty
let's see about my path okay so my path
for example has a Conda things will see
and then executables and binaries so
this is so now we learn two things one
is echo echo hello I go just print
anything you throw at it and the other
thing is you reference environment
variables using your dollar sign so now
the question is obviously cool these are
the environments variables that are
built in right that are set somewhere
how can I set my own environment
variables if I want to use them in any
like script for example or if my if my
application wants it again like my
Python path for some reasons empty a lot
of times it says add it to your Python
path or set your path so you set
environment variables using a command
called export I can show that real quick
so the syntax is export and then these
assign a name of the variable and then
you say equals the value so this is
pretty straightforward exported my bar
equals 42 or some text in quotes shells
are very very sensitive to spaces
quoting etc etc so make sure like the
syntax is correct
one thing I think you is echo export my
var and when I'm setting it I don't use
the dollar sign it is hello this is very
boring and then I can say echo my var so
now I use the dollar sign to references
well it says hello because that's the
value of my variable I can also
overwrite
so now I want my bar to be say 43 and I
echo it now it's 43 so this is a really
nice way to set your environment
variables in your shower and your in
your terminal
it's basically a global variable that
your particular shell knows about and
the only problem here is if I open a new
tab and I'm using a different terminal
from usual so I'm not sure if this
actually sources it but let's see what
happened for type echo my var and you
tap it's empty because we wherever I set
my environment variables only that
she'll actually knows about that
environment variable that I just said
that kind of makes sense I guess because
there is a scope to that variable the
way to make that permanent to make if I
want my bar to be available in all my in
all my shells like in all my terminals
that I opened by by default is to send
what's called a profile file so you
might have heard of something called a
bash profile or a shell profile or bash
RC or other things and I'm really just
going through this real quick there is a
profile file that every terminal reads
out the startup and it it does what's
called sourcing your environment
variables so if you're using bash for
example if your own get bash it's
usually called bash profile or that
profile bash RC there are differences
between them please do write up but it
gets pretty nitpicky for seashells or
the whatever the default is on Mac OS
right now it's a file in your home
directory called Z shell RC and I can
Capra's or as we from before because I
know mine is pretty small and this is
basically everything that's in my sea
shell RC so it does a bunch of exports
and sets like I use Apache airflow it's
it's maker
floo home to this it's Conda at some
stuff if you add it I've got a bunch of
aliases for yet and every time you open
your terminal your your terminal will
look at this file and your profile file
and create all these variables so you
have them available so I'm not going to
show the example but you can totally go
through that in your on your own when
you have the site okay last thing shell
scripting 101 instead of typing all
these commands to the command line every
single time that gets pretty annoying
you can use you can basically just dump
all your commands into a script so I can
show you that clear and I go into
terminal workshop okay so I have this
file
Sam script but it's H that I've prepared
and again I can use cap or less for
example to show what's in the content of
this file and in this case is just one
line that echos something really boring
the way I can run the script there's
multiple different ways but I can
basically say for example Sam script
broad as H this is one way to execute my
script so what I would expect to happen
is for this is for the echo to just
print to the screen so basically all I
want to see is hello this is the script
saying hi if I execute the script well
that doesn't work
permission denied why is the permission
denied if I go back to the line that I'm
highlighting here and this block and at
the very beginning actually shows you
the file permissions and in this case
what I see is I have read/write
permissions so I have this on the slides
for more detail but basically you have
read wide execute read write execute
read write execute for user group and
other and in this case I can only read
and write but
can't execute my script so what I have
to do is change my permissions the way
you change your permissions is yet
another command called change mod change
the mode of my file and I'm just gonna
make some magic happen right now real
quick
d + X so I'm setting the user gets
execution rights on samskaras SH I'm
changing the permissions of what I could
do with a script so if I go back and do
an LS L a let students just on the Sam
script up not SH you can see that read
write execute so now I have set plus X
that means I can execute and run my
script ooh
really really really basic this is just
the very beginnings of shell scripting
you can do for loops you can do Wiles
you can do pounds you have data
structures in there so shell scripting
is a whole new topic on its own this is
just basically me showing you that you
can take any shell command and dump it
into a file change the permissions make
sure the permissions are right and then
you can just run it all right I'm going
to wrap up so we have a couple of
minutes left at the end for
congratulations this was it I'm going to
wrap up and do a quick summary at the
end and then we have a couple of minutes
for questions so what we've covered
directory navigation of file
manipulation
so remember PWD LS CD copy move for move
and all that with covered searching for
texts and finding files with a copied
less and grep and find um we've covered
environment variables and your shell
profile and I've showed you a tiny tiny
little shell script this is this section
is actually super important because this
really you have a tiniest tiniest
tiniest overview anything I could
squeeze into this one hour
other important things to look up sudo
command super super important super sudo
command means you basically overriding
default permissions and you're doing
something as a super user so you will
run into the sooner or later so look it
up what sudo does um one thing that's
super helpful this is just a nice to
have is setting aliases for shell
commands you might have seen that I have
a bunch of aliases for my kid commands
just because I don't want to type that
much text manipulation so using them as
a text editor even if it's just the most
basic commands from them super super
helpful for all your data folks out
there CSV kit is a super awesome library
that allows you to do some really cool
CSV manipulation and your command-line
strongly recommend looking it up so
remember when I said like your find or
your grab or all that doesn't know that
it's a CSV file it has a header of row
etc etc CSV could basically knows that
you're dealing with a CSV file er we're
dealing with data and it knows about
columns and knows about rows so really
really cool one other interesting thing
to look up is ways to kill and exit kill
processes and exit things for example if
you're starting up a Jupiter notebook
you can control C it sometimes processes
hang you have to do other things
so do look that up how do you accept
basic ill processes and what's the
difference between control xenia control
C control D and all that and the nurse
with other front stuff like Cal for
example date you can whoops check disk
space looking using things like D udh
there's some fun utility is called cows
say cows a is just over writes echo and
prints a cow so there's a bunch of other
fun stuff for that's built into your
your shell but this is green Aegis I
only just scratched the surface so and
again the slides are going to be on
line so I know this was like a whirlwind
tour pretty fast if of all the terminals
staff I hope this was helpful I hope
this has given you some idea some idea
of like what the key things are does
anyone have questions we have two
minutes left for questions there aren't
any questions I can maybe see if cows a
works oh no that is per install it any
other questions
okay it was fine Oh angel that's a great
question so angels asking how important
is bash or shell scripting for job
searches you mean for the job search
itself or for actually for for being
getting hired I assume you mean like for
for employers so this is really
interesting because I I actually think
based on my experience interviewing
candidates and looking at resumes and
stuff no one ever tests for that in a
job search like no interview will ever
like test your scripting skills I think
it's something that comes out very
quickly in your productivity um so I do
think being really good at scripting
things and navigating around your shell
will increase your productivity pretty
quickly and will just show that you kind
of know what you're doing and will you
know stop you from like manually having
to do a lot of a lot of clicking and
stuff I do think in terms of like
actually finding a job it's usually not
part of the interview process so you
might not meet that Oh so Kimberly I'm
sorry go and top down Candida asked his
feet kid like here a number of times
missing words at 3:05 I don't actually
know about CSP could specifically I
would recommend look
it's super it's it's got a bunch of
really cool stuff in there so that's all
I can say is I don't know exactly but
try it out and then Kimberly asks
whether there is a good resource for
translating shell commands into bash
windows friendly shells so two things
one option on Windows is something
called git bash which crash usually
comes with if you install git for
windows it will also install git bash
which is a wrapper around your windows
command line that is bash like it's not
that great honestly but it does a job
for some basic stuff about translating
between bash or just the UNIX shells in
Windows shell I don't actually know
fantastic question I will find something
I'm actually very very curious I'll find
something and put it into the repository
put it in the slides
that's a great question thanks Kevin I
know we're over time sorry everyone
any other questions uh grips I would run
often to increase efficiency great
question so I think I use find on the
command line lots of some many scripts
to run but it's just commands to run
there's other things you could do to
have like a little script that for
example copies or bulk renames files so
if you do a lot of file operations I
think that's one of the examples like
just moving files from one from one
directory into another for example those
kinds of things that you usually do by
clicking for bulk operations I think
that's the biggest efficiency win yeah
any other questions all right
I think and feel free just going back to
my slides feel free to connect with me
on Twitter if you have it as an SP bail
or connect with me on LinkedIn
if you have any additional questions
more than happy to answer them let me
know I'll hand this back to Richmond to
wrap up thanks everyone
I can hear and see you yes okay great
thank you so much Sam for your
presentation and there will be recording
which I will post on the data umbrella
website and thank you so much for
joining us and thank you for the
presentation a lot of people really
enjoyed it thank you so much that's
great thanks for all the questions they
were really good
