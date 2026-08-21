# Raw Transcript — Game_Development — NOVA Capability Wishlist (Segment 2 of 2)
**Date:** August 14, 2026, 2:09 PM ET
**Segment:** Segment 2 of 2
**Summary note:** [[Meeting_Notes_NOVA_Capability_Wishlist-August-14-2026-Part_2]]
---
WEBVTT

00:00:03.106 --> 00:00:22.386
<v Michael Gottlieb>of the product, right? So it starts with the envisioning of what the product is. And in my kind of dream perfect world, I would love a tool that has templates. Okay, and what do I mean by that? If I want to start a one real...</v>

00:00:23.346 --> 00:00:42.866
<v Michael Gottlieb>three by three, I've got a template that I can open for that, and that we have a handful of template math behaviors, math characteristics, right, that we could literally have math models of games that we've done before, and then have the ability</v>

00:00:42.946 --> 00:01:01.506
<v Michael Gottlieb>to modify those math models on the fly. And this could be fantasy land, but the idea of changing, you know, right now of free spins is whatever, one and 120. I'd love to be able to just punch into a pulldown menu. Let me try one and 110 or, you know.</v>

00:01:02.066 --> 00:01:22.386
<v Michael Gottlieb>one in 100 and see what that feels like. Now, accordingly, as Efim would say, if you're taking, you know, that changes hit frequencies and it does all sorts of stuff, and I'm not sure how to exactly contend with that. Efim might somehow, it might have some ideas, but I think that would be</v>

00:01:22.866 --> 00:01:41.986
<v Michael Gottlieb>fantastic to be able to play with and give us a sandbox to try some different things. Why do I bring this up? Here's a perfect example. We've got this game called Crazy Spins and Efim and I have been coming up with different changes that we could conceivably make to it.</v>

00:01:42.386 --> 00:02:01.866
<v Michael Gottlieb>But without going through a fairly extensive process of implementing the change, and we don't really have like a dev environment where we can goof around, we basically have to have to touch a programmer if we wanted to say, you know, have different behavioral symbols on Real 4, if we wanted Real 4 to do something different.</v>

00:02:02.146 --> 00:02:23.346
<v Michael Gottlieb>than Real 4 currently does, right? And we have to, and that's a very key point of what I'm saying is that the more we can do without the programmers, the better off everybody is. And then moving beyond that in terms of the production environment and putting games together,</v>

00:02:24.146 --> 00:02:47.546
<v Michael Gottlieb>I would strongly advocate for something that people always talk about, but it never seems to happen. And what it is, it's called a modular code base. So there's modules, right? If we've got free spins with added wilds, that is its own module. And like Legos, if we have a game and we went, okay, I want free spins with added wilds, I want to be able to take that module</v>

00:02:48.386 --> 00:03:07.186
<v Michael Gottlieb>and plug that into the game. Now, this is on the programmer side. And unfortunately, what ends up happening is stuff gets spaghetti-ized and intertwined. And there isn't necessarily the, because we push so hard, and everybody does in this business, technical debt gets generated.</v>

00:03:07.466 --> 00:03:27.346
<v Michael Gottlieb>it doesn't necessarily get dealt with and addressed, and it becomes highly problematic to execute kind of on a modular level, right? Great example would be, okay, so we've got 3 symbols trigger something. I want 3 symbols to trigger free spins.</v>

00:03:27.586 --> 00:03:47.346
<v Michael Gottlieb>Now, maybe I wanted to trigger a hold and re-spin bonus. If the code is done in a modular way, I should be able to unplug that one thing and plug something else in there comparatively painlessly, right? What we do now is what a lot of the companies do, which is basically we build on the previous code base, which was built on a previous code base.</v>

00:03:47.746 --> 00:04:07.986
<v Michael Gottlieb>and it's a cumulative thing. And then new engineers get involved and it can be really, really challenging. So I was thinking about that. And then obviously, I'm sure Juan will talk to, oh, obviously better debug tools and logging. I'm not an engineer, so maybe I'm missing something, but I'm hearing things about.</v>

00:04:08.146 --> 00:04:28.066
<v Michael Gottlieb>Things are crashing and we're having, it's taking time to debug them. I don't know if that means we need more debug information, different debug information, a way to look at what the hell happened 3 cycles before it crashed and things of that nature. But better debug tools and better logging tools.</v>

00:04:28.226 --> 00:04:49.306
<v Michael Gottlieb>And then on the end of the process, you talk about fantasy dream. I'd love to be able to log into a machine and look at its performance, right? Just log into a machine with Wi-Fi and look at its performance. And I know there needs to be a wall of what we necessarily have access to. I mean, maybe I don't get actual numbers. Maybe I just get percentages.</v>

00:04:49.426 --> 00:05:09.186
<v Michael Gottlieb>Right, because I know that our customers don't necessarily want to share data. But if I could see nothing more than this machine has six games, and here is the percentage breakdown of play of which game is most popular to which game is least popular, and then maybe average bet or something along those lines.</v>

00:05:09.466 --> 00:05:25.586
<v Michael Gottlieb>just that alone could be hugely valuable. And that's, I wouldn't think that's information the operator would be too wound up about. So anyway, those are, that's a lot. Those are a couple of top level thoughts, but I guess at this juncture, I'll turn it over to whomever wants to pick it up.</v>

00:05:29.826 --> 00:05:30.786
<v Juan Martinez>I'll go last.</v>

00:05:33.346 --> 00:05:54.946
<v Lena Zhukova>Okay, I can go like a minimal product would be like working properly. Miranda design environment with manifest, which will help us to create scenes much faster. We did not try it yet, so it was like manifest.</v>

00:05:55.026 --> 00:06:15.586
<v Lena Zhukova>So, very like implemented, but because we did not produce like anything in Omnia except Kayocho, so we didn't have chance like to really like benefit to feel the benefit from it, and also like adding ability to see it.</v>

00:06:15.666 --> 00:06:36.426
<v Lena Zhukova>Toppers in in the build, because we decided not to do toppers for Kaiochi only, and we definitely will need them, so we need to include them in the build, and also we need to work with show mode, because show mode was extremely limited for Kaiochi only. We had a lot of...</v>

00:06:38.866 --> 00:06:54.786
<v Lena Zhukova>requirements for show mode, but developers said like they didn't have time at the moment when we asked. So we need a pretty advanced show mode to model all kind of situations inside the game.</v>

00:06:56.066 --> 00:07:17.106
<v Lena Zhukova>We need to finish working with framework dialogues because, again, we did something, but then we decided we are not going to release only and we did not test it properly, so we need to see how our like approach with dialogues is it working properly or not.</v>

00:07:17.426 --> 00:07:40.546
<v Lena Zhukova>So this is like working like elements which we definitely need to release games in the fantasy land. And we definitely need integration of this mass game launcher into design environment so we can use mass as soon as possible.</v>

00:07:40.946 --> 00:07:57.186
<v Lena Zhukova>Add our art assets, see the real gameplay inside Miranda, even before creating a build. Change assets if you don't like how animation works, for example, in this.</v>

00:07:59.626 --> 00:08:19.706
<v Lena Zhukova>Together with other symbols, so we definitely we can see like size of the symbols is all for, like, for example, like with this lines in the lines features, right? So, yeah, first we thought that it's going to be a good idea to create a huge line, but then when we see this line with other symbols, we immediately see that we need.</v>

00:08:19.826 --> 00:08:39.346
<v Lena Zhukova>to reduce size of this line. And all these experiments we can do like in half an hour if we can run spins inside Miranda. And it's possible, I know it for sure. Like I talked to Dima already, but it will need time to build this system.</v>

00:08:41.026 --> 00:08:51.906
<v Lena Zhukova>Yes, changing art assets for artists and see immediate results, it would be like the most probably important part from my side.</v>

00:09:06.426 --> 00:09:27.226
<v Efim Podvoiski>Okay, I came here with a request to have a better prototype and can Lena and Michael already mentioned it. So one thing that is not exactly Nova, but the whole system, including backend, the holy grail, I think, is to be able to see players behavior.</v>

00:09:06.866 --> 00:09:07.426
<v Juan Martinez>Aksamit.</v>

00:09:27.306 --> 00:09:38.146
<v Efim Podvoiski>The actual players, uh, to see if I what will they do at the machine particular player, not just not just average.</v>

00:09:39.026 --> 00:09:50.786
<v Efim Podvoiski>Across all of them, but to see, OK, this player came with $60, put $20, played, put $20, played, won, changed bet, and so on, so we could.</v>

00:09:52.146 --> 00:09:53.586
<v Efim Podvoiski>Charter to the players.</v>

00:09:55.586 --> 00:10:01.466
<v Efim Podvoiski>Ideally, because right now we don't know what they don't know what they want, really.</v>

00:10:03.266 --> 00:10:19.746
<v Efim Podvoiski>We can compare our games to our games. We can compare our games to other people games, our machines to other people machines from the worlds of operators. But we don't really know what exactly players do.</v>

00:10:22.306 --> 00:10:25.906
<v Efim Podvoiski>And cannot guess why they like this and don't like this.</v>

00:10:28.066 --> 00:10:38.546
<v Efim Podvoiski>And this is, this is still not, it is not a silver bullet, but it's one more stone in the world to be able to predict.</v>

00:10:39.426 --> 00:10:42.146
<v Efim Podvoiski>Is the game good or not before we release it?</v>

00:10:47.986 --> 00:11:03.266
<v Juan Martinez>And it seems some of the things you mentioned are beyond SAS 602 protocol. You're suggesting that we would gather that type of data through directly through the operating system and not necessarily SAS, correct?</v>

00:11:03.586 --> 00:11:04.466
<v Efim Podvoiski>Yes, yes.</v>

00:11:09.426 --> 00:11:12.546
<v Efim Podvoiski>And ideally, ideally, tracking the players.</v>

00:11:14.546 --> 00:11:18.626
<v Efim Podvoiski>If you have more than, if you have more than one machine application.</v>

00:11:14.986 --> 00:11:15.506
<v Juan Martinez>Val.</v>

00:11:19.826 --> 00:11:22.466
<v Efim Podvoiski>We would like to know what this player did.</v>

00:11:24.146 --> 00:11:31.666
<v Juan Martinez>Right, but obviously without access to player tracking, which say doesn't exist in Georgia, are we just going to assume?</v>

00:11:28.386 --> 00:11:32.226
<v Efim Podvoiski>Yeah, yeah, yeah, yeah. I am dreaming. I am dreaming.</v>

00:11:33.586 --> 00:11:41.946
<v Juan Martinez>that a cash out means a new player came in. We could use that as a trigger, right? If the... Okay.</v>

00:11:40.546 --> 00:11:41.026
<v Efim Podvoiski>Right.</v>

00:11:45.426 --> 00:11:54.386
<v Efim Podvoiski>The problem is when it reaches 0 and in 20 seconds somebody put another $20. Is it is it a new player or not?</v>

00:11:54.866 --> 00:11:56.706
<v Juan Martinez>Yeah, we would. We would not know.</v>

00:12:05.586 --> 00:12:24.706
<v Juan Martinez>Yeah, I can tell you Light and Wonder showed a prototype to us once about, you know, installing a camera at a machine that could tell you if it was male or female and that just didn't go over well with the industry. You know, they were trying to not do pure facial recognition,</v>

00:12:25.106 --> 00:12:41.826
<v Juan Martinez>but form recognition, but it's still, it was hard from a gaming perspective and just the overall policies of, you know, being tracked just didn't go over well, but there is value to what you asked for, that's for sure.</v>

00:12:47.186 --> 00:12:48.386
<v Juan Martinez>Is that a Efim?</v>

00:12:49.106 --> 00:12:50.786
<v Efim Podvoiski>Yes, I don't.</v>

00:12:50.226 --> 00:13:08.746
<v Juan Martinez>Okay, okay. Yeah, I mean, so for me, I've got five points and I'll e-mail them out to everybody after we're done. But the, I guess the most critical part is game recovery. You know, in many cases, our games crash. Well, let me go back to what Michael said.</v>

00:13:09.106 --> 00:13:27.426
<v Juan Martinez>The modular structure is what I think we need to get to. You know, separating the game framework from anything else that the game does. You know, why would a printer failure take down the cabinet when there's a bunch of other working components? And I'd like for us to think about...</v>

00:13:27.746 --> 00:13:28.226
<v Juan Martinez>You know.</v>

00:13:29.506 --> 00:13:45.906
<v Juan Martinez>creating compartments or modules where all of these devices exist in their own little world, but don't necessarily affect each other when there is a crash. And I'll write that up fully. And then the next thing is,</v>

00:13:46.866 --> 00:14:06.226
<v Juan Martinez>I think we need a location for backup memory. When our games crash, they crash hard, and it's very hard to do forensics. You know, I think ideally we want to create a constantly written to second set of memory where we could recover.</v>

