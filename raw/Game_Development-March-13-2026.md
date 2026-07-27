**Game_Development-20260313_143522-Meeting Recording**

13 March 2026, 06:35pm

18m 32s

**\
Val Levitan** 0:04\
OK. So let\'s move on to Lena. Thank you for sharing the screen. I appreciate it. We don\'t need it anymore. What else, Michael, where are you taking us from here?

**\
Michael Gottlieb** 0:15\
I think I just want Lena to show the actually. Lena, could you show the Dragonpay\'s main game screen just so people can get a sense of of what we\'ve done with it?

**\
Lena Zhukova** 0:23\
I\'m sure.

**\
Michael Gottlieb** 0:38\
So zoom in on the uh the reels.

**\
Val Levitan** 0:39\
Great. So, so sorry. Hold on, hold on. Zoom out, Zoom out.

**\
Michael Gottlieb** 0:43\
Yeah.

**\
Val Levitan** 0:46\
Give me a second here.\
OK. Thank you.

**\
Michael Gottlieb** 1:09\
Zoom in on a real bundle.\
And this is just kind of for Juan a little bit. The the big thing I am pleased with is you can notice how we went from the generic room temperature Royals to kind of these Asian looking Royals.\
They and they\'re a little smaller. They\'re a little desaturated. The queen kind of disappears and that dragon just pops like a son of a gun. The other symbols I think pop pop well relative to their hierarchy. And it\'s good. I think it. I think it\'s good. We\'ve got the liquid glass across the bottom there, the new ticker implement.\
Implementation that I was talking about, we want to see that put put in there, but I just wanted to give you a sense of of you know what we\'re doing, what the new Dragon page is going to look like versus the previous one.\
And then, Lena, if you could bring up the the coin, the jackpot coin on reel three that we\'ve been working on this week, yes.\
So zoom in just to touch.\
Here we go.\
So that\'s the new jackpot coin.

**\
Val Levitan** 2:28\
Can you put the the two games side by side?

**\
Lena Zhukova** 2:35\
To switch to games.

**\
Val Levitan** 2:38\
This one and the previous one.

**\
Lena Zhukova** 2:39\
But they\'re from different products and from different machines. Previous one for horizontal, this one for your to call.

**\
Val Levitan** 2:50\
I just want to ask a question so it would be easier for me if I could see side by side.\
So um.\
The machine on the right, the design on the right consumes.\
Very small edge around the real bundle.\
And machine on the left consumes or I guess the real bundle is considerably smaller.\
And I understand that one is a vertical design and other is horizontal.\
But is there a specific strategy for that or what? What\'s the thinking behind this? Like the real bundle is considerably smaller.\
Visually on a horizontal machine.

**\
Michael Gottlieb** 4:15\
Yeah, well, the one, the one on the left is D27. That\'s the D27 implementation that we have and the.

**\
Val Levitan** 4:21\
But but I understand but D27 is is a very very large screen.\
Horizontally, because it really houses only the real bundle, right?

**\
Lena Zhukova** 4:35\
Yes, and physically it\'s going to be like very big because I can imagine that this is full screen.

**\
Michael Gottlieb** 4:38\
Right.

**\
Lena Zhukova** 4:42\
So it\'s going to be like really big like symbols in front of you like this.

**\
Val Levitan** 4:47\
But I know, but you specifically left a huge border around it by making the real bundle smaller, where on the other design you consume the entire field without the the edges on the left and on the right.

**\
Lena Zhukova** 5:01\
Because again, physically a vertical screen is narrower, so like in in the real size of the symbol is going to be even bigger on on horizontal than on vertical.\
Because the horizontal screen is wide and the vertical screen is narrow.

**\
Val Levitan** 5:25\
But I think you\'re misunderstanding my question.\
Let me let me try to rephrase it.\
The benefit of the vertical screen is, you know, a certain expression of of of of the game that we\'re looking for vertical, let\'s say for you know.\
4 by 5 reels especially, but in here we have 3 by 5 reel which is kind of a.

**\
Lena Zhukova** 6:04\
Strunken.

**\
Val Levitan** 6:04\
Reduced, reduced height. It\'s shorter, but the width we\'re specifically putting it on a horizontal layout, but we\'re taking this horizontal layout and we\'re saying I\'m going to instead of making the reels.\
Broader, I\'m putting a edge on both sides and maybe this is by intent. I mean, obviously this is by intent, but I\'m trying because we\'re trying to establish our own school.\
I\'m trying to understand what\'s the.\
Philosophy behind it and whether we overlooked it or we did it by intent specifically or maybe.

