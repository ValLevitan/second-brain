# Raw Transcript — Game_Development
**Date:** November 13, 2026, 12:10 PM – 1:41 PM Eastern
**Summary note:** [[Meeting_Notes_Class_A_Party_Time_Math_and_Colombia_Vertical_Games-November-13-2026]]
---
WEBVTT

00:00:03.741 --> 00:00:07.861
<v Michael Gottlieb>Thing it was going to say line lines one, three, 7, and nine pay.</v>

00:00:03.941 --> 00:00:03.981
<v Efim Podvoiski>Ah.</v>

00:00:05.141 --> 00:00:21.741
<v Efim Podvoiski>If they have exactly the same, the same being symbols, it's not like all of them are bundled together. It shows animation, if it's animation matches several lines, it shows the list of lines. And I have seen it, I don't know, maybe.</v>

00:00:09.781 --> 00:00:10.261
<v Michael Gottlieb>Right.</v>

00:00:21.381 --> 00:00:27.621
<v Michael Gottlieb>Okay, I'll take I must not be understanding it then I'll take a look I'll take another look at it, but it's in yesterday's build is what you're saying, right?</v>

00:00:27.421 --> 00:00:28.461
<v Efim Podvoiski>It is, it is.</v>

00:00:28.821 --> 00:00:46.101
<v Lena Zhukova>But I will send fresh soon, once it's finished building. So, and then at least if you Jamber Lanto together with this adjusted pay table, if everything is good, Vitaliy will record demo video already because game.</v>

00:00:28.901 --> 00:00:29.461
<v Michael Gottlieb>Okay.</v>

00:00:31.221 --> 00:00:31.621
<v Michael Gottlieb>Yeah.</v>

00:00:40.741 --> 00:00:41.141
<v Michael Gottlieb>Right.</v>

00:00:47.381 --> 00:00:48.261
<v Lena Zhukova>In Dzmitry.</v>

00:00:48.981 --> 00:00:50.021
<v Michael Gottlieb>Okay, good.</v>

00:00:52.981 --> 00:00:53.901
<v Val Levitan>Hello, guys.</v>

00:00:54.181 --> 00:00:54.741
<v Efim Podvoiski>Pavel.</v>

00:00:54.301 --> 00:00:56.021
<v Michael Gottlieb>Morning, Val, how are you?</v>

00:00:56.701 --> 00:00:59.741
<v Val Levitan>Thank you for asking. I'm well. How's everybody doing?</v>

00:01:00.261 --> 00:01:00.821
<v Efim Podvoiski>Good, good.</v>

00:01:01.301 --> 00:01:02.021
<v Lena Zhukova>Good, thank you.</v>

00:01:02.661 --> 00:01:06.621
<v Michael Gottlieb>Fine, we're finally getting a little bit of rain here in Southern California, which we need.</v>

00:01:03.101 --> 00:01:03.821
<v Val Levitan>Okay.</v>

00:01:07.821 --> 00:01:09.261
<v Val Levitan>Yeah, with Andrei.</v>

00:01:10.021 --> 00:01:15.541
<v Michael Gottlieb>Very, very dry and very, it's devil's weather as they call it, the fire season.</v>

00:01:15.341 --> 00:01:15.581
<v Val Levitan>No.</v>

00:01:16.501 --> 00:01:35.781
<v Michael Gottlieb>really hot and windy and winds are whipping up, you know, and so we need the rain to wet everything down. Susan and I were driving down the street the other day and, you know, a fire truck and another fire truck and another fire truck, we had to keep pulling over.</v>

00:01:36.181 --> 00:01:53.541
<v Michael Gottlieb>And then we looked and there was the smoke billowing out in the brush area. There was a fire, you know, hopefully it's not people starting them because it just stuff starts. They have power line issues and all sorts of things. So yeah, it's a challenging situation.</v>

00:01:55.301 --> 00:01:56.901
<v Michael Gottlieb>You, you're down in Miami, yes?</v>

00:01:56.301 --> 00:01:56.541
<v Val Levitan>Yeah.</v>

00:01:59.181 --> 00:02:01.661
<v Val Levitan>Yeah, I arrived.</v>

00:02:03.181 --> 00:02:08.381
<v Val Levitan>late last night, today I'm in Miami and then back to Atlanta on Monday.</v>

00:02:08.821 --> 00:02:09.381
<v Michael Gottlieb>Okarak.</v>

00:02:10.581 --> 00:02:11.141
<v Michael Gottlieb>Okay.</v>

00:02:12.301 --> 00:02:13.541
<v Michael Gottlieb>Excuse me, so...</v>

00:02:13.021 --> 00:02:15.741
<v Val Levitan>Well, uh, where, where are we on Class A?</v>

00:02:17.021 --> 00:02:30.381
<v Val Levitan>And before I ask that question, just spark that for a second. Are Giorgi or Cohen math, is it a finite math or is it a like a random math?</v>

00:02:33.021 --> 00:02:37.781
<v Efim Podvoiski>Finite, you mean predetermined outcome? Yes, yes, yes, yes.</v>

00:02:35.501 --> 00:02:36.861
<v Val Levitan>Yeah, predetermined.</v>

00:02:38.541 --> 00:02:41.581
<v Val Levitan>Does it have to be predetermined or could it be random?</v>

00:02:44.421 --> 00:03:02.101
<v Efim Podvoiski>I think at some point when we started it, we have seen somewhere that they expected to be predetermined. And it's easier to have it predetermined because we can do some interesting things with masks that's hard to achieve naturally.</v>

00:03:04.861 --> 00:03:08.861
<v Val Levitan>I'm confused. What is the 10 simple words?</v>

00:03:11.781 --> 00:03:26.141
<v Michael Gottlieb>There are specific outcomes that we want the player to experience, and it's far easier to do that with predetermined math than actual true class 3 math. Is that an accurate statement of theme? Okay.</v>

00:03:24.981 --> 00:03:26.021
<v Efim Podvoiski>Yes, yes.</v>

00:03:27.021 --> 00:03:29.181
<v Val Levitan>So we want it to be predetermined.</v>

00:03:29.621 --> 00:03:30.101
<v Efim Podvoiski>Yes.</v>

00:03:30.421 --> 00:03:30.901
<v Michael Gottlieb>Yes.</v>

00:03:33.021 --> 00:03:36.461
<v Val Levitan>Do others have does does aristocrat have predetermined?</v>

00:03:37.781 --> 00:03:38.661
<v Efim Podvoiski>How could I know?</v>

00:03:39.461 --> 00:03:40.661
<v Michael Gottlieb>I don't know, Lena, I don't know.</v>

00:03:43.061 --> 00:03:47.421
<v Val Levitan>Doesn't random math feel better for a player?</v>

00:03:51.381 --> 00:04:14.981
<v Michael Gottlieb>No, no, not necessarily. I know that Blueberry, Blueberry has uses some predetermined math with Shark's Lock and Devil's Lock. Those were very popular games. I don't think it makes, I mean, probabilities are probabilities, right? And RTP is RTP. It's just that with predetermined, we can</v>

00:04:15.301 --> 00:04:36.261
<v Michael Gottlieb>we can force specific rewards and outcomes and especially with three by threes and most the heightened case of it is our spins games, crazy spins. That's where we ended up, you know, like that's where we ended up getting.</v>

00:04:32.341 --> 00:04:32.901
<v Efim Podvoiski>Yes.</v>

00:04:38.021 --> 00:05:00.341
<v Michael Gottlieb>getting burned because we took Liberty spins to South Dakota and we took a certain approach with it. And because we couldn't do predetermined math, we took an approach that you thought was going to work and it didn't. And the game ended up being dead last in the rankings. So we've made some substantial changes to it for rodeo spins for South Dakota and hopefully that will go</v>

00:05:00.421 --> 00:05:15.461
<v Michael Gottlieb>and that will work. But that's a perfect example, Val, of a math model, predetermined math model that we tried to bring to class 3, and because we couldn't do predetermined, it was hugely problematic. Is that accurate, Efim?</v>

00:05:16.021 --> 00:05:16.581
<v Efim Podvoiski>Yes.</v>

00:05:16.981 --> 00:05:17.221
<v Michael Gottlieb>Yeah.</v>

00:05:17.941 --> 00:05:25.621
<v Val Levitan>Because we, you said because we couldn't do it predetermined, so we had to do it random, so random didn't work, but predetermined worked.</v>

00:05:25.781 --> 00:05:26.741
<v Michael Gottlieb>Yes, exactly.</v>

00:05:30.101 --> 00:05:36.021
<v Val Levitan>And the reason we couldn't do it predetermined, because South Dakota prohibits predetermined, they only want random.</v>

00:05:36.541 --> 00:05:37.021
<v Efim Podvoiski>Yes.</v>

00:05:37.301 --> 00:05:37.861
<v Michael Gottlieb>Correct.</v>

00:05:37.541 --> 00:05:44.181
<v Val Levitan>And so we took our predetermined math, we converted it into random, assuming that we can succeed, but we failed.</v>

00:05:45.781 --> 00:05:46.421
<v Michael Gottlieb>Yes.</v>

00:05:46.061 --> 00:05:46.541
<v Efim Podvoiski>Yes.</v>

00:05:53.621 --> 00:05:56.421
<v Val Levitan>But class A, you will be doing random.</v>

00:05:56.861 --> 00:05:57.341
<v Efim Podvoiski>No.</v>

00:05:59.501 --> 00:06:00.461
<v Efim Podvoiski>No presentment.</v>

00:05:59.741 --> 00:06:00.101
<v Val Levitan>No.</v>

00:06:05.421 --> 00:06:06.301
<v Efim Podvoiski>It's not around them.</v>

00:06:05.621 --> 00:06:06.581
<v Val Levitan>but will behave.</v>

00:06:07.581 --> 00:06:08.061
<v Efim Podvoiski>Sorry?</v>

00:06:09.061 --> 00:06:09.621
<v Val Levitan>Go ahead.</v>

00:06:10.621 --> 00:06:23.021
<v Efim Podvoiski>It's it cannot be a purely random period because it's has this partial time, this predicted outcome, so it's not random already.</v>

00:06:25.741 --> 00:06:34.541
<v Efim Podvoiski>But yeah, we probably could do something with random. But why? There is no</v>

00:06:35.701 --> 00:06:36.221
<v Efim Podvoiski>Beautiful.</v>

00:06:37.221 --> 00:06:42.741
<v Val Levitan>So our preference would always be predetermined math if the law permitted.</v>

00:06:43.581 --> 00:07:01.901
<v Efim Podvoiski>Yes, because this pre-etermined mass, you can do whatever you want with random mass, you try to do whatever what you want, this pay table and alliance, and it's not always achievable. And for example, some things you never can get, you can never promise players</v>

00:07:01.981 --> 00:07:08.941
<v Efim Podvoiski>She goes to free spins that there will be some bins, at least like 5 beds or something.</v>

00:07:09.821 --> 00:07:20.861
<v Efim Podvoiski>This random mass, sometimes they just get zero, and if we want, if if we want to avoid it, we cannot do it, and this terminal mass, we can do it.</v>

00:07:23.061 --> 00:07:34.101
<v Michael Gottlieb>But on the player presentation level, because we're going to dual box for Class A, it will be superior to Nudge.</v>

00:07:35.061 --> 00:07:54.981
<v Michael Gottlieb>Because when you take something like Fiery Ice and you have to use Nudge for Fiery Ice, the way the bonus triggers and the way the game behaves is basically not as good as the Class 3 implementation. So by not having Nudge,</v>

00:07:46.781 --> 00:07:47.021
<v Val Levitan>Good.</v>

00:07:47.701 --> 00:07:48.181
<v Efim Podvoiski>Mhm.</v>

00:07:55.061 --> 00:08:14.821
<v Michael Gottlieb>and just being able to use dual box, we can use, let's say, a class 3 presentation, even though the math is predetermined. It will look more like a class 3 game is probably a better way of saying it. It'll look exactly like a class 3 game because we no longer have the nudge. We basically had to</v>

00:08:05.741 --> 00:08:06.221
<v Efim Podvoiski>Mhm.</v>

00:08:09.861 --> 00:08:10.341
<v Efim Podvoiski>Yeah.</v>

00:08:15.381 --> 00:08:34.501
<v Michael Gottlieb>take when we did Fiery Ice, we created a class 3 product and then had to reverse engineer it to support nudge. And in the process of doing so, it's not as good of a game because the way the symbol trigger works, you have to nudge on real three and it's just not as good. And by the way, Jackpot Rush is the exact same thing.</v>

00:08:34.821 --> 00:08:43.181
<v Michael Gottlieb>Jackpot Rush is going to play a hell of a lot better as a Class A product than it did as a nudge product.</v>

00:08:44.501 --> 00:08:46.501
<v Michael Gottlieb>In my opinion, I don't know what you think, Efim.</v>

00:08:46.941 --> 00:09:01.261
<v Efim Podvoiski>Yeah, so, so this is different issues, not just one thing, outcomes is another thing, and just in Georgia, we had both of them, and so, yeah, and they have different effect on.</v>

00:08:53.701 --> 00:08:56.101
<v Michael Gottlieb>Right, yes. All I'm saying is that on a pre... yeah.</v>

00:09:02.381 --> 00:09:03.101
<v Efim Podvoiski>But, uh...</v>

00:09:02.581 --> 00:09:24.501
<v Michael Gottlieb>I'm just saying the dual box dual box frees us up, it unshackles us, and it allows us to create an experience that basically plays like a class 3 game, other than the dual box. It's not invasive the way Nudge is invasive. You have to make do all sorts of Mickey Mouse and compromises in order to make the Nudge work on these five real games.</v>

00:09:12.141 --> 00:09:12.541
<v Efim Podvoiski>Yes.</v>

00:09:24.701 --> 00:09:45.541
<v Michael Gottlieb>Nudge on three reel is okay. Our competitors are still doing nudge on three reel, but nudge on five reel is not as compelling by any stretch of the imagination as a class 3 presentation. So the net result is that the class A versions of Jackpot Rush, Fiery Ice, and the other five reelers are going to be...</v>

00:09:31.541 --> 00:09:32.021
<v Efim Podvoiski>Mhm.</v>