00:14:06.306 --> 00:14:25.586
<v Juan Martinez>the game in any state because we've recorded it and saved it elsewhere in RAM or somewhere else so that the customers don't have to do a full reinstall, which means wiping out the data, which means alerting the regulator, which means people not getting paid right away because</v>

00:14:25.906 --> 00:14:32.546
<v Juan Martinez>You're not exactly sure how much you owe them. So I think that that one is critical for us.</v>

00:14:34.946 --> 00:14:35.186
<v Efim Podvoiski>Mm.</v>

00:14:39.826 --> 00:14:59.546
<v Juan Martinez>And I mean, the next one is also just a jurisdictional layer. You know, I think that if a lot of the base code is the same and there's just the uniqueness of going to South Dakota where they've got a $1000 win cap or, you know, Nebraska with the Simon Says memory</v>

00:15:01.106 --> 00:15:22.546
<v Juan Martinez>section, but if the base games are very close, can we just separate what's a jurisdictional requirement separately from the game? And we may be doing that today, I'm not sure, i.e. these fixes we're doing in Georgia, we're able to do them without affecting the game per se and not changing any CRCs.</v>

00:15:23.026 --> 00:15:26.626
<v Juan Martinez>So that's a direction I want us to continue going in.</v>

00:15:35.106 --> 00:15:42.386
<v Juan Martinez>And I've got these written up, so I'll share them here shortly. I'll just renumber them in MVP order.</v>

00:15:48.306 --> 00:15:57.266
<v Juan Martinez>I didn't mention about RIS Val, because we're already working on making that go away. So I just assumed that that would carry over to Nova.</v>

00:16:06.066 --> 00:16:07.346
<v Efim Podvoiski>Raise going away.</v>

00:16:07.906 --> 00:16:22.786
<v Juan Martinez>Well, you know, today in South Dakota, Nebraska, the operators are unhappy with us because they always need to call JVL to make a setting change to the machine because we've locked it.</v>

00:16:21.906 --> 00:16:31.346
<v Val Levitan>It's not, it's not going away. We're addressing the negative side of RAS that.</v>

00:16:32.226 --> 00:16:33.666
<v Val Levitan>is hindering.</v>

00:16:34.786 --> 00:16:37.026
<v Val Levitan>A third-party operation.</v>

00:16:38.626 --> 00:16:43.986
<v Val Levitan>But you know, I look at it as RIS evolving rather going away.</v>

00:16:45.626 --> 00:17:05.666
<v Juan Martinez>Correct. Yeah, basically the ability to allow the local operator to make a manual setting change without needing a new file from us. If they want to move the machine 5 hours away and it's in a different time zone, they should be able to change the time zone. They don't need our permission to do that, as an example.</v>

00:17:12.706 --> 00:17:13.746
<v Val Levitan>Thank you very much.</v>

00:17:15.426 --> 00:17:17.266
<v Val Levitan>I appreciate everybody's input.</v>

00:17:18.466 --> 00:17:24.546
<v Val Levitan>I can assure you that many things that you mentioned here have already been discussed.</v>

00:17:33.906 --> 00:17:36.946
<v Val Levitan>But nevertheless, it's good to hear it from you.</v>

00:17:38.346 --> 00:17:45.186
<v Val Levitan>Aside from trying to generate an engineering solution to how it's done.</v>

00:17:48.226 --> 00:17:48.786
<v Val Levitan>Um...</v>

00:17:51.346 --> 00:17:54.786
<v Val Levitan>Lena, I would recommend for you to rephrase your...</v>

00:17:56.626 --> 00:18:07.026
<v Val Levitan>desirable outcome without generating an engineering solution of how it is called on or how it is done.</v>

00:18:08.306 --> 00:18:19.026
<v Val Levitan>So you would like to see something happen, but you're automatically limiting yourself with thinking about a manifest or Miranda.</v>

00:18:21.306 --> 00:18:30.226
<v Val Levitan>which may or may not be an engineering solution, I don't know. So it's better to focus on what you want to do instead of how it is done.</v>

00:18:33.106 --> 00:18:33.586
<v Lena Zhukova>Okay.</v>

00:18:34.386 --> 00:18:40.066
<v Val Levitan>Can we have an open conversation and just shoot the **** about?</v>

00:18:41.826 --> 00:18:49.826
<v Val Levitan>each of you with Elon Musk and you can buy a city or town in Texas and</v>

00:18:51.746 --> 00:18:55.666
<v Val Levitan>shoot rockets to Mars every 45 minutes.</v>

00:18:57.986 --> 00:18:59.586
<v Val Levitan>and build a Tera factory.</v>

00:19:02.306 --> 00:19:04.546
<v Val Levitan>Terra Fab Factory in Texas.</v>

00:19:06.146 --> 00:19:11.906
<v Val Levitan>So let's apply this to JVL and just.</v>

00:19:15.346 --> 00:19:17.586
<v Val Levitan>For example, let me start this conversation.</v>

00:19:19.266 --> 00:19:19.986
<v Val Levitan>Um...</v>

00:19:22.306 --> 00:19:36.546
<v Val Levitan>I like if we can place a camera in the machine and identify a player. I don't know, does it have to be a camera, maybe a scent detector, maybe a heartbeat, maybe a pulse generator, I don't know.</v>

00:19:37.506 --> 00:19:38.066
<v Val Levitan>Thank you.</v>

00:19:40.626 --> 00:19:41.506
<v Val Levitan>What could it be?</v>

00:19:43.826 --> 00:19:46.946
<v Val Levitan>I love the idea of being able to identify a player.</v>

00:19:47.706 --> 00:19:54.306
<v Juan Martinez>Yeah, well, like what we ran into with the gaming commission was when you say camera.</v>

00:19:54.706 --> 00:20:03.186
<v Val Levitan>Let me let me just let me just quickly and abruptly stop this. Let's assume that gaming commission is cooperating.</v>

00:20:05.346 --> 00:20:08.466
<v Val Levitan>Um, let me, let me also take it further.</v>

00:20:09.906 --> 00:20:15.106
<v Val Levitan>In the next five years, I don't see much business coming out from Class 3 market.</v>

00:20:16.706 --> 00:20:32.466
<v Val Levitan>So it's a street market for us. And we could do all kinds of interesting things on the street market. What can we do? How can we win that war? I think it was Michael Gottlieb who said, well, maybe we should focus on what we do best.</v>

00:20:33.746 --> 00:20:37.466
<v Val Levitan>Street market is better for us than competing with Light and Wonder and...</v>

00:20:39.666 --> 00:20:40.466
<v Val Levitan>Cluster.</v>

00:20:41.426 --> 00:20:43.986
<v Val Levitan>Maybe, maybe, just maybe. I don't know.</v>

00:20:45.826 --> 00:20:47.426
<v Val Levitan>Remember, we're shooting **** here, right?</v>

00:20:48.506 --> 00:21:03.346
<v Juan Martinez>Yeah, yeah. Well, I mean, so a camera is okay, as long as we don't use the word facial recognition and that we are not storing that information anywhere.</v>

00:21:04.306 --> 00:21:23.506
<v Juan Martinez>But that's the cell that, hey, we use it. We know that at, you know, 1125 A.m. the person who played this game, their pattern looked like it was a woman or it looked like it was a man. And we've recorded that and we use it on our side, but there's no.</v>

00:21:23.986 --> 00:21:26.026
<v Juan Martinez>No traceable evidence in the machine.</v>

00:21:24.586 --> 00:21:44.946
<v Val Levitan>It doesn't, it doesn't, it doesn't have to be. It could be, we could say this shadow in front of the machine has not moved from, you know, certain time to certain time, and it was the same shadow or the same height or the same volume of shadow.</v>

00:21:45.506 --> 00:21:48.466
<v Val Levitan>That inserted bills.</v>

00:21:49.106 --> 00:21:49.346
<v Juan Martinez>Sure.</v>

00:21:49.506 --> 00:21:54.706
<v Val Levitan>It wasn't a different shadow; it was it wasn't something else; it was the same mass of.</v>

00:21:55.826 --> 00:22:01.666
<v Val Levitan>of BLOB that stood in front of the machine and inserted cache.</v>

00:21:57.986 --> 00:21:58.306
<v Juan Martinez>Yeah.</v>

00:22:04.546 --> 00:22:20.066
<v Efim Podvoiski>But if you don't save names or something, why do cannot be saved like signature of the face or something? So we know that this player came back in two weeks or that she moved to another machine.</v>

00:22:18.626 --> 00:22:19.426
<v Val Levitan>And to say...</v>

00:22:20.506 --> 00:22:22.626
<v Val Levitan>and then profile, say white or black.</v>

00:22:23.706 --> 00:22:25.506
<v Val Levitan>Or Chinese, so.</v>

00:22:25.066 --> 00:22:25.306
<v Juan Martinez>Yeah.</v>

00:22:25.426 --> 00:22:29.826
<v Efim Podvoiski>Yes, is this true? Yeah, that I didn't didn't think about it yet, but yes.</v>

00:22:31.786 --> 00:22:43.826
<v Michael Gottlieb>Juan, if you remember a lifetime ago, WMS actually had a player pin thing that they did back in the days of Star Trek. I think it was Star Trek.</v>

00:22:38.946 --> 00:22:39.306
<v Juan Martinez>Yeah.</v>

00:22:42.666 --> 00:22:48.706
<v Juan Martinez>Yeah, yeah, it was definitely the start. It was with Star Wars. I mean Star Trek, sorry. Yes. The journey.</v>

00:22:46.706 --> 00:23:10.266
<v Michael Gottlieb>Star Trek, and you sit down and, exactly, and you would get a pin, and then when you came back for repeat play, you would enter that pin in and it would save your progress. And the concept was that the player would be willing to re-enter their pin and be</v>

00:23:10.346 --> 00:23:30.386
<v Michael Gottlieb>tracked because the tracking was something interesting that they were actually making progress within the game, but it didn't, it kind of fizzled because you can't have state, you can't have, you know, true persistent state in a slot machine. So all you could do is, you know,</v>

00:23:17.746 --> 00:23:18.066
<v Juan Martinez>Yeah.</v>

00:23:30.506 --> 00:23:49.666
<v Michael Gottlieb>change the galaxy you were playing the slot machine in or something silly like that and it didn't have any have any stickiness associated with it. It's interesting because in a perfect scenario, you would love every player to sit down and punch in their JVL pin and for us to be able to give them a reason to do that.</v>

00:23:49.706 --> 00:24:12.466
<v Michael Gottlieb>but it is counterproductive and counterintuitive. Here would be a perfect example, right? Let's say we do a puppy game and it's all about collecting puppies. And as you progress in every, you know, each time you play free spins, you get an additional puppy and those puppies get saved in your puppy pen or whatever.</v>

00:24:11.906 --> 00:24:12.306
<v Juan Martinez>Right.</v>

00:24:12.986 --> 00:24:35.346
<v Michael Gottlieb>Well, conceptually, all of that sounds great, but the problem you run into is that, and believe me, I designed video games for 15 years before I came to this world. Any of that mishugas takes the player away from 6 seconds of spin, right? It breaks the rule that you want them to be gambling. You don't want them to be goofing around looking at their puppies.</v>

00:24:28.346 --> 00:24:28.626
<v Juan Martinez>Right.</v>

00:24:34.786 --> 00:24:38.226
<v Juan Martinez>Yeah, yeah, yeah, but I mean, so...</v>

00:24:39.306 --> 00:24:43.346
<v Juan Martinez>What WMS did, you know, in fact, it was called episodic.</v>

00:24:43.586 --> 00:24:44.066
<v Michael Gottlieb>Mhm.</v>

00:24:44.226 --> 00:25:04.226
<v Juan Martinez>journeys. Like a video game, when you're playing, you make it to level one, you make it to level 2, you make it to level 3, and what that pin let you do is if you made it to level 3, but you cashed out when you came back and entered your pin, you knew you were going to already be at level 3 when you got to that bonus.</v>

00:25:04.546 --> 00:25:04.946
<v Michael Gottlieb>Right.</v>

00:25:04.866 --> 00:25:09.666
<v Juan Martinez>So, I honestly, I just think that that was ahead of its time.</v>

00:25:09.946 --> 00:25:10.546
<v Michael Gottlieb>Mm-hmm.</v>

00:25:10.946 --> 00:25:19.906
<v Juan Martinez>You know, but I, there is, there's, I think that's a good way to incentivize a player to come back, you know, just, just for their pin.</v>

00:25:23.586 --> 00:25:23.986
<v Juan Martinez>You know.</v>

00:25:23.826 --> 00:25:27.426
<v Val Levitan>There was a thing discussed at JVL that...</v>

00:25:30.706 --> 00:25:42.866
<v Val Levitan>If somebody won a mega win and wanted to brag about it, we would allow them to record that winning session and post it on social media.</v>

