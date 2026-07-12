---
tags:
  - performance-analysis
  - testing
  - project-meeting
  - strategy
  - hardware
  - omni
---

FP-7 performance analysis - January 13, 2025

Transcript:\
Okay, good morning everyone

Welcome back. I hope everybody had a good holiday refreshed

We want to talk today about test results of the FR seven

Sample CPU board that was sent from China to Minsk and I understand that
Mitri

Handoff and Alexander Beratka ran a number of tests on it and conveyed
these results

to Lena and my understanding that Lena and Dima had a conversation and
they have

certain opinions that are formed. Keep in mind that

Our goal as a company is to leave

the Flex -S cabinet for street operation mainly,

right now we\'re using it for casino operation, but our goal is to
develop Flex -C

With stronger hardware with more robust hardware The question is can FR7
solution do

the job right now at the level of the games that we\'re trying to
develop today not

Not looking much in the future but today

And if the result is marginal, then my next question would be to Gennady
Perry and

see if the current hardware could be slightly improved and at what cost.

So let\'s start with recapping the test results,

then interpret those test results in what it really means for visual
effects of

games that we\'re trying to produce then analyze if this is enough or
not then if

it\'s not enough let\'s see if there is an immediate solution and if
that is not

enough then let\'s pause and think of What could be done in the meantime
because we

must release The future full pause games a game future full or future
full pause

game out in the market in June in

The market in September, but in the lab in June and this game is going
to be

released on the Omni platform. So I think this introduction to the
subject is

thorough enough for us to start the meeting. I\'m gonna let Sasha
Biratka speak

first. Tell us about the test results or the methodology that was used
in the test

in testing the FR7 hardware.

Ну,

принцип такой. Дима создал сцену с большим количеством видео.

Количество видео, по -моему, было где -то 10 или 11. 13 изначально
видео.

И

Сразу первый тест, который я запустил со всеми 13 видео, получил где -то
примерно 5

флпс. Но это большие видео, все видео большого размера, кроме на 1 .4,

которые на VDK, они такие же большие, но только сжатые до половины
FullHD.

После этого я Удалил часть видео половину где -то видео,

у меня сейчас запущено где -то 4 видео больших и 2 видео на видейке.

При этом на экране изображение, я снимал на фотоаппарат видео,

есть оно, можно закинуть, если кто хочет посмотреть это качество видео
то есть там в

районе где -то до 20 фпс ну визуально конечно это не склеша там очень
красиво он по

крайней мере терпимо то есть если в некоторых моментах например при
каком -то бонусе

у нас вдруг чуть -чуть просядут фпс до такого уровня то может быть
возможно на этом

можно закрыть глаза То есть, мы приблизились до границы
производительности именно по

видео для этого

борда.

running videos in HD resolution. Dima, correct me if I\'m wrong.

And Alexander fed these videos simultaneously through FP7 hardware and
that practically

choked the hardware to a grinding halt.

And so then the methodology was to keep on subtracting or reducing
number of

simultaneously running videos to the point where he found a threshold of
tolerable.

The definition of tolerable is a video is running at approximately 20
frames per

second. Realizing the 20 frames per second as obviously not the best we
can do,

but he defines it as a threshold of tolerable.

I don\'t define it as threshold of tolerable, I\'m sure Lena doesn\'t
define it either,

it will not be a satisfactory game for us, but regardless, this is the
methodology

of testing And at the threshold of tolerable as defined by Aleksandar
Duratka,

he managed to run seven simultaneous HD videos plus two half screens on
VDAC.

If I misunderstood something or mistranslated something, please correct
me.

Is it true anymore? Because I thought it was 7 at all for 3 monitors,
topper,

main screen and VDEC.

Yes, first of all, on VDEC technically we are repacking the full HD
video,

it\'s not half, it\'s just visually half, but the actual file is full
HD. Because we

have a full HD monitor on VDEC. Second of all, I would like to add a
little bit

about the seen we\'ve been using for testing, because the scene also
helps some spine

objects. And spine objects demonstrate quite nice for functional.

They\'ve been nice and smooth without visual delays. Same time when we
have delays in

video files.

So this is another interesting point of their commission. So you\'re
saying we can