00:09:47.381 --> 00:09:50.741
<v Michael Gottlieb>better. Although right now we're not doing... Go ahead.</v>

00:09:49.141 --> 00:09:49.861
<v Val Levitan>Saute.</v>

00:09:51.101 --> 00:09:51.701
<v Val Levitan>Yeah, go ahead.</v>

00:09:52.261 --> 00:10:06.741
<v Michael Gottlieb>I was just going to say, but as the caveat is right now, because we don't have progressives, we're not doing Fiery Ice and Jackpot Rush for Class A yet. Someday we will. But for the five real games that we're going to have in Class A, they're going to play a hell of a lot better, in my opinion.</v>

00:09:52.821 --> 00:09:53.461
<v Val Levitan>Both.</v>

00:10:11.621 --> 00:10:13.661
<v Val Levitan>OK, let's go through one.</v>

00:10:12.101 --> 00:10:13.861
<v Efim Podvoiski>Less artificial for sure.</v>

00:10:15.781 --> 00:10:17.301
<v Val Levitan>Let's go through schedule, please.</v>

00:10:23.141 --> 00:10:24.101
<v Michael Gottlieb>Lena, can you share?</v>

00:10:34.901 --> 00:10:36.261
<v Michael Gottlieb>You open up Game Concept.</v>

00:10:44.261 --> 00:10:54.901
<v Michael Gottlieb>Okay, so in game concept, the design work for South Dakota 3 is all complete. Excuse me, the concept work, the abstract, go ahead.</v>

00:10:53.701 --> 00:10:53.861
<v Val Levitan>Yeah.</v>

00:10:55.701 --> 00:10:58.981
<v Val Levitan>Excuse me, one second. I need to make that correction here.</v>

00:11:36.021 --> 00:11:37.381
<v Val Levitan>Just bear with me, please.</v>

00:11:37.781 --> 00:11:38.341
<v Michael Gottlieb>No, sorry.</v>

00:12:59.301 --> 00:13:04.261
<v Val Levitan>Okay, I am with you now, so IP 1225. Please proceed, Michael.</v>

00:13:06.661 --> 00:13:07.461
<v Michael Gottlieb>Oh.</v>

00:13:08.501 --> 00:13:28.741
<v Michael Gottlieb>Right, so, well, going back a step, so South Dakota, D2703, Nova, all of that concept work is done. IP 1190, Georgia Class A, V43, the concept work is done. Just as a side note, Efim and I are going through</v>

00:13:28.901 --> 00:13:48.941
<v Michael Gottlieb>basically on a game by game basis, testing the different party time implementations to get a feel for it. Efim has a simulator, so we're playing the simulator and observing the behaviors of party time triggers. We feel we've got lines, riches dialed in, so we're going to move on to rodeo spins, which is a more difficult</v>

00:13:49.301 --> 00:13:54.261
<v Michael Gottlieb>challenge or to tackle that. So that's what we're going to be focusing on next.</v>

00:13:54.421 --> 00:14:01.781
<v Val Levitan>Can you explain? Can you explain to me? You said we have a simulator. Yeah, you.</v>

00:14:03.141 --> 00:14:06.101
<v Val Levitan>You're not discussing game mechanics, you're...</v>

00:14:07.181 --> 00:14:11.461
<v Val Levitan>Going into this, you already know what the mechanics is, right?</v>

00:14:11.301 --> 00:14:12.341
<v Michael Gottlieb>Correct, yes.</v>

00:14:12.901 --> 00:14:23.621
<v Val Levitan>So, you're simulating, knowing the mechanics, you're simulating, I guess, contribution to every.</v>

00:14:25.621 --> 00:14:28.021
<v Val Levitan>Branch of the game, if I may call it this way.</v>

00:14:27.821 --> 00:14:30.421
<v Michael Gottlieb>Well, we're looking at spin outcomes.</v>

00:14:33.941 --> 00:14:39.861
<v Val Levitan>spin outcomes meaning all the spins or you're looking at.</v>

00:14:41.301 --> 00:14:41.941
<v Val Levitan>Oh.</v>

00:14:45.221 --> 00:14:50.581
<v Val Levitan>split into categories, for example, base game versus bonus game.</v>

00:14:51.141 --> 00:14:56.821
<v Michael Gottlieb>Right, yeah, we're, yeah, base game versus bonus game. Here, I'll even, let's see here, share.</v>

00:14:58.341 --> 00:15:06.381
<v Efim Podvoiski>Basically, we're playing the game on a very primitive level. It's how it feels, because you still need to see.</v>

00:14:58.581 --> 00:14:59.061
<v Michael Gottlieb>There.</v>

00:15:07.061 --> 00:15:12.981
<v Efim Podvoiski>to see how it feels. The numbers are there, but how it actually works.</v>

00:15:14.261 --> 00:15:26.501
<v Michael Gottlieb>Right, so this is running in autoplay, basically simulating the game. And then over here, we can track number of rounds, number of free spin rounds, number of party time starts.</v>

00:15:16.661 --> 00:15:16.741
<v Lena Zhukova>Ha.</v>

00:15:27.461 --> 00:15:32.261
<v Michael Gottlieb>So there you go. So now we're we're now we're in party time.</v>

00:15:33.261 --> 00:15:36.101
<v Val Levitan>But I'm sorry, are you, are you?</v>

00:15:33.621 --> 00:15:34.421
<v Michael Gottlieb>Or no, what?</v>

00:15:38.181 --> 00:15:43.621
<v Val Levitan>Are you discussing IP 1225 because it says Georgia QAM V43?</v>

00:15:43.141 --> 00:15:47.141
<v Michael Gottlieb>Oh, I'm sorry, I was sharing my screen. You're not seeing you guys can't see my screen?</v>

00:15:47.541 --> 00:15:54.021
<v Val Levitan>I know I am, and I appreciate it. I just, I got lost, I got lost in.</v>

00:15:49.941 --> 00:15:50.501
<v Michael Gottlieb>Yeah, yeah.</v>

00:15:51.061 --> 00:15:51.781
<v Efim Podvoiski>Well, I see.</v>

00:15:55.381 --> 00:15:56.181
<v Val Levitan>In Jira.</v>

00:15:55.821 --> 00:16:17.461
<v Michael Gottlieb>Yeah, this would be this would be underneath IP 1190. It's IP 1193. This is technically done. I mean, I guess this is really part of the design phase. I was just throwing this in midstream to communicate that this is what Efim and I have been working on this week.</v>

00:16:18.221 --> 00:16:24.021
<v Val Levitan>No, okay, I appreciate it and I appreciate that you're showing it to me and explaining it to me.</v>

00:16:18.501 --> 00:16:18.981
<v Lena Zhukova>Yes.</v>

00:16:21.461 --> 00:16:21.781
<v Michael Gottlieb>Yeah.</v>

00:16:24.901 --> 00:16:25.461
<v Val Levitan>Um...</v>

00:16:26.421 --> 00:16:37.221
<v Val Levitan>Are you looking for a particular outcome, a particular percentage, or a number of hits, or number of hits per minute per hour?</v>

00:16:32.901 --> 00:16:35.061
<v Michael Gottlieb>Yes, yeah, exactly. We're...</v>

00:16:38.341 --> 00:16:55.981
<v Michael Gottlieb>No, it's just a function of if I'm playing this thing, the very specific question or questions we're focused on are, does party time happen often enough? And when it does happen, does it happen?</v>

00:16:56.101 --> 00:17:16.021
<v Michael Gottlieb>pay enough. That's what we're, so I had, Efim and I had a premise, a theory on a hit ratio. So we're testing that hit ratio to see if this happens often enough and then compared to free spins and how much free spins pay.</v>

00:17:16.301 --> 00:17:37.701
<v Michael Gottlieb>Because you want party time to be compelling and pay well. You want free spins to be compelling and pay well. And the other thing we're looking at is making sure that we still have a base game. Because those Primero games don't have base games. They don't pay, as you saw. The base games are complete garbage. So we're essentially looking at all three legs of the stool and saying, okay, in a typical play session,</v>

00:17:37.821 --> 00:17:58.101
<v Michael Gottlieb>Am I getting some decent base game pays? Am I, is free spins triggering and the out or the EV of free spins pretty solid and decent? I feel good about that. And then am I triggering party time with a reasonable degree of frequency, even though it's kind of far out there and the party time wins are decent wins. So just the holistic, the entire.</v>

00:17:45.421 --> 00:17:45.861
<v Val Levitan>Yeah.</v>

00:17:58.221 --> 00:18:18.141
<v Michael Gottlieb>game experience, the three legs of the stool, is it balanced? That's what we're looking at. And specifically, because we're introducing this party time feature, right, which takes RTP away from the base game conceivably in theory and from free spins in theory. So how does that, you know, are we screwing anything up?</v>

00:18:18.221 --> 00:18:37.381
<v Michael Gottlieb>Are we destroying the base game? Are we screwing up free spins? Where do we have to pull from to get the stool level? To get the three legs to be about where, and obviously you don't want everything to be perfectly level because you want party time to be more compelling than the base game. Free spins is more compelling.</v>

00:18:37.621 --> 00:18:57.141
<v Michael Gottlieb>than the base game, right? So there are levels of how much excitement and the roller coaster you're going to have, but you don't want anything, any one thing to completely overpower it to the point of where, you know, the rest of the game isn't worth playing. And you end up with the experience that we had when we were there where you're just</v>

00:18:57.541 --> 00:19:02.101
<v Michael Gottlieb>slamming waiting for party time to begin. So that's what we're focused on.</v>

00:18:58.421 --> 00:18:58.581
<v Val Levitan>Yeah.</v>

00:19:03.141 --> 00:19:07.381
<v Val Levitan>And what is the verdict so far? Can you achieve your desired?</v>

00:19:08.821 --> 00:19:12.861
<v Val Levitan>design stage, design intent.</v>

00:19:10.941 --> 00:19:11.101
<v Michael Gottlieb>With.</v>

00:19:13.421 --> 00:19:35.381
<v Michael Gottlieb>With Lion's Riches, so of the six games, one of them we believe we're in good shape. One of them, Efim and I both feel good about. So as I was saying, we need to move on to Rodeo Spin. So we need to go through all six of the games, because all the games are different and they all behave different. And Rodeo Spins is even stranger and weirder because it has a re-spin feature.</v>

00:19:35.941 --> 00:19:56.021
<v Michael Gottlieb>Right? So, and we're trying to figure out when we would conceivably trigger party time if we have to, especially if you get wind capped. So what Efim was bringing up, for example, is that Rodeo Spins has a multiplier on Real 4 that's a 5x multiplier. So bang, you're wind capped.</v>

00:19:56.261 --> 00:20:15.861
<v Michael Gottlieb>with one spin without any difficulty. So re-spins within that aren't going to be really exciting and compelling. So we're going to bolt party time onto the back end of it. And the analogy would be we're doing the same thing that we did with free spins, because free spins gets win capped. So we're going to bolt party time on the back end of free spins.</v>

00:20:16.021 --> 00:20:34.981
<v Michael Gottlieb>to keep the ride going, we're going to do the same thing with the re-spin feature in Rodeo Spins. So we've got six games to go through to get the Class A math to all behave the way that we want it to. Lions Riches was the one that we started with. We feel good about that. And then we're moving on to subsequent games.</v>

00:20:36.101 --> 00:20:46.901
<v Efim Podvoiski>Maybe we don't need all six games to be the same, to pay the same attention to all six games, but first three probably or four, we would have to...</v>

00:20:47.381 --> 00:20:50.981
<v Michael Gottlieb>Right, because then we'll have some baseline. Yeah.</v>

00:20:48.501 --> 00:20:51.821
<v Efim Podvoiski>Look, look closely and say different, and...</v>

00:20:52.581 --> 00:21:11.141
<v Michael Gottlieb>But then we'll have some baseline math characteristics and behaviors and say, oh, okay, we now know that one in 240 with a minimum of two party time rounds when party time triggers at $10 per party time at a dollar bet,</v>

00:20:55.301 --> 00:20:56.981
<v Efim Podvoiski>Yes, yes.</v>

00:21:11.221 --> 00:21:32.021
<v Michael Gottlieb>that feels good so that we can take that template and then build on it. So yeah, Efim is right. The more of this we do, the better at it we become because we build on our confidence factors of previous. So we started from Bupkus. We started with nothing with Lions Riches and started playing with it.</v>

00:21:32.501 --> 00:21:43.061
<v Michael Gottlieb>And we have that dialed in. Now we want to tackle rodeo spins because that's a weird, it's an outlier, it's a weird bird because it's a single line game with a fourth reel modifier.</v>

00:22:26.581 --> 00:22:30.421
<v Val Levitan>You have three parts that...</v>

00:22:32.341 --> 00:22:40.021
<v Val Levitan>You're saying my 100% money contribution will go into these three parts: base game.</v>

00:22:41.181 --> 00:22:46.261
<v Val Levitan>the party time game, and the free speeches.</v>

00:22:44.981 --> 00:22:45.701
<v Michael Gottlieb>Free spins.</v>

00:22:48.181 --> 00:22:53.301
<v Val Levitan>And my big win is the party time.</v>

00:22:54.501 --> 00:23:05.781
<v Val Levitan>But it can only happen, and you would say one in, it could be triggered one in, let's support two. Okay, I was going to say two one. Okay, two fold.</v>

00:23:01.381 --> 00:23:02.181
<v Michael Gottlieb>240.</v>

00:23:07.141 --> 00:23:07.941
<v Val Levitan>And.</v>

00:23:09.301 --> 00:23:11.461
<v Val Levitan>I will win somewhere from.</v>

00:23:12.541 --> 00:23:15.781
<v Val Levitan>100 to 500 credits.</v>

00:23:15.301 --> 00:23:15.821
<v Efim Podvoiski>No.</v>

00:23:17.061 --> 00:23:17.461
<v Efim Podvoiski>No.</v>

00:23:17.141 --> 00:23:18.261
<v Michael Gottlieb>Depends on that level.</v>

00:23:19.221 --> 00:23:19.781
<v Val Levitan>Sorry.</v>

00:23:20.101 --> 00:23:21.301
<v Michael Gottlieb>Depends on bet level.</v>

00:23:24.821 --> 00:23:26.661
<v Val Levitan>At a maximum bet, let's say.</v>

