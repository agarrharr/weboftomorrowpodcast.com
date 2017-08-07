---
layout: post
title: "39: Gatsby - Kyle Mathews"
summary: "Kyle Mathews is the creator of Gatsby, a blazing fast React static site generator. He talks about why he made Gatsby, why it's so fast, and why you should use it."
link: https://s3.amazonaws.com/weboftomorrow/2017-08-07-39.mp3
size: 44548581
length: '00:48:15'
permalink: /39
---

## Show Notes

- [Gatsby Website](https://www.gatsbyjs.org/)
- [Gatsby Github](https://github.com/gatsbyjs/gatsby)
- [Plugins wishlist (and example sites)](https://github.com/gatsbyjs/gatsby/issues/1199)

<article class="Transcript">
<h2>Transcript</h2>
<dl>
<dt>Adam Garrett-Harris</dt>
<dd>Alright, welcome to Web of Tomorrow. I'm Adam Garret-Harris and today we're talking with Kyle Matthews and creator of Gatsbyjs</dd>

<dt>Kyle Mathews</dt>
<dd>Hey everyone!</dd>


<dt>Adam</dt>
<dd>So what is Gatsby?</dd>

<dt>Kyle</dt>
<dd>Gatsby is a blazing fast React static site generator and it aims to give you a really nice out-of-the-box experience where everything is set up for you: React, Webpack, different CSS options, modern JavaScript etc. And you can build really fast sites without a lot of effort on your part.</dd>

<dt>Adam</dt>
<dd>Cool. So, how did you get the idea for Gatsby?</dd>

<dt>Kyle</dt>
<dd>Basically, so I started using React pretty early so it was open source like mid 2013 and it got on my radar then and I was working at a job in in San Francisco, a startup, building JavaScript web applications with Backbone and I really liked in a lot of ways, but it had a lot of weird sharp edges / missing things and React just came along I was like "This is so beautiful, the component model." Because I mean components is an old idea. React didn't invent the idea of components. I mean backbone components existed but they were kind of just missing a lot of stuff. Anyway, so React component was just like so beautiful.</dd>
<dd>And so anyway, I start following that and I quit that job like early 2014 and just started doing a bunch of stuff with React was like this is the future that's what I want to learn and do everything with and then kind of mid ish 2014 a friend and I we started working on startup. So I worked on that for a while and it was building our web application with react of course and then early 2015 it was kind of getting to a point we were like "Ok, we kind of know what we're doing. We have the application sort of working like start to go public pretty soon and of course need website and I was like "Okay, I haven't build like a website website in a while. How do people do that these days?" And I was looking around I was like "Oh man. I hate all these things you know because I'd use like Drupal and WordPress and built my own little static site generator in the past. I was like "These are all terrible. I want to use React components and Webpack and all these other really nice modern tools. There was other people thinking about the same thing at the time and I just thought about it a bunch and I figured out a clever way to pull all those together. And so that was the first version of Gatsby that I built just for my startup's website.</dd>
<dd>And then I open source that and then a lot of other people got interested and it just kind of snowballed from there</dd>
<dt>Adam</dt>
<dd>Cool, so what what is the tech behind Gatsby? You mentioned React. What else?</dd>
<dt>Kyle</dt>
<dd>So, the goal of Gatsby is to use industry standard stuff with the idea being that if you're a React web application developer you can install and use Gatsby and it feels completely natural. That's what I wanted. I mean, I'd already learned Webpack, and React, how to use those two together, and loaders and so forth for the applications I had been building. So that's what I wanted from Gatsby. So, it uses React and then Webpack for module bundling, and then normal standard loaders and so forth. So if you build a React, Webpack, Babel web app then using Gatsby should feel pretty you know</dd>
<dt>Adam</dt>
<dd>And then, it also has Redux and graphQL, right? </dd>
<dt>Kyle</dt>
<dd>Yeah so the latest version of Gatsby, it adds Redux but that's just for managing internal state. While using Gatsby you shouldn't see Redux at all. And yeah, graphQL is also new addition to the new major version of Gatsby that was released recently and graphQL is used very much like Relay or Apollo, those those kind of clients for building stuff on the web. It works pretty similar that on React page components in Gatsby you can have a query which says, for this page, for this blog index page, or for this product overview page, here's the query it describes the data that is needed for that page. And then Gatsby makes sure while you're developing and in production that when that page gets rendered that data that you query for is there.</dd>
<dt>Adam</dt>
<dd>Cool. Alright. So, who who is Gatsby for? Who you want to be using this. What kind of stuff can you build with Gatsby?</dd>
<dt>Kyle</dt>
<dd>Yeah so, the first version of Gatsby is kind of intended for. Basically my mindset was: hey React developers who also want to build websites. So you want to have a static render of everything. You have your different React pages and you can throw in some markdown as well. And you just want to have a static render of that so that it loads faster. That was kind of the the main use case that I had in mind for the first version of Gatsby, but Gatsby v1 is much more ambitious, the latest version, in that it adds the ability to pull data from remote api's and this is really important because most websites in the world are powered by content management systems and the reason for that is it's not just one or two developers who are cranking out the site. There's lots of course, but the vast majority websites in the world are big complex operations with dozens or even hundreds of people who all have their hands on all sorts of different pieces of it and they need specialized tools for managing the content, which we know is content management systems. And so for any website building tool to actually make it outside of the little niche of programmers you need the ability to integrate with content management systems and so that's one of the major focuses of Gatsby v1, to be able to do that. Which has already paid of because I've seen there's number of agencies that are working on Gatsby WordPress sites where they're using WordPress as a CMS and then building the actual site in Gatsby. So they get the advantage of modern JavaScript and CSS and the React component model, but they still have the familiar WordPress ecosystem to set up you know the actual content editing experience for their clients. And they've been really happy with that.  There's also a lot of new startups offering CMS's that are headless basically, where all they are is the content editing part and an API. WordPress is that piece plus everything around actually building and running the website and those work really well with Gatsby because they just they concentrate on having a really nice interface for creating editing content and then Gatsby has a really nice tool set for building really fast websites</dd>
<dd>Yeah so anyway, to your question, the audience is pretty much anyone building any sort of website</dd>
<dt>Adam</dt>
<dd>Especially if you want to be fast</dd>
<dt>Kyle</dt>
<dd>Yeah, especially if you want it to be fast, which is pretty much everyone.</dd>
Yeah, it's also an interesting fit for kind of like hybrid website web apps. There's several startups that are
<dd>building everything basically on Gatsby. So they have their marketing site, which is static but then Gatsby v1 also has the ability to have client only sections of the site, which then just a traditional web app that loads up and hits an API and then does it's thing from there.</dd>
<dt>Adam</dt>
<dd>Yeah, because you're just building it in React</dd>
<dd>Yeah, and then it's just all React and so it just works.</dd>
<dt>Adam</dt>
That's cool because I've seen companies in the past build their marketing site with Jekyll but they
<dd>clearly couldn't make their their app with Jekyll.</dd>
<dt>Kyle</dt>
<dd>Exactly, and there's a ton of inefficiencies through that model because you have different programming languages, you have different models of thinking about things, you have different build steps, you have the problem of merging styles back and forth, and this that and the other thing.</dd>
<dd>If everything's in Gatsby you can reuse the same layout components and other components across the whole site. It's the same styles, it's the same way of thinking about the world, so there's no friction because in a lot of companies the marketing site is like the redheaded stepchild. Where marketing people are always begging for engineer time like "Hey somebody come work on our site" and they don't want you because it's this big abrupt shift to "How's the stupid thing work again?" But if everything is the same everything kind of moves alone together. It's a much cleaner more efficient model</dd>
<dt>Adam</dt>
<dd>Okay, so why is Gatsby so fast.</dd>
<dt>Kyle</dt>
<dd>Great question. There's a few ways to answer that. First is, Gatsby as a static site generator inherits all the speed advantages of static sites, which is basically... If you think about how a website gets loaded. It's like person A is somewhere in the world and they type in the browser a site. There's DNS resolution and then there's a little HTTP request that sends on the packet over the Internet and it gets routed to a server somewhere which then does some work and then sends back data. And then that comes to the browser and gets all assembled in the browser pulls it all together and renders pixels on the screen, which then we see as the website.</dd>
<dd>So why static sites in general are fast is because they A) avoid doing any work on the server. So if you have a site that runs code for each response, there's a cost from running the code and especially if there's database queries that has to be run before data could be sent back to the client.</dd>
<dd>So static sites avoids that because a request comes in and then you just load files off the disk and send it back, which is like super-duper fast compared to running queries and running code and that sort of thing</dd>
<dt>Adam</dt>
<dd>Yeah so I thought Jekyll was super fast because it's static, but then Gatsby takes us to another level.</dd>
<dt>Kyle</dt>
<dd>Yeah, so Gatsby gets a lot from that, but Gatsby also it tries to bake in... So it does several things. First it tries to enforce everyone using all the best performance techniques. So one example is by default Gatsby inlines CSS in the head so you're not making... Most sites you have an HTTP request and that loads in and then it does another request for CSS and JavaScript and so forth, but it's actually much faster if you inline CSS into the head of the HTML, and Gatsby does some nice tricks to make that really easy to do. And so that saves oftentimes like 3-750 milliseconds on the initial paint time. So that's something that most people don't even know about definitely aren't doing that Gatsby just does for you.</dd>
<dd>So, there's a few of the tricks like that, that Gatsby does, but the other big thing is that Gatsby is kind of a universal JavaScript, so it can render your site at build time to HTML, but it can also render in the client. So once Gatsby loads, all subsequent pages are rendered in the client and not on the server and so that means that there's no latency at all when clicking on different pages. Gatsby just prefetches all the data and code needed for each new page so when you click on it that there's no request to the Internet at that point. It's just assembling the new page in your browser and then boom there it is.</dd>
<dd>And so frequently that's like 30-50 milliseconds versus if you have to go back to the Internet to get stuff for the new page you're looking at at least like 100, but often times especially on mobile like 500-1000 milliseconds.</dd>
<dt>Adam</dt>
<dd>Don't you have another project that helps make websites faster with web fonts?</dd>
<dt>Kyle</dt>
uh yeah
that's the typefaces yeah the basic idea
is that you know self hosting your fonts
is faster almost always then like google
fonts yeah I had no idea I thought yeah
it's just getting it from somewhere so
well yeah why is it why is it slower
from Google so the reason is is that
like what google fonts gives you is a
CSS file so so what units when you add
google fonts to a site it adds basically
a CSS file that Google hosts and so you
first have to make a request to get that
CSS file and then in that CSS file
there's like then links to the actual
font files for whatever font that you
want to add to your site and so google
fonts is like always like to request
before you start you know before you
have the funds and then when you self
host and was like in lining it it's like
the request to anyway there's no
additional request I guess it's just
like it's like you load the foot you
love you love the page and then you like
there's the links right already there to
the font files yeah so just avoid this
extra request so you mentioned you you
get data from external API hmm and and
then you are going to generate static
sites locally instead of
server and pre shut those static files
what happens when that data changes from
the time you build it to the time a user
visits the site do they get the old data
and then it is like flickers for a
second get some new data so no so Gatsby
I mean is a static site generator so
it's like you're kind of like outputting
like you know static bundles like the
whole site you know is just like HTML
and java javascript and json on sort of
things so basically you need to rebuild
the site every time there's a change and
so whatever so basically you can think
of as like versions of the site so if
user a loads version you know 273 then
they'll be like navigating within
version 273 and if there's like a change
to like content or to code or whatever
like version 274 is out okay then they
won't see that until they like reload
the same okay hey so so if you built
gatsby site and then someone makes
change on the CMS maybe reason WordPress
and CMS site will not be updated and
yellow until you build Gatsby again yeah
exactly have people come up with a way
to automate that yeah that's actually
yeah so a lot of people are doing that
basically you just need to have like a
build server of some sort and there's a
few sources that do that like net with
Phi and then you have like a you know a
web hook from your CMS that then just
triggers a rebuild on your build server
and so yeah so it's it's it's fairly
straightforward to do I know some people
also do like a cron job there's another
option if you're you know that doesn't
change that often okay in a current job
we just run a certain interval like
every night or something yeah something
like that but but generally speaking
like a left hook works really well and
yeah fairly straight for setup most most
CMS's is especially like the the API 18
messes then they're already like set up
to do this out of the box yeah you
probably get an email if something
didn't build right yeah exactly yeah
yeah awesome so one question I'm really
interested in is that a year ago you
announced your work and Gatsby full time
and so how do you make money if you
don't mind now that's a great question
ah because I think it seems like you're
kind of like living the dream yeah and
just like I'm just going to quit my job
and diss open-source project yeah so um
basically I've been basically it's it's
been a few different sources there's
been a number of companies who've been
you know who are really interested in
the plan for one point out and have
either directly sponsored it or pay me
to work on projects using the kind of
work in progress 1.0 code and that's
been the majority of funding and yeah so
that's been what I've been doing so far
but anyways the tricky thing our open
source is that you know you really need
I for an open source project to really
take off you really need at a minimum of
like hundreds of thousands of dollars
investment you know you get some of that
of course like you have like if you have
lots of people using it and lots of
people so many PRS like they're
individually it's like if you think
about the time value of about these
different PRS that people are
contributing like each PR is like
minimal like hundreds of dollars
investment and some like you know mid to
major type PRS like they could easily be
like thousands of dollars of you know
time that these you know really talented
engineers are condemning to the open
source project so there's definitely
like awesome investment so how much
learning is involved with guess T to get
go keep going with gatsby say so you
don't know react yeah is reacting need
to know or what what else um yeah you
definitely you definitely have to have a
probably
even like a fairly beginner level of
understanding Adriana should be
sufficient because most most of the time
you're just using like reactive
components and you really can use just
like the the function you know great
combo eternal step so like basic
understanding of gesture basic
understanding three attics some
understanding of what PAC is is helpful
especially if you want to do like more
complicated things and then path that
it's really how far you want to go in
different directions okay how much is it
Gatsby API do you need to know and again
it depends like if it's a pretty simple
site like person at all you know you
just like you know start using guy C and
then you have two plugins and then you
just write react components and then
build it and off you go but if you want
to like start writing like custom
plugins in that of course you can have
to dive into the api's CS so it is the
goal is that the plug-in the plug-in
system is like robust enough but as time
goes on more and more use cases will be
solved by just aligned with it yeah I
was looking through the posts on the
Gatsby blog about how to how to get
started and make you know making a
Gatsby blog and a lot of it is just in
spawn gaspy plugins yeah but it still
seems fairly intensive as far as install
all of these and then here's all this
boilerplate code yeah to wire it all up
yeah yeah yeah and that's and so I
actually have a plug-in in mind that
will remove most of that photo book
light
okay so yeah so it in and that's
testicle I just uh you know with like
all the work just in gets you out period
I left it kind of global flaky but the
idea is that any any boilerplate can be
subsumed within uploading yes this kind
of any is also kind of cool because even
though it is boilerplate it's it it
describes exactly what your site is
doing and you can change it yeah exactly
it's not it's not super opinionated it
doesn't say how you have to name your
files or where you put files or how
things go or what a post is or what a
pages you know you can get ever yeah so
I think I think the right because like
there's always like there's just
trade-off between you know like you have
use cases and i/o will build around
those use cases and then those use cases
are very easy to to accomplish but then
oh I'm going to step outside of those
kind of like you know blessed blessed
path then all of a sudden like life is
hard yeah and a lot of systems kind of
end up in that that kind of that trap I
guess call truck and then I got the
other one does have a Gatsby so what I
think like the best patterns that you
have pretty low level primitives that
you say like these are like you know
these like basic things are what
constitutes you know it is what the
system supports and then you add kind of
like scaffolding tooling at that then
you can build up abstractions on top of
you can build up arbitrary abstractions
on top of those little roller coasters
it's like you think like a programming
language like programming is your
awesome there are a completely designer
out that's like they give you like
different data types like with your
strings yeah hints you have you know
your clips and you have like functions
and whatever and then using it like blue
like pretty low level stuff you can then
build up you know any sort of
abstraction on top of that yeah and
we're you know so cool well so you can
think of like Gatsby is like kind of an
that same sort of thing where Gatsby's
like hey you have pages you have layouts
you know you have data of various sorts
you have like queries you know that you
can like clear your data and pull that
into you know your components and then
using these like kind of like
site-specific primitives then you can
like build up abstractions on top of
that cool so you said you can pull data
from PPIs but you can also just have
local data and then you got your pages
and posts so how describe queries how do
you get how do you use that data and so
interesting thing about like the local
stuff is that in the Gatsby world like
data coming from like your local file
system is treated exactly the same as
data coming from remote API school my
first guys concerned is just data that
just arrives from somewhere so they took
a key that system is basically there's
source plugins and then there's
transformer plugins and so source
plugins their responsibility is like
somewhere out there in the world there's
data and it pulls it in somehow and it's
up to the source plug-in how it does
that because use carrier business or
probably doesn't but probably uses like
JavaScript you know NPM libraries or
something or you know API calls to get
stuff and so in the case of like a file
system we you know the source file
system plug-in you just tell it what
directory to look at and then it goes
through that you know director and
cursive Lee finds all the files and then
adds those as like as files file it was
as those of notes like which is no
telling like the basic gatsby data type
into Gatsby and then it was usable but
like a remote source plugin it was just
hit an API and then pull into that from
there and then somehow turn that into
again notes which then go into Gatsby
and then transform plugins how they work
is that source plugins can say so sort
of like and say hey like I know how to
handle my my I know how to completely
handle my data
so I'm just going to add them as like
you know the dad was already kind of
like decompose into like fields so
there's no more can I be composed
decomposition that can happens like like
there's a title field and there's like a
field and there's any other thing it's
already kind of like in its final state
but there's often times where you have
like data that you know like the source
plugins like well I don't really know
exactly what the end user wants to do
with this and so I'm going to have to
leave it and kind of like like
unconverted form a kind of like like raw
source form that then can be converted
per the needs of an individual site so
markdown is like a really obvious
example of this because it's like pretty
common and so so a source plug-in say
hey I have this note and it's marked
down and I'm not going to do anything
with it it's just like but here's my
time for this note is like has is like
raw content that's markdown that a
transformer plug-in can come long and
say hey I know how to transform markdown
into something else
which of course typically is you know
HTML so there's I thin like transformer
plugins that take this raw content
markdown and then turn it into HTML and
so it basically says choose them here's
here's a note that's a type you know
markdown and I'm going to transform it
into a new note that's a type HTML okay
and so this can be this sort of like
transformations can happen from any one
data type to another data type so like
there's like a CSE transformer which
takes like a CSV file and turns it into
like you know each each row is now a new
note you know same thing like JSON you
know Gamal there's like image
transformer plugins with key K an image
and then can turn it into like you know
resize the image and yeah you know turn
down the grayscale you know can do
basically anything that you want and is
it all done with JavaScript uh not
necessarily it can be done with
JavaScript and for the image case
there's a this
NPM packets called sharp which has which
kind of like anyways it uses another
like really kind of like older image
magic or something it's not using its
lid bips or something like well anyways
it's like super fast and it's like
really it's pretty easy to install and
press you know pop one so yeah it does
it has a lot of the image
transformations but you could you could
totally write within this magic v1
anyways yeah so it's like so you have
source nodes and the transform nodes
like take you know data and turn into
other sorts of data anyways and it's all
eventually kind of like this is kind of
like chain and transformation so it's
just kind of like automatically happens
using all the plugins that you install
and then out of that comes then a
graphical schema which is like you know
all the different types of data you have
and all the fields that you have because
turn to this this is schema and so it's
kind of like it's kind of one way of
thinking about is like you know you're
basically constructing on the fly a
database yeah we have all your data and
like all the transformations of the data
and then you then how like a database
schema which in this case is very
powerful well and then kind of like you
know old-school like PC or something
like that then like when you're creating
pages then you can just write queries
directly against you know your database
to like pulling the data that you want
and yeah so graph tools like a really
nice query language for that because I
would just pull it into parts you need
yeah yeah yeah yeah so if you're like oh
I need a list of all the authors mm-hm
you do it
yeah tags for yeah for the pages tags
that are within those pages or pages
there with it within this tax yeah some
stuff that can be really hard with
aesthetics I generated yeah exactly I
just come up with an idea of what you
want to query for and then you got it
yeah yeah cuz that look like yeah that
was one of the big motivations for this
new data layer and no graphical system
is that yeah I static
generators are really nice for simple
types because like it's very simple it's
just like oh you like you have done and
you like put free templates and outcomes
pages and you're assuming the kind of
data that you want yeah yes
they let you put some custom work done
and stuff but creating it's not that
easy
yeah but yeah it's kind of like you kind
of like the idea of like jumping across
lots of different files or the logic and
data source and seeing it look we're
like all authors or you know oh hey all
posts created by out there or all posts
we're attack shows up Unitas or stuff
that gets like weird to do in static
site
Trisha sighs degeneration generators and
so the graphical wall and stuff makes it
better really true be able to do and it
also makes it trivial to do all sorts of
like complex data transformations that
are like just powered by plugins and a
performant cache and so forth so what
are there other types of plugins besides
be what you call it source yeah so I
just said source and transform yeah so
so there's plugging with that or for the
data layer so those are the source and
transformer plugins
those are responsible for like patching
data and then transforming data in
different ways so those are both plugins
but then there's also plugins for kind
of two other categories that guess would
be like wet pack related plugins so you
know if you want to set up like you know
if you want to use less for example
there's a web pack world you know
there's a left loader that you use to
then like add support for you know
transformer for for kind of like what
that going to loading less files and
like doing different stuff to it and so
there's actually not a gap you what's
buggin yet but some news that's a good
example to similar than that maybe I
just got the SAP plugin okay we're still
is all set up for using sass in your
site and then there's also another
category plugins for like collect
solving the Shalini
yes in a website so for example like
adding Google Analytics hmm
you know there's just gastric bookends
latitude you know like at the end of
your body and all the kind of normal
stuff all you have to do is they okay
here's my you know here's the shiny ID
and then you know it happens and it was
like an offline plugin you know which
generates you know a serviceworker
automatically it's like set up for your
site so you add that house in your
sacred stuff like so if this was a whole
bunch to will look very long list of
random you know stuff like that
that bookings can handle it cool so so
when you just said admit gatsby how how
hard was it
and how did you figure it out and do you
think you would be able to do it yeah
yeah ah there's definitely a many
moments where i sadly that's just like
yeah this is it's just I don't know neat
whenever you do like something novel
it's like we don't know you're getting
yourself into
and so it's book like it feels hard like
both like the end nouns just you can you
don't know how long the pathways are
what you're going to count it all the
way and so there's a lot of you know
fears associated what kind of like that
um know that to add their own s of the
path you know it's like I'm going to
have to have resources to get through
like what is it actually solvable you
know like I haven't I when I started gap
speed you know the next next major
version gaps we had a pretty good idea
of what I wanted to do what is like is
it actually doable you know like all
these things that I want to make happen
um yeah I think for me I wouldn't I
wouldn't think is it doable but can't I
do it yeah no yeah it's like I don't
know I mean I kind of I don't know I
kind of very much uh you know I think
most people are people doing
they think they can it's just letting
yourself I'll leave that and then
they're putting in the time
yeah to get there and there's definitely
I had to learn a ton of stuff to do
gah yeah there's a lot of a lot of kind
of like Co techniques I hadn't used
before getting the necessarily know
existed but I I got the thing is it's
like you can overcome your fear of the
unknown and just kind of like plunge in
it's like it's kind of like you dive in
and then I mean you can't see that app
that you're going to take necessarily
but like once you get there either you
can like cut your way through or you can
let go ran upsala back and that's what I
it was a lot of meta forcing user but
basically it's like advice you like
allow yourself the time to learn things
you know you can do a lot more than you
think you can it's like if other people
you know people who do stuff that you
haven't done it isn't because they're
like smarter than us it's because you
know for whatever reason they've had the
opportunity to learn you learn the
skills and knowledge necessary to do
those things and so if you allow
yourself the time to learn those skills
and those and you knows a lot you can do
cool so when you started this did you
have a full-time job and you're sitting
on side and now so we talked earlier
about a about the startup so I built the
first version Gatsby just to build that
website basically and so I started
working on the next major version that
gets you go which is released a few
weeks ago when I quit that startup ok
and so I put that startup I was like
looking around ok what's the next big
thing I'm going to do and Gatsby seems
kind of like it is just like this tons
of changes right now around how we go
separate web and yeah a lot of kind of
like the mainstays of you know tool to
go to websites like forecast to pool you
know Jim wanna you know a whole host of
like proprietary tools like they're just
they just don't work as well anymore for
you know with all the you know the
smartphone like all like cover all
shifted to using smartphones all the
thing and the billions of people coming
online
you know another country yes that are
like on smartphones I'm like you know
crapping networks and so forth like
anyway like most of the old tools assume
your desktop and have reliable network
connection and like you shift away from
that world all of a sudden these sites
get super slow you know like like I
profiled just you know the the gang comm
awhile ago and it was like a 3G network
kind of smartphone is like 18 seconds or
something to look this is great yeah
which is just insane it's like you have
this like really pretty high profile
site that's just like yeah horrendously
an optimize anyways the point is I got
stopped looking around like like all the
a ton of companies know that they're
they need to have their websites work
fast on mobile and they just don't have
the tools to do it and like really
technically advanced companies they're
like figuring outs they're just building
stuff custom in-house but you know
that's only you know a few small
percentages you know companies that are
able to do that yeah have kind of the
engineering talent vision and in a guest
like a critical need to you know spend
the 500k or something to build their own
framework in-house 2 to 5 innings so
here I noticed I know something else is
really cool gonna gatsby is if you turn
off javascript still works
yeah yeah at least the initial like page
loads and all the links work it just as
a full does the full network request
mm-hmm yeah pretty cool yeah yeah that's
that's that's that's something you get
from the static generation yeah Drupal
are you familiar with next Jesus
uh yeah loosely I have this or anything
but I mean it's it's in this can you
have a you have a comparison between
next and Gatsby um not that I've ever
down but I mean just there's never too
laughs about this
you know something I thought about and
discussions with people about and I
think on the whole the very they have
very similar goals and you know that you
want to be able to like easily create
websites that are fast using reacts and
I guess the big difference is that you
know gas using a very focus on kind of
like the status a goal the coming
version of next you know adds a static
export which is like sim water I'm not
I'm not entirely sure in the details of
that but it seems like fairly similar to
what gets you goes and I think like the
biggest differentiator is that you know
next doesn't have an opinion on
downloading it just gives you like a
function that it calls when it wants
that and give it to add and so that's
what that's always very do it yourself
operation and where Gatsby has seen to
the whole data layer and graphical
system and multiple sources transformer
plugins to make it very easy to you know
get data from wherever it is into your
site so yeah so I think because the
website without that I'm isn't that's a
no so nothing yeah so I think that's a
enough that's been like the major focus
of all the work of daily Batsy cuz I
guess you want to also add like code
splitting and like a few of the things
but honestly all that stuff was done in
like a few weeks you know was August
okay man I'd really like nine ten months
of work all around you know let this
whole data layer and plug-in system yeah
because that's the road road blocking
for most sites is it's like you know
getting the
yeah getting data to the right place the
right time and why I got everyone so
fast that you know just saw it just like
mix it just handles behind the scene
like getting data loaded at the right
time in the right place so that when you
click around everything's just like
they're like prefetching data yeah okay
yeah just because it like knows you know
I was like what links are in the page
yeah and gets the data for those yeah
that's exactly mechanics like it's just
like it knows so you land on a page
level Gatsby's like hey you're linking
to these other pages so I'm going to
start prefetching the data for each one
of those page data and sometimes code
for all those pages so that when you
click on it everything is already there
two to go cool so one thing I love about
Gatsby is how you've got your pages
directory and then inside of there you
can just make a folder for each post or
page and and then that way like for
normal markdown posts or images are
right there next to the post and then
but then also you can just instead of
doing markdown you can do a really good
job a script file who knows yeah yeah
yeah yeah that's up I mean you could
just have like a live demo inside yeah
the ghost yeah yeah exactly want a
component or whatever yeah yeah that
that fun I like yeah stuff like number
one my first I working in guest is like
that was so cool just he dropped the
react component in terms of to a page
it's a very straightforward way to think
about things
yeah a lot of people's in my bed so why
is it called gasps me ah so yeah people
often applicants your story behind it
and really but not like actually
recently I never I haven't even read
caps be like a great book like The Great
Gatsby before I started working on get
Swedish buddy
is really just starting to project and
like okay what I'm going to need this
and I is like I really like books with
it triggered all sorts
and it's not that one apparently yeah
actually it's not right it looks done
stand out like white people here is what
so famous it's just kind of like weird
people with beard problems yeah one
loser it's a church
yeah that's like gassy it's just the eye
sees not what we though yeah yeah and
yeah I entertaining book I guess a movie
but not anyway uh so yeah I just like
googled like literary names famous
literary names and I just went through
the lessons like which ones sound good
you know kind of rememberable and sound
good and then also you know which ones I
already have the Indian buckets and
looks like and
Twitter handle yeah and Gatsby fit all
those names but I can't feed up like a
fun name in ceasing librarian yeah it's
kind of Awesome is there anything else
you wanted to say ah he's got a nickel
request and yeah I mean didn't you have
13 contributors on this v1 know a lot
was that actually there was like maybe
it was made of look typing at one point
three yeah just in the latest minor
release there's no it's been four four
four before the multi released there is
something like forty fifty people
contributing to the initial stuff and
since then there have been like 30 ish
have made the exact count but somewhere
the 30s I think contributors since and
just in the last like three weeks look
do you have helpful links or how to get
started contributing and or easy pull
request to get started on or anything
like that
[Music]
there's yeah there's there's so probably
easiest way to get going is just there's
a long list of plugins that can be
written and example sites and so there's
an issue for you know just just people
brainstorming different stuff that can
result so that would be kind of a fun
place to start so the plugins in example
sites or would those be a part of the
Gatsby or
work or just your own repo unique so
example fights are to demonstrate the
use of plugins or particular techniques
okay
if yet so so kind of actually need to
write this up but kind of try to think
about like the Gatsby mono repo is it's
for like Gatsby related infrastructure
so plugins like data plugins you know
let pack plugins that sort of stuff
anything that's kind of like at kind of
like lower levels of building the
website but kind of add more teenage
stuff like hey here's like a sweet you
know sweet theme for building I could
get people or something like that that
kind of like outside of yeah yeah but I
mean other total useful to I mean lots
of people build it first gatsby site
based on like what we feel like starters
you know guess we started that so I'm
just contributed so literally awesome so
if you if you're more of a kind of like
she enjoyed more kind of like the design
side of things and you just want to
build or get your caps you know like
blog and then build up Gatsby and then
share with the road then like building
and contributing back like a Gatsby
starting would be awesome and if you
want to write anyone you know like like
a cache of shit bugging pit they cook
like plumbing taking this stuff then I
put a lot to get your book and stay here
as well oh I'll put a link to that units
awesome all right well thank you so much
for coming on show yeah my question yes
<div class="Transcript_Expander"></div>
</dl>
</article>