increase the number of spine objects while creating great visual
presentation,

however reducing the load on the processor. Yes, I think 200 degrees.

We need to think how to optimize it properly to combine Spine,
technology and video.

Lena is saying that we have to find a balance between using spine and
regular

videos. - When you did your video, when you did your video load test,
did you

collect any metrics about where the video source was coming from? Were
you able to

load it fully into RAM and spool it off of RAM? Was it reading off of
disk? - I

asked that question yesterday from Alexander Beratka.

He did a thorough measure of RAM and other memory.

He says that memory is not overloaded and the speed of transition
between memory and

the processor is plenty. Nothing is overloaded. So what type of
compression format

were the videos in MP4, or were they something else? No, no, they are
VPA8.

It\'s a special format. That\'s special, yes. It\'s supposed alpha and
that\'s pretty

much was our only option. VPA8, VPA9, we tested a lot and we find out
that those

two formats are most like the best formats we can do right now. But we
actually

test with such a good another test, different formats. Sorry guys,

I understand we get is full HD. What are the resolution for the videos?

It\'s not the vastest, what\'s the most? Full HD. Yes, it\'s full HD.
What is full

HD? So all of them\... 1930 by 1080.

And what are the\... Why is 6 videos on it, really? Like,

we need at least two videos for Topper or Progressive Signage. We need
at least two

videos for VDec. That\'s how we\'re running now. And the rest is for
Mesh.

What operating system did you run the test on?

Linux. Did you have appropriate drivers to use? Could you confirm
hardware decoding

and rendering of the video? No. I don\'t No.

It looked like CPU was doing the rendering.

Probably. Actually, it did not dig too deep,

understand particular limitations.

They feel like establishing baseline. I mean, this test was to kind of
validate

baseline requirements of capabilities of the port, right?

\- You just tried to make the standard Linux distribution quite new,

not so special with drivers. - Okay.

Sasha, what did you use to profile the performance or characterize it
when it was

running?

I don\'t know, but could you exit?

Only visual\... Just watching it? Yeah. Because I see 16 FPS,

but video looks

don\'t

look good. We have visual 60 FPS on the meter, 60.

But At the same time, a spine object shows nice smooth animation, but
the video, we

can see the frame skips.

So it\'s like,

moving a bit, not smooth enough.

The problem we can meet is when we will try to combine spine animation
and video

effects, it can be problems with synchronization between video effects
and spinal

image? Well, look, we haven\'t done an absolute perfect testing,

but we\'ve done enough testing to understand whether the FP7 hardware
can be used,

assuming that we can find further automation or efficiencies. But I
would not rely

much on further efficiencies if\...

market, as far as I understand, next releases for Georgia we will be
doing only

using this further, right?

Georgia is not my concern. My concern is putting

the full pass game on this hardware.

We will For Fortune for Pulse, I think without starting and trying to do
actual

animations and running main scene effects and bonuses,

we cannot tell you the full truth, but I think it\'s doable,

but with a lot of efforts for optimization. What do you think, Jim?

I\'m going to agree on this one. I think we can combine different type
of functions,

many type of optimization. And so, yes, my opinion is doable.

I have a question regarding just the regular hardware platform. So,

Lanna, you\'re saying that the FP7 motherboard would be perfectly fine
for the

Georgian market given the types of games that are playing, right? I
don\'t want to

discuss Georgia market, it\'s a placeholder for other markets where the
games are more

important. But I don\'t know why Lena answered that question in this
way. I\'m really

focused on class introducing a future full pause for class 3 Florida
market.

Let me finish my question.

The actual question I\'m asking is does the FB7 board have a Thunderbolt
and can you

use a Thunderbolt connected GPU to drive your displays and whatever you
please.

This way you have a swappable rendering hardware heavy -lifter for your
video.

I think this question should have been that should have been asked as a
As a

second or third question Sure, the reason I asked the question and the
reason I

bring in Georgia market is that by modularizing a little bit, you\'re
able to just

plug in a Thunderbolt and enable display adapter to drive high
performance displays

and you don\'t need it for those that don\'t need it. But it\'s a wrong
question to

ask because the question really is, is the current FP7 board enough for
future full

pause? That is the question that I have