00:23:27.781 --> 00:23:28.421
<v Efim Podvoiski>So, yeah.</v>

00:23:28.221 --> 00:23:30.341
<v Michael Gottlieb>Our maximum bet is now 3 bucks.</v>

00:23:31.021 --> 00:23:31.381
<v Val Levitan>What?</v>

00:23:32.181 --> 00:23:36.181
<v Efim Podvoiski>So, in party time, even from 60 to...</v>

00:23:38.021 --> 00:23:38.741
<v Michael Gottlieb>180.</v>

00:23:38.421 --> 00:23:40.421
<v Val Levitan>Sorry, we can talk about multiplier.</v>

00:23:39.501 --> 00:23:42.501
<v Efim Podvoiski>Two to two, 200 to 200.</v>

00:23:42.341 --> 00:23:42.821
<v Michael Gottlieb>Yeah.</v>

00:23:43.701 --> 00:23:44.421
<v Efim Podvoiski>Butter then.</v>

00:23:44.261 --> 00:23:49.141
<v Val Levitan>From from multiplier 60 to multiplier 200, did you say?</v>

00:23:49.621 --> 00:23:51.141
<v Efim Podvoiski>Yes, 18, yeah.</v>

00:23:55.781 --> 00:24:03.141
<v Val Levitan>Okay, so if it's 3 bucks, so you're gonna win, yeah, roughly from 180 to 600.</v>

00:24:04.501 --> 00:24:06.661
<v Efim Podvoiski>Oh, sorry, sorry, sorry, sorry.</v>

00:24:08.181 --> 00:24:18.101
<v Efim Podvoiski>No, I am, if I was talking about, sorry, I was confused. Four of multiplier is 10 to 60.</v>

00:24:19.221 --> 00:24:23.941
<v Val Levitan>Ten to 60, so you will weigh in somewhere between 30.</v>

00:24:20.821 --> 00:24:21.781
<v Efim Podvoiski>Alright, alright.</v>

00:24:25.061 --> 00:24:25.821
<v Val Levitan>And 180.</v>

00:24:26.261 --> 00:24:26.741
<v Efim Podvoiski>Yes.</v>

00:24:30.581 --> 00:24:36.501
<v Val Levitan>And you will win, and that will trigger one in 240 times.</v>

00:24:36.581 --> 00:24:37.061
<v Efim Podvoiski>Yes.</v>

00:24:37.821 --> 00:24:39.461
<v Michael Gottlieb>For Lions Riches specifically, yeah.</v>

00:24:41.701 --> 00:24:45.701
<v Val Levitan>So when you establish, let's say, that sweet spot.</v>

00:24:48.901 --> 00:24:49.541
<v Val Levitan>Is it?</v>

00:24:50.661 --> 00:24:58.821
<v Val Levitan>Similar for other games that have party time, I mean similar credit contribution on a $3 bet.</v>

00:25:00.181 --> 00:25:01.221
<v Val Levitan>And, and the.</v>

00:25:02.461 --> 00:25:03.381
<v Val Levitan>Hit frequency.</v>

00:25:04.341 --> 00:25:08.061
<v Michael Gottlieb>Not necessarily, because all the games, all the games are different.</v>

00:25:04.421 --> 00:25:06.661
<v Val Levitan>I'm asking, I'm asking, I don't know.</v>

00:25:08.661 --> 00:25:09.621
<v Efim Podvoiski>But.</v>

00:25:09.141 --> 00:25:09.461
<v Michael Gottlieb>All the.</v>

00:25:10.821 --> 00:25:12.421
<v Efim Podvoiski>But you, I mean, because...</v>

00:25:11.221 --> 00:25:15.861
<v Val Levitan>I know, I know that, I know that all games are different. I understand this.</v>

00:25:16.821 --> 00:25:19.541
<v Efim Podvoiski>You should, you mean pre pre premier games or what?</v>

00:25:21.381 --> 00:25:22.901
<v Efim Podvoiski>Oh, I'm confused.</v>

00:25:23.061 --> 00:25:23.861
<v Val Levitan>Very good.</v>

00:25:25.821 --> 00:25:27.701
<v Val Levitan>While we're discussing her never games.</v>

00:25:28.301 --> 00:25:37.381
<v Michael Gottlieb>No, no, he's talking about our game, Efim. He means, he means of, he means of the games that we're doing, of the six games that we're doing.</v>

00:25:28.421 --> 00:25:32.341
<v Efim Podvoiski>No, you said other games is party time, but the only...</v>

00:25:40.101 --> 00:26:00.341
<v Michael Gottlieb>And the answer, Val, is that it varies on a game-by-game basis because the party time hit frequency is partially derived from the free spins hit frequency, and the free spins hit frequency varies on a game-by-game basis.</v>

00:26:01.221 --> 00:26:02.981
<v Michael Gottlieb>So, for that.</v>

00:26:02.821 --> 00:26:04.821
<v Val Levitan>I understand, but...</v>

00:26:06.981 --> 00:26:13.861
<v Val Levitan>So let's say Lions reaches, you establish that hit frequency for party time is 1 in 240.</v>

00:26:15.221 --> 00:26:21.861
<v Val Levitan>and you're pretty well happy with it. Whatever, whether it's right or wrong, doesn't matter. You feel that this is the right thing.</v>

00:26:17.381 --> 00:26:17.861
<v Michael Gottlieb>Yes.</v>

00:26:22.341 --> 00:26:22.661
<v Michael Gottlieb>Right.</v>

00:26:22.901 --> 00:26:25.701
<v Val Levitan>OK, so if...</v>

00:26:26.981 --> 00:26:31.221
<v Val Levitan>If the games that were designing other five games that were designing.</v>

00:26:32.261 --> 00:26:33.701
<v Val Levitan>Have 3?</v>

00:26:35.061 --> 00:26:37.301
<v Val Levitan>Pots base game.</v>

00:26:38.501 --> 00:26:45.221
<v Val Levitan>Free spins and party time - wouldn't the second, third, or other games?</v>

00:26:46.341 --> 00:26:57.941
<v Val Levitan>have the same or wouldn't you want all the rest of the games to have one in 240 hit frequency for party time?</v>

00:26:58.181 --> 00:26:59.701
<v Michael Gottlieb>No, not necessarily.</v>

00:27:00.661 --> 00:27:03.941
<v Val Levitan>Okay, so this is what I'm not understanding. Why not?</v>

00:27:04.341 --> 00:27:12.181
<v Michael Gottlieb>Because some games are hard have harder math and some games have softer math and that math a lot.</v>

00:27:11.381 --> 00:27:11.861
<v Val Levitan>What the?</v>

00:27:13.101 --> 00:27:14.581
<v Val Levitan>But it will probably.</v>

00:27:15.701 --> 00:27:17.621
<v Val Levitan>Still be somewhere between.</v>

00:27:18.981 --> 00:27:20.581
<v Val Levitan>Two 100 and 300.</v>

00:27:19.301 --> 00:27:19.781
<v Efim Podvoiski>It's what?</v>

00:27:21.061 --> 00:27:24.901
<v Efim Podvoiski>Yes, yes, not radically different, not radically different.</v>

00:27:22.821 --> 00:27:24.821
<v Michael Gottlieb>Yeah, theoretically.</v>

00:27:26.261 --> 00:27:31.781
<v Michael Gottlieb>But we'll see, we don't know. It's entirely possible that, you know, if we get something that...</v>

00:27:34.421 --> 00:27:49.141
<v Michael Gottlieb>is too much of A hammer, will pull party time in and have it happen a little more often so you don't feel like, because if you're getting a ton of zeros, you got to throw some meat to the wolves, okay? It's A volatility. Yeah, yeah.</v>

00:27:46.941 --> 00:28:06.101
<v Val Levitan>No, I understand. No, I understand. I understand. But I'm just trying to understand the depth of this fine-tuning. I mean, you're still fine-tuning between 2 and 300, but I'm going to call it three parts of wins, base,</v>

00:28:07.381 --> 00:28:09.141
<v Val Levitan>Free games, and...</v>

00:28:08.661 --> 00:28:09.141
<v Michael Gottlieb>Mhm.</v>

00:28:10.301 --> 00:28:14.901
<v Val Levitan>they still have to hit somewhere between an acceptable rate of frequency.</v>

00:28:16.341 --> 00:28:30.821
<v Val Levitan>So, what is that rate of frequency that you are contemplating? It's known that it's known in the industry, right? It's not a complete.</v>

00:28:32.581 --> 00:28:33.221
<v Michael Gottlieb>Mystery.</v>

00:28:33.781 --> 00:28:34.421
<v Val Levitan>Yeah.</v>

00:28:34.501 --> 00:28:54.261
<v Michael Gottlieb>Yeah, no, it's not a complete mystery. Your free spins hit rate is pretty well defined and we're locked in with these games on what those are. I guess the point I'm making is that if you have a game where the free spins are, you know, more like one and 150, you can't do it linearly and have</v>

00:28:54.301 --> 00:29:14.101
<v Michael Gottlieb>party time be one and 300. You would conceivably take your free spins from one and 150 down to one and 120 to help potentially adjust or you might push free spins out a little bit depending upon.</v>

00:29:14.341 --> 00:29:16.901
<v Michael Gottlieb>How, what money you want, where you want it to go?</v>

00:29:16.901 --> 00:29:36.021
<v Val Levitan>I, I fully, I fully understand, like I, I have 100% comprehension with this. I'm trying to establish in JVL's rules and what's our house rule for designing games? What's the hit frequency for?</v>

00:29:18.901 --> 00:29:19.301
<v Michael Gottlieb>Yeah.</v>

00:29:36.581 --> 00:29:40.261
<v Val Levitan>each of those parts an interval. Can you give it to me?</v>

00:29:41.541 --> 00:29:50.021
<v Michael Gottlieb>I would, well, there it does vary, it varies on a game to game basis, but I would say one, one and 120, one and 120 for free spins.</v>

00:29:45.381 --> 00:29:47.541
<v Val Levitan>I know, but I'm talking about the interval.</v>

00:29:50.821 --> 00:29:58.021
<v Val Levitan>Okay, one and 120 for free spins, one and 240 for, let's call it large.</v>

00:29:59.141 --> 00:30:00.021
<v Michael Gottlieb>For party time.</v>

00:30:01.461 --> 00:30:16.261
<v Val Levitan>Well, I intentionally didn't want to call it Party Time because Party Time is something that you coined for Class A games, but it's actually a pretty good name. So you could probably apply it to...</v>

00:30:11.301 --> 00:30:11.701
<v Michael Gottlieb>Right.</v>

00:30:22.741 --> 00:30:24.101
<v Michael Gottlieb>Right, right.</v>

00:30:24.141 --> 00:30:31.381
<v Val Levitan>One and 240 free spins is 1 and 120, and what's the hit frequency in base gain?</v>

00:30:33.221 --> 00:30:36.261
<v Val Levitan>One in one in 80, one in 60.</v>

00:30:36.581 --> 00:30:37.541
<v Efim Podvoiski>Hear frequency.</v>

00:30:37.861 --> 00:30:40.741
<v Michael Gottlieb>There, it's not like that. There's a there's what?</v>

00:30:39.941 --> 00:30:40.821
<v Efim Podvoiski>Wants.</v>

00:30:40.181 --> 00:30:43.941
<v Val Levitan>Yeah, base, yeah, base game because the partial wins.</v>

00:30:44.181 --> 00:30:48.661
<v Michael Gottlieb>It's a wind distribution curve. There's a wind distribution curve that we have.</v>

00:30:50.941 --> 00:30:56.101
<v Michael Gottlieb>I don't know if you, do you have one accessible theme? Can you bring up a win distribution curve of just any game?</v>

00:30:57.141 --> 00:30:58.021
<v Efim Podvoiski>Give me a second.</v>

00:30:58.501 --> 00:30:58.821
<v Michael Gottlieb>Yeah.</v>

00:31:05.461 --> 00:31:24.781
<v Michael Gottlieb>Because that kind of shows where it gets complicated. It's of the EV of the base game, what percentage of that EV is assigned to winning two times your bet, three times your bet, for the da da da da. So it goes up.</v>

00:31:24.861 --> 00:31:40.261
<v Michael Gottlieb>And then it falls off because obviously winning huge multiples of your bet, the hit frequency of that happening is significantly lower. So that win profile is something that Efim and I massage and play with.</v>

00:31:43.301 --> 00:32:04.981
<v Michael Gottlieb>And yes, we look at the most successful games and we look at the win profiles of those games, and then we take that win profile and look at, you know, what it is players are responding to, and then we adapt it to other games. And then we look at our games that have failed, and we look at those win profiles to determine, well, is it the theme or is there something about the math that people absolutely hate?</v>

00:32:08.181 --> 00:32:09.061
<v Michael Gottlieb>Okay, here you go.</v>

00:32:08.301 --> 00:32:09.301
<v Efim Podvoiski>And this is.</v>

00:32:10.501 --> 00:32:13.701
<v Efim Podvoiski>Yes, this is how, what was the portion of...</v>

00:32:15.341 --> 00:32:20.661
<v Efim Podvoiski>What portion of RTP is put into each interval?</v>

00:32:21.941 --> 00:32:26.421
<v Efim Podvoiski>For example, here you see that for interval from...</v>

00:32:28.101 --> 00:32:29.301
<v Efim Podvoiski>Two to four.</v>

00:32:30.821 --> 00:32:31.861
<v Efim Podvoiski>That's win.</v>

00:32:33.141 --> 00:32:38.341
<v Efim Podvoiski>You we put 14% of RTP goes into these bins.</v>

00:32:40.901 --> 00:32:48.181
<v Efim Podvoiski>So in the this gray one is Lyashenko, which is well accepted by players.</v>

00:32:49.301 --> 00:32:53.221
<v Efim Podvoiski>So, I tried this party time not to go too far from this.</v>

00:32:54.741 --> 00:33:02.221
<v Val Levitan>So, that's very interesting. I assume that you could probably move this fusion.</v>

00:33:04.181 --> 00:33:05.141
<v Val Levitan>Gruff.</v>

00:33:06.261 --> 00:33:06.741
<v Efim Podvoiski>Sorry?</v>

