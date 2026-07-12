---
tags:
  - AI-assisted-development
  - VS-Code
  - coding-tools
  - github
  - technical
  - software
---

AI-Assisted Development with VS Code, Git, and MCP

ChatGPT link:
<https://chatgpt.com/share/67869a13-407c-8013-a97c-437ef9185c27>

RAW Transcript of the meeting:\
\
I want to make sure that you have the same exact tools at your disposal
because I

think that if given some time to experiment with this, you may find them
very, very

valuable. I also want to explain where you should use them and where you
should not

use them.

So one of the things that I want to share with you is an article to
start with.

Right here, I\'ll put it in chat.

And let\'s just kind of go over the basics of this. This is a excellent
discussion

about how developers are actually using AI.

So we have different types of approaches to using AI tools and code
development,

bootstrapers and iterators. We\'re going to take more of the
bootstrapping approach

today, which is to start something from nothing, and then we\'re also
going to talk

a little bit about iteration where we take existing code base and
gradually improve

it. So bootstrapers start with the design a rough concept and use AI to
generate

the initial code base and get a working prototype in hours or days
instead of

weeks. Then you have to do rapid validation and iteration.

Once you get past the bootstrapping phase, you need to be able to work
into daily

development. So daily development means using AI as a pair programmer to
solve

problems, to generate tests and documentations, to be able to refactor
things that

are pain in the ass, to be able to use AI for code completion and
suggestions.

During today\'s chat, we\'re going to use Visual Studio Code. And
hopefully, we can

use both Co -Pilot, which is built into VS Code, if you\'ve got a GitHub
account, as

well as Climb, which is an anthropic -based agentic tool for writing
code as well.

So There are problems with using these tools, and you probably have
experienced or

thought about them a little bit When you use these AI tools They can do
stuff to

lead you down to the path they could march you to do that March you to
the path

of destruction very easily one of the first things that they tend to do
and you

have to watch this is they just sort of infinitely refactor code Or
they\'ll write

everything in one giant module, or they\'ll keep changing things that
you had already

written down. Or additionally, they might take something that was
working, completely

break it and focus on something else. Have you guys ever heard of a
maximizer?

Have you ever heard of that term?

No. Okay. So, here is an example,

a thought experiment. An AI is designed to, is given the,

a very intelligent AI, is given the task of creating paper clips.

The AI will do everything it can possibly do to create paper clips.
That\'s its job,

is is to make paper clips. It\'s going to maximize this.

There\'s a video

game. It\'s not really a game. It\'s a game called Universal Paper
Clips.

You make is that you play the role of an AI. And what happens is
eventually the

AI takes over the entire universe to make paperclips. When you maximize
something,

in this case, making paperclips, it will catabolize everything else. It
will destroy

everything else. It will change everything it possibly can to make
paperclips. And

actually, what\'s happening here is in this sort of AI speed, the AI
tool is

starting to maximize itself for the tasks that you give it at hand. So
part of the

drawback of using these tools is that you have to be able to notice when
it\'s

going off the rails or notice when it\'s optimizing, overly optimizing
something that

you don\'t want it to do. And that\'s the nuance of control for these
tools. And one

of the benefits of being a software engineer or developer with rich
history of

building things is that you will recognize these patterns very early and
stop it

from doing it. It\'s kind of like if you were a farmer and you had
horses to pull

your plow, right? Do you do you just hook the plow up to the horses and
let them

go out of the field on their own or do you have to steer them the entire
time?

stay on the subject. So, I strongly recommend for you to stay on the
subject and

not to deviate into paper clips. Well, we have to get this part
established first

because we\'re going to go directly into building the tool, getting the
tool set up

next.

So, the last bit I want you to be concerned about, I\'ll let you read
the rest of

this article yourself, is that you can create a paradox knowledge about
these using

these tools seniors can you senior developers can use AI to accelerate
what they

already know how to do Junior developers try to use AI to learn what to
do or if

you don\'t and sometimes we\'re all senior or junior in certain things
There might be

subjects that we\'re not familiar with

Pauble I would say that you probably haven\'t Approached a lot of the
continuous

integration and delivery scripting YAML files on GitHub get on GitHub
too much yet

Have you like you know of the concept right? And you know you you worked
and built

a couple of them by hand I\'ve seen your commits with some of the stuff,
but it\'s

not like it\'s the back of your you can\'t just do it easily You have to
think

about it a little bit, right? Exactly But you\'re very experience than
other things.

And so we have to recognize and be honest with ourselves about where we
have

experience and where we don\'t, and make sure we, as the human component
of this AI

-human software development relationship, leverage our strengths
mutually.

All right. So the rest of that article definitely wants you to read
later.

Let\'s start with this. I want all of you To tell me give me a thumbs up
that you

have Visual Studio code installed on your computer. Do you?

Okay

Let\'s Hang on one second

Okay one

moment while I set up my thing here

So I have set up a BitBucket environment right here.

Can you guys get to the BitBucket environment?

It\'s called genwork. It\'s the repo name. It\'s on Arbitbucket
environment.

I\'m going to go ahead and create a gitignore so

we can get flown something.

And then I need you to,

in

your console, in your terminal,

go ahead and\...

Get your latest first copy of this directory, okay, or this recovery
both

Can you please send heading to the server? Yes, of course There you go

What we\'re going to do is all of us are going to, I have the main repo
here,

main, but we\'re going to make some other branches. I want us all to
make a branch

with our first name. We\'re not going to do that by hand. We\'re going
to start by

using our AI tool to start with. That\'s our very first thing. I\'ll let
you,

Actually, does anybody want to just try creating one by hand first as
well?