00:25:46.466 --> 00:25:48.306
<v Val Levitan>So, for that, he would need...</v>

00:25:50.546 --> 00:25:52.626
<v Val Levitan>We would know who it is.</v>

00:25:54.826 --> 00:25:55.066
<v Juan Martinez>Yeah.</v>

00:25:55.506 --> 00:26:01.746
<v Val Levitan>Do we want a feature like this? Because we'll have to kind of have a recording of things.</v>

00:26:02.306 --> 00:26:21.746
<v Michael Gottlieb>We, you know, the problem, the challenge associated with that, we played with that at Bally and the, I think they spent, as they always did, stupid money on focus groups. And the response from the focus groups, the translation was, hey man, if I'm playing a slot machine with somebody other than my wife,</v>

00:26:21.826 --> 00:26:46.746
<v Michael Gottlieb>if you know what I'm saying. I don't want anybody to know about it. Hey man, if I have a big win, I don't want my friends to know about it. I don't want social media to know about it. So I would say that there is a large, massive universe of players, but there's an incredibly small universe of what, let's just call them influencers, right? There's maybe 10, 20,</v>

00:26:22.066 --> 00:26:22.466
<v Juan Martinez>Yeah.</v>

00:26:30.266 --> 00:26:30.546
<v Juan Martinez>Right.</v>

00:26:46.826 --> 00:27:08.066
<v Michael Gottlieb>30 people online that post their wins and they have followers, they've monetized it, right? They found a way to make money themselves because hey, I'm slot machine gal and hey, look at my big winner or whatever else. And so in any case, the data that we got out of it and all the money that we spent on the marketing was.</v>

00:27:08.626 --> 00:27:18.626
<v Michael Gottlieb>People are, when it comes to money, people are incredibly private and they no more want to post their win than they do video of them pulling money out of an ATM.</v>

00:27:20.146 --> 00:27:20.386
<v Juan Martinez>Yeah.</v>

00:27:20.946 --> 00:27:22.226
<v Val Levitan>Have you, um...</v>

00:27:23.506 --> 00:27:23.986
<v Val Levitan>Um...</v>

00:27:28.466 --> 00:27:30.306
<v Val Levitan>Do you guys have social media?</v>

00:27:31.506 --> 00:27:32.066
<v Val Levitan>I don't.</v>

00:27:33.106 --> 00:27:35.266
<v Michael Gottlieb>I do, I'm on everything. I just never post.</v>

00:27:35.826 --> 00:27:36.946
<v Juan Martinez>Yeah, me too.</v>

00:27:36.146 --> 00:27:40.546
<v Val Levitan>Okay, but, but no, I understand, but do any of you post?</v>

00:27:42.146 --> 00:27:42.466
<v Juan Martinez>No.</v>

00:27:42.546 --> 00:27:43.346
<v Efim Podvoiski>Very little.</v>

00:27:42.786 --> 00:27:44.706
<v Val Levitan>So, I find that I find.</v>

00:27:43.746 --> 00:27:54.066
<v Juan Martinez>I just want to stay in touch with the technology and the features, but other than a couple pictures of my cars and my cameras, I haven't posted anything in years.</v>

00:27:55.266 --> 00:27:56.066
<v Val Levitan>So, I...</v>

00:27:55.426 --> 00:27:59.106
<v Lena Zhukova>I have, yeah, I have Instagram, but I don't post; I just follow people.</v>

00:28:00.506 --> 00:28:01.826
<v Val Levitan>So, I found that.</v>

00:28:03.266 --> 00:28:04.146
<v Val Levitan>Alarming.</v>

00:28:04.946 --> 00:28:08.226
<v Val Levitan>when people post pictures of their children.</v>

00:28:08.466 --> 00:28:09.026
<v Michael Gottlieb>Oh yeah.</v>

00:28:09.426 --> 00:28:09.746
<v Juan Martinez>Yeah.</v>

00:28:10.226 --> 00:28:10.786
<v Lena Zhukova>I agree.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

00:29:03.106 --> 00:29:04.146
<v Michael Gottlieb>Well, and the other...</v>

00:29:03.266 --> 00:29:12.626
<v Val Levitan>So my question is whether Val research is valid in today's AMH. I'm not saying that it wasn't valid then.</v>

00:29:14.226 --> 00:29:16.866
<v Val Levitan>Everything that you, Michael.</v>

00:29:20.426 --> 00:29:22.466
<v Val Levitan>Is it Friday? Is it good? Yeah.</v>

00:29:21.266 --> 00:29:31.186
<v Michael Gottlieb>I think it's more valid. I think it's more valid, and I'll tell you why. I'll tell you why it's more valid. I think that the number of people that have gotten X...</v>

00:29:22.946 --> 00:29:23.266
<v Juan Martinez>Yeah.</v>

00:29:32.346 --> 00:29:37.746
<v Michael Gottlieb>Exposed or in trouble because they had a job and the or they were.</v>

00:29:38.946 --> 00:29:45.586
<v Michael Gottlieb>to get a job and somebody who researched their social media and the number of people, especially young people, there was that whole phase of...</v>

00:29:46.586 --> 00:29:49.026
<v Michael Gottlieb>Where they were posting themselves.</v>

00:29:53.026 --> 00:29:57.346
<v Michael Gottlieb>and they were partying and they were showing off their living their best life.</v>

00:29:57.906 --> 00:30:17.586
<v Michael Gottlieb>You're talking about Justin Trudeau? Sure. Well, I mean, yeah, it's up and down. It's all of them. Remember the guy that was at the Coldplay concert and he was at the Coldplay concert and the camera cut to him and he was holding the HR one? That cost, yeah, that cost them.</v>

00:29:59.986 --> 00:30:00.306
<v Juan Martinez>Ha ha ha.</v>

00:30:08.146 --> 00:30:08.546
<v Juan Martinez>Yeah.</v>

00:30:12.946 --> 00:30:15.026
<v Val Levitan>The, the, the lover.</v>

00:30:17.746 --> 00:30:36.746
<v Michael Gottlieb>everything, right? So the thing is, is that, you know, you're not safe anywhere. And I can tell you that both of my boys came into social media after all of that Mickey Mouse took place. So if they post pictures, it's them of maybe doing athletic sports.</v>

00:30:37.066 --> 00:31:00.746
<v Michael Gottlieb>or maybe at a food festival or something like that. But I mean, neither of them drink anyway. But I think that there's a real awareness on the part of people that you are being watched, your behavior can be researched, people can see what you're doing. And now, I mean, Juan knows about this, of course, as well, is that you've got these, I'll call them sour grapes people.</v>

00:31:01.066 --> 00:31:20.586
<v Michael Gottlieb>on LinkedIn, you know, they'll do whatever, 20 years at IGT, they get fired, and then they post these freaking paragraphs of ranting on LinkedIn about how awful IGT is and how they got F'd by Apollo and all of this stuff. And it's like, are you trying to never get a job in your life? You know, are you trying to never, never mind the.</v>

00:31:09.466 --> 00:31:09.866
<v Juan Martinez>Yeah.</v>

00:31:21.746 --> 00:31:30.106
<v Michael Gottlieb>The fact that adults take whatever their issues are directly to the person that's creating the issue, you don't do that separately. That's...</v>

00:31:30.986 --> 00:31:33.426
<v Michael Gottlieb>That's like childish behavior, but apparently a lot of people are...</v>

00:31:34.986 --> 00:31:36.266
<v Michael Gottlieb>Having a lot of emotional.</v>

00:31:37.546 --> 00:31:48.986
<v Michael Gottlieb>Issues right now, so stated, I mean, I get it, but if you're looking for a job, that behavior is counterproductive. Nobody's attracted to vinegar and acid, right?</v>

00:31:49.386 --> 00:31:54.666
<v Val Levitan>Okay, point well taken. No posting.</v>

00:31:57.146 --> 00:32:00.266
<v Val Levitan>Does it does it also kill our camera ambitions?</v>

00:31:59.786 --> 00:32:16.826
<v Juan Martinez>Well, so just a quick note on that. So I think I had an old stat from IGT saying that for every 20 jackpots that were awarded, only one person out of 20 would agree to hold the check up and take his picture. But</v>

00:32:18.826 --> 00:32:38.666
<v Juan Martinez>So a lot of casinos have shifted not to showing the player winning, but showing the machine announcing the jackpot win. That we could do. If we could take a screenshot of our own machine in lockup mode that displays the payout amount, that is something we could post and remains anonymous.</v>

00:32:40.906 --> 00:32:41.946
<v Juan Martinez>You know, hey, another.</v>

00:32:42.826 --> 00:32:52.346
<v Juan Martinez>That part of the JDL game, and we we've got a picture of the screen, which, you know, a screenshot of our own screen with no human in it, and that that posting has value.</v>

00:32:56.106 --> 00:32:57.226
<v Val Levitan>Is this what we want to do?</v>

00:33:00.586 --> 00:33:17.786
<v Juan Martinez>I think it's interesting. I'd like to know how much work is involved. Like with all the things we have going on, I wouldn't say it's priority #1 and maybe understanding the engineering work behind it would help me better answer that question.</v>

00:33:19.386 --> 00:33:22.346
<v Val Levitan>I don't think engineers will be objective about it.</v>

00:33:25.866 --> 00:33:27.946
<v Val Levitan>I have to be an engineer that says, yeah.</v>

00:33:29.226 --> 00:33:30.666
<v Val Levitan>I know we have time, we can do it now.</v>

00:33:32.426 --> 00:33:38.706
<v Juan Martinez>So yeah, because there's questions like where do we store that file to picture, so it's going to be a there's.</v>

00:33:32.666 --> 00:33:33.226
<v Val Levitan>Okarak.</v>

00:33:37.546 --> 00:33:46.186
<v Val Levitan>The storage, the storage has been resolved. We are going to put a black box in our machines.</v>

00:33:49.426 --> 00:33:55.306
<v Val Levitan>for other reasons, so storage should not be an issue. We're also installing your modem in every machine.</v>

00:33:56.826 --> 00:33:57.226
<v Val Levitan>Um...</v>

00:33:58.466 --> 00:34:05.106
<v Val Levitan>Let's, okay, let's move on. I mean, I gotta push this meeting forward. Yeah.</v>

00:34:06.186 --> 00:34:09.786
<v Val Levitan>Inexpensive board and expensive board.</v>

00:34:11.386 --> 00:34:12.266
<v Val Levitan>So, Inna.</v>

00:34:13.786 --> 00:34:15.386
<v Val Levitan>Expensive work abilities.</v>

00:34:16.506 --> 00:34:19.226
<v Val Levitan>is roughly the D1000 scale.</v>

00:34:23.946 --> 00:34:28.506
<v Val Levitan>The expensive board is a lot of capabilities.</v>

00:34:30.026 --> 00:34:30.746
<v Val Levitan>So...</v>

00:34:31.946 --> 00:34:33.226
<v Val Levitan>When we compile the program.</v>

00:34:35.626 --> 00:34:40.506
<v Val Levitan>We can make it in a way relatively easy. We can make it in a way that it compiles for both.</v>

00:34:41.466 --> 00:34:44.666
<v Val Levitan>At the same time, do we want that capability?</v>

00:34:45.786 --> 00:34:48.266
<v Val Levitan>We want, do we want expensive and expensive?</v>

00:34:50.026 --> 00:34:53.706
<v Val Levitan>Or, or, or limit the capability, a lot of capabilities.</v>

00:34:56.586 --> 00:34:58.746
<v Juan Martinez>Val, because go ahead.</v>

00:35:00.946 --> 00:35:10.346
<v Juan Martinez>No, I mean, getting what if the customer loves the more advanced game with a couple of additional features, but now we have to offer from a C.</v>

00:35:11.506 --> 00:35:18.346
<v Juan Martinez>PU upgrade. We have a hard time getting them to just do software upgrades. Now imagine a hardware upgrade, you know.</v>

00:35:18.186 --> 00:35:21.466
<v Val Levitan>No, I mean two ranking, two different machines.</v>

00:35:25.066 --> 00:35:39.306
<v Efim Podvoiski>So, the let me understand, you are talking about because exactly the same code, but it knows on which machine it's running and it's gracefully reduces the effects to have the same to keep the performance or what?</v>

00:35:40.586 --> 00:35:46.826
<v Val Levitan>No, a game specifically designed for inexpensive and expensive.</v>

00:35:47.546 --> 00:35:48.986
<v Efim Podvoiski>Two different designs.</v>

00:35:49.866 --> 00:35:50.266
<v Val Levitan>Yeah.</v>

00:35:55.946 --> 00:35:56.906
<v Efim Podvoiski>It's probably.</v>

00:35:56.026 --> 00:35:58.026
<v Val Levitan>Do we have to worry about two sets of hardware?</v>