00:33:10.101 --> 00:33:14.341
<v Val Levitan>You could, you could probably move the the.</v>

00:33:15.621 --> 00:33:22.021
<v Val Levitan>Li lines and li lines riches, the fuchsia colored.</v>

00:33:23.221 --> 00:33:25.941
<v Val Levitan>Scale. We could probably move it, right?</v>

00:33:26.901 --> 00:33:38.021
<v Efim Podvoiski>Move it? No, no, I cannot. No, it's not like, no, I cannot move it here. I have to change the distribution and then I get the outcomes and I see it.</v>

00:33:39.301 --> 00:33:39.781
<v Efim Podvoiski>Why?</v>

00:33:40.981 --> 00:33:46.021
<v Efim Podvoiski>I don't even, I don't have to run the game, but I have to go somewhere, get the values sent.</v>

00:33:46.981 --> 00:33:50.021
<v Val Levitan>I guess my question is, can you?</v>

00:33:47.461 --> 00:33:48.581
<v Efim Podvoiski>You get it here.</v>

00:33:52.581 --> 00:33:57.701
<v Val Levitan>Emulate the gray graph more exactly.</v>

00:33:59.621 --> 00:34:02.101
<v Val Levitan>Like without the deviation in the beginning.</v>

00:34:07.181 --> 00:34:09.301
<v Val Levitan>And maybe I'm asking stupid questions, I don't know.</v>

00:34:09.061 --> 00:34:13.221
<v Efim Podvoiski>No, no, no, it's not. It's a right question, but we have...</v>

00:34:09.221 --> 00:34:10.581
<v Michael Gottlieb>No, no, I, you're.</v>

00:34:11.941 --> 00:34:12.421
<v Michael Gottlieb>Yeah.</v>

00:34:15.221 --> 00:34:18.021
<v Efim Podvoiski>Uh, yes, but uh...</v>

00:34:19.701 --> 00:34:33.781
<v Efim Podvoiski>I think it's close enough in this stage and there are some features that prevent from freely moving it because here we introduced party time, we moved</v>

00:34:35.541 --> 00:34:46.821
<v Efim Podvoiski>some wins from free spins into party time and it's changed a little bit this distribution. But essentially it's not that different actually.</v>

00:34:47.661 --> 00:34:53.541
<v Michael Gottlieb>especially in the what I call the meaty middle, which is that 10 times your bet.</v>

00:34:55.061 --> 00:35:10.421
<v Michael Gottlieb>Moving up there, the peak of the mountain. Because the thing is Val, it actually kind of deceptive because you can look at that stuff on the left, but then you have to look at the contribution and the percentages are such that it's not necessarily, you know, that that.</v>

00:34:58.581 --> 00:34:59.061
<v Efim Podvoiski>Yeah.</v>

00:35:11.461 --> 00:35:33.061
<v Michael Gottlieb>that big of a deal, but more importantly, you have to be careful because you can deceive yourself by trying to mold this in a certain way, and then you play the game and you end up with a dribbler that's absolutely awful, or you end up with something that never pays. You get tons of zeros, and then you have these massive, massive wins that are</v>

00:35:33.541 --> 00:35:50.181
<v Michael Gottlieb>that are outliers. So I don't, I've never found these, I found these to be helpful, but I don't find them to be definitive. You have to play the game itself and let the randomness of the game dictate to you the play experience, if that makes any sense.</v>

00:35:54.181 --> 00:36:03.141
<v Michael Gottlieb>Put a different way, the most important thing that we need to achieve, which is that mountain at 10 times your bet and above, we're achieving that.</v>

00:36:04.421 --> 00:36:13.221
<v Val Levitan>At which stage, I'm looking at Jira now. If we could switch to Jira. Thank you, Efim. I appreciate it.</v>

00:36:04.661 --> 00:36:05.301
<v Michael Gottlieb>You know, but...</v>

00:36:15.061 --> 00:36:21.621
<v Val Levitan>At which stage are you guys working on the math? Is it the concept stage?</v>

00:36:22.621 --> 00:36:27.861
<v Michael Gottlieb>Sometimes it depends on if we're doing something completely new or if it's something.</v>

00:36:22.981 --> 00:36:23.221
<v Efim Podvoiski>Uhh.</v>

00:36:26.821 --> 00:36:28.021
<v Efim Podvoiski>You just see us.</v>

00:36:29.541 --> 00:36:32.821
<v Michael Gottlieb>Yeah, in this case, yes, right, because we haven't and and it.</v>

00:36:31.861 --> 00:36:36.221
<v Efim Podvoiski>Because we are trying this party time, an absolutely new concept.</v>

00:36:34.661 --> 00:36:53.101
<v Michael Gottlieb>Right. And Lena's team schedule is not necessarily the same as our schedule. And so if Efim has bandwidth and we have a premise and a theory and we want to cook on something, we will absolutely work on it in the concept phase. If it's something else that's more...</v>

00:36:54.741 --> 00:37:18.381
<v Michael Gottlieb>defined, then we will defer it. We'll kick the can down the road because we know we can deal with that. But from a risk management standpoint, philosophically, you want to front load your risk and you need to get this blank and figured out now because this is one of the, this is it. This is the most important element and aspect of what Class A is, is this whole party time experience.</v>

00:37:19.621 --> 00:37:21.781
<v Michael Gottlieb>So that's why we're focusing on it right now.</v>

00:37:22.421 --> 00:37:31.461
<v Efim Podvoiski>But actually, actually, the tasks we were put on game design. I'm sorry. Yeah, for for confusion. It's actually in game designs.</v>

00:37:31.781 --> 00:37:45.141
<v Michael Gottlieb>Right, but we started talking about this extensively before it ever got to the design phase. So I would say it's a gray area. It is bled from the game concept phase over into the game design phase.</v>

00:37:33.781 --> 00:37:35.461
<v Efim Podvoiski>Yes, yes, yes.</v>

00:37:36.901 --> 00:37:38.341
<v Efim Podvoiski>Yes, yes, yeah.</v>

00:37:45.861 --> 00:37:50.581
<v Lena Zhukova>But where it's in game design, because class A.</v>

00:37:50.181 --> 00:37:52.901
<v Efim Podvoiski>Under IP 1197.</v>

00:37:53.461 --> 00:37:58.021
<v Lena Zhukova>Right, why, why, why it doesn't show it here?</v>

00:37:59.221 --> 00:37:59.901
<v Efim Podvoiski>That doesn't?</v>

00:38:00.501 --> 00:38:01.701
<v Lena Zhukova>No, it doesn't.</v>

00:38:02.101 --> 00:38:06.661
<v Efim Podvoiski>I under IP 1197 there is cap 286.</v>

00:38:08.501 --> 00:38:12.261
<v Lena Zhukova>No, I'm sharing. See, it's everything is done here.</v>

00:38:12.941 --> 00:38:13.461
<v Efim Podvoiski>What?</v>

00:38:15.861 --> 00:38:18.901
<v Lena Zhukova>Should I update, but I updated 2 minutes ago?</v>

00:38:20.901 --> 00:38:25.861
<v Efim Podvoiski>So I don't see the issue on 1197, yes? I don't understand.</v>

00:38:24.741 --> 00:38:25.141
<v Lena Zhukova>Yeah.</v>

00:38:25.141 --> 00:38:29.061
<v Michael Gottlieb>Yeah, I know you put tasks in for it. I saw it, but you're right, it's not there now.</v>

00:38:30.581 --> 00:38:30.981
<v Efim Podvoiski>For me.</v>

00:38:30.581 --> 00:38:37.621
<v Michael Gottlieb>Has it been done for so long that it got blown out? Because if it's done for 30 days, it goes away, but that hasn't been done for 30 days.</v>

00:38:36.741 --> 00:38:41.541
<v Lena Zhukova>But no, no, now now I am opening like inside it, so it it so it was.</v>

00:38:37.061 --> 00:38:37.781
<v Efim Podvoiski>No.</v>

00:38:40.741 --> 00:38:43.221
<v Efim Podvoiski>No, I see it. I don't know what...</v>

00:38:45.701 --> 00:38:46.501
<v Lena Zhukova>She, I do.</v>

00:38:49.461 --> 00:38:53.101
<v Efim Podvoiski>I don't understand. It's capability, it's not a...</v>

00:38:53.221 --> 00:39:01.141
<v Lena Zhukova>Ohh, it's capability, I, because I don't, I don't see capability, so that probably I don't have filter or something, I don't see.</v>

00:38:53.381 --> 00:38:54.421
<v Val Levitan>So, it takes.</v>

00:38:55.701 --> 00:38:56.101
<v Val Levitan>So.</v>

00:39:00.421 --> 00:39:03.061
<v Efim Podvoiski>Ah, you probably filtered capability out or something.</v>

00:39:02.421 --> 00:39:05.461
<v Lena Zhukova>I, I did not work this capability before, so...</v>

00:39:03.061 --> 00:39:03.461
<v Val Levitan>It.</v>

00:39:07.061 --> 00:39:07.381
<v Val Levitan>Okay.</v>

00:39:07.941 --> 00:39:09.301
<v Lena Zhukova>How should I go there?</v>

00:39:10.261 --> 00:39:14.101
<v Efim Podvoiski>No, I don't know for people for me, just showing the time.</v>

00:39:12.701 --> 00:39:16.101
<v Lena Zhukova>And maybe I don't even have access to there, so I need to ask.</v>

00:39:18.341 --> 00:39:19.141
<v Efim Podvoiski>That's maybe.</v>

00:39:24.661 --> 00:39:26.261
<v Lena Zhukova>So maybe you can share your screen.</v>

00:39:26.901 --> 00:39:27.861
<v Efim Podvoiski>Okay, so...</v>

00:39:31.021 --> 00:39:33.461
<v Lena Zhukova>Because I, I strangely, I don't see it.</v>

00:39:34.901 --> 00:39:40.421
<v Lena Zhukova>And they, I need to have take a screenshot and send it to our IT guys and ask why I don't see it.</v>

00:39:44.661 --> 00:39:46.181
<v Lena Zhukova>I need to have access to it.</v>

00:39:47.101 --> 00:39:47.781
<v Efim Podvoiski>You just...</v>

00:39:49.221 --> 00:39:50.061
<v Efim Podvoiski>The Beat.</v>

00:39:49.981 --> 00:39:56.861
<v Lena Zhukova>No, I see, I, I, I don't see exist cups. OK, yeah, so maybe Michael doesn't have access to that.</v>

00:39:52.581 --> 00:39:53.861
<v Michael Gottlieb>Yeah, I don't see that either.</v>

00:39:57.061 --> 00:39:57.541
<v Michael Gottlieb>No.</v>

00:39:58.581 --> 00:39:59.301
<v Efim Podvoiski>All interesting.</v>

00:40:25.861 --> 00:40:28.981
<v Val Levitan>So, again, if I look at...</v>

00:40:30.661 --> 00:40:31.541
<v Val Levitan>Classy.</v>

00:40:33.061 --> 00:40:34.261
<v Val Levitan>For Giorgi.</v>

00:40:39.061 --> 00:40:40.621
<v Val Levitan>I can see that.</v>

00:40:44.221 --> 00:40:48.501
<v Val Levitan>the design stage, sorry, the concept stage is practically done, right?</v>

00:40:48.501 --> 00:40:48.981
<v Michael Gottlieb>Yes.</v>

00:40:49.941 --> 00:40:58.101
<v Val Levitan>So does it mean that you guys have the idea of how the math will work?</v>

00:40:59.221 --> 00:41:01.701
<v Val Levitan>On the Class A machines.</v>

00:41:01.701 --> 00:41:03.541
<v Michael Gottlieb>Yes, it means we have a sense of it.</v>

00:41:06.981 --> 00:41:08.821
<v Michael Gottlieb>But it'll definitively get done in the...</v>

00:41:07.101 --> 00:41:25.861
<v Efim Podvoiski>We have a, we have a, we have exactly, we have a concept, but design is the next stage. The actual, we have a concept that we agreed on that we will have party time which is proportional to the bed, and that's an important point, and we have some idea how often the party time should happen.</v>

00:41:11.501 --> 00:41:11.861
<v Val Levitan>And...</v>

00:41:26.421 --> 00:41:27.141
<v Lena Zhukova>Alright.</v>

00:41:26.581 --> 00:41:29.141
<v Efim Podvoiski>And from that, we go into the details.</v>

00:41:29.501 --> 00:41:31.781
<v Michael Gottlieb>And we have the storyboards of how the mechanic will work.</v>

00:41:30.101 --> 00:41:30.461
<v Lena Zhukova>Absolutely.</v>

00:41:32.501 --> 00:41:39.301
<v Lena Zhukova>Hey, Kim, can you move for the IP 1197 in progress, because otherwise it's very confusing?</v>

00:41:39.461 --> 00:41:40.261
<v Efim Podvoiski>Ohh, OK.</v>

00:41:51.781 --> 00:42:04.661
<v Lena Zhukova>I think you need to renew first, and then one day you can go to the next. You need to you need to refresh the page, yeah, save your changes, and only then you can go to the next step.</v>

00:41:54.741 --> 00:41:56.341
<v Efim Podvoiski>Sorry, I sent you.</v>

00:41:58.261 --> 00:42:00.901
<v Val Levitan>Very fresh, very fresh.</v>

00:42:03.221 --> 00:42:03.781
<v Efim Podvoiski>Oh.</v>

00:42:26.701 --> 00:42:26.821
<v Val Levitan>Yeah.</v>

00:42:36.901 --> 00:42:38.261
<v Lena Zhukova>In progress, and then...</v>

00:42:41.941 --> 00:42:43.541
<v Lena Zhukova>And refresh again, please.</v>

00:42:44.341 --> 00:42:45.621
<v Efim Podvoiski>Okay, okay, okay, sir.</v>

00:42:47.381 --> 00:42:48.501
<v Efim Podvoiski>Keep forgetting about this.</v>

00:42:48.661 --> 00:43:00.301
<v Lena Zhukova>Okay. Great. I will ask IT guys why me and Michael don't see this capabilities level, so we probably need to have access to it.</v>

00:42:53.181 --> 00:42:53.541
<v Val Levitan>People.</v>

00:43:06.701 --> 00:43:07.221
<v Lena Zhukova>Anton.</v>

