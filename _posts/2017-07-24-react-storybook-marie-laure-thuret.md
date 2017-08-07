---
layout: post
title: "38: Storybook - Marie Laure Thuret"
summary: "Storybook is an interactive development & testing environment for React and React-Native UI components. Marie explains why it's useful and how they use it at Algolia."
link: https://s3.amazonaws.com/weboftomorrow/2017-07-24-38.mp3
size: 26318152
length: '00:23:25'
permalink: /38
---

- [Storybook](https://github.com/storybooks/storybook)
- [Marie's Talk at React Conf](https://www.youtube.com/watch?v=PF0Vi-iIyoo)

## Transcript

<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Welcome to Web of Tomorrow, a podcast all about the web and the people who build it. This is Adam Harris.
</li>
<li>
In this episode I talked with Marie who is a front-end developer at Algolia in France and she talked about Storybook, which is an interactive development and testing environment for React and React Native UI components.
</li>
<li>
Thanks for coming on the show.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Thank you. 
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
How did you first hear about React Storybook? or how did you get started with it?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
I heard about it pretty close to the release date, the beginning of 2016. So, I was working on a presentation about how you can test your React and Redux application and basically I just came across React Storybook and I actually loved the idea because of a previous mission I worked on with Ember while doing Storybook and it was a way for us to showcase our components and to test them, and to show how you can use them. And I found that very useful and so having a tool that already does everything for you and you just have to start developing. I think it was an amazing idea and started to use it.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, and so what is React Storybook exactly?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Basically it's a tool that provides a nice enviroment where you can develop your UI components in total isolation, and so it forces you to be outside of your complex application, which actually is easier to develop because you are not polluted by a lot of stuff. You just design your components and develop it and that's it. So you can concentrate on the API. And so basically this tool is a dedicated interface when you write your own stories, which is basically your component at a precise state.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
 Ok, cool, so you actually create your components first inside of React Storybook. That way you're not inside of your complex app or anything. You're not having to click around a million times to get to that component or whatever.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yes, exactly. If you want to actually concentrate on a specific substate of your component, you can pass the right props and you will have a dedicated story for it. And then it's easier to develop your app. Then you need to actually be in the right substate to actually develop your dedicated behavior. So it's a lot easier. And one thing that is great is that you can think of the API first. It's something that I like to say because often we want to create generic components. So here you are not inside your app you are forced to design in isolation so you can really create generic components.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, so how do you get started using it? Do you just npm install in inside of your app?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
The team developed a command line, so if you already have a react application you just install it globally. It's called `create-storybook` and then you run it, and it will create for you, all of the config files, which at the beginning is not a lot of files, but to see something working you type `npm run storybook` and that's it. You get the environment and you can start adding your stories.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, and do you like to put those stories right alongside the component or in a seperate place in your app?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
On my current project, I do it in a separate place, but I know that some people prefer to have it just next to it. I mean, it's a matter of taste. Maybe I'm working on a widget library and so I don't have that much widgets, so in the end, the directories are full of files. But if you have a big application, it might be better to put them next to the components.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Or at least to respect your directory stategy
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Yeah. Ok, so in your talk about React Storybook you talked about it helps you design, document, debug, and discuss. Can you talk about each of those, starting with how it helps you design?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yes, so actually in that talk, I talk about all the stages you go through and it starts obviously with the development and the api, but then you need to actually style your components. With Storybook, it's convenient because once again you can be very quickly on one substate of it. So, if you know that for example, with my talk I showcase a pagination component, but if because you're on the first page you want to disable one button and you want to style this thing, then you can do it quickly. And then at some point, about the documentation, because you have all those stories, you actually created the documentation. It's already there. You don't have anything more to do. Because you can pubish the storybook. So it means that you can statically build the storybook, then publish it on the web, or anywhere else. And then people can start looking at your components. They can start playing with them. And Storybook provides different add-ons that help you document more of your components. So it's a great way to showcase your components to other people. And then for the devlopers, it's not about debugging. To be efficient when debuggin you need to produce a bug in the smallest number environment possible to be sure you are not polluted by your other stuff. So with Storybook it's easy because you are already isolated, so you can reuse you components or you can create a story with 2 or 3 of them and you can actually try to reproduce a bug with the least amount of code involved. And the last part is my favorite part: discussion. Because you can share this storybook with others. Others can actually use your storybook to start discussion. So, one obvious example is that if you develop something that involves a component, you can link to the storybook and actually add people to visually see what you are saying in your issue or whatever. 
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, so you said you can kind of create a static website off of it and then you also said you can link to your storybook. So how does that work exactly. Do you run a command to create a static site and then upload it somewhere and then share that link?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah exactly. Storybook provides a command that is called `build storybook`. So if you do npm run with storybook you get the storybook files statically. So then you just deploy it somewhere. So, for example, at Algolia, we deploy the storybook on Netlify, which is a hosting service. And each time we do a PR, it will be deployed on the service and everyone can access it. But it means you can also deploy elsewhere, for example, Airbnb, it's what they do. If you go on their github website, you have a link. You can click on it and you can actually browse that storybook and you can see the widgets. So it's up to you to imagine what will fit your need best, but you have the tools to do it.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
So you can just have it as a part of your build process automatically.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah, exactly.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool. So, let's talk a little bit about what it looks like and how you use it. You've got a panel on the left showing all the components, right? And then, in the middle, you can see the component. And then down below, you have some tabs? Ok, so how do you show events that are happening from the component.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
So you've got a special add-on. It's called the action add-on. And so basically, for all your actions that are props. When you pass in a function, and the function is used by the component. You can replace this function with another function, which is provided by the add-on and then if you click somewhere on your component, then you will see the events logged on the panel on the tab below so you can see what's happening.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, and then how do you show the component in various states.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
So when you first create a story, it's what's called a story skin. So, let's say we have a component, which is a pagination component. You will say, I want to create stories for the pagination. And then you will start to write a story. And basically, each story is a substate of your component because for each story, you actually declare your components so you can vary the props you use and stuff like that to have your components in seperate states.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, and then can you also just play around with the props as well.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah, definitely. You've got another add-on. In the same way, you can, instead of just passing a prop, you can pass a prop with a different value, but then also add extra information, like if it's a number or if it's a string, or if it's an object, etc. And then this add-on will display those props inside the panel and then everybody can play with it. For example, if you have a number on you component, and you set the value as 1, then you will have a new entry on this panel and you will be able to type any number. And then the component will be able to render with the new props. So it's great because, your user or collegues can actually play with the props and see what the props are doing, what the bahavior is.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Yeah, I think that's useful, not only for your fellow programmers, but also designers, and PMs, and managers, and things like that.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yes, definitely.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool. So, you talked a lot about add-ons. You also made an add-on, right?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah, because I really love the concept of live documentation and before working on content stuff, I had a lot of interest in behavior [...] and those two converge given that allows you to write some [...]. And now you can write some documentation. So when I switched to content development with Storybook it was a bit of the same thing for me. You've got your stories and then, because it's like your code that is executed. I wanted a way to test them because I know that when we develop, at some point, you get incorrect things if it's not tested. So obviously, you would probably test your components in other files and stuff like that. But then you end up with duplication between your stories and your test files and I wanted a way to actually avoid that. So I can test my stories directly. You can write your tests just next to your stories and then display those directly in the storybook. The idea was to use those tests as specification of your components because even though it's a UI component and should not have that much business logic inside it, often you get things that are actually business related. And so if you're a new employee, or even yourself later, sometimes it's great to actually [..] and the tests are actually good for that. That was the idea, to write the test next to the stories.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, cool, so what kind of tests are you writing on components. Are you doing snapshot tests to see what the output of the render function is? Or is there... You mentioned business logic. What kind of business logic could you test?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Actually, with Storybook you can snapshot your stories. It's provided by the tool. It's called snapshots. And it's based on [...]. So, what this library does is that it takes all your stories and snapshots them, so you've got all of that markup somewhere and if you start developing, then you will see the diff, and you'll see if you made some regressions on that. The idea of my add-on which is called the Specification add-on, is a bit different. It's not really to test markup, it's more like to check actions, or like I said, things that you want to  be explicit on, like business logic and [...], and things that actually relate to data. And then for that you can use whatever you want that works in the browser. So I typically use Enzyme and Expect for the assertion. So you make your stories and then you can use the Enzyme API to make the assertions.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, so you can see those tests, whether they pass or fail, in Storybook. Can you also see if they fail somewhere else, like in the command line?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah, you can use both, inside the storybook and inside the CI.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, does the tab, light up red or something if you have a failing test inside that tab? Because you might forget to look in there.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Oh yeah, definitely. I mean, inside the tab is more to actually see the specs. To me, a failure is better to see in the CI. In the storybook, it's more about the specification of the component.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool. What other kind of add-ons are there?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
There's a lot. I would divide them into 2 parts. Some are about styling components. For example, there's some add-ons that helps with resizing the window to help you ensure that your components are responsive. Some add-ons that will change the background color of the storybook, again to help you with the styling. And you also have add-ons that are more related to documentation. For example you've got one that will generate the source of your components in a way that if somebody goes into the storybook, you see the component and then the usage, so you can copy paste. And other stuff like generate props. What else? I think there are some that allows you to actually add a readme, if you need that. So there are a lot of different things. And the good thing with Storybook is that creating an add-on is easy. So anybody can create their own if they need to. And then they can share it with others.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool. So another thing you mentioned in your talk was linking stories together where if you click on one component, it will link you to another. Or if you click on one story, it will link you to another story. What is the purpose of that exactly? I wasn't sure.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Yeah, it depends on how you use the storybook. For example, us at Algolia, we are using fully connected components. If you click on them, it's a top component. Often you actually need the raw components, so the lowest one. So, one idea would be to show how the component, like if you click on the button, what that button is supposed to do. And so, probably to get you to another substate of this component, you can link the stories together to show how they can interact together.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, yeah. So, do you know examples of who is using React Storybook?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
They added a new page on the website that showcases companies and projects that are using Storybook. If I remember correctly, so obviously I already mentioned us and Airbnb, but you've also got Buffer, Learning Planet, and there's others. Those are jus the public ones. I believe a lot of people are using Storybook, but internally, so you can't see the project. But now the project as over 10,000 stars.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Oh yeah, it's saying Slack and Squarespace also. Yeah, cool. I don't think I have any more questions. Is there anything else that you wanted to say?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
So, one thing I would like to add now that I didn't say in March, when I did React Conf about Storybook is that at that moment the project was a bit dead because it was created by Kadira, a company. This company shut down and then there was no more activity on the Github repository. So fixes were not getting done, and pull requests were not merged anymore. At some point, people were asking if it was possible to take over the project. So, it was opened to the world community and a lot of people are really involved to make this project live. And so there just really is the salvation of Storybook and what's really great is that you've got some initiative to extend Storybook to Vue and possibly other frameworks. So, it's really cool. I think it's a project will keep living in the future.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Cool, are you a contributor to Storybook?
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
I'm part of the team, but because I don't have that much time, I'm just doing small fixes or talking about it at conferences, but I'm not writing a lot of code for Storybook right now.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Ok, cool. Well, thanks for letting me know about React Storybook. I had never heard of it before, until you talked about it.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Sure. I hope you like it.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Yeah, I'm really thinking about using at our work because we do something similar, but it's just our own code and it's not nearly as full-featured as Storybook is.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Ok, well I think you should definitely try it.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Yeah, I think it would be great, especially for pull requests, and being about to build a component in an isolated environment. Alright, well thank you so much for coming on the show.
</li>
</ul>
<h3><font color="#3366FF">Marie</font></h3>
<ul>
<li>
Thank you. It was great. Thanks.
</li>
</ul>
<h3><font color="#3366FF">Adam</font></h3>
<ul>
<li>
Thanks for listening. You can find us online at weboftomorrowpodcast.com and on Twitter at weboftomorrowfm. Be sure to subscribe on your favorite podcast player or on YouTube if you prefer so you don't miss out on any upcoming episodes.
</li>
</ul>
