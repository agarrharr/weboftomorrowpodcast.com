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
<dd>Alright, welcome to Web of Tomorrow. I'm Adam Garrett-Harris and today we're talking with Kyle Matthews and creator of Gatsbyjs</dd>

<dt>Kyle Mathews</dt>
<dd>Hey everyone!</dd>


<dt>Adam</dt>
<dd>So what is Gatsby?</dd>

<dt>Kyle</dt>
<dd>Gatsby is a blazing fast React static site generator and it aims to give you a really nice out-of-the-box experience where everything is set up for you: React, Webpack, different CSS options, modern JavaScript etc. And you can build really fast sites without a lot of effort on your part.</dd>

<dt>Adam</dt>
<dd>Cool. So, how did you get the idea for Gatsby?</dd>

<dt>Kyle</dt>
<dd>Basically, so I started using React pretty early so it was open source like mid 2013 and it got on my radar then and I was working at a job in San Francisco, a startup, building JavaScript web applications with Backbone and I really liked in a lot of ways, but it had a lot of weird sharp edges / missing things and React just came along I was like "This is so beautiful, the component model." Because I mean components is an old idea. React didn't invent the idea of components. I mean backbone components existed, but they were kind of just missing a lot of stuff. Anyway, so React component was just like so beautiful.</dd>
<dd>And so anyway, I start following that and I quit that job like early 2014 and just started doing a bunch of stuff with React was like this is the future that's what I want to learn and do everything with and then mid-ish 2014 a friend and I we started working on startup. So I worked on that for a while and it was building our web application with react of course and then early 2015 it was getting to a point we were like "Ok, we kind of know what we're doing. We have the application sort of working like start to go public pretty soon and of course need website and I was like "Okay, I haven't build like a website website in a while. How do people do that these days?" And I was looking around I was like "Oh man. I hate all these things because I'd use like Drupal and WordPress and built my own little static site generator in the past. I was like "These are all terrible. I want to use React components and Webpack and all these other really nice modern tools. There was other people thinking about the same thing at the time and I just thought about it a bunch and I figured out a clever way to pull all those together. And so that was the first version of Gatsby that I built just for my startup's website.</dd>
<dd>And then I open source that and then a lot of other people got interested and it just kind of snowballed from there</dd>
<dt>Adam</dt>
<dd>Cool, so what is the tech behind Gatsby? You mentioned React. What else?</dd>
<dt>Kyle</dt>
<dd>So, the goal of Gatsby is to use industry standard stuff with the idea being that if you're a React web application developer you can install and use Gatsby and it feels completely natural. That's what I wanted. I mean, I'd already learned Webpack, and React, how to use those two together, and loaders and so forth for the applications I had been building. So that's what I wanted from Gatsby. So, it uses React and then Webpack for module bundling, and then normal standard loaders and so forth. So if you build a React, Webpack, Babel web app then using Gatsby should feel pretty...</dd>
<dt>Adam</dt>
<dd>And then, it also has Redux and graphQL, right? </dd>
<dt>Kyle</dt>
<dd>Yeah so the latest version of Gatsby, it adds Redux, but that's just for managing internal state. While using Gatsby you shouldn't see Redux at all. And yeah, graphQL is also new addition to the new major version of Gatsby that was released recently and graphQL is used very much like Relay or Apollo, those kind of clients for building stuff on the web. It works pretty similar that on React page components in Gatsby you can have a query which says, for this page, for this blog index page, or for this product overview page, here's the query it describes the data that is needed for that page. And then Gatsby makes sure while you're developing and in production that when that page gets rendered that data that you query for is there.</dd>
<dt>Adam</dt>
<dd>Cool. Alright. So, who is Gatsby for? Who you want to be using this. What kind of stuff can you build with Gatsby?</dd>
<dt>Kyle</dt>
<dd>Yeah so, the first version of Gatsby is kind of intended for... Basically my mindset was: hey React developers who also want to build websites. So you want to have a static render of everything. You have your different React pages and you can throw in some markdown as well. And you just want to have a static render of that so that it loads faster. That was kind of the main use case that I had in mind for the first version of Gatsby, but Gatsby v1 is much more ambitious, the latest version, in that it adds the ability to pull data from remote api's and this is really important because most websites in the world are powered by content management systems and the reason for that is it's not just one or two developers who are cranking out the site. There's lots of course, but the vast majority websites in the world are big complex operations with dozens or even hundreds of people who all have their hands on all sorts of different pieces of it and they need specialized tools for managing the content, which we know is content management systems. And so for any website building tool to actually make it outside of the little niche of programmers you need the ability to integrate with content management systems and so that's one of the major focuses of Gatsby v1, to be able to do that. Which has already paid of because I've seen there's number of agencies that are working on Gatsby WordPress sites where they're using WordPress as a CMS and then building the actual site in Gatsby. So they get the advantage of modern JavaScript and CSS and the React component model, but they still have the familiar WordPress ecosystem to set up the actual content editing experience for their clients. And they've been really happy with that.  There's also a lot of new startups offering CMS's that are headless basically, where all they are is the content editing part and an API. WordPress is that piece plus everything around actually building and running the website and those work really well with Gatsby because they just they concentrate on having a really nice interface for creating editing content and then Gatsby has a really nice tool set for building really fast websites</dd>
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
<dd>clearly couldn't make their app with Jekyll.</dd>
<dt>Kyle</dt>
<dd>Exactly, and there's a ton of inefficiencies through that model because you have different programming languages, you have different models of thinking about things, you have different build steps, you have the problem of merging styles back and forth, and this that and the other thing.</dd>
<dd>If everything's in Gatsby you can reuse the same layout components and other components across the whole site. It's the same styles, it's the same way of thinking about the world, so there's no friction because in a lot of companies the marketing site is like the redheaded stepchild. Where marketing people are always begging for engineer time like "Hey somebody come work on our site" and they don't want you because it's this big abrupt shift to "How's the stupid thing work again?" But if everything is the same everything kind of moves along together. It's a much cleaner more efficient model</dd>
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
<dd>Yeah, that's the typefaces. Yeah, the basic idea is that self hosting your fonts is faster almost always than Google Fonts.</dd>
<dt>Adam</dt>
<dd>Yeah, I had no idea. I thought it's just getting it from somewhere so why is it why is it slower from Google?</dd>
<dt>Kyle</dt>
<dd>So the reason is that, what Google Fonts gives you is a CSS file so when you add Google Fonts to a site it adds basically a CSS file that Google hosts. So you first have to make a request to get that CSS file and then in that CSS file there's then links to the actual font files for whatever font that you want to add to your site and so Google Fonts is always like two request before you have the fonts.</dd>
<dd>And then when you self-host and with inlining it, there's no additional request, I guess. You load the page and then the links are already there to the font files. So it just avoids extra requests.</dd>
<dt>Adam</dt>
<dd>So you mentioned you can get data from external APIs and then you are going to generate static sites locally instead of on the server and push up those static files. What happens when that data changes from the time you build it to the time a user visits the site. Do they get the old data and then it flickers for a second and gets the new data</dd>
<dt>Kyle</dt>
<dd>So no, Gatsby. I mean is a static site generator so you're kind of outputting static bundles. The whole site is just like HTML and JavaScript and json and that sort of thing. So basically you need to rebuild the site every time there's a change and so whatever so basically you can think of as versions of the site. So if user A loads version 273 then they'll be navigating within version 273 and if there's a change to content or to code or whatever, like version 274 is out, then they won't see that until they reload the site.</dd>
<dt>Adam</dt>
<dd>So, if you build a Gatsby site and then someone makes a change on the CMS, maybe they're using WordPress as a CMS, the site will not be updated until you build Gatsby again.</dd>
<dt>Kyle</dt>
<dd>Yeah, exactly.</dd>
<dt>Adam</dt>
<dd>Have people come up with a way to automate that?</dd>
<dt>Kyle</dt>
Yeah, so a lot of people are doing that. Basically you just need to have a build server of some sort and there's a few sources that do that like Netlify and then you have web hook from your CMS that then just triggers a rebuild on your build server.  And so yeah, it's fairly straightforward to do. I know some people
<dd>also do a cron job. That's another option if your data doesn't change that often.</dd>
<dt>Adam</dt>
<dd>Okay and a cron job we just run a certain interval, like every night or something?</dd>
<dt>Kyle</dt>
<dd>Yeah, something like that, but generally speaking a web hook works really well and it's fairly straight forward to setup. Most CMS's, especially the API CMS's are already set up to do this out of the box.</dd>
<dt>Adam</dt>
<dd>Yeah, and then you probably get an email if something didn't build right.</dd>
<dt>Kyle</dt>
<dd>Yeah exactly.</dd>
<dt>Adam</dt>
<dd>Awesome, so one question I'm really interested in is that a year ago you announced you're working on Gatsby full-time. And so how do you make money? If you don't mind.</dd>
<dt>Kyle</dt>
<dd>No, that's a great question.</dd>
<dt>Adam</dt>
<dd>Because, I think it seems like you're kind of living the dream. You were like , "I'm just going to quit my job and do this open source project</dd>
<dt>Kyle</dt>
<dd>Yeah, so basically it's been a few different sources. There's been a number of companies who are really interested in the plans for 1.0 and have either directly sponsored it or pay me to work on projects using the work in progress 1.0 code and that's been the majority of funding. And yeah so that's been what I've been doing so far, but this the tricky thing about open source is that you really need, for an open source project to really take off, you really need at a minimum of like hundreds of thousands of dollars investment. You know? And you get some of that of course if you have lots of people using it and lots of people submitting PRS they're individually it's like if you think about the time value of a lot these different PRS that people are contributing, Each PR is minimum hundreds of dollars investment and some mid to major PRS could easily be thousands of dollars of time that these really talented engineers are contributing to the open source project. So there's definitely lots of investment.</dd>
<dt>Adam</dt>
<dd>So how much learning is involved with Gatsby? To get going with Gatsby? Say so you don't know React. Is React all you need to know or what else?</dd>
<dt>Kyle</dt>
<dd>You definitely have to have a probably even a fairly beginner level of understanding React should be sufficient because most of the time you're just using like React components and you really can use just the function React components for most stuff. So, basic understanding of JavaScript, basic understanding React some understanding of Webpack is helpful, especially if you want to do more complicated things and then past that it's really how far you want to go in different directions.</dd>
<dt>Adam</dt>
<dd>Okay, how much of the Gatsby API do you need to know?</dd>
<dt>Kyle</dt>
<dd>Again, it depends. If it's a pretty simple site perhaps none at all. You just start using Gatsby and then you add your plugins and then you just write React components and then build it and off you go. But if you want to start writing custom plugins, then of course you have to dive into the API's. So the goal is that the plugin system is robust enough that as time goes on more and more use cases will be solved by just installing a plugin.</dd>
<dt>Adam</dt>
<dd>Yeah, so was looking through the posts on the Gatsby blog about how to get started making a Gatsby blog and a lot of it is just installing Gatsby plugins, but it still seems fairly intensive as far as install all of these and then here's all this boilerplate code to wire it all up.</dd>
<dt>Kyle</dt>
<dd>Yeah, and I actually have a plugin in mind that will remove most of that boilerplate. So yeah, that's the goal. With all the work just to get 1.0 out, I left it kind of boilerplatey, but the idea is that any boilerplate can be subsumed within a plugin.</dd>
<dt>Adam</dt>
<dd>Yeah, I think it's also kind of cool because even though it is boilerplate it describes exactly what your site is doing and you can change it.</dd>
<dt>Kyle</dt>
Yeah exactly.
<dt>Adam</dt>
<dd>It's not it's not super opinionated. It doesn't say how you have to name your files or where you put files or how things go or what a post is or what a pages is, you know? You can do whatever.</dd>
<dt>Kyle</dt>
<dd>Yeah, there's always this trade-off between use cases, and it's like "Oh, we'll build around those use cases" and then those use cases are very easy to accomplish, but then "Oh if I want to step outside of those blessed paths, then all of a sudden life is hard. And a lot of systems end up in that trap I guess. And I didn't want that to happen with Gatsby. So what I think the best patterns is, is that you have pretty low-level primitives that you say these these basic things are what constitute. It is what the system supports and then you add scaffolding tooling that then you can build up abstractions on top of. You can build up arbitrary abstractions on top of those lower level constructs. And so if you think about a programming language. Programming languages are awesome. There'll all completely designed around this. They give you different data types, you have strings, you have ints, you have your floats, and you have functions, and whatever, and then using this pretty low level stuff you can then build up any sort of abstraction on top of that and it works super well. You can think of Gatsby like that same sort of thing where Gatsby's like "Hey, you have pages, you have layouts, you have data of various sorts, you have queries that you can query your data and pull data into your components and then using these site-specific primitives then you can build up abstractions on top of.</dd>
that cool so you said you can pull data
from PPIs, but you can also just have
local data and then you got your pages
and posts so how describe queries how do
you get how do you use that data and so
interesting thing about the local
stuff is that in the Gatsby world 
data coming from your local file
system is treated exactly the same as
data coming from remote API school my
first guys concerned is just data that
just arrives from somewhere so they took
a key that system is basically there's
source plugins and then there's
transformer plugins and so source
plugins their responsibility is 
somewhere out there in the world there's
data and it pulls it in somehow and it's
up to the source plug-in how it does
that because use carrier business or
probably doesn't, but probably uses 
JavaScript NPM libraries or
something or API calls to get
stuff and so in the case of a file
system we the source file
system plug-in you just tell it what
directory to look at and then it goes
through that director and
cursive Lee finds all the files and then
adds those as as files file it was
as those of notes which is no
telling the basic gatsby data type
into Gatsby and then it was usable, but
a remote source plugin it was just
hit an API and then pull into that from
there and then somehow turn that into
again notes which then go into Gatsby
and then transform plugins how they work
is that source plugins can say so sort
of and say hey I know how to
handle my I know how to completely
handle my data
so I'm just going to add them as 
the dad was already decompose into fields so
there's no more can I be composed
decomposition that can happens 
there's a title field and there's a
field and there's any other thing it's
already in its final state
but there's often times where you have
data that the source
plugins well I don't really know
exactly what the end user wants to do
with this and so I'm going to have to
leave it and 
unconverted form a raw
source form that then can be converted
per the needs of an individual site so
markdown is a really obvious
example of this because it's pretty
common and so a source plug-in say
hey I have this note and it's marked
down and I'm not going to do anything
with it's just , but here's my
time for this note is has is 
raw content that's markdown that a
transformer plug-in can come long and
say hey I know how to transform markdown
into something else
which of course typically is HTML so there's I thin transformer
plugins that take this raw content
markdown and then turn it into HTML and
so it basically says choose them here's
here's a note that's a type markdown and I'm going to transform it
into a new note that's a type HTML okay
and so this can be this sort of 
transformations can happen from any one
data type to another data type so 
there's a CSE transformer which
takes a CSV file and turns it into
each row is now a new
note same thing JSON you
know Gamal there's image
transformer plugins with key K an image
and then can turn it into resize the image and yeah turn
down the grayscale can do
basically anything that you want and is
it all done with JavaScript uh not
necessarily it can be done with
JavaScript and for the image case
there's a this
NPM packets called sharp which has which
anyways it uses another
really older image
magic or something it's not using its
lid bips or something well anyways
it's super fast and it's 
really it's pretty easy to install and
press pop one so yeah it does
it has a lot of the image
transformations, but you could you could
totally write within this magic v1
anyways yeah so it's so you have
source nodes and the transform nodes
take data and turn into
other sorts of data anyways and it's all
eventually this is 
chain and transformation so it's
just automatically happens
using all the plugins that you install
and then out of that comes then a
graphical schema which is all the different types of data you have
and all the fields that you have because
turn to this is schema and so it's
it's one way of
thinking about is you're
basically constructing on the fly a
database yeah we have all your data and
all the transformations of the data
and then you then how a database
schema which in this case is very
powerful well and then you
know old-school PC or something
that then when you're creating
pages then you can just write queries
directly against your database
to pulling the data that you want
and yeah so graph tools a really
nice query language for that because I
would just pull it into parts you need
yeah so if you're oh
I need a list of all the authors mm-hm
you do it
yeah tags for yeah for the pages tags
that are within those pages or pages
there with it within this tax yeah some
stuff that can be really hard with
aesthetics I generated yeah exactly I
just come up with an idea of what you
want to query for and then you got it
yeah because that look yeah that
was one of the big motivations for this
new data layer and no graphical system
is that yeah I static
generators are really nice for simple
types because it's very simple it's
just oh you you have done and
you put free templates and outcomes
pages and you're assuming the 
data that you want yeah yes
they let you put some custom work done
and stuff, but creating it's not that
easy
yeah, but yeah it's you kind
of the idea of jumping across
lots of different files or the logic and
data source and seeing it look we're
all authors or oh hey all
posts created by out there or all posts
we're attack shows up Unitas or stuff
that gets weird to do in static
site
Trisha sighs degeneration generators and
so the graphical wall and stuff makes it
better really true be able to do and it
also makes it trivial to do all sorts of
complex data transformations that
are just powered by plugins and a
performant cache and so forth so what
are there other types of plugins besides
be what you call it source yeah so I
just said source and transform yeah so
so there's plugging with that or for the
data layer so those are the source and
transformer plugins
those are responsible for patching
data and then transforming data in
different ways so those are both plugins
but then there's also plugins for kind
of two other categories that guess would
be wet pack related plugins so you
know if you want to set up if you want to use less for example
there's a web pack world there's a left loader that you use to
then add support for transformer for what
that going to loading less files and
doing different stuff to it and so
there's actually not a gap you what's
buggin yet, but some news that's a good
example to similar than that maybe I
just got the SAP plugin okay we're still
is all set up for using sass in your
site and then there's also another
category plugins for collect
solving the Shalini
yes in a website so for example 
adding Google Analytics hmm
there's just gastric bookends
latitude at the end of
your body and all the normal
stuff all you have to do is they okay
here's my here's the shiny ID
and then it happens and it was
an offline plugin which
generates a serviceworker
automatically it's set up for your
site so you add that house in your
sacred stuff so if this was a whole
bunch to will look very long list of
random stuff that
that bookings can handle it cool so
when you just said admit gatsby how
hard was it
and how did you figure it out and do you
think you would be able to do it yeah
yeah ah there's definitely a many
moments where i sadly that's just 
yeah this is it's just I don't know neat
whenever you do something novel
it's we don't know you're getting
yourself into
and so it's book it feels hard 
both the end nouns just you can you
don't know how long the pathways are
what you're going to count it all the
way and so there's a lot of fears associated what that
um know that to add their own s of the
path it's I'm going to
have to have resources to get through
what is it actually solvable you
know I haven't I when I started gap
speed the next major
version gaps we had a pretty good idea
of what I wanted to do what is is
it actually doable all
these things that I want to make happen
um yeah I think for me I wouldn't I
wouldn't think is it doable, but can't I
do it yeah no yeah it's I don't
know I mean I don't know I
very much uh I think
most people are people doing
they think they can it's just letting
yourself I'll leave that and then
they're putting in the time
yeah to get there and there's definitely
I had to learn a ton of stuff to do
gah yeah there's a lot of a lot of kind
of Co techniques I hadn't used
before getting the necessarily know
existed, but I got the thing is it's
you can overcome your fear of the
unknown and just plunge in
it's it's you dive in
and then I mean you can't see that app
that you're going to take necessarily
but once you get there either you
can cut your way through or you can
let go ran upsala back and that's what I
it was a lot of meta forcing user, but
basically it's advice you 
allow yourself the time to learn things
you can do a lot more than you
think you can it's if other people
people who do stuff that you
haven't done it isn't because they're
smarter than us it's because you
know for whatever reason they've had the
opportunity to learn you learn the
skills and knowledge necessary to do
those things and so if you allow
yourself the time to learn those skills
and those and  a lot you can do
cool so when you started this did you
have a full-time job and you're sitting
on side and now so we talked earlier
about a about the startup so I built the
first version Gatsby just to build that
website basically and so I started
working on the next major version that
gets you go which is released a few
weeks ago when I quit that startup ok
and so I put that startup I was 
looking around ok what's the next big
thing I'm going to do and Gatsby seems
it is just this tons
of changes right now around how we go
separate web and yeah a lot of the mainstays of tool to
go to websites forecast to pool you
know Jim wanna a whole host of
proprietary tools they're just
they just don't work as well anymore for
with all the
smartphone all cover all
shifted to using smartphones all the
thing and the billions of people coming
online
another country yes that are
on smartphones I'm crapping networks and so forth 
anyway most of the old tools assume
your desktop and have reliable network
connection and you shift away from
that world all of a sudden these sites
get super slow I
profiled just the gang comm
awhile ago and it was a 3G network
smartphone is 18 seconds or
something to look this is great yeah
which is just insane it's you have
this really pretty high profile
site that's just yeah horrendously
an optimize anyways the point is I got
stopped looking around all the
a ton of companies know that they're
they need to have their websites work
fast on mobile and they just don't have
the tools to do it and really
technically advanced companies they're
figuring outs they're just building
stuff custom in-house, but that's only a few small
percentages companies that are
able to do that yeah have the
engineering talent vision and in a guest
a critical need to spend
the 500k or something to build their own
framework in-house 2 to 5 innings so
here I noticed I know something else is
really cool gonna gatsby is if you turn
off javascript still works
yeah at least the initial page
loads and all the links work it just as
a full does the full network request
mm-hmm yeah pretty cool yeah that's
that's that's that's something you get
from the static generation yeah Drupal
are you familiar with next Jesus
uh yeah loosely I have this or anything
but I mean it's it's in this can you
have a you have a comparison between
next and Gatsby um not that I've ever
down, but I mean just there's never too
laughs about this
something I thought about and
discussions with people about and I
think on the whole the very they have
very similar goals and that you
want to be able to easily create
websites that are fast using reacts and
I guess the big difference is that you
know gas using a very focus on 
the status a goal the coming
version of next adds a static
export which is sim water I'm not
I'm not entirely sure in the details of
that, but it seems fairly similar to
what gets you goes and I think the
biggest differentiator is that next doesn't have an opinion on
downloading it just gives you a
function that it calls when it wants
that and give it to add and so that's
what that's always very do it yourself
operation and where Gatsby has seen to
the whole data layer and graphical
system and multiple sources transformer
plugins to make it very easy to get data from wherever it is into your
site so yeah so I think because the
website without that I'm isn't that's a
no so nothing yeah so I think that's a
enough that's been the major focus
of all the work of daily Batsy because I
guess you want to also add code
splitting and a few of the things
but honestly all that stuff was done in
a few weeks was August
okay man I'd really nine ten months
of work all around let this
whole data layer and plug-in system yeah
because that's the road blocking
for most sites is it's getting the
yeah getting data to the right place the
right time and why I got everyone so
fast that just saw it just 
mix it just handles behind the scene
getting data loaded at the right
time in the right place so that when you
click around everything's just 
they're prefetching data yeah okay
yeah just because it knows I was what links are in the page
yeah and gets the data for those yeah
that's exactly mechanics it's just
it knows so you land on a page
level Gatsby's hey you're linking
to these other pages so I'm going to
start prefetching the data for each one
of those page data and sometimes code
for all those pages so that when you
click on it everything is already there
two to go cool so one thing I love about
Gatsby is how you've got your pages
directory and then inside of there you
can just make a folder for each post or
page and then that way for
normal markdown posts or images are
right there next to the post and then
but then also you can just instead of
doing markdown you can do a really good
job a script file who knows yeah
yeah that's up I mean you could
just have a live demo inside yeah
the ghost yeah exactly want a
component or whatever yeah that
that fun I yeah stuff number
one my first I working in guest is 
that was so cool just he dropped the
react component in terms of to a page
it's a very straightforward way to think
about things
yeah a lot of people's in my bed so why
is it called gasps me ah so yeah people
often applicants your story behind it
and really, but not actually
recently I never I haven't even read
caps be a great book The Great
Gatsby before I started working on get
Swedish buddy
is really just starting to project and
okay what I'm going to need this
and I is I really books with
it triggered all sorts
and it's not that one apparently yeah
actually it's not right it looks done
stand out white people here is what
so famous it's just weird
people with beard problems yeah one
loser it's a church
yeah that's gassy it's just the eye
sees not what we though yeah and
yeah I entertaining book I guess a movie
but not anyway uh so yeah I just 
googled literary names famous
literary names and I just went through
the lessons which ones sound good
rememberable and sound
good and then also which ones I
already have the Indian buckets and
looks and
Twitter handle yeah and Gatsby fit all
those names, but I can't feed up a
fun name in ceasing librarian yeah it's
Awesome is there anything else
you wanted to say ah he's got a nickel
request and yeah I mean didn't you have
13 contributors on this v1 know a lot
was that actually there was maybe
it was made of look typing at one point
three yeah just in the latest minor
release there's no it's been four
four before the multi released there is
something forty fifty people
contributing to the initial stuff and
since then there have been 30 ish
have made the exact count, but somewhere
the 30s I think contributors since and
just in the last three weeks look
do you have helpful links or how to get
started contributing and or easy pull
request to get started on or anything
that
[Music]
there's yeah there's there's so probably
easiest way to get going is just there's
a long list of plugins that can be
written and example sites and so there's
an issue for just people
brainstorming different stuff that can
result so that would be a fun
place to start so the plugins in example
sites or would those be a part of the
Gatsby or
work or just your own repo unique so
example fights are to demonstrate the
use of plugins or particular techniques
okay
if yet so actually need to
write this up, but try to think
about the Gatsby mono repo is it's
for Gatsby related infrastructure
so plugins data plugins let pack plugins that sort of stuff
anything that's lower levels of building the
website, but add more teenage
stuff hey here's a sweet you
know sweet theme for building I could
get people or something that
outside of yeah, but I
mean other total useful to I mean lots
of people build it first gatsby site
based on what we feel starters
guess we started that so I'm
just contributed so literally awesome so
if you if you're more of a 
she enjoyed more the design
side of things and you just want to
build or get your caps 
blog and then build up Gatsby and then
share with the road then building
and contributing back a Gatsby
starting would be awesome and if you
want to write anyone 
a cache of bugging pit they cook
plumbing taking this stuff then I
put a lot to get your book and stay here
as well oh I'll put a link to that units
awesome all right well thank you so much
for coming on show yeah my question yes
<div class="Transcript_Expander"></div>
</dl>
</article>