00:43:06.821 --> 00:43:12.101
<v Val Levitan>I am, I am 90% sure that it's not an access issue, but it's...</v>

00:43:13.541 --> 00:43:17.221
<v Val Levitan>a setup on your screen. I mean on your...</v>

00:43:18.661 --> 00:43:19.461
<v Val Levitan>In your Giorgi.</v>

00:43:20.741 --> 00:43:29.781
<v Lena Zhukova>Okay, I will ask you guys because it's not only in timeline, but also when I go inside the IP, I don't see this capability on the voice.</v>

00:43:29.381 --> 00:43:30.021
<v Efim Podvoiski>You're right.</v>

00:43:31.701 --> 00:43:32.981
<v Val Levitan>Yeah, ask, yeah.</v>

00:43:33.501 --> 00:43:33.981
<v Lena Zhukova>Mhm.</v>

00:43:36.741 --> 00:43:37.861
<v Val Levitan>Okay, so...</v>

00:43:39.861 --> 00:43:45.861
<v Val Levitan>Thank you, I appreciate it. So then back to the schedule. So from my understanding.</v>

00:43:47.381 --> 00:43:47.621
<v Val Levitan>Um...</v>

00:43:53.461 --> 00:43:58.461
<v Val Levitan>And again, when I, when I just look at the schedule, right, I'm trying to kind of...</v>

00:43:59.581 --> 00:44:02.021
<v Val Levitan>Get a quick visual comprehension.</v>

00:44:05.541 --> 00:44:08.461
<v Val Levitan>So, the, and I'm only referring to Class A right now.</v>

00:44:10.661 --> 00:44:29.221
<v Val Levitan>So I understand that the concept stage is done. In my mind, that means that you guys pretty well understand what you're doing with games. You have your concept, you have your kind of, maybe not fully, but your math is worked out more or less.</v>

00:44:31.061 --> 00:44:45.701
<v Val Levitan>And I see that Class A right now is in design stage. The actual schedule shows that it's continuing, but it's actually done. So you came ahead of schedule.</v>

00:44:46.661 --> 00:44:50.101
<v Lena Zhukova>Uh, Efim just refreshed it and move it and progress.</v>

00:44:56.421 --> 00:44:58.981
<v Val Levitan>Sorry, please say it again.</v>

00:45:00.101 --> 00:45:01.221
<v Michael Gottlieb>You have to hit refresh.</v>

00:45:00.501 --> 00:45:00.821
<v Lena Zhukova>Ohh.</v>

00:45:07.781 --> 00:45:10.821
<v Val Levitan>Ah, okay, it's in progress. Got it, got it.</v>

00:45:13.381 --> 00:45:16.981
<v Val Levitan>Uh, okay, so then...</v>

00:45:38.341 --> 00:45:43.141
<v Val Levitan>Again, only as I look at the schedule.</v>

00:45:44.021 --> 00:45:50.421
<v Val Levitan>Again, in the game design for Class A, I kind of understand that math is already done.</v>

00:45:51.061 --> 00:45:51.621
<v Efim Podvoiski>No.</v>

00:45:52.101 --> 00:45:55.381
<v Val Levitan>About like any, any, any moment now.</v>

00:45:56.261 --> 00:45:56.821
<v Val Levitan>Yes?</v>

00:45:57.221 --> 00:45:57.861
<v Efim Podvoiski>No, no.</v>

00:46:01.381 --> 00:46:02.581
<v Val Levitan>Ohh, I'm just...</v>

00:46:01.541 --> 00:46:06.021
<v Michael Gottlieb>That's the point that we're making is that these capabilities aren't showing up in the schedule.</v>

00:46:06.421 --> 00:46:16.661
<v Efim Podvoiski>It's not even, it's even, mass is done, it means a lot of things, like production mass done, it's not even touched yet.</v>

00:46:17.941 --> 00:46:21.941
<v Efim Podvoiski>They are not in the station, because it's something new, something totally new.</v>

00:46:20.421 --> 00:46:27.141
<v Val Levitan>I am, I am, I am referring to a game design, so in the design stage.</v>

00:46:26.341 --> 00:46:30.101
<v Efim Podvoiski>No, no, not done, not done, and did...</v>

00:46:29.621 --> 00:46:35.701
<v Val Levitan>No, I see it. I see that it's not done. I'm just looking at the time bar. I'm just reading.</v>

00:46:36.261 --> 00:46:38.341
<v Efim Podvoiski>Ah, okay, because, because we...</v>

00:46:36.701 --> 00:46:38.661
<v Val Levitan>And I'm not, I'm not, I'm not.</v>

00:46:42.021 --> 00:46:42.181
<v Val Levitan>Okay.</v>

00:46:45.301 --> 00:46:45.861
<v Val Levitan>Go ahead.</v>

00:46:46.581 --> 00:46:50.181
<v Efim Podvoiski>Because we didn't add the following tasks.</v>

00:46:51.541 --> 00:46:56.421
<v Efim Podvoiski>And I didn't know, even didn't realize that they will be there.</v>

00:46:59.381 --> 00:47:08.501
<v Efim Podvoiski>When I started, when I did the first one, I did realize it will be the second and the third. But now I realize that there will be four of them probably.</v>

00:47:16.581 --> 00:47:17.061
<v Val Levitan>Okarak.</v>

00:47:18.221 --> 00:47:19.781
<v Val Levitan>When I look at schedule.</v>

00:47:21.221 --> 00:47:22.981
<v Val Levitan>What should I look at?</v>

00:47:24.101 --> 00:47:29.941
<v Val Levitan>How should I read it in order to have my own understanding of what's happening?</v>

00:47:43.101 --> 00:47:43.901
<v Michael Gottlieb>What the ants?</v>

00:47:43.101 --> 00:47:45.621
<v Val Levitan>What is the good? What is the good system?</v>

00:47:46.181 --> 00:47:52.741
<v Michael Gottlieb>The answer is that it needs to be correctly populated with these math tasks. That's the answer.</v>

00:47:52.141 --> 00:47:54.661
<v Val Levitan>OKOK, why are you doing?</v>

00:47:55.381 --> 00:47:55.861
<v Michael Gottlieb>The theme.</v>

00:47:57.221 --> 00:48:00.981
<v Val Levitan>Okay. Before the meeting or after the meeting?</v>

00:48:02.501 --> 00:48:08.101
<v Michael Gottlieb>Well, ideally before the meeting, we're identifying for some reason that he has actually put it in here, but we're not seeing it.</v>

00:48:11.701 --> 00:48:15.301
<v Val Levitan>Okay, so should we check what we see?</v>

00:48:16.501 --> 00:48:20.461
<v Val Levitan>In preparation to the meeting, or should we discover it at the meeting?</v>

00:48:21.781 --> 00:48:24.821
<v Michael Gottlieb>Should absolutely be in preparation before the meeting, of course.</v>

00:48:25.621 --> 00:48:28.101
<v Val Levitan>Okay, can we please, as a group?</v>

00:48:30.101 --> 00:48:32.421
<v Val Levitan>Take an undertaking of.</v>

00:48:34.181 --> 00:48:35.381
<v Val Levitan>Abolishing this off.</v>

00:48:37.141 --> 00:48:39.501
<v Val Levitan>All right, moving on.</v>

00:48:41.461 --> 00:48:42.821
<v Val Levitan>Game production.</v>

00:48:44.581 --> 00:48:51.741
<v Val Levitan>I'm only referring to Class A. So when I look at game production, my understanding that it's not scheduled.</v>

00:48:52.381 --> 00:48:52.901
<v Lena Zhukova>Inna.</v>

00:48:53.941 --> 00:48:56.901
<v Val Levitan>OK, so I'm actually reading it correctly, right?</v>

00:48:57.301 --> 00:48:57.621
<v Lena Zhukova>Yeah.</v>

00:48:58.501 --> 00:48:59.701
<v Val Levitan>Okay, thank you.</v>

00:49:00.981 --> 00:49:04.021
<v Val Levitan>So then, I'm asking a question.</v>

00:49:05.141 --> 00:49:10.021
<v Val Levitan>It's not scheduled because you don't have all the game.</v>

00:49:12.021 --> 00:49:15.701
<v Val Levitan>Class A game design ideas.</v>

00:49:17.221 --> 00:49:19.701
<v Val Levitan>You need to design something more.</v>

00:49:21.061 --> 00:49:24.421
<v Val Levitan>or probe something, test, spike.</v>

00:49:25.781 --> 00:49:28.421
<v Val Levitan>before you can schedule production.</v>

00:49:29.381 --> 00:49:34.981
<v Val Levitan>or you just don't want to schedule production, or you don't have resources.</v>

00:49:35.781 --> 00:49:40.901
<v Val Levitan>for production, therefore you're not scheduling it. I'm just trying to understand.</v>

00:49:41.061 --> 00:50:00.181
<v Lena Zhukova>Yeah, I just thought it's a little bit early to schedule it in production because we only will start it after we will finish Nebraska. So it's going to be in January 2027 and it's going to be in NOAA. And first of all, I need to understand more clearly what is going to be the flow.</v>

00:50:00.341 --> 00:50:13.461
<v Lena Zhukova>Of working in this new framework, I am talking now to Igor and talking to Anton Leshkevich. I'm trying to understand the flow and steps and what are going on.</v>

00:50:11.861 --> 00:50:15.101
<v Val Levitan>And what are they, and what are they, what are they telling you?</v>

00:50:15.861 --> 00:50:20.741
<v Lena Zhukova>So, if they're telling me this is going to be like new, um...</v>

00:50:22.861 --> 00:50:43.301
<v Lena Zhukova>environment when we are going to assemble games using AI, but they don't have clear vision yet, but they are working on it. So that I think we will continue to discuss it and in December probably we will have a clear picture and I will start to schedule.</v>

00:50:45.061 --> 00:50:48.501
<v Val Levitan>Okay, so that's why it's not scheduled, understood.</v>

00:50:49.861 --> 00:50:54.101
<v Val Levitan>Okay, I have my questions on plus I answered.</v>

00:50:56.021 --> 00:50:58.581
<v Val Levitan>Do you have any questions for me, last say?</v>

00:51:02.421 --> 00:51:08.421
<v Michael Gottlieb>As the market, the market's continuing to grow, we're still hearing positive things about it.</v>

00:51:02.581 --> 00:51:03.301
<v Val Levitan>Okarak.</v>

00:51:09.221 --> 00:51:23.301
<v Val Levitan>No, the market doesn't, the market is not growing because Primero is failing and the operators also have hesitation because Class A is not.</v>

00:51:25.541 --> 00:51:26.661
<v Val Levitan>Regulated.</v>

00:51:28.501 --> 00:51:29.461
<v Val Levitan>And so...</v>

00:51:31.061 --> 00:51:35.301
<v Val Levitan>They're hesitating whether even to put it in locations.</v>

00:51:38.261 --> 00:51:43.781
<v Val Levitan>And because it's not me, and because Primero is not making money, there, you know, there's no...</v>

00:51:44.981 --> 00:51:45.621
<v Val Levitan>Growth.</v>

00:51:46.941 --> 00:51:59.301
<v Michael Gottlieb>Well, everything starts with that, right? I mean, if you're not making money, you're just taking capital, you're risking capital, and you're risking the headache, and there's no upside. If there's money, then all of a sudden people's tone changes very quickly.</v>

00:52:00.981 --> 00:52:08.421
<v Val Levitan>Right on. That is exactly what's happening. So the bottom line today is that nobody is interested in it.</v>

00:52:12.141 --> 00:52:13.221
<v Val Levitan>Let me rephrase it.</v>

00:52:17.941 --> 00:52:23.061
<v Val Levitan>Majority of people don't want it in the market because they feel that.</v>

00:52:24.901 --> 00:52:27.461
<v Val Levitan>It will jeopardize their licensing.</v>

00:52:29.381 --> 00:52:35.621
<v Val Levitan>Not even licensing, it will jeopardize, it will possibly alienate legislators.</v>

00:52:38.341 --> 00:52:46.101
<v Val Levitan>or not even that. It will, they don't want to bring, they don't want to surface anything.</v>

00:52:47.701 --> 00:52:48.661
<v Val Levitan>That is.</v>

00:52:49.781 --> 00:52:52.661
<v Val Levitan>Doesn't need to be surfaced. I mean that.</v>

00:52:51.701 --> 00:53:00.181
<v Michael Gottlieb>They will want to give anybody a reason to have a negative perception, attitude, or disposition on the entire thing.</v>

00:53:00.741 --> 00:53:04.581
<v Val Levitan>They don't want any legislators to think that, you know...</v>

00:53:06.341 --> 00:53:09.941
<v Val Levitan>Operators are taking advantage of a loophole in the law.</v>

00:53:12.341 --> 00:53:16.181
<v Val Levitan>And because it's not making money.</v>

00:53:17.701 --> 00:53:20.981
<v Val Levitan>then majority of people think.</v>

00:53:22.501 --> 00:53:27.141
<v Val Levitan>kind of all great. We don't have to worry about it now.</v>

00:53:28.581 --> 00:53:30.341
<v Val Levitan>Let's continue with what we have.</v>

00:53:33.661 --> 00:53:34.341
<v Val Levitan>Which?</v>

00:53:39.461 --> 00:53:43.861
<v Val Levitan>So if we don't make money, then nobody wants it.</v>

00:53:46.741 --> 00:53:54.901
<v Val Levitan>But I do have operators to try it. And if it makes money, then there is a conversation. But it's a shot in the dark.</v>

00:53:57.461 --> 00:54:02.181
<v Val Levitan>But I believe that we should take this shot because...</v>

00:54:05.061 --> 00:54:06.981
<v Val Levitan>We, we need another product.</v>

00:54:10.021 --> 00:54:14.501
<v Val Levitan>And this market will have three new players that are coming in.</v>

00:54:16.901 --> 00:54:17.781
<v Michael Gottlieb>Into Class A.</v>

00:54:18.741 --> 00:54:19.861
<v Val Levitan>Into Class B.</v>

00:54:20.741 --> 00:54:21.301
<v Michael Gottlieb>Okay.</v>

00:54:23.261 --> 00:54:24.181
<v Michael Gottlieb>Who, who is that?</v>