How about Paw Bowl? I want you to create your repo just in local
terminal.

So get branched. Or you can also use VS Code here.

So, for example, let\'s go into the right directory.

So I want you to start, some of you want you to start Visual Studio Code
in this

directory that you\'ve just cloned or this project you\'ve just cloned.
And I want one

of you to go ahead and create one, your own branch name, so you know how
to do

that, right? Source code, you can create branches here, you can, oops,

right?

Create branch, just like this, if you want to. But I don\'t want all of
you to do

it. We\'re gonna go through this using AI a little bit just to kind of
get you

familiar with where this starts at. So follow along with me to the point
of you

having this locally. So you can see here I\'m on main and we have BS
code open.

Give me a thumbs up when you\'re all there.

And if anybody has a little bit of trouble, let me know, and let\'s walk
through

it. I\'m going to stop my screen shift for a minute.

I\'ll give you until 7 .45. Let\'s give you another two minutes.

You guys still okay?

Yep All right, so thumbs up from everybody. We all have,

we all have VS Code, we all have the Git clone repo.

Who doesn\'t? Bob, are you good?

What\'s up, Joe?

I don\'t plan anything. Can you translate for me, please? The repo
won\'t clone.

It\'s not able to clone.

Okay. Is it maybe a permissions issue? Let\'s look in browser. I can
just see the

report. Can you share your screen? Okay.

Sorry.

Я пытаюсь\... И просто\... Водить что -нибудь.

А. Это ждать для\... Паспорт, наверное? Я не знаю.

Я не знаю, у меня\... Индопст.

Програду закрыть еще раз, упустите, кому?

О,

It\'s done. Ну, вышло. You just have a potato for a computer, that\'s
the only

problem. Okay, no problem. Alright, next thing we need to do. Let me
turn my screen

share back on.

Let\'s see, here we go.

So I need you in the plugins to search for Clyde.

You see it right here?

I want you to install this plugin.

Give me a thumbs up when you got that plugin installed in your
community.

It\'s already installed.

Okay, Sasha, or Pasha, you got it too? Yeah. Go to Climb,

and I need you to click the little gear button, and I need you to go to
the API

provider settings. I want you to change it to Open Router, and we need
to get the

open if router API key.

So the open router API key, I believe either Andre, you were working
with Val or

Val was asking you to get the open router API key available for you?

Is that right? \>\> Yeah, I sent to the API the open router for Anton,

Sasha, Pasha, and me. \>\> Can Can you send it to me?

I need to create one second. So just to kind of give you an idea of what
we\'re

looking at here, this is Open Router. So Open Router is a very fantastic
tool to

abstract token logins for all of the AI providers that are out there. So
it\'s this

company that has been formed, very smart people, they give you access to
all of the

models, every single model possible. See how long this is?

So what their goal is, is to collect people\'s money, skim a little off
the top,

about 10%, charge about 10%, and give you unlimited access to these
models.

Because in most cases, These models give you rate limits, meaning you
can use them

for a certain period of time on the API, and it says you\'ve used
enough, you have

to wait an hour before you can use it again.

And the way it then works is you go to keys, and you just create a key,

and you can then grant these keys to different machines or different
people,

and basically do what happens. Where do I use, where do I put the key
that Andrej

just sent me? I sent you on mail though. Yes, yes, I received it. So you
put the

key, so from the front of Visual Studio Code,

you\'ll have a client robot. Oh, I see, okay, I\'m not there, I\'m not
there, that\'s

fine. I\'ll work with you on this later, I don\'t want to slow them
down. Yep.

So you\'ve got the API key in there. And then the model that you want to
use,

because it reveals all these models here, is Anthropic Cloud 3 .5
Sonnet.

That\'s the one we\'re going to use right now. There are other code
models that also

work just fine. You\'ll see that it\'ll change the way the parameter\'s
here,

because each\-- this tool is designed\-- if you\'re using the API
provider open wrap.

You can also add custom instructions to this if you want to fine -tune
the way it

works but This is just sort of the basics right now So once you\'ve got
this set

up You can then

We\'ll go into a little more of these details later here But just wanted
to show

you there are a lot of boxes that allow you to do things automatically.
So,

for instance, I auto -approve. I\'m going to turn off a lot of these
auto -approve

things here, I think, just so we can see what it can do.

So, I\'m going to turn off auto -approve, but I\'m going to allow it to
read files

and directories on my computer. I\'m going to allow it to edit files.
I\'m going to

allow it to execute commands. I\'m going to allow it to use my web
browser and I\'m

going to allow it to use model context protocol servers. I\'m going to
force a

maximum of 20 requests before it pauses and stops and says, \"Are you
sure that you

want to let this thing continue?\" Because it could take over
everything. I\'ve

actually told it to do stuff and it kind of just started doing things
and you\'ve

got to be careful. this is a very powerful tool did you did you
understand sasha

do you understand what erin says or do you want to pause yes yes i
understand okay

just again please participate say yes no raise your hand stop let\'s
let\'s participate

because erin is really spilling his guts out do you understand the
expression

spilling your guts out Открывает вам душу и нужна обратная связь,

которую тяжело получить. Или моргните глазом, или поднимите руку. Ну,
просто\... Пока

что мы\... Ну, Эрн показывает то, что мы сами попробовали. Ну, хорошо,
тогда просто\...

Ок, просто покажите палец, потому что человек\... Открывает вам душу.
Надо, чтобы была

какая -то Okay, moving on. - Okay, so what I\'m going to do is I ask,

because we\'ve already started in a Git repo, do you see how if I click
on the

source code control tab in VS Code, we can see my first control item on
main.

I\'m going to be a little lazy and I\'m gonna tell Client to my first
instruction.