As I said in my opinion for Fortune for Posts it\'s doable, but with a
lot of

efforts for optimization and special way of doing

different kind of animation and effects and maybe like heavy -involved
like programmers

efforts because we are going to have a lot of simultaneous action on the
screen

like objects acting like together, like the special points and cats and
maybe

programmers can help us to do some animations in more like optimal ways
than just

like presenting it as a video, right?

Basically we have a feature the animation controller and animation
controller can do

this. He can swap objects, yes. And we don\'t need programmers for that.
We don\'t

need. \>\> Yeah. Yeah, that\'s true. Because we are doing it in Miranda.
And in

Miranda now we have this. \>\> Yeah. \>\> Yeah.

\>\> So what does it mean a lot of effort from the design team.

Can you explain that? Are you saying that producing a regular video
could be done

easily and producing spine animation is difficult? No, no,

like combining because in spine you cannot do like a lot of nice
effects,

like particle effects and some like effects and what we are going to do,

we are going to do like animation itself is fine, like a movement of
cat, for

example, moving like cat\'s paw or something like this, but sparkles or
flame or

something like this, like smoke, we are going to do in video, and then
like

combine, combine and of this it will take some effort because when
you\'re it to

other one video piece, it\'s much easier than doing this combination.

Is there a measure of the difficulty,

like I said, measure it in time or in the expertise of the individual
who does it?

In time, Yeah, because you need to synchronize it and you need to
prepare a

different kind of assets in a special way. But it seems like it\'s a
minimal

overhead on the overall game production. It sounds like minimal overhead
when you

have one or two animations, but when you have 60 or 70, it\'s double or
even triple

time of the entire of the entire game no like of previous in this
animation I know

but the animation is only a portion of the entire game so if I look at
the entire

game and I add this element of synchronizing 60 videos well how much
overhead is

that like 10 % on the game I think it\'s more demagodition

I It depends how we go to synchronize it in a different place, but okay,
we\'re

talking about slightly more videos we need to produce. I\'ll put it this
way. First,

sometimes we use one layer for this type of animation, then just another
overlaid

layer. Now we need to combine those two to save some power on the
machine,

but now we need more general videos to be produced for each situation.
So for

example, this combination can lead to like four more videos, but we
don\'t need

actual programmers for that, I don\'t think so. Yeah, yeah. I need to
take an

account that we have this new feature in Miranda. We didn\'t use it in
practice yet.

It\'s a new feature, but yeah, we will use it and it should work. No,

we tried with Sasha with the - Yeah, I don\'t like, I mean, we didn\'t
do anything

like we always did yet. I know the feature is working, yeah, because
you\'re tested.

Again, I think it\'s doable for fortune for post. We just need to
consider that we

might need a little bit more time.

And well, I can explain why I

started with Georgia market because you said like in your introduction
balls that we

are in future we are going to use these machines like street machines
mostly and we

will move for C3 market to let\'s see that\'s why I said if we in future
we\'re

going to use it for street machines so it\'s totally enough

but that was clear for me from the start.

Okay, Gennady, what was your question, please address?

\- This was the first try with FP7 platform, I mean FP7 socket,

and we used the most popular, I mean, sweet spot for the APU, which was
not the

most powerful, but with the best ratio of price versus performance.

And this was a 6 ,800 APU from 6 ,000 Serious Ryzen.

When I checked, it\'s basically there is 8 ,000 Serious Ryzen,

which is also pretty popular and available for this socket.

And the gain in performance might be about 20%. And it won\'t be big,

I don\'t have the numbers for the pricing, but it will be more
expensive, but not

drastic. So my suggestion just to go with 8000 series, I\'m not sure
it\'s available

right now, but I know that are developing the board and will be at the
end of

February for sure available for us so 20 % is guaranteed in terms of
like 20 -50

bucks up Understood. I understand that there is a more powerful
processor.

I understand that Paddle need to search Maybe more optimized drivers for
Linux.

I don\'t know if it exists and I understand that Dima and Lena have ways
of dealing

with optimization of videos. So as a result of this meeting I think the
conclusion

is that we could successfully move into FG7 processor especially for
Flex -S hardware.

We can implement Omni platform assuming

that we will resolve the development pipeline issues that we discussed
earlier this