00:36:00.586 --> 00:36:10.826
<v Val Levitan>Because if you ask me choose one or the other, I'd rather overpay money and choose the very capable one and keep on pushing towards very capable all the time.</v>

00:36:12.586 --> 00:36:14.586
<v Juan Martinez>Yeah, that that makes more sense.</v>

00:36:16.266 --> 00:36:20.586
<v Val Levitan>So scrub the inexpensive one. Time to make decisions.</v>

00:36:21.866 --> 00:36:23.546
<v Val Levitan>Let me turn on for five seconds.</v>

00:36:22.026 --> 00:36:40.986
<v Juan Martinez>Yeah, if we're talking about five or eight years in CPU technology change, nobody in this call would want to buy an eight-year-old computer on purpose because you know how much better the new ones are. So this is the same scenario. The CPU has way more advancements than the older one.</v>

00:36:41.306 --> 00:36:53.946
<v Juan Martinez>And that doesn't mean we have to inundate new games with all of these features just because it can support it. We'll get there over a scale time, but I'm in favor of the new hardware.</v>

00:36:54.746 --> 00:37:15.146
<v Michael Gottlieb>I am. I mean, the theory with Moore's Law is prices are going to drop for the exact same stuff over time anyway, right? So if that's if that's what you're looking at. I guess I'll be back in a second, but something very controversial is if you presented me with, you know, I don't know what the VDEC costs.</v>

00:36:58.666 --> 00:36:59.066
<v Juan Martinez>Yeah.</v>

00:37:15.186 --> 00:37:16.666
<v Michael Gottlieb>versus mechanical buttons.</v>

00:37:17.946 --> 00:37:21.826
<v Michael Gottlieb>But I'd spend the money on the CPU and the hardware before I'd spend it on the VDEC.</v>

00:37:22.906 --> 00:37:22.986
<v Juan Martinez>The.</v>

00:37:23.386 --> 00:37:30.906
<v Michael Gottlieb>Maybe the VDEC is considered industry standard now, and it's expected, but I think with some of the feedback we got from, you know, we got from...</v>

00:37:32.426 --> 00:37:33.066
<v Michael Gottlieb>Felipe.</v>

00:37:36.186 --> 00:37:38.026
<v Michael Gottlieb>The mechanical buttons were perfectly fine.</v>

00:37:38.306 --> 00:37:38.506
<v Juan Martinez>Yep.</v>

00:37:41.946 --> 00:37:42.426
<v Juan Martinez>Agree.</v>

00:37:45.786 --> 00:38:03.306
<v Juan Martinez>And it's Light and Wonder has physical buttons. Aristocrat has physical buttons. IGT's older cabinet, which has not been replaced by new cabinet, has a very small V deck, you know, probably 4 by 6 inches.</v>

00:38:07.866 --> 00:38:19.866
<v Juan Martinez>But, I mean, we're in markets where these are operators and route operators and St. machines. So, you know, let's just say the V-DEC is a $1,500 part when you know a button is $5 each.</v>

00:38:24.586 --> 00:38:26.746
<v Val Levitan>summarize the decision, what is it?</v>

00:38:26.906 --> 00:38:50.186
<v Michael Gottlieb>I was just making the, well, let's take a step back. So I think Juan and I are both in agreement that the more expensive hardware makes sense. I decided, you know, you've got Moore's Law, where in theory, the price of the component should only come down over time. Electronics are obsolete the second they're released. So whatever we consider to be the high performance platform now, if we're going to ride that platform for some interval of time.</v>

00:38:50.506 --> 00:39:10.586
<v Michael Gottlieb>It's not going to be the most high performance platform a couple of years from now. The other point that I made is that somewhat controversially, perhaps, I'll say that if you presented me with a choice between the better hardware with no VDEC or the lower grade hardware with the VDEC, I would go for the higher grade hardware with no VDEC.</v>

00:39:11.066 --> 00:39:22.266
<v Michael Gottlieb>I think the VDEC's neat as a game designer, I think it's fun, but our competitors, our competitors are doing just fine without it, and I'd rather put the money into the into the motherboard.</v>

00:39:14.186 --> 00:39:28.906
<v Lena Zhukova>I mean, she said she said people were different. She said they used.</v>

00:39:33.146 --> 00:39:38.106
<v Val Levitan>I, I just want to, I just want to change the question slightly.</v>

00:39:38.506 --> 00:39:38.786
<v Michael Gottlieb>Okay.</v>

00:39:43.386 --> 00:39:51.146
<v Val Levitan>More capability, sorry, restricted capability or unrestricted capability of design.</v>

00:39:50.906 --> 00:39:52.746
<v Michael Gottlieb>Unrestricted capability.</v>

00:39:52.866 --> 00:39:53.466
<v Juan Martinez>Yeah, for sure.</v>

00:39:53.506 --> 00:39:55.706
<v Efim Podvoiski>What kind of question? What kind of equation is it?</v>

00:39:53.546 --> 00:39:54.186
<v Lena Zhukova>Of course.</v>

00:39:56.586 --> 00:39:58.346
<v Val Levitan>It's a it's a good question.</v>

00:39:59.706 --> 00:40:00.826
<v Val Levitan>It's a good question.</v>

00:40:02.106 --> 00:40:04.506
<v Val Levitan>Because I am.</v>

00:40:06.106 --> 00:40:08.426
<v Val Levitan>I am not certain that.</v>

00:40:12.106 --> 00:40:14.346
<v Val Levitan>Unrestricted is necessarily it.</v>

00:40:15.546 --> 00:40:16.346
<v Val Levitan>Great looking.</v>

00:40:21.506 --> 00:40:22.986
<v Juan Martinez>Are we talking about the CPU?</v>

00:40:24.266 --> 00:40:26.586
<v Val Levitan>No, overall, overall.</v>

00:40:24.906 --> 00:40:25.466
<v Juan Martinez>Pavel.</v>

00:40:28.106 --> 00:40:28.986
<v Val Levitan>The deck.</v>

00:40:30.506 --> 00:40:31.546
<v Val Levitan>As part of it.</v>

00:40:36.866 --> 00:40:39.546
<v Val Levitan>Transitions, elaborate transitions.</v>

00:40:48.386 --> 00:40:54.586
<v Michael Gottlieb>I mean, I think our competitors are running the same generation of hardware in those markets as they're running in Class Three.</v>

00:40:55.866 --> 00:41:14.546
<v Juan Martinez>Even worse, Aristocrats Mars X was obsoleted in Class 3, and that's what's in Georgia right now. You know, so they took their obsolete dual screen cabinet from Class 3 that came back in from leases and whatever, and that's what they're selling in Georgia.</v>

00:41:48.866 --> 00:42:01.146
<v Juan Martinez>Yeah, I mean, my statement would be if we could upgrade to the more advanced CPU graphics card package and shave some costs off the cabinet, that would, that still makes sense.</v>

00:42:45.386 --> 00:42:46.506
<v Val Levitan>Promo credits.</v>

00:42:48.266 --> 00:42:49.706
<v Val Levitan>In St. locations.</v>

00:42:52.266 --> 00:42:52.826
<v Val Levitan>Yes or no?</v>

00:42:56.266 --> 00:42:59.866
<v Juan Martinez>A street location like Texas, where anything goes.</v>

00:43:00.746 --> 00:43:01.706
<v Val Levitan>No, Georgia.</v>

00:43:00.746 --> 00:43:18.026
<v Juan Martinez>probably of value, but like I know Georgia has some anti-player incentivizing rules, which I think this would fall under. You know, we're giving money to the player under what condition?</v>

00:43:21.226 --> 00:43:23.706
<v Val Levitan>that they come in and spend it on the machine.</v>

00:43:25.466 --> 00:43:29.546
<v Val Levitan>I mean, it's non-cashable credit, so it's not.</v>

00:43:30.866 --> 00:43:37.306
<v Val Levitan>And I doubt very much that the law speaks about pro credits to a player.</v>

00:43:40.186 --> 00:43:57.706
<v Val Levitan>I mean, I'm not here to legislation, whether it's in Texas or in Nebraska. Let's not focus on the jurisdiction right now and the legislative restrictions. Let's talk about machine design.</v>

00:43:59.906 --> 00:44:03.666
<v Val Levitan>approach to how we do things from a technology perspective.</v>

00:44:04.226 --> 00:44:04.426
<v Juan Martinez>Sure.</v>

00:44:07.386 --> 00:44:25.306
<v Juan Martinez>Normally, promo credits are awarded to a specific player. So you would need a player tracking system. So you would know, hey, it's John's birthday today. Let's give him $5. All the markets we're currently in, there is no such thing as player tracking.</v>

00:44:25.626 --> 00:44:26.826
<v Juan Martinez>So, this would be a...</v>

00:44:25.666 --> 00:44:36.706
<v Val Levitan>Or a face, or a face, or excuse me for interruption, or a Facebook page where we say we have location at the XYZ address, and here's a QR code.</v>

00:44:37.866 --> 00:44:43.466
<v Val Levitan>Come with your phone, we scan your QR code, we don't even know, we don't even need to know who you are.</v>

00:44:44.586 --> 00:44:44.906
<v Juan Martinez>Sure.</v>

00:44:48.266 --> 00:44:50.146
<v Michael Gottlieb>So it's timely. Go ahead.</v>

00:44:48.346 --> 00:44:51.146
<v Juan Martinez>And how would... Oh, so go ahead, Michael.</v>

00:44:51.386 --> 00:45:12.266
<v Michael Gottlieb>I said this is timely because apparently Treasure Island in Las Vegas just ran a promotion within the last couple of days for $200 in free slot play. And it was so popular, there were people waiting in line up to six hours to do it. So it was so popular, they ended up canceling it.</v>

00:45:13.706 --> 00:45:25.106
<v Michael Gottlieb>But the flip is that a friend of mine messaged me the story and said, he said, these are the dregs of society. They burn through the 200 bucks and disappear because they have no money to begin with.</v>

00:45:25.786 --> 00:45:26.106
<v Juan Martinez>Right.</v>

00:45:26.626 --> 00:45:46.626
<v Michael Gottlieb>So it was just an interesting kind of anecdote that you're driving traffic, but not all business is good business, and these aren't customers. They're just leeches trying to get the 200 bucks in free play, going through it, and then they're done. So it's costing Treasure Island quite a bit of money on this promotion.</v>

00:45:46.746 --> 00:45:50.826
<v Michael Gottlieb>Obviously, of a much greater magnitude and scale, because you're doing, you know, 200 bucks.</v>

00:45:51.546 --> 00:45:51.826
<v Juan Martinez>Yeah.</v>

00:45:52.426 --> 00:45:53.386
<v Val Levitan>How interesting.</v>

00:45:54.426 --> 00:46:14.506
<v Juan Martinez>Yeah, no, we had the same thing at Hard Rock. We cut all the busing programs because that player who would get $20 in free play plus the free bus ride to and from the casino, once they played those $20, they never went into their wallet to get any more money out. They just hung around the casino.</v>

00:46:15.386 --> 00:46:25.066
<v Juan Martinez>getting free drinks and sodas, waiting for their bus to pick them up. So that takes up space from people who want to play and it became counterintuitive financially.</v>

00:46:25.266 --> 00:46:33.386
<v Michael Gottlieb>And you **** *** your regulars because there's some Yahoo on your machine, right? If you come into your location every Friday night, have a shot and a beer and you want to sit down.</v>

00:46:29.146 --> 00:46:29.426
<v Juan Martinez>Yeah.</v>

00:46:34.826 --> 00:46:47.706
<v Michael Gottlieb>and you and you love rodeo spins, all you want to do is play rodeo spins. You **** *** that player, he goes over to a different machine, your your your bottom sucker is in there, you know, getting his 20 bucks in free play, he disappears and nobody wins.</v>

00:46:50.906 --> 00:46:52.906
<v Val Levitan>Oh, how interesting. Agreed.</v>

00:46:59.306 --> 00:47:00.986
<v Val Levitan>Um, okay.</v>

00:47:03.866 --> 00:47:05.546
<v Val Levitan>inexpensive hardware.</v>

00:47:06.906 --> 00:47:08.346
<v Val Levitan>For home use.</v>

00:47:09.746 --> 00:47:12.906
<v Val Levitan>where we will put our slot machines briefly.</v>

00:47:14.106 --> 00:47:14.666
<v Val Levitan>With.</v>

00:47:18.106 --> 00:47:20.586
<v Val Levitan>Access to an offshore.</v>

00:47:24.426 --> 00:47:25.066
<v Val Levitan>Server.</v>

00:47:32.026 --> 00:47:41.266
<v Juan Martinez>Playing the machine you described is basically a dumb terminal, and you're actually playing a game that is online somewhere else.</v>

00:47:41.626 --> 00:47:42.346
<v Val Levitan>That's right.</v>

00:47:47.866 --> 00:47:50.506
<v Efim Podvoiski>Was I playing for money or for fun?</v>