I would like you to create a working branch for me in this repo. Can you
call it

the errandev branch?

I\'m going to let it do its thing.

It\'s going to give an action of what it\'s going to say. I need to
create a new

branch and give it get repository. Since this is a git operation that
could affect

the repository state, I should use execute command with requires
approval to set to

true. I\'ll first check to see if we\'re going to get repository then
create the

branch. I\'m going to go ahead and let it run the command. It\'s going
to check

that. Great, we\'ve confirmed we\'re going to get repository and
currently in main

branch. Now we can create the checkout and branch called Aaron Dev,
okay, done.

It\'s very simple. I mean, this is stuff that we could just type right
And it says

tasks completed From this point forward in order to save time with going
to auto

-approve all these things and I want you to note the cost We sense it 52
,000

tokens. We got back 271 tokens in this action cost 8 cents to operate.

So, all of us here know how to use Git, right?

Does everybody in QA comfortable with Git right now?

Your opinion?

Not sure. Not sure. Actually, I think nobody from QA used Git.

Other than just to see what\... \>\> Right,

right. So, my next question is, if we were to consider the people that I
talked

about in that article about the hard truths about this, the 70 %
problem,

what types of people are QA engineers.

They\'re juniors trying to learn how to use what to do with AI.

And here\'s the thing, is that this tool can provide a learning pattern
to help

these people become better at this. If they just simply focus their
efforts on using

These tools for simple operations that they\'re unfamiliar with What
you\'ll find is is

that by doing it a lot repetition tends to give you if you\'re paying
attention

repetition tends to give you practice in it, so It\'s very handy to have
so Go back

to this now If I look at our code look at our branch we can see that
I\'m on

here in depth, right? I have not published this yet. I could just as
easily publish

it here. I could type git push origin main. Or,

you know, or Aaron Devin. Right? There\'s multiple ways to do this.

I\'m going to go ahead and just have client inside of this thing. Even
though it

says it\'s task completed, I\'m going to say

Please push this back to origin.

I\'m going to approve it.

I\'m going to give it my credentials

It\'s now pushing it back to bid bucket So I want you to do that same
thing for

your git repos not using Git commands manually unless you\'re Pasha
Pasha you have a

choice to do it by hand or the other one, and there\'s a reason I\'m
giving you a

choice. So when we\'re done here, we should be able to look in here,

and I can see everybody.

So Andre, Anton, so Sasha, your branch is up there.

Does anybody want to share their screen while they\'re doing it or have
any questions

about what we\'re doing this? So far so good.

For me, I have some proteins. Yeah, but at MAD, if I\'m being honest,

I\'ve created my branch before you asked me to use the eye, so I\'m
gonna create a

simple commit with the clawing distance. This is exciting. This is what
I want you

to do. You don\'t have to stay in lockstep with me. Jumping ahead.
Don\'t jump too

far ahead, but I want you to play with it.

We\'re gonna do some merges later is what we\'re gonna do.

What do you think? You got it working It works for me,

but it\'s saying that there\'s error In bits and output from terminal
the quiet is

very your screen?

How old is VS Code?

1 .9 to 6,

quite new. That\'s you\'ve got point. Oh, I\'ve got point to

Which shell are you using

Actually, I don\'t know what is What\'s here? So if you were it says
could be should

hold if P Terminal Select Default Profile. Try doing that.

Ctrl +Shift +P.

Just basically open up the command terminal.

I\'ll show you the same thing. Configure Terminal Settings and then you
scroll to

Default right

there. Oh, I guess I\'m not sharing my screen. So, press Ctrl +Shift +P.

Hmm, it opens\... I think it\'s not what\'s supposed\... Oh, you\'ve got
something else

going on. Snag it. Just open your command terminal.

No, the command terminal in VS Code. Oh, this one?

Yep. Well, no, not that one.

The \-- I forget how you \-- I just press Ctrl +Shift +P. It\'s usually
what I do to

run it. Go to View, do Command +Palette.

Very first item. Out there and then type in \@feature.

I\'ll paste it in the chat here.

You want to go to that portion of it.

View command palette backspace to carry it out of there If you\'re rid
of the care

at first hit

enter Yep

I don\'t know, that\'s not working right.

Andre, do you push Visual Studio code onto people\'s computers or do
this allow

people to\...

They can install Visual Studio on the computer itself. \>\> Okay.

Instead of trying to go directly to it, backspace that all off and just
instead use

the carat, type in the carat and then type config. Try that.

\>\> Type config. \>\> Что -то случилось, у тебя есть все контроли там,
а потом что

-то\... Да, просто нажимай в интернете прямо там.

Я не знаю. Визуальный студий у тебя просто бежит на компьютере.
Наверное, ты бежит

на компьютере. Это все твои ошибки.

Попробуй

Саша, у тебя получилось? Что -то сделано? Да, у меня все отлично. Не
делает,

но он не читает вывод консоли, не может прочитать консоли. С одну
сторону.

It\'s one -way communication from C -line to terminal.

Yeah, you need to be able to get information And then this will not work
at all

without this for you.

You could just try updating. Go to\... I think if you just go to health
and then

download available update it might work okay let\'s let\'s do it quick
just it should

take a second go to help

check the best chip update okay the other thing you can try doing is
just closing

VS code once and opening it against the times yeah

\>\> I have error with creating new branch too.

\>\> Can you share your screen with Andre?

So it looks like you already have a branch up there.

\>\> When I try, for example, when I try to create a new branch,

it\'s in error. API failed.

So, is it possible that\... I will come back in a but I need to regroup
my videos.

\- Okay, we\'ll see you in a minute. Is it possible that we\'re running
into network