**\
Michael Gottlieb** 6:52\
No, this is absolutely intentional.

**\
Val Levitan** 6:55\
Great.\
Because I\'ll tell you that proportionately the eye catches the real bundle as being small.\
Like if you again put it side by side, no, but you\'re you\'re faking.

**\
Lena Zhukova** 7:13\
But you might imagine you\'re going to see it like this, like see it. So it\'s a white screen, so you\'ll see it like that.

**\
Efim Podvoiski** 7:20\
OK, Lena, can you put it side by side with real dimensions in in mind so it will be a real comparison, not not like.

**\
Lena Zhukova** 7:29\
Oh, good.\
And probably sounds like this. Mm-hmm.

**\
Val Levitan** 7:46\
No way, no.

**\
Efim Podvoiski** 7:47\
Why? Why not?

**\
Val Levitan** 7:50\
Because I look at the at the tinker at the bottom, it\'s much smaller. This one is much bigger.

**\
Lena Zhukova** 7:58\
See, it\'s 100% and this is 100%, but what figure is different size, so on vertical and horizontal it\'s it\'s really different size.

**\
Val Levitan** 8:06\
OK, OK, so yeah, so put put them, put them side by side so I I could see it.\
Maybe my eye is lying to me, I don\'t know.

**\
Juan Martinez** 8:28\
I guess just to rephrase the question, or is the the square box imaginary box around the symbol, are they the same actual dimensions on the left and the right? You know, is it, you know, 200 millimeters by 200 millimeters and is it the?\
Same on the verta.

**\
Lena Zhukova** 8:48\
No physical uh uh uh symbols and horizontal screen is going to be bigger even on this size of rails.

**\
Val Levitan** 8:57\
They should be because it\'s a 3 by 5 and it\'s horizontal, so it should be bigger.\
OK, so I\'m I\'m, I\'m raising the concern that.\
All right, I I I would make it larger, but OK.

**\
Michael Gottlieb** 9:22\
Well, the the challenge is that Juan wants to have a play button on the screen that was part of the REQ, and the play button has to have a certain size associated with it for it to make sense for a human finger. So when you start, you know, kind of filling in your.

**\
Val Levitan** 9:36\
Mhm.

**\
Michael Gottlieb** 9:40\
Your puzzle pieces. If you\'ve got the play button a certain size, then it starts to propagate and dictate other ratios and proportions, and the ratios and proportions need to be preserved.\
Because if you go, you know if you can\'t just stretch one way and not stretch in a different way.

**\
Val Levitan** 10:00\
Of course.\
OK, alright.

**\
Michael Gottlieb** 10:06\
OK, so let\'s let\'s just look at crazy. OK, yeah, let\'s just look at crazy Colt for a second here, Lena.

**\
Val Levitan** 10:07\
I\'m moving, moving, moving on.\
Just before you remove the other game off the screen, I just want to let you know that visually Crazy Colt looks better to me than the other game I cannot.

**\
Michael Gottlieb** 10:16\
And.

**\
Val Levitan** 10:28\
Well, I can. I mean the other game, the Crazy Cold has very aesthetically to my eye, very aesthetically pleasing contrast.\
And everything pops out nicely. The background is nicely contrasted with the pay table and the main symbol and the name of the game. Everything contrasts very nicely where the other game to my eye.\
And I\'m being just a single critic of it is all one gold thing.\
So that\'s that\'s one opinion of an individual. You can totally dismiss it and move on.

**\
Michael Gottlieb** 11:19\
OK, noted. So we\'ve got the liquid glass progressive meters here, Juan, up on top.

**\**
11:28\
Mhm.

**\
Michael Gottlieb** 11:29\
Color-coded.\
And then if you zoom in a little bit, Lena.\
We\'ve got this new presentation where it says four with the jackpot coin stacked Unreal 3 award progressive bonus.\
Just to give you a sense of where we\'re headed with it.\
That was it. Just to give you guys some visibility into what we\'ve been, what we\'ve been cranking on.

**\
Val Levitan** 12:11\
Crazy cold is made for which market?

**\
Juan Martinez** 12:14\
This is for Georgia.

**\
Val Levitan** 12:17\
Is it? Is it? Is it the first time we\'re introducing crazy cold in Georgia? Is it? Is it successful?