00:47:48.546 --> 00:47:48.906
<v Michael Gottlieb>Bar.</v>

00:47:51.746 --> 00:47:59.466
<v Val Levitan>When you when you access a legal offshore terminal, then you play for money.</v>

00:48:08.106 --> 00:48:15.466
<v Juan Martinez>I've always liked that idea and COVID proved that something like that could be extremely successful if done right.</v>

00:48:16.506 --> 00:48:22.906
<v Juan Martinez>Um, the problem though is we, we still we now need to have tracking of the player.</v>

00:48:24.026 --> 00:48:26.346
<v Juan Martinez>because they need to log in to this website.</v>

00:48:27.546 --> 00:48:32.986
<v Juan Martinez>That way they can earn points or redeem points if we want to go to those levels.</v>

00:48:37.906 --> 00:48:55.466
<v Michael Gottlieb>I think one of the challenges is in so many ways that it already exists. I mean, I know people who gamble online with a VPN. All you need is a VPN and you can gamble illegally. And, you know, it's gray, it's suspect, but it goes on.</v>

00:48:56.106 --> 00:48:56.426
<v Juan Martinez>Yeah.</v>

00:48:56.586 --> 00:48:59.226
<v Michael Gottlieb>So, if that, if that's the fix that you need.</v>

00:49:00.666 --> 00:49:02.746
<v Michael Gottlieb>You can, you can find it.</v>

00:49:04.586 --> 00:49:07.866
<v Val Levitan>You can find it, but most people cannot set up a VPN.</v>

00:49:11.546 --> 00:49:13.466
<v Val Levitan>And, and, and we can set up VPN.</v>

00:49:16.426 --> 00:49:21.466
<v Val Levitan>And there is no, there's nothing in the load that says that we cannot set up a VPN.</v>

00:49:24.586 --> 00:49:27.226
<v Juan Martinez>Yeah, Val, what's interesting here is, I'm sorry, you could...</v>

00:49:24.746 --> 00:49:25.306
<v Michael Gottlieb>Igor.</v>

00:49:24.986 --> 00:49:31.466
<v Val Levitan>And, and, and it's great, and it's great, but I made a shitload of money in my life and great business.</v>

00:49:33.866 --> 00:49:40.146
<v Val Levitan>Same, same as Mark Mackey today, making a killing in great business.</v>

00:49:41.866 --> 00:49:42.106
<v Juan Martinez>Yeah.</v>

00:49:43.466 --> 00:49:46.906
<v Val Levitan>And I'm a little bit, I'm a little bit tired of not making money.</v>

00:49:43.626 --> 00:49:44.026
<v Michael Gottlieb>I had a...</v>

00:49:51.946 --> 00:49:57.386
<v Michael Gottlieb>I think the other challenge is the kind of cash that people would have to spend to purchase their own slot machine.</v>

00:49:58.186 --> 00:49:59.066
<v Val Levitan>Not an issue.</v>

00:49:59.666 --> 00:50:01.706
<v Michael Gottlieb>to have in their home. You give it to them for free.</v>

00:50:02.386 --> 00:50:09.546
<v Val Levitan>No, but they, you know, up to $1500 finance, people buy machines.</v>

00:50:11.146 --> 00:50:14.426
<v Val Levitan>We've tested the market with Amazon, no issues.</v>

00:50:16.266 --> 00:50:17.626
<v Michael Gottlieb>Well, I can't tell you.</v>

00:50:16.346 --> 00:50:20.186
<v Juan Martinez>So, I'm sorry, so we are talking about an at-home machine.</v>

00:50:16.666 --> 00:50:18.426
<v Val Levitan>If, if the price, if the...</v>

00:50:20.986 --> 00:50:21.866
<v Val Levitan>At home machine.</v>

00:50:22.346 --> 00:50:23.226
<v Juan Martinez>Okay, I'm sure.</v>

00:50:23.946 --> 00:50:44.586
<v Michael Gottlieb>Yeah, I had a friend, this goes way back, but he worked on, I think it was called Farmville in the early days of Zynga and Facebook. And what ended up happening was husbands or wives would get addicted to it and then they would start hiding how much money they were spending on it.</v>

00:50:45.026 --> 00:51:06.106
<v Michael Gottlieb>And then the spouse would find out and they saw a precipitous drop off of people playing it. So I think there's a risk associated with the somebody who's got a gambling problem, gambling too much, and then the other person in the house saying, get this thing.</v>

00:51:06.506 --> 00:51:08.826
<v Michael Gottlieb>Out of here.</v>

00:51:10.506 --> 00:51:15.066
<v Val Levitan>Husband takes that machine and throws it off the cliff and it's it.</v>

00:51:16.466 --> 00:51:35.986
<v Michael Gottlieb>Yeah, I mean, I think the point is, is ideally you want a sustainable business. And I guess, in all honesty, the people that are gambling with a VPN, using offshore accounts and whatever else, I'm not sure that their significant others know that they're doing it. I mean, this is kind of morbid.</v>

00:51:36.066 --> 00:51:53.866
<v Michael Gottlieb>But unfortunately, with some of the people with gambling problems that end up committing suicide, in many, many, many instances, and I've just, we've had, I've read lots of reports about this stuff. In many, many instances, the spouse had absolutely no idea that they were 40, 50, 60, $80,000 in debt.</v>

00:51:55.226 --> 00:52:12.426
<v Michael Gottlieb>they keep it from the other person. So I'm just talking from a psychological standpoint, having a slot machine in somebody's house. I mean, in a fraternity house, you know, maybe, although they tend to be more oriented towards sports gambling, but, you know,</v>

00:52:14.346 --> 00:52:19.066
<v Val Levitan>Makes sense. I agree. It's a big model stumbling block.</v>

00:52:24.066 --> 00:52:30.346
<v Juan Martinez>Yeah, it is interesting. Yeah, the guys at Hard Rock recently told me that the Hard Rock bed...</v>

00:52:31.386 --> 00:52:41.706
<v Juan Martinez>Now that they've added online play for money games, it's starting to affect the brick and mortar. They've even seen people on the casino floor.</v>

00:52:43.746 --> 00:52:46.666
<v Juan Martinez>As a machine, one on the phone side by side.</v>

00:52:55.066 --> 00:52:56.986
<v Val Levitan>Should we be ready for it?</v>

00:52:59.066 --> 00:53:09.146
<v Juan Martinez>I mean, we should be. I think we should have a longer conversation about it, but there's definitely, you know, money to be made.</v>

00:53:09.626 --> 00:53:14.986
<v Val Levitan>It will take us quite a bit of time to settle the technology on this.</v>

00:53:18.986 --> 00:53:23.706
<v Val Levitan>By settle, I mean it, I mean it needs to be flawless and it needs to work.</v>

00:53:24.426 --> 00:53:24.546
<v Juan Martinez>Yeah.</v>

00:53:30.506 --> 00:53:32.066
<v Val Levitan>Or just scrubbing a deal together.</v>

00:53:36.026 --> 00:53:55.066
<v Juan Martinez>I wouldn't say scrap, but I mean, everyone knows that online gaming is the future. You know, these younger kids, all they do is they're on their tablets, because you know, sizes keep getting smaller. You know, once this last round, the player...</v>

00:53:55.626 --> 00:54:09.386
<v Juan Martinez>dies off, you know, there isn't necessarily someone to backfill their shoes. You know, the retirees of today are going to be gone soon and there's nobody really filling their space.</v>

00:54:12.586 --> 00:54:13.866
<v Juan Martinez>You also.</v>

00:54:13.026 --> 00:54:24.026
<v Val Levitan>And funny enough, I detect that casinos are not really longer fighting St. business. Street business is just becoming more potent.</v>

00:54:26.266 --> 00:54:29.946
<v Juan Martinez>Yeah, I would say the only fight in the US right now is in Pennsylvania.</v>

00:54:33.146 --> 00:54:43.146
<v Juan Martinez>Casinos are demanding that the gray machines, the skill-based games, be taxed at the same rate they are, which would obviously wipe them out.</v>

00:54:45.466 --> 00:54:49.786
<v Juan Martinez>But it's in the news and it's in front of the legislation there now, so...</v>

00:54:50.826 --> 00:54:52.266
<v Juan Martinez>Mark Pace is.</v>

00:54:53.786 --> 00:54:54.506
<v Juan Martinez>Really worried.</v>

00:54:57.826 --> 00:55:17.466
<v Michael Gottlieb>California casino guys that I talked to, they know there's challenges, but their take on it is that as long as they can provide destination level service, which is to say a golf course, good restaurants, a concert, that people need something.</v>

00:55:17.506 --> 00:55:38.746
<v Michael Gottlieb>thing to do. And there is a school of thought that after you turn 50 years old, all of a sudden something switches and you become more open to the idea of playing slot machines. It's safe, it's air conditioned. There are a lot of people with disposable income that unfortunately lose their spouses and they need something to do.</v>

00:55:39.946 --> 00:55:58.506
<v Michael Gottlieb>These are not people that are necessarily tech savvy or care about messing with their phone, their eyesight isn't great, but they still come out to the casinos and they still make an eye out of it and they still spend money. I think the biggest challenge is just this kind of commoditization of gaming.</v>

00:55:58.786 --> 00:56:08.906
<v Michael Gottlieb>where, and we've talked about this before, Vegas was the only place you could get it, and Reno was the only place you could get it. Now it's everywhere. You know, the pizza place and the BBQ place, I...</v>

00:56:12.466 --> 00:56:27.146
<v Michael Gottlieb>who are going to as a child, took out boots and they now have slot machines everywhere in Illinois. So I would suggest that the street level locations are becoming more potent and it's kind of everywhere. But most importantly, you don't need to go to Vegas anymore.</v>

00:56:28.426 --> 00:56:47.546
<v Michael Gottlieb>And they have diminished their destination level entertainment. I read an article a while ago that talked about, you know, you go to Vegas and Treasure Island had the pirate show and, you know, there was this going on and there was that going on and there was lots of, you know, there was tigers to look at at MGM and they've cut back.</v>

00:56:47.786 --> 00:57:06.906
<v Michael Gottlieb>further and further and further. And now they just want your money as quickly as possible. So there's not nearly as many justifiable reasons to go. We're drawing really AAA acts out here in San Diego to the local casinos. And they're getting a lot of traffic there, according to my friends that, you know, run Pechanga and Viejas and whatever else.</v>

00:57:07.386 --> 00:57:16.906
<v Michael Gottlieb>But it's just gaming is everywhere now. So I could only see the places like Georgia and Nebraska and South Dakota that it will continue to spread.</v>

00:57:19.626 --> 00:57:38.426
<v Michael Gottlieb>And as you remember, Juan, it's the evolution, right? When I came to California, Barona was a tent with fans and Chinese guys screaming taigao and chain smoking unfiltered cigarettes. It was filthy, it was stinky, it was awful, and it was miserable. And I see not to</v>

00:57:23.186 --> 00:57:23.546
<v Juan Martinez>Yeah.</v>

00:57:38.506 --> 00:57:58.906
<v Michael Gottlieb>you know, condemn some of the locations that we're operating in. But I see the photos that you send of some of these places, they're not great. But as they continue to make money, the theory would be that those locations will become more attractive, they will get more machines, or they'll have more locations with more machines because they don't have the machines' limitations.</v>

00:57:59.226 --> 00:58:11.706
<v Michael Gottlieb>and it will be, you know, a place that Val would be willing to go, or you or me to actually have dinner or something like that, as opposed to looking at it and going, wow, what the hell is holding this place up? Well, this used to be a laundromat. Oh my gosh.</v>

00:58:22.106 --> 00:58:26.146
<v Val Levitan>OK, still didn't get the other direction, but what are we doing?</v>

00:58:27.226 --> 00:58:28.666
<v Val Levitan>Speaking technology right now.</v>

00:58:27.626 --> 00:58:28.106
<v Juan Martinez>Office.</v>

00:58:29.706 --> 00:58:47.226
<v Juan Martinez>It's a very huge undertaking to host games unless we're talking about somebody else hosting on our behalf. But the infrastructure to have these games, servers, whatever this country is, where this data is going to sit.</v>

00:58:48.666 --> 00:58:58.106
<v Juan Martinez>And is it ultimately, how is it going to be allowed on a state-by-state basis? If you're playing for real money, it needs to be approved at a state level.</v>

00:59:00.106 --> 00:59:03.866
<v Val Levitan>Okay, so we'll park this idea right now, at least, at least for now.</v>

00:59:06.146 --> 00:59:07.546
<v Val Levitan>Is that the consensus?</v>

00:59:09.866 --> 00:59:11.866
<v Juan Martinez>I think so. That's a huge project.</v>

00:59:12.026 --> 00:59:12.506
<v Michael Gottlieb>Mhm.</v>