VPN sanction problems, Andre?

\- Huh, maybe, one second.

\- Anton, do you still have access to

Yeah, okay. My mind works just fine. Mine works as well.

Sasha, how about you? Is it working good? Still working for you? Yeah,
well,

okay. Alright. While we\'re waiting for Pavel to reboot,

I want you to, Let\'s talk about what sort of simple project we want to
play with.

What are we going to make?

Why don\'t we make what we have to make?

Why do we need to make a simple project?

So I think that we could go up to it including that.

How would we do that? Val, don\'t you have a very good document that was
just

written describing all this?

\- Yes, I circulated this document to Pavel and Andre.

\- Okay, so here\'s what we\'re going to\-- - With an updated document.
And So the three

of you now, Aaron, Andre, and Pavel, have the same document. You can
choose to do

whatever you want with it.

So while Pavel\'s coming back, I\'m going to share my screen,

There it is.

I guess it would be in.

Okay.

I don\'t know why I can\'t copy this whole thing.

I\'m on.

Control + A should work. Want it?

No.

It\'s because it\'s in read -only mode, so it\'s hard to get the cursor
in the right

spot.

Why is this so difficult?

Well, fine. We\'ll do it this way.

Okay, got a copy of it.

So what we\'ll do here is

I\'m gonna make a new file. I\'m gonna call our new folder in structure.
I\'m going

to call it docs.

I\'m going to go into docs.

And I\'m going to say,

I

was going to make a directory called project init. And I\'m going to
make the thing

called the

pipeline problem. And I\'m just going to copy and paste that entire
document right

into there, OK? So I\'m going to save that. So now I have in my docs
folder,

I have a thing. We have a git ignore. And I haven\'t published any
changes, because

I don\'t need to do anything yet. But I\'m working on my project.

Actually, it\'s the architectural proposal. Let\'s\-- \[VIDEO PLAYBACK\]

So please read all the docs and let\'s put together a set of development
guidelines

based on goals, use best development processes, guidelines, and hiking.

So it\'s going to look at all the docs.

It\'s going to find that one in there. It\'s going to ingest it.

And What we\'re going to do is we\'re going to create an initial file
called

\"clinrules .clinrules\". \".clinrules\" is a special file that when you
save it and

commit it to the branch or to your repository, it will read that and use
that as

a set of instructions every time you work on this project.

project.

So, if we take a look at climb rules, let\'s just sort of

cheek at it here.

It\'s also modifying the \"get ignored\" for us as well.

So let\'s take a look at the

guidelines, so core development guidelines, single source of truth,
infrastructure is

code,

kind of talking about how we\'re trying to potentially structure the
project, there\'s

a lot of detail in here. It is up to us to decide whether this detail is
required

or should exist in here. Remember that this will always influence the
way this code

works now if this file is inherent.

So we think about version selections and things like that, testing
requirements,

all sorts of stuff. Like it\'s talking about all these pieces in here.
This is all

the guidelines that it\'s interpreted from what Valve had written right
here trying to

put something together, right? Because isn\'t this basically a set of
requirement

specifications in a way or kind of describing the problem that we\'re
trying to do?

Because if you look down here, we\'re looking at parameterization and
version

selection. We\'re talking about, it\'s

at Taking it for granted that this is what we wanted to write remember
what I said

about the paperclip maximizer Is this what we wanted to do is my
question to you

I think a possible way

Say that again, I Think it\'s possible a way to organize all of our
pipelines.

\>\> Right.

One of the things that I feel is probably important is that I think this
is way

too detailed, actually.

And so what we can do is we can revise it. So in the same session here,
even

though it\'s told us that here\'s the changes, right, we can see the
changes in this

file too. I\'m going to say\...

So, this is, can you guys read that prompt right there, what I\'ve
changed? I think

the guidelines will never know. I think there is some, uh, display
capture panel,

and, uh, covers, you know. There we go. I think the guidelines that you
have are a

bit too detailed. They are too forward -reaching and will cause our
approach to be

brittle and not agile, but start with absolute basics. I believe we
should develop a

small MVP approach to this that demonstrates the approach with minimal
distractions or

confusion.

So just take your inner thoughts when you read it and just be honest
with yourself

so I\'m gonna oops let me go back to that so do you see how I can go I
can

click start new task and it will forget everything or I can go back into
a task

and remember where I was at last so I\'m not gonna finish this task up
until I

give it correction here

I understand the concern, the current guidelines are too comprehensive,
it might be

overwhelming, potentially hindering agility. Let\'s create a minimal,
focused MVP

approach that demonstrates the core concepts from the pipeline
documentation. I\'ll

revise guidelines to be more concise and focus on essential practices.

So let\'s review what this looks like now.

Our goal is to create a simple flexible iso build process that maintains
quality,

store all code, and get blah blah blah. So

Let\'s start a new task and let\'s experiment for a minute.

Please put together a prototype pipeline for Bitbucket that would
demonstrate our

guidelines and approach to a template project

So read this is where I\'m going to show you something new here read all
the ads

when I hit the act sign You see how it says add folder at file. We\'re
including

context here Read all the docs

to ensure we\'re building accordingly.

This tool is context aware. If it sees that you have a tab open, it\'s
going to

read the content in the tab too, by the way.

So it\'s reading the docs again in a new session.

So it\'s going to start creating some, looks like it\'s going to create
some YAML

pipelines to create some things. So Bitbucket pipelines and a build
config YAML.

So now what we have is it\'s storing some of these files.

I\'m just generating some content to show you the flow and process of
communicating

with this right now. We\'re going to do something interesting coming up
here in a

second.