00:54:25.381 --> 00:54:29.701
<v Val Levitan>Well, AGS is coming in, and there are two other new manufacturers.</v>

00:54:46.141 --> 00:54:47.661
<v Val Levitan>Any more questions on Plus A?</v>

00:54:54.101 --> 00:54:57.941
<v Val Levitan>Well, let's go with Class B. I understand that we're working on...</v>

00:54:59.061 --> 00:55:01.941
<v Val Levitan>V4 for Georgia COO.</v>

00:55:03.941 --> 00:55:09.061
<v Michael Gottlieb>I'm going to, yeah, I've done some preliminary work on it, but I haven't really full force.</v>

00:55:10.181 --> 00:55:15.061
<v Michael Gottlieb>Started on it, I have a list of games and some preliminary designs.</v>

00:55:19.461 --> 00:55:23.621
<v Michael Gottlieb>And I will probably get this scheduled next week.</v>

00:55:25.141 --> 00:55:28.581
<v Michael Gottlieb>I'm focused on Nebraska right now, Nebraska in Class A.</v>

00:55:30.341 --> 00:55:33.061
<v Val Levitan>Okay, no problems. Let's look at the...</v>

00:55:42.261 --> 00:55:47.341
<v Val Levitan>Sorry, Nebraska, I only see Nebraska in the production stage. Am I correct?</v>

00:55:47.701 --> 00:55:48.181
<v Michael Gottlieb>Yes.</v>

00:55:49.701 --> 00:55:52.021
<v Val Levitan>All other stages are closed from Nebraska.</v>

00:55:52.901 --> 00:56:02.661
<v Michael Gottlieb>Yes, yeah, we're going through the game right now. The guys are, you know, sending us new build every couple of days. So we're going through it right now and making final adjustments.</v>

00:56:04.101 --> 00:56:07.221
<v Michael Gottlieb>And enhancements. Wild cold has been enhanced.</v>

00:56:17.301 --> 00:56:20.181
<v Michael Gottlieb>We're working on the Jim Brilliante pay table.</v>

00:56:23.701 --> 00:56:32.981
<v Lena Zhukova>Yeah, midnight night, money assets also will be updated, yeah, not major already designed, but some.</v>

00:56:27.141 --> 00:56:27.381
<v Michael Gottlieb>Yeah.</v>

00:56:34.421 --> 00:56:38.181
<v Val Levitan>So there are 15 games for Nebraska.</v>

00:56:34.581 --> 00:56:36.581
<v Lena Zhukova>Play it.</v>

00:56:40.501 --> 00:56:43.781
<v Val Levitan>And they will be on Rage Studio, right?</v>

00:56:44.341 --> 00:56:44.901
<v Lena Zhukova>Yes.</v>

00:56:46.181 --> 00:56:54.981
<v Val Levitan>And so, the 15 games were taken previous six, and we are in nine more.</v>

00:56:57.061 --> 00:57:00.581
<v Val Levitan>I'm kind of aligning with you. It's not a, it's not a...</v>

00:57:02.181 --> 00:57:04.581
<v Val Levitan>It's not a trick question, I'm just aligning myself with it.</v>

00:57:04.741 --> 00:57:04.981
<v Michael Gottlieb>Right.</v>

00:57:06.981 --> 00:57:07.941
<v Val Levitan>And.</v>

00:57:09.301 --> 00:57:15.541
<v Val Levitan>Can you tell me the philosophy behind redesigning the six games that...</v>

00:57:16.861 --> 00:57:22.981
<v Val Levitan>While already in the market, what are the redesigning? Is it math or visuals or?</v>

00:57:21.941 --> 00:57:33.221
<v Michael Gottlieb>Well, I wouldn't use the word redesigning. We're just doing some graphical enhancements to make them more applicable, make them more current, I guess.</v>

00:57:32.741 --> 00:57:42.661
<v Lena Zhukova>But also also the change in bonus and progressive from this golden husk. We are moving to March 3. Yeah, it's a big change.</v>

00:57:37.221 --> 00:57:37.861
<v Efim Podvoiski>All right.</v>

00:57:38.981 --> 00:57:41.381
<v Michael Gottlieb>To match three, that's the big change.</v>

00:57:44.341 --> 00:57:47.701
<v Michael Gottlieb>And we're introducing both Jackpot Rush and Fiery Ice.</v>

00:57:51.581 --> 00:57:55.141
<v Val Levitan>OK, and it will be a liquid glass, right?</v>

00:57:55.461 --> 00:57:56.021
<v Michael Gottlieb>Oh, yes.</v>

00:57:55.581 --> 00:57:56.181
<v Lena Zhukova>It's.</v>

00:57:57.621 --> 00:58:02.021
<v Val Levitan>And the 15 games will also be 10 in front.</v>

00:58:03.301 --> 00:58:03.861
<v Val Levitan>Right.</v>

00:58:04.981 --> 00:58:11.061
<v Val Levitan>And 5 that we could change to change the settings, but we're loading all 15.</v>

00:58:09.541 --> 00:58:09.941
<v Lena Zhukova>No.</v>

00:58:11.421 --> 00:58:12.421
<v Michael Gottlieb>It's 11, right?</v>

00:58:16.021 --> 00:58:17.141
<v Michael Gottlieb>It's 11, it's not.</v>

00:58:16.301 --> 00:58:18.821
<v Val Levitan>For Nebraska, for Nebraska Accounts.</v>

00:58:17.541 --> 00:58:19.381
<v Lena Zhukova>Yeah, it's actually not 15.</v>

00:58:19.461 --> 00:58:20.421
<v Michael Gottlieb>Yeah, it's 11.</v>

00:58:30.821 --> 00:58:34.821
<v Michael Gottlieb>So, 7 and Wildfire Wildfire Ranch is brand new.</v>

00:58:32.261 --> 00:58:37.861
<v Val Levitan>They counting, I'm counting 15 on your list.</v>

00:58:40.381 --> 00:58:41.781
<v Michael Gottlieb>Which list are you looking at?</v>

00:58:43.301 --> 00:58:46.021
<v Val Levitan>in JIRA under IP 1143.</v>

00:58:46.981 --> 00:58:53.541
<v Efim Podvoiski>There is a liquid glass style home screen. My still bonus check.</v>

00:58:49.541 --> 00:58:55.221
<v Lena Zhukova>Yeah, so there are some different different ideas, so this is this is so.</v>

00:58:54.461 --> 00:58:56.661
<v Val Levitan>Oh yeah, yeah, these are not games, right?</v>

00:58:56.421 --> 00:59:02.901
<v Lena Zhukova>Yeah, yeah, so this is home screen for Nebraska and yeah, all games here.</v>

00:59:05.221 --> 00:59:15.541
<v Val Levitan>Or there is an interesting comment that I observed on the graphic user interface. People are trying to press.</v>

00:59:16.741 --> 00:59:19.301
<v Val Levitan>The category, they think that it's a button.</v>

00:59:22.181 --> 00:59:24.581
<v Val Levitan>So let's say fiery ice link.</v>

00:59:26.101 --> 00:59:27.781
<v Val Levitan>To them looks like a button.</v>

00:59:31.941 --> 00:59:36.821
<v Val Levitan>And, and they just repeatedly trying to press it.</v>

00:59:38.581 --> 00:59:40.581
<v Val Levitan>They get frustrated. They get.</v>

00:59:38.901 --> 00:59:41.141
<v Michael Gottlieb>That's really strange.</v>

00:59:42.421 --> 00:59:50.901
<v Michael Gottlieb>Sorry, go ahead. They get frustrated because they keep touching it. Wow, we're not dealing with high IQ people. That's staggering.</v>

00:59:43.781 --> 00:59:44.181
<v Val Levitan>Yeah.</v>

00:59:47.061 --> 00:59:47.541
<v Val Levitan>Yeah.</v>

00:59:52.741 --> 00:59:54.501
<v Val Levitan>Well, it's nothing new to you, right?</v>

00:59:56.181 --> 01:00:01.941
<v Michael Gottlieb>I guess, I just, you know, our competitors, everything is game icon driven. Everything.</v>

01:00:02.981 --> 01:00:07.461
<v Val Levitan>Oh, no, no, no, oh, oh, no, they appreciate the game icon.</v>

01:00:08.461 --> 01:00:10.101
<v Val Levitan>But they're treating.</v>

01:00:11.301 --> 01:00:13.861
<v Val Levitan>The larger Bob as a...</v>

01:00:17.301 --> 01:00:20.421
<v Val Levitan>I guess a category selection button.</v>

01:00:20.901 --> 01:00:21.461
<v Michael Gottlieb>Right.</v>

01:00:24.261 --> 01:00:25.941
<v Michael Gottlieb>That's really strange.</v>

01:00:31.541 --> 01:00:34.341
<v Val Levitan>I observed it, I observed it a number of times.</v>

01:00:34.741 --> 01:00:35.141
<v Michael Gottlieb>Ha.</v>

01:00:54.261 --> 01:01:07.781
<v Michael Gottlieb>I'll give that some thought, but in all honesty, off the top of my head, I'm not exactly sure other than putting words in red that say not a button. I'm being facetious on there. I don't.</v>

01:00:55.941 --> 01:00:56.501
<v Lena Zhukova>You can.</v>

01:00:59.061 --> 01:00:59.381
<v Lena Zhukova>And.</v>

01:01:07.061 --> 01:01:07.421
<v Val Levitan>Yeah.</v>

01:01:11.301 --> 01:01:13.701
<v Lena Zhukova>Let's think about it.</v>

01:01:11.701 --> 01:01:15.381
<v Val Levitan>Alright, then, anyways, I'm gonna, I'm gonna park it with you.</v>

01:01:15.701 --> 01:01:16.181
<v Lena Zhukova>Ohh.</v>

01:01:16.101 --> 01:01:36.581
<v Michael Gottlieb>Well, I can tell you the solution for Jackpot Rush and Fiery Ice Link is you extend the collision box of Calle Ocho vertically, Rodeo spins vertically, Sparkle Sevens and Sapphire Star vertically. So if you touch basically the left part of Jackpot Rush, it will pick Sparkle Sevens. And if you pick the right half of the Jackpot Rush bar, it'll pick</v>

01:01:36.661 --> 01:01:54.901
<v Michael Gottlieb>Sapphire Star. So at least you're picking something. You know, if that's the thing. Lines and ways, I don't, we're not going to have the player touch lines and ways and then have a separate screen presented to them with seven selectable games. That ain't happening. So I'll think about it.</v>

01:01:55.621 --> 01:01:56.581
<v Efim Podvoiski>How can we?</v>

01:01:55.781 --> 01:01:57.861
<v Michael Gottlieb>That's really strange behavior.</v>

01:01:58.901 --> 01:02:00.981
<v Efim Podvoiski>Show it like, just not like a...</v>

01:02:00.821 --> 01:02:05.461
<v Val Levitan>Maybe, maybe we don't have to do anything about it. Maybe, maybe it will go away.</v>

01:02:03.941 --> 01:02:04.981
<v Efim Podvoiski>Mix, mix.</v>

01:02:06.141 --> 01:02:16.901
<v Efim Podvoiski>So, just like, so it would be like a flat text text on the phone on on the on the background, rather than looking something like it looks like a widget.</v>

01:02:14.661 --> 01:02:20.341
<v Lena Zhukova>But the screen will screen will look unorganized and unstructured.</v>

01:02:19.701 --> 01:02:20.981
<v Michael Gottlieb>Right, right.</v>

01:02:19.861 --> 01:02:22.661
<v Efim Podvoiski>Yeah, I see, I see, I see, I see.</v>

01:02:25.301 --> 01:02:33.941
<v Lena Zhukova>We can make it much more transparent than buttons. I don't know, that's the only solution is coming in my head right now. I mean this rectangle.</v>

01:02:25.461 --> 01:02:25.861
<v Michael Gottlieb>OK.</v>

01:02:31.621 --> 01:02:32.021
<v Efim Podvoiski>Ohh.</v>

01:02:35.701 --> 01:02:39.101
<v Lena Zhukova>But they will, I, I feel like they will still like touch it.</v>

01:02:39.981 --> 01:02:48.621
<v Efim Podvoiski>Yeah, but okay. If people are doing this, we, something, I think we have to at least think about it.</v>

01:02:48.941 --> 01:03:03.021
<v Michael Gottlieb>Yeah, I didn't say we shouldn't think about it. I'm just not quite sure. I mean, you know, aesthetically, it would not be nearly as attractive, but if you completely remove the border altogether, that would work. I don't think it would look good.</v>

01:02:50.701 --> 01:02:51.181
<v Efim Podvoiski>Yeah.</v>

01:03:04.701 --> 01:03:11.021
<v Michael Gottlieb>But it wouldn't look like a button anymore, it would simply look like text. But see, even then, there's still no guarantee they won't touch the text.</v>

01:03:08.301 --> 01:03:08.861
<v Efim Podvoiski>Mikhail.</v>

01:03:12.461 --> 01:03:14.861
<v Efim Podvoiski>If you make some fancy border, like...</v>

01:03:14.141 --> 01:03:16.461
<v Val Levitan>I, I don't know how big of an issue it is.</v>

01:03:16.861 --> 01:03:17.741
<v Michael Gottlieb>Okay, fair enough.</v>

01:03:18.301 --> 01:03:20.461
<v Val Levitan>I, I cannot, I cannot measure it.</v>

01:03:21.341 --> 01:03:34.061
<v Michael Gottlieb>Well, I guess the question is, is from a player friction standpoint, is the person, you know, hitting the thing and then, you know, after it not doing anything, a touch or two, they touch a game icon.</v>

01:03:34.901 --> 01:03:45.421
<v Michael Gottlieb>because you're talking about 1/2 an inch or 1/4 of an inch away from the label above the icon to just simply bring your finger down and touch the icon.</v>

01:03:47.821 --> 01:03:53.021
<v Michael Gottlieb>And select, and and and you know, and selecting a game in the process, so I would hope.</v>

01:03:54.101 --> 01:03:54.461
<v Michael Gottlieb>That.</v>