00:59:13.466 --> 00:59:13.946
<v Val Levitan>Great.</v>

00:59:16.266 --> 00:59:18.186
<v Val Levitan>Toppers on the machines.</v>

00:59:22.266 --> 00:59:31.626
<v Michael Gottlieb>I think they're a great come on. I think that they're attractive to the player. I just worry about whatever, is it line of sight or whatever term you use, Juan, and location height.</v>

00:59:32.746 --> 00:59:50.946
<v Juan Martinez>Yeah, but everybody, you know, we were a bit misinformed with South Dakota and Nebraska. Definitely toppers have value Val, and we should never not offer them, but it should not be a permanent fixture in the machine. We can remove it or add it as needed, but</v>

00:59:51.546 --> 00:59:54.146
<v Juan Martinez>It's A secondary marketing screen, and...</v>

00:59:55.066 --> 01:00:01.226
<v Juan Martinez>You know, you, if you're just a few inches taller than the next guy, somebody can see your machine from 10 feet away.</v>

01:00:01.106 --> 01:00:20.106
<v Michael Gottlieb>And it's a great come on for those progressives. The theory is once those progressive values get to something that you can get excited about, there's nothing more compelling. Walk through a modern casino. It's just a world of progressive signs, really. And if we've got a nice big prominent progressive sign, and I think, you know, what Lena designed is gorgeous,</v>

01:00:20.826 --> 01:00:23.546
<v Michael Gottlieb>Um, I very much pro tower.</v>

01:00:25.466 --> 01:00:28.506
<v Val Levitan>Okay, similar question.</v>

01:00:30.426 --> 01:00:36.666
<v Val Levitan>I think I know how to design a machine wedges.</v>

01:00:40.506 --> 01:00:42.426
<v Val Levitan>With LCD screens.</v>

01:00:47.626 --> 01:00:48.426
<v Michael Gottlieb>Waste of money.</v>

01:00:50.346 --> 01:00:50.826
<v Val Levitan>Okay.</v>

01:00:51.386 --> 01:00:54.106
<v Michael Gottlieb>Huge waste of money, waste of money, waste of time.</v>

01:00:53.066 --> 01:00:53.386
<v Juan Martinez>Yeah.</v>

01:00:55.266 --> 01:00:57.346
<v Michael Gottlieb>I'll tell you exactly.</v>

01:00:56.146 --> 01:01:14.746
<v Juan Martinez>Especially in the street market, there's seldom 3 machines in a pie or circle format. There simply isn't that kind of space. You definitely lose space when you introduce a wedge. And the markets we're all in today, it's four to five to seven machines in a row. There is no</v>

01:01:15.186 --> 01:01:16.586
<v Juan Martinez>No place for a wedge.</v>

01:01:16.986 --> 01:01:19.546
<v Val Levitan>Okay, good. Let's continue.</v>

01:01:23.306 --> 01:01:24.266
<v Val Levitan>Toppers.</v>

01:01:27.706 --> 01:01:30.026
<v Val Levitan>Design them as a separate commodity.</v>

01:01:31.306 --> 01:01:35.866
<v Val Levitan>Sorry, a separate item or permanently built in.</v>

01:01:37.386 --> 01:01:38.746
<v Michael Gottlieb>Sounds like one-one separate.</v>

01:01:37.786 --> 01:01:38.586
<v Val Levitan>No option.</v>

01:01:39.386 --> 01:01:58.346
<v Juan Martinez>Yeah, the customer should have the right to, why would we lose a sail if we're 3 inches taller than we need to be, knowing that we could remove the topper and now we fit. So I'd like to, it should be seamlessly connected to the top monitor so it looks like 1 continuous screen.</v>

01:01:58.586 --> 01:02:02.826
<v Juan Martinez>But by all means, it needs to be removable, or we have potential to lose business.</v>

01:02:04.546 --> 01:02:06.386
<v Val Levitan>Like, hold, hold on one second, just one second.</v>

01:02:13.386 --> 01:02:16.586
<v Michael Gottlieb>I'm thinking, I'll be right back.</v>

01:02:17.786 --> 01:02:18.346
<v Efim Podvoiski>Okay.</v>

01:02:22.586 --> 01:02:24.346
<v Efim Podvoiski>I go grab something to drink.</v>

01:02:24.826 --> 01:02:28.826
<v Juan Martinez>Yeah, Michael, you were supposed to take your camera and post from the bathroom.</v>

01:04:48.586 --> 01:04:59.146
<v Val Levitan>Topper, there is a new technology now. I mean, I know that you guys have heard about it, but there is a next generation technology right now on...</v>

01:05:00.586 --> 01:05:05.146
<v Val Levitan>for 3D monitors that does not require glasses.</v>

01:05:06.626 --> 01:05:10.906
<v Val Levitan>A new generation is substantially better from what I've heard.</v>

01:05:11.786 --> 01:05:16.586
<v Val Levitan>Do we want to test it for toppers?</v>

01:05:26.026 --> 01:05:45.666
<v Michael Gottlieb>Boy, that's a tough one. You know, pioneers get the arrows, settlers get the land. I'm obviously knee-jerking because as Juan remembers, Spielo went *******, excuse me, with their 3D slot machines. It was going to be the future, just like the motion chair and everything else was going to be the future. And it made people sick.</v>

01:05:46.346 --> 01:05:47.946
<v Juan Martinez>Oh, it made people dizzy.</v>

01:05:48.666 --> 01:05:51.786
<v Michael Gottlieb>Yeah, it made people dizzy, made people sick, it made them uncomfortable.</v>

01:05:54.506 --> 01:06:05.066
<v Lena Zhukova>I know a lot of people who doesn't like to go when they go to the movies, they hate all this kind of like 3D, IMAX, they only go to regular movies because...</v>

01:06:01.546 --> 01:06:01.866
<v Michael Gottlieb>Yeah.</v>

01:06:04.426 --> 01:06:07.626
<v Michael Gottlieb>Yeah, my wife will not go to the 3D anything. She doesn't like it.</v>

01:06:08.666 --> 01:06:09.146
<v Michael Gottlieb>Um...</v>

01:06:08.666 --> 01:06:09.546
<v Juan Martinez>Now, with with with.</v>

01:06:08.906 --> 01:06:21.146
<v Lena Zhukova>And you need to prepare assets in a special way, so now we are using assets for toppers, we're using like logos and characters, and for three toppers you need to render in a special way.</v>

01:06:11.946 --> 01:06:12.346
<v Michael Gottlieb>Right.</v>

01:06:23.226 --> 01:06:34.506
<v Juan Martinez>Yeah, Val, I would say because we're focusing on St. that's not necessary. If we got back into HHR or Class 3 in the future, that could be interesting.</v>

01:06:36.826 --> 01:06:37.946
<v Val Levitan>Perimeter lights.</v>

01:06:40.666 --> 01:06:44.506
<v Juan Martinez>Yeah, they're now the de facto default on everyone's cabinets.</v>

01:06:45.786 --> 01:06:49.146
<v Juan Martinez>The key is to tie in the perimeter lights with game activity.</v>

01:06:50.826 --> 01:06:53.466
<v Val Levitan>Per mirror lights on V deck.</v>

01:06:59.866 --> 01:07:00.266
<v Val Levitan>Great.</v>

01:07:00.026 --> 01:07:01.786
<v Juan Martinez>At the time, it's blocked by the chair.</v>

01:07:01.466 --> 01:07:01.626
<v Efim Podvoiski>Mm.</v>

01:07:06.106 --> 01:07:15.466
<v Michael Gottlieb>And you're creating visual information to the human eye when you want them, you're distracting them from what you want them to be looking at.</v>

01:07:16.666 --> 01:07:29.866
<v Michael Gottlieb>Right? You want the console to be black because you want them to be looking at the VDEC or the buttons. If you put that other Mickey Mouse around there, it's just a distraction to the eye. And it's fatiguing. They don't know it, but it's fatiguing.</v>

01:07:35.146 --> 01:07:37.626
<v Val Levitan>perimeter lights or halo lights.</v>

01:07:39.866 --> 01:07:40.986
<v Juan Martinez>What's the difference?</v>

01:07:42.666 --> 01:07:44.826
<v Michael Gottlieb>Halo lights cast light down, correct?</v>

01:07:42.746 --> 01:07:43.626
<v Val Levitan>For a matter of late.</v>

01:07:45.706 --> 01:07:49.786
<v Val Levitan>Or around an object, doesn't matter, but...</v>

01:07:49.546 --> 01:08:01.386
<v Michael Gottlieb>Yeah, I mean, if there's some diffused lighting that casts light down or around the perimeter, I wouldn't object to that, but just something that's garish in your face where the V deck is located, I think is counterproductive.</v>

01:08:01.146 --> 01:08:09.466
<v Val Levitan>No, I'm really no I'm talking about the monitor around the monitor halo lights or the perimeter lights definitive line of lights.</v>

01:08:10.906 --> 01:08:17.106
<v Val Levitan>On A perimeter or a diffused.</v>

01:08:18.826 --> 01:08:20.746
<v Michael Gottlieb>Oh, I like the definitive line.</v>

01:08:19.706 --> 01:08:21.546
<v Val Levitan>But bad luck.</v>

01:08:21.146 --> 01:08:21.546
<v Juan Martinez>Yeah.</v>

01:08:22.026 --> 01:08:41.066
<v Michael Gottlieb>Yeah, the definitive line, you want it to be like, you know, at the carnival, if you take the, you take the hammer and you hit the thing and it hits the bell and the lights go up, you want, you want that celebratory lighting experience. I think people have come to expect it and they enjoy it.</v>

01:08:41.866 --> 01:08:42.826
<v Val Levitan>Thick or thin?</v>

01:08:46.866 --> 01:08:49.386
<v Michael Gottlieb>But we just have to be mindful of how we use it.</v>

01:08:50.666 --> 01:08:52.666
<v Val Levitan>They quite on the perimeter.</v>

01:08:53.546 --> 01:09:13.186
<v Michael Gottlieb>I mean, I'd have to see a rendering from Genadi of what you're talking about, what your definition of thick versus thin is. But, you know, when I think thin, I think little tiny LED strip. And I don't think that the amount of lumens that that generates is maybe as compelling as we want. I mean, when we want the damn thing to light up, you want it to light up.</v>

01:09:13.266 --> 01:09:19.066
<v Michael Gottlieb>The player feels good, the person in the environment looks like, oh my gosh, what? Why? You lit up like a slot machine.</v>

01:09:21.306 --> 01:09:22.506
<v Val Levitan>Two type of lights.</v>

01:09:23.386 --> 01:09:26.906
<v Val Levitan>Thin perimeter and huge.</v>

01:09:29.466 --> 01:09:32.666
<v Val Levitan>Two-inch lights on the perimeter.</v>

01:09:32.346 --> 01:09:32.986
<v Efim Podvoiski>Orange.</v>

01:09:34.746 --> 01:09:36.826
<v Juan Martinez>I, I think that, so that's overkill.</v>

01:09:34.906 --> 01:09:35.306
<v Val Levitan>Yeah.</v>

01:09:36.266 --> 01:09:40.586
<v Michael Gottlieb>That, that's overkill; that's unnecessary. It'll it won't look good.</v>

01:09:39.466 --> 01:09:44.186
<v Val Levitan>It's uh, it's your, yeah, sure, it's your new light and wonder, two-inch light.</v>

01:09:49.546 --> 01:09:54.506
<v Michael Gottlieb>Yeah, I don't like that. The one that, yeah, that's got the spiral thing in it that they have on Frankenstein.</v>

01:09:53.386 --> 01:09:55.546
<v Val Levitan>Yeah, they have, they have different shapes.</v>

01:09:55.866 --> 01:10:02.186
<v Michael Gottlieb>Yeah, I know the guy that designed that and he thinks it's ****. He's not happy with it, but they told him that's what they wanted. That's what they wanted.</v>

01:10:03.386 --> 01:10:22.346
<v Michael Gottlieb>I mean, everybody's entitled to their own opinion. I don't, I'm not impressed. I don't think it's necessary. I don't think it's elegant. I mean, I think the translation in the mind of human beings now of elegant lighting is diffused LED or directional LED, but you know something that that looks sophisticated and I...</v>

01:10:22.466 --> 01:10:29.866
<v Michael Gottlieb>I think what Light and Wonder did looks, I don't know, sloppy, kludgy. I'm not impressed. I don't know what you think, Juan.</v>

01:10:30.826 --> 01:10:49.466
<v Juan Martinez>Yeah, no, I mean, they really only feature it on their premium games, like Frankenstein and whatever, but I've never heard anybody actually say, oh, those are wonderful. I'm going to go play the game. Does it, you know, draw them in? No, probably the animation of the game and the top.</v>

01:10:49.666 --> 01:11:01.626
<v Juan Martinez>is what's really drawing them in or the branding behind the product. From being a technical person, if we do two different types of lights, it's just one more thing to fail mechanically on the cabinet.</v>