morning which you know I don\'t see why not one way or the other we will
resolve

it and the question that I personally have, should we add any of the
requirements

for

further optimization of either Omni platform or the Linux drivers.

I\'m referring to the requirements specifically, so we can address them
now.

And I think my question is mainly to Alexander and to Pavel.

Again, I\'m going to reiterate maybe for the third time that

My understanding is that the current FP7 solution, especially from the
tongue, which

is our main supplier,

with the same socket, allows for the 8000 processor,

which we estimate could improve power by additional 20%.

However, leaving it

for the very end, if and when necessary, and I\'m not saying that we
shouldn\'t be

using 8 ,000 processor, maybe we should, but not relying on it. Can we
add anything

to the requirements now to further, right now, as we\'re about to
release Omni

platform? Do we need to add anything to the requirements that could
further optimize

this how we deal with these videos.

Right now I do not have such a climate but I think we need to have some

measurement tool that will answer us where is the bottleneck because
right now I do

not know where

we need to make some measurements on different videos on different
number of videos

on the stand where we have a bottleneck so Pavel is suggesting to
further test the

hardware to establish where exactly the bottlenecks are. And what sort
of tests are

those? Can you explain it verbally what it is? How would you, what\'s
the methodology

of testing?

I do not know any methodology but I need at least some,

Some tools or probably just logs from browser that shows this particular
video has

frames drop

In some environment

Conditions, okay, so please so here\'s how we move forward Lena\'s team
should continue

developing future full -pass game based on the current limitations that
we have

established meaning the number of videos etc. So that\'s your threshold.

So you need to come under the threshold when you when you release this
game. Is

this enough guidance for you to continue with the game?

Yes. Okay. Okay, so with that in mind go ahead and continue making the
game under

coming in under these thresholds

Gennady, can you please provide us with?

Hardware with 8000 processor it will take us approximately 30 days to
receive it in

Minsk. So you need to ship it as soon as possible. You need to ship two
samples

to Minsk and probably two samples to Canada.

So that\'s your undertaking.

Pavel and Alexander, please do your tests and I will set a meeting for
Friday of

this week. Would that give you enough time?

Okay, to examine the results of your further investigation.

Has that conclusive enough for everyone? Yeah. I just have one question.

It\'s a question for You are like from business point of view as a plan
be as a

plan be can we consider if we will have like Some issues with
performance When game

will be fully developed is it possible to consider that we will remove
like signage

Yes from controlling from this hardware so in control signage is
different Yes,

yes, as a matter of fact, I believe that signage should actually, and
this is a

part of discussion of the architecture. But I think our architecture,
although we now

have embedded controller for progressive, I actually think that we
should probably

have a standalone hardware,

isolated hardware for progressive but don\'t take it don\'t take it as a
as a

guidance on the architecture this is my no but this is actually my
personal thinking

that I should take up with Pavel and Gennady as a matter of overall
discussion but

I just want to say that my thinking today from a market perspective I
think the

market understands the external controller better

and thinking about Flex C,

the screen and the size of the screen is large enough probably to
consider signage

as a separate element. So, for flex C on a moving forward basis but now
for flex

S most likely that would be an acceptable solution and I\'m in
particularly answering

your question Lena.

But as a plan B right?

We\'re still trying to work under the current threshold and under
current requirements.

Yes, we will start And we will continue development under considerations
that we have

one controller for all moment

Yes, correct Sorry guys for the testing purpose will three video outputs
motherboard

will be good for the testing performance or it has to be for I Mean my
under

video, but not my my preference is for I would not even entertain three
no no just

for testing because this might be available right now but the other one
might take

time just for testing I\'m asking when you do performance test you can
run all

videos but take out it\'s not like that

For real test, it\'s better to have four, because at some moment you
will need to

utilize all of them.

So with that in mind, I consider this meeting closed.

Thank you very much, and I\'ll be in touch with you and I will send an
invitation

for Wednesday and for Friday on a moving forward basis.

I will exclude Lena and Dima from the Friday\'s meeting. There\'s no
need for that.

I will only invite the hardware people. Thank you very much. We\'re
wishing you a

good day and good week. Erin, I\'ll talk to you now.