Created both the required files that demonstrate our pipeline approach.

So it\'s telling us how to use this.

Now, I\'m going to finally say, please update our docs. So\--

please update our docs including a readme so people new to this process
or even QA

will begin to understand our approach.

So we\'re going to get to the bare minimum of a code repo that\'s going
to have

some stuff in it. We\'re going to have some pipelines, we\'re going
We\'re gonna have

some documentation We\'re gonna have a little bit of just example pieces
of code in

here nothing special yet We\'re just like that document. I said the
seventy percent.

We\'re just instant. We\'re getting something started This is not a
finished product.

Okay,

And since I would typically be more careful in actually review this
myself,

including what it described, that takes longer than what we have during
this session

here. We\'re going to assume that it\'s okay.

Let\'s let it finish writing the guides.

Okay. And the last bit is that I don\'t really feel like writing a git
commit and

committing all these changes and doing all that work because it\'s a
bunch of git

faffery that I don\'t want to deal with. So I\'m just going to say
please commit all

your with a description, with a good description of the changes.

And it\'s going to go ahead and commit this to my Git repo, to the Git
repo,

and it\'s going to create a detailed commit message of what happened.

Instead of changes or refactoring or work, It\'s actually a really good
commit message

that describes what changed.

I\'m going to pause here for a minute and ask you a question. What\'s
the danger of

doing what we just did? What\'s the number one problem with what we just
did?

From a developer understanding what the hell happened perspective.

I guess it kind of attracts a lot of things, but I don\'t know if it\'s
really a

problem. The problem for me is that when you kind of click lots of auto
-proof

checkboxes, it can lead you somewhere to the long -term client.

It can lead you to doom. Right. So maybe instead of 20 steps, it\'s like
let it do

five or three. Like one, two, three, bang, and stop, right? Another
thing.

go, \"Aaron, what did you do?\" And I\'m going to be like, \"Well, you
see, my friend

Klein wrote all this stuff for me, and I\'m not really sure.\" Like,
that\'s the

problem, right? So, we have to be sure to limit our changes to human
-sized changes.

It is extremely easy to just overindulge in this tool and make changes
that Проблема

на то, что ты будешь нормально помещать или помещать в кодбейсе.

Как часто ты делаешь сквозь коммит? Саша, ты делаешь сквозь коммит перед
коммитом,

или ты просто поставил много сериализированных коммитов в репо?

Я покажу Антон, если вы хотите просто поговорить о Брошене.

Ну, спрашиваю, Он спрашивает, сквошишь ли ты комит и перед тем, как
мерзнуть?

Не совсем понял, что случилось с кого? В общем, идея в том, что это,
например, если

напрямую в транк комитить, то это не имеет смысла, но можно, например,
сделать ветку,

сделать там в этой ветке 10 комитов и перед тем, как мерзить в транк,
эти 10

комитов собрать в один, чтобы легче, ну не завтра реакция историй в
гитаре.

Ну я бы оставил комиты как есть, ну там более понятно мне кажется,

что хотел человек сделать, ну именно по отдельности, ну мы как бы с
гитом немного

еще работаем поэтому. Ну да,

альтернерс says that he would leave the history as is. He also mentions
that we

probably lack lots of experience in it. From my personal experience,

it depends. If I work in a feature in a branch and commit history seems
to be

clear, then I would merge without squashing. But if I have lots of
little commits

where I do small incremental changes like update the bucket pipelines
update bucket

pipelines I would squash that like okay like five subsequent update
bucket pipelines

commit into one okay

so I want to talk a little well I don\'t want to get too far ahead of
myself but

we\'re going to talk about how to affect those things in just a minute
here too And

now, finally, if we go over to, let\'s see,

where\'s Bitbucket?

Oops, that\'s not the right Bitbucket. There it is.

So we should see Aaron Dev, we should see some content in here. We talk
about the

ISO build pipeline,

docs folder, QA guide, so forth. We can start reading about things in
here.

So, I don\'t know if pipelines are created yet in here yet,

but you know,

I think you should merge your branches into main and then it\'ll
probably do that.

So let\'s do it the lazy way.

Please merge my branch into main, push it to remote, and close my branch
out.

It\'s a lot easier than having to actually click on stuff I\'ve found.

It\'s checking to make sure mains up to date. It\'s going to pollate as
changes. I\'ve

got to type my key here.

Already up to date.

Go ahead and merge.

Oh look there\'s a problem

sometimes it has problems so

it doesn\'t have I don\'t have less on my machine just FYI

so here we are using fast forward merging emerging erin dev, pushing
from origin

back to main, whoops. Are you on Linux? Yeah. What do you use?

I use Arch.

I use Arch by the way. What\'s that? I use Arch by the way. Oh yeah.

That\'s the meme, right? Yeah, yeah.

So do you see where I allowed it to proceed before typing my credentials
and it

says I see the push command is still running I\'ll wait for the
passphrase once the

user enters it. I\'ll proceed with the leading

I now have to tell it I\'m ready for it to continue

It\'s like working with somebody like side -by -side is really what it
is well it\'s

right it\'s doing the work I\'m just sort of the leaning over the
shoulder and

telling what to do

so it deleted my air and depth branch they committed it to Maine and so
now when

we go back over to here

There\'s main with our stuff now. I want you guys

To

Synchronize your branches to me with the code read with with client Only
don\'t want

you guys to do it. Who\'s gonna do it first

on her? Want to do it Anton? Yeah, Okay,

I want you guys to follow along with that tongue

So

so let\'s let\'s make sure that you\'re before you hit go on that
prompt. Let\'s talk

about your prompts a little bit Yeah, so I\'m currently on my bridge So
I wanted to