01:11:11.866 --> 01:11:17.786
<v Val Levitan>Okay, switching the subject. Let's go to discuss math. So we're making a game.</v>

01:11:18.986 --> 01:11:21.226
<v Val Levitan>and who want to try different.</v>

01:11:23.306 --> 01:11:25.066
<v Val Levitan>Math quickly.</v>

01:11:28.506 --> 01:11:29.786
<v Val Levitan>How can we do that?</v>

01:11:37.306 --> 01:11:39.626
<v Efim Podvoiski>I think compared to...</v>

01:11:40.746 --> 01:11:50.746
<v Efim Podvoiski>If the mechanics is basically the same, we are just playing with parameters mostly, or switching and changing some known elements.</v>

01:11:52.026 --> 01:12:04.026
<v Efim Podvoiski>The time that we spent actually playing and playing testing is smaller than time I will spend on creating the prototype mass.</v>

01:12:05.546 --> 01:12:18.106
<v Efim Podvoiski>So, putting aside, how can I quickly change the mass? We can put it aside for a while and slowly get more automations there.</v>

01:12:19.306 --> 01:12:26.106
<v Efim Podvoiski>I think, and to concentrate on the question, how can we quickly prototype the gameplay?</v>

01:12:27.066 --> 01:12:46.146
<v Efim Podvoiski>and mechanics. So we have something that just follows the rules that maths dictates and we put some placeholder assets and we can play the game early before without any programmers or something. And I think hundreds are working on</v>

01:12:46.586 --> 01:12:47.626
<v Efim Podvoiski>Something close yourself.</v>

01:12:49.546 --> 01:12:50.106
<v Efim Podvoiski>Honders.</v>

01:12:50.506 --> 01:12:50.986
<v Lena Zhukova>Dima.</v>

01:12:53.066 --> 01:12:53.946
<v Efim Podvoiski>Zima and Andrei.</v>

01:13:01.386 --> 01:13:20.586
<v Efim Podvoiski>But what Michael said initially is that how can we, how can him play this mass settings? It's another story. It's insistent. I don't know how to do it, but eventually if we can do it, it would be great. But for now...</v>

01:13:19.786 --> 01:13:23.946
<v Lena Zhukova>You mean, more modules, like, uh, like, set?</v>

01:13:22.666 --> 01:13:44.986
<v Efim Podvoiski>Like, yeah, so something, yeah, it's not easy. You, you, you want, you can say I want free spins, not 120 times, but one in 100 times. But to do it, I have to change. Somebody has to change the reels. Somebody has to balance the RCP, otherwise.</v>

01:13:46.266 --> 01:14:04.546
<v Efim Podvoiski>You're playing the games that play 120%, you like it, but it's not the game that you can really put on the machine. So I wouldn't now concentrate on this hard step, how do you avoid go around me, but</v>

01:14:04.746 --> 01:14:08.106
<v Efim Podvoiski>How do we go around programmers? It's another story, and we are working on this.</v>

01:14:09.306 --> 01:14:28.466
<v Michael Gottlieb>I think of just as a first step, we had a means by which of loading some meaningful number of our pre-existing math models as a foundation, as a starting point, to just say, you know, I want to do a 5 by 3 with free spins that hit 1 and 120 and some tool.</v>

01:14:28.666 --> 01:14:34.746
<v Michael Gottlieb>that would allow us to just kind of choose that. Because right now everything is...</v>

01:14:36.106 --> 01:14:56.826
<v Michael Gottlieb>You know, templates, basically math templates would be the correct way of saying it, because right now everything is roll your own. Every time we want to do something, you have to start. And I know you don't start from square zero. I know you've got where ground zero. I know you're starting from a certain place, but I'd like to collate a library of math.</v>

01:14:56.906 --> 01:15:17.306
<v Michael Gottlieb>templates. So then we want when we want to start something, we've got some concrete already poured for the foundation of the house and maybe even A-frame. And that gives us more flexibility and room to play with doing more with the math as opposed to just getting the math up and playing period.</v>

01:15:18.266 --> 01:15:33.706
<v Michael Gottlieb>Right, so for example, like with Twin Bison, now we've got double reels. If we had that as a math template, we could use that as a launching point for maybe we want to do triple reels, maybe we want to do 4 reel bundles at a certain point. You know what I mean?</v>

01:15:43.066 --> 01:16:00.746
<v Efim Podvoiski>Not sure how it can work, but I think you can push me in this direction and we will discuss it and we'll see where it's going. But I think right now the longest part is to wait for game to be up and running on Windows Build so we can play it.</v>

01:15:48.426 --> 01:15:48.746
<v Michael Gottlieb>Yeah.</v>

01:16:01.826 --> 01:16:03.066
<v Efim Podvoiski>And it takes 2 weeks.</v>

01:16:04.186 --> 01:16:05.706
<v Efim Podvoiski>And if it takes...</v>

01:16:07.546 --> 01:16:08.506
<v Michael Gottlieb>Sometimes months.</v>

01:16:08.346 --> 01:16:11.786
<v Efim Podvoiski>A half a day for me to change to to to change the mask.</v>

01:16:12.906 --> 01:16:15.786
<v Efim Podvoiski>It's a big, big step forward.</v>

01:16:17.306 --> 01:16:21.866
<v Efim Podvoiski>Okay, that means it's much better than half a day, but half a day is much better than two weeks.</v>

01:16:22.266 --> 01:16:22.666
<v Michael Gottlieb>Right.</v>

01:16:24.186 --> 01:16:24.826
<v Val Levitan>Um...</v>

01:16:26.506 --> 01:16:29.866
<v Val Levitan>Okay, I've got that recorded, so that's fine.</v>

01:16:31.146 --> 01:16:31.866
<v Val Levitan>Um...</v>

01:16:40.986 --> 01:16:44.546
<v Val Levitan>Yes. Anybody else wants to say anything else?</v>

01:16:47.466 --> 01:16:50.386
<v Michael Gottlieb>I just, you know, you're talking about a lot of different...</v>

01:16:51.466 --> 01:17:10.026
<v Michael Gottlieb>ideas which I really I love. It's exciting that you know to approach it from that standpoint. I would like any insight, Juan, that Felipe or whomever could provide into what is it what is it that we're missing because form follows function, right?</v>

01:17:10.306 --> 01:17:31.466
<v Michael Gottlieb>And what I mean by that is, we talked about countertop product at one point. Just a confirmation that a single screen, flat screen countertop product doesn't make any sense. I mean, maybe it doesn't make any sense because, you know, people don't want it, but is there something we can do because we're fast, because we're nimble, because Genadi?</v>

01:17:31.506 --> 01:17:51.626
<v Michael Gottlieb>can make things happen. Is there something we can do and offer in terms of our product offering that is unique or different than our competitors? All the way, including to, you know, maybe there are pre-existing bars and we have, like, you know, like they have in Vegas, they've got the monitors.</v>

01:17:51.746 --> 01:18:11.066
<v Michael Gottlieb>built into the bars, you know, how can we, how can we bring something that they don't have? You know, I mean, a cocktail back in the 80s when we made video games, there was this big thing about we had big video games. And they said, oh, that's too big. And then we went to something called Cabaret.</v>

01:17:53.546 --> 01:17:54.186
<v Juan Martinez>Right, right.</v>

01:18:11.626 --> 01:18:30.346
<v Michael Gottlieb>which was a smaller cabinet video game. I know Val remembers all this. And then Bally had cocktail video games and they were flat and one person would sit on one side, the other person would sit on the other side and you could play Space Invaders and Pac-Man and whatever else. And those</v>

01:18:30.586 --> 01:18:51.506
<v Michael Gottlieb>you would have like a trendy cool nightclub or bar that would never have them as Pac-Man, but they'd have a bunch of these of these cocktail tables, you know, in there. So, and I don't believe in all the ******** that's going on with like, oh, you know, we're going to get them where we either these, I think we had at Light and Wonder it was called the Prism.</v>

01:18:51.706 --> 01:19:12.906
<v Michael Gottlieb>table, which was some garbage thing that they did. I'm not talking about that. I'm talking about taking a slot machine, its form factor, reimagining it in a way where you could have a location that you could say, you know what, you've got this tall table. You can take this table out. You can put a JVL</v>

01:18:53.506 --> 01:18:53.706
<v Juan Martinez>Yeah.</v>

01:18:54.986 --> 01:18:55.306
<v Juan Martinez>Yeah.</v>

01:19:13.066 --> 01:19:29.626
<v Michael Gottlieb>console in and people can play while they're hanging out with their friends and talking or whatever the case may be or they can play, you know, just one one person. I don't know. I don't know. I'm just I'm just wondering what can we reimagine.</v>

01:19:29.546 --> 01:19:48.346
<v Val Levitan>It's actually a very interesting idea where you're pushing this, because in those productive locations that in Georgia, for example, that has a maximum of 10 machines, what is the definition of a machine? Can we have a two-sided cocktail?</v>

01:19:48.426 --> 01:19:56.666
<v Val Levitan>Table with two screens that seats two players, and add, for example, a tournament.</v>

01:19:58.506 --> 01:19:59.306
<v Val Levitan>Element.</v>

01:20:00.506 --> 01:20:07.066
<v Val Levitan>to it, will it be considered as one machine or two machines if it's in the same body?</v>

01:20:07.546 --> 01:20:07.866
<v Juan Martinez>Right.</v>

01:20:08.346 --> 01:20:11.706
<v Val Levitan>and adding a tournament between them.</v>

01:20:12.866 --> 01:20:15.146
<v Val Levitan>where they could also side that.</v>

01:20:16.346 --> 01:20:17.226
<v Val Levitan>with each other.</v>

01:20:18.986 --> 01:20:24.506
<v Val Levitan>Uh, that's a clever idea. I actually think that it's it has legs.</v>

01:20:23.386 --> 01:20:23.626
<v Juan Martinez>Yeah.</v>

01:20:25.946 --> 01:20:32.826
<v Val Levitan>And we can easily try it with two small monitors, curved, two small curved monitors.</v>

01:20:34.306 --> 01:20:35.226
<v Val Levitan>Uh, back-to-back.</v>

01:20:36.986 --> 01:20:40.666
<v Val Levitan>And the footprint would not be that significantly huge.</v>

01:20:44.346 --> 01:20:45.386
<v Val Levitan>So it's it's something.</v>

01:20:44.426 --> 01:20:47.226
<v Efim Podvoiski>What will be internally?</v>

01:20:46.266 --> 01:20:47.546
<v Val Levitan>That's an interesting idea.</v>

01:20:48.266 --> 01:20:51.786
<v Efim Podvoiski>You'll be two motherboards inside or one?</v>

01:20:53.146 --> 01:21:03.546
<v Val Levitan>And part that for a second, Efim, I mean, you're knocking on the door of some other question that I have. The new Nova platform.</v>

01:21:05.466 --> 01:21:16.106
<v Val Levitan>Do we want it to spin multiple slot machines at the same time on the same screen? Which also brings us to Efim question partially.</v>

01:21:16.786 --> 01:21:17.226
<v Michael Gottlieb>Yes.</v>

01:21:19.466 --> 01:21:21.546
<v Juan Martinez>Can you clarify what you mean?</v>

01:21:20.106 --> 01:21:31.066
<v Efim Podvoiski>Independent, independent machines or multi, multi, multi-field, multi-set of reels games, because it's a little bit different things.</v>

01:21:31.546 --> 01:21:32.186
<v Val Levitan>I don't know.</v>

01:21:33.266 --> 01:21:34.306
<v Efim Podvoiski>It's a different.</v>

01:21:33.786 --> 01:21:34.346
<v Juan Martinez>But, but...</v>

01:21:33.786 --> 01:21:53.066
<v Michael Gottlieb>I want enough horsepower to be able to spend 4 real bundles simultaneously within the same game. Aristocrat had something called Wonder Four that did pretty well for them. So I think if we want to, either that or, Juan, you remember, more chilies.</v>

01:21:53.146 --> 01:22:00.746
<v Michael Gottlieb>and more hearts, you go into free spins, one real bundle, two real bundles, three real bundles, 4 real bundles. We need to be able to support 4 real bundles.</v>

01:21:53.626 --> 01:21:54.106
<v Juan Martinez>Yeah.</v>

01:21:57.626 --> 01:21:57.906
<v Juan Martinez>Yeah.</v>

01:22:01.546 --> 01:22:08.346
<v Val Levitan>Great, so let's build on it as well as the two side by side, sorry, back-to-back.</v>

01:22:10.186 --> 01:22:13.786
<v Val Levitan>Can we verbalize what is it that we want from the platform?</v>

01:22:14.826 --> 01:22:15.226
<v Juan Martinez>Sure.</v>