01:03:55.901 --> 01:04:16.741
<v Michael Gottlieb>At least for me, if I get frustrated with an ATM and it's not recognizing what I'm doing, I do move my finger around the withdrawal box in order to get the thing to trigger, or in a gas pump, a gas station, right? You have to touch something, a touchscreen on a gas station. Same deal. You just kind of poke around until it does something.</v>

01:04:24.501 --> 01:04:26.421
<v Michael Gottlieb>Wow, okay, well, interesting comment.</v>

01:04:54.781 --> 01:04:57.501
<v Val Levitan>Okay, so back to...</v>

01:05:00.141 --> 01:05:02.621
<v Val Levitan>Version 2 of NAD.</v>

01:05:08.301 --> 01:05:12.941
<v Val Levitan>Do I understand it correctly that it will be raining by the end of December, right?</v>

01:05:14.621 --> 01:05:18.781
<v Lena Zhukova>Assets, it doesn't mean that they're going to be like that.</v>

01:05:17.901 --> 01:05:19.981
<v Val Levitan>But not the integration, right?</v>

01:05:21.421 --> 01:05:42.181
<v Lena Zhukova>No, it will be integrated. Everything will be integrated, but not tested, not necessarily. It might need some adjustments, so it everything will be in the build, but maybe we will, especially this new game, maybe we will need.</v>

01:05:21.821 --> 01:05:23.101
<v Val Levitan>That's what, that's what you.</v>

01:05:31.181 --> 01:05:31.661
<v Val Levitan>Okay.</v>

01:05:42.341 --> 01:05:43.821
<v Lena Zhukova>To do some adjustments.</v>

01:05:46.781 --> 01:05:51.741
<v Efim Podvoiski>Some, some of the games that are down low on the schedule, right?</v>

01:05:52.461 --> 01:05:54.061
<v Lena Zhukova>Mm-hmm, yeah.</v>

01:05:53.341 --> 01:05:55.581
<v Efim Podvoiski>Because some games are going already.</v>

01:05:56.061 --> 01:06:04.621
<v Lena Zhukova>Yes, yes, some games are done already, like, yeah, like some five stars, line switches, so if somebody wants to test them, they can start to test.</v>

01:06:12.701 --> 01:06:23.261
<v Michael Gottlieb>And these are vertical games that we're taking to dual screen for the first time, Val, so we need to make sure that all looks good. So far with the Jackpot Rush, it looks fine, but we still have to check with Fiery Ice and make sure all those look good.</v>

01:06:22.461 --> 01:06:42.141
<v Lena Zhukova>Yeah, fine, yes, yes, it's a it's a not an easy task to move bonus diamond bonus to dual screens. I'm working on it right now, so maybe next week we will have like first insertion in the build. I think we will need to adjust maybe something.</v>

01:07:11.021 --> 01:07:11.581
<v Val Levitan>No.</v>

01:07:23.021 --> 01:07:24.861
<v Val Levitan>So, the reason...</v>

01:07:26.061 --> 01:07:29.421
<v Val Levitan>Lena, I'm asking a question. The reason is, the reason we...</v>

01:07:34.381 --> 01:07:37.101
<v Val Levitan>I'm going to ask the question again. So the reason we have...</v>

01:07:37.981 --> 01:07:41.901
<v Val Levitan>And they de-scheduled as a priority for production.</v>

01:07:43.981 --> 01:07:50.941
<v Val Levitan>Basically 2 reasons. First of all, we started to work on it prior to Class A.</v>

01:07:52.941 --> 01:07:58.941
<v Val Levitan>And second reason is that Class A is going to be done in Novo.</v>

01:08:00.301 --> 01:08:03.021
<v Val Levitan>And that's why you do them in schedule production, right?</v>

01:08:09.101 --> 01:08:18.301
<v Val Levitan>And Efim, you said that, sorry, not Efim, Michael, you said that you and Efim are practically zeroed in on the math, right?</v>

01:08:20.541 --> 01:08:36.621
<v Michael Gottlieb>The concept, but all of the heavy lifting, Efim still has to do all the work of creating the math. Conceptually, we've got a couple, we've got one game done, we've got five games to go. Once we get all the games done, then Efim can actually do the math.</v>

01:08:37.541 --> 01:08:37.981
<v Efim Podvoiski>Yes.</v>

01:08:39.341 --> 01:08:49.501
<v Val Levitan>Okay, so question, if you, for you to do the math for class A, can you give me roughly how much time it will take for you?</v>

01:08:50.461 --> 01:08:53.341
<v Efim Podvoiski>I hope to finish by New Year.</v>

01:08:55.181 --> 01:08:57.661
<v Efim Podvoiski>I, I think I, I think it should.</v>

01:08:55.261 --> 01:08:59.821
<v Val Levitan>Oh, it will take, it will take, it will take five, six weeks.</v>

01:09:00.621 --> 01:09:06.141
<v Efim Podvoiski>Yeah, to do production mass, yes, to finish everything, yes, maybe.</v>

01:09:07.421 --> 01:09:26.141
<v Efim Podvoiski>At this moment, I cannot promise anything better. Maybe if we pass design stage in two, two, three weeks, and I will see that I can automate the production masks. But anyway, it's not a big difference. Not less than four weeks, I am sure.</v>

01:09:36.461 --> 01:09:37.101
<v Val Levitan>Great.</v>

01:09:46.381 --> 01:09:57.421
<v Val Levitan>Question to Lena and Michael. So for NAD second version, Lena, can you pull up the screen again so I could see how it will look?</v>

01:10:07.101 --> 01:10:09.501
<v Val Levitan>So it's going to be a dual screen, right?</v>

01:10:10.221 --> 01:10:10.781
<v Michael Gottlieb>Yes.</v>

01:10:14.701 --> 01:10:17.261
<v Val Levitan>Dual screen in Rage Studio.</v>

01:10:31.341 --> 01:10:32.621
<v Michael Gottlieb>With 5 new games.</v>

01:10:46.621 --> 01:10:46.661
<v Val Levitan>I.</v>

01:10:47.981 --> 01:10:48.621
<v Val Levitan>Okay.</v>

01:10:50.221 --> 01:10:57.421
<v Val Levitan>So then I have another question probably and that's it. For class 3 in Colombia.</v>

01:10:51.741 --> 01:10:51.901
<v Lena Zhukova>Yeah.</v>

01:10:59.261 --> 01:11:01.261
<v Val Levitan>Did you get all the answers, Michael?</v>

01:11:02.621 --> 01:11:20.981
<v Michael Gottlieb>I'm still waiting for some more feedback from Martha, but I've got enough to know what I think we should do. And I have a preliminary list of games. The greatest challenge is going to be the perceived persistence.</v>

01:11:21.261 --> 01:11:39.981
<v Michael Gottlieb>games. And I can tell you right now that you're going to have to hold your breath or hold your nose or whatever you want to say because there's a couple of elements of the new popular perceived persistence games that I don't think you're really going to like. One of them is that</v>

01:11:40.021 --> 01:12:01.821
<v Michael Gottlieb>the second screen or the above the real bundle, basically it's objects. It's firecrackers. Just think 3 strands of firecrackers or three gold pots with accumulations of gems, 3 treasure chests with accumulations of gems. So you don't have that big dominant striking image of a person or an animal.</v>

01:12:03.021 --> 01:12:25.181
<v Michael Gottlieb>So it's a very, very different presentation. And secondly, people are the, our competitors, our most successful competitors. I don't really pay attention to the ones that aren't succeeding in the marketplace. Their art style is, I would say, very cartoony and not photorealistic. There's an extremely cartoony look that is the popular look.</v>

01:12:25.221 --> 01:12:29.821
<v Michael Gottlieb>Now, and that is the direction that we that we need to go.</v>

01:12:30.541 --> 01:12:36.301
<v Lena Zhukova>Yeah, I would say it's a minimalistic cartoon style, not, not exact style, like.</v>

01:12:33.901 --> 01:12:35.661
<v Michael Gottlieb>Yeah, minimalistic cartoons though.</v>

01:12:34.461 --> 01:12:37.661
<v Val Levitan>So, why, why my Michael, why would I care?</v>

01:12:38.781 --> 01:12:40.141
<v Michael Gottlieb>Uh, because...</v>

01:12:40.381 --> 01:12:42.221
<v Val Levitan>You're not designing games for me.</v>

01:12:42.541 --> 01:12:48.541
<v Michael Gottlieb>Okay, well, I'm just telling you right now, this is it's not here. Let me share just to give you a visual.</v>

01:12:47.581 --> 01:12:53.101
<v Val Levitan>I have no, I have no influence about that. I don't even pretend to influence.</v>

01:12:52.701 --> 01:13:02.701
<v Michael Gottlieb>Okay, here's a visual of, you know, the cat with the big eyes and then just pots up here.</v>

01:13:03.501 --> 01:13:06.541
<v Michael Gottlieb>You know, the art style is very cartoony.</v>

01:13:09.501 --> 01:13:15.501
<v Michael Gottlieb>That's all. I just wanted to make you aware. I mean, again, I think, you know, no surprises is good.</v>

01:13:11.021 --> 01:13:11.501
<v Val Levitan>Okay.</v>

01:13:14.061 --> 01:13:14.541
<v Val Levitan>Efim.</v>

01:13:19.341 --> 01:13:22.541
<v Michael Gottlieb>And it's really, really complicated.</v>

01:13:23.781 --> 01:13:41.821
<v Michael Gottlieb>I thought Efim, I thought Efim was going to plots on me when he and I were talking about what it's going to take to do this. It's unfortunately, these games are very, very complicated, but we will, you know, start with one and go from there.</v>

01:13:44.701 --> 01:13:46.861
<v Michael Gottlieb>This is the, I'll give you a sense.</v>

01:13:49.901 --> 01:13:53.581
<v Val Levitan>So you're talking about game design.</v>

01:13:55.021 --> 01:13:58.221
<v Val Levitan>Sorry, concept stage and game design stage, right?</v>

01:14:01.101 --> 01:14:05.901
<v Michael Gottlieb>Basically all the phases are going to take longer because of the degree.</v>

01:14:04.941 --> 01:14:13.421
<v Val Levitan>No, but the no, but the complication today, I don't see complication for Lena for production, but the complication.</v>

01:14:11.381 --> 01:14:32.021
<v Michael Gottlieb>Oh no, I think, no, there's a huge amount of complication. And here, let me just show you, let me give you a sense, I can show you. Okay, so perceived persistence, these firecrackers, if you count how many firecrackers there are, right, each one of them.</v>

01:14:14.861 --> 01:14:15.341
<v Val Levitan>No.</v>

01:14:32.101 --> 01:14:45.261
<v Michael Gottlieb>needs to be animated and lit, and you have all of these, what are called false hits. That's a false hit, that's not a trigger, right? You have zillions of these false hits that take place while you're playing the game.</v>

01:14:41.101 --> 01:14:41.661
<v Val Levitan>Which?</v>

01:14:49.661 --> 01:15:00.701
<v Michael Gottlieb>You have to do these animations, run the firecrackers up to the strands, and then the strands all have multiple states, like a lot of states of visual behavior.</v>

01:15:02.301 --> 01:15:11.101
<v Michael Gottlieb>So I would say one of these games is anywhere from, it's the equivalent of 6 to 8, doing 6 to 8 regular games in terms of complexity.</v>

01:15:13.821 --> 01:15:17.101
<v Michael Gottlieb>They're extremely complex.</v>

01:15:16.741 --> 01:15:19.261
<v Val Levitan>What's the what's the name of this game? Sorry.</v>

01:15:19.981 --> 01:15:25.181
<v Michael Gottlieb>Oh, this is Baozu, Baozu Festival, one of the popular Aristocrat games.</v>

01:15:24.061 --> 01:15:27.501
<v Val Levitan>Hey, can you send? Can you send it to me in chat? I don't want to misspell it.</v>

01:15:30.661 --> 01:15:32.821
<v Michael Gottlieb>Yeah, I'll have to find the...</v>

01:15:33.101 --> 01:15:34.381
<v Val Levitan>And this is by whom?</v>

01:15:35.261 --> 01:15:36.501
<v Val Levitan>Aristocrat, I think.</v>

01:15:36.541 --> 01:15:37.661
<v Michael Gottlieb>Yeah, it's aristocrat.</v>

01:15:39.661 --> 01:15:41.901
<v Val Levitan>And what other games that you?</v>

01:15:43.341 --> 01:15:43.901
<v Val Levitan>Um...</v>

01:15:44.301 --> 01:15:45.461
<v Michael Gottlieb>Well, this is so the...</v>

01:15:45.021 --> 01:15:45.981
<v Val Levitan>Identified.</v>

01:15:47.061 --> 01:15:50.141
<v Michael Gottlieb>Hold on just a second here. Yes, submit.</v>

01:15:51.661 --> 01:15:59.101
<v Michael Gottlieb>Okay, hold on. This will give you a sense. This is one of the things we're going to be doing.</v>

01:16:01.981 --> 01:16:02.141
<v Val Levitan>Yeah.</v>

01:16:02.381 --> 01:16:20.381
<v Michael Gottlieb>That's the game. Baozu Zafu. So basically it's three firecracker strands. Excuse me, strands. What I am working on is a Brazilian carnival game. Excuse me, Colombian, Colombian, Colombian carnival game.</v>

01:16:16.781 --> 01:16:17.261
<v Lena Zhukova>A lot.</v>

01:16:21.661 --> 01:16:39.741
<v Michael Gottlieb>using the Colombian colors for the carnival. You've seen, we did Crescent City Carnival, right? You've seen that. Think, well, but this is going to be strands of firecrackers. This is going to be strands of firecrackers just in a different, in a different color.</v>

01:16:30.301 --> 01:16:31.181
<v Val Levitan>Gorgeous Mery.</v>

01:16:40.381 --> 01:16:40.701
<v Michael Gottlieb>Um...</v>

01:16:41.861 --> 01:16:47.901
<v Michael Gottlieb>Excuse me, so, and I can't even pronounce the bar barquanilla.</v>

01:16:48.861 --> 01:16:53.181
<v Michael Gottlieb>I don't speak Spanish. Anyway, this is the this is that's going to be the name of it.</v>

01:16:50.301 --> 01:16:51.181
<v Efim Podvoiski>Genadi.</v>