pull the remote changes for me

into my my local branch correct You forget please Yeah I\'ll let it in
the end.

I Actually find that saying please and thank you actually does help
Sasha The other

thing you can do is Exclamation points and being excited will get it
excited too.

It\'ll actually work harder if you\'re if you\'re nice to it I\'ve
noticed which

is really funny to think about

Yeah, when our digital overload so observe all the data, yeah

So it\'s asking to run that certain commands that will always are hard
-coded to to

give approval so

run that command so figured out that you\'re running Windows PowerShell
because it

couldn\'t use those commands.

Yeah by the way before today I didn\'t know that you can combine with
the sync

command. Oh you did? Yeah I knew about this one and it never worked for
me because

of the PowerShell on Windows not that Yep. Didn\'t know how to do it in
Windows.

Yep.

I had to manually exit the window. Yeah, I saw that.

So it\'s pulling and pushing is what it\'s doing right now, mm -hmm.

There we go.

So let\'s look at your code there There we go.

Yeah

Can everybody else do that so we can be all synchronized I\'ll do it as
well.

Are you working on main branch or your branch? I\'m on my own. I see you
have a

JavaScript file in there. So everybody else needs to make sure they\'re
up to date

too. Let\'s use the code, let\'s use the tool rather than\... I know
there\'s a joke I

like to say is that sometimes it feels like you\'re typing with oven
mitts on, you

know, oven mitts to pick hot things out of the oven. And trying to type
with oven

mitts is very difficult because you can basically slap your keyboard and
not really

do anything useful.

Sometimes these tools feel a bit like coding with oven mitts and you
need to

recognize when that\'s the case if it doesn\'t help you. But you also
have to

recognize that it still can be helpful, so you have to, you know, have
the nuances

between the two.

So what have we done so far?

Um, Pavel, can you describe what it feels like we\'ve gone through that
so far.

What we\'ve done, just to try to be an automatic tool client,

and to

make

some task to automate some

general general, I would say, general tasks. Yep. For example, to
organize,

you recreate a trepa.

I think it will be quite useful if you need to at least to create a
project

structure. Correct. Correct. So,

shall we continue? Can this plug -in work with self -hosted open source
large language

models? I have a server in my apartment. Yeah, yeah. I\'ll make your
button. I tried

it with

is it good though no it\'s kind of terrible i\'m small i don\'t have a
good enough

gpu if i had like an nvidia a1000 gpu you know like the the ten thousand
dollar

gpu hosted and also used the central heating in my house um then i think
it would

actually be fine because i\'ve used it against um uh llama three Llama 3
.2,

the 192 billion, the very large model out paying credits for,

you know, you can actually try it right there, you can experiment. So if
you stick

it, stay on open router, and instead of clawed sonnet, so click away
from that,

change that type, type Llama.

So you can pick one of the big ones like is it is it go up to llama
it\'s the

405 3 .1 405 billion not

that one click does not support image does not work computer you but try
it Hit

done,

start a new task,

say describe what we\'ve got so far in my codebase.

So

what we\'re going to do is we\'re going to see if

it failed. yeah try hit resume task and see if it works maybe it\'ll so

that may not work so let\'s try a different model use quen

qw quen to 72 billion instruct

or or 2 .5 coder.

There you go, right there. It\'s done on that one.

Okay, alright.

So

I want you to notice the cost when it\'s done. It\'s almost free. clean
is almost 50

times cheaper than Claude to operate.

So you have all these different agents at your disposal to be able to
use including

local ones if we if you build a big enough water heater to run.

Okay, so for now, go back to Claude for now, just because it\'s pretty
much one of

the better ones. 3 .5\'s on it, just scroll down, it should be.

There you go, okay, all right. So the next thing that we\'re gonna do,
I\'m gonna

switch back to my screen share.

There is very interestingly a thing called MCP. You see it right there
model context

protocol Model context protocol is an open standard to allow a language
model to

interact with tools so tools is When we saw

Let\'s see if we can find here.

I don\'t know if it said it. I don\'t know if you caught it earlier. But
there was

a thing where it said, I will use so and so. And it said, like, a file
name

underscores something. That was a model context protocol tool.

Let me just do it this Go look in JBL Jira to see if you can find any
issues

Any

I can use the okay, so we don\'t want to use prima so hang on I might
need it.

I might have to fix something One minute, please

There it is.

I need to close and open Claude for this to work, because I made a
change, or

code I should say.

Go back to our last command that we did, I\'m

I\'m just gonna start a new task.

So it\'s finding a bunch of work in JIRA that might exist.

So it\'s found some JIRA projects that might exist in here. - How does
it know Where

did you is and what what\'s the correct URL for the jura? This is the
tool So

we\'ve created what\'s called a model context protocol server That
presents a unified

tool set to the language model

It uses these tools to then query Jira,

update Jira, edit it, and so forth.

It presents these tools to any of the code, the models. Now, Anthropic,
Claude,

is configured to know how to use model context protocol very clearly.

However, the Client plugin injects commands into any of the calls to the
other

language models, such as Lama or OpenAI or whatever, and also gives it
the ability

to ask how to use these tools. Let\'s look and see what it actually
said. I\'ll use

the JVL Jura MCP server to search for initiative issues. Since
initiative issues are

prefixed with IP -, I can use the search Jura issues tool. You see it,

how it\'s underscores here? With a JQL query to find these.

looking at this environment details, this appears to be a project focus
on

development pipelines and QA processes. Let me look at the initiatives.

Let me get more details about IP693 pipeline automations, since it\'s
most directly

related. So it\'s getting additional issue data into here. And then
it\'s kind of

