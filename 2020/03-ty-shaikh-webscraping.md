# Ty Shaikh: Scraping Poshmark Data with Python

## Key Links
- Meetup Event:  https://www.meetup.com/nyc-data-umbrella/events/270285046/
- Video:  https://youtu.be/0L1uM_18TTA
- GitHub repo:  https://github.com/ty-shaikh/scraping_poshmark_webinar
- Binder:  https://mybinder.org/v2/gh/ty-shaikh/scraping_poshmark_webinar/master?filepath=1-scraping_poshmark_listings.ipynb


## Transcript


everyone I am doing a recording of the
scraping presentation and the original
recording from the webinar didn't come
out well so this is just a recording in
today's presentation I'm going to talk
about web scraping we're going to look
at the website Poshmark comm and we're
going to use Python and some additional
packages to gather the data so agenda
I'm gonna give a quick introduction
about myself and the group then we're
going to talk about web scraping and
high level then we'll walk through a
code example I'm going to share the code
files so you can walk through it on your
own as well and then during the webinar
there was obviously QA it's a little bit
about me I'm a product manager with
General Assembly I used to run
operations at an online data science
bootcamp and that's kind of where I
picked up everything I know about Python
and programming and data science and
then I'm a assistant organizer with data
umbrella so a little bit more about data
umbrella the mission of the group is to
provide a welcoming and educational
space for underrepresented groups or you
are G's in the fields of data science
and machine learning and we primarily do
this through meet of events now virtual
webinars and open source sprints with
most of our events it's open to people
of all levels we we usually assume some
familiarity with Python or data signs
but we're happy to have beginners to
advanced people attend and then we're
always looking for volunteers and
speakers so you can check out our
homepage at data umbrella org and reach
out to us if you want to learn more
so what is web scraping I've pasted the
really technical dictionary definition
here which is the programmatic
extraction of unstructured data from
websites to usable structured data if
you have a technical background you
probably understand what this means but
for most people this is just a bit out
there so let's take a look at a
practical example on the Left we have a
screen shot of Amazon listings for TVs
and on the right is what our output
would look like from scraping so if you
take a look at each row which has an
item you see that there's there's tons
of usable information right we see the
brand Samsung the size of the TV the
type of TV resolution like 4k or 5k if
it's a smart TV or not then you can see
how many reviews were written what was
the average rating the price the
discount the original price the shipping
how many are in stock are there used
used or other seller selling so we can
see that all on the website but that's
not in a usable form unless you're you
know just using your eyes you can you
can read that you can digest that but
it's a we wanted to do extract the data
for like 10,000 TV listings right like I
could do this manually for five or ten
or a hundred and would be that bad but
if we wanted to repeat that process for
a thousand or 10,000 listings you'd want
to use web scraping and with web
scraping we can extract out the
individual values from this website and
extract out the brand the TV size
whether it's a smart TV or not what the
price is whether there's price prime
shipping or not and I'll do a little
assign and kind of explain how web pages
work here as well web pages are built
with HTML and CSS so this is the output
but there are two components so HTML is
really
the layout and the content so for
example in HTML you'll see a block that
says Samsung and this text and then
you'll see a block that has the price a
block that has the image and then what
CSS does is you add classes to different
HTML blocks and for example in CSS you
can tell it to make this image 200 by
200 pixels you can tell the web page to
print this out and smaller font and red
so that's what CSS does right make this
font Orange make this fawn bigger and
bold and so HTML gives it the layout so
we want text here we want the stars here
we want more text to the pricing here we
want the shipping text here we want the
stock pricing and then CSS tells you how
to style that so we want the shipping in
gray and smaller and then we want this
in red so that's that's how those work
and and we'll take a look at that in the
code notebook I thought I'd just give
you a a brief summary of that so how is
web scraping used in real life these are
just a couple use cases there's dozens
more so you can keep track of
competitors monitor consumer sentiment
so looking at reviews aggregate news and
other data like on Amazon lead
generation and CRM in Richmond so
finding out the background of people
that contact you gathering data for news
stories like 538 and the New York Times
The Washington Post
so what are we scraping today we're
going to be looking at posh Montcalm so
if you're not familiar with posh mark
you can think of it more as like a hip
eBay or Etsy it's basically a social
platform for clothing shoes and
accessories so you can buy and sell used
and new clothing items and it's become
incredibly popular with the with the
younger audience the millennial and
younger generation but I think I think
it's a cool platform I've actually used
it a couple times to buy some items I
like fashion so I thought it was cool
and there was the reason I was actually
interested in scraping Poshmark
is that compared to other social
commerce platforms they don't have like
a saved search feature so say you're
really interested in the example here
like you really want Clark boots in a
certain style and a certain size there's
actually no way I mean it's probably on
the roadmap I don't know why they
haven't built it but there's no way to
like save that search and get like a
daily digest or weekly digest at least
in the last month when I saw it so on
eBay or Etsy or really any other social
commerce platform you usually can save
your search and get like a daily digest
or a weekly digest like hey these were
the items posted in that and so I did
this scraping exercise in order to build
like a personal email reminder that
would send me updates like hey these
things were were posted under this
category or and good.this like these
parameters and I mean it's it's on the
road max map somewhere I mean dozens of
people have told them I've seen people
complain about it online and like read
another like public review and forums so
it's definitely there but that was kind
of my interest in scraping so I would
scrape a certain search and then send
myself an email reminder so to get
started you can just access this link
goes to my github repo and and I've
included this this binder blank it's a
cloud-based program which allows you to
run Jupiter notebooks and I've seen some
other people use it and essentially what
it does is it builds a docker image
under the hood
don't take a probably 20 or 30 seconds
to get running okay so I'm just gonna go
line by line and walk through my logic
and the decisions I made and then yeah
and that's pretty much the presentation
will comprise of the rest of the
notebook
to get started the first cell is really
just a way to set some custom settings
and ipython so I'm just expanding the
window and making the text bigger
webpages one on one the websites are
built using HTML and CSS HTML is a type
of markup language you can think of it
similar to markdown it provides the
layout for our websites and then CSS
provides the styling so when you have
different font sizes colors of text and
backgrounds spacing between elements and
you can see here we have a screenshot of
Poshmark but why don't we just take a
look at the actual website and this is
Poshmark com you aren't familiar it's
it's just a social commerce platform so
there are listings of diesel men's jeans
here and you can see all the images all
the prices all the text who the sellers
are and you'll notice on this website
there are a bunch of repeating tiles and
each tile kind of has some items inside
of it so if we take a look at the HTML
code you'll notice that there are a
bunch of blocks and they're all called
the same thing so although they're all
divs and they have a class tile call x
12 x l6 and so the tile is what we're
mostly concerned about the other classes
are basically showing how it would
appear in in kind of like a mobile view
so how many tiles would you have in a
row and so what we'll notice when we
take a look at this div is that each of
these tiles actually has the same
underlying code underneath it but to the
the actual text or image link is
different but the markup is the same so
we're going to use that with Python to
kind of extract out the data so if we
take a look under this tile there's a
card
and then we have a link block which is a
tag and so the link has a image
underneath it so if you if you click
that link it actually goes to e click
the link or the top half or the image it
goes to the individual page of the
listing so we'll go to this diesel jeans
listing and so that's just one block and
then you have another items detail block
which is denoted with the div and then
you have conditions and then you have
the price and the brand as well and
you'll notice that these each have these
weird sometimes named classes fw - bolin
and then here you have some better thing
a better named class which is tile
details pipe size and so these classes
are the same if we take a look at the
next tile and so that's that's what
we'll do if we take a look at for the
next tile you'll notice that the classes
are the same
and we're going to use that to extract
out the data so once we figure out how
to scrape and extract the data from one
tile we will repeat it on all the tiles
let's dive into the code
we're going to scrape down the denim
listing so the first thing we have to do
is use the request package we're going
to import get from that and we'll have
the URL and what we're gonna do is we're
gonna run get on that URL and it's gonna
return a response object the response
object has a status and a text and the
status is kind of like what happened did
you get the page or not and the text is
the actual raw HTML text and so we're
going to just print out a slice of the
first 500 characters now it's a large
string so don't print it all out because
it'll be hundreds and hundreds of lines
so you can see this is just kind of the
HTML page it has the has kind of the
title their diesel jeans for men
Poshmark and then of course all the rest
of them is there as well we're going to
use the package twelve beautifulsoup and
that is meant for parsing raw HTML and
what we do is we give it the HTML string
and then we feed it a parser and then it
will return a beautiful soup object and
we can run very specific methods on that
beautiful soup object
so there are several methods what we're
gonna do is we're actually gonna do is
to find all so if you notice when we go
back to the top and look at all the
tiles you'll notice that all the tiles
have a class tile and that's only for
these elements on the page do they have
that class tile so what we're gonna do
is we're gonna research and find all the
elements that have tile and that will
give us our clothing containers so on
the super object we run the method find
all and we give it the element so the
div element and then we give it the
class tile and remember you have to have
class underscore equals and that's
because class is of course a protected
keyword in Python so you can never have
you can never just type in class without
actually defining a class and here we go
we get a result set which is just a type
of beautifulsoup object and then just
like a combination of several beautiful
sleep objects and then we have the lens
which is 48 which makes sense because we
get 48 listings when the page loads
so we can take a look at the first aisle
because it's just a result set which is
similar to a list we can extract out the
first element and then print it now
unless you're familiar with web
development this is gonna look like a
lot of gibberish it's very hard to read
and see what's going on what we can do
is we can actually run prettify on that
text and what that will do is actually
indent everything properly so we can
read it better but still it's very hard
to read you you all must notice some of
the blocks kind of breaking out you have
like the top link block which has the
image in it then you have like the item
details which has the title and and so
forth
so now all we want to do is extract out
the individual values
in order to extract out the values what
we need to do is find each element that
we want that has have either the title
or the price of the brand and then and
then extract out the text so what we're
going to do is we're going to take our
tile and we're gonna do find the a tag
the link tag that has a class tile title
so we have one H egg at the beginning
that has kind of the link to the
individual page and the image and so
that's useful we definitely want that so
for example it takes you to the page
but we're really interested in the tile
title so that is actually the second a
tag within item details
it's an item details and a title
condition container and then here we
have this the a tag and has the tile
title and so when we find that element
do we see here again this has the link
to the individual and the title and so
what we want to do is we find that a tag
and then we want that the one
specifically that has the class tile
title if we look for other eight tags
we're getting other HTML elements
so when we print it out we get this
whole block of text and
this is you know this is what we wanted
but we really want some specific
information from there so it has the the
link to the individual page but really
what we want is the the title and so
what we can do is we can run we can run
this method on that object so what we do
what we would want to do is just run the
same code and then and then just modify
it so what we're gonna do is beautiful
soup has this method called get text
it's it's just built-in and what it does
is it just gets the underlying text in
between the a tag opening which is that
whole part that's the the you know HTML
tags I usually open and close some are
self closing but the majority open and
closed so we have a and then we have in
the middle of the text and then the
o'clock closing with the backslash so
what this does is when we do get text we
we get the text in between a tag
and so when we print it out we get the
text now we don't have any of the extra
HTML we just get that you'll notice it
looks a bit weird we have all this space
there's like a new line and there's all
this white space and really that that
happens when HTML pages and elements are
dynamically generated so you can see
even the space appears in the in the
code right there and so what we can do
is we can we can actually pass a
parameter strip equals true and that's
gonna strip all the whitespace and then
we really just repeat the same logic on
the other elements so we can find the
span with the class fw - - bold which
corresponds to the span that stores the
the price
actually funny story I made this
tutorial two weeks ago and then just
checked it the night before and this
class had actually changed and I had to
fix it and changed his name and I had to
fix it to make sure the code was working
before I recorded this
so just notice I'm just kind of
highlighting with HTML that it has it
has it like a tree structure and so
sometimes if you don't have like
well-defined classes or they're they're
just gibberish what you can do is you
can actually just try to find like a
parent element or a top-level element
and then you can find children and
sibling elements and kind of traverse
the tree that's what they call it so
here we're just gonna find the span
again with the class fw - - bowles and
that's going to get our span element and
if we just do the same logic get text a
strip equals true we get out the price
and then we can do the same thing for
size we can get the a tag with the class
tile details pipe size
and then we get size 36 and we can do
the same thing with brand and we get
diesel the the last two will be a little
different we're going to be looking at
the link and so with link we can we can
just grab the link with a glass tile
title but then what we're gonna do is we
actually want to get one of its
attributes and so if you remember this
big block of code with the a tag it has
a bunch of attributes so it has the href
attribute and all these other ones and
href is basically stands for a link so a
reference and so that is they reference
to the individual product page and so
that's the attribute we want to get to
the value for you could almost think of
it like a dictionary is a bunch of key
value pairs right key is the href the
value is that string
and so if we just get the href you can
see we get this string value and you can
even get the class or any other other
kind of attribute the one problem with
this string value is that it's it's not
complete right it's it's the trailing
strength it's the trailing URL after you
have Poshmark com so we'd actually want
to do this just add wwhy calm before
that to get the actual working link and
then we can really just do the same
thing with the image we want to get the
image URL in case you want to store the
image later so we can get we can find to
the image there's only one image tag a
nested under there and then we want to
get this source attribute and so we can
get the value for that
the next step we want to do is we can
just kind of print out a summary of our
data the problem is that when you scrape
information from a website everything is
a string value so all these are strings
and and what we really want to do is we
want to convert the price to just an int
and then the same with a size right we
just want to say area we have a the
price is 55 because we will know it's in
dollars and then the size is 36 and and
we'll kind of just know that's 36 waist
size inches for men's like men's jeans
because we're looking at men's jeans
so we're gonna take the first price
variable and then we're just going to
use a basic string manipulation to
replace out the unwanted characters you
can use something more complicated like
regular expressions but I think since
our use case is very simple it makes
sense just to use a string to replace
and so what we're gonna do is we replace
the dollar sign with a empty string so
essentially we will delete the dollar
sign and so now we get 55 but it's still
of type string so what we want to do is
wrap it into a int type conversion so if
you do that you will actually get to
integer 55 and the reason you can't just
do that
you can't just into first prices because
it's unable to kind of convert the
string like the dollars the dollar sign
string that makes it the cause of some
issues now we can do the same exact
thing with size we'll just replace the
size colon space with an empty space so
essentially deleting it and then we can
print out the type and the value
now one thing you'll notice with the
image link is that you can actually see
the posted date so this product was
posted on 20/20 May 10th and we can do
is we actually can extract that and find
out how long an item has been listed so
we could we could kind of subtract out
the difference between the posted date
and today's date so here we can we can
kind of find the value 20/20 and what
that really does is it fine this is a
string so we can we can do string
indexing so we'll find the index value
so when does when does that start so it
starts at the 43rd character and then
our 44th if you're indexing from zero
and then all the dates are the same
right it's it's ten characters long you
have you have the year you have the
month and you have the day and then the
slash is in between and so you can
technophile the beginning and end and
just extract that out because you know
all the date strings will be the same
for all the image lengths and so you
just do a string slice and just extract
out that substring
and then we're going to bring in that
date you tell parser package now this is
is gonna do some magic underneath but
essentially you can parse a bunch of
different string dates and then return a
Python date object so we really just
just really import parse and then and
then just feed it and then it finds out
that what the date is and if you want to
find the difference between days you can
actually use a day time to find out
today's date or right now as date and
then it will find the exact day and in
seconds and then we can kind of subtract
out the difference between the days and
and take the absolute value of the
number of days and we get one and so
you're always going to get a positive
number because we did the absolute value
but also because you kind of have
seconds and minutes that happen
difference and then again if you're
doing this in a professional work show
workflow you'll have to make sure you
have like the time zones and everything
but but normally what you'll do is
you'll scrape the raw data store the raw
data and kind of a flat file like CSV or
JSON then you will type format the data
and then you will extract out new
features so you'll want to kind of silo
each process so you can create different
versions of the data
and then we'll just take a few minute
break the next part of the notebook is
really showing how to refactor code and
and create functions and so the code
before was just really procedural code
kind of a string string code what you
would call just kind of writin what
comes up and then just trying to put it
all together and make sure it works but
what you want to do is really create
functions and module has it and so here
are some good guidelines just like
sensible names single responsibility
includes a doc string returns a value
and it's not longer than 50 lines and I
don't really follow this exactly in the
functions I've created but just to give
you an example of what some better
better organized code would look like
and just kind of each function is
responsible for one thing you know
extracting the title extracting the
price extracting the brand and so forth
and normally you probably wouldn't have
two things for example like in this
price function I am getting the price
and then I'm type converting and
formatting it you'd you'd actually
separate that into two functions so you
can kind of have a single responsibility
but that's more just kind of you know
just some software engineering tips and
then here I have another function called
combined data and what this does is it
has a bunch of try and accept blocks and
then it returns an object with all the
values but with web scraping sometimes
there is no values on the webpage right
like a title could be missing a size
could be missing it might not have a
size it could be like unisex sizing or
whatever and that's why we have to have
try and accept blah except blocks
because we need to return an empty
string or empty value in a case it
doesn't find anything because we don't
want our code just to break and crash in
the middle of a loop and so that's why
it looks really ugly but but that's just
what we need to do in order to ensure
that ensure that the code runs and
doesn't kind of break several times
and so once we have those values you
know title or price size brand and all
those values from the tile you know
basically take a tile and then we we
insert that in there and then run all
these kind of nested functions we just
returned in this object just a
dictionary key value pairs of the
private all the values and so let's
let's try to extract out all the tiles
on an initial page we're going to
download the page we're going to create
a beautiful super object we're going to
extract out all the tiles and then I and
then I have kind of this list
comprehension which is really just an
easy way to do a for loop while
appending to a list I can you can kind
of just like break out what that looks
like in case you're not familiar so if
we have all the tiles we have a list of
all the HTML tiles this is what a all
this comprehension will look like next
basically we want to run a function on
every single tile and return a
dictionary of the values what we do is
for each tile in item tiles we would run
the function combined data on the tile
and we would assign that to a variable
it can be it could be anything and then
what we would want to do is we'd have
some like item objects and we depend
that so you'd also have to create that
item objects it would be an empty string
and really what a list comprehension
does is just this is just a very common
procedure that you have to do in Python
encoding and so it just tracks that to
one line and this is not something you
can do in every language it's it's
something that only exists in Python a
couple of other languages so but it's
just a nifty trick all right so we have
48 tiles that means if we run this we
should have 48 item objects and then if
we print we can take a look at each one
so it's a bit hard to read so you can
bring in the package P print or pretty
print and
it looks better
kind of the same as prettify just gives
you the indentation and spacing
oh yeah so one thing to notice is you're
only get 48 items because you'll notice
here as I'm scrolling it adds more items
to the page using JavaScript
um but we can only get 48 because we're
doing a programmatic request and if you
really want to get all the paid items
that load you you really have to use
another package that that lets you use
headless browsers and what that does is
it creates like a ghost instance of
Firefox or Chrome and actually browses
the page and then downloads the the HTML
and so in the git repo that I've linked
there is an advanced notebook that kind
of shows you how to use it in advance a
headless browser it it kind of requires
a bit of configuration so it might not
be easy but it might not be easy to run
it on your local computer
all right so why don't we look at a
bunch of brands let's extract out a
bunch of other men's denim brands and
really what we can do is we can just run
that same block of code just looping
through a list of brands and so if I
penned this to this like master store
what we're gonna get is the store is
gonna be aligned thefor because we have
four brands and then each item within
the store is gonna have 48 item objects
so it's really gonna be a list of lists
right for and then each for as 48 and we
don't really want that because we really
just want 4 times 48 right like 196 or
yes or maybe a hundred ninety-two sorry
about Malthus my math is off but what we
really want to do is just extend how the
lists and and so instead of append we do
extend and that will just add and add
and add to the same master list so I
think oh yeah 192 right ok there we go
and then we'll have a length of the
first item as 8 and that's really just
an 8 8 key value pairs from the object
so just gonna run through this last
section really quickly if you if you're
familiar with pandas or not pandas is
kind of like microcell for Python if you
will it allows you to manipulate and
organize data in tabular form and so we
can kind of create a new column with the
length of the title we can look at a
preview of the data we can kind of take
a subset of numeric data I'm just kind
of like the price size difference length
so then we can the reason why I just
want the numeric data so I can I can do
some kind of analysis on that by just
looking at like the mean and the
outliers and so forth
so you'll notice the kind of difference
the differences is the days right we
have some that were listen for two days
and some that were listed for like a
couple years and so I guess something
was just not popular too expensive or
even if you're actually a Poshmark user
you'll know this
some people just kind of check out right
they they kind of list a product and
then and then they they don't ever check
their account
so you notice some brands are listed the
at median is longer and the price is
obviously different for different brands
you can bring in matplotlib to visualize
some of these things like the kind of
distribution of prices and you'll notice
it's more pronounced with the individual
brands but you kind of have like two
peaks you have like one center around 20
30 40 and then one at the end and so
really what that is is again this is
like another kind of data science domain
expertise or if you use Poshmark people
can list new and used objects or items
so for each brand you'll see two
groupings and one grouping is the used
items and the other grouping is like
completely like totally new items or
slightly slightly used or like new
without tagged this type of thing and so
so something definitely if we were to
redo this analysis is we definitely want
to extract out whether yes you see kind
of like the separate Peaks or separate
groupings and so one thing you want to
do is extract out new and used items I
could have kind of like a boolean value
and then in another column
and we can also look at just like the
difference the days listed as well as a
whole and then and then kind of by brand
and you'll see some we can you can kind
of look at which brand has the longest
one so it looks like naked famous takes
the cake it's it's more of a niche brand
Basso tarik so uh yeah I make sense that
some items were just like a little out
there
so there's obviously more analysis you
can do I kind of did a very rudimentary
exploratory data analysis but it was it
was useful you know this just don't land
up the titles which doesn't really show
anything so feel free to this was like a
live webinar so there's questions but
there's a feedback form in the notebook
and and you know you can send me a
message on meetup if you have any
questions or concerns or just anything
about scraping I'm not like a
professional I just kind of do it as a
hobby so I might not be able to answer
all your questions but I'll try my best
and stay tuned for more events from dat
umbrella and pilotis in the future