01:22:14.986 --> 01:22:24.186
<v Val Levitan>because we're all confused about multiple games at the same time. And Efim asked a question which I cannot even elaborate to the engineers.</v>

01:22:22.826 --> 01:22:34.026
<v Michael Gottlieb>Well, no, no. OK, so let me be clear. Let me be clear. I'm not talking about multiple games at the same time. I'm talking about one game that would support 4 real bundles simultaneously.</v>

01:22:36.586 --> 01:22:47.386
<v Val Levitan>So when you say one game, let's say your bet is 25 cents and you have four games, you divide that 25 cents into four.</v>

01:22:47.786 --> 01:22:59.146
<v Juan Martinez>The other way, 25 cents for each game enabled. You can enable or disable. If you want to play one, you play one. If you want to play 4, it costs you an extra 75 cents.</v>

01:22:57.146 --> 01:22:57.706
<v Val Levitan>But it's.</v>

01:22:59.306 --> 01:23:02.026
<v Val Levitan>The same game or other games?</v>

01:23:02.466 --> 01:23:05.146
<v Juan Martinez>Other games, or the same game, like...</v>

01:23:04.346 --> 01:23:05.306
<v Michael Gottlieb>Or the same game.</v>

01:23:04.826 --> 01:23:15.946
<v Val Levitan>So if you have, let's say, 12 games on the machine, you could say this one, this one, this one, not this one, but this one, four of them.</v>

01:23:16.826 --> 01:23:25.226
<v Val Levitan>put them on the screen, go zoom on the screen, and you say, my bet is 25 cents times 4, spin.</v>

01:23:25.866 --> 01:23:27.946
<v Juan Martinez>Yes, that's exactly.</v>

01:23:26.746 --> 01:23:27.626
<v Val Levitan>Is this what you want?</v>

01:23:26.826 --> 01:23:39.546
<v Michael Gottlieb>That's the, well, that is the extreme version of that because you'd have to have all the games have to be 5 by fours, the math has to be accounted for with all the games. So that's more complicated, but yes.</v>

01:23:31.386 --> 01:23:32.666
<v Efim Podvoiski>Yeah, it's a stadium.</v>

01:23:38.986 --> 01:23:50.186
<v Val Levitan>Not necessarily, because we already discussed this issue and the way the engineers look at it is they will use the same LGS, but</v>

01:23:51.346 --> 01:24:00.186
<v Val Levitan>consecutively, not in parallel. So within a second or millisecond, they start next game, next game, next game.</v>

01:24:03.826 --> 01:24:13.946
<v Juan Martinez>Yeah, well, Michael's just saying is we need to be mindful. In a package of 12, we can't offer them the ability to enable all 12. We have to pick a group of games.</v>

01:24:11.066 --> 01:24:11.706
<v Efim Podvoiski>It's.</v>

01:24:12.586 --> 01:24:13.226
<v Val Levitan>Mhm.</v>

01:24:14.106 --> 01:24:15.386
<v Val Levitan>No, no, I understand.</v>

01:24:14.346 --> 01:24:18.026
<v Efim Podvoiski>Now, if you select four different games, OK, you have...</v>

01:24:17.066 --> 01:24:36.306
<v Val Levitan>I understand. I just said 12 games. Let's call it six games or eight games, whatever we allow in the package. So let's say the package is on the screen, multi-game screen, and the player says, I want to play four games simultaneously out of this package, selects 4 out of a package.</v>

01:24:23.466 --> 01:24:23.746
<v Juan Martinez>Yeah.</v>

01:24:36.586 --> 01:24:48.186
<v Val Levitan>and says these four I want to play simultaneously. From an LGS perspective, LGS can start spinning this game a few milliseconds apart.</v>

01:24:49.746 --> 01:24:55.346
<v Efim Podvoiski>Yeah, but how do we present? We we have a screen, OK, to present for for set of zero for.</v>

01:24:53.386 --> 01:24:58.426
<v Val Levitan>We split the screen, we we split, we split the screen into four.</v>

01:24:59.626 --> 01:25:05.786
<v Val Levitan>And we have a start button in the middle, and somebody says start.</v>

01:25:04.906 --> 01:25:05.306
<v Efim Podvoiski>None.</v>

01:25:07.226 --> 01:25:21.866
<v Val Levitan>and four games play simultaneously. The question arises is, if each game has their individual bonus games and free play games, how does it end? How do you control it?</v>

01:25:23.306 --> 01:25:36.746
<v Val Levitan>So to me, it's not an issue. One game ends, so it sits there, the other game continues, and you play in that quadrant with that game, and you move on.</v>

01:25:38.506 --> 01:25:51.946
<v Efim Podvoiski>But my question is, you only present a part of the game, you only can show reels in this case, or you have very small, very, very small screens for each game, very small screen.</v>

01:25:51.546 --> 01:25:54.186
<v Juan Martinez>I, I, I just posted a video.</v>

01:25:53.026 --> 01:25:55.626
<v Efim Podvoiski>You don't have the play table, you don't have the bonus.</v>

01:25:54.826 --> 01:25:58.346
<v Michael Gottlieb>And I just posted a screenshot. I just posted a screenshot.</v>

01:25:58.546 --> 01:26:05.386
<v Juan Martinez>And there's a good YouTube video, you could see how they're using the single screen to show all four games.</v>

01:26:05.706 --> 01:26:08.586
<v Efim Podvoiski>Yeah, is it for games or is it?</v>

01:26:09.466 --> 01:26:10.666
<v Juan Martinez>It's 4 games.</v>

01:26:10.466 --> 01:26:11.306
<v Michael Gottlieb>Four different games.</v>

01:26:10.506 --> 01:26:14.266
<v Efim Podvoiski>It's for games, it's for games. I see, I see. Wow.</v>

01:26:13.626 --> 01:26:16.666
<v Juan Martinez>And they could all be the same, or they could all be different.</v>

01:26:15.706 --> 01:26:16.346
<v Efim Podvoiski>Val.</v>

01:26:16.986 --> 01:26:17.386
<v Michael Gottlieb>Right.</v>

01:26:17.226 --> 01:26:17.546
<v Efim Podvoiski>Val.</v>

01:26:18.826 --> 01:26:20.466
<v Juan Martinez>You see, there's a select.</v>

01:26:19.146 --> 01:26:24.666
<v Efim Podvoiski>Okay, interesting, interesting, but it's a big deal for...</v>

01:26:24.106 --> 01:26:45.466
<v Michael Gottlieb>Yes, it is a big deal. And I'm not saying that we would do it tomorrow. We're talking about capacity and capability, having this ability. Now, okay, but so, okay, yes, that's a big deal Efim to do this. But now, picture if you will, as Rod Sterling from the Twilight Zone would say, imagine we do Twin Bison Quad. And what happens in Twin Bison Quad is you start</v>

01:26:25.546 --> 01:26:27.146
<v Efim Podvoiski>For, for design, for design.</v>

01:26:45.786 --> 01:26:58.666
<v Michael Gottlieb>with a single real bundle in free spins, and then a symbol hits, and then you have two real bundles, and then another symbol hits, and you have three real bundles, and then another symbol hits, and you can have up to four real bundles running simultaneously.</v>

01:26:58.666 --> 01:27:03.226
<v Efim Podvoiski>Yeah, sure, sure, that's something I clearly understand, yeah.</v>

01:26:59.946 --> 01:27:01.546
<v Michael Gottlieb>Okay, well that's something we that.</v>

01:27:03.146 --> 01:27:08.986
<v Michael Gottlieb>We can do that. That's something we can do. But whether you're still running for real bundles.</v>

01:27:12.346 --> 01:27:13.546
<v Michael Gottlieb>It's just that this, this...</v>

01:27:12.506 --> 01:27:31.066
<v Efim Podvoiski>For real balance, for real balance, for different games, for me, it's different, but, and at some point, from my perspective, for different games is nothing, because from the mass perspective, they're just running, they're just scoring mass server four times. I don't.</v>

01:27:18.106 --> 01:27:20.506
<v Michael Gottlieb>Yes, exactly. It is the most extreme.</v>

01:27:31.146 --> 01:27:37.706
<v Efim Podvoiski>OK, but, but the engineers more care care and Lena care a lot.</v>

01:27:32.186 --> 01:27:35.706
<v Michael Gottlieb>You don't care, but the engineers might, because they have to be able to run.</v>

01:27:38.026 --> 01:27:40.266
<v Michael Gottlieb>Ding, ding, ding, ding, ding, you got it, okay.</v>

01:27:43.866 --> 01:27:45.546
<v Val Levitan>So what's the verdict on this?</v>

01:27:46.746 --> 01:27:47.066
<v Efim Podvoiski>Thin.</v>

01:27:46.906 --> 01:28:01.306
<v Juan Martinez>Oh yeah, that game is extremely successful for Aristocrat, and especially that, you know, they hand selected the games to put in there, one of them being Buffalo, the other being Hello Kitty. I mean, there's the game does very well.</v>

01:28:02.506 --> 01:28:06.826
<v Val Levitan>Okay, so we definitely want to move in simultaneous game play.</v>

01:28:02.746 --> 01:28:03.306
<v Juan Martinez>And.</v>

01:28:10.226 --> 01:28:14.826
<v Michael Gottlieb>Yes, the system should support it. There'd be no reason to handcuff ourselves and not.</v>

01:28:16.106 --> 01:28:16.746
<v Val Levitan>Okay.</v>

01:28:21.946 --> 01:28:39.746
<v Juan Martinez>And Val, what you said earlier makes sense to having one cabinet with one serial number and two player interfaces that could be sold as one machine, yet the operator gets an extra game. There's definitely a...</v>

01:28:40.826 --> 01:28:43.306
<v Juan Martinez>Value to that from the operator perspective.</v>

01:28:43.706 --> 01:29:04.146
<v Val Levitan>Okay, so from a fit form design standpoint of view, we're going for vertical landscape, 2 curved monitors, two panels opposite to each other, back-to-back, one CPU board, running two games with a</v>

01:29:04.746 --> 01:29:06.986
<v Val Levitan>Bet between the two of them.</v>

01:29:08.586 --> 01:29:09.786
<v Val Levitan>Like a tournament bet?</v>

01:29:09.946 --> 01:29:12.586
<v Juan Martinez>Yeah, some sort of shared experience, yes.</v>

01:29:12.666 --> 01:29:14.906
<v Efim Podvoiski>But separate, separate accounts, right?</v>

01:29:17.786 --> 01:29:30.106
<v Juan Martinez>Oh, yeah, yeah, yeah. Oh, no, no, no. From the regular regulator perspective, we just pitched it as one machine with one serial number. So everything has to be reported under one serial.</v>

01:29:19.466 --> 01:29:20.106
<v Efim Podvoiski>So.</v>

01:29:26.826 --> 01:29:27.226
<v Efim Podvoiski>Yeah.</v>

01:29:30.586 --> 01:29:34.186
<v Efim Podvoiski>Uh, players, players have different separate balances.</v>

01:29:35.226 --> 01:29:35.866
<v Juan Martinez>Correct.</v>

01:29:36.426 --> 01:29:38.106
<v Michael Gottlieb>And 2 different bill validators.</v>

01:29:36.506 --> 01:29:42.986
<v Efim Podvoiski>So, it's it's yet another mode. It's not the same as Ryan for games for the same players.</v>

01:29:36.946 --> 01:29:37.706
<v Juan Martinez>Yeah, they're.</v>

01:29:44.666 --> 01:29:50.666
<v Efim Podvoiski>It's not just adding additional, but it's a new a new thing.</v>

01:29:46.586 --> 01:29:49.106
<v Juan Martinez>Yeah, yeah, yeah, this is different from the wonderful.</v>

01:29:53.386 --> 01:29:55.226
<v Efim Podvoiski>And, well, supporting too.</v>

01:29:54.746 --> 01:30:04.026
<v Michael Gottlieb>I guess, so the question is, the question is, Juan, if you took two JVL slot machines and you were able to fuse them together,</v>

01:30:05.106 --> 01:30:13.226
<v Michael Gottlieb>Could you sell it and basically make it one cabinet with two slot machines? Can you sell that as a single cabinet?</v>

01:30:13.266 --> 01:30:28.586
<v Juan Martinez>A 100%. I've done it 1000 times along with every major operator. If you guys have seen an electronic roulette table like inner blocks, roulette or craps or whatever, the same premise that is treated as one machine.</v>

01:30:30.826 --> 01:30:33.786
<v Val Levitan>Bravo, that's the killer application.</v>

01:30:36.026 --> 01:30:37.066
<v Val Levitan>As soon as possible.</v>

01:30:38.506 --> 01:30:45.866
<v Val Levitan>Okay, I think we have enough ideas. I'm going to stop the recording with your permission. Yes.</v>

01:30:46.266 --> 01:30:46.546
<v Juan Martinez>Yeah.</v>