looking at a couple different items trying to figure out what\'s going
on. So we can

see here pipeline automations while currently in concept phase and
lacking detail

description this initiative Especially specifically focus on pipeline
automation is

assigned to Andre Andre Hmm, how would we update IP 693 from here?

Okay, and some things right or if you have a model context protocol
server and you

have this thing here

Help Andre know what\'s going on with IP693 by updating the description
of the

initiative. I\'ll update the description of IP693 to provide clear
direction for the

pipeline automations initiative.

It\'s now going to read the work that we\'ve done so far and it\'s going
to update

the docs with a better description.

So if we go over to Jira,

sorry.

It\'s now updated the description of the initiative for this in here.
Just the same

as I\'ve done the initiative, we could start describing stories or even
read stories

as well.

So, Sasha, if you have user stories underneath a project or a feature or
something

like that that you need to work on, you could use this tool to read the
user

story and begin working on it, updating the issue state and everything
else and

allow it to go through and work with you during this process. If you
need to do

most of the coding yourself because that\'s what we\'re comfortable
doing, this tool

can simply be the interface to help you work with JIRA to deal with the
paperwork,

so to speak, of working on an item.

Let me explain how model context protocol works for just a minute.

So there\'s a directory in here under my documents folder called client
and then

underneath that there\'s a thing called MCP and we can see here that I
have a

Confluence Cloud MCP, a Jira Cloud MCP and a GitHub MCP.

We\'re using Jira Cloud MCP and you can see here that we it\'s based on
node so we

can see if we enter Let\'s take a look here.

Sorry, my screen is too big.

We can see we have a client called GiraClient. I have handlers that
I\'ve created

for looking at, like, scrum boards or, you know, sprint boards. I have
one,

a handler for looking at issues. I have a handler for dealing with
projects. And I

have a handler for search. These two here, the schemas, present the
schemas for the

handlers back to the language model and then we have a type index and a
text

processing utility to be able to convert the last in text formatting
back to just

plain markdown text for the model to understand. Did you wrote it or is
it like a

community? I wrote it with Klein, actually actually Clang wrote it. I
asked Clang to

create one and then I guided it through because what it first did is it
created a

juroclient .js file and everything was in it which of course we all know
is a

terrible idea so I said no we need to modularize this let\'s make a
handlers and

schemas and some other stuff and broke it out and refactored it and kept
I\'ve just

been improving it over time and I\'ve been using the process of this to
even push

it back up to GitHub. So in GitHub, let me show you what this looks
like.

So here is the Jira Cloud MCP. It\'s a little bit.

And the documentation is written by a client

The all the parameters that what it can do is all written by it as well.
I really

just provided guidance for it

So this is based in typescript and runs as just a big type script tool
basically

so My point is is that It\'s pretty powerful when you start thinking
about how does

this development environment actually work behind the scenes to get
information and

start grabbing stuff. You could just as easily build a Model Context
Protocol Server.

Let\'s do that for a minute here. I want to start a new project,

so I\'m going to close out Visual Studio for code. I\'m going to go back
to

projects, JBL, JVL, and I\'m gonna make a

Bitbucket MCP Okay

Actually, let\'s do one even better than that. We won\'t just make a
directory just

while I\'m thinking about it here

Let\'s go into BitBucket. Where

would we want to make a model context protocol server posted in our Git
repo under

Tools maybe?

Yeah, okay

See projects tools. Let\'s create a new repository. We\'ll call it MCP
AI MCP

main tools

So let\'s go ahead and clone this so I\'m just kind of giving you an
idea of how

this starts out again

So let\'s clone that

So we know that the MCP directory where we actually do work,

where we actually use them for Claude is under, on my computer at least,
is under

Documents,

Client, MCP, right?

So it\'s in this folder.

So we\'re going to give it some instructions.

So it\'s going to probably use a TypeScript template. There\'s actually
a template

project style.

So it\'s going to run the MCP creation tool, which is here.

And what it\'s going to do is it knows that npm node is already on here.
I have

npx, I have like node 22, something like that on here. It\'s It\'s gonna
install a

set of modules.

So it\'s gonna correct some names here \'cause I renamed itself. It had
made some

assumptions on names. And it\'s gonna take the template MCP server,
which is out on

modelcontactprotocol .io, and it\'s going to now start to combine these
things together.

It already has an knowledge of Bitfucket itself and the API calls
required for it

and it already has access to some node modules that allow us to have
just we just

grab the module for for Bitfucket and start using that instead we don\'t
have the

right stuff from scratch right so

it\'s going to correct some text script errors and some Java problems
that it looks

like it\'s trying to work out because it\'s just using IntelliSense,
it\'s using linting

as it writes it, and so it\'s looking at the lint output and making
these changes

for us.

When it scrolls really fast it\'s using diffs and prompt caching, so it
doesn\'t have

to consume as many tokens.

So it\'s now testing it. It\'s trying to run the server. So now it\'s
asking for my

Bitbucket username, an application password, and then the app for needs
these

permissions, repositories, and pull requests. From this point forward, I
would continue

to refine this tool by using it, testing it, implementing it, and
committing code.

So once we have something like this, you could add this to the MCP set
of tools

that you\'ve got on your computer that client can use. And it can
interact with

BitBucket directly if it needs to. I mean, a lot of this stuff just
happens in the

Git repo. You don\'t have to\-- you can just use Git commands with\--

It\'s that it\'s using a set of tools to do it with, interacting with
any system you

want.

So, for example, if you have the local gaming server and there are
endpoints to hit

against the local gaming server, you could create a model context
protocol server

that could talk to an LGS, and then interrogate or talk to the LGS and
invoke

