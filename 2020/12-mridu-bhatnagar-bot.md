# Mridu Bhatnagar:  Building a Conversational Bot for WhatsApp w/Twilio & Python

video:  https://youtu.be/dqab-FcAirA

hey everybody welcome to a data umbrella
webinar
um i am joining um from new york and
uh i'm just gonna do a a brief
introduction about
data umbrella and then we'll get started
on the um
webinar um
so it'll be it'll sort of go like i'll
do the introduction
um we'll do the talk and then you can
post any questions
in the chat or in the q a and
we'll sort of answer those as they pile
up over time
and just to let people know this
will be recorded and will be available
on our youtube
i posted a link to youtube in the chat
if you're not able to see it just let me
know and i can share it again
about me i'm the founder of data
umbrella i'm a statistician
data scientist and i am also an
organizer for the new york city chapter
of
pi ladies and i am on twitter at reshma
s
okay the mission of data umbrella is to
provide a welcoming educational
inclusive
space for underrepresented persons in
the field of data science and machine
learning
um check out our website we are pretty
much on every social media platform
as data umbrella and we are a
volunteer-run organization
pi ladies is an international group
there's
over 100 active chapters and it's for
python it's for women and gender
minorities of all levels of programming
experience
you can follow us on twitter as well
i want to go over a code of conduct
we're dedicated to providing harassment
free experience for everyone
be kind be professional and that also
applies to the chat
as well
um on the data umbrella website which is
dataumbrella.org
there are many resources available for
um you know responsibility ethics
inclusivity diversity and also you know
learning r
and python and open source so feel free
to check those out on our website
um we have the best place to find out
about our events are on meetup i also
joined an event for next tuesday's
webinar which is on
creating nimble data processes which
will be um
which will be fun um if you are
um on linkedin i share a lot of articles
including job postings so
if you're interested in that feel free
to follow us on linkedin
feel free to subscribe to our youtube
channel for our videos
um and follow us on twitter for updates
and so now we're going to get started
i'm going to turn this over
who is joining us from central india
in dore right um yeah thank you so much
for joining
us um and it's 9 30 wonder time
right
[Music]
i'll just
i'll share my screen
uh is the screen visible now
i see drag and drop files i think it
might just be loading yep now we can see
your screen
all right is it visible
yes okay yeah uh
hello everyone i'm ridhoo bhatnagar i'm
from india
and i am a software engineer by
profession
and when i am not programming or
building stuff then i
love giving talks at various meetups and
conferences
so during this time i have been giving
talks all across the group
in every possible meetup that is
possible
so into today's session we'll be
covering up
about building a conversational bot for
whatsapp
and here is the bot uh you like
on the left hand side you may be seeing
uh
uh what jf uh
this one this is the what i had recently
built it is vocab but
and the features it includes it are
it tells you the word definition it
tells synonyms it tells antonyms and it
tells examples
based on whatever you query it for so
like it is squaring
examples for amazing so this would
return some examples for amazing
so this was the board that i had
recently built
and the session for today we would be
covering that how
you too can build any build any of the
bots
and bring your ideas to life so
moving ahead the requirements for
uh this session include that
what i have used is i have used python
version 3.6
greater than 3.6 and then we will be
using flask
for running the web server and then we
will be using
another package that is ngrok ngrok is
basically used for testing up
our bot with the mobile application so
there is there needs to be some way
where we can
just test whether the bot is working as
expected or not
so for that we will be using ngro and
all these things that i have mentioned
are pip installable so pip
is the python package manager you just
have to do
pipe like pip install flask paper
install
ngrok uh sorry ngrok is not
prep installable for ngrok you need to
go on to
ngrok website and from ngrok website you
can download ngrok
so that is how you install ngrok and
then all you need
is a smartphone with whatsapp installed
on it
and then there needs to be a twilio
account
so this is the url at the bottom is for
creating the twilio account
i can maybe share this link
or okay later i can share this link
so that if you want you can just open up
and create your own accounts i will just
share it just a second
if you are following along or later you
want to create
a twilio account you can use this url
that i have put up in the chat
the initial account trial account is
basically free so it won't charge you
anything
so moving ahead here is how you can
configure your twilio whatsapp sandbox
so once you have created your account on
twilio
you can just go on to twilio console sms
whatsapp learn this url so first
and foremost thing is to create uh
the
account on twilio and then there is
something as twilio sandbox
so our application basically will be
communicating to
twilio so imagine that you have opened
your
whatsapp and you are querying your
whatsapp
with uh like suppose you wanted word
definition
or you are saying hi to your whatsapp so
whatever message you are sending to the
whatsapp should go to twilio so we are
trying to make a connection between
whatsapp
and twilio so for that connection to
happen
this url is what is needed
connection between
whatsapp and twilio
so the url that i had sent above was for
connection between
whatsapp and twilio and if you have
already created that
this account and you go on
to this url this is how your page would
look like
i'll just expand it
this is how basically your screen is
going to look like
once you are on our twilio sandbox
i cannot uh live uh like i cannot go on
the actual website and show you live
because there are some secret codes that
are there
that are not to be shown so make sure
that whenever
you two are using the twilio application
you hide your own codes don't
just go and put it up on github or
somewhere these are your own codes
and so the left hand side number that
you see
here is something that you have to store
you have to save it on your mobile phone
and this is your joining code so once
you save this contact number on your
mobile phone
this contact would basically appear on
your whatsapp contacts
so this is your whatsapp contact
number and this is the joining code
and everyone is going to have their
different joining codes and joining
codes
code needs to be hidden because after a
certain point of time when all the
twilio free credits are over
it are like every query is chargeable
so that's why don't just disclose your
secret code otherwise others will be
able to use it and your free credits
will be gone so that is the reason
basically to hide it
so next step is after you create the
account just
save whatever number comes on to your
screen
you will have to save it on your phone
and then uh
this is the joining code so on your
whatsapp what you have to do is the
first
message you will see is join followed by
whatever is the code this message you
will have to send on the whatsapp
now this whole setup make sure that our
whatsapp is being connected to twilio
this is the very first part of the chat
bot
okay and now as if you have already
saved the number
so this is the initial step of the board
that we have already done
i saved that number using the name vocab
bot you can save it by anything that you
like
so this is the very initial step
and now how we will go on doing this
programmatically
is what i what i am going to explain in
the next steps
so the next steps include creating a
python virtual environment
so once you create once you have the
initial thing set up
all you have to do is by create a python
virtual environment
so i'll just briefly explain what is
meant by a virtual environment in case
you don't
know so what happens is in python
we install all the external packages by
doing
pip install and if we are not using the
virtual environment
all these packages get globally
installed
on our system so as a result a lot of
times between
multiple projects there can be version
conflict
suppose you are using django one
suppose you are using django two in one
project and django three in another
project then
it is difficult for the project to
determine that
which django version should i use
so to avoid scenarios like these we use
python virtual environment and here are
the steps to create
the virtual environment so that there is
no virgin conflict
now in case you are a mac or linux user
uh all you have to do is run the
following commands
so mkdir is basically for creating a new
directory that is the whatsapp bot
and the cd was for changing the
directory
of the bot and then python minus
m when whatsapp bought when you do uh
this command creates the virtual
environment
when is the package
and whatsapp what is your name of the
virtual environment that you are going
to create
if when is not installed on your system
you will have to install
when on your system
and then once the virtual environment is
like once this
virtual environment is created all you
have to do is
activate the virtual environment that is
source
whatsapp bin activate
so then you have to activate
this virtual environment and ah you
would come to know whether the
environment is activated or not by this
last command
so if you are able to see on the left
hand side that
such a thing is coming like whatsapp
which means that the bot has got
activated and now i am just installing
my requirements i need a twilio library
then i need requests and request
is the http library in python it helps
us in communicating with the external
third party apis
or any kind of apis for that matter and
then
flask is a micro web framework in python
and python.10 is another package it is
used to save all our secret keys
so
and if you are a windows user then the
commands are different
so for making the directory you need to
do md whatsapp bot for changing we have
whatsapp what
then we have python minus and when
whatsapp bot
this is for again creating the virtual
environment
then we are trying to activate the
virtual environment and then
similarly you just need to install all
the requirements
so before we go ahead i would like to
tell that twilio we are installing so
that
uh from twilio we are able to send some
req
response to the bot so if you send any
message to your bot
the bot must reply something and for the
getting the reply from the bot we need
to install a twilio application so that
it sends us
some response and request library is for
communicating with any third party
library
flask flask is basically
the micro frame framework that is used
for running the server at our back end
and then python.10 we are using so that
we don't disclose any secret key
to anyone it needs to be saved on our
part
and we'll see uh everything working
later in the session and now before i
go on with the code are there any
questions or anything till now or
something that i
haven't explained in greater detail so
you can ask the question if there i
didn't
i don't see any questions uh so far
except is the webinar being recorded
which it is um but if anybody has any
questions feel free to post on the
um um yeah we will have a link to the
slides afterwards
okay
yeah so moving ahead the next step
basically is
that how that we need to clear create a
flask chatbot
service so we are trying to create the
service because
we need to send some data to the user
so the workflow basically is user enters
the query to the whatsapp
and then instead of a human being
replying to you there is a bot
there and instead of human the bot is
basically replying to you
so for this whole workflow to take place
we need
flask applications there needs to be a
server running that would keep on
replying to your messages
so this is how we create the very first
step is
so uh in the presentation here i won't
be explaining the process of building
vocab bot
but i am explaining a general uh
giving a general idea that how
you can create your own bots and bring
your own ideas to life and
this is the very basic like hello world
of bots we can say like that this is the
very basic bot that you can
create on your own and then feel free to
incorporate your own ideas and convert
those into bots
so i am just explaining a very generic
process
so this is the very first step of
creating the flask service
so first i am trying to import
flask class so i am doing from flask
import flask in line 1 and then
i am initializing the app from flask
class and all i am doing then
is app.root hello world
so whatever communication is going to
take place
is going to take place through this
endpoint hello world
i am going to post my messages on hello
world
endpoint and whatever the user
is sending will also be coming on this
hello world end point
so we'll be seeing ahead how this
happens
and app.run allows us to run the server
abdul run basically allows us to run the
application
and by default the application runs on
port number 8000 localhost port 8000
so our initial very initial setup is
this now the next
step is when i have already created one
endpoint and i know that this is where i
need to send my data
the next point is how are we going to
receive the incoming message from the
user
so now for that to happen all you need
to do is
app dot hello world method
post we are trying to post something
and then we do request dot values dot
get
and body dot lower so what this conveys
is that if the request message contains
a key
named as body then we need to we are
trying to
fetch the value corresponding to this
body
and if it doesn't find any key
corresponding to but
like if it doesn't find the key body
then the message would be
empty and then i am trying to convert my
whole message
into lower case
so that is the meaning of this whole
line request
dot values dot get i am trying to
get the value and
whatever is the value that the user
sends to the whatsapp bot so in your
what if you write hi
so here in this function your incoming
message would be high
if the user is sending hello the
incoming
value of incoming message would be hello
so
line number six is just for retrieving
the incoming message by the user
next step is uh
we we like want to willy
to send a message to the user back
so for that purpose twilio has a
messaging response it has a twilio ml
library in it so if you want to check
out
all these documentation are very well
explained on the twilio's website
website itself so whenever you are
building one for your own
you can just check the documentation
there wml is the library
so what we are trying to do is we are
trying to initialize this class
messaging response then we have a
response object with us
and in the response i want that i should
send a message
so all i am doing is response dot
message and here
i am initializing the variable message
with it
and then my app is still running for
running my app i am doing
app dot run line number eight and line
number nine
why we are doing this is because this is
a format that is suggested by twilio
so only when you have this format in
your application you would be able to
send
the message back to the user
so step one is user is sending the
message to twilio
that is line number seven line number
eight and nine is twilio is trying to
send back
something to the user so that is what
line number 7
8 and 9 are doing
and now what we want is that whenever
the incoming message is high
the output message should be hello hope
you have a good day
so now i am saying that
a user is entering the message high so
your
value of incoming message in line number
seven would be high
and then when you are doing response is
equal to messaging response
message is equal to response dot message
when we do this thing
from here i am trying to now send
the bot is trying to send the message to
the user
so there is another built-in method in
that library itself that is message.body
so
now i am doing is hello plus the
incoming message
so hello would be
is a static thing that i am sending and
plus the incoming message
so suppose the incoming message is high
so
the returned response would be hello hi
or suppose if i am sending the incoming
messages
i am sending my name itself so it would
say hello
if the user is sending word world so the
output is hello world
so this is a very trivial application of
how
message sending and message receiving
takes place
in this bot
at the moment we are stands uh i am
sending some static messages
that always this is going to return
hello plus the incoming message but we
can say
send dynamic messages as well like i was
doing in the vocab bot
so for sending dynamic messages we need
a
we basically need an api so that we'll
be discussing ahead
but the process of the that workflow of
incoming messages
and outgoing message is this
that you see here are there any doubts
till now
uh yeah the presentation slides i i'll
be sharing
any doubts apart from the presentation
slide thing are there any questions
or have i gone too fast
i don't see any other questions there so
that's good
okay are things
understandable to till now or it is a
bit confusing
okay so we'll just and here uh i'm sorry
i think
this is going to be hello plus
high so if the incoming message was high
the output that
our function was sending was hello and
followed by hello a high
this is a very trivial application just
to make things
easier and so that you understand the
process of building the bot
and usually the way the risk request and
response
twilio accepts is in the xml format
so it is not json format it is xml
format
and the body keyword that we were using
was
this body keyword and if you have to
send any image
so for image you need to use media key
so all this is very well explained in
their documentation
and just for running your application
all you have to do is python app.py
so earlier by mistake i have said that
we are running
the application on port number 8000
so i am sorry for that the port is not 8
000
the application is running on port port
5000 all right
so once all your code is ready and in
place
all you have to do is run your
application so now your application is
running
basically on port 5000
so now what problem do we have is
we want the bot to run on whatsapp
and whatsapp is on your mobile and
your code is on your laptop so there are
two different website
two different devices that we want to
communicate in between
so uh the next step is how how do the
communication between the two devices
happen
so that communication happens with the
use of this
ngrok so initially i had told that you
need to install
ngrok from the from its website so now
next step
is like you open another terminal on
your laptop
go on to the location where this ngrok
has got installed
so usually it would be in your downloads
folder and then
all you have to do is run dot slash
ngrok http 5000
what this will do is this will run ngrok
at port 5000 so now you have
on one terminal flask running on another
terminal you have this
ngrok running there are two things
running
and now twilio will help us in
connecting these two devices
so the terminal would look something
like this when you once you
run your ngrok the terminal is going to
look something like this
okay so now next step is making a
connection with
twilio so now all you have to do is
just copy this forwarding url on
everyone's laptop the forwarding url
will be different
so now next step is for connecting the
two devices you have to just
copy paste copy the url and then
by copying the url you just need to
uh put the url in
in the twilio sandbox for whatsapp you
would be able to
see this twilio sandbox in the console
itself just go on to the twilio website
all these things are available there
and as i had mentioned above add your
ngrok forwarding url in the text box
so you have to add the ngrok url here
and then after adding the ngrok url at
the end you have to put
slash and followed by the end point
hello world that we had used
so forwarding url followed by the end
point that was hello world
so this is basically now everything is
set now twilio knows how the
communication between the devices
needs to take place
and now if you test your flask service
again
you would see that the communication is
taking place whenever you
send hi will you would send you hello
followed by a high or based on whatever
code that you have
written in the in your application so
this is a very
simple application that i had demoed on
how to build a bot
and the next one was
how to how do we send a dynamic response
or how dynamic responses
are to be sent so we in the above
example we were sending
the static responses that
if whenever you send hello it will send
you high
but for dynamic responses what can be
done is
there are lot of apis already available
so there is some examples of apis are
there is google maps api there is cad
pictures api you have twitter api news
api github api
now you can use all these use cases with
your whatsapp so one use case could be
you are sending some location or you are
suppose sending latitude and longitude
and then google maps returns you the
location on the map
or you are sending some location and the
google map returns you that exact map
location
or you you are interested in seeing some
cat picture so you just
and start querying that cat pictures api
or you are just interested in knowing
the trend what is trend
trending on twitter and you are
interested in seeing
that trending twitter thing on whatsapp
so you can just use the twitter api
or you are interested in reading the
google news on whatsapp
so you can use google news for that if
you want your
to check whether the open source project
you are contributing to
has some new pull requests on it or has
some new
issues opened on it so instead of
opening it up time and again you can
just
use whatsapp for it if you are more
accustomed to using whatsapp
so these are couple of use cases and for
the bot that i had basically initially
shown you
so for that what i am also using an api
for that
so there is a dictionary api
that i had used
so the dictionary api was miriam's
webster's api so that merriam-webster's
api returns
all this word definition synonyms
antonyms and examples
and that is how for any random word i
was entering
uh the bot was returning me
a response dynamic response
and using twilio is also net
not necessary to leo we are using
i am using twilio but
original whatsapp api can be used
the problem however with whatsapp api is
that it is not a developer api by this i
mean
is like first you need to be a business
owner
only then you would be able to use the
original whatsapp api
i don't think they have opened the
whatsapp api
for even the developers to use for their
projects
so there is some kind of restriction at
their end and also they are very
particular about what kind of messages
you send
so suppose if someone is trying to spam
anyone or someone is trying to
send incorrect messages then whatsapp
blocks the user
so before deciding on to the use case
for
building the bot first before using the
apis the use case needs to be very well
thought of
that what we are trying to send and
whatsapp also has certain restrictions
that what should be the template of the
messages that the bot is sending
and also with whatsapp uh
the thing is you need to get approval
from whatsapp
for using all these things
so and one way to put this bot in
production is like if you just want to
put your twilio broad
for in production and run it so you can
maybe deploy
it on heroku so i i use my bot
often and i have deployed it on hiroku
as
i don't own any business and i'm not
using whatsapp official apis
so i'm basically i have basically
deployed it on heroku and i have
kept the secret keys with me so it is
just used for private purposes
and uh these days if you would have
noticed
lot of businesses are using whatsapp as
a platform for marketing
so it has pretty good business use case
attached to it
and companies can use it and are using
it for providing customer support
and even some companies are using it for
broadcasting the messages
regarding events and all so there can be
various business use cases attached to
whatsapp
so this was all i had and if you are
interested in building the vocab bot
itself
uh so here is a blog that i had recently
written
for twilio themselves
so here is the bot
url so whenever you are trying to build
it
if you want to build the same one or
trying to have some
idea you can just check out this blog
the blog has
is beginner friendly blog so it has
detailed
explanation of why a particular decision
is taken
and why i am doing what i am doing so
you can just add a lot bought logic
based on your own needs and requirements
so and the last step
after discussing these apis is as
throughout we were using python
so in python just for integrating the
api
there is a simple module that we use
that is requests
so if you want to integrate any api to
your code
all you have to do is use requests.get
now this method depends whether depends
on your api whether it accepts a get
request
post request but all you need to do is
install requests and then there is a
built-in json module
through json what gets done is json
converts your string data
into dictionary data and this dictionary
data in the end is parsable
so instead of sending all your
information returning all your
information you can just
send the needed information to the user
so this small snippet just
explains that part and based on your own
use case you can write your own logic
and a lot of times it it is only about
writing conditional statements
and
if you are interested in exploring all
of this further
so if you are interested in flask then
you can check out the flask official
documentation
and blog link i have already shared with
you all
and then github has a long list of
public apis that you can use
i have only i had only listed a couple
of them so you can
have a look at all these public apis as
well
when you built one of your own so
thank you that was all i had for the
session
does anybody have any questions please
um feel free to um
post them in the chat and i can read
them
thanks so much for the presentation it
was great
and thank you thank you
okay so i'm just gonna turn on my mic
um i don't see um any questions here
um all right so um we'll be sharing the
video soon with the link
um for the slides and a couple of links
that you posted
on um in the chat as well
yeah those uh links are there in the
presentation as well
uh on the last video okay that's great
so they'll be in the presentation
you'll be able to access them um
gabrielle writes um i would have liked
to learn a little bit more on how to
publish the bot do you have resources
for that
uh for publishing the bot i don't really
have resources but i have
done one another blog for twilio that
talks about this publishing thing
so i think i can point to that one the
hiroku part
for publishing that i'm using so
okay
here is a another uh use case so this
was basically not
for uh okay sorry
this one is not basically using whatsapp
but it is using heroku so
from here that publishing part you can
learn
that how you can publish your
work okay uh
we have another question which is is it
possible to add
ml cognitive service from azure on the
bot
um i am not really into
ml and i i am not very sure if that is
possible or not
but you can check this out on
twilio's website on itself they have lot
of blogs and there are a lot of people
working on lot of interesting ideas for
the bot so i think this azure thing you
can find it up there if someone has used
or
not and if this uh azure service is an
api
itself then it can def definitely be
used
any kind of api you can integrate with
twilio
okay uh next question i am new to flask
what does flask
do uh flask uh i don't know if you have
heard of django or not blood flask
like django is a web framework so web
frameworks are basically
used to build websites it helps in
easing the process of building the
websites for you
so without the framework if you start
going and writing
uh the normal python code so things get
pretty
complex and commercially you need to
write a lot of code
and it is not viable to do so so that is
why we
use frameworks for the same so a lot of
things are already built in and then
other parts you have
to develop on your own so flask is
basically a web framework that is used
the next question is um thank you for
your questions afterwards there's our
slack channel where we can post them to
um data umbrella has a discord
um server so and it's on our website
there's a link to how to join on the
website
so if you go to dataumbrella.org
you can join discord that way
um it says the publishing link is not
found
oh yeah just a second i think there is
some problem
[Music]
you will have to scroll down on this
link and
then there is a section where i am
publishing my
application on heroku so from that whole
blog you can take that part of how our
application is published on heroku
okay all right great
um and if anybody has any more questions
now is the time to ask
and i'm there on twitter so if there are
any further questions so i can take it
up there as well
that's right um has our twitter handle
in the
event description on meetup so that's
another way
all right so uh it looks like there are
no other
questions so i am going to
um thank you uh thank you
thanks for sharing the twitter handle
it's at mridu
underscore underscore yeah
great uh thank you so much for joining
us
um i know it's uh 10 30 p.m your time
now right
yeah i think yeah 10 15.
okay and we'll be sharing the recording
soon thanks for joining us everybody
yeah
thank you