**\
Lena Zhukova** 12:17\
This will should come crazy.

**\
Efim Podvoiski** 12:24\
No.

**\
Juan Martinez** 12:28\
We have no data to.

**\
Val Levitan** 12:36\
OK. And so for Georgia, the the main move here is we moved away from abstract Royals to casino type Royals.\
Let\'s call it Skill Royals versus Casino Royals, yeah.

**\
Michael Gottlieb** 12:52\
Absolutely, yeah, 100%.

**\
Lena Zhukova** 12:54\
Yeah, yeah, they look much better.

**\
Michael Gottlieb** 12:57\
Mhm.

**\
Val Levitan** 12:57\
This game, this, this game, this game is going to kill it. It\'s it. It looks right. It it looks right.

**\
Michael Gottlieb** 13:08\
Please do you like it?

**\
Val Levitan** 13:08\
Can we can we introduce it in Nebraska and Texas?

**\
Juan Martinez** 13:14\
Yeah, Nebraska vertical and South Dakota vertical are our next topics of conversation. So absolutely.

**\
Val Levitan** 13:22\
This is a fantastic vertical game. I need 3 minutes to take to have a drink and I\'ll be right back.

**\
Juan Martinez** 13:31\
OK.

**\
Michael Gottlieb** 13:32\
OK.

**\
Val Levitan** 15:52\
You feel where\'s your, uh, where are your tasks?\
For all of these designs.

**\
Efim Podvoiski** 16:03\
Uh, I will start uh. When you go to design, I will start on uh.

**\
Val Levitan** 16:09\
But where are your tasks?\
Do you have a? Do you have features here?

**\
Efim Podvoiski** 16:14\
The tasks that I\'m doing anything or this related to game design?

**\
Val Levitan** 16:21\
Related to game design and or game production, whatever stages.

**\
Efim Podvoiski** 16:25\
But at this moment there is nothing. When we go, I just did a little tasking concept. I prepared, prepared the.\
Mass parameters for this twin bison, but I didn\'t made a special feature for it. It\'s just preparing a small document discussing this Michael and putting it into.\
Into into the issue, attaching to the what\'s the name to the abstract.

**\
Val Levitan** 16:56\
OK, so you and I should just get on the subject of how to do it integrated and with everybody else\'s work. No, not a part of, not a part of this meeting.

**\
Efim Podvoiski** 17:07\
Uh.\
OK.

**\
Val Levitan** 17:12\
All right, so.

**\
Efim Podvoiski** 17:12\
But the moment is we start design of yeah.

**\
Val Levitan** 17:15\
I I got it. Let let me let me get back to you on this. Let\'s, yeah, Michael, continue.

**\
Efim Podvoiski** 17:18\
M.

**\
Val Levitan** 17:23\
You\'re muted.

**\
Juan Martinez** 17:23\
You\'re muted. You\'re muted.

**\
Michael Gottlieb** 17:27\
I believe, I believe that covers it, unless you have anything else you want to touch on.

**\
Val Levitan** 17:35\
1.

**\
Juan Martinez** 17:36\
No, I don\'t.

**\
Val Levitan** 17:39\
OK, so just uh.\
As a general view, the.\
Nebraska 2 is done and we\'re back on pushing Georgia release, right? Sorry, South Dakota and Georgia.

**\
Michael Gottlieb** 17:58\
South Dakota. Yeah, we need to get South Dakota done and then we move on to Georgia.

**\
Juan Martinez** 18:00\
Yeah.

**\
Val Levitan** 18:03\
Gotcha. OK, understood. I don\'t have any more questions.\
We\'re good to go.

**\
Michael Gottlieb** 18:12\
OK, well, as they say, as they say in Ireland, Shabbat Shalom and have a nice Saint Patrick\'s Day.

**\
Val Levitan** 18:16\
Yes, yes, same, same. Yeah. Great weekend, everyone. And if you, if you let me call you.

**\
Juan Martinez** 18:17\
Yeah.

**\
Efim Podvoiski** 18:20\
Yeah.

**\
Juan Martinez** 18:21\
Thanks everybody.

**\
Efim Podvoiski** 18:21\
Thank you.

**\
Lena Zhukova** 18:22\
Thank you.

**\
Efim Podvoiski** 18:25\
OK, sure.

**\
Val Levitan** 18:25\
Thank you. Bye.

**\
Lena Zhukova** 18:25\
Thank you.

**\
Val Levitan** stopped transcription