things against it.

You could then write new modules based on what LGS responds against, for
example.

So I\'m just trying to crack open the door.

I\'m strongly encouraging you to try to use this tool. We\'ve got just
like five

minutes left on the

to try to use\--to just experiment with this.

Try creating some projects. You\'re going to go back and forth. There\'s
a learning

curve associated with this. Part of it is knowing when to stop it and
when to

break it up and giving it good, best practices on how to code things.
But the fact

that you can create these context protocol servers is amazing. There\'s
probably a

whole separate conversation I could teach you about how MCP works and
where you

could use it at.

Can you imagine the type of scenarios where if you\'re using this
against a code

base and you wanted to just build a build of something, if you had \--
if it was

all in Jenkins, for example, you might have to click on the web page.
And this

thing can click on web pages and stuff too, don\'t get me wrong. But if
you have

it all in the Git repo, you could have it build any sort of build
pipeline you

want and then just put it in a branch and be done. If you already know
what

you\'re doing, you don\'t have to use it for everything. It\'s, like I
said, don\'t put

on the oven mitts and start doing stuff when you can easily do it
yourself faster.

But be creative in thinking about how this actually can accelerate your
work.

So the homework I\'m going to give you guys for this is I don\'t want
you to start

writing a bunch of crazy AI -generated code against their code base and
committing

it. That probably isn\'t a good first step. But what I would like you to
try to do

is to use a set of prompts with this to open a code base from, yet
probably from

Bitbucket or move something into Bitbucket that you want to and do a
little bit of

exploration with it with the tool. So have it read the code base. Try
reading

portions of the code base. You\'re going to see that the size of a code
base for a

module or for a component or something like that, the bigger it gets,
the more

stuff is pushed into a giant monolithic application, the more difficult
it is for

these tools to provide value. So you also can consider that if you\'re a
mere

mortal, a regular human, it\'s very difficult to read large code bases
and understand

what you\'re working on as well. So, it\'s kind of a bit of do the
things that you

would do if you were writing code in an ideal fashion. So when you
take\--when you

open up, let\'s say if LGS is a really big code base,

there\'s tons and tons\--you know, hundreds of files, it\'s all over the
place, that\'s

actually a great place to start because these tools can still help you
map out what

it is. And just start writing documentation for it until it makes sense
and start

documenting what pieces might be missing.

That\'s\--I would recommend you try to take a\--some code that you\'re
familiar with,

that you already understand how it works. You know, Sasha, for you, it
might be

something in the Omni Framework. Sasha, for you, I\'m picking an LGS,
Anton, RGS,

I guess. I don\'t know. Andre, you may have some build scripts or other
pipeline

stuff that\'s happening to be able to push things out to the, you know,
to

Kubernetes, for example. Use these tools to do some analysis and
understanding of

what your code bases are and start there. And maybe in a week, we can
come back

and I would love to see a docs folder in some of the Git repos that is
using

some of these techniques to understand what is happening to your code
bases.

This meeting has been recorded as you know. I have recording available
to you.

I will provide you with the raw transcript if you want to use AI for
yourself,

you could translate it, you could drill down on it.

If you want me to use ChargeGPT Pro for transcript or any drill downs or
any

suggestions, I\'m happy to do it. But in the meantime, I\'ll provide the
raw

transcript.

Aaron, would you please schedule a meeting in one of those windows that
I\'ve

reserved with you? Sure. Directly with the guys and include me as an
option.

Yep. And then I want you to discuss amongst yourself if there\'s
interest in focusing

specifically on model context protocol. I think I could sit down with an
hour for

you guys with you guys and kind of just explain how it works. As far as
I know,

I\'m only a half a step ahead of you guys, I would love it for you to be
an

expert in it rather than me and I think you might find it very, very
useful for

some of these tools that we\'re talking about here. I\'m going to leave
us with a

link here, give me one second,

here we go,

go visit this page as a starting point, and you\'ll recognize the
TypeScript template

that I was using to build a MCP for Bitbucket starting to.

There\'s a Python TypeScript and Kotlin SDK template available for these
things.

From a corporate direction and from a corporate perspective we are
looking for a

leader on this subject, somebody who would learn it better than Aaron
knows or more

than Aaron knows and lead us into that direction. We identify it as an
area

for growth

For that individual and by growth, I mean obviously financially

So yeah anybody who wants to take a lead on this and embrace it and
teach us and

Move us in that direction We\'re ready to compensate for it.

I I\'ve been doing some cost modeling for these tools and developers who
could use

these competently within that 70 % range that we were talking about.

There is a potential savings of 20 hours a month at least for this
middle

Sir developer so 10 10 developers 200 hours per per month right So two
thousand two

thousand hours per year. That\'s roughly one employee per year That\'s
good.

That\'s two thousand hours Right, so a company of ten people could shave
off one

employee

Or acts like they\'ve added a second another or scale up. Yeah, of
course.

Yeah We are looking to scale up. So for us, it\'s a scale up thing And
that\'s the

minimum bottom case Like that\'s minimum usage. That\'s using it as a as
a as an

errand boy for Committing my code or for looking up to your issues,

basic stuff. - For me, I\'ll tell you, I used to have one personal
assistant and one

receptionist. I got rid of both. I am more efficient.

All right, thank you very much. Again, Aaron, another meeting next week
we will take

our company into that direction so I strongly recommend for you to excel
if you

have questions or ideas or anything I\'m happy to talk about this stuff
just hit me

up on teams and enthusiastic about it I am enthusiastic about it Aaron
do you have

another 10 minutes? Yeah. Okay, so I would like to stay with Andre and
you.

Okay. I\'m terminating the recording.
