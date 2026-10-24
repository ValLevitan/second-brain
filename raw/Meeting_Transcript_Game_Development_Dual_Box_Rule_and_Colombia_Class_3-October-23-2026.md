# Raw Transcript — Game_Development
**Date:** October 23, 2026, 2:00 PM – 2:57 PM Eastern
**Summary note:** [[Meeting_Notes_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026]]
---
WEBVTT

00:00:07.356 --> 00:00:11.116
<v Efim Podvoiski>Yeah, they have an ability to do it differently, yes.</v>

00:00:12.436 --> 00:00:15.196
<v Michael Gottlieb>OK, OK. Hello, Val.</v>

00:00:15.836 --> 00:00:18.876
<v Val Levitan>Hello everyone, good to see you. How is everyone doing?</v>

00:00:17.716 --> 00:00:18.156
<v Lena Zhukova>Seven.</v>

00:00:20.756 --> 00:00:21.756
<v Efim Podvoiski>Good, good, thank you.</v>

00:00:22.156 --> 00:00:24.556
[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

00:00:25.036 --> 00:00:25.516
<v Lena Zhukova>Yeah.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

00:00:39.476 --> 00:00:43.436
<v Val Levitan>Glad to hear. Okay guys, what do we have?</v>

00:00:44.396 --> 00:01:07.036
<v Michael Gottlieb>Well, what I would like to start with is we have the Nebraska build up and playing, and Efim and I have been going back and forth, and there is a meaningful change we want to make in terms of how the skill, the dual box skill behaves. So the first question I have for you, Val, is</v>

00:01:07.996 --> 00:01:11.756
<v Michael Gottlieb>Roughly how many machines do we have deployed in Nebraska?</v>

00:01:12.476 --> 00:01:13.036
<v Val Levitan>Ten.</v>

00:01:13.916 --> 00:01:21.916
<v Michael Gottlieb>Okay, so that's not a huge number. So if we change the mechanic and the behavior, it's not going to be terribly consequential.</v>

00:01:15.276 --> 00:01:15.476
<v Val Levitan>Yeah.</v>

00:01:23.036 --> 00:01:23.836
<v Val Levitan>Not a factor.</v>

00:01:24.156 --> 00:01:29.756
<v Michael Gottlieb>Okay, well I will show all of you. Let's see here.</v>

00:01:31.276 --> 00:01:32.076
<v Michael Gottlieb>That.</v>

00:01:33.676 --> 00:01:39.436
<v Michael Gottlieb>And then that, so currently the way it works.</v>

00:01:41.196 --> 00:01:43.996
<v Michael Gottlieb>And this is the old build when we had the golden husk.</v>

00:01:46.196 --> 00:01:47.676
<v Michael Gottlieb>You go into the Bonus.</v>

00:01:50.796 --> 00:01:52.156
<v Michael Gottlieb>You pick the Coin.</v>

00:01:55.836 --> 00:01:59.436
<v Michael Gottlieb>Iraq, and then we don't do...</v>

00:02:00.636 --> 00:02:04.076
<v Michael Gottlieb>the skill part until now.</v>

00:02:05.676 --> 00:02:20.716
<v Michael Gottlieb>And what Efim and I want to do, because it makes perfect sense, is we're going to move the skill part to the outcome of the spin. That's how it behaves for line wins. We'll see if we can get a line win here.</v>

00:02:25.756 --> 00:02:28.716
<v Michael Gottlieb>There we go. So on a typical line when...</v>

00:02:32.636 --> 00:02:51.676
<v Michael Gottlieb>And I want to move the racking until after the dual box selection. So now we've got the dual box selection. Now, Lena, what we'll need to do though is in the instance of the match 3 Progressive being triggered, this message will need to say to access Bonus, because technically you haven't...</v>

00:02:45.756 --> 00:02:46.236
<v Lena Zhukova>Mhm.</v>

00:02:49.436 --> 00:02:49.836
<v Lena Zhukova>Uh-huh.</v>

00:02:51.716 --> 00:03:07.836
<v Michael Gottlieb>one, you know, we're saying to access win. In this instance, we have a win, but in the case of triggering the match 3 Progressive, you're choosing to access the Bonus. And then like I said, Lena, we don't want to rack on the outcome of the spin. We only want to rack here.</v>

00:03:10.276 --> 00:03:17.356
<v Efim Podvoiski>And not just much 3 bonus, right, but any kind of bonus, but free Spins or bonus in fire eyes.</v>

00:03:10.396 --> 00:03:10.956
<v Lena Zhukova>Mhm.</v>

00:03:16.316 --> 00:03:20.076
<v Michael Gottlieb>Well, but there's, but some games have entry wins for free spins though.</v>

00:03:21.516 --> 00:03:21.996
<v Michael Gottlieb>Right.</v>

00:03:21.596 --> 00:03:25.836
<v Efim Podvoiski>Yeah, yeah, but I think more consistent with me.</v>

00:03:24.876 --> 00:03:43.196
<v Michael Gottlieb>Yeah, you're right. You're right. You're right. Let's have, okay, you're right. We have to, we have to set some guidelines here. So the rule is on a regular line win, don't rack, dual box comes up, pick a choice, rack. And then in the instance of the match three Progressive,</v>

00:03:43.676 --> 00:04:01.356
<v Michael Gottlieb>or free spins, the text should read to access, do we want, should it say to access free spins? You know, or just bonus, to access bonus. Okay, I'm fine with that. Yeah, to access bonus. Yeah, sure, why not? To access bonus.</v>

00:03:53.196 --> 00:03:53.996
<v Efim Podvoiski>A Bonus.</v>

00:04:00.316 --> 00:04:07.836
<v Lena Zhukova>Igor, Igor asked me if it's possible to write the requirements for the behavior of the box, yeah.</v>

00:04:05.596 --> 00:04:06.396
<v Efim Podvoiski>Yeah, sure.</v>

00:04:07.036 --> 00:04:08.476
<v Michael Gottlieb>Yeah, yes.</v>

00:04:08.076 --> 00:04:10.556
<v Efim Podvoiski>We just want to want to decide first.</v>

00:04:10.796 --> 00:04:11.116
<v Michael Gottlieb>Right.</v>

00:04:10.876 --> 00:04:11.796
<v Lena Zhukova>Yeah, yeah, yeah.</v>

00:04:15.036 --> 00:04:22.876
<v Michael Gottlieb>It's a theme just identified what it was. It's A byproduct of, if you remember, we had the skill meter.</v>

00:04:18.396 --> 00:04:19.036
<v Lena Zhukova>Ssn.</v>

00:04:23.516 --> 00:04:23.676
<v Lena Zhukova>Uh-huh.</v>

00:04:23.996 --> 00:04:43.596
<v Michael Gottlieb>So that changed everything, right? Because it was fractional, percentage fractional win, and that kind of goofed everything up. And then we went to the dual box. We now have the freedom to do it on the front end. And this basically is how we're going to be doing it for Class A as well when we move forward with the Class A stuff.</v>

00:04:43.996 --> 00:04:46.876
<v Michael Gottlieb>So good. Okay, so we got that taken care of.</v>

00:04:49.196 --> 00:04:53.036
<v Michael Gottlieb>Lena, do you want to show Val Aaron's pub?</v>

00:04:53.916 --> 00:04:54.396
<v Lena Zhukova>Sure.</v>

00:05:30.756 --> 00:05:31.836
<v Efim Podvoiski>Two different girls.</v>

00:05:35.436 --> 00:05:36.716
<v Michael Gottlieb>Yes, two different girls.</v>

00:05:38.396 --> 00:05:40.316
<v Val Levitan>Why, why there are two different girls?</v>

00:05:41.356 --> 00:05:42.476
<v Michael Gottlieb>Two different symbols.</v>

00:05:43.836 --> 00:05:46.636
<v Val Levitan>Oh, I see. Are they almost equal or?</v>

00:05:48.076 --> 00:05:52.876
<v Michael Gottlieb>No, she's worth more, and she triggers the bonus, the redhead.</v>

00:05:56.996 --> 00:05:58.716
<v Michael Gottlieb>I just didn't want to put a guy in there.</v>

00:06:00.396 --> 00:06:02.236
<v Michael Gottlieb>I just didn't think.</v>

00:06:15.356 --> 00:06:18.556
<v Michael Gottlieb>So this has got the simplified Paytable across the top.</v>

00:06:21.676 --> 00:06:23.916
<v Michael Gottlieb>Nice big prominent image of the redhead.</v>

00:06:25.276 --> 00:06:25.996
<v Michael Gottlieb>With the pint.</v>

00:06:27.356 --> 00:06:30.636
<v Michael Gottlieb>Technically, it should be Guinness, but Guinness is too dark.</v>

00:06:31.556 --> 00:06:32.236
<v Michael Gottlieb>Doesn't look good.</v>

00:06:31.676 --> 00:06:36.476
<v Lena Zhukova>Yeah, we we started with uh Guinness and it doesn't look right, yeah, so...</v>

00:06:35.756 --> 00:06:39.436
<v Michael Gottlieb>Yeah, Guinness is appropriate is what is correct, but it doesn't look good.</v>

00:06:39.676 --> 00:06:45.116
<v Lena Zhukova>Yeah, golden, yeah, golden color is much better, especially for for the symbol, which is special.</v>

00:06:45.516 --> 00:06:46.876
<v Michael Gottlieb>Right, and it pops.</v>

00:06:55.276 --> 00:06:57.276
<v Val Levitan>May I cast my opinion?</v>

00:06:57.556 --> 00:06:58.436
<v Michael Gottlieb>Please, of course.</v>

00:06:57.916 --> 00:06:58.316
<v Lena Zhukova>Yeah.</v>

00:07:02.236 --> 00:07:08.556
<v Val Levitan>I would love to suggest for the red hair girl.</v>

00:07:09.436 --> 00:07:10.876
<v Val Levitan>Who is your dominant?</v>

00:07:12.636 --> 00:07:15.036
<v Val Levitan>First of all, she is beautiful, and my compliments of love.</v>

00:07:18.236 --> 00:07:27.756
<v Val Levitan>But the blonde girl is serving the beer. I think the red girl should not be here.</v>

00:07:28.836 --> 00:07:30.076
<v Val Levitan>holding a deer.</v>

00:07:31.276 --> 00:07:39.836
<v Val Levitan>I think it's a dominant figure. It's almost like she needs to have her arms crossed around her chest.</v>

00:07:41.036 --> 00:07:44.316
<v Michael Gottlieb>That would cover up, that would cover up her chest.</v>

00:07:45.116 --> 00:07:50.796
<v Val Levitan>Well, no, because she can't, no, because she crosses the arms under her chest.</v>

00:07:50.716 --> 00:07:51.676
<v Michael Gottlieb>At the waist.</v>

00:07:52.316 --> 00:07:55.436
<v Val Levitan>Well, not at the waist, but you know, under the cleavage.</v>

00:07:56.396 --> 00:07:57.356
<v Michael Gottlieb>Yeah.</v>

00:07:58.956 --> 00:08:01.356
<v Val Levitan>And I think it promotes her cleavage even more.</v>

00:08:04.716 --> 00:08:09.436
<v Val Levitan>All I'm saying, all I'm saying here, all I'm saying is that...</v>

00:08:10.556 --> 00:08:12.756
<v Val Levitan>The red hat, the the red hat.</v>

00:08:14.956 --> 00:08:17.356
<v Val Levitan>needs to be dominant according to your...</v>

00:08:19.836 --> 00:08:20.396
<v Val Levitan>Ohh.</v>

00:08:20.076 --> 00:08:20.796
<v Michael Gottlieb>Hierarchy.</v>

00:08:21.916 --> 00:08:22.396
<v Val Levitan>Right.</v>

00:08:23.596 --> 00:08:35.356
<v Val Levitan>And I think that it's not instantly viewed like that. And that's, I mean, it wasn't, it wasn't clear to me, but now it's clear to me.</v>

00:08:36.796 --> 00:08:42.956
<v Val Levitan>So it takes me a little bit of time to look at the dominance hierarchy. I think that...</v>

00:08:45.356 --> 00:08:54.156
<v Val Levitan>I would recommend to create a little further dominance. And I think beer is too repetitive within two girls.</v>

00:08:55.276 --> 00:09:04.396
<v Val Levitan>Those are not significant comments if you don't want to take them. I'm also OK with that, but I think that my suggestions will improve the game, but...</v>

00:09:05.276 --> 00:09:07.356
<v Val Levitan>Either or the, I think the game is beautiful.</v>

00:09:09.956 --> 00:09:30.316
<v Michael Gottlieb>Thank you. Yeah, Lena yet again has done a really nice job. I mean, I see it as an invitation to have a pint. I want it to be inviting as opposed to having too much attitude. I didn't want it to be kind of confrontational.</v>

00:09:30.996 --> 00:09:32.436
<v Michael Gottlieb>Um, it's her pub.</v>

00:09:33.036 --> 00:09:40.556
<v Lena Zhukova>Yeah, even for transition, yeah, we wanted a beer coming from the glass, yeah, so it's going to be like a...</v>

00:09:36.236 --> 00:09:38.076
<v Michael Gottlieb>The beer comes from the Glass.</v>

00:09:41.356 --> 00:09:41.916
<v Val Levitan>Okay.</v>

00:09:45.916 --> 00:09:47.676
<v Michael Gottlieb>And then you can move to Free Spins.</v>

00:09:57.676 --> 00:10:08.276
<v Michael Gottlieb>So the thing that Lena did, I don't know if you notice it, but the Topper and the second screen integrate to basically create the facade of the pub.</v>

00:10:09.356 --> 00:10:09.916
<v Val Levitan>Yes.</v>

00:10:09.596 --> 00:10:27.756
<v Michael Gottlieb>Yes, it's a bit, it's a bit, there's a touch of fantasy in it. Like if I'm in Ireland, it's not exactly going to look like that. It looks more like a marquee type treatment, but the actual top of a pub is not visually compelling and overwhelming.</v>

00:10:28.156 --> 00:10:33.356
<v Michael Gottlieb>But, but this in this within the context of the style, I think this turned out really cool.</v>

00:10:33.996 --> 00:10:38.796
<v Lena Zhukova>Yeah, and even without Topper, it still it will still look good.</v>

00:10:34.156 --> 00:10:34.476
<v Val Levitan>Yeah.</v>

00:10:37.916 --> 00:10:38.316
<v Michael Gottlieb>Ssn.</v>

00:10:39.436 --> 00:10:41.996
<v Val Levitan>Is this a dual screen or a vertical?</v>

00:10:41.996 --> 00:10:43.196
<v Lena Zhukova>Do all, do all.</v>

00:10:42.716 --> 00:10:43.356
<v Michael Gottlieb>Full screen.</v>

00:10:44.396 --> 00:10:49.356
<v Val Levitan>Yeah, I really like, because it's dual screen, I like the three segments of the front screen.</v>

00:10:50.796 --> 00:10:57.956
<v Michael Gottlieb>Yeah, it turned out really nice. So we're bringing this one to Nebraska and then it will...</v>

00:10:57.276 --> 00:11:08.796
<v Val Levitan>This is a clever execution. I would love to adopt it for other games. That's a clever execution of the use of three screens.</v>

00:11:10.796 --> 00:11:14.876
<v Michael Gottlieb>Okay, I'll make a note of it. There could be other scenarios where we could do something with it.</v>

00:11:15.116 --> 00:11:35.276
<v Lena Zhukova>Yeah, not all seems all like suitable for this, yeah, sometimes, yeah, like for Wildfire Ranch, you wanna see the Ranch and the girl and Sky already on the second screen, because otherwise, without Topper, you will not like present the scene properly, so in this case, you cannot just show Sky on the...</v>

00:11:32.476 --> 00:11:32.876
<v Michael Gottlieb>Right.</v>

00:11:35.516 --> 00:11:40.796
<v Lena Zhukova>Topper right, so even, but for some, but for some, for some seem it works very well.</v>

00:11:37.676 --> 00:11:38.076
<v Michael Gottlieb>Yeah.</v>

00:11:44.236 --> 00:11:50.156
<v Michael Gottlieb>Lena, can you bring up Wildfire Ranch? Because I think he saw the early stuff, but I don't think he saw kind of where we're at now.</v>

00:11:48.516 --> 00:11:49.036
<v Lena Zhukova>Mmh.</v>

00:12:08.636 --> 00:12:13.036
<v Efim Podvoiski>David, you said we are bringing this to Nebraska or you meant South Dakota?</v>

00:12:15.756 --> 00:12:21.836
<v Lena Zhukova>I think Michael meant like next Nebraska release, not this one.</v>

00:12:21.436 --> 00:12:21.836
<v Michael Gottlieb>Right.</v>

00:12:22.476 --> 00:12:23.836
<v Efim Podvoiski>Next, next week.</v>

00:12:23.596 --> 00:12:23.996
<v Michael Gottlieb>Right.</v>

00:12:32.436 --> 00:12:33.276
<v Michael Gottlieb>There we go.</v>

00:12:43.436 --> 00:12:46.636
<v Lena Zhukova>And, for the presentation, such a long question.</v>

00:12:46.716 --> 00:12:48.876
<v Michael Gottlieb>Yeah, and this is what we're doing with Free Spins.</v>

00:12:52.676 --> 00:12:54.796
<v Michael Gottlieb>Can you go down just a such so we can see the Topper?</v>

00:12:53.236 --> 00:12:53.596
<v Lena Zhukova>Yeah.</v>

00:12:55.596 --> 00:13:01.396
<v Lena Zhukova>Yeah, actually, that's not, yeah, this one here.</v>

00:12:59.116 --> 00:13:00.316
<v Michael Gottlieb>Oh, that's not the average right.</v>

00:12:59.436 --> 00:13:06.316
<v Val Levitan>I, I, I, I can, I can tell you that I really don't like the repetitive screens.</v>

00:13:06.636 --> 00:13:10.076
<v Lena Zhukova>We are not going to have it like this. We are going to have it like this. Yeah.</v>

00:13:09.036 --> 00:13:10.396
<v Michael Gottlieb>Yeah, right.</v>

00:13:12.476 --> 00:13:16.156
<v Lena Zhukova>Because we can, and we always gave in Bonus on on Topper, always.</v>

00:13:12.636 --> 00:13:13.676
<v Val Levitan>Ohh, I see.</v>

00:13:16.556 --> 00:13:16.956
<v Michael Gottlieb>Right.</v>

00:13:22.436 --> 00:13:24.396
<v Michael Gottlieb>The horse looks like a real horse, Val.</v>

00:13:25.916 --> 00:13:26.316
<v Val Levitan>Yeah.</v>

00:13:26.636 --> 00:13:27.116
<v Michael Gottlieb>Yeah.</v>

00:13:28.396 --> 00:13:37.036
<v Michael Gottlieb>It's a very expensive horse, by the way. I did a lot of research on the most expensive horses you can buy out there, and that thing is pricey.</v>

00:13:38.716 --> 00:13:40.796
<v Michael Gottlieb>You can spend big money on those things.</v>

00:13:43.636 --> 00:13:49.036
<v Michael Gottlieb>But I think this should play well with that demographic. And again, this is a game we can bring to all of the markets.</v>

00:13:52.556 --> 00:14:10.956
<v Michael Gottlieb>I consider this, this is aspirational wealth and not everything in aspirational wealth is Hollywood or Miami nightclubs and $500 bottle of vodka in private room. Aspirational wealth in a place like Nebraska or South Dakota is this. Who's got the biggest ranch?</v>

00:14:12.316 --> 00:14:13.596
<v Michael Gottlieb>The expense of horse.</v>

00:14:15.116 --> 00:14:17.916
<v Michael Gottlieb>The rustic-looking cowboy, the attractive woman.</v>

00:14:18.636 --> 00:14:21.276
<v Val Levitan>Can I see the images up close, please?</v>

00:14:29.196 --> 00:14:34.716
<v Val Levitan>Do you have an eloquent description of each of those images?</v>

00:14:40.796 --> 00:14:47.276
<v Michael Gottlieb>No, not particularly. I really, I create, I pull reference art.</v>

00:14:48.356 --> 00:15:07.596
<v Michael Gottlieb>I go through and I find things on the internet that visually tell the story that we want to tell. And then I work with Lena to create it. I mean, that mansion, the facade of that mansion symbol, that's like a real mansion of extremely expensive home.</v>

00:15:08.076 --> 00:15:11.756
<v Lena Zhukova>But not open, Justin, it is the same as just inspired, yeah.</v>

00:15:08.396 --> 00:15:08.956
<v Michael Gottlieb>In.</v>

00:15:10.396 --> 00:15:18.236
<v Michael Gottlieb>Yeah, it's not the same. It's not the same, but it's the architectural design, the lighting, the snow, having the snow on the roof.</v>

00:15:20.476 --> 00:15:38.876
<v Michael Gottlieb>That dog is a very popular breed of dog in that market. You know, authenticity, people can smell when something is phoned in or fake. So you really have to, you know, this owl is actually, even though it's not the greatest looking owl, it's an appropriate owl. That is an owl that would be in that environment.</v>

00:15:40.396 --> 00:15:45.116
<v Lena Zhukova>And it's cheapest symbol, so it's it's good to solve, yeah.</v>

00:15:42.236 --> 00:15:43.356
<v Michael Gottlieb>Yeah, it's worthless.</v>

00:15:51.196 --> 00:15:53.356
<v Michael Gottlieb>So, that's where we are with Wildfire Ranch.</v>

00:16:00.876 --> 00:16:03.356
<v Michael Gottlieb>Do you want to go through the schedule or what?</v>

00:16:04.796 --> 00:16:06.476
<v Val Levitan>Yeah, let's look at the schedule, please.</v>

00:16:06.716 --> 00:16:07.116
<v Michael Gottlieb>Okay.</v>

00:16:17.516 --> 00:16:36.156
<v Michael Gottlieb>Okay, so under IP 531, game concepts, if you expand 1164, all of the South Dakota D2703 Nova concepts are complete.</v>

00:16:36.956 --> 00:16:39.196
<v Michael Gottlieb>I got that done.</v>

00:16:40.276 --> 00:16:47.436
<v Michael Gottlieb>And then moving on from there, IP 1190. Go ahead, please.</v>

00:16:45.356 --> 00:16:47.356
<v Val Levitan>Sorry, sorry, sorry.</v>

00:16:48.556 --> 00:16:52.236
<v Val Levitan>For 1164.</v>

00:16:53.676 --> 00:16:54.156
<v Val Levitan>Oh.</v>

00:16:55.756 --> 00:16:59.356
<v Val Levitan>Do we have, do we know the math for it?</v>

00:17:02.036 --> 00:17:07.116
<v Michael Gottlieb>For, for not for all the games, not for all the games.</v>

00:17:06.396 --> 00:17:08.876
<v Val Levitan>No, not for all the games.</v>

00:17:08.876 --> 00:17:29.596
<v Michael Gottlieb>Oh no, oh no. No, we still specifically, Efim need and I need to work. I mean, we have a sense of what we want to do, the basic concept of the math construct and the mechanics are defined. But for example, Aaron's Pub and Wildfire Ranch, we need to get builds up and playing and then Efim and I need to play the hell out of it.</v>

00:17:30.076 --> 00:17:31.276
<v Michael Gottlieb>To see what the...</v>

00:17:30.316 --> 00:17:34.316
<v Lena Zhukova>And may in two keynotes, we have two new keynotes, solar keynotes, and...</v>

00:17:33.476 --> 00:17:43.276
<v Michael Gottlieb>And there's two new keynos that have to get played as well, which have timing, choreography, all the stuff that we went through with the first two keynotes, we need to go through with Keynote 3 and Keno 4.</v>

00:17:44.156 --> 00:17:47.676
<v Lena Zhukova>Because they're totally different, they're not skins, they're too different.</v>

00:17:46.676 --> 00:17:47.356
<v Michael Gottlieb>Completely.</v>

00:17:48.236 --> 00:17:52.876
<v Michael Gottlieb>Completely different mechanics, completely different choreography, timings.</v>

00:17:53.596 --> 00:17:55.356
<v Val Levitan>So, for let's say...</v>

00:17:58.156 --> 00:17:59.636
<v Val Levitan>Rodeo Queen.</v>

00:18:01.796 --> 00:18:08.236
<v Val Levitan>Is this the same Rodeo Queen that we had in Georgia or somewhere else?</v>

00:18:07.196 --> 00:18:09.276
<v Michael Gottlieb>Yes, yeah, yes, yes.</v>

00:18:08.396 --> 00:18:12.956
<v Lena Zhukova>Yeah, but for for dual screens, different, different layout.</v>

00:18:10.796 --> 00:18:12.076
<v Michael Gottlieb>But it's a dual-screen version.</v>

00:18:12.556 --> 00:18:13.116
<v Efim Podvoiski>Not, not.</v>

00:18:14.476 --> 00:18:18.796
<v Efim Podvoiski>No, not for Georgia, because it cannot be the same in Georgia.</v>

00:18:17.836 --> 00:18:18.956
<v Michael Gottlieb>Well, the map, the map.</v>

00:18:17.996 --> 00:18:20.276
<v Lena Zhukova>Mass, mass, mass is different.</v>

00:18:20.316 --> 00:18:21.276
<v Michael Gottlieb>The math is different.</v>

00:18:22.476 --> 00:18:23.596
<v Michael Gottlieb>Because the Georgia map is.</v>

00:18:22.636 --> 00:18:26.716
<v Val Levitan>The math is different, but the math is different, but the assets are the same, right?</v>

00:18:22.876 --> 00:18:23.356
<v Lena Zhukova>Hello.</v>

00:18:26.956 --> 00:18:29.276
<v Michael Gottlieb>Correct. Except it's dual screen.</v>

00:18:29.436 --> 00:18:37.356
<v Lena Zhukova>Not the same, it's dual screen, so it's different size, different size of the wheels, different size of proportion of symbols.</v>

00:18:41.596 --> 00:18:42.236
<v Val Levitan>Sorry.</v>

00:18:47.916 --> 00:18:51.116
<v Val Levitan>I understand that the proportion are different, but...</v>

00:18:54.156 --> 00:18:55.596
<v Val Levitan>It will look the same, right?</v>

00:18:56.796 --> 00:18:58.756
<v Val Levitan>The proportions are different, I understand.</v>

00:18:57.276 --> 00:19:00.236
<v Michael Gottlieb>Yes, yes, yes.</v>

00:18:58.556 --> 00:18:59.196
<v Lena Zhukova>Yeah.</v>

00:19:00.396 --> 00:19:04.396
<v Val Levitan>And the reels are also the same, right?</v>

00:19:06.236 --> 00:19:06.876
<v Michael Gottlieb>Yes.</v>

00:19:08.396 --> 00:19:09.516
<v Val Levitan>Proportions are different.</v>

00:19:09.756 --> 00:19:10.236
<v Michael Gottlieb>Yes.</v>

00:19:11.036 --> 00:19:12.556
<v Val Levitan>And what about the background?</v>

00:19:13.996 --> 00:19:22.356
<v Lena Zhukova>Different because we cannot reuse vertical background for horizontal, we have much more space around and then for horizontal.</v>

00:19:20.956 --> 00:19:22.716
<v Val Levitan>I might not, not.</v>

00:19:24.396 --> 00:19:26.876
<v Val Levitan>I got it, I, I got it, I, I...</v>

00:19:25.116 --> 00:19:35.836
<v Lena Zhukova>Ah, I mean, you mean like philosophically, yeah, it's the same, it's the same thing, yeah, the same. I mean, my characters.</v>

00:19:33.036 --> 00:19:35.916
<v Val Levitan>Not philosophically, not philosophically.</v>

00:19:37.756 --> 00:19:40.236
<v Val Levitan>Not philosophically, aesthetically it's the same, right?</v>

00:19:44.876 --> 00:19:47.756
<v Val Levitan>The proportions are different, but aesthetically it's the same, right?</v>

00:19:48.676 --> 00:19:54.716
<v Michael Gottlieb>Background is going to look different because like she said, the proportions are different, the scale.</v>

00:19:53.836 --> 00:20:09.676
<v Lena Zhukova>You will see different pieces of background, some some pieces we will need to illustrate from scratch because for on vertical screen you will not see this areas and for horizontal screens they will be visible.</v>

00:20:11.276 --> 00:20:12.236
<v Val Levitan>Okay, so...</v>

00:20:14.716 --> 00:20:19.036
<v Val Levitan>From has has anything been done for?</v>

00:20:20.716 --> 00:20:24.476
<v Val Levitan>D27 Nova accept the concept stage.</v>

00:20:25.756 --> 00:20:30.716
<v Lena Zhukova>Design for some games, design is design stage is done.</v>

00:20:36.876 --> 00:20:41.436
<v Val Levitan>And the design stage is, is what this is when you will.</v>

00:20:40.796 --> 00:20:44.596
<v Lena Zhukova>It's what you saw for Aaron's pub.</v>

00:20:46.076 --> 00:20:48.156
<v Val Levitan>So those are final images.</v>

00:20:51.756 --> 00:20:53.276
<v Val Levitan>Those are the final images, right?</v>

00:20:53.276 --> 00:20:56.076
<v Lena Zhukova>Yeah, ready to be given to production, yeah.</v>

00:21:02.876 --> 00:21:03.836
<v Val Levitan>Is.</v>

00:21:05.036 --> 00:21:10.076
<v Val Levitan>Math for Wild Colt D 27 done.</v>

00:21:12.756 --> 00:21:13.996
<v Michael Gottlieb>That's on the theme question.</v>

00:21:14.396 --> 00:21:19.596
<v Efim Podvoiski>Wild Colt, I think it be just the same game that we had already, right?</v>

00:21:20.076 --> 00:21:23.036
<v Lena Zhukova>But with a match three, which match three.</v>

00:21:22.236 --> 00:21:23.516
<v Michael Gottlieb>But it's got match three.</v>

00:21:23.916 --> 00:21:38.236
<v Efim Podvoiski>Oh, okay, okay, I forgot, I forgot, we want to move to add much, so nothing is done, nothing is even started, but I think it's not even in pipeline because first we have to do class A, right?</v>

00:21:38.316 --> 00:21:48.716
<v Lena Zhukova>Yes. So when we finish Nebraska, we plan to start with Class A project. If we still okay with your plans, well, we wanted to confirm it.</v>

00:21:53.116 --> 00:21:54.476
<v Val Levitan>With my plans, you mean?</v>

00:21:54.476 --> 00:21:54.796
<v Lena Zhukova>Uh-huh.</v>

00:21:55.276 --> 00:21:55.996
<v Michael Gottlieb>Priorities.</v>

00:21:55.596 --> 00:21:57.516
<v Val Levitan>Yeah, yeah, it's the same, same.</v>

00:21:58.556 --> 00:22:16.596
<v Lena Zhukova>Okay, so our plan, our first project in Nova is going to be Class A, Alliance reaches design stage completely done for Class A, and we will be ready to start to do this transition of assets.</v>

00:22:17.116 --> 00:22:37.076
<v Lena Zhukova>Because we already have vertical lines which is done for Georgia, so we will make transition of symbols and backgrounds. And it's going to be our like first Nova project. I think it's a good first project because a lot of things in terms of...</v>

00:22:37.196 --> 00:22:38.836
<v Lena Zhukova>Graphical assets are.</v>

00:22:41.156 --> 00:22:51.476
<v Lena Zhukova>Like firm and confirmed and certain, and but on backstage we will have a lot of work to do, right? Are you for Class A?</v>

00:22:52.556 --> 00:22:54.956
<v Efim Podvoiski>Yeah, for the masses totally new.</v>

00:22:55.356 --> 00:23:14.636
<v Lena Zhukova>Yeah, and what we will work on for class A also is going to be a shader for Liquid Glass. So we will do Liquid Glass in a new way for our new framework. And in this project, we will do it like first time.</v>

00:23:19.316 --> 00:23:19.436
<v Val Levitan>The.</v>

00:23:34.796 --> 00:23:36.076
<v Val Levitan>South Dakota.</v>

00:23:37.156 --> 00:23:39.596
<v Val Levitan>T27 is the first.</v>

00:23:42.396 --> 00:23:45.516
<v Val Levitan>release of Nova or in Nova, right?</v>

00:23:46.236 --> 00:24:03.836
<v Michael Gottlieb>No, no, what we're saying is we were under the impression that Class A was a higher priority. So we were going to put Class A in front of South Dakota D27. But we still have time to make going a different direction if you'd rather focus on South Dakota first.</v>

00:24:07.356 --> 00:24:13.356
<v Val Levitan>No, no, I'm not changing the priority. The priority is fine. So then...</v>

00:24:14.876 --> 00:24:18.076
<v Val Levitan>Can I look at Class A then?</v>

00:24:20.556 --> 00:24:21.836
<v Val Levitan>The schedule, please.</v>

00:24:23.676 --> 00:24:27.596
<v Val Levitan>So class A now is in concept stage as well, right?</v>

00:24:23.916 --> 00:24:24.556
<v Lena Zhukova>Oh.</v>

00:24:27.996 --> 00:24:28.476
<v Michael Gottlieb>Yes.</v>

00:24:28.316 --> 00:24:31.676
<v Lena Zhukova>It's, yeah, so it's also in design stage.</v>

00:24:31.836 --> 00:24:43.356
<v Michael Gottlieb>Yeah, it is. Yeah, it's both in concept and design stage, but the the I expect to have basically everything in the concept stage done by end of end of next week.</v>

00:24:44.716 --> 00:24:59.036
<v Michael Gottlieb>Class A requirements are done. We agreed on what we were doing with Lions Riches. So the first one took a while. Lions Riches took a while because that was the test bed of what we wanted it to look like, play like, and whatever else. The rest of them I can knock out quick.</v>

00:25:05.196 --> 00:25:13.316
<v Lena Zhukova>And we created this very detailed storyboard for which we would, yeah.</v>

00:25:11.276 --> 00:25:14.076
<v Val Levitan>Yeah, yeah, you, yeah, you showed it to me.</v>

00:25:17.036 --> 00:25:17.676
<v Val Levitan>Quite good.</v>

00:25:19.116 --> 00:25:20.076
<v Lena Zhukova>So this.</v>

00:25:19.916 --> 00:25:20.716
<v Michael Gottlieb>It's crucial.</v>

00:25:20.876 --> 00:25:28.476
<v Val Levitan>Oh, by the way, by the way, why don't you use the same selection box with this level of opacity?</v>

00:25:30.636 --> 00:25:33.436
<v Val Levitan>On on now.</v>

00:25:38.076 --> 00:25:39.836
<v Val Levitan>Was it Nebraska that you showed me?</v>

00:25:41.436 --> 00:25:43.996
<v Val Levitan>Previously, as you do in.</v>

00:25:43.036 --> 00:25:46.956
<v Michael Gottlieb>Oh, the dual, the dual box, you talking about the dual box implementation?</v>

00:25:46.876 --> 00:26:01.676
<v Lena Zhukova>Yeah, I can explain you, because, as I said, like, for this is designed for Class A, and in Class A, we are going to, we are going to make it.</v>

00:26:03.676 --> 00:26:26.396
<v Lena Zhukova>We are going to work on shader, which will show you like, we cannot do it now with our approach, how we are dealing with Liquid Glass. Now, it's fake, and in the new framework we are going to work on shader, so you can really show</v>

00:26:27.476 --> 00:26:39.516
<v Lena Zhukova>transformation of real reels, which is dynamic and you show different image all the time under this glass dialogue box and shape.</v>

00:26:38.516 --> 00:26:43.596
<v Val Levitan>So, so you treat it, you treat it as a layer, separate layer, right?</v>

00:26:43.756 --> 00:26:56.156
<v Lena Zhukova>Yes, yes, so in your framework, we we can we can do it. That's why we we are going to use semi-transparent dialogue pads and.</v>

00:26:55.596 --> 00:27:13.796
<v Michael Gottlieb>And right, so that's the technical part of it. For me, from my perspective, Val, I'm just looking for player comfort and player familiarity in terms of interface. And we're taking this interface approach because it is in alignment with what class A looks like.</v>

00:27:13.916 --> 00:27:33.916
<v Michael Gottlieb>in that market. Whereas in Nebraska, our competitors are doing the larger dual box implementation. And I think that makes more sense. I think it's more coherent. I think it's actually easier to understand. I think there's less probability of making a mistake.</v>

00:27:33.996 --> 00:27:41.836
<v Michael Gottlieb>Not so much making a mistake with your choice, but with a box being as huge as it is, it's easy to, you know, to pick the one with the big Coin.</v>

00:27:43.116 --> 00:27:49.276
<v Michael Gottlieb>So I think both implementations are good and appropriate, I guess. I think they're market appropriate implementations.</v>

00:27:59.276 --> 00:28:17.676
<v Michael Gottlieb>And of all the feedback that we've had in Nebraska, nobody at any point, I didn't hear from Juan or anybody say the way in which we implemented the dual box is problematic or unacceptable or, you know, creates an issue. So I always, when I make changes, I always think, what's the first rule of medicine? Do no harm.</v>

00:28:20.796 --> 00:28:28.956
<v Michael Gottlieb>Start from a position of strength and move stronger as opposed to, you know, cracking the patient back open when you don't know whether or not that makes sense.</v>

00:28:43.916 --> 00:28:44.236
<v Val Levitan>Right.</v>

00:28:53.596 --> 00:29:14.476
<v Michael Gottlieb>Okay, so by end of next week, excuse me, all of the abstracts and the concept stuff for the George Coin Class A, Nova will be complete. And then we're going to be focused on just getting Nebraska done. Subsequent to that, we find we have a build up and running, but that's</v>

00:29:14.516 --> 00:29:16.236
<v Michael Gottlieb>That's going to be the primary focus.</v>

00:29:16.876 --> 00:29:36.236
<v Lena Zhukova>Yeah, and I'm continuing to work on design stages for all South Dakota 3 in Nova games, so now I'm working on Queen of Luxor, Keno, Queen of Luxor, Keno.</v>

00:29:36.716 --> 00:29:44.156
<v Lena Zhukova>Totally different Keno Games, but with using a theme of Egyptian theme, and after...</v>

00:29:43.436 --> 00:29:46.556
<v Val Levitan>How many, how many Keno, how many Keno will you guys have?</v>

00:29:48.076 --> 00:29:52.956
<v Lena Zhukova>We are going to have four of them, right?</v>

00:29:50.556 --> 00:29:51.756
<v Michael Gottlieb>Should be the 4th, right?</v>

00:29:54.396 --> 00:29:55.436
<v Val Levitan>For additional.</v>

00:29:55.996 --> 00:29:58.476
<v Lena Zhukova>No, for total.</v>

00:29:56.316 --> 00:29:56.716
<v Efim Podvoiski>No.</v>

00:29:56.676 --> 00:30:00.156
<v Michael Gottlieb>No, for cumulative, yeah, Black Hills came.</v>

00:29:59.196 --> 00:30:01.516
<v Val Levitan>So, one, one, one more, yeah?</v>

00:30:02.236 --> 00:30:02.796
<v Lena Zhukova>Two more.</v>

00:30:02.396 --> 00:30:17.036
<v Michael Gottlieb>Yeah, three and four, two more. That'll be 3 and four. Excuse me, Nebraska or South Dakota. South Dakota 2 has Black Hills Keno Deluxe and Cool Cat Keno. And then...</v>

00:30:18.076 --> 00:30:31.196
<v Michael Gottlieb>South Dakota 3, excuse me, 3 will add Solar Keno, which you've seen, and then Queen of Luxor Keno, which we're just getting started on now.</v>

00:30:36.156 --> 00:30:37.436
<v Michael Gottlieb>So that'll be 4 Keno.</v>

00:30:47.756 --> 00:30:50.956
<v Val Levitan>The tentative date for South Dakota is when?</v>

00:30:53.756 --> 00:31:12.636
<v Lena Zhukova>We don't know yet. We even maybe we wanted to discuss that after we will finish class A in Nova. Maybe it makes sense to work on a new Georgia before release in Nova if you want to.</v>

00:31:12.676 --> 00:31:27.676
<v Lena Zhukova>present a nice curved machine with curved monitor in August and with new, impressive new release, maybe it makes sense to do Georgia first.</v>

00:32:12.796 --> 00:32:13.836
<v Val Levitan>I'm thinking.</v>

00:32:17.596 --> 00:32:18.876
<v Val Levitan>I'm thinking maybe.</v>

00:32:21.396 --> 00:32:25.116
<v Val Levitan>To go back to Class 3 for Columbia.</v>

00:32:33.436 --> 00:32:35.676
<v Val Levitan>In Nova, in Nova.</v>

00:32:33.676 --> 00:32:34.156
<v Michael Gottlieb>Okay.</v>

00:33:00.236 --> 00:33:01.756
<v Lena Zhukova>Vertical door screen.</v>

00:33:05.356 --> 00:33:10.556
<v Lena Zhukova>Or one screen, like, remember, we had one screen of cabinets and...</v>

00:33:14.636 --> 00:33:19.836
<v Val Levitan>I think in Nova we could do vertical or horizontal, like universal.</v>

00:33:31.596 --> 00:33:34.396
<v Val Levitan>It would be a very easy test bed for us.</v>

00:33:41.436 --> 00:33:43.836
<v Val Levitan>I just don't know how to manage.</v>

00:33:46.716 --> 00:33:49.356
<v Val Levitan>part of the product ownership.</v>

00:33:54.916 --> 00:33:56.316
<v Val Levitan>Who can give?</v>

00:33:57.836 --> 00:33:59.676
<v Val Levitan>Prod ownership direction.</v>

00:34:00.796 --> 00:34:01.676
<v Val Levitan>Or Columbia.</v>

00:34:05.436 --> 00:34:06.876
<v Michael Gottlieb>Do we still have a guy down there?</v>

00:34:08.716 --> 00:34:09.196
<v Val Levitan>Yeah.</v>

00:34:12.596 --> 00:34:14.636
<v Val Levitan>We have a reliable person there.</v>

00:34:17.116 --> 00:34:20.876
<v Val Levitan>But she has never been trained on product ownership.</v>

00:34:23.676 --> 00:34:25.356
<v Val Levitan>I think she will struggle with it.</v>

00:34:30.236 --> 00:34:37.916
<v Michael Gottlieb>Do you think maybe she would be capable of identifying what products are successful in the market right now and just simply providing some screenshots and a list?</v>

00:34:38.316 --> 00:34:40.476
<v Val Levitan>Yeah, that she will be able to.</v>

00:34:44.636 --> 00:34:48.316
<v Val Levitan>She would do a good job on this. She's given direction on what to do.</v>

00:34:49.436 --> 00:34:50.876
<v Val Levitan>Should do a good job on this.</v>

00:34:52.396 --> 00:34:54.076
<v Val Levitan>She's a clever, clever woman.</v>

00:34:57.036 --> 00:34:57.996
<v Val Levitan>An engineer.</v>

00:35:01.436 --> 00:35:06.076
<v Val Levitan>If she understands the ask, she will deliver the reply.</v>

00:35:08.156 --> 00:35:11.756
<v Michael Gottlieb>Do we still have a number of machines deployed in that market?</v>

00:35:12.556 --> 00:35:13.036
<v Val Levitan>Yeah.</v>

00:35:24.156 --> 00:35:28.156
<v Val Levitan>and that might give us the practice that we need for class 3.</v>

00:35:37.396 --> 00:35:38.796
<v Val Levitan>What are your thoughts on this?</v>

00:35:44.516 --> 00:35:46.396
<v Michael Gottlieb>You talking about like regular class 3?</v>

00:35:48.716 --> 00:35:52.636
<v Michael Gottlieb>Like Florida or are you talking about South Dakota and Nebraska?</v>

00:35:54.956 --> 00:35:56.476
<v Val Levitan>No, regular toss three.</v>

00:35:58.196 --> 00:35:59.116
<v Michael Gottlieb>I think it's suicide.</v>

00:36:00.716 --> 00:36:07.036
<v Michael Gottlieb>I know it's suicide because I have a lot of friends that are at our competitors and they are getting their ***** handed to them.</v>

00:36:09.436 --> 00:36:12.156
<v Michael Gottlieb>The situation is just continuing to deteriorate.</v>

00:36:14.236 --> 00:36:14.956
<v Val Levitan>You thought so?</v>

00:36:15.836 --> 00:36:17.276
<v Michael Gottlieb>Very much so. Oh, yeah.</v>

00:36:20.796 --> 00:36:30.796
<v Michael Gottlieb>Yeah, lots and lots and lots of money is being thrown against the wall. Dozens and dozens of games are being released and not a whole lot is sticking.</v>

00:36:32.796 --> 00:36:53.276
<v Michael Gottlieb>There's a lot of capital constraint on the casino part because as we all know, the casinos have sold the property. And well, all you have to do is read the Las Vegas Review Journal and it tells you about tourism is down. The joke now is that the customers, they call them the Coleman's,</v>

00:36:53.596 --> 00:37:12.076
<v Michael Gottlieb>because there's a brand of ice cooler, ice chest called Coleman. And the Coleman's are the, it's a euphemism for people that show up with an ice chest filled with their own beer and baloney and white bread. And so they don't eat at the casino, they don't drink at the casino, they don't gamble at the casino.</v>

00:37:12.596 --> 00:37:31.116
<v Michael Gottlieb>and they just spend as little as possible. Combined with a contracting economy, you know, insurance rates have skyrocketed, medical, everything has skyrocketed. Gasoline is completely off the charts. Diesel gasoline here is like $9.40 a gallon.</v>

00:37:31.916 --> 00:37:52.476
<v Michael Gottlieb>And everything's transported with diesel. You know, everything at the grocery store is insane. So all I'm hearing from my friends is that people are simply tapped. They're tapped. They're not, the Coin in is not what it used to be. They have spent a lot of money, casinos have spent a lot of money on equipment over the last couple of years. And they've got 10 year cycles.</v>

00:37:53.636 --> 00:38:12.836
<v Michael Gottlieb>There's no reason to change anything, replace anything, bring anything in new. They'll take anything you want for test. They'll take your money all day long, you know, they'll take the machine earnings all day long, test your game, and then after 30 days, out the door it goes. I mean, Konami, Aristocrat, Blueberry.</v>

00:38:14.316 --> 00:38:18.876
<v Michael Gottlieb>Novomatic Gaming Arts is now in it aggressively.</v>

00:38:21.356 --> 00:38:23.756
<v Michael Gottlieb>It's just bad. I don't know what else to tell you.</v>

00:38:28.516 --> 00:38:29.116
<v Val Levitan>You're out.</v>

00:38:30.876 --> 00:38:37.276
<v Val Levitan>I don't have any other information. Maybe from time to time I get delirious, but...</v>

00:38:40.236 --> 00:38:43.676
<v Val Levitan>Delirious in thinking that, well, maybe, but...</v>

00:38:45.516 --> 00:38:47.876
<v Val Levitan>If you want to be pragmatic, you're very correct.</v>

00:38:49.276 --> 00:38:54.556
<v Michael Gottlieb>I think your vision for the transactional product is genius.</v>

00:38:55.676 --> 00:38:57.036
<v Michael Gottlieb>I think that's where it's at.</v>

00:38:57.916 --> 00:38:59.676
<v Val Levitan>Just call me Mr. Genius, please.</v>

00:38:59.996 --> 00:39:01.516
<v Michael Gottlieb>Well, okay, Mr. Genius.</v>

00:39:02.876 --> 00:39:06.396
<v Michael Gottlieb>But I think your vision for that, and it's in your wheelhouse.</v>

00:39:09.036 --> 00:39:16.716
<v Michael Gottlieb>You've had tremendous success in that space, in that market. You know it. You know it better than anybody. You've had just about more success than anybody.</v>

00:39:19.356 --> 00:39:22.956
<v Val Levitan>Yes, stay focused on what we're doing. Stay nimble.</v>

00:39:24.316 --> 00:39:28.556
<v Val Levitan>So, what uh, so this cycle, and I'm just...</v>

00:39:31.116 --> 00:39:32.236
<v Val Levitan>Shooting the **** here.</v>

00:39:32.476 --> 00:39:33.196
<v Michael Gottlieb>Yeah, please.</v>

00:39:34.796 --> 00:39:36.076
<v Val Levitan>So, this cycle.</v>

00:39:38.796 --> 00:39:40.076
<v Val Levitan>How long can it last?</v>

00:39:41.436 --> 00:39:45.116
<v Val Levitan>So, we should see that we should see the domino effect.</v>

00:39:47.996 --> 00:39:50.796
<v Val Levitan>much sooner. Interest rates are climbing.</v>

00:39:53.116 --> 00:40:04.476
<v Val Levitan>There is absolutely zero chance, regardless of our party, whoever's going to control the house or stand up, makes no difference. The interest rate will stay high or higher.</v>

00:40:05.036 --> 00:40:05.356
<v Michael Gottlieb>Yes.</v>

00:40:05.356 --> 00:40:08.956
<v Val Levitan>And the Fed and the Fed has no choice but to print money.</v>

00:40:10.076 --> 00:40:10.876
<v Val Levitan>No choice.</v>

00:40:12.236 --> 00:40:18.396
<v Val Levitan>So with interest rate higher, the inflation will also accelerate because you print money.</v>

00:40:27.836 --> 00:40:30.076
<v Val Levitan>Traffic is down, yeah, I agree with that.</v>

00:40:33.476 --> 00:40:36.636
<v Val Levitan>Casinos will be strapped. They're not going to be spending any money.</v>

00:40:39.116 --> 00:40:43.276
<v Val Levitan>So it will wear them down. They start using Talent as well.</v>

00:40:48.556 --> 00:40:52.476
<v Val Levitan>The Gaming manufacturers cannot survive on the street business.</v>

00:40:55.116 --> 00:40:57.116
<v Val Levitan>New casinos cannot open.</v>

00:40:58.276 --> 00:40:59.916
<v Val Levitan>Because interest rates are high.</v>

00:41:07.676 --> 00:41:10.476
<v Val Levitan>The demand will continue diminishing.</v>

00:41:13.116 --> 00:41:15.436
<v Val Levitan>So, what's going to happen to the manufacturers?</v>

00:41:16.316 --> 00:41:17.596
<v Val Levitan>Gaming manufacturers.</v>

00:41:18.036 --> 00:41:37.916
<v Michael Gottlieb>I think a lot of them are in a lot of trouble, except for the ones that have dominance in other markets and focus in other markets. You know, the Novamatics of the world are going to be fine. Zitro and Ortiz and, you know, those guys, they're going to be fine because they're in other markets. I think that...</v>

00:41:37.996 --> 00:41:57.556
<v Michael Gottlieb>that IGT and Light and Wonder are aggressively trying to continue to court Macau and other international markets. I mean, that was one of the, it was an early lesson I learned because back in the mid 70s, my dad was exporting over 70%</v>

00:41:58.556 --> 00:42:18.756
<v Michael Gottlieb>of his production runs to outside of the United States. So I think people with strength outside the United States stand a fighting chance. But it is inevitable that there is going to be contraction because a lot of people are answering questions that nobody is asking.</v>

00:42:19.436 --> 00:42:39.116
<v Michael Gottlieb>And you're not even touching on the number of jobs that are going to be lost due to AI. And I don't mean like legitimately, sincerely, like, oh, this was the right decision. I mean that corporate America are lemmings and they're all doing, they're all chasing something. Some of them will be successful at it. Some of them will fail.</v>

00:42:39.396 --> 00:42:58.356
<v Michael Gottlieb>tactically at it, but the net result is that people are being terminated in droves. Electronic Arts just shut down BioWare this week, and that's another 400 people that got fired. And Qualcomm is going to be having layoffs, and when you have layoffs, unemployment is going to be...</v>

00:42:58.436 --> 00:43:19.036
<v Michael Gottlieb>climb and you're going to have a scenario where there are fewer consumers. I mean, it's a K-shaped economy. You've got a very, very small percentage of people that are doing very well, and then the rest of the masses that are struggling tremendously. All you have to do, I follow, you know, I read.</v>

00:43:19.276 --> 00:43:41.836
<v Michael Gottlieb>a lot and bankruptcies are accelerating. Credit card delinquencies are accelerating. There's some concern that, you know, cars during COVID were very expensive and people went out and got 10 year loans on their cars. And now they're talking about, remember the subprime fiasco we had in whatever it was, 2007 and 2008.</v>

00:43:41.956 --> 00:43:52.156
<v Michael Gottlieb>There's some people speculating there's trillions of dollars of these bad car loans on the books. And if people can't, don't have the money, they're not going to be able to pay. Yeah, their car will get repossessed. But there's.</v>

00:43:51.596 --> 00:43:52.716
<v Val Levitan>Same as the homes.</v>

00:43:53.196 --> 00:44:12.156
<v Michael Gottlieb>Exactly, same as the homes, same as the homes, in some instances worse because of what you needed to get a home, I mean, excuse me, what you need to be able to buy a car, and the value of that asset, you know, has dropped drastically, has has diminished, you know, significantly.</v>

00:44:12.796 --> 00:44:32.516
<v Michael Gottlieb>So I think, you know, the cycle, I think we're in for austerity. I think the quality of life in the United States for the average American is going to be significantly lower than it has been. The ability for people to afford $1000 iPhones every year and take vacations or, you know, live in a home versus in an apartment.</v>

00:44:32.956 --> 00:44:42.316
<v Michael Gottlieb>I'm not particularly encouraged by this scenario. Give me some data that tells me otherwise. Forgetting about the emotion, just the pure data, Val. None of it is encouraging.</v>

00:44:44.876 --> 00:44:45.356
<v Val Levitan>Yeah.</v>

00:44:48.156 --> 00:44:48.636
<v Val Levitan>Yeah.</v>

00:44:49.116 --> 00:44:51.036
<v Michael Gottlieb>All that being said, go ahead.</v>

00:44:49.596 --> 00:44:52.396
<v Val Levitan>I'm also, I'm also, I'm also very scared.</v>

00:45:07.716 --> 00:45:16.796
<v Michael Gottlieb>If there's a silver lining in any of it, if people can't afford to go to Las Vegas to gamble, the street locations are only going to get more popular.</v>

00:45:13.756 --> 00:45:14.076
<v Val Levitan>Right.</v>

00:45:17.516 --> 00:45:17.996
<v Val Levitan>Right.</v>

00:45:18.996 --> 00:45:37.996
<v Michael Gottlieb>People in Georgia that can't afford the air, because you know airplanes run on fuel, fuel costs are skyrocketing, airplane tickets are skyrocketing, hotels are three, 4, 5, $700 a night. If you can't go on a vacation, you can still go with a couple 100 bucks to your local gas station and play a slot machine to escape.</v>

00:45:38.556 --> 00:45:51.676
<v Michael Gottlieb>So I continue to believe that those markets, the things I saw in Georgia, the things that are going on in Illinois and Texas, I mean, that will continue to grow. Regional Gaming, I think, is going to continue to grow.</v>

00:46:09.676 --> 00:46:12.076
<v Val Levitan>There you go, you resolved the issue.</v>

00:46:14.236 --> 00:46:22.556
<v Michael Gottlieb>If there's an opportunity in Colombia where people have like Jvl machines in the past, I would, you know,</v>

00:46:23.716 --> 00:46:35.356
<v Michael Gottlieb>say that the quality of our product has continued to improve. We have not been in that market for quite a period of time. If there is an appetite and if there is an interest level,</v>

00:46:36.556 --> 00:46:54.556
<v Michael Gottlieb>I think we have more competitive product now than, you know, it was competitive at the time, but as the market has changed, the quality of our art, our presentation layer, the mechanics that we're offering, there's a whole new universe of stuff that Jvl has to offer that Columbia has never seen.</v>

00:46:55.916 --> 00:46:59.996
<v Michael Gottlieb>I mean, did they ever see Jackpot Rush? Did the old Jackpot Rush ever go to Columbia?</v>

00:47:01.356 --> 00:47:01.836
<v Lena Zhukova>No.</v>

00:47:02.716 --> 00:47:03.116
<v Efim Podvoiski>Oh.</v>

00:47:02.956 --> 00:47:20.276
<v Michael Gottlieb>Okay, and certainly fiery ice has never been there. The match 3 bonus, the new art that we've done for a lot of these games, the tweaks and adjustments. So if there's an opportunity there to make money all day long. But as a test bed and proving ground for doing something else,</v>

00:47:21.436 --> 00:47:22.716
<v Michael Gottlieb>I respectfully do.</v>

00:47:21.756 --> 00:47:32.316
<v Val Levitan>Well, Columbia, Columbia has, we're very well established in Columbia. Our business is ran by a very reliable individual.</v>

00:47:33.516 --> 00:47:34.396
<v Val Levitan>Ohh.</v>

00:47:36.316 --> 00:47:37.116
<v Val Levitan>So...</v>

00:47:37.996 --> 00:47:40.636
<v Val Levitan>We have, we have installed base that.</v>

00:47:41.516 --> 00:47:46.556
<v Val Levitan>We haven't touched, and that's that cow that keeps on giving milk.</v>

00:47:47.916 --> 00:47:48.556
<v Val Levitan>But.</v>

00:47:51.036 --> 00:47:55.196
<v Val Levitan>We need, we need something for the end of 2027.</v>

00:47:58.156 --> 00:48:05.116
<v Val Levitan>If we don't have something by the end of 2027, we will lose that cow. That cow will die.</v>

00:48:07.196 --> 00:48:07.916
<v Val Levitan>Solved.</v>

00:48:10.716 --> 00:48:15.596
<v Val Levitan>Let's gently plan a class 3.</v>

00:48:16.396 --> 00:48:18.156
<v Val Levitan>Can you create a...</v>

00:48:21.436 --> 00:48:28.236
<v Lena Zhukova>Can we introduce a new available at any bed which we created for class three?</v>

00:48:22.276 --> 00:48:22.476
<v Val Levitan>Good.</v>

00:48:27.596 --> 00:48:35.836
<v Val Levitan>Let's not, let's not do that. Let's ask, let's ask what's making money right now in Colombia. Let's start from that.</v>

00:48:34.476 --> 00:48:35.036
<v Lena Zhukova>Mhm.</v>

00:48:36.036 --> 00:48:37.076
<v Lena Zhukova>OKOK.</v>

00:48:37.836 --> 00:48:44.716
<v Efim Podvoiski>But do we have any new cabinets there or try to replace old ones? I replaced software.</v>

00:48:45.356 --> 00:48:48.716
<v Val Levitan>We have first version of Flex.</v>

00:48:52.076 --> 00:48:53.436
<v Val Levitan>So, we can upgrade it.</v>

00:49:00.476 --> 00:49:03.036
<v Michael Gottlieb>And this would be Nova. This would be Nova.</v>

00:49:00.596 --> 00:49:01.516
<v Val Levitan>Which is not here.</v>

00:49:10.316 --> 00:49:14.876
<v Val Levitan>Nova, because we're decommissioning.</v>

00:49:17.116 --> 00:49:18.236
<v Val Levitan>Rage completely.</v>

00:49:21.116 --> 00:49:26.476
<v Michael Gottlieb>Understood. And so are we talking about selling software upgrades or selling new hardware down there?</v>

00:49:26.876 --> 00:49:28.956
<v Val Levitan>It's our own machine by participating.</v>

00:49:31.116 --> 00:49:37.356
<v Michael Gottlieb>Okay, so we would upgrade the machines with a new CPU, new graphics card.</v>

00:49:38.236 --> 00:49:39.596
<v Michael Gottlieb>They don't have V-Dex then.</v>

00:49:38.916 --> 00:49:39.196
<v Val Levitan>Yeah.</v>

00:49:40.356 --> 00:49:42.236
<v Val Levitan>Then we have VDACs, yeah.</v>

00:49:42.556 --> 00:49:44.396
<v Michael Gottlieb>Oh, they do have V-Dex. Okay.</v>

00:49:43.996 --> 00:49:45.356
<v Val Levitan>Yeah, yeah, we have defects.</v>

00:49:47.676 --> 00:49:52.316
<v Val Levitan>We have V-Dex and we will upgrade our own stuff.</v>

00:49:55.436 --> 00:50:04.316
<v Michael Gottlieb>Well, then obviously the first step is identifying of our own stuff, what, what, what's the most popular, what's working, and then...</v>

00:50:06.676 --> 00:50:10.636
<v Michael Gottlieb>what the players are gravitating to.</v>

00:50:11.636 --> 00:50:12.796
<v Michael Gottlieb>from our competitors.</v>

00:50:19.036 --> 00:50:33.596
<v Michael Gottlieb>Because we got a lot of answers now, and we've got more answers coming, and we can come up with more answers. We just need to know what's going on down there, what's working, what's resonating, and we can build off of that.</v>

00:50:37.796 --> 00:50:41.436
<v Val Levitan>So, do you wanna ask those questions in a written form?</v>

00:50:42.516 --> 00:50:44.076
<v Val Levitan>And I'll open that dialogue.</v>

00:50:45.116 --> 00:50:48.076
<v Michael Gottlieb>Yes, let me give some thought to it, yeah.</v>

00:50:49.156 --> 00:50:51.596
<v Michael Gottlieb>Does the individual speak English as well as Spanish?</v>

00:50:53.276 --> 00:50:55.916
<v Val Levitan>Doesn't matter today, it's so easy, and uh...</v>

00:50:57.436 --> 00:51:01.516
<v Val Levitan>You know, Claude Code, I mean, Claude translates it, doesn't matter.</v>

00:50:59.516 --> 00:50:59.836
<v Michael Gottlieb>Right.</v>

00:51:01.916 --> 00:51:09.516
<v Michael Gottlieb>I just meant in the sense of actually being able to have a Teams call with this person, you know, establish a rapport.</v>

00:51:14.556 --> 00:51:15.836
<v Val Levitan>She is very quiet.</v>

00:51:20.716 --> 00:51:23.276
<v Val Levitan>She's she's not a conversationist.</v>

00:51:25.756 --> 00:51:26.876
<v Michael Gottlieb>I can get her to talk.</v>

00:51:30.396 --> 00:51:32.076
<v Val Levitan>I am happy to arrange a call.</v>

00:51:32.476 --> 00:51:36.556
<v Michael Gottlieb>Yeah, no, I'll do like hand puppets. I don't even have to talk. I'll just do it with puppets.</v>

00:51:38.076 --> 00:51:38.716
<v Michael Gottlieb>It's all good.</v>

00:51:41.276 --> 00:51:49.636
<v Val Levitan>Okay, think about it. Let's put a set of questions together. She'll prepare the answers and we can arrange for a conversation.</v>

00:51:51.276 --> 00:51:51.916
<v Michael Gottlieb>Sounds good.</v>

00:51:55.196 --> 00:52:00.396
<v Val Levitan>Okay, that's it for me. Ah, yes, no, sorry. I have...</v>

00:52:02.236 --> 00:52:05.356
<v Val Levitan>Can, can you, are you guys done? Can I ask my question?</v>

00:52:05.516 --> 00:52:06.076
<v Michael Gottlieb>Blaze.</v>

00:52:10.636 --> 00:52:15.316
<v Val Levitan>Actually, no, sorry. I want to see game production on the schedule.</v>

00:52:21.516 --> 00:52:22.316
<v Val Levitan>There we go.</v>

00:52:23.196 --> 00:52:26.156
<v Val Levitan>Yes, ohh, you started from Nebraska. Got it.</v>

00:52:27.676 --> 00:52:31.476
<v Lena Zhukova>That's the only project in production right now.</v>

00:52:31.836 --> 00:52:34.796
<v Val Levitan>Can I see the time schedule where it takes me?</v>

00:52:36.476 --> 00:52:37.836
<v Lena Zhukova>December 21st.</v>

00:52:43.276 --> 00:52:43.916
<v Val Levitan>Okay.</v>

00:52:44.876 --> 00:52:48.876
<v Val Levitan>Clear. Can somebody explain to me a churn?</v>

00:52:53.356 --> 00:52:53.836
<v Efim Podvoiski>Sorry?</v>

00:52:54.556 --> 00:52:55.036
<v Lena Zhukova>Dwolla.</v>

00:52:54.716 --> 00:52:55.356
<v Val Levitan>Charm.</v>

00:52:56.156 --> 00:52:57.436
<v Efim Podvoiski>In what context then?</v>

00:52:58.236 --> 00:53:00.796
<v Val Levitan>in contest of gaming machines.</v>

00:53:02.476 --> 00:53:03.676
<v Val Levitan>Churn.</v>

00:53:04.316 --> 00:53:05.676
<v Efim Podvoiski>Yeah, it's like.</v>

00:53:06.476 --> 00:53:09.356
<v Efim Podvoiski>Your Rtp is like 90%, for example.</v>

00:53:10.316 --> 00:53:11.596
<v Efim Podvoiski>You come with $20?</v>

00:53:12.756 --> 00:53:14.076
<v Efim Podvoiski>Play a dollar game.</v>

00:53:15.036 --> 00:53:35.476
<v Efim Podvoiski>Play 20 games, lose your $20, but you won an average $18.00, then you play on this $18.00 and so on and so forth. So, actually, before you lose all your money, you probably your total bet is not $20, but probably 50 or...</v>

00:53:36.076 --> 00:53:54.716
<v Efim Podvoiski>Seventy dollars, so remember, is a ratio of your money in of your, sorry, of your total bet to cash in to your $20, so you come with $20, you actually...</v>

00:53:54.756 --> 00:54:00.156
<v Efim Podvoiski>Played 50 games, so your turn is 2 1/2.</v>

00:54:05.356 --> 00:54:05.996
<v Val Levitan>Okay.</v>

00:54:08.476 --> 00:54:14.876
<v Val Levitan>You came with $20, but you placed $50 worth of bet.</v>

00:54:15.356 --> 00:54:15.756
<v Efim Podvoiski>Yes.</v>

00:54:17.356 --> 00:54:21.356
<v Val Levitan>So it is your initial money that you come with.</v>

00:54:23.436 --> 00:54:25.276
<v Val Levitan>Divide it into.</v>

00:54:26.316 --> 00:54:27.276
<v Efim Podvoiski>The other way around.</v>

00:54:26.956 --> 00:54:27.436
<v Val Levitan>Both.</v>

00:54:29.596 --> 00:54:31.436
<v Val Levitan>Sorry, yes, the other way around.</v>

00:54:32.476 --> 00:54:37.396
<v Val Levitan>total number of beds divided by the amount of money you came with.</v>

00:54:38.076 --> 00:54:38.636
<v Efim Podvoiski>Yes.</v>

00:54:41.996 --> 00:54:46.316
<v Val Levitan>So the higher the churn, the supposedly better the math.</v>

00:54:53.156 --> 00:55:02.476
<v Efim Podvoiski>First of all, it depends on the first variable, the most important one is the Rtp. So the higher the Rtp is the be.</v>

00:55:01.356 --> 00:55:03.756
<v Val Levitan>At the same, at the same Rtp.</v>

00:55:06.316 --> 00:55:19.996
<v Efim Podvoiski>I don't know what better means in this case. Better for players who look for time on the machine, yes. But that means that it might be a dribbling game, it's just...</v>

00:55:21.436 --> 00:55:28.796
<v Efim Podvoiski>Gives you ninety-eight cent over your dollar, but you stay in forever and never have any actions, so...</v>

00:55:30.876 --> 00:55:36.916
<v Efim Podvoiski>I don't the highest volatility is the lower the chart, so it's...</v>

00:55:38.316 --> 00:55:39.356
<v Efim Podvoiski>It's a Bonus.</v>

00:55:41.996 --> 00:55:43.596
<v Val Levitan>How do you measure it?</v>

00:55:45.116 --> 00:55:46.796
<v Val Levitan>Over a long period of time.</v>

00:55:49.276 --> 00:55:49.676
<v Efim Podvoiski>So, yeah?</v>

00:55:51.156 --> 00:55:53.836
<v Val Levitan>Is there a way to measure it over a long period of time?</v>

00:55:51.356 --> 00:55:52.396
<v Efim Podvoiski>Measure.</v>

00:55:54.156 --> 00:55:55.876
<v Efim Podvoiski>Measuring in the field.</v>

00:55:56.636 --> 00:55:57.036
<v Val Levitan>Yeah.</v>

00:55:57.596 --> 00:56:12.636
<v Efim Podvoiski>Yeah, it's just simply divide like money in like a total bet by money into much. It's not exactly because sometimes people take money out before they use everything, but more or less.</v>

00:56:32.716 --> 00:56:33.276
<v Val Levitan>Clear.</v>

00:56:34.156 --> 00:56:35.356
<v Val Levitan>That's it for me, guys.</v>

00:56:37.676 --> 00:56:40.556
<v Michael Gottlieb>Okay, enjoy your couple of days off there next week.</v>

00:56:42.796 --> 00:56:44.796
<v Val Levitan>Thank you very much. All the best to everyone.</v>

00:56:45.156 --> 00:56:46.556
<v Michael Gottlieb>OK, take care.</v>

00:56:46.116 --> 00:56:47.676
<v Efim Podvoiski>Have a good weekend, everybody.</v>

00:56:47.676 --> 00:56:49.476
<v Lena Zhukova>Yeah, I will put it in time.</v>