01:16:55.021 --> 01:17:18.741
<v Michael Gottlieb>And they're going to be 3 firecracker strands above the real bundle, red, yellow, and green, which are the colors of the carnival. And then it's going to be these kind of cartoony graphics with elements of the carnival. And the trick is to do something that will be authentic and attractive and be embraced by the Colombians, but at the same time could conceivably</v>

01:17:18.821 --> 01:17:37.501
<v Michael Gottlieb>work in Georgia as well, because this is going to be a monster. This is going to be a big one. So yeah, that's the idea behind that. Now, here is the challenge. You are Nostradamus, Val, because you predicted a couple years ago that everything was going to go vertical.</v>

01:17:37.901 --> 01:17:52.221
<v Michael Gottlieb>Everything has gone vertical, and the reason it's gone vertical is what I just showed you. You've got the real bundle, and then you've got shooting stuff shooting up to things above the real bundle. The challenge in Columbia is that you want dual screen, and dual screen does not...</v>

01:17:51.501 --> 01:17:59.181
<v Val Levitan>No, no, no, no, no, I don't want dual screen. I don't care what screen. I don't care. I don't care which screen.</v>

01:17:55.581 --> 01:17:58.381
<v Michael Gottlieb>Okay, then we want vertical. Okay.</v>

01:17:59.581 --> 01:18:05.021
<v Michael Gottlieb>Then it's vertical from here on out. I thought that you had D27s that you wanted to put new software in.</v>

01:18:04.541 --> 01:18:10.861
<v Val Levitan>I, I mean, I have D27s, but it doesn't matter. It's very easy to convert our hardware.</v>

01:18:12.781 --> 01:18:18.301
<v Lena Zhukova>And then we can easily use the same assets for Georgia before and calendar.</v>

01:18:18.701 --> 01:18:20.701
<v Val Levitan>You could absolutely go over the call.</v>

01:18:21.181 --> 01:18:25.661
<v Michael Gottlieb>Right, okay, it will be vertical then. It will absolutely be vertical.</v>

01:18:25.741 --> 01:18:31.261
<v Lena Zhukova>And it's much better for this type of games to be on vertical screen.</v>

01:18:33.821 --> 01:18:39.581
<v Val Levitan>So, can you, uh, you said you identified 3 games. What other two games did you identify?</v>

01:18:39.821 --> 01:18:49.981
<v Michael Gottlieb>Well, the second one is that Midnight Express that I saw while I was in Georgia. So I already have a design, preliminary design for that called Fly Me to the Moon. And</v>

01:18:49.741 --> 01:18:51.981
<v Val Levitan>Is it also perceived persistence?</v>

01:18:52.061 --> 01:18:52.541
<v Michael Gottlieb>Yes.</v>

01:18:54.541 --> 01:18:55.101
<v Val Levitan>Okarak.</v>

01:18:55.421 --> 01:19:08.461
<v Michael Gottlieb>Yeah, that one's perceived persistence. And then the third one, now these are big, so I'm not saying we're going to be able to do all three of these in the next go around. We might, we'll see how we do, but I have a vision for where we're going.</v>

01:19:11.101 --> 01:19:32.141
<v Michael Gottlieb>Three perceived persistence games. One is called Fly Me to the Moon based upon the Midnight Train game at Aristocrat. The second one is this Colombian carnival game. Three strands of firecrackers above the real bundle, cartoony graphics, heavily honoring and embracing this wonderful carnival that they have in Colombia. It's apparently the most important thing in the world.</v>

01:19:23.421 --> 01:19:24.061
<v Lena Zhukova>Something.</v>

01:19:32.421 --> 01:19:41.901
<v Michael Gottlieb>And the third one is going to be called Treasure Island, and it's going to be a gem game because everybody is doing this.</v>

01:19:43.581 --> 01:19:44.461
<v Michael Gottlieb>It's just...</v>

01:19:45.821 --> 01:20:08.061
<v Michael Gottlieb>gems, gems, and more gems, infinite amounts of gems. So we'll do a Treasure Island game with three treasure chests. And I zoomed in close so Lena can see the effects, the special effects that they're doing. But you can see they're running lots of layers. There's a lot going on here in order to make this stuff look the way that it does. And then you've got this</v>

01:20:08.181 --> 01:20:11.821
<v Michael Gottlieb>the gems hit and increase.</v>

01:20:17.341 --> 01:20:27.901
<v Michael Gottlieb>So I just triggered the jackpot feature there. This is very similar to our match 3, but you can see, I mean, they're doing like Pixar quality graphics with the characters.</v>

01:20:29.181 --> 01:20:30.541
<v Michael Gottlieb>So, I want to focus.</v>

01:20:29.461 --> 01:20:32.781
<v Val Levitan>Is this your? Is this your middle finger on the screen?</v>

01:20:33.181 --> 01:20:33.661
<v Michael Gottlieb>Yes.</v>

01:20:39.981 --> 01:20:58.861
<v Michael Gottlieb>Yeah, I went out to the casino and spent an ungodly amount of money playing all the new stuff to just get my finger on the pulse of what's going on out there. This is Spooky Link, which is basically an evolution of Mo Mummy. It's a bit the same gameplay mechanic with different art.</v>

01:21:00.141 --> 01:21:02.221
<v Michael Gottlieb>You can see the very, very cartoony.</v>

01:21:03.981 --> 01:21:22.381
<v Michael Gottlieb>looking characters. And then so here, page one, two, three, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14,</v>

01:21:22.541 --> 01:21:36.221
<v Michael Gottlieb>15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27,</v>

01:21:24.461 --> 01:21:24.621
<v Efim Podvoiski>Yeah.</v>

01:21:35.341 --> 01:21:43.021
<v Lena Zhukova>No, the the help is crazy. I think nobody would, yeah, nobody would understand the reading help how the game works.</v>

01:21:37.661 --> 01:21:40.141
<v Efim Podvoiski>And now we are going to normal.</v>

01:21:41.221 --> 01:21:53.661
<v Michael Gottlieb>Yeah, 28, 29, 30. So 30 pages, 30 pages of help screens. That gives you a sense of how ****** complicated these games are. And then like I was saying about the art.</v>

01:21:52.541 --> 01:21:57.101
<v Val Levitan>Can you please, can you please do me a favor, put everything in the chat here?</v>

01:22:00.701 --> 01:22:15.101
<v Michael Gottlieb>Well, I can do, would you want me to just share? I have these massive zip files I can add you that I shared with Lena and Efim. I'll just share those with you so you can have, you can see everything. But you can, yeah, you can see, just look at the art style.</v>

01:22:10.781 --> 01:22:11.741
<v Val Levitan>Fantastic.</v>

01:22:16.181 --> 01:22:17.021
<v Michael Gottlieb>You know this.</v>

01:22:17.901 --> 01:22:24.861
<v Michael Gottlieb>simplified, cartoony, it is not photorealistic. So it's different. And this is what players are...</v>

01:22:23.261 --> 01:22:30.661
<v Lena Zhukova>Yeah, definitely. Maybe we can, we can do it, yeah, because we can do any style, no problem, but just need to understand.</v>

01:22:26.221 --> 01:22:27.661
<v Michael Gottlieb>Yeah, yeah, yeah.</v>

01:22:29.901 --> 01:22:48.461
<v Michael Gottlieb>And the symbol design, if you look at the symbol design, it's actually pretty simple. You know, very minimalistic. Yeah, that's the word. You know, there's the wolfy guy. And the base game is flat as hell. It's completely worthless. I mean, look at this.</v>

01:22:34.621 --> 01:22:36.301
<v Lena Zhukova>Yeah, very minimalistic.</v>

01:22:48.781 --> 01:23:09.581
<v Michael Gottlieb>This is ridiculous. These are your top five symbols. They all pay the same. There are no base game pays. Everything is in these crazy bonuses. Everything is in these crazy bonuses. But yeah, I mean, a typical slot, the regular slot, you have help screens of, I don't know, three or four pages, and now we've got 30.</v>

01:23:09.861 --> 01:23:28.901
<v Michael Gottlieb>And the problem, Val, is all of the combinations and permutations. You can trigger one, two, and three. You can trigger all three. You can trigger one and two. You can trigger one and three. You can trigger two and three. You can, I mean, it's mind-bending. But we have smart people, and I am undaunted.</v>

01:23:29.021 --> 01:23:50.621
<v Michael Gottlieb>and we will do it and we can do it. But I'm not going to tell you that it's not going to be easy. It's going to be extraordinarily challenging. So we'll pick our, pick what makes the most sense where we can, which is like I said, we'll do firecrackers because firecrackers make sense. Here's the, let's see, this is Aristocrats chili game.</v>

01:23:55.821 --> 01:23:58.941
<v Michael Gottlieb>You know, with these silly looking guys with the big eyes.</v>

01:24:03.741 --> 01:24:25.821
<v Michael Gottlieb>But interestingly, and this is what Efim was saying to me yesterday, it's all just hold and re-spin. You know, it's a variance of something that there isn't a lot of kind of innovation going on. It's more complexity than innovation, if that makes any sense. And Efim and I were staring at this yesterday, trying to ascertain, well, what is it that the players love? And my theory</v>

01:24:26.141 --> 01:24:40.061
<v Michael Gottlieb>is that it's just, it's the sense of accumulation of trying to fill the screen with gold coins and it's money. And even though the amount that you would win in this bonus is maybe similar to what you would win in something like free spins,</v>

01:24:42.781 --> 01:24:45.261
<v Michael Gottlieb>They, they, you want to fill the grid.</v>

01:24:46.381 --> 01:25:05.501
<v Michael Gottlieb>You feel, you know, look at this. I mean, the idea of making all of the dark, real Windows gold is very attractive, even though when you add it all up, the ultimate pay isn't anything to get excited about. So a hell of a lot of entertainment value, not a crazy amount of pay.</v>

01:25:06.701 --> 01:25:07.981
<v Michael Gottlieb>So, here we go. I think we're...</v>

01:25:24.421 --> 01:25:28.621
<v Michael Gottlieb>And of course you get to the end and you zero out. You don't reset to three anymore.</v>

01:25:32.621 --> 01:25:35.261
<v Michael Gottlieb>So, a $19.50 win.</v>

01:25:36.381 --> 01:25:37.421
<v Michael Gottlieb>Or no, it's more than that.</v>

01:25:39.901 --> 01:25:41.981
<v Michael Gottlieb>They had to write, okay, $34 win.</v>

01:25:45.421 --> 01:26:09.941
<v Michael Gottlieb>And that's the instant feature buy a bet, because I didn't want to sit there for days to trigger the bonus. I just bet 100 bucks and saw how, if you bet $100, you can buy the bonus. So that's what I was doing. So anyway, yeah, that's what's going on in the market. This Holden Respin stuff. Like I said, I've got a very strong vision for what I think the first three should be. One of them is very specifically directed toward the Georgia market and Flying Me to the Moon. One of them is very</v>

01:26:10.381 --> 01:26:29.541
<v Michael Gottlieb>specifically directed to the Columbia market and the Carnival game. And then Treasure Island is a universal, you know, treasure chests filled with gems. I chose Treasure Island because nobody else is really doing it. And I think that you're far enough south in the United States and South America that, you know, Pirates of the Caribbean, Pirates, that</v>

01:26:29.661 --> 01:26:41.581
<v Michael Gottlieb>type of vibe will sell. That'll go to people will, people will like that. We'll have a real pretty female pirate in the game, but she's going to look cartoony. She's not going to look like real.</v>

01:26:38.541 --> 01:26:38.701
<v Val Levitan>It.</v>

01:26:46.621 --> 01:26:48.621
<v Val Levitan>Okay, guys, we have a plan.</v>

01:26:49.261 --> 01:26:49.661
<v Michael Gottlieb>Oh yeah.</v>

01:26:51.181 --> 01:26:55.421
<v Val Levitan>So this is going into a game concept now, right?</v>

01:26:56.621 --> 01:27:00.781
<v Michael Gottlieb>Yes, yeah, yeah, I...</v>

01:27:00.781 --> 01:27:04.181
<v Val Levitan>When, when are you going to uh, put it at the game console?</v>

01:27:04.861 --> 01:27:25.541
<v Michael Gottlieb>I'll probably get started scheduling it next week. We need to get done with Nebraska and the class A math. That's what I'm, like I said, that's what I've been focused on. I have been working on this, but I'll get it scheduled. I'll get it scheduled next week. I know in my mind what it's going to be. I just, I just need to, you know, flesh it all out.</v>

01:27:25.661 --> 01:27:31.021
<v Michael Gottlieb>And I, at whenever Lena has bandwidth, we need to start the process of...</v>

01:27:32.781 --> 01:27:34.061
<v Michael Gottlieb>Going back and forth.</v>

01:27:34.301 --> 01:27:50.141
<v Lena Zhukova>I think once you finish concept stage, I will finish all designs for South Dakota and Laura, and we will be starting doing like design like images for all these new games.</v>

01:27:43.261 --> 01:27:43.741
<v Michael Gottlieb>Yeah.</v>

01:27:50.581 --> 01:27:50.861
<v Michael Gottlieb>Bye.</v>

01:27:53.981 --> 01:27:58.141
<v Val Levitan>Okay, okay. Thank you very much. Can I answer any of your questions?</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

01:29:25.581 --> 01:29:26.861
<v Efim Podvoiski>Just summarize.</v>

01:29:28.781 --> 01:29:31.181
<v Val Levitan>Yeah, summarize, actually. It looks like it's all right.</v>

01:29:31.341 --> 01:29:31.821
<v Lena Zhukova>Mhm.</v>

01:29:33.181 --> 01:29:33.741
<v Lena Zhukova>So, Kim.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

01:31:14.301 --> 01:31:16.141
<v Michael Gottlieb>Okay, we'll talk to you later.</v>

01:31:16.621 --> 01:31:18.381
<v Val Levitan>Okay guys, have a good weekend.</v>

01:31:17.781 --> 01:31:20.221
<v Lena Zhukova>Have a good weekend, bye.</v>

01:31:18.341 --> 01:31:19.101
<v Michael Gottlieb>Yep, take care.</v>

01:31:18.621 --> 01:31:20.621
<v Efim Podvoiski>Send you too. Bye.</v>

01:31:19.821 --> 01:31:20.541
<v Val Levitan>Thank you, buddy.</v>

