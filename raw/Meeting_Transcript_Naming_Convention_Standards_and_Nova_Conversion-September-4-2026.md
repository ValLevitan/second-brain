# Raw Transcript - Game_Development (Naming Convention Standards and Nova Conversion)
**Date:** September 4, 2026, 2:07 PM - 4:27 PM Eastern
**Source meeting:** Game_Development - September 4, 2026
**Summary note:** [[Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026]]
---
WEBVTT

00:00:10.267 --> 00:00:12.347
<v Michael Gottlieb>There was some type of asset.</v>

00:00:13.387 --> 00:00:32.907
<v Michael Gottlieb>thing, mess that they ran into that we had to untangle. And so that's what last week and this week has consisted of. It's finally settled down and gotten to the point of where it's under control. And the build, I think, is now in a state where</v>

00:00:33.147 --> 00:00:36.907
<v Michael Gottlieb>You know, Felipe should get an ISO and play the hell out of it.</v>

00:00:37.467 --> 00:00:46.347
<v Lena Zhukova>But the Queen of Luxor is still not fully done, so we are still finishing new assets for Queen of Luxor.</v>

00:00:42.747 --> 00:00:43.147
<v Michael Gottlieb>Right.</v>

00:00:47.147 --> 00:00:57.787
<v Efim Podvoiski>Yeah, and this is this issue we wanted to extend Nigeria and I believe it's not in plant for some reason.</v>

00:00:52.827 --> 00:00:53.307
<v Michael Gottlieb>Yes.</v>

00:00:53.787 --> 00:00:54.347
<v Juan Martinez>Yes.</v>

00:00:54.347 --> 00:00:55.547
<v Lena Zhukova>When you to the expert.</v>

00:00:57.227 --> 00:01:15.867
<v Lena Zhukova>We need to re-export 6 scenes, so it depends some experts from artists as well. So, because touch area is defined by a special object planar in the 3D scene, so...</v>

00:01:15.947 --> 00:01:24.507
<v Lena Zhukova>We have six type of different matches depending on layout of the game.</v>

00:01:25.627 --> 00:01:25.787
<v Val Levitan>Yeah.</v>

00:01:25.667 --> 00:01:34.907
<v Lena Zhukova>Because we have six different type of, so yeah, it's it's not it's not much, but there are a lot of such things, so...</v>

00:01:30.107 --> 00:01:31.707
<v Efim Podvoiski>So, you, you already did this.</v>

00:01:34.427 --> 00:01:43.227
<v Efim Podvoiski>But you already discussed this, because, as far as I knew, and nothing moved, yeah, yeah, yeah.</v>

00:01:36.187 --> 00:01:38.427
<v Lena Zhukova>Yes, yes, I discussed it with Igor.</v>

00:01:40.587 --> 00:02:01.947
<v Lena Zhukova>No, no, no. I discussed it with Natalia and Igor, everything is in progress. And we also spent a lot of time trying to investigate these mysterious issues with mismatching assets. And we found the root because Fire Island games were developed first, like single games, and there are a lot of same names, like...</v>

00:01:44.427 --> 00:01:44.747
<v Michael Gottlieb>Yeah.</v>

00:02:01.987 --> 00:02:13.627
<v Lena Zhukova>Transition, for example, or big green talker. It's not specified that it's Larosa big green talker or Crescent City Karnava big green talker.</v>

00:02:11.787 --> 00:02:18.267
<v Val Levitan>So, it's a it's a it's a issue with the.</v>

00:02:19.627 --> 00:02:22.427
<v Val Levitan>Naming convention standards, right?</v>

00:02:25.787 --> 00:02:28.507
<v Lena Zhukova>And yeah, one one of the issue was this, yes.</v>

00:02:27.547 --> 00:02:32.267
<v Val Levitan>Or, or the lack, the lack of standards for naming convention, right?</v>

00:02:33.027 --> 00:02:38.907
<v Lena Zhukova>No, because, uh, yeah, because it is, uh, uh...</v>

00:02:33.307 --> 00:02:34.907
<v Val Levitan>There's not no standard.</v>

00:02:40.267 --> 00:02:52.987
<v Lena Zhukova>Product was changed, we are reusing, we are reusing assets from a single games products for FireEyes Link, and we...</v>

00:02:52.347 --> 00:02:54.947
<v Val Levitan>Let's just, let's just, let's just pause. Hold on a second.</v>

00:02:56.827 --> 00:03:06.747
<v Val Levitan>In my mind, what you identified, that there is a, there is no standard for naming convention of the files.</v>

00:03:09.307 --> 00:03:11.227
<v Val Levitan>Am I correct or am I wrong?</v>

00:03:13.387 --> 00:03:15.307
<v Lena Zhukova>You are like...</v>

00:03:14.547 --> 00:03:17.067
<v Val Levitan>What's the root? What's the root issue?</v>

00:03:16.547 --> 00:03:37.627
<v Lena Zhukova>Like both, both, because for a single game release, it was it was not necessary, so it was like proper proper name like Big Wind, and and but for multi-game product, it was not a...</v>

00:03:29.067 --> 00:03:31.707
<v Val Levitan>I'm struggling. I'm struggling.</v>

00:03:36.987 --> 00:03:39.067
<v Michael Gottlieb>Right, okay, let me.</v>

00:03:37.747 --> 00:03:39.227
<v Lena Zhukova>Yeah, yeah, yeah.</v>

00:03:38.427 --> 00:03:41.227
<v Efim Podvoiski>Convention was there, but it was inadequate.</v>

00:03:41.307 --> 00:03:41.867
<v Lena Zhukova>Yes.</v>

00:03:41.347 --> 00:04:00.347
<v Michael Gottlieb>Yes, the naming convention was adequate and acceptable if it was just a single game release. Where we ran into trouble is we have multiple games in the umbrella and the naming conventions were not set up for that.</v>

00:04:01.307 --> 00:04:06.507
<v Lena Zhukova>They, they needed the, yeah, we needed the additional specification, additional.</v>

00:04:06.187 --> 00:04:06.587
<v Michael Gottlieb>Right.</v>

00:04:10.667 --> 00:04:12.507
<v Val Levitan>You will not like what I'm gonna say now.</v>

00:04:15.867 --> 00:04:21.467
<v Val Levitan>But I must just, I have to say, we gotta, we gotta get out from this attitude, OK?</v>

00:04:24.107 --> 00:04:31.467
<v Val Levitan>Let's identify the issue. Let's be honest what the issue is. Let's fix the root of the issue so we never run into it.</v>

00:04:32.387 --> 00:04:44.027
<v Lena Zhukova>It was done already, and we for the future, because we just start we just started to create multi multi-category products for the future, it will we will not run to this issue again.</v>

00:04:37.227 --> 00:04:40.507
<v Val Levitan>Let me okay. Okay, let me.</v>

00:04:45.707 --> 00:04:47.067
<v Val Levitan>Let's just review it, okay?</v>

00:04:48.027 --> 00:04:49.707
<v Val Levitan>So when you said it's done.</v>

00:04:51.387 --> 00:04:52.027
<v Val Levitan>Okay.</v>

00:04:53.387 --> 00:04:56.827
<v Val Levitan>So there is a standard, right? So you developed a new standard.</v>

00:04:57.187 --> 00:04:57.707
<v Lena Zhukova>Yes.</v>

00:04:58.747 --> 00:05:03.387
<v Val Levitan>Okay, and the standard is documented, so it's a document.</v>

00:05:03.947 --> 00:05:07.147
<v Lena Zhukova>No, it wasn't recommended. It was verbal agreement.</v>

00:05:09.387 --> 00:05:09.867
<v Val Levitan>No.</v>

00:05:15.107 --> 00:05:15.627
<v Val Levitan>Amazing!</v>

00:05:16.907 --> 00:05:20.667
<v Val Levitan>Now we have a verbal agreement. Finally, we have a verbal agreement.</v>

00:05:22.027 --> 00:05:25.067
<v Val Levitan>I cannot help myself but you just to be sarcastic.</v>

00:05:29.227 --> 00:05:32.107
<v Michael Gottlieb>This just happened within the last couple of days.</v>

00:05:33.387 --> 00:05:35.187
<v Val Levitan>No, it always had.</v>

00:05:35.427 --> 00:05:45.547
<v Michael Gottlieb>No, that's not true. It doesn't always happen. This has been the worst ******* development process I've ever had at JVL for one game release. It has been an absolute mess.</v>

00:05:43.227 --> 00:06:01.747
<v Val Levitan>No, no, no, I thought. No, it always happens. The standards are always agreed verbally. It becomes tribal knowledge. It carries through the company. And I have been trying to root it out for years.</v>

00:06:01.947 --> 00:06:03.067
<v Val Levitan>Now, for years.</v>

00:06:04.747 --> 00:06:14.267
<v Michael Gottlieb>I respectfully disagree with you because I have developed, we have developed well more than a dozen games prior to this point without this problem.</v>

00:06:05.307 --> 00:06:05.427
<v Val Levitan>You.</v>

00:06:15.707 --> 00:06:17.147
<v Michael Gottlieb>None of these problems.</v>

00:06:15.707 --> 00:06:22.267
<v Val Levitan>Yes, because, yes, because you kept your word. You all agreed, and you kept that word.</v>

00:06:23.627 --> 00:06:30.907
<v Val Levitan>And you kept that concept verbally, everybody knew it, and it was verbally kept.</v>

00:06:32.427 --> 00:06:39.787
<v Val Levitan>There's, unless I don't know, point me to a repository that lists the standards.</v>

00:06:46.347 --> 00:06:54.267
<v Val Levitan>If the repository doesn't exist, then it will be impossible to keep standards in the long time, in the long run.</v>

00:06:55.307 --> 00:06:55.787
<v Michael Gottlieb>Agreed.</v>

00:06:57.227 --> 00:06:57.787
<v Val Levitan>Okay.</v>

00:07:00.347 --> 00:07:12.587
<v Val Levitan>We've discussed this many times. I don't know if, Michael, you were part of this discussion or not, but there's no question that Lena will not deny the fact that we've discussed it many times.</v>

00:07:15.547 --> 00:07:16.907
<v Val Levitan>Do you agree with me, Lena?</v>

00:07:20.427 --> 00:07:23.227
<v Lena Zhukova>And we discussed it in general, but not.</v>

00:07:26.107 --> 00:07:26.827
<v Lena Zhukova>About.</v>

00:07:26.347 --> 00:07:41.707
<v Val Levitan>We agree that there will always be, we will start with developing standards. These standards will be written down and will become a part of a written repository of standards.</v>

00:07:42.027 --> 00:08:02.267
<v Lena Zhukova>Actually, we have this document for Omnia, for Nova, when we started to develop games in Omnia, like Fortune Football or Caiochi Omnia, but we don't have this document for...</v>

00:08:03.147 --> 00:08:27.267
<v Lena Zhukova>Rage Studio, and I, I don't think we need to spend time now to create creating the document if you, but of course, yeah, we we we can, we can, yeah, we we have now shortage of artists, so we in a big rush to finish this release after we finish this release next week, we can start start to start to do this for.</v>

00:08:24.427 --> 00:08:25.467
<v Val Levitan>I respectfully.</v>

00:08:27.307 --> 00:08:27.867
<v Val Levitan>Irish.</v>

00:08:27.707 --> 00:08:29.947
<v Lena Zhukova>Reach to you, if if it's needed.</v>

00:08:32.667 --> 00:08:33.867
<v Val Levitan>Are we saying that?</v>

00:08:35.867 --> 00:08:38.827
<v Val Levitan>The file naming convention will be different.</v>

00:08:39.707 --> 00:08:42.707
<v Val Levitan>For Nova versus Rage Studio.</v>

00:08:41.867 --> 00:08:42.427
<v Lena Zhukova>Yes.</v>

00:08:44.027 --> 00:08:44.987
<v Val Levitan>It will be different.</v>

00:08:45.267 --> 00:08:45.707
<v Lena Zhukova>Yes.</v>

00:08:46.187 --> 00:08:47.387
<v Val Levitan>Why will it be different?</v>

00:08:47.307 --> 00:08:48.587
<v Lena Zhukova>Because.</v>

00:08:53.067 --> 00:09:02.107
<v Lena Zhukova>So, like, we are going to have different type of assets and different type of structure. How are we going to store these assets?</v>

00:09:00.667 --> 00:09:04.147
<v Val Levitan>Like, like, explain, explain to me, I, I just don't get it.</v>

00:09:06.027 --> 00:09:16.587
<v Lena Zhukova>We are going to keep everything in GitHub. We have different structural folders and repositories. How we are going to keep it in GitHub.</v>

00:09:10.747 --> 00:09:13.747
<v Val Levitan>We can, we can still wick it.</v>

00:09:15.747 --> 00:09:25.627
<v Val Levitan>We can still, we can still keep everything in GitHub. Nothing's stopping us. Even in Rage Studio, we could still have standards in GitHub.</v>

00:09:27.947 --> 00:09:32.347
<v Lena Zhukova>I'm not talking about standards, I'm talking about structure of assets, how they are.</v>

00:09:33.147 --> 00:09:39.707
<v Val Levitan>I'm talking, I'm talking about, I'm talking about standards; we're discussing naming convention standards.</v>

00:09:40.427 --> 00:09:58.587
<v Lena Zhukova>And for now, I think if we are going to start to rename assets, it will cause like big problems for us because for now, like for some games, which assets we are reusing, we are just cutting this branches from already like done games and we have already some names if we will start to rename.</v>

00:09:59.027 --> 00:10:03.787
<v Lena Zhukova>In Rich Studio assets, we will have bigger problems than what we have now.</v>

00:10:02.587 --> 00:10:11.867
<v Michael Gottlieb>There's no, yes, okay, excuse me for an update. There's no reason to rename assets. This was a folder structure problem. We have addressed the folder structure.</v>

00:10:10.907 --> 00:10:16.187
<v Val Levitan>But the folder structure problem will continue until we develop standards.</v>

00:10:17.627 --> 00:10:25.547
<v Michael Gottlieb>We need to document what it is that Lena is articulating. So yes, let's please document what the folder structure should look like.</v>

00:10:24.427 --> 00:10:39.307
<v Val Levitan>What does it mean? This is this is this is this is a publicly correct statement, but what does it mean if you're not trying to be publicly correct? But just just lay it out to me in a plain plain English.</v>

00:10:40.747 --> 00:10:49.387
<v Michael Gottlieb>Well, from my perspective, it just means one confluence page that says folder default folder structure with the name of the folder.</v>

00:10:41.027 --> 00:10:41.987
<v Val Levitan>What does that mean?</v>

00:10:48.587 --> 00:10:52.187
<v Val Levitan>Why does it have to? Why does it have to be a confluence page?</v>

00:10:52.227 --> 00:11:04.667
<v Michael Gottlieb>It doesn't have to be, you asked me a question, I'm giving you an answer. It can be anything you want it to be. All it needs to be is an articulation of what the asset folder structure is, what the folders, what...</v>

00:11:03.547 --> 00:11:10.827
<v Lena Zhukova>I don't, I don't think it's such a great problem as we're trying to discuss now, because we just agreed, so...</v>

00:11:09.307 --> 00:11:16.907
<v Val Levitan>But it's a great problem because right now there was a set of screw-ups because it, because there wasn't proper naming convention, right?</v>

00:11:16.467 --> 00:11:40.987
<v Lena Zhukova>It was, no, it was just one problem which we run in because we started to do multi-category and multi-game product which we never did before. And some, and when we discovered this problem, only one decision was made. Now each like folder and each like export should contain like...</v>

00:11:41.387 --> 00:11:47.947
<v Lena Zhukova>unique game code names. That's it. It's only one simple decision and it will...</v>

00:11:42.747 --> 00:11:45.387
<v Val Levitan>Okay, it seems okay.</v>

00:11:48.827 --> 00:12:08.147
<v Val Levitan>It seems it seems like there is absolutely zero chance. I stand 0 chance of proving my point, 00. Like, you're totally missing the point, totally. And so I have a choice, either waste this meeting on an argument or just give up and continue.</v>

00:12:08.267 --> 00:12:20.907
<v Val Levitan>with the meeting. So I choose to continue with the meeting. 100% disagreed with you. Ridiculous statements. Bunch of silly, childish, ridiculous statements.</v>

00:12:22.187 --> 00:12:23.707
<v Val Levitan>Totally not professional.</v>

00:12:25.467 --> 00:12:27.947
<v Val Levitan>I choose not to continue. Let's move on.</v>

00:12:31.467 --> 00:12:31.947
<v Val Levitan>Give up.</v>

00:12:40.027 --> 00:12:51.787
<v Val Levitan>What's next? Okay, so we have naming convention misalignment, which caused wrong assets to be placed in.</v>

00:12:52.987 --> 00:12:56.827
<v Val Levitan>in the game. So we're now fixing this, right?</v>

00:12:57.787 --> 00:13:00.027
<v Lena Zhukova>It's already it's already fixed.</v>

00:12:57.827 --> 00:13:04.187
<v Michael Gottlieb>Yes, that was one one set of the ones it is already fixed. It's one set of bugs of many that we ran into.</v>

00:12:57.947 --> 00:12:58.747
<v Val Levitan>OK, so.</v>

00:13:04.907 --> 00:13:13.307
<v Val Levitan>But what else? I'm trying to, so we have a misalignment, naming misalignment, caused wrong file. What else?</v>

00:13:14.267 --> 00:13:16.267
<v Michael Gottlieb>There were audio bugs.</v>

00:13:17.067 --> 00:13:23.787
<v Val Levitan>So how, when you say audio bugs, it doesn't, it could be that a programmer.</v>

00:13:24.947 --> 00:13:29.627
<v Val Levitan>Cause the bug, it could be wrong audio file placed in.</v>

00:13:28.827 --> 00:13:37.707
<v Michael Gottlieb>Right, there were some instances where Vladimir had provided the wrong audio file. I got that address. There were other instances where the programmers made a mistake.</v>

00:13:36.747 --> 00:13:44.907
<v Val Levitan>So why, so why was the wrong file provided? Was it also because of naming conventions?</v>

00:13:46.907 --> 00:13:49.707
<v Michael Gottlieb>No, I think it was just a mistake.</v>

00:13:48.587 --> 00:13:49.147
<v Val Levitan>Stop.</v>

00:13:52.387 --> 00:13:59.867
<v Val Levitan>It was a mistake like what he provide boogie woogie instead of something else.</v>

00:14:00.027 --> 00:14:08.667
<v Michael Gottlieb>Yeah, he provided the wrong sound effect. The wrong sound effect was provided. We're getting incredibly granular here. All I'm saying is there were a handful of bugs.</v>

00:14:08.107 --> 00:14:14.267
<v Val Levitan>We're getting incredibly granular because I need to understand. There's no other way for me to understand.</v>

00:14:12.587 --> 00:14:12.987
<v Michael Gottlieb>Right.</v>

00:14:14.747 --> 00:14:32.427
<v Michael Gottlieb>Absolutely. So there were audio bugs related to Val, Vlad providing an incorrect sound file. There was an issue where Anton used the wrong sound file. And then there were a couple of instances where there are games that</v>

00:14:31.307 --> 00:14:35.307
<v Val Levitan>Why, why would, why would he use the wrong file?</v>

00:14:36.347 --> 00:14:45.467
<v Michael Gottlieb>That's an excellent question that I don't know the answer to. I don't know why in Rodeo Queen or in Rodeo Queen had music from La Rosa.</v>

00:14:47.547 --> 00:14:50.187
<v Val Levitan>But he he doesn't he his.</v>

00:14:51.787 --> 00:15:08.747
<v Val Levitan>He doesn't apply his ear to listen to a file. He takes a file that he gets from somewhere. He doesn't create the file. So it has to be given to him and it has to be placed in a certain, probably, I assume, place folder, drive.</v>

00:15:08.427 --> 00:15:09.467
<v Michael Gottlieb>Right, right.</v>

00:15:09.827 --> 00:15:13.867
<v Val Levitan>And then he takes that. So how is it?</v>

00:15:16.427 --> 00:15:19.307
<v Val Levitan>Has he been told to take this file?</v>

00:15:20.267 --> 00:15:24.267
<v Val Levitan>I can't imagine he's been told something and he's taken something else.</v>

00:15:24.587 --> 00:15:42.907
<v Michael Gottlieb>I can only theorize that this problem is an extension of the previous issue that we mentioned, where we were previously created. This is, let's be very specific. This is fiery ice, right? And let's say in Florida, we deployed Laura Rosa.</v>

00:15:43.387 --> 00:16:02.747
<v Michael Gottlieb>or, you know, Laura Rosa. That's one game. One game, one set of assets. It is contained, right? We are doing multiple fiery ice titles for these markets that we're doing multiple games. And somewhere in there, when they loaded everything up or</v>

00:16:02.867 --> 00:16:21.947
<v Michael Gottlieb>populated whatever they were populating, stuff got goofed around and switched around. We had the jackpot rush, jackpot rush. We did the game for Georgia and it said at any bet, done. And then Felipe said, I don't want this.</v>

00:16:22.387 --> 00:16:41.867
<v Michael Gottlieb>and the build said at any bet. And then when we go and do Georgia V3, I'm looking at Jackpot Rush and it says with max bet. So the only theory I can come up with is they grab the Florida non at any bet graphical asset and put it in there.</v>

00:16:41.947 --> 00:16:43.627
<v Michael Gottlieb>But it can't be a naming convention.</v>

00:16:42.467 --> 00:16:55.147
<v Val Levitan>What, what do you, what do you, what do you mean? They grabbed, so there is a developer who's being given a set of assets. This set of assets is supplied by...</v>

00:16:49.147 --> 00:16:49.547
<v Michael Gottlieb>Yes.</v>

00:16:51.947 --> 00:16:52.347
<v Michael Gottlieb>Right.</v>

00:16:56.507 --> 00:17:02.747
<v Val Levitan>Non-developer, so I assume it comes from Lena's department, my assumption, correct me.</v>

00:17:01.147 --> 00:17:18.907
<v Lena Zhukova>No, they decided they decided to cut a branch from already existed product and they cut it from different from wrong products. They did not ask me from what product to cut all Michael. They they they did not ask. They decided Irina decided with somebody else that we are going to cut it from Florida branch. That's it.</v>

00:17:14.907 --> 00:17:15.787
<v Val Levitan>Who, who are?</v>

00:17:22.107 --> 00:17:24.667
<v Lena Zhukova>Nobody asked me from Biratko.</v>

00:17:24.187 --> 00:17:26.987
<v Val Levitan>I, I need, I need to understand this. I apologize. I'm sorry.</v>

00:17:26.027 --> 00:17:37.787
<v Michael Gottlieb>Okay, let me take you through. I'll take you through it. Jackpot Rush. We finished Jackpot Rush at any bet for Georgia. The graphic.</v>

00:17:36.907 --> 00:17:55.627
<v Val Levitan>So sorry. I'm sorry. I want to go back to the branch. Sorry. They cut it from, they decided on themselves, for themselves, to cut it from some other branch. Please explain that. I'm struggling. I'm asking a question. I don't know. I'm learning.</v>

00:17:56.027 --> 00:18:15.467
<v Lena Zhukova>Then, since they we reusing resources from previous products, developers cutting to to start development, they cutting like base for their like future like development from some existing product and Irina, I don't know.</v>

00:18:01.147 --> 00:18:03.147
<v Val Levitan>Sorry, sorry.</v>

00:18:15.627 --> 00:18:25.307
<v Lena Zhukova>Probably now they they consult with developers, they decided from what product to to cut this branch, never with me.</v>

00:18:20.787 --> 00:18:23.227
<v Val Levitan>Well, most likely.</v>

00:18:26.907 --> 00:18:34.747
<v Val Levitan>And if, and if they would, so they should have consulted with you? Did you say you're saying they should have?</v>

00:18:31.947 --> 00:18:44.827
<v Lena Zhukova>No, I don't think so. Maybe sometimes maybe they should consult with me or Michael, because there are some situations like this, for example, like this jackpot rush with Anibal.</v>

00:18:38.267 --> 00:18:39.787
<v Val Levitan>Not so, you say?</v>

00:18:46.267 --> 00:18:48.507
<v Lena Zhukova>Or maybe it was just a genuine mistake.</v>

00:18:46.667 --> 00:18:47.147
<v Val Levitan>Sorry.</v>

00:18:50.267 --> 00:18:51.067
<v Val Levitan>Sorry.</v>

00:18:50.507 --> 00:18:51.387
<v Lena Zhukova>I don't know.</v>

00:18:52.827 --> 00:18:53.867
<v Val Levitan>Sorry, not clear.</v>

00:18:54.907 --> 00:18:56.987
<v Val Levitan>Are you, are you saying that?</v>

00:18:58.667 --> 00:19:04.787
<v Val Levitan>The starting point should have been consulted with you, correct? Do I understand you correct?</v>

00:19:03.787 --> 00:19:10.107
<v Lena Zhukova>Rather with Michael, rather with Michael and Juan, then with me, because there are some requirements for the...</v>

00:19:08.827 --> 00:19:16.027
<v Val Levitan>Well, why would they consult Juan? Like, what would Juan say? He does, he doesn't have, he doesn't have the line of branches.</v>

00:19:11.787 --> 00:19:26.227
<v Lena Zhukova>Because one is creating, because one is creating requirements, because one is creating requirements for the product, because one is VP product owner, VP product owner is creating backlog for the product and requirements for the product.</v>

00:19:19.307 --> 00:19:20.947
<v Val Levitan>But he doesn't know the bread.</v>

00:19:27.067 --> 00:19:47.227
<v Michael Gottlieb>And he's perfectly capable of saying, let's start with the known finished Georgia version of Jackpot Rush and integrate that into the larger Georgia V3 release that we're creating. To your question, in theory, they should not have had to ask us the question,</v>

00:19:47.467 --> 00:20:07.067
<v Michael Gottlieb>because we had a finished jackpot rush for Georgia. Why they went and took the Florida branch of jackpot rush and used that, I don't know. But if they had a reason or a theory as to why they needed to do that, then yes, they should have consulted Lena.</v>

00:20:07.307 --> 00:20:26.507
<v Michael Gottlieb>or I, and said, we need to start with the Florida version. What's the difference between the two? And we could have identified, well, the Georgia version says at any bet. So for God knows what reason, they grabbed Florida assets, and that's where we started from, and it created a bug.</v>

00:20:34.187 --> 00:20:44.747
<v Juan Martinez>I would disagree though, Lena. I don't even know where these file repositories are, you know, so I have no idea of the naming convention.</v>

00:20:44.067 --> 00:21:05.867
<v Lena Zhukova>No, I, I, I, I'm with you, Ivan. I'm just saying about requirements, so what they are using as a base for the future product, it should should be based on requirements and requirements are in, yeah, requirements are in Jira and Confluence, and in requirements it says, so it should be at any bed.</v>

00:20:49.747 --> 00:20:50.027
<v Juan Martinez>Sure.</v>

00:20:56.667 --> 00:20:56.787
<v Juan Martinez>Yeah.</v>

00:20:56.747 --> 00:20:58.827
<v Michael Gottlieb>And the requirements are documented.</v>

00:21:01.467 --> 00:21:01.947
<v Michael Gottlieb>Right.</v>

00:21:06.427 --> 00:21:06.827
<v Juan Martinez>Yes.</v>

00:21:06.587 --> 00:21:12.667
<v Michael Gottlieb>We literally named the ******* product AAB because it was at any bet, but...</v>

00:21:10.187 --> 00:21:10.427
<v Juan Martinez>Yeah.</v>

00:21:14.027 --> 00:21:34.747
<v Michael Gottlieb>Whatever, it is what it is. I don't anticipate these issues going forward because obviously we need to document all of this, but more importantly, we now have a template for how we're doing multi-game. And there's no reason, they're not going to go randomly grab something from Florida because that stuff is all obsolete now.</v>

00:21:35.947 --> 00:21:40.027
<v Michael Gottlieb>I don't know why they did it in the 1st place, but they did, and it created a lot of problems.</v>

00:21:46.387 --> 00:21:46.747
<v Michael Gottlieb>Martha?</v>

00:21:52.347 --> 00:22:01.627
<v Val Levitan>I don't think that this is how simply they just go out and grab without consulting. I mean,</v>

00:22:03.547 --> 00:22:04.507
<v Val Levitan>I don't think so.</v>

00:22:06.027 --> 00:22:07.707
<v Val Levitan>I, I, I don't see.</v>

00:22:11.987 --> 00:22:31.307
<v Val Levitan>There has to be something else which I'm trying to understand what it is. But I don't see simply mature people grabbing just in an abstract, you know, I'm just going to start from this branch or I'm just going to do this.</v>

00:22:16.827 --> 00:22:17.547
<v Efim Podvoiski>Maybe they had.</v>

00:22:32.027 --> 00:22:37.707
<v Michael Gottlieb>Of course there's a reason, we just don't know what it is. I'm not saying the guys didn't do it with a reason, I'm saying that...</v>

00:22:35.787 --> 00:22:40.747
<v Val Levitan>But, but, but, but it's important to understand the reason, for example.</v>

00:22:41.627 --> 00:22:47.507
<v Val Levitan>I now understand that there is an issue with the fact that we have no naming conventions.</v>

00:22:48.827 --> 00:22:50.107
<v Val Levitan>Standardized.</v>

00:22:50.987 --> 00:22:52.027
<v Val Levitan>Written down.</v>

00:22:53.147 --> 00:22:56.507
<v Val Levitan>something that we can constantly refer to.</v>

00:22:58.347 --> 00:23:08.587
<v Val Levitan>I mean, you, there is an agreement between in the department, there's an agreement, verbal agreement, from now on we're going to do this. But these agreements, they don't hold.</v>

00:23:09.547 --> 00:23:09.947
<v Michael Gottlieb>Agreed.</v>

00:23:09.667 --> 00:23:12.907
<v Val Levitan>People change, people forget, so there has to be you.</v>

00:23:13.987 --> 00:23:21.147
<v Val Levitan>A repository where all standards are written, and when there is a...</v>

00:23:22.307 --> 00:23:40.507
<v Val Levitan>file to be named. It cannot be named manually. It should probably be named through a reference by, you know, Claude. I would use that. I mean, that's, you know, I use my files that way. I mean, that's how I name my files.</v>

00:23:43.067 --> 00:23:54.027
<v Val Levitan>And if it would be properly agreed naming standards, then files randomly would not get used, you know, or sent in a in a.</v>

00:23:55.587 --> 00:23:57.067
<v Val Levitan>Yeah, you know.</v>

00:23:58.507 --> 00:23:59.307
<v Val Levitan>Incorrectly.</v>

00:24:00.427 --> 00:24:19.147
<v Val Levitan>But so I understand the I understand now the sound issue. I understand. Visual files incorrectly placed. I understand the source. Now I'm trying to understand the source for as Lena angrily.</v>

00:24:20.147 --> 00:24:21.467
<v Val Levitan>So determinedly.</v>

00:24:23.787 --> 00:24:30.027
<v Val Levitan>insisted that it was them taking the wrong starting point.</v>

00:24:31.787 --> 00:24:36.267
<v Michael Gottlieb>Of course it was, because we finished the product for Georgia that was correct. It was done.</v>

00:24:37.387 --> 00:24:39.467
<v Michael Gottlieb>I got angrier than she did last week.</v>

00:24:38.187 --> 00:24:46.987
<v Val Levitan>It could, could, could be, could be, but really hard for me to understand. Hard for me to believe, really.</v>

00:24:49.707 --> 00:24:52.507
<v Val Levitan>There has to be, there has to be something else.</v>

00:24:55.227 --> 00:24:56.187
<v Val Levitan>It's not such a...</v>

00:24:55.387 --> 00:24:55.867
<v Michael Gottlieb>Yes.</v>

00:24:58.667 --> 00:25:00.747
<v Val Levitan>I mean, these are, these are...</v>

00:25:02.267 --> 00:25:03.467
<v Val Levitan>Reasonable people.</v>

00:25:04.907 --> 00:25:06.587
<v Val Levitan>And, and knowledgeable people.</v>

00:25:08.027 --> 00:25:12.347
<v Val Levitan>They know, they know that if they take the starting point incorrectly, then...</v>

00:25:16.027 --> 00:25:19.027
<v Efim Podvoiski>Yeah, they probably had some reasons, and...</v>

00:25:18.347 --> 00:25:23.227
<v Val Levitan>I'm trying, I'm trying to get, I'm trying to understand what that issue was.</v>

00:25:25.787 --> 00:25:27.707
<v Lena Zhukova>Maybe because, maybe because...</v>

00:25:25.867 --> 00:25:35.387
<v Val Levitan>And I actually, I actually don't really care what, who is at fault. My goal is to determine that it never happens again.</v>

00:25:36.187 --> 00:25:54.187
<v Lena Zhukova>Maybe because Florida product was tested and Georgia was just like all assets were inserted, but it was never tested because we cancelled it at some point. That's probably why they decided to do it.</v>

00:25:41.147 --> 00:25:41.867
<v Val Levitan>Maybe him.</v>

00:25:56.587 --> 00:26:12.907
<v Juan Martinez>But even in the V2 version, there were some very bizarre, you know, the European currency was selected for jackpot rush. Why anything in the US would you be able to drag up that file? Makes no sense.</v>

00:25:56.667 --> 00:25:57.227
<v Val Levitan>Man.</v>

00:26:11.867 --> 00:26:13.067
<v Efim Podvoiski>Well, we lost Val.</v>

00:26:15.947 --> 00:26:25.107
<v Efim Podvoiski>I guess they had some reasons to do it, and then they forgot to make sure that everything is changed back to Anibal.</v>

00:26:32.107 --> 00:26:34.347
<v Michael Gottlieb>I'm going to run to the washroom. I'll be right back.</v>

00:27:48.107 --> 00:27:54.507
<v Val Levitan>And it's interesting if, if this, if they took an incorrect branch.</v>

00:27:55.947 --> 00:28:02.827
<v Val Levitan>What, what should have been, what should the guidance have been, and who should that guidance?</v>

00:28:04.347 --> 00:28:05.707
<v Val Levitan>Should have come from.</v>

00:28:08.027 --> 00:28:10.667
<v Val Levitan>Maybe that's the right question to ask.</v>

00:28:15.307 --> 00:28:18.587
<v Val Levitan>What should have been this? What should the starting point?</v>

00:28:19.507 --> 00:28:21.547
<v Val Levitan>What should have the starting point be?</v>

00:28:23.947 --> 00:28:33.547
<v Val Levitan>And who should have that guidance come from? Start from here. This is the starting point. You have to branch out here.</v>

00:28:34.587 --> 00:28:45.467
<v Val Levitan>And why would, and it's hard for me to imagine that, let's say, Irina or Pavel would make that decision. Maybe they did. Okay, maybe they did.</v>

00:28:46.267 --> 00:28:57.787
<v Val Levitan>So then they should know not to make this decision. And if they should know not to make this decision, who should then make this decision, what the starting point should be.</v>

00:28:59.547 --> 00:29:05.147
<v Val Levitan>So the fact that if it was them that should have made that decision.</v>

00:29:06.347 --> 00:29:08.347
<v Val Levitan>And they made it incorrectly.</v>

00:29:09.427 --> 00:29:16.667
<v Val Levitan>then what should have gone into making that decision? What considerations should have been made?</v>

00:29:20.507 --> 00:29:22.667
<v Val Levitan>This is, this is what I would like to get.</v>

00:29:25.227 --> 00:29:43.707
<v Juan Martinez>Well, I guess without understanding the containers they follow today, I'm not sure I can comment on that. Like once the family is created, let's just say Nebraska D2702, isn't that container, the all-inclusive or whatever,</v>

00:29:25.307 --> 00:29:26.107
<v Val Levitan>That would be.</v>

00:29:25.307 --> 00:29:27.787
<v Michael Gottlieb>The the the specification.</v>

00:29:43.947 --> 00:29:47.707
<v Juan Martinez>branches need to be filled to supply that product.</v>

00:29:50.347 --> 00:30:09.387
<v Michael Gottlieb>In theory, everything you're asking for, Val, exists and was mandated by the collective population of this information in JIRA. It is why the REQ gets generated. It is why we generate all of this documentation. And even if they...</v>

00:30:08.427 --> 00:30:26.107
<v Val Levitan>It's very, very possible, very possible. And very possible we don't know how to use it. But if we don't know how to use it, it doesn't help us. So do you know how to use it? Would you have known where to start? Teach us.</v>

00:30:11.947 --> 00:30:13.467
<v Michael Gottlieb>Right, it it it.</v>

00:30:19.307 --> 00:30:19.867
<v Michael Gottlieb>Agreed.</v>

00:30:26.987 --> 00:30:45.387
<v Michael Gottlieb>No, that's exactly the point that I'm making. I don't give a **** where they start. I'm not a programmer. That's not my responsibility. And I cannot tell them, oh, you're best off starting with this code base versus that code base. All I can say is we've had you guys do a product for Georgia.</v>

00:30:45.627 --> 00:31:04.347
<v Michael Gottlieb>We finish that product for Georgia. That is the final product I want in Georgia. As simple as that. And the fact that if they had to start with an earlier branch and change assets, so be it. That's perfectly fine. But the problem comes in is when they don't reference back to what it is we</v>

00:31:03.387 --> 00:31:06.187
<v Val Levitan>This is, this is not, this is not helpful.</v>

00:31:08.187 --> 00:31:08.827
<v Val Levitan>Not helpful.</v>

00:31:13.947 --> 00:31:15.707
<v Val Levitan>Michael, this is not helpful.</v>

00:31:16.187 --> 00:31:18.587
<v Michael Gottlieb>Okay, what is it you're suggesting then?</v>

00:31:19.627 --> 00:31:30.187
<v Val Levitan>I would like to understand how to properly make a decision in the future from which branch to start, assuming that they started from the wrong branch.</v>

00:31:32.107 --> 00:31:45.067
<v Val Levitan>It would be great for me to understand what methodology to use for making that decision, or what information, or how to make that decision, or where to find it.</v>

00:31:46.107 --> 00:31:53.307
<v Michael Gottlieb>That information will be in JIRA going forward, and I will specify for.</v>

00:31:52.827 --> 00:32:00.507
<v Val Levitan>I, I, I, I don't know how. I mean, I, I mean, I, I don't understand. Sorry, maybe it's me.</v>

00:32:01.707 --> 00:32:06.587
<v Efim Podvoiski>No, no, it's complicated. It's really complicated issue. It's really not that simple.</v>

00:32:02.027 --> 00:32:02.987
<v Val Levitan>I just don't get.</v>

00:32:06.107 --> 00:32:08.267
<v Lena Zhukova>No, I agree. It's not that simple.</v>

00:32:07.947 --> 00:32:30.707
<v Efim Podvoiski>And again, now Irina is here, but I make my guess, they made the decision, they made the decision that they thought was right, for some reason, they heard their reasons, but then people forgot to fix the assets. And in Michael's mind, these assets are already there, but they are not.</v>

00:32:26.907 --> 00:32:29.547
<v Val Levitan>I, I, there is not, but...</v>

00:32:31.387 --> 00:32:40.307
<v Val Levitan>But for God is just the wrong concept. They shouldn't be forgetting that it should be determined.</v>

00:32:41.547 --> 00:32:46.907
<v Val Levitan>Right, because if you rely on your memory, you're bound to forget something, right?</v>

00:32:44.907 --> 00:32:45.267
<v Efim Podvoiski>Yeah.</v>

00:32:47.227 --> 00:32:52.507
<v Lena Zhukova>But it was determined in the requirements. It was determined requirements that it should be a tenure bit.</v>

00:32:47.307 --> 00:32:50.627
<v Efim Podvoiski>You, you, there is no way there isn't.</v>

00:32:51.947 --> 00:32:53.707
<v Efim Podvoiski>Yes, yes, yes.</v>

00:32:54.987 --> 00:32:57.147
<v Val Levitan>Well, why don't we ask Irina?</v>

00:32:57.627 --> 00:32:58.027
<v Efim Podvoiski>Yes.</v>

00:32:59.867 --> 00:33:01.787
<v Val Levitan>So, let me let me switch to Russian.</v>

00:33:00.587 --> 00:33:01.507
<v Irina Shishko>Yeah.</v>

00:33:18.747 --> 00:33:38.307
<v Irina Shishko>No, I wish not. It do what we did. We did release Nova. Release. No product. South Dakota. No, South Dakota. South Dakota.</v>

00:33:56.867 --> 00:33:58.707
<v Irina Shishko>Yes.</v>

00:34:01.267 --> 00:34:01.827
<v Val Levitan>So.</v>

00:34:04.147 --> 00:34:06.627
<v Val Levitan>In this case, in this release, for...</v>

00:34:07.827 --> 00:34:11.267
<v Val Levitan>Version 3, Georgia Quam Version 3.</v>

00:34:11.907 --> 00:34:12.307
<v Irina Shishko>The.</v>

00:34:13.587 --> 00:34:25.667
<v Val Levitan>The game, particularly game, which one? Jackpot Rush. Jackpot Rush. Where did you, where did you cut this from?</v>

00:34:18.787 --> 00:34:22.987
<v Lena Zhukova>Just put us.</v>

00:34:36.307 --> 00:34:36.827
<v Irina Shishko>Good.</v>

00:34:37.907 --> 00:34:46.347
<v Efim Podvoiski>Yeah, sorry Val, I think you asked the wrong question. What you used to start Zakharenkov?</v>

00:34:41.987 --> 00:34:42.867
<v Val Levitan>Okay, sorry.</v>

00:35:03.667 --> 00:35:04.067
<v Irina Shishko>No.</v>

00:35:13.907 --> 00:35:18.307
<v Lena Zhukova>If you taste food, it is.</v>

00:35:27.347 --> 00:35:29.587
<v Irina Shishko>In your.</v>

00:35:31.507 --> 00:35:37.107
<v Lena Zhukova>Yeah, that it's just.</v>

00:35:46.387 --> 00:35:50.987
<v Lena Zhukova>I need at any bed.</v>

00:35:54.147 --> 00:35:54.547
<v Irina Shishko>On.</v>

00:35:58.627 --> 00:36:05.907
<v Lena Zhukova>I need.</v>

00:36:02.307 --> 00:36:03.267
<v Irina Shishko>Yeah, yeah, yeah, with the...</v>

00:36:08.947 --> 00:36:11.907
<v Irina Shishko>But you want to switch you less duck down.</v>

00:36:43.027 --> 00:36:43.467
<v Irina Shishko>Madrid.</v>

00:36:44.867 --> 00:36:54.907
<v Val Levitan>Why, why in June? We're now in September, and you're saying that what, what relationship does it have in June?</v>

00:36:56.547 --> 00:36:59.067
<v Val Levitan>to now September. I'm confused.</v>

00:37:07.347 --> 00:37:13.027
<v Val Levitan>But why would Michael bring up June issue right now in September? I don't understand.</v>

00:37:12.147 --> 00:37:15.387
<v Lena Zhukova>Just as an example, it was just an example.</v>

00:37:14.627 --> 00:37:19.467
<v Val Levitan>But, but it's not, but it's an example for June, not for September, no.</v>

00:37:21.027 --> 00:37:22.787
<v Lena Zhukova>Right, it was, it, it, it was.</v>

00:37:21.107 --> 00:37:26.867
<v Val Levitan>Wait, but I, but I'm asking, I'm asking why do we have such a delay?</v>

00:37:28.787 --> 00:37:30.147
<v Val Levitan>Right now, in September.</v>

00:37:31.987 --> 00:37:35.667
<v Val Levitan>And you say that we started from the wrong version.</v>

00:37:37.187 --> 00:37:37.507
<v Lena Zhukova>Oh.</v>

00:37:37.587 --> 00:37:37.867
<v Val Levitan>No.</v>

00:37:38.867 --> 00:37:40.547
<v Lena Zhukova>Michael Gidner says.</v>

00:37:39.267 --> 00:37:39.987
<v Irina Shishko>Yeah, to.</v>

00:37:43.587 --> 00:37:45.187
<v Michael Gottlieb>I said there was a graph I...</v>

00:37:49.187 --> 00:37:52.067
<v Juan Martinez>Are we talking about the picture Michael posted in the chat?</v>

00:37:51.907 --> 00:37:52.947
<v Michael Gottlieb>Yes, yes.</v>

00:37:53.507 --> 00:38:05.187
<v Juan Martinez>Yeah, so that says win at max bet, which is not what's called for for Georgia, and this made it out into the V2 software that's live in the field.</v>

00:38:00.427 --> 00:38:01.827
<v Val Levitan>But we're not, but...</v>

00:38:00.627 --> 00:38:00.947
<v Michael Gottlieb>Right.</v>

00:38:05.987 --> 00:38:15.187
<v Val Levitan>But we now when we now understand that it came in June and it was fixed post Val, so this was probably fixed already for this trade show.</v>

00:38:06.067 --> 00:38:07.267
<v Juan Martinez>and will be fixed.</v>

00:38:16.307 --> 00:38:25.667
<v Juan Martinez>No, it was the bug was present in the trade show, and the 10 machines on trial for V2 have this same language in it.</v>

00:38:30.307 --> 00:38:35.187
<v Juan Martinez>The Georgia is not at max bet. Georgia is at any bet.</v>

00:38:40.867 --> 00:38:41.427
<v Val Levitan>Okay.</v>

00:38:43.427 --> 00:38:46.627
<v Val Levitan>All right, thanks, Irina. Sorry to have disturbed you.</v>

00:38:45.667 --> 00:38:57.507
<v Juan Martinez>Okay, but real quick though, does any, for my sake, what is a branch? Is it a structured Windows folder that says graphics, that says toppers, that says document?</v>

00:38:56.787 --> 00:38:57.107
<v Efim Podvoiski>No.</v>

00:38:58.587 --> 00:39:00.547
<v Juan Martinez>What, what, what is a branch?</v>

00:39:02.867 --> 00:39:14.427
<v Efim Podvoiski>It's it's it's branches are in SVSV and it's it's in version can control software and this is a.</v>

00:39:08.387 --> 00:39:08.867
<v Irina Shishko>All right.</v>

00:39:12.467 --> 00:39:12.867
<v Juan Martinez>Okarak.</v>

00:39:13.987 --> 00:39:14.027
<v Irina Shishko>Uhh...</v>

00:39:15.827 --> 00:39:16.307
<v Efim Podvoiski>Yes, sir.</v>

00:39:16.067 --> 00:39:22.667
<v Irina Shishko>Is really.</v>

00:39:24.747 --> 00:39:26.707
<v Irina Shishko>What?</v>

00:39:25.107 --> 00:39:31.667
<v Lena Zhukova>Yes, it was just casual guys, should be Brian.</v>

00:39:31.227 --> 00:39:34.947
<v Irina Shishko>Is this branch?</v>

00:39:35.587 --> 00:39:42.507
<v Lena Zhukova>developer in a branch.</v>

00:39:45.187 --> 00:40:05.027
<v Lena Zhukova>What is branch? I didn't touch country. Branches South Dakota.</v>

00:39:55.907 --> 00:39:57.107
<v Irina Shishko>No.</v>

00:39:58.227 --> 00:39:59.227
<v Irina Shishko>The data.</v>

00:40:00.627 --> 00:40:01.507
<v Irina Shishko>Saita Pavel.</v>

00:40:04.787 --> 00:40:06.387
<v Irina Shishko>I didn't.</v>

00:40:05.107 --> 00:40:08.227
<v Lena Zhukova>Come right, so that the I think that's it from that.</v>

00:40:08.307 --> 00:40:09.827
<v Irina Shishko>Tagdasha Pavel.</v>

00:40:17.027 --> 00:40:18.787
<v Efim Podvoiski>So, in the...</v>

00:40:19.987 --> 00:40:38.547
<v Efim Podvoiski>source control tool, like SVM, you have branches in which different developers work on the same branch and then can share files and commit files into the same place so other people can use the same files and they build from specific snapshot.</v>

00:40:39.827 --> 00:40:40.547
<v Efim Podvoiski>And the...</v>

00:40:41.907 --> 00:40:43.507
<v Efim Podvoiski>The whole codebase is...</v>

00:40:45.027 --> 00:40:48.707
<v Efim Podvoiski>Has several branches, because when you develop some product you want.</v>

00:40:49.827 --> 00:41:10.707
<v Efim Podvoiski>changes that made for other products or for improvement in the main going forward, they don't contaminate the current development. So, but because we have different products and they're going different ways and we return to some products and sometimes we switch product and move it into another place.</v>

00:41:11.387 --> 00:41:21.907
<v Efim Podvoiski>In another jurisdiction, you have to make a decision from what, which is a snapshot from where you start your product, and this is, and that's the branch.</v>

00:41:22.947 --> 00:41:41.427
<v Efim Podvoiski>And sometimes it's not trivial because you have similar product, but very old code base with old bugs and no features in data center, for example, or something like this. And you have newer products, but different games and what to choose.</v>

00:41:43.107 --> 00:41:47.667
<v Efim Podvoiski>It's not it's not always very clear where to start.</v>

00:41:51.347 --> 00:41:59.867
<v Lena Zhukova>Which branch, the closest branch to the current requirements of the product we are going to develop?</v>

00:41:57.027 --> 00:41:57.587
<v Efim Podvoiski>Yes.</v>

00:42:19.027 --> 00:42:22.627
<v Val Levitan>So, we've determined two types of...</v>

00:42:24.067 --> 00:42:25.347
<v Val Levitan>Two type of issues.</v>

00:42:27.027 --> 00:42:28.627
<v Val Levitan>I mean, at least in my mind.</v>

00:42:31.107 --> 00:42:32.547
<v Val Levitan>One is.</v>

00:42:33.627 --> 00:42:37.187
<v Val Levitan>The absence of a written referable.</v>

00:42:39.267 --> 00:42:41.187
<v Val Levitan>File naming convention.</v>

00:42:43.027 --> 00:42:48.307
<v Val Levitan>And the second one is an issue that I still didn't get fully.</v>

00:42:49.427 --> 00:42:51.427
<v Val Levitan>Still didn't fully understand, but...</v>

00:42:55.747 --> 00:42:57.347
<v Val Levitan>Where to start?</v>

00:42:59.227 --> 00:43:01.747
<v Val Levitan>Where to branch off when we make?</v>

00:43:03.347 --> 00:43:04.307
<v Val Levitan>A new beginning.</v>

00:43:05.587 --> 00:43:06.467
<v Val Levitan>A new release.</v>

00:43:10.547 --> 00:43:16.387
<v Val Levitan>That is a loaded question. Okay, so, and what else? What were the other issues?</v>

00:43:18.227 --> 00:43:33.747
<v Lena Zhukova>The other issue is that we need to finish updating graphics for new game, which we decided that it's going to be a benefit for this product if we will update the graphics for Queen of Luxon. So it's not finished here.</v>

00:43:35.067 --> 00:43:37.747
<v Efim Podvoiski>In addition, we decided last Friday to add this.</v>

00:43:39.987 --> 00:43:41.027
<v Efim Podvoiski>Not sure.</v>

00:43:41.067 --> 00:43:43.027
<v Michael Gottlieb>Touch expanded touch to the nudge arrows.</v>

00:43:41.427 --> 00:43:41.907
<v Lena Zhukova>Yeah.</v>

00:43:42.787 --> 00:43:45.187
<v Efim Podvoiski>Yeah, and there were some just...</v>

00:43:46.067 --> 00:43:49.107
<v Efim Podvoiski>Just bugs, just since they're not working.</v>

00:43:50.187 --> 00:43:51.107
<v Efim Podvoiski>Samsung Frolov.</v>

00:43:52.387 --> 00:43:57.987
<v Efim Podvoiski>The software crashed. For example, there was, there is a bug that...</v>

00:43:57.027 --> 00:44:00.467
<v Val Levitan>But the bugs, but my understanding that bugs were...</v>

00:44:01.747 --> 00:44:06.067
<v Val Levitan>would have been fixed that would have wouldn't have taken us to September 10th.</v>

00:44:10.147 --> 00:44:13.347
<v Val Levitan>So, I'm reading between the lines here.</v>

00:44:14.787 --> 00:44:17.587
<v Val Levitan>It seems to me that the longest...</v>

00:44:19.267 --> 00:44:20.227
<v Val Levitan>Duration.</v>

00:44:21.747 --> 00:44:28.067
<v Val Levitan>that pushed us to September 10th is the change of graphics for Quino Luxor.</v>

00:44:30.147 --> 00:44:31.027
<v Lena Zhukova>I don't know.</v>

00:44:30.227 --> 00:44:32.467
<v Val Levitan>I'm reading, I'm reading between the lines.</v>

00:44:32.867 --> 00:44:38.947
<v Lena Zhukova>Irina, is everything else except Queen of Luxor fully ready for submission?</v>

00:44:39.827 --> 00:44:46.227
<v Val Levitan>I'm not saying that it's fully ready. I'm not saying that it's fully ready. I'm saying that it would not have taken us to September 10th.</v>

00:44:40.787 --> 00:44:41.147
<v Irina Shishko>All right.</v>

00:44:48.427 --> 00:44:51.507
<v Val Levitan>For example, bugs we could fix very quickly.</v>

00:44:52.787 --> 00:44:53.667
<v Efim Podvoiski>Not to awesome.</v>

00:44:54.267 --> 00:44:55.347
<v Val Levitan>The sorry.</v>

00:44:55.987 --> 00:44:58.147
<v Efim Podvoiski>Not all of them are some are some are nasty.</v>

00:44:58.947 --> 00:45:05.187
<v Val Levitan>All right. The naming convention, the substitution of files.</v>

00:45:07.027 --> 00:45:11.747
<v Val Levitan>Reading between the lines, it seems that it has already been fixed.</v>

00:45:13.107 --> 00:45:15.347
<v Val Levitan>I'm reading between the lines. Don't kill me.</v>

00:45:18.627 --> 00:45:20.227
<v Val Levitan>Am I correct here or not?</v>

00:45:20.467 --> 00:45:36.707
<v Michael Gottlieb>Yes, just in, okay, from my perspective, just in the last couple of days of this week, I have finally gotten a Giorgi V3 build that has settled down and is actually behaving the way that it's supposed to.</v>

00:45:37.107 --> 00:45:53.107
<v Val Levitan>Michael, I fully respect this. I understand this. And it will, we all, we need to step back and acknowledge the fact that Rage, the development environment for Rage, is not conducive to</v>

00:45:40.467 --> 00:45:40.867
<v Michael Gottlieb>Right.</v>

00:45:55.907 --> 00:45:57.667
<v Val Levitan>Effective output.</v>

00:46:00.627 --> 00:46:05.347
<v Val Levitan>And for as long as we continue working on rage, we will continue.</v>

00:46:08.147 --> 00:46:10.147
<v Val Levitan>The aggravation will continue.</v>

00:46:10.947 --> 00:46:15.907
<v Val Levitan>But not not the naming convention that could have been prevented.</v>

00:46:18.147 --> 00:46:19.027
<v Val Levitan>Very easily.</v>

00:46:23.347 --> 00:46:27.187
<v Val Levitan>So that the naming convention could have been easily prevented.</v>

00:46:30.267 --> 00:46:31.347
<v Val Levitan>Drenching.</v>

00:46:32.147 --> 00:46:34.867
<v Val Levitan>I still, I don't know.</v>

00:46:35.827 --> 00:46:39.587
<v Val Levitan>Bugs, I think they're more or less they're fixed.</v>

00:46:40.387 --> 00:46:47.827
<v Val Levitan>I'm going to revert to Irina on this or maybe it's another day or two. So the fact that we are pushed into September.</v>

00:46:48.907 --> 00:46:49.947
<v Val Levitan>I'm repeating myself.</v>

00:46:50.867 --> 00:46:53.587
<v Val Levitan>It seems to me I'm reading between the lines.</v>

00:46:54.467 --> 00:46:59.267
<v Val Levitan>that this is a subject of graphical redesign for Queen of Luxor.</v>

00:47:00.387 --> 00:47:01.667
<v Val Levitan>So, let me part.</v>

00:47:00.627 --> 00:47:01.267
<v Lena Zhukova>Yes.</v>

00:47:02.707 --> 00:47:17.667
<v Lena Zhukova>Yes, and it was a decision which we made. We knew that it will take us extra time, and this game is ready. We can submit this product without this new graphics, but we decided we decided to update it.</v>

00:47:11.107 --> 00:47:12.307
<v Val Levitan>I think not.</v>

00:47:14.627 --> 00:47:15.587
<v Val Levitan>Sorry, was I?</v>

00:47:19.027 --> 00:47:24.547
<v Val Levitan>OK, great. Please remind me, was I part of this decision? Could have been, because I'm maybe I'm...</v>

00:47:23.667 --> 00:47:25.987
<v Michael Gottlieb>Yes, absolutely. Absolutely.</v>

00:47:24.827 --> 00:47:25.267
<v Juan Martinez>Yes.</v>

00:47:26.867 --> 00:47:30.467
<v Val Levitan>I was part of the decision to push it to September 10th.</v>

00:47:27.107 --> 00:47:27.827
<v Michael Gottlieb>That being.</v>

00:47:31.267 --> 00:47:36.067
<v Michael Gottlieb>No, the September 10th date wasn't discussed. It was the fact that we wanted to add Queen of Luxor.</v>

00:47:38.947 --> 00:47:43.267
<v Michael Gottlieb>And we also brought up there were a number of bugs that needed to be fixed post show.</v>

00:47:45.187 --> 00:47:59.427
<v Val Levitan>But it was, and I remember discussing it, but it was kind of a, in one sentence, generalized, well, we need to fix bugs. We need to, we need to finish Queen of Luxor, but there has never been really.</v>

00:47:53.827 --> 00:47:55.187
<v Michael Gottlieb>And finish Queen of Luxor.</v>

00:48:00.627 --> 00:48:08.147
<v Val Levitan>A statement, then it will push us to September 10th, and from September 10th, we probably need...</v>

00:48:11.667 --> 00:48:17.107
<v Val Levitan>I assume there might be other bugs, give or take another day or so.</v>

00:48:18.787 --> 00:48:20.227
<v Val Levitan>Five days for.</v>

00:48:22.067 --> 00:48:26.467
<v Val Levitan>Eclipse, so we're now somewhere in closer to the 20th.</v>

00:48:27.507 --> 00:48:28.947
<v Val Levitan>September 20th release.</v>

00:48:31.587 --> 00:48:32.547
<v Val Levitan>Irina.</v>

00:48:33.907 --> 00:48:39.347
<v Val Levitan>If we do, do we still have bugs or have the bugs been were the bugs fixed already?</v>

00:49:10.947 --> 00:49:19.587
<v Lena Zhukova>But we still need to implement this wider area for not just. It's a separate task.</v>

00:49:32.307 --> 00:49:40.227
<v Lena Zhukova>And it was it was a requirement from Val to change animation of the force, and we are working on this.</v>

00:49:41.187 --> 00:49:43.267
<v Val Levitan>Did you guys see the animation on the horse?</v>

00:49:44.187 --> 00:49:51.587
<v Lena Zhukova>Of course you saw it, we approved it, it was already like released and everybody liked it.</v>

00:49:52.227 --> 00:49:52.787
<v Val Levitan>No way.</v>

00:49:56.467 --> 00:49:59.027
<v Val Levitan>No way. It's impossible to like.</v>

00:50:00.387 --> 00:50:00.787
<v Lena Zhukova>Wow.</v>

00:50:00.627 --> 00:50:02.307
<v Val Levitan>No way, no way you like that.</v>

00:50:03.747 --> 00:50:04.227
<v Lena Zhukova>Okay.</v>

00:50:06.227 --> 00:50:09.827
<v Val Levitan>The horse doesn't kick naturally.</v>

00:50:11.187 --> 00:50:18.347
<v Val Levitan>I mean, it doesn't land on on its on the on the back back legs, you know, doesn't land.</v>

00:50:20.307 --> 00:50:28.387
<v Val Levitan>It needs to, it needs to jump and kick, jump and kick, but it needs to land. The physics is wrong.</v>

00:50:31.267 --> 00:50:34.787
<v Val Levitan>The motion of the horses run, there's no way you could like it, just...</v>

00:50:45.427 --> 00:50:49.187
<v Lena Zhukova>So, we are working on doing this animation.</v>

00:50:49.427 --> 00:50:50.467
<v Val Levitan>Okay, so...</v>

00:50:52.307 --> 00:50:58.067
<v Val Levitan>But you're reworking the animation. Who's reworking this animation?</v>

00:50:58.147 --> 00:50:59.027
<v Lena Zhukova>Anastasiya.</v>

00:51:00.387 --> 00:51:01.027
<v Val Levitan>Okay.</v>

00:51:02.147 --> 00:51:04.467
<v Val Levitan>and who is working on the...</v>

00:51:05.787 --> 00:51:06.947
<v Val Levitan>On Queen of Luxor.</v>

00:51:07.267 --> 00:51:26.227
<v Lena Zhukova>Everybody else. All artists in our department now are working to finish this game. Anastasiya is also doing some part because she needs to finish her tasks on Queen of Luxor and then she will do this course as well.</v>

00:51:11.867 --> 00:51:11.987
<v Val Levitan>Yeah.</v>

00:51:15.027 --> 00:51:18.227
<v Val Levitan>Not, not on a station, not on a station.</v>

00:51:26.467 --> 00:51:30.067
<v Lena Zhukova>So, she is to enforce them, some tasks, something of.</v>

00:51:27.827 --> 00:51:28.547
<v Val Levitan>Okay.</v>

00:51:30.707 --> 00:51:33.267
<v Val Levitan>So, if it wasn't for Queen of Log 4.</v>

00:51:36.227 --> 00:51:38.467
<v Val Levitan>We could have gone into...</v>

00:51:39.947 --> 00:51:43.587
<v Val Levitan>approval either today or Monday.</v>

00:51:47.347 --> 00:51:48.947
<v Val Levitan>That's the honest truth.</v>

00:51:49.987 --> 00:51:52.467
<v Michael Gottlieb>Oh, it's ready to submit. It's ready to submit right now.</v>

00:51:54.147 --> 00:51:55.427
<v Michael Gottlieb>There aren't any more bugs.</v>

00:51:55.027 --> 00:52:00.227
<v Efim Podvoiski>If you did, but we're not doing at all that it it started.</v>

00:51:55.227 --> 00:51:55.667
<v Juan Martinez>So...</v>

00:51:55.347 --> 00:51:57.667
<v Val Levitan>If so, so.</v>

00:51:59.107 --> 00:52:02.507
<v Val Levitan>So, all, all, so all bugs are finished.</v>

00:52:03.427 --> 00:52:04.067
<v Val Levitan>Fixed.</v>

00:52:05.427 --> 00:52:15.187
<v Val Levitan>There is an issue with horse animation in Rodeo Spencer, Rodeo Queen, I don't remember the name.</v>

00:52:14.627 --> 00:52:15.667
<v Lena Zhukova>Roger Spence.</v>

00:52:15.827 --> 00:52:16.547
<v Michael Gottlieb>Producements.</v>

00:52:16.067 --> 00:52:27.267
<v Val Levitan>and Rodionov Spins, but Rodionov Spins animation is worked by Anastasiya, was also working on Queen of Luxor partially.</v>

00:52:28.627 --> 00:52:32.947
<v Val Levitan>So, she spreads herself in between the two projects.</v>

00:52:35.347 --> 00:52:37.027
<v Val Levitan>But everything else is fixed.</v>

00:52:37.987 --> 00:52:43.347
<v Juan Martinez>Yeah, but got based on V2, Felipe found several problems.</v>

00:52:44.307 --> 00:53:00.947
<v Juan Martinez>at the show or after we got it from Eclipse. So wouldn't it be wise to get him the ISO build and test the full machine with Topper and everything before we send it to Eclipse? That's an extra day or two.</v>

00:53:02.307 --> 00:53:12.787
<v Val Levitan>Yes, extra day or two, I fully understand. So we would have submitted today or Monday. That's exactly what I said. Had it not been for Quino Luxor.</v>

00:53:13.347 --> 00:53:15.987
<v Michael Gottlieb>Felipe has an ISO. He's testing an ISO one.</v>

00:53:16.267 --> 00:53:18.547
<v Juan Martinez>No, he does not have an iPhone.</v>

00:53:17.667 --> 00:53:22.867
<v Val Levitan>Felipe would Felipe would have received an ISO today or Monday.</v>

00:53:24.067 --> 00:53:28.707
<v Val Levitan>had it not been for Queen of Luxor. That's the statement, that's the final statement.</v>

00:53:34.627 --> 00:53:35.267
<v Val Levitan>Okarak.</v>

00:53:36.147 --> 00:53:38.147
<v Val Levitan>Clear, now I got the whole story.</v>

00:53:45.987 --> 00:53:46.707
<v Val Levitan>Okay.</v>

00:53:47.267 --> 00:53:56.987
<v Irina Shishko>The the release of chromia.</v>

00:53:55.187 --> 00:53:55.827
<v Val Levitan>Yes.</v>

00:54:04.227 --> 00:54:07.907
<v Val Levitan>Okay, Irina, clear. Thank you. It's clear.</v>

00:54:11.827 --> 00:54:14.227
<v Val Levitan>Thank you very much. Good night. Good night.</v>

00:54:12.227 --> 00:54:13.387
<v Juan Martinez>Have a good weekend.</v>

00:54:12.947 --> 00:54:13.667
<v Lena Zhukova>Are super.</v>

00:54:14.507 --> 00:54:15.947
<v Efim Podvoiski>I also had no.</v>

00:54:15.507 --> 00:54:16.387
<v Val Levitan>Goodnight, bye.</v>

00:54:16.067 --> 00:54:16.867
<v Lena Zhukova>No.</v>

00:54:16.507 --> 00:54:17.267
<v Irina Shishko>The hospital.</v>

00:54:18.227 --> 00:54:19.587
<v Irina Shishko>Spicy.</v>

00:54:20.227 --> 00:54:20.947
<v Val Levitan>Thank you, bye.</v>

00:54:23.147 --> 00:54:27.907
<v Val Levitan>Okay, gentlemen and ladies, I understand this part.</v>

00:54:31.747 --> 00:54:32.387
<v Val Levitan>Um...</v>

00:54:35.787 --> 00:54:38.947
<v Val Levitan>What else on our agenda? What do we have to review?</v>

00:54:39.707 --> 00:54:46.547
<v Val Levitan>Should we review next schedule, what's upcoming, your priorities? Do you guys?</v>

00:54:45.507 --> 00:55:02.147
<v Michael Gottlieb>Well, okay, yes. I would say the first question is, where does this new Georgia skill initiative that you brought up at the beginning of the week, where does that reside? Are we pursuing it? Are we using it on hold?</v>

00:55:01.507 --> 00:55:06.067
<v Val Levitan>No, it's on hold. I wanted to understand.</v>

00:55:07.587 --> 00:55:18.387
<v Val Levitan>If we were to move forward, what may come out from it, but it's still on hold. I need to understand, I need to understand if we will have a customer support.</v>

00:55:13.587 --> 00:55:14.227
<v Michael Gottlieb>Okay.</v>

00:55:20.067 --> 00:55:29.427
<v Val Levitan>Sorry, customer commitment to purchase. And I still do not have it. But next week I'm meeting with the CEO.</v>

00:55:26.947 --> 00:55:27.507
<v Michael Gottlieb>Okay.</v>

00:55:31.907 --> 00:55:34.227
<v Val Levitan>I will iron this out.</v>

00:55:35.827 --> 00:55:54.707
<v Michael Gottlieb>Okay, well, from a math standpoint, Efim and I still have some specific questions that we need to get resolved via getting more game footage. We need to see free spins and that winning streak feature that they have, you know, and not on autoplay.</v>

00:55:55.667 --> 00:55:59.507
<v Michael Gottlieb>We don't need that right now. If we're still in an evaluation stage, that's fine.</v>

00:55:56.387 --> 00:55:56.867
<v Val Levitan>What?</v>

00:55:59.267 --> 00:56:02.547
<v Val Levitan>You want, you wanna see the actual racking?</v>

00:56:03.587 --> 00:56:12.947
<v Michael Gottlieb>Well, the racking and free spins specifically. We need to see free spins, we need to see how free spins behave, and then they have a...</v>

00:56:12.467 --> 00:56:16.467
<v Val Levitan>I will, I will go and I will, I will record it for you.</v>

00:56:15.667 --> 00:56:17.507
<v Efim Podvoiski>And hot and hot drink.</v>

00:56:17.507 --> 00:56:18.547
<v Michael Gottlieb>and hot streak.</v>

00:56:18.787 --> 00:56:24.227
<v Efim Podvoiski>Yeah, and we try to play on the highest bet with and without auto play.</v>

00:56:24.867 --> 00:56:31.427
<v Michael Gottlieb>Right. No autoplay, we need to see hot streak, we need to see racking, and we need to see free spins.</v>

00:56:32.467 --> 00:56:35.987
<v Val Levitan>Okay, I will. I will record this for you.</v>

00:56:33.507 --> 00:56:33.947
<v Michael Gottlieb>Okay.</v>

00:56:36.467 --> 00:56:41.347
<v Michael Gottlieb>Okay, next, Lena, could you please share the image that you mocked up?</v>

00:56:36.867 --> 00:56:37.427
<v Efim Podvoiski>Thank you.</v>

00:56:42.467 --> 00:56:45.027
<v Michael Gottlieb>of what it would conceivably look like.</v>

00:56:57.587 --> 00:57:09.427
<v Michael Gottlieb>Okay, so what we did is we took Lions Riches, we got rid of the progressives across the top. We've got our dual box skill feature.</v>

00:57:10.627 --> 00:57:29.507
<v Michael Gottlieb>and we lowered it down. So ergonomically, when you physically go to touch the screen, the boxes are massive. And then we're using that same sense of choose the larger coin to win $50. And if you look across the bottom, we have credits on the left.</v>

00:57:29.907 --> 00:57:31.347
<v Michael Gottlieb>and a ward in the center.</v>

00:57:32.947 --> 00:57:39.827
<v Michael Gottlieb>So this is a template of what the JVL envisioning of this type of product could look like.</v>

00:57:43.667 --> 00:57:44.467
<v Val Levitan>Um...</v>

00:57:46.227 --> 00:57:55.827
<v Val Levitan>The first comment that comes to mind is I would increase the transparency of the bigger rectangle.</v>

00:57:59.347 --> 00:58:00.707
<v Val Levitan>Make it more transparent.</v>

00:58:02.467 --> 00:58:03.667
<v Michael Gottlieb>The one with the coins?</v>

00:58:04.547 --> 00:58:06.147
<v Val Levitan>No, the.</v>

00:58:07.347 --> 00:58:14.307
<v Val Levitan>The the bigger one, the where it says, so choose the large larger coin.</v>

00:58:09.267 --> 00:58:09.707
<v Efim Podvoiski>Around.</v>

00:58:15.667 --> 00:58:18.387
<v Juan Martinez>The entire dual coin box frame.</v>

00:58:18.947 --> 00:58:19.907
<v Val Levitan>The frame, yeah.</v>

00:58:20.227 --> 00:58:20.547
<v Michael Gottlieb>OK.</v>

00:58:20.787 --> 00:58:24.147
<v Val Levitan>So the background of the frame, I would make it more transparent.</v>

00:58:25.907 --> 00:58:30.147
<v Val Levitan>And I would make it the whole box, I would make it flutter.</v>

00:58:32.787 --> 00:58:33.427
<v Val Levitan>Squeeze it.</v>

00:58:32.867 --> 00:58:33.507
<v Michael Gottlieb>Make it what?</v>

00:58:34.867 --> 00:58:35.507
<v Val Levitan>Flower.</v>

00:58:36.587 --> 00:58:38.947
<v Val Levitan>Squeeze it, it's too square.</v>

00:58:37.987 --> 00:58:38.507
<v Efim Podvoiski>No.</v>

00:58:37.987 --> 00:58:43.667
<v Michael Gottlieb>Less, less verticality. It's too, it's too rectangular. You want the vertical.</v>

00:58:42.547 --> 00:58:46.787
<v Val Levitan>It's too. It's too square. I'd like it more rectangular.</v>

00:58:48.067 --> 00:58:55.987
<v Michael Gottlieb>even more rectangular. Okay, so then we would reduce the size of the icons and squeeze it down further.</v>

00:58:55.707 --> 00:58:57.027
<v Val Levitan>Yeah, yeah.</v>

00:58:57.907 --> 00:58:58.387
<v Michael Gottlieb>Okay.</v>

00:58:58.787 --> 00:59:01.107
<v Val Levitan>probably by 30%.</v>

00:59:02.667 --> 00:59:03.587
<v Michael Gottlieb>Uh, okay.</v>

00:59:07.107 --> 00:59:11.187
<v Val Levitan>So, it becomes it becomes a secondary thing.</v>

00:59:12.467 --> 00:59:16.307
<v Val Levitan>Right now it's primary, like it's blocking everything and it's...</v>

00:59:17.427 --> 00:59:19.827
<v Val Levitan>You know, center attention.</v>

00:59:21.267 --> 00:59:22.347
<v Michael Gottlieb>Right, yeah, the orig.</v>

00:59:21.427 --> 00:59:28.867
<v Val Levitan>I actually, I actually have to give a compliment to Primero, and I don't even like the company.</v>

00:59:30.307 --> 00:59:34.707
<v Val Levitan>But their implementation is better than Piggy.</v>

00:59:37.027 --> 00:59:43.347
<v Michael Gottlieb>I found it very confusing. It looks to me like you actually have to think. Piggy, you don't have to think.</v>

00:59:37.347 --> 00:59:37.667
<v Val Levitan>I...</v>

00:59:42.267 --> 00:59:43.187
<v Juan Martinez>You can do.</v>

00:59:45.427 --> 00:59:46.387
<v Juan Martinez>Yeah, you there's.</v>

00:59:45.507 --> 00:59:53.587
<v Michael Gottlieb>You're presented with Piggy, you're presented with two choices. Here you have two choices. With Primero, you've got four choices.</v>

00:59:54.867 --> 00:59:55.747
<v Michael Gottlieb>And the odds.</v>

00:59:54.947 --> 00:59:59.507
<v Val Levitan>Four choices, but the way they're positioned is so easy to understand.</v>

01:00:00.707 --> 01:00:04.067
<v Val Levitan>Not only position because of the shape, same shape.</v>

01:00:05.667 --> 01:00:08.387
<v Val Levitan>Very easy to point your finger at the same shape.</v>

01:00:09.667 --> 01:00:16.467
<v Val Levitan>And also, because Premier has this huge 50-some vertical screen.</v>

01:00:17.547 --> 01:00:18.467
<v Val Levitan>Huge screen.</v>

01:00:19.587 --> 01:00:22.227
<v Val Levitan>They position at very low, so it's...</v>

01:00:24.307 --> 01:00:26.147
<v Val Levitan>Less destructive for the eye.</v>

01:00:32.067 --> 01:00:56.507
<v Michael Gottlieb>Yeah, Aristocrat kind of does, our competitors are doing the complete opposite. They're making the really boxes really big and prominent because basically it's a stopper. I mean, I'm not, I wasn't, you know, I would, the only thing, the only observation I would make is that if you're clueless as a player, the first time playing the Primero game, the gameplay stops and you're trying to figure out what you need to do to get the game</v>

01:00:56.627 --> 01:01:07.987
<v Michael Gottlieb>play to continue and you have to look at this bar down at the bottom of the screen and it just doesn't seem like it hits you over the head with this is what you need to do.</v>

01:01:08.627 --> 01:01:12.147
<v Val Levitan>Yeah, I agree, but only the first time.</v>

01:01:13.027 --> 01:01:14.147
<v Michael Gottlieb>Okay, fair enough.</v>

01:01:16.787 --> 01:01:22.307
<v Val Levitan>But ours and the competitors.</v>

01:01:23.347 --> 01:01:24.307
<v Val Levitan>Is very.</v>

01:01:25.507 --> 01:01:28.547
<v Val Levitan>This destructive, it's like it's...</v>

01:01:27.827 --> 01:01:30.787
<v Michael Gottlieb>Yes, I think it's intentionally so.</v>

01:01:33.267 --> 01:01:35.027
<v Michael Gottlieb>I think it's intentionally supposed to.</v>

01:01:34.067 --> 01:01:37.267
<v Val Levitan>I'm not, I'm not a designer, I'm just...</v>

01:01:36.947 --> 01:01:37.267
<v Michael Gottlieb>Yeah.</v>

01:01:38.787 --> 01:01:49.507
<v Val Levitan>I played Primero for the first time and I played the Light and Wonder as well. And I like Primero better, but this is my personal, non-professional opinion.</v>

01:01:51.827 --> 01:01:53.707
<v Val Levitan>To me, that experience was better.</v>

01:01:57.027 --> 01:02:00.747
<v Michael Gottlieb>Okay, well we can certainly thin the box.</v>

01:01:59.747 --> 01:02:03.667
<v Val Levitan>I, I, I, but I don't know what's right and wrong. I have no idea.</v>

01:02:05.587 --> 01:02:06.787
<v Michael Gottlieb>Juan, what do you think?</v>

01:02:07.827 --> 01:02:27.267
<v Juan Martinez>I mean, I agree that making this more rectangular is less imposing to the player, but no, this is a faster touch and move on to the next game. There's no way that the Palomino solution does require a nanosecond or two</v>

01:02:27.667 --> 01:02:36.227
<v Juan Martinez>of more thought process versus selecting the bigger coin. So I think this will lead to more games played over time.</v>

01:02:37.747 --> 01:02:44.387
<v Lena Zhukova>At first, we created this version, but we then we decided that we don't want to cover dashboard.</v>

01:02:44.787 --> 01:02:49.267
<v Michael Gottlieb>Right, you don't want to, you can't cover the dashboard because you need the win to go to the award meter.</v>

01:02:46.187 --> 01:02:46.467
<v Juan Martinez>Yeah.</v>

01:02:49.227 --> 01:03:04.347
<v Val Levitan>No, no, no, no, that is not a good solution. That is for sure. You're covering the dashboard. It's not a good solution. I agree. But if you move if you move that box on top on top of the yeah on top of the.</v>

01:02:49.867 --> 01:02:50.147
<v Juan Martinez>Yeah.</v>

01:02:53.027 --> 01:02:53.427
<v Michael Gottlieb>Right.</v>

01:02:53.067 --> 01:02:53.307
<v Juan Martinez>Yeah.</v>

01:02:55.267 --> 01:02:55.827
<v Lena Zhukova>Mhm.</v>

01:02:56.547 --> 01:02:56.867
<v Michael Gottlieb>Right.</v>

01:03:03.587 --> 01:03:05.267
<v Michael Gottlieb>Can you do that, Lena? Can you move it?</v>

01:03:05.507 --> 01:03:06.387
<v Lena Zhukova>Yeah, sure.</v>

01:03:05.827 --> 01:03:06.307
<v Val Levitan>Yeah.</v>

01:03:06.547 --> 01:03:07.587
<v Michael Gottlieb>Okay, there you go.</v>

01:03:13.747 --> 01:03:17.187
<v Juan Martinez>Yeah, just increase the transparency. There you go.</v>

01:03:19.987 --> 01:03:23.747
<v Juan Martinez>I think that's an acceptable display there.</v>

01:03:26.107 --> 01:03:29.027
<v Val Levitan>Yeah, and your hand is there, your hand is low, right?</v>

01:03:29.427 --> 01:03:29.747
<v Michael Gottlieb>Right.</v>

01:03:29.507 --> 01:03:29.827
<v Juan Martinez>Yeah.</v>

01:03:30.867 --> 01:03:32.947
<v Michael Gottlieb>That's why we put the box as low as we did.</v>

01:03:36.067 --> 01:03:46.787
<v Val Levitan>I don't know. I mean, this could probably be slightly bigger. I don't know, but that's the right, that's the right direction for me. I'm not an expert.</v>

01:03:49.187 --> 01:03:53.587
<v Val Levitan>I, I don't know what's right and wrong, but for me, you know, probably better.</v>

01:03:55.187 --> 01:04:14.387
<v Michael Gottlieb>I'm not necessarily opposed to this. I think, again, in terms of collision detection, we basically, if you touch the right of that rectangular box, you'll choose the right. If you choose the left, you'll choose the left. I think just as long as the player doesn't have to get super granular with where they put their finger,</v>

01:04:06.707 --> 01:04:07.107
<v Juan Martinez>Right.</v>

01:04:14.867 --> 01:04:15.507
<v Michael Gottlieb>On.</v>

01:04:16.667 --> 01:04:30.627
<v Michael Gottlieb>It's perfectly fine. And if this is if this is more in the in the comfort factor of that specific player base, because the nature of our competitor is executing in a similar fashion, OK, I don't object to it.</v>

01:04:17.107 --> 01:04:17.387
<v Juan Martinez>Yeah.</v>

01:04:31.347 --> 01:04:31.587
<v Juan Martinez>Yeah.</v>

01:04:34.307 --> 01:04:51.907
<v Juan Martinez>And Val, this is probably a longer term question, but Primero has a mechanical button deck. Are we going to keep the V deck long term, or do we want to consider the V deck option, I mean, mechanical button option for the future?</v>

01:04:53.907 --> 01:04:58.147
<v Val Levitan>So, this, uh, this provokes another conversation, one.</v>

01:04:58.867 --> 01:04:59.587
<v Juan Martinez>Understood.</v>

01:05:02.067 --> 01:05:07.027
<v Val Levitan>Well, many conversations, they're not easy, they're difficult conversations.</v>

01:05:09.347 --> 01:05:10.707
<v Val Levitan>But I'm glad you asked.</v>

01:05:13.387 --> 01:05:15.507
<v Val Levitan>And I, I was thinking about it quite a bit.</v>

01:05:16.627 --> 01:05:19.987
<v Val Levitan>So let me start by saying that I love VDEC.</v>

01:05:22.867 --> 01:05:32.467
<v Val Levitan>But I'm analyzing why is our machine making less money than aristocrat, for example.</v>

01:05:36.547 --> 01:05:48.067
<v Val Levitan>One thing that jumps at me when I look at machines in locations, and I go from location to location, in Georgia specifically.</v>

01:05:54.467 --> 01:06:00.867
<v Val Levitan>Aristocrat also has a mechanical mechanical deck.</v>

01:06:02.787 --> 01:06:04.387
<v Val Levitan>with one slam button.</v>

01:06:05.747 --> 01:06:13.427
<v Val Levitan>An aristocrat has this small scale on the main screen that increases or decreases the bet.</v>

01:06:14.547 --> 01:06:14.947
<v Juan Martinez>Yes.</v>

01:06:16.467 --> 01:06:18.147
<v Val Levitan>And they start at a dollar.</v>

01:06:19.747 --> 01:06:22.027
<v Juan Martinez>They they default to a dollar.</v>

01:06:22.867 --> 01:06:28.027
<v Val Levitan>My apologies. The right word, the correct word is they default to a dollar.</v>

01:06:29.587 --> 01:06:32.227
<v Val Levitan>And then you could decrease or increase.</v>

01:06:35.027 --> 01:06:44.067
<v Val Levitan>But I don't know if it, let's say when you play our machine, like it's natural to start from the left.</v>

01:06:45.147 --> 01:06:50.467
<v Val Levitan>like the left button, the smallest button, it's very easy to jump into the smallest button.</v>

01:06:51.987 --> 01:06:54.387
<v Val Levitan>And that's almost kind of...</v>

01:06:56.387 --> 01:07:05.507
<v Val Levitan>We almost like question, do you really want to go and spend $4 or $3? Like it becomes scary, you know.</v>

01:07:07.227 --> 01:07:20.307
<v Val Levitan>Where with aristocrat, it's just slam button. It's like you put that bat and you really don't kind of, it's not in your face. I don't know if there is anything mental in there.</v>

01:07:17.187 --> 01:07:17.467
<v Juan Martinez>Yeah.</v>

01:07:21.587 --> 01:07:35.507
<v Val Levitan>And we are almost counterproductive and discouraging people, like almost warning, you're entering a danger zone now, you're going to be playing $3 a game or $4 a game.</v>

01:07:36.867 --> 01:07:39.587
<v Val Levitan>So I don't know if there is any psychological...</v>

01:07:40.787 --> 01:07:41.427
<v Val Levitan>Um...</v>

01:07:47.027 --> 01:08:01.427
<v Juan Martinez>There is Val. I mean, I, there's a few manufacturers who enable dollars to be displayed on the buttons. Everything I've ever learned is Americans can't count. So</v>

01:07:47.267 --> 01:07:47.827
<v Val Levitan>You know.</v>

01:08:02.387 --> 01:08:23.787
<v Juan Martinez>600 credits is not as much as $6. Bad example, but yes, I understand what you're saying. Yeah, if it were up to me, I would always display things in credits because they can't count and they're not adding it up, but actually seeing a dollar, seeing $5.</v>

01:08:24.387 --> 01:08:30.627
<v Juan Martinez>Seeing $3, you're able to know how much you're about to spend, and you may spend less.</v>

01:08:33.067 --> 01:08:38.227
<v Juan Martinez>That's why those who offer it let you toggle that option at the operator's discretion.</v>

01:08:39.107 --> 01:08:45.987
<v Juan Martinez>But Georgia and everybody else's machines have always been like this in dollar amounts.</v>

01:08:47.347 --> 01:08:53.587
<v Val Levitan>Well, no, because light and wonder now uses credits.</v>

01:08:51.187 --> 01:08:51.667
<v Juan Martinez>Yes.</v>

01:08:53.947 --> 01:08:55.587
<v Juan Martinez>Correct. I'm sorry, correct. You're right.</v>

01:08:58.467 --> 01:09:08.147
<v Val Levitan>So I think that we're almost like discouraging people. We're saying, ****, man, you're about to bet 4 bucks, you know?</v>

01:09:08.787 --> 01:09:09.027
<v Juan Martinez>Sure.</v>

01:09:10.387 --> 01:09:12.467
<v Val Levitan>Maybe you should reconsider. I have no idea.</v>

01:09:13.187 --> 01:09:35.787
<v Michael Gottlieb>Well, even the counter argument of what you actually do see of slot players is that if they're up at 4:00 and they spin and they lose and they spin and they lose, they back down. They back down on their bet. And to your point, if you kind of like are locked and loaded where you're not really paying attention to your bet and it's, we make it easy. We make it easy to bet down.</v>

01:09:35.347 --> 01:09:39.667
<v Val Levitan>Yes, yes, yes. Yeah, we make it easy to hesitate.</v>

01:09:39.907 --> 01:09:41.907
<v Michael Gottlieb>Right, and to lower your back.</v>

01:09:42.547 --> 01:09:43.587
<v Val Levitan>And lower your bed.</v>

01:09:45.427 --> 01:09:56.387
<v Michael Gottlieb>I would agree with that. I mean, yeah, you give the player, the player has choice and when you're just dealing with the little arrows and whatever the bet level is, you default to a buck. Are they going to change it?</v>

01:10:00.307 --> 01:10:03.507
<v Juan Martinez>But are we saying redesign the?</v>

01:10:01.187 --> 01:10:06.307
<v Val Levitan>But, but I, but, but I love, I love Vivek, I love it.</v>

01:10:07.587 --> 01:10:14.147
<v Juan Martinez>But we could still have the up or down, not on screen like Aristocrat does, but we could do that on the V-Deck.</v>

01:10:17.667 --> 01:10:21.747
<v Val Levitan>No, we, no, look, we don't have to satisfy Val. We have to make money.</v>

01:10:22.587 --> 01:10:23.587
<v Efim Podvoiski>What is it?</v>

01:10:22.707 --> 01:10:34.067
<v Val Levitan>It's all about it's all about us making money, and if it results to, man, let's put A1 slam button on on the B. deck.</v>

01:10:36.787 --> 01:10:42.867
<v Michael Gottlieb>Is the V-Deck expensive in our bill of materials compared to just having a panel with one single button?</v>

01:10:43.747 --> 01:10:46.147
<v Val Levitan>Yeah, of course, of course. Yeah.</v>

01:10:45.667 --> 01:10:46.627
<v Michael Gottlieb>Well, I don't, I mean...</v>

01:10:47.347 --> 01:10:48.627
<v Val Levitan>Yeah, yeah, yeah.</v>

01:10:47.667 --> 01:10:49.827
<v Michael Gottlieb>Fifty, 100, $200.</v>

01:10:57.827 --> 01:11:01.347
<v Val Levitan>Probably 120 our cost.</v>

01:11:00.907 --> 01:11:21.227
<v Michael Gottlieb>Okay, that's a lot of money. I mean, I have to, you have to believe that our aristocrat has infinite money, infinite research analysis, infinite everything. And they obviously have a couple of different massively large VDECs. If they're coming into this market with a blank panel and a play button, that has to mean something.</v>

01:11:03.547 --> 01:11:05.347
<v Val Levitan>Yeah, yeah, yeah, yeah.</v>

01:11:20.227 --> 01:11:20.707
<v Juan Martinez>Yeah, but...</v>

01:11:21.307 --> 01:11:21.587
<v Michael Gottlieb>thing.</v>

01:11:22.147 --> 01:11:41.987
<v Juan Martinez>Michael, they they they unretired a class 3 cabinet called the Mars X, so that that and that always had buttons, so it never had a V deck, so they came in with their cheap cabinet that they brought back to life and it had mechanical buttons, but they also may have heard comments.</v>

01:11:28.627 --> 01:11:29.027
<v Michael Gottlieb>Right.</v>

01:11:42.307 --> 01:12:00.867
<v Juan Martinez>Well, the master is saying, hey, these digital screens are breaking. Felipe reported last week that that's what he heard now in Georgia, that light and wonder sales are down a little bit because people are breaking their VDEX. You know, true or false, I don't know, but that.</v>

01:12:00.227 --> 01:12:09.907
<v Val Levitan>I, I could, I could tell you, I could tell you that if we submit to a gossip that V. decks are breaking.</v>

01:12:11.107 --> 01:12:13.267
<v Val Levitan>We may even regenerate sales.</v>

01:12:19.587 --> 01:12:23.107
<v Val Levitan>You know what I'm saying? You know, you know, do you understand my point?</v>

01:12:24.227 --> 01:12:28.547
<v Juan Martinez>Yeah, that we have strong gorilla glass and ours doesn't break.</v>

01:12:29.347 --> 01:12:35.027
<v Val Levitan>No, if we say, if we take our VDAC out and put buttons.</v>

01:12:35.027 --> 01:12:35.507
<v Juan Martinez>Yes.</v>

01:12:35.827 --> 01:12:39.427
<v Val Levitan>Then the operators may say, finally, we convinced you.</v>

01:12:40.227 --> 01:12:40.707
<v Juan Martinez>Yeah.</v>

01:12:41.267 --> 01:12:49.907
<v Val Levitan>Give me a couple of shekels, couple of shekels of discount, and okay, fine. Finally, we convinced you we won, we're going to stop buying.</v>

01:12:41.707 --> 01:12:42.067
<v Michael Gottlieb>Peari.</v>

01:12:42.947 --> 01:12:43.427
<v Juan Martinez>Joe.</v>

01:12:49.347 --> 01:12:49.827
<v Juan Martinez>Sure.</v>

01:12:50.787 --> 01:13:10.147
<v Juan Martinez>And that would be a great way to help promote our data collection as an example of something we've observed. And yeah, I think that's a great idea, Val. And I know Class A is more price sensitive than the Class B machines in Georgia. So wherever we can save, the better we are.</v>

01:13:13.107 --> 01:13:21.267
<v Val Levitan>OK, but I also, on a fly, made an executive decision, and I said...</v>

01:13:23.027 --> 01:13:26.307
<v Val Levitan>Our first couple of introductions to an operator.</v>

01:13:29.427 --> 01:13:31.107
<v Val Levitan>No, let me, let me go back.</v>

01:13:38.467 --> 01:13:39.907
<v Val Levitan>I am making a play.</v>

01:13:41.747 --> 01:13:45.747
<v Val Levitan>With operators, by giving away.</v>

01:13:46.907 --> 01:13:48.627
<v Val Levitan>Flexport.</v>

01:13:51.187 --> 01:13:52.627
<v Val Levitan>Flex IQ.</v>

01:13:54.467 --> 01:14:00.627
<v Val Levitan>And flex pay, sorry, five additional 5 flex ports.</v>

01:14:01.747 --> 01:14:04.307
<v Val Levitan>One IQ and one.</v>

01:14:05.987 --> 01:14:07.107
<v Val Levitan>Flex P.</v>

01:14:09.507 --> 01:14:12.867
<v Val Levitan>For with each machine that they buy.</v>

01:14:16.547 --> 01:14:17.507
<v Val Levitan>And so.</v>

01:14:19.987 --> 01:14:27.107
<v Val Levitan>I increased the price from get-go, even at the show, to 14.5.</v>

01:14:30.387 --> 01:14:38.947
<v Val Levitan>But as Felipe was talking to an operator and I was listening, Felipe was promoting 10 game library.</v>

01:14:41.827 --> 01:14:44.787
<v Val Levitan>And I needed to increase the price even further.</v>

01:14:47.347 --> 01:14:55.107
<v Val Levitan>So I said in the same conversation, the kind of flew, kind of flew out of my mouth too, in a way.</v>

01:14:56.947 --> 01:15:00.467
<v Val Levitan>And I said, but with 15 games.</v>

01:15:01.547 --> 01:15:11.507
<v Val Levitan>We are selling at 15,750, which represents $250 per game more, which is exactly what you want.</v>

01:15:12.707 --> 01:15:16.387
<v Val Levitan>But then I didn't really offer that package deal.</v>

01:15:18.147 --> 01:15:28.707
<v Val Levitan>But then when I added the package deal, then I said this package deal is only valid for the $15,750 machine.</v>

01:15:35.747 --> 01:15:39.347
<v Val Levitan>My point is that the reason that what I'm saying here is that...</v>

01:15:40.707 --> 01:15:45.267
<v Val Levitan>The operator actually took very well to 15 gates.</v>

01:15:46.707 --> 01:15:48.467
<v Val Levitan>It actually went very well.</v>

01:15:50.387 --> 01:15:55.747
<v Juan Martinez>The problem, though, is we can only display 10 right now per arena.</v>

01:15:50.707 --> 01:15:51.267
<v Val Levitan>And then?</v>

01:15:56.387 --> 01:15:59.187
<v Val Levitan>I understand. I understand.</v>

01:16:00.267 --> 01:16:07.987
<v Val Levitan>But I think that there's actually, and I looked at the interface, the interface in the location looks actually very attractive.</v>

01:16:09.187 --> 01:16:13.667
<v Val Levitan>And I have a couple of notes here. So I would like to extend it.</v>

01:16:14.667 --> 01:16:16.627
<v Val Levitan>Two 15 games.</v>

01:16:17.987 --> 01:16:21.107
<v Val Levitan>But I think we cannot do 50 like it has to be an even number.</v>

01:16:24.467 --> 01:16:28.027
<v Val Levitan>Or maybe we can four, I would do four, four.</v>

01:16:25.187 --> 01:16:25.507
<v Juan Martinez>Yeah.</v>

01:16:30.707 --> 01:16:32.787
<v Val Levitan>And what is it, 7?</v>

01:16:34.787 --> 01:16:35.107
<v Juan Martinez>Yeah.</v>

01:16:37.267 --> 01:16:38.547
<v Val Levitan>Yeah, that would work.</v>

01:16:40.227 --> 01:16:44.227
<v Efim Podvoiski>But you don't have 4-4 and seven, do we? You have 4-4.</v>

01:16:40.787 --> 01:16:40.987
<v Juan Martinez>Yeah.</v>

01:16:43.307 --> 01:16:48.627
<v Juan Martinez>Oh, we have 4, 4, and six. Oh, no, we could do 7.</v>

01:16:50.627 --> 01:16:52.147
<v Juan Martinez>We're trying to get to 15.</v>

01:16:54.227 --> 01:17:10.547
<v Val Levitan>But regardless, so I would do more games. I would increase the price a little bit more, which is 15, 750 is great. We land it nicely. And then give that discount. And honestly, I believe that will kill the market.</v>

01:17:13.747 --> 01:17:16.307
<v Val Levitan>Not kill the market, we will kill it in the market, sorry.</v>

01:17:16.307 --> 01:17:17.667
<v Juan Martinez>Yeah, understood.</v>

01:17:19.587 --> 01:17:24.627
<v Lena Zhukova>But what product are we talking about? Is it going to be next, Georgia?</v>

01:17:24.307 --> 01:17:27.507
<v Val Levitan>No, no, no, no, no, just this V3.</v>

01:17:28.947 --> 01:17:35.987
<v Lena Zhukova>But to redo interface to show in 15 games, it will take a significant amount of time.</v>

01:17:36.147 --> 01:17:39.827
<v Efim Podvoiski>I also not sure that we can have 15 games loaded.</v>

01:17:36.387 --> 01:17:36.867
<v Val Levitan>Yes.</v>

01:17:41.907 --> 01:17:45.187
<v Efim Podvoiski>I, I just don't know if you, if you should confirm it.</v>

01:17:45.987 --> 01:17:46.627
<v Juan Martinez>Right, Val.</v>

01:17:46.227 --> 01:18:02.547
<v Val Levitan>So, no, hold on a second. I jumped too far. So right now, the operator understands that we can only load 10 games, but they buy 15 games. And because we have a modem, we'll be able to set it through the modem.</v>

01:18:03.347 --> 01:18:03.587
<v Juan Martinez>Right.</v>

01:18:04.147 --> 01:18:10.467
<v Val Levitan>Enable it through the modem, and they're and they're ecstatic about it; they're not even thinking about showing all 15 games.</v>

01:18:10.867 --> 01:18:11.107
<v Lena Zhukova>Yeah.</v>

01:18:12.547 --> 01:18:16.147
<v Val Levitan>But I think, like looking at the interface.</v>

01:18:17.227 --> 01:18:19.347
<v Val Levitan>I think we should make a couple of changes.</v>

01:18:20.707 --> 01:18:26.787
<v Val Levitan>And again, I am the VDEC guy, right? Like I love VDEC. I think we should.</v>

01:18:28.147 --> 01:18:33.107
<v Val Levitan>Go for button deck, mechanical deck.</v>

01:18:37.507 --> 01:18:43.107
<v Val Levitan>I think that we should go for that trick that Aristocrat has.</v>

01:18:44.067 --> 01:18:45.827
<v Juan Martinez>Sure, the bed up, bed down, yeah.</v>

01:18:46.547 --> 01:18:49.907
<v Val Levitan>That up and down, but with the default value of a dollar.</v>

01:18:50.627 --> 01:18:51.027
<v Juan Martinez>Right.</v>

01:18:52.227 --> 01:18:55.507
<v Val Levitan>And make it as part of our of our.</v>

01:18:57.867 --> 01:19:01.507
<v Val Levitan>What do you guys call it? The dashboard, yeah, dashboard.</v>

01:18:58.387 --> 01:18:59.747
<v Michael Gottlieb>Dashboard, dashboard.</v>

01:18:59.507 --> 01:19:00.227
<v Juan Martinez>Okay.</v>

01:19:04.627 --> 01:19:08.387
<v Val Levitan>And by the way, I think that our dashboard could...</v>

01:19:10.067 --> 01:19:16.547
<v Val Levitan>go higher vertically because we have enough space. The screen is good enough, it's big enough.</v>

01:19:19.587 --> 01:19:22.547
<v Val Levitan>Our dashboard is too tiny.</v>

01:19:23.667 --> 01:19:34.627
<v Juan Martinez>Yeah, but we, according to Felipe, he already had some complaints about a player reaching the top nudge arrow on a V43, so this would push everything up.</v>

01:19:33.747 --> 01:19:37.587
<v Val Levitan>So, so yes, exactly, I agree.</v>

01:19:39.027 --> 01:19:44.147
<v Val Levitan>But change the nudge to selection box.</v>

01:19:46.227 --> 01:19:48.547
<v Michael Gottlieb>That's a huge, huge change.</v>

01:19:49.027 --> 01:19:53.267
<v Val Levitan>Yes, I'm not asking for right now. Let's call it V4.</v>

01:19:53.507 --> 01:19:55.427
<v Michael Gottlieb>Oh, okay, okay, okay, thank you.</v>

01:19:56.067 --> 01:20:03.187
<v Juan Martinez>Yeah. And I still like what Aristocrat did, where they mixed traditional nudge and a little piggy.</v>

01:20:03.667 --> 01:20:09.827
<v Val Levitan>I don't think so. I think they just simply did not transfer all of their games.</v>

01:20:13.747 --> 01:20:14.787
<v Val Levitan>Pink it works better.</v>

01:20:15.987 --> 01:20:17.987
<v Juan Martinez>No, I, it's definitely faster, agreed.</v>

01:20:20.547 --> 01:20:36.867
<v Michael Gottlieb>Okay, so Georgia will call it V4, mechanical button deck, bet up and down on the dashboard, default of $1, make the dashboard larger, and then use the dual box probably in a similar fashion that we just designed, that we just showed you.</v>

01:20:37.347 --> 01:20:39.107
<v Juan Martinez>To replace all nudge.</v>

01:20:39.587 --> 01:20:40.627
<v Michael Gottlieb>In place of nudge.</v>

01:20:43.107 --> 01:20:43.667
<v Efim Podvoiski>And just...</v>

01:20:43.107 --> 01:20:46.547
<v Val Levitan>And did you say 15 games selection?</v>

01:20:46.787 --> 01:20:49.427
<v Michael Gottlieb>You want 15 games on the game selection screen?</v>

01:20:49.427 --> 01:20:57.107
<v Val Levitan>Yes, yes. I think you guys really nailed the interface.</v>

01:20:58.787 --> 01:21:14.147
<v Val Levitan>And I think people actually now, like when I explained to Felipe, when I explained to a couple of customers that we now have three different progressives and they all play a different role.</v>

01:21:16.547 --> 01:21:22.707
<v Val Levitan>People starting to understand this now. So I would make progressive a little more.</v>

01:21:23.907 --> 01:21:25.907
<v Val Levitan>Are prominent on the.</v>

01:21:27.827 --> 01:21:32.027
<v Val Levitan>Main screen on the initial in the initial screen.</v>

01:21:32.307 --> 01:21:33.667
<v Juan Martinez>The attraction loop.</v>

01:21:32.867 --> 01:21:33.347
<v Val Levitan>Right.</v>

01:21:34.787 --> 01:21:40.067
<v Val Levitan>I, you know, I don't know yet, but let me come back to attraction, so...</v>

01:21:41.587 --> 01:21:50.147
<v Val Levitan>In the location, when machines like you, you need to understand these locations is a real shithole, like.</v>

01:21:51.227 --> 01:21:51.827
<v Val Levitan>Shishko.</v>

01:21:53.107 --> 01:21:54.267
<v Val Levitan>Like, disgusting.</v>

01:21:57.707 --> 01:21:59.027
<v Val Levitan>Dirty, disgusting.</v>

01:22:01.907 --> 01:22:03.907
<v Val Levitan>And all machines kind of look the same.</v>

01:22:06.547 --> 01:22:11.427
<v Val Levitan>So, what the moment you guys came out with this liquid crystal?</v>

01:22:12.547 --> 01:22:15.107
<v Val Levitan>Liquid glass, it stands out.</v>

01:22:16.187 --> 01:22:19.827
<v Val Levitan>So, I think that you should work on the main screen.</v>

01:22:20.867 --> 01:22:24.467
<v Val Levitan>Make it more stand out, like, put your effort in there.</v>

01:22:27.107 --> 01:22:28.867
<v Juan Martinez>OK, and I guess refer.</v>

01:22:28.067 --> 01:22:33.987
<v Val Levitan>It's too static right now, too static, and it needs a little more.</v>

01:22:36.147 --> 01:22:39.667
<v Val Levitan>I think, I don't remember, I think it was Felipe who recommended.</v>

01:22:41.347 --> 01:22:44.227
<v Val Levitan>advertising, full screen advertising mode.</v>

01:22:44.867 --> 01:22:47.587
<v Lena Zhukova>But we, we are going to fail it, and we see.</v>

01:22:46.707 --> 01:22:47.107
<v Juan Martinez>Yeah.</v>

01:22:47.027 --> 01:22:49.427
<v Val Levitan>I think, I think it's a good idea.</v>

01:22:49.507 --> 01:23:10.307
<v Lena Zhukova>Behaving it now, it's not going to be static at all, because you will see first of all, like animated logo, then full screen game with bonus. And then again, you're coming back to game selection and you advertise, for example, like twin bison logo and then full screen twin bison game with a bonus.</v>

01:22:50.787 --> 01:22:51.107
<v Juan Martinez>Yeah.</v>

01:23:11.267 --> 01:23:13.107
<v Val Levitan>Yes, I think it will go very well.</v>

01:23:15.507 --> 01:23:32.707
<v Juan Martinez>And Michael, I think maybe the limitation of 10 is maybe for future games we need to focus on 100% mathematical clones so that we're not pushing or stressing the box. Maybe that's the limitation. Don't know that.</v>

01:23:31.907 --> 01:23:37.427
<v Efim Podvoiski>Ohh, clones? No, that's, yeah, what do you mean, push on stress in the box?</v>

01:23:37.987 --> 01:23:47.507
<v Juan Martinez>I don't know why, why is there a limitation of, first it was 14 and now it's 10. Why can't I cross 10?</v>

01:23:42.787 --> 01:23:44.787
<v Efim Podvoiski>Oh, it's it's it's.</v>

01:23:46.107 --> 01:23:49.267
<v Lena Zhukova>No, 12, 12, we never show more than 12.</v>

01:23:49.907 --> 01:23:54.147
<v Juan Martinez>Right, so, but that, but now we've got three different families of progressives.</v>

01:23:54.227 --> 01:24:03.187
<v Efim Podvoiski>It's not math, it's what's in the box is graphical assets that have to.</v>

01:24:02.227 --> 01:24:05.427
<v Val Levitan>Yeah, it's a no, it's a memory.</v>

01:24:06.307 --> 01:24:13.027
<v Efim Podvoiski>It's memory, yeah. We want almost everything build ready when you, otherwise you have loading time.</v>

01:24:14.187 --> 01:24:18.547
<v Efim Podvoiski>When you press the button, so we have every single memory, almost every single memory.</v>

01:24:19.347 --> 01:24:19.627
<v Juan Martinez>Okay.</v>

01:24:19.507 --> 01:24:25.747
<v Lena Zhukova>Yeah, nobody likes when you press the button game button and you see this loading bar.</v>

01:24:25.347 --> 01:24:26.067
<v Juan Martinez>Absolutely.</v>

01:24:27.587 --> 01:24:36.027
<v Juan Martinez>But Val, is that fixable by just a RAM upgrade to the new machines? And I don't know if it is or isn't.</v>

01:24:36.787 --> 01:24:37.427
<v Val Levitan>I don't know.</v>

01:24:40.627 --> 01:24:45.587
<v Efim Podvoiski>If you have the RAM upgrade, of course, but RAM was not cheap now, right?</v>

01:24:45.907 --> 01:24:47.347
<v Juan Martinez>I know, I know.</v>

01:24:47.307 --> 01:24:49.187
<v Val Levitan>Right, right now, it's crazy expensive.</v>

01:24:49.827 --> 01:24:50.147
<v Juan Martinez>Yeah.</v>

01:24:51.347 --> 01:25:08.467
<v Efim Podvoiski>I wanted to ask a question. Is it, do we know that aristocrat or whoever has the mechanical buttons and start with dollar aristocrat, right? Do we know that their average bet is higher than ours significantly?</v>

01:25:09.827 --> 01:25:15.907
<v Juan Martinez>We only know that they're currently number one in the market, but we don't have any data to support that. Yeah.</v>

01:25:13.187 --> 01:25:29.507
<v Efim Podvoiski>They make more money, but yeah, but is it due to high number of plays? Of course, they have a high number of plays, no way around it, but do they also have a higher average bet? Because if they don't, then...</v>

01:25:31.187 --> 01:25:32.307
<v Efim Podvoiski>Probably doesn't work.</v>

01:25:33.107 --> 01:25:41.507
<v Michael Gottlieb>They have to have higher average bet based upon everything we just discussed. If they default to a dollar and we, what do we default? We default to the lowest, right?</v>

01:25:35.347 --> 01:25:35.747
<v Juan Martinez>Yeah.</v>

01:25:41.747 --> 01:25:44.427
<v Juan Martinez>Yeah, just, yeah, yeah, fine, yeah.</v>

01:25:41.987 --> 01:25:42.787
<v Efim Podvoiski>25 here.</v>

01:25:43.027 --> 01:25:45.267
<v Michael Gottlieb>25. Okay, that's four to one.</v>

01:25:45.907 --> 01:25:46.227
<v Juan Martinez>Yeah.</v>

01:25:47.107 --> 01:25:58.627
<v Michael Gottlieb>So we've got poor, I don't want to say poor people, we've got people with smaller bankrolls sitting on JVL machines because they can play 25 cents a spin and other people are on the dollar machine because that's what they're on.</v>

01:25:59.347 --> 01:26:04.227
<v Val Levitan>No, no, no, no, no, no, you could lower your bet to twenty-five cents.</v>

01:25:59.467 --> 01:26:02.307
<v Juan Martinez>Right, but you only get on that first spin.</v>

01:26:04.307 --> 01:26:05.187
<v Michael Gottlieb>An aristocrat.</v>

01:26:04.547 --> 01:26:07.667
<v Juan Martinez>Yeah, yeah, yeah, they just defaulted.</v>

01:26:05.587 --> 01:26:06.227
<v Val Levitan>Yes.</v>

01:26:06.347 --> 01:26:16.707
<v Michael Gottlieb>But players don't, they don't because they put money in the machine and they start hitting spin and it's too hard to change the freaking denom or change the change your bet level and they just play.</v>

01:26:17.827 --> 01:26:23.267
<v Val Levitan>Seems that way. I mean, could be a theory, yeah. We don't know for sure.</v>

01:26:26.227 --> 01:26:27.107
<v Val Levitan>It could be.</v>

01:26:32.787 --> 01:26:50.547
<v Michael Gottlieb>Okay, well of your list of suggested changes, I'm comfortable with everything except the larger dashboard. And the only reason I say that is we have an entire library of games now that we've built using the existing dashboard. And I don't think in making it 5% bigger,</v>

01:26:50.387 --> 01:26:55.267
<v Val Levitan>I'm happy. I'm happy to forego that. Not an issue. Not an issue.</v>

01:26:53.507 --> 01:26:54.947
<v Michael Gottlieb>Okay, done.</v>

01:26:55.027 --> 01:26:56.547
<v Lena Zhukova>I agree with Mike, yeah.</v>

01:26:57.107 --> 01:27:03.587
<v Efim Podvoiski>I want to mention that the fact that it's hard to change the bed down also means that it's hard to change the bed up.</v>

01:26:57.507 --> 01:26:57.987
<v Michael Gottlieb>Yeah, Efim.</v>

01:27:04.147 --> 01:27:04.547
<v Michael Gottlieb>Yes.</v>

01:27:06.707 --> 01:27:15.107
<v Efim Podvoiski>And we spent so much efforts into advertising, advertising better, better being some progressive for this hot buttons and.</v>

01:27:09.907 --> 01:27:12.547
<v Juan Martinez>I'm sorry, Efim, can you clarify?</v>

01:27:15.827 --> 01:27:17.187
<v Michael Gottlieb>He said what Efim is saying.</v>

01:27:15.987 --> 01:27:18.467
<v Val Levitan>Yeah, Val valid, valid point.</v>

01:27:18.787 --> 01:27:37.747
<v Michael Gottlieb>Yeah, what Efim is saying is that if you put 20 bucks in the machine and it's at a buck, it is just as confusing and it requires just as much effort to up your bet as it does to go down with your bet. So our theory is that is that we would benefit. There's a</v>

01:27:37.947 --> 01:28:00.067
<v Michael Gottlieb>far higher probability that the player will sit there and play at a dollar, won't bet up, won't bet down. And that is a superior mathematical solution than our player who can play the piano, who can play, who can bounce all around the damn deck. And then when they're on their last 10 bucks, they go down to 25 cents and sit there</v>

01:27:53.427 --> 01:27:53.987
<v Juan Martinez>Yes.</v>

01:28:00.387 --> 01:28:01.587
<v Michael Gottlieb>on 25 cents.</v>

01:28:01.827 --> 01:28:11.107
<v Juan Martinez>Well, no, but I mean they do have a they do have a button to bed up and down on screen and on the on their deck, so.</v>

01:28:10.227 --> 01:28:13.827
<v Michael Gottlieb>But it's just bet up, bet down though, it's not, it doesn't show numbers.</v>

01:28:14.267 --> 01:28:17.827
<v Juan Martinez>Yeah, it shows 25 cents, 50 cents, dollar. Yeah, yeah.</v>

01:28:17.107 --> 01:28:30.707
<v Michael Gottlieb>No, no, no. What I'm saying is on the button deck, it's just an up arrow and a down arrow. We're what Val is saying, and I see his point, is that our V deck glaringly shows you, do you want to bet five US dollars?</v>

01:28:28.387 --> 01:28:28.867
<v Juan Martinez>Yes.</v>

01:28:31.107 --> 01:28:32.067
<v Juan Martinez>Right, right.</v>

01:28:31.907 --> 01:28:45.587
<v Michael Gottlieb>And it creates it creates friction, it creates hesitancy, it creates second guessing, whereas that up and that down, it's more abstract. It is conceptually more abstract. So what we're.</v>

01:28:34.707 --> 01:28:35.027
<v Juan Martinez>Ohh.</v>

01:28:42.747 --> 01:28:42.947
<v Juan Martinez>Yeah.</v>

01:28:44.627 --> 01:28:49.027
<v Val Levitan>Yeah, good, uh, yeah, that's a good, good, uh, choice of words.</v>

01:28:49.667 --> 01:28:49.907
<v Juan Martinez>Yep.</v>

01:28:50.227 --> 01:28:51.587
<v Val Levitan>Good choice of words.</v>

01:28:51.587 --> 01:28:56.947
<v Efim Podvoiski>But when you press up or down, you don't immediately, but you just change the value and you see this value.</v>

01:28:56.147 --> 01:28:59.507
<v Michael Gottlieb>Correct. Yes. You change your bet level.</v>

01:28:56.347 --> 01:28:57.747
<v Juan Martinez>Correct, correct.</v>

01:28:58.787 --> 01:29:01.187
<v Efim Podvoiski>So, you see this really?</v>

01:29:01.827 --> 01:29:03.907
<v Michael Gottlieb>Oh, sure. Yeah, you can change your bet level.</v>

01:29:02.267 --> 01:29:06.467
<v Efim Podvoiski>Yes, there's a big differences, yeah.</v>

01:29:03.027 --> 01:29:03.347
<v Juan Martinez>Yeah.</v>

01:29:03.707 --> 01:29:09.267
<v Val Levitan>Yeah, yeah, but you feel, you feel, but after the first spin, you forgot that value.</v>

01:29:10.107 --> 01:29:17.267
<v Efim Podvoiski>Yeah, but in our case you you also we also have a spin button, right? You don't have. Oh, you don't.</v>

01:29:13.627 --> 01:29:24.707
<v Val Levitan>No, no, no, no, no, no, no, we do, we do, we do, Efim, we do, we do, but look at our V deck.</v>

01:29:25.907 --> 01:29:38.787
<v Val Levitan>the mass, the total mass of our VDEC, our slam button, although the largest button on the market, it's still, percentage-wise, much smaller than the entire...</v>

01:29:39.947 --> 01:29:45.987
<v Val Levitan>Well-appointed, colorful, big, prevalent, wonderful.</v>

01:29:47.107 --> 01:29:55.427
<v Val Levitan>gorgeous V deck with prominently displayed dollar value saying, schmuck, you're about to bet 5 bucks.</v>

01:29:57.187 --> 01:29:59.987
<v Val Levitan>And, and a fire on that 5 bucks.</v>

01:30:02.147 --> 01:30:04.307
<v Val Levitan>You lighting your 5 bucks on fire.</v>

01:30:05.347 --> 01:30:07.827
<v Val Levitan>I am not sure that I never thought about it.</v>

01:30:09.747 --> 01:30:16.947
<v Val Levitan>I'm thinking about it for the first time. I'm making a theory out of it, but it might be total BS. I have no idea.</v>

01:30:09.987 --> 01:30:11.187
<v Efim Podvoiski>I think of.</v>

01:30:17.507 --> 01:30:19.427
<v Juan Martinez>No, I mean the the the.</v>

01:30:17.507 --> 01:30:26.147
<v Efim Podvoiski>In my mind, once you select it, you just hit play, play, play, play, play. No? Okay.</v>

01:30:23.667 --> 01:30:26.307
<v Michael Gottlieb>No, absolutely not. Not with that VDEC.</v>

01:30:23.987 --> 01:30:25.907
<v Juan Martinez>No, no, no, no, no.</v>

01:30:25.787 --> 01:30:28.867
<v Val Levitan>Not, not on our deck, our deck is a piano.</v>

01:30:29.267 --> 01:30:32.387
<v Michael Gottlieb>Yes, you're all over the damn place. You bet, hi.</v>

01:30:31.107 --> 01:30:42.467
<v Juan Martinez>Yes, and that's not normal player behavior. They go all over the button deck, especially after they've had a big win or they're feeling lucky. So yeah, they're all over.</v>

01:30:43.587 --> 01:30:47.667
<v Val Levitan>My whole point is our deck is a beautiful, gorgeous piano.</v>

01:30:48.947 --> 01:30:53.987
<v Val Levitan>And an aristocrat deck is no choice. Keep on slamming.</v>

01:30:55.267 --> 01:31:01.507
<v Val Levitan>So yes, I mean you could slam 25 cents, but you could also slam something else.</v>

01:30:55.507 --> 01:30:56.067
<v Efim Podvoiski>I would.</v>

01:31:02.387 --> 01:31:04.147
<v Michael Gottlieb>You slam whatever you default to.</v>

01:31:02.907 --> 01:31:12.627
<v Efim Podvoiski>Can they, is it possible to experiment for us to replace some some on some machines, not on all on the same release?</v>

01:31:14.227 --> 01:31:20.867
<v Efim Podvoiski>Because I believe we can software doesn't know and is able to work with VDEC and.</v>

01:31:19.827 --> 01:31:34.707
<v Michael Gottlieb>That's a very expensive, that would be a very expensive test. I think the greater question Efim is that what's the downside of changing it and doing it the way Val is saying? And if Aristocrat's #1 in the marketplace, I just don't see what the downside is.</v>

01:31:38.267 --> 01:31:44.387
<v Efim Podvoiski>At least if you are making a mistake in this direction, it's mistakes that everybody will be making soon.</v>

01:31:44.867 --> 01:32:05.347
<v Michael Gottlieb>Again, I don't call it a mistake. I mean, I hear what you're saying, Juan, that they're taking old hardware and repurposing it, but you can't tell me that they haven't spent, you know, hundreds of thousands of dollars on play test, player focus groups, meeting with customers. What's the customer need? And if they can shave, if they don't need a freaking VDEC, they're not going to ship it with a VDEC.</v>

01:31:50.547 --> 01:31:50.867
<v Juan Martinez>Yeah.</v>

01:31:57.907 --> 01:31:59.107
<v Juan Martinez>Oh, of course they have.</v>

01:32:05.747 --> 01:32:07.747
<v Michael Gottlieb>If they can get away with it, then so be it.</v>

01:32:08.267 --> 01:32:09.347
<v Juan Martinez>Yeah, definitely.</v>

01:32:13.667 --> 01:32:28.307
<v Juan Martinez>And we keep all the bets that we have today, six or seven buttons a theme. We don't change any of that. It's just that you're not directly going to the bet. You've got to go up or down to select your bet.</v>

01:32:27.587 --> 01:32:33.187
<v Efim Podvoiski>Yeah, I understand. Yeah, I understand what you're talking about. Yes, it's possible to select here, so...</v>

01:32:28.907 --> 01:32:29.187
<v Michael Gottlieb>Yeah.</v>

01:32:34.987 --> 01:32:35.347
<v Efim Podvoiski>Okay.</v>

01:32:36.987 --> 01:32:38.787
<v Michael Gottlieb>Are we taking a bathroom break?</v>

01:32:40.707 --> 01:32:41.027
<v Efim Podvoiski>Have you?</v>

01:32:41.907 --> 01:32:43.107
<v Michael Gottlieb>I, I, I am.</v>

01:32:43.827 --> 01:32:44.307
<v Efim Podvoiski>Okay.</v>

01:32:44.187 --> 01:32:46.787
<v Michael Gottlieb>He's muted, so I'm dropping off for a minute.</v>

01:32:47.027 --> 01:32:47.507
<v Efim Podvoiski>You.</v>

01:35:33.907 --> 01:35:34.867
<v Efim Podvoiski>I just want to...</v>

01:35:36.147 --> 01:35:41.267
<v Efim Podvoiski>It mentions that, uh, it's totally replaced of the mask.</v>

01:35:46.627 --> 01:35:47.267
<v Efim Podvoiski>close the board.</v>

01:35:50.867 --> 01:35:51.587
<v Efim Podvoiski>Totally do.</v>

01:35:54.827 --> 01:35:57.827
<v Lena Zhukova>Hi, you're on mute, Mike, you're muted.</v>

01:35:59.027 --> 01:36:03.267
<v Michael Gottlieb>Yeah, this would be for V4. It would be for V4, so we'll have...</v>

01:36:02.387 --> 01:36:03.907
<v Lena Zhukova>Oh, it was Florida.</v>

01:36:04.227 --> 01:36:05.027
<v Michael Gottlieb>We'll have time.</v>

01:36:12.227 --> 01:36:21.187
<v Michael Gottlieb>I mean, we have a lot of theories of theme. Obviously, getting V3 deployed is going to be one of the most valuable things that we can do.</v>

01:36:20.067 --> 01:36:31.267
<v Lena Zhukova>And we, we, if we squeeze a little bit like buttons, we have actually like space here for 15 things, like, I mean, we, we, we move everything a little bit up and put here.</v>

01:36:29.107 --> 01:36:36.467
<v Val Levitan>I think, I think that I think that line and ways should be a single.</v>

01:36:37.347 --> 01:36:38.227
<v Val Levitan>Single row.</v>

01:36:43.187 --> 01:36:48.987
<v Michael Gottlieb>It didn't look good like that and you just said you want to focus on the progressive and it says speech right.</v>

01:36:46.867 --> 01:36:49.107
<v Lena Zhukova>Yeah, we want to promote to fix.</v>

01:36:48.507 --> 01:36:56.947
<v Val Levitan>No, no, no, no, not the actual games, like you're putting six games, we should probably have a single row.</v>

01:36:58.147 --> 01:37:02.787
<v Lena Zhukova>But if we are going to have seven games, icons is going to be very small.</v>

01:37:02.867 --> 01:37:05.027
<v Michael Gottlieb>Yeah, the icons shrink significantly.</v>

01:37:05.827 --> 01:37:07.187
<v Lena Zhukova>It's a vertical screen.</v>

01:37:08.547 --> 01:37:08.867
<v Lena Zhukova>Yeah.</v>

01:37:09.907 --> 01:37:24.387
<v Lena Zhukova>Yeah, I we have space to add two games here and one more games on this row, so yeah, it it will work. I mean, 15 games, yeah, we have, yeah, we can we can position soon.</v>

01:37:26.467 --> 01:37:28.067
<v Val Levitan>It doesn't have to be 15.</v>

01:37:29.427 --> 01:37:30.627
<v Val Levitan>Could be 14.</v>

01:37:30.867 --> 01:37:42.067
<v Michael Gottlieb>14 is a great number. 14 would visually look, in fact, to that point, maybe now is a good time. Well, actually, Val, can we shift gears or do you want to continue on with this discussion?</v>

01:37:32.547 --> 01:37:32.747
<v Lena Zhukova>Yeah.</v>

01:37:41.987 --> 01:37:45.427
<v Val Levitan>No, no, no, we could shoot gears any way you want.</v>

01:37:45.667 --> 01:37:55.987
<v Michael Gottlieb>Okay, so I'd like to shift gears just because this is all kind of within the same space. Lena, can you go ahead and show that game selection screen?</v>

01:37:57.267 --> 01:37:58.467
<v Michael Gottlieb>That you were working on.</v>

01:37:57.587 --> 01:38:00.947
<v Lena Zhukova>For for South Dakota Vitaliy.</v>

01:37:59.907 --> 01:38:01.267
<v Michael Gottlieb>Yeah, the Kinos.</v>

01:38:00.227 --> 01:38:05.267
<v Val Levitan>Just keep, just keep, just keep in mind, I'm only giving you my input. I'm not an expert.</v>

01:38:04.787 --> 01:38:05.107
<v Michael Gottlieb>Right.</v>

01:38:07.587 --> 01:38:18.307
<v Lena Zhukova>Yeah, that's for South South Dakota D27 #3 like.</v>

01:38:08.507 --> 01:38:09.827
<v Michael Gottlieb>OK, so zoom in.</v>

01:38:17.987 --> 01:38:38.347
<v Michael Gottlieb>Right. So this is the proposed, this is just a mock-up. We can move things around as we see fit, but this is the proposed game list and interface for South Dakota D2703, because Val you said you don't want vertical there now.</v>

01:38:38.627 --> 01:38:43.507
<v Michael Gottlieb>At least at this point, you want us to continue with dual screen. Is that still?</v>

01:38:42.787 --> 01:38:43.427
<v Val Levitan>Yes.</v>

01:38:42.787 --> 01:38:52.467
<v Lena Zhukova>For D27, we can easily put six games in one line and it looks good because monitor is white. Yeah, and icons will be big enough.</v>

01:38:58.307 --> 01:39:17.427
<v Michael Gottlieb>And this is preliminary. Juan still has to evaluate the games, determine if this is what he wants, determine if we really do want to add both Fiery Ice Link and Jackpot Rush to this offering. But there is more Keno. We've got the two Kenos that we've done, and then we'll add Solar Keno, and then I'm pitching Juan on Queen of Luxor Keno.</v>

01:39:17.667 --> 01:39:23.667
<v Michael Gottlieb>Because IGT's got a Cleopatra, you know, that is a standby, you know, standard.</v>

01:39:24.707 --> 01:39:27.587
<v Val Levitan>So, so I think that.</v>

01:39:32.467 --> 01:39:35.827
<v Val Levitan>First of all, I love it. It's beautiful.</v>

01:39:37.187 --> 01:39:43.427
<v Val Levitan>But I would like to add something that most likely the number of keynote games will be growing.</v>

01:39:45.827 --> 01:39:46.627
<v Val Levitan>And.</v>

01:39:48.187 --> 01:40:07.387
<v Val Levitan>By a lot, because from when I traversed through all the locations in South Dakota, and I went to a lot of locations, I had a massive list, I hired a driver and drove throughout, I don't know, countless number of locations. Kino is.</v>

01:40:07.507 --> 01:40:07.907
<v Val Levitan>Martha.</v>

01:40:09.747 --> 01:40:10.307
<v Val Levitan>Martha.</v>

01:40:11.187 --> 01:40:13.427
<v Val Levitan>I will go see you at 20 Keno games.</v>

01:40:17.787 --> 01:40:27.347
<v Val Levitan>So why I'm saying this? Because I think that this particular layout lends itself beautifully to multiple carousels.</v>

01:40:31.987 --> 01:40:33.107
<v Val Levitan>Like, scrolling.</v>

01:40:37.027 --> 01:40:51.267
<v Michael Gottlieb>I watched a video of you struggle with that carousel from Primero, where you wanted to pick the lion game, and you scrolled, you scrolled too far, you scrolled back, and it was 3 layers deep.</v>

01:40:50.387 --> 01:41:04.627
<v Val Levitan>Because because it was implemented incorrectly, but Lena has implemented carousel on our video game and it worked beautifully.</v>

01:41:08.067 --> 01:41:09.267
<v Juan Martinez>You mean on echo?</v>

01:41:09.747 --> 01:41:14.707
<v Val Levitan>Yeah, on amusement echo, Lena created carousel.</v>

01:41:15.667 --> 01:41:16.227
<v Val Levitan>With.</v>

01:41:19.907 --> 01:41:23.107
<v Val Levitan>See-through, see-through tiles.</v>

01:41:24.547 --> 01:41:26.787
<v Val Levitan>And we're talking about 30 years ago.</v>

01:41:27.867 --> 01:41:31.907
<v Val Levitan>whatever, 20 years ago, that was very revolutionary.</v>

01:41:33.667 --> 01:41:34.627
<v Lena Zhukova>But now.</v>

01:41:33.667 --> 01:41:49.827
<v Val Levitan>I'm not saying that it should be implemented now. I'm just, all I'm saying is that I'm complimenting you on the layout and I see that it could be continued with more games in here in the form of multiple carousels.</v>

01:41:52.747 --> 01:41:57.267
<v Michael Gottlieb>When you use the figure of speech multiple carousels, you're referring to on.</v>

01:41:56.467 --> 01:42:00.147
<v Val Levitan>Fiery, fiery ice link, a jackpot.</v>

01:41:58.467 --> 01:42:14.627
<v Michael Gottlieb>Yeah, yeah. No, but what I'm saying, right, no, but just so I understand, so I'm clear, underneath Kino, you would physically swipe where the Kino game icons are and additional Kino game icons would come up. Is that accurate?</v>

01:42:02.947 --> 01:42:03.907
<v Val Levitan>Sorry, sorry.</v>

01:42:15.507 --> 01:42:22.787
<v Val Levitan>But I would not point arrows left and right. I would make it a visual infinity.</v>

01:42:19.907 --> 01:42:20.627
<v Michael Gottlieb>Right, okay.</v>

01:42:24.947 --> 01:42:26.787
<v Val Levitan>On the left and on the right.</v>

01:42:25.347 --> 01:42:25.907
<v Michael Gottlieb>Okay.</v>

01:42:30.787 --> 01:42:31.267
<v Michael Gottlieb>Okay.</v>

01:42:32.547 --> 01:42:34.387
<v Michael Gottlieb>Okay, well, that that will get...</v>

01:42:33.107 --> 01:42:34.307
<v Lena Zhukova>I, I, I...</v>

01:42:33.667 --> 01:42:51.347
<v Val Levitan>But I'm only assuming that this keynote will evolve into 10 keynote games and 15 keynote games. Then what do you do? And this is a restrictive frame of horizontal layout and you kind of stuck in it.</v>

01:42:53.667 --> 01:42:58.227
<v Val Levitan>If you are planning to put more games, I don't know if you want more games, maybe you don't.</v>

01:42:58.467 --> 01:43:06.307
<v Michael Gottlieb>Well, sure we do. And I think we're good for, we're probably good for this release. And the next release, if we add two more Keynote, you know.</v>

01:42:59.467 --> 01:42:59.707
<v Lena Zhukova>Yeah.</v>

01:43:05.587 --> 01:43:07.907
<v Val Levitan>Yeah, you will still be good.</v>

01:43:09.027 --> 01:43:13.587
<v Val Levitan>But, but, uh, link games, you will be a...</v>

01:43:14.667 --> 01:43:18.307
<v Val Levitan>Maybe one more per category, that's it, you'll be stuck.</v>

01:43:18.867 --> 01:43:28.467
<v Michael Gottlieb>Right. Well, and I think Juan's point is that he wants to be able to have the operator switch which games are offered to keep it fresh and not offer everything all the time. Right, Juan?</v>

01:43:29.027 --> 01:43:29.347
<v Juan Martinez>Yeah.</v>

01:43:31.747 --> 01:43:38.307
<v Val Levitan>Well, I think this is also a good idea, and then use top screen maybe for advertising.</v>

01:43:42.227 --> 01:43:48.787
<v Val Levitan>But again, don't try me, don't try for me to get creative. That's not going to work.</v>

01:44:00.267 --> 01:44:00.467
<v Juan Martinez>Yeah.</v>

01:44:02.467 --> 01:44:04.627
<v Val Levitan>Easy to understand. Yeah, I like it.</v>

01:44:07.067 --> 01:44:19.507
<v Michael Gottlieb>Great. Yeah, I think Lena did a very nice job with this. So, okay, Juan, let's carry on. Can you please continue to think about, you know, which games you want in there? And we will do Queen of Luxor, Keno.</v>

01:44:22.227 --> 01:44:28.627
<v Michael Gottlieb>And then we will slot that in instead of the South Dakota vertical product.</v>

01:44:28.867 --> 01:44:34.947
<v Lena Zhukova>Yeah, and we will redo solar from vertical to horizontal because I created design for vertical.</v>

01:44:36.627 --> 01:44:39.507
<v Val Levitan>So if I may go back to Georgia Market now.</v>

01:44:39.507 --> 01:44:40.067
<v Michael Gottlieb>Please.</v>

01:44:40.947 --> 01:44:47.267
<v Val Levitan>I think that we should not offer any upgrades for D27 machines.</v>

01:44:50.547 --> 01:44:54.787
<v Val Levitan>And the next trade show, we should show.</v>

01:44:56.867 --> 01:44:58.547
<v Val Levitan>43 inch curve.</v>

01:45:08.867 --> 01:45:09.427
<v Michael Gottlieb>Okay.</v>

01:45:10.667 --> 01:45:12.547
<v Val Levitan>So, I would like...</v>

01:45:14.387 --> 01:45:16.707
<v Val Levitan>to ask if curve</v>

01:45:18.867 --> 01:45:25.267
<v Val Levitan>graphic user interface and the whole presentation could be designed.</v>

01:45:27.267 --> 01:45:29.507
<v Val Levitan>Differently from V43.</v>

01:45:32.227 --> 01:45:41.107
<v Michael Gottlieb>I think we just did. I mean, I think we just went through all the changes that we want, which will be an evolution. It'll still be liquid glass, but by putting the bets.</v>

01:45:40.387 --> 01:45:45.427
<v Val Levitan>No, I'm saying, no, no, maybe, maybe you, maybe I don't say it correctly.</v>

01:45:45.187 --> 01:45:45.507
<v Michael Gottlieb>Yeah.</v>

01:45:46.547 --> 01:45:47.587
<v Val Levitan>Vertical.</v>

01:45:48.747 --> 01:45:49.667
<v Val Levitan>And curve.</v>

01:45:50.507 --> 01:45:52.067
<v Val Levitan>Should not look the same.</v>

01:45:53.747 --> 01:45:54.387
<v Michael Gottlieb>Why?</v>

01:45:57.267 --> 01:45:57.987
<v Val Levitan>I don't know.</v>

01:45:58.467 --> 01:46:03.587
<v Lena Zhukova>With with the same games, but a different look, or yeah, games should be different.</v>

01:46:03.667 --> 01:46:10.227
<v Michael Gottlieb>That's a that's basically a violation of branding 101 if we're trying to establish JVL branding comfort.</v>

01:46:04.067 --> 01:46:04.867
<v Val Levitan>No.</v>

01:46:09.267 --> 01:46:10.107
<v Val Levitan>No, no.</v>

01:46:10.947 --> 01:46:17.747
<v Val Levitan>No, for example, our D27 does not look the same as vertical.</v>

01:46:18.547 --> 01:46:21.747
<v Michael Gottlieb>Correct, because it's because it's yeah.</v>

01:46:18.827 --> 01:46:25.467
<v Val Levitan>There is resemblance, yeah, because of the monitor orientation and...</v>

01:46:26.107 --> 01:46:32.707
<v Michael Gottlieb>Right, but because the design is, right, the design has evolved. I would suggest that the current design we...</v>

01:46:26.627 --> 01:46:28.387
<v Val Levitan>Screen screen geometry.</v>

01:46:28.987 --> 01:46:29.267
<v Juan Martinez>Yeah.</v>

01:46:30.867 --> 01:46:31.187
<v Juan Martinez>Yeah.</v>

01:46:31.827 --> 01:46:47.587
<v Val Levitan>No, not because design has evolved. Let's assume that both designs are the same implementation. So liquid glass here and liquid glass on D27.</v>

01:46:43.347 --> 01:46:43.827
<v Michael Gottlieb>Right.</v>

01:46:49.107 --> 01:46:54.307
<v Val Levitan>But because of the screen geometry, it will not look identical.</v>

01:46:55.267 --> 01:46:59.587
<v Michael Gottlieb>Right, but the aspect ratio of curve is the same as the aspect ratio of vertical.</v>

01:46:59.827 --> 01:47:00.347
<v Lena Zhukova>Mhm.</v>

01:46:59.907 --> 01:47:19.627
<v Juan Martinez>No, I think what Val was saying is how can we do a liquid glass plus for the curve to make it appear as a premium, a more premium product? Just to refresh visually to make it a little more eye-catching is how I'm taking what he's trying to say.</v>

01:47:21.427 --> 01:47:25.907
<v Michael Gottlieb>Right, but the one that we've just done hasn't even been deployed yet.</v>

01:47:21.827 --> 01:47:22.307
<v Juan Martinez>Hello.</v>

01:47:26.787 --> 01:47:47.067
<v Val Levitan>I understand, I understand, but I'm hoping that during this year, leading up to the trade show in 2027, especially, hopefully, keeping my fingers crossed, using the promotion that or the special that we are implementing right now,</v>

01:47:26.867 --> 01:47:27.827
<v Juan Martinez>We, we have it done.</v>

01:47:47.347 --> 01:47:56.547
<v Val Levitan>hopefully will put a lot of machines in the market. I'm hoping. And if that happens, and if we introduce...</v>

01:47:58.067 --> 01:48:02.227
<v Val Levitan>Let's call it C for curve, C43.</v>

01:48:04.547 --> 01:48:05.987
<v Val Levitan>How could it be?</v>

01:48:07.027 --> 01:48:10.867
<v Val Levitan>How could it look different from the V43?</v>

01:48:11.987 --> 01:48:12.787
<v Val Levitan>It's a question.</v>

01:48:14.907 --> 01:48:16.147
<v Val Levitan>And is it even possible?</v>

01:48:17.427 --> 01:48:20.307
<v Val Levitan>I mean, surely it's possible. Clearly it's possible, but...</v>

01:48:17.587 --> 01:48:18.147
<v Michael Gottlieb>I mean it.</v>

01:48:17.667 --> 01:48:18.307
<v Juan Martinez>Okay.</v>

01:48:20.867 --> 01:48:33.267
<v Michael Gottlieb>It's possible, but it is extremely unconventional. Our competitors don't do it. Curve is just a different, curve is the same as a vertical in the minds of...</v>

01:48:32.867 --> 01:48:46.067
<v Juan Martinez>Well, Michael, a lot of them launched premium products on Curve. And while that's gone less and less, we're just trying to say, if we want to sell Curve for $1,000 more, how do I get there visually?</v>

01:48:46.387 --> 01:48:56.227
<v Lena Zhukova>But they should be premium not only for the reason of difference in home screen, probably games different, like more premium games, I don't know, some licensed games or whatever.</v>

01:48:57.347 --> 01:49:09.427
<v Juan Martinez>Yeah, I mean, I don't think we're there yet for licensed games, but what just can we do to make a premium, a curve look a little more expensive than a V43? That's it.</v>

01:49:09.107 --> 01:49:14.547
<v Lena Zhukova>But this is the same games. I mean, like if you want to change home screen, will it feel like...</v>

01:49:14.387 --> 01:49:22.147
<v Michael Gottlieb>No, it's not the home screen. It's the they're talking about maybe changing the dashboard. I mean, let us let us give some thought to it. I.</v>

01:49:17.427 --> 01:49:17.747
<v Lena Zhukova>I.</v>

01:49:20.627 --> 01:49:20.907
<v Juan Martinez>Yeah.</v>

01:49:21.587 --> 01:49:24.947
<v Lena Zhukova>But, but games should stay the same, I mean, still complete.</v>

01:49:24.587 --> 01:49:31.987
<v Michael Gottlieb>No, no, we'll have more new games for that release and then we'll also have our tried and true, we'll have a blend.</v>

01:49:29.267 --> 01:49:30.147
<v Lena Zhukova>Ah, okay.</v>

01:49:32.947 --> 01:49:33.267
<v Lena Zhukova>Oh.</v>

01:49:32.947 --> 01:49:37.827
<v Michael Gottlieb>Right, you're going to want a blend of the stuff that has been crushing it, just like Aristocrat.</v>

01:49:38.147 --> 01:49:48.307
<v Lena Zhukova>So for this, for this C43, we are going to have 15 games on the screen and all these changes we just discussed.</v>

01:49:48.787 --> 01:49:49.267
<v Michael Gottlieb>Yes.</v>

01:49:48.947 --> 01:49:56.227
<v Val Levitan>I don't know, can I fire a stupid crazy idea and if you don't like it, trash it.</v>

01:49:56.307 --> 01:49:57.107
<v Michael Gottlieb>Go for it.</v>

01:49:58.387 --> 01:50:14.147
<v Val Levitan>Maybe Curve should be a collection of large format premium type of games. Instead of collection of multiple games, it's a collection of only premium games.</v>

01:50:16.627 --> 01:50:38.387
<v Michael Gottlieb>I don't think that's where the market is headed based upon what our competitors are doing. If anything, they're going further and further back in their library to older and older, crappier looking games for these markets. I mean, not in all cases and not in all instances, and nor would I ever suggest that we don't have the best looking games we possibly can.</v>

01:50:38.787 --> 01:50:44.947
<v Michael Gottlieb>But they've got a lot of older stuff in their library that they're introducing as part of their releases.</v>

01:50:45.347 --> 01:50:48.387
<v Val Levitan>Let me, let me explain to you what's happening in the...</v>

01:50:50.147 --> 01:50:59.587
<v Val Levitan>the way I read the market. And this is something that I really understand very well, and this is my strong thing. This is, like, I read markets very well.</v>

01:51:01.107 --> 01:51:10.707
<v Val Levitan>This is, so first of all, the market, so you guys understand, it's 47,000 machines in 7,400 locations.</v>

01:51:11.787 --> 01:51:14.147
<v Val Levitan>with 5.9 machines per location.</v>

01:51:18.147 --> 01:51:24.387
<v Val Levitan>Two years ago, it was 35,000 machines in 6,200 locations.</v>

01:51:26.067 --> 01:51:33.107
<v Val Levitan>And when I started Georgia Market, it was 25,000 machines in 5,000 locations.</v>

01:51:34.827 --> 01:51:35.907
<v Val Levitan>That was five years ago.</v>

01:51:40.387 --> 01:51:47.827
<v Val Levitan>The market is mainly C stores, convenience stores, gas station stores, variety stores, 7-Eleven.</v>

01:51:50.307 --> 01:51:51.027
<v Val Levitan>Um...</v>

01:51:52.107 --> 01:52:05.667
<v Val Levitan>dirty locations for the most part, poor service, machines are usually locked up in a small room or in between the boxes and cases.</v>

01:52:06.947 --> 01:52:07.667
<v Val Levitan>Something.</v>

01:52:09.027 --> 01:52:09.667
<v Val Levitan>Dusty.</v>

01:52:11.587 --> 01:52:15.107
<v Val Levitan>And it's run by Indians and Pakistanis.</v>

01:52:17.227 --> 01:52:18.387
<v Val Levitan>Not even careers.</v>

01:52:21.267 --> 01:52:29.427
<v Val Levitan>And it's a Uber super duper Uber gossipy environment.</v>

01:52:31.187 --> 01:52:33.747
<v Val Levitan>And so the advertising there works.</v>

01:52:35.187 --> 01:52:37.347
<v Val Levitan>Basically, Sam.</v>

01:52:38.787 --> 01:52:41.027
<v Val Levitan>Every self-respected.</v>

01:52:42.987 --> 01:52:55.427
<v Val Levitan>C-store owner, if they don't have this machine, that means you are antiquated, like you're, you're not, yeah, you're less, you're less in your in your.</v>

01:52:51.147 --> 01:52:51.907
<v Michael Gottlieb>You're less than.</v>

01:52:57.507 --> 01:53:02.307
<v Michael Gottlieb>status and the culture and the ranking of the Indian fellows who talk to each other at the temple.</v>

01:53:03.987 --> 01:53:04.627
<v Val Levitan>Bridal.</v>

01:53:05.747 --> 01:53:18.947
<v Val Levitan>So, by creating a curve machine of a premium brand, and by the way, Sam doesn't buy machines. It's the operator that buys machines, and the operator will buy whatever Sam wants.</v>

01:53:22.227 --> 01:53:30.227
<v Val Levitan>And Sam will put his choice of a machine in a premium location within the ****** location.</v>

01:53:32.067 --> 01:53:33.347
<v Val Levitan>So less dusty.</v>

01:53:35.267 --> 01:53:36.227
<v Val Levitan>Less crappy.</v>

01:53:38.467 --> 01:53:44.307
<v Val Levitan>more convenient. Let me give you an example. Like, it will blow you away.</v>

01:53:45.907 --> 01:53:49.067
<v Val Levitan>We wanted to test our machine with an operator.</v>

01:53:50.947 --> 01:53:57.907
<v Val Levitan>He placed, he brought our machine and it seems like the location owner really didn't want it.</v>

01:53:58.987 --> 01:54:00.707
<v Val Levitan>But he probably forced them into it.</v>

01:54:01.867 --> 01:54:08.147
<v Val Levitan>So, you placed our machine next to an ice maker the size of a small tank.</v>

01:54:09.747 --> 01:54:11.027
<v Val Levitan>And the ice maker.</v>

01:54:12.387 --> 01:54:23.027
<v Val Levitan>Every 3 minutes, crushes the ice. The ice falls in the bucket, like a, like a, with a crazy sound, you know, like something is smashing.</v>

01:54:24.307 --> 01:54:36.227
<v Val Levitan>So machine is not close to the ice maker. Machine is touching the ice maker, but it's not next. They're not.</v>

01:54:37.347 --> 01:54:48.787
<v Val Levitan>side to side, they're kind of 90 degrees. So you sit at the throat where the thing opens up, the hood opens up, and you grab your eyes.</v>

01:54:49.667 --> 01:54:51.987
<v Val Levitan>So, your chair is...</v>

01:54:54.627 --> 01:55:00.867
<v Val Levitan>prohibiting the door opening of the ice maker. You're an obstruction, yeah, you're an obstruction.</v>

01:54:56.867 --> 01:54:59.427
<v Michael Gottlieb>Right, you're an obstruction. You're an obstruction.</v>

01:55:05.507 --> 01:55:10.467
<v Val Levitan>You don't want that spot. You want to be a jam of a location.</v>

01:55:13.507 --> 01:55:27.987
<v Val Levitan>And V27 or V43 already at this stage is not going to be a gem. But what is a gem, and especially if Sam wants it and made an operator buy it for him, is going to be</v>

01:55:29.187 --> 01:55:30.987
<v Val Levitan>Prime location exposed.</v>

01:55:32.147 --> 01:55:33.747
<v Val Levitan>Sam will make sure of it.</v>

01:55:39.747 --> 01:55:43.107
<v Val Levitan>So I'm trying to create a visual candy.</v>

01:55:46.547 --> 01:55:48.067
<v Val Levitan>Sorry, unusual.</v>

01:55:49.187 --> 01:55:50.307
<v Val Levitan>Visual camping.</v>

01:55:59.707 --> 01:56:00.227
<v Michael Gottlieb>Guzzles.</v>

01:56:01.867 --> 01:56:02.307
<v Val Levitan>Mm.</v>

01:56:02.867 --> 01:56:04.227
<v Michael Gottlieb>Lights, bezels.</v>

01:56:05.107 --> 01:56:05.587
<v Val Levitan>Yeah.</v>

01:56:06.227 --> 01:56:08.547
<v Michael Gottlieb>To think that things gotta have.</v>

01:56:09.747 --> 01:56:12.067
<v Michael Gottlieb>some serious visual presence to it.</v>

01:56:20.347 --> 01:56:27.907
<v Michael Gottlieb>And maybe, you know, do you remember the, well, candles? You remember candles on slot machines?</v>

01:56:28.787 --> 01:56:29.107
<v Juan Martinez>Push.</v>

01:56:29.187 --> 01:56:31.027
<v Val Levitan>Candles? Yeah, of course, yeah.</v>

01:56:29.427 --> 01:56:45.667
<v Michael Gottlieb>The light? Yeah, exactly. So instead of a candle, you know, one of those red dome police lights that when you get a jackpot, the thing's got a reflective thing in it and it rotates around and flashes red all over the place.</v>

01:56:30.267 --> 01:56:30.547
<v Lena Zhukova>And.</v>

01:56:30.387 --> 01:56:31.827
<v Juan Martinez>They're still, they're still there.</v>

01:56:47.987 --> 01:56:49.747
<v Michael Gottlieb>Conceptually, something like that.</v>

01:56:54.067 --> 01:56:54.707
<v Val Levitan>So.</v>

01:56:54.307 --> 01:56:57.267
<v Michael Gottlieb>A projector that projects the word winner onto the ceiling.</v>

01:56:58.227 --> 01:57:04.787
<v Val Levitan>So it's interesting what I've noticed in our showroom we have two machines and it never actually...</v>

01:56:58.867 --> 01:56:59.107
<v Juan Martinez>But.</v>

01:57:07.827 --> 01:57:28.307
<v Val Levitan>I never actually thought about it from a visual perspective, but when you play your jackpot rush on any bet and you bet 25 cents and you have this ****** jackpots, little ones, and then somebody plays $4 and the two machines side by side, you know how much status it is?</v>

01:57:28.707 --> 01:57:36.787
<v Val Levitan>for people to see what you're bearing. I never realized, but visually it's such a provocative.</v>

01:57:31.387 --> 01:57:31.827
<v Michael Gottlieb>Sure.</v>

01:57:37.867 --> 01:57:41.667
<v Val Levitan>You know, I don't know how to express myself, but...</v>

01:57:44.147 --> 01:57:46.227
<v Val Levitan>The status symbol, I guess.</v>

01:57:46.547 --> 01:57:46.947
<v Michael Gottlieb>Right.</v>

01:57:48.867 --> 01:57:55.667
<v Val Levitan>What are you betting? Like, look at your jackpots. Like, you should be ashamed. Get out of here. Like, don't sit next to me, you peasant.</v>

01:57:57.867 --> 01:58:12.547
<v Michael Gottlieb>And the people with the big bankrolls' chests are puffed up, and when they win free spins on 5 bucks a bet, or they win a big scatter at 5 bucks a bet, they lean back in their chair and they look around to see if people were watching their win.</v>

01:58:02.467 --> 01:58:03.187
<v Val Levitan>Yeah.</v>

01:58:08.747 --> 01:58:09.427
<v Val Levitan>You know that?</v>

01:58:14.227 --> 01:58:24.867
<v Val Levitan>The operators, when they get to a meeting, they arrive, they drive themselves in, you'll never guess what car, in Maybach.</v>

01:58:27.747 --> 01:58:29.587
<v Michael Gottlieb>Ohh, okay, yeah, yep.</v>

01:58:30.307 --> 01:58:34.307
<v Val Levitan>My boss is a top line of Mercedes.</v>

01:58:39.267 --> 01:58:41.507
<v Val Levitan>Their net worth, I don't know this.</v>

01:58:43.187 --> 01:58:45.027
<v Val Levitan>Not, not my buck net worth.</v>

01:58:46.547 --> 01:58:54.467
<v Michael Gottlieb>But image is everything. Perception, image, how you portray yourself, how you carry yourself, who you are in the community.</v>

01:58:52.867 --> 01:58:58.467
<v Val Levitan>That's that's so that's the master operator, and obviously.</v>

01:59:00.147 --> 01:59:04.867
<v Val Levitan>the same status symbols throughout the chain of commands.</v>

01:59:08.107 --> 01:59:13.187
<v Val Levitan>Very big deal. I think if we properly designed curve screen.</v>

01:59:15.107 --> 01:59:15.747
<v Val Levitan>We can.</v>

01:59:17.027 --> 01:59:18.067
<v Val Levitan>Have a good year.</v>

01:59:23.347 --> 01:59:29.027
<v Val Levitan>And we're now advertising in the location-based.</v>

01:59:30.627 --> 01:59:31.507
<v Val Levitan>Newspaper.</v>

01:59:43.427 --> 02:00:00.947
<v Michael Gottlieb>Chrome, Chrome might be back, Juan. If you remember, everything was Chrome, and then the trend was black, black, black, black, powder coat, black, everything. But the type of customer that you're talking about, basically the bling, there's a bling factor.</v>

01:59:48.627 --> 01:59:49.267
<v Juan Martinez>Oh yeah.</v>

02:00:01.907 --> 02:00:03.027
<v Michael Gottlieb>That they're looking for.</v>

02:00:05.027 --> 02:00:25.907
<v Juan Martinez>Yeah, we just have to balance it because as Val, I mean, these are 50% ****** locations. Your machines are blocked by some partial wall. No one can see them unless you go to that gas station on a daily basis. So it's bling, but it's obscured.</v>

02:00:25.987 --> 02:00:34.307
<v Juan Martinez>you know, because you're not, this isn't a casino floor where you could see the machine from 20 feet away. So some of it could be wasteful.</v>

02:00:31.907 --> 02:00:32.387
<v Michael Gottlieb>Right.</v>

02:00:32.227 --> 02:00:32.787
<v Val Levitan>You know.</v>

02:00:34.707 --> 02:00:40.947
<v Val Levitan>Chrome, but chrome in the dark looks black, so it's not nice, but the shiny lights.</v>

02:00:39.267 --> 02:00:39.587
<v Juan Martinez>Yeah.</v>

02:00:42.227 --> 02:00:44.467
<v Val Levitan>That curve silhouette.</v>

02:00:45.987 --> 02:00:48.707
<v Val Levitan>That scores, it's unusual.</v>

02:00:52.387 --> 02:00:59.027
<v Val Levitan>And that's why I want to push curve, and that's why I would like visually curve.</v>

02:01:01.107 --> 02:01:05.107
<v Val Levitan>the main screen, the GUI screen, to be slightly different.</v>

02:01:11.107 --> 02:01:12.227
<v Val Levitan>Because I want...</v>

02:01:13.747 --> 02:01:16.707
<v Val Levitan>Sam to come to, you know.</v>

02:01:17.787 --> 02:01:19.667
<v Val Levitan>An association dinner and say...</v>

02:01:21.427 --> 02:01:23.987
<v Val Levitan>I have what you don't have.</v>

02:01:26.947 --> 02:01:29.427
<v Val Levitan>Because I am Sam.</v>

02:01:30.147 --> 02:01:30.387
<v Juan Martinez>Yeah.</v>

02:01:37.267 --> 02:01:48.067
<v Val Levitan>So, it's a status, it's a status symbol society. If we hit this right and have this, like you, you really nailed this interface.</v>

02:01:37.507 --> 02:01:39.187
<v Michael Gottlieb>I understand what you're, yeah.</v>

02:01:51.427 --> 02:01:52.947
<v Val Levitan>Move in a different direction.</v>

02:01:55.147 --> 02:02:00.947
<v Val Levitan>with this next interface. Whatever it is, I don't know, but play with it and.</v>

02:02:03.027 --> 02:02:03.987
<v Val Levitan>You could, you could.</v>

02:02:05.347 --> 02:02:06.467
<v Val Levitan>Reuse games.</v>

02:02:07.987 --> 02:02:12.307
<v Val Levitan>But the initial screen, the invitation, the advertisement.</v>

02:02:13.107 --> 02:02:14.627
<v Val Levitan>Should be my bar.</v>

02:02:16.667 --> 02:02:36.147
<v Juan Martinez>And what's interesting, Michael, is could the effect and the extra glitz and glitter be an on and off switch so that we only have one software and you're just enabling it for the curb, disabling it for the V43 just as a cost reduction?</v>

02:02:38.387 --> 02:02:45.107
<v Michael Gottlieb>Well, I mean, would we continue to do V43 releases or would everything be curved going forward?</v>

02:02:43.987 --> 02:02:50.867
<v Val Levitan>Yeah, yeah, yeah, yeah, yeah, yeah, yeah, yeah, I see before the 43 for probably three years.</v>

02:02:52.707 --> 02:02:54.147
<v Michael Gottlieb>Okay, that says a lot.</v>

02:02:54.547 --> 02:03:05.667
<v Lena Zhukova>Oh, sorry, so we're going to have VV forty-three 4, V4, and in parallel we're going to have curve.</v>

02:03:02.547 --> 02:03:04.787
<v Val Levitan>And 5 and six and seven.</v>

02:03:07.027 --> 02:03:07.747
<v Michael Gottlieb>Lev both.</v>

02:03:07.107 --> 02:03:07.987
<v Lena Zhukova>Two different.</v>

02:03:07.427 --> 02:03:07.907
<v Juan Martinez>Yes.</v>

02:03:08.787 --> 02:03:09.107
<v Juan Martinez>Yeah.</v>

02:03:08.867 --> 02:03:11.587
<v Val Levitan>And, and we will discontinue in D.</v>

02:03:14.387 --> 02:03:32.787
<v Michael Gottlieb>Right, the D27 goes away. So we'll continue on with the V43 for three years, the C43 starting when we launch it to who knows when. But basically, what we're saying is you have a V43 and a C43, we need to reimagine the interface in such a fashion that the C43</v>

02:03:33.107 --> 02:03:38.787
<v Michael Gottlieb>has a come on factor that says this is fresh, this is more expensive, this is new.</v>

02:03:39.267 --> 02:03:40.147
<v Val Levitan>More expensive.</v>

02:03:40.627 --> 02:03:41.027
<v Michael Gottlieb>Right.</v>

02:03:42.547 --> 02:03:43.667
<v Val Levitan>More expensive, yeah.</v>

02:03:46.547 --> 02:03:49.027
<v Val Levitan>And it gives me another leg.</v>

02:03:50.627 --> 02:03:54.627
<v Val Levitan>Like, if you, if you guys come up with, let's say, 15 or 14 game.</v>

02:03:57.827 --> 02:03:58.787
<v Val Levitan>Interface.</v>

02:04:00.387 --> 02:04:05.587
<v Val Levitan>I can now say, well, you no longer have to only...</v>

02:04:06.827 --> 02:04:11.027
<v Val Levitan>Provide 10 games, you could now have 14 games, and you know...</v>

02:04:13.027 --> 02:04:23.667
<v Val Levitan>I can nudge. I need to get closer to 18 plus 1000. Then I can discount it. I could provide more.</v>

02:04:24.547 --> 02:04:25.507
<v Val Levitan>And grab the market.</v>

02:04:27.747 --> 02:04:30.307
<v Val Levitan>If my plan works, then...</v>

02:04:36.947 --> 02:04:37.827
<v Val Levitan>We should.</v>

02:04:41.907 --> 02:04:43.587
<v Val Levitan>Operator should say.</v>

02:04:45.827 --> 02:04:48.067
<v Val Levitan>I'm getting the stuff for free I want.</v>

02:04:49.187 --> 02:04:57.107
<v Val Levitan>I don't even care, but she makes more or less money. I'm getting all this stuff for free. If I'm reading my client correctly.</v>

02:04:56.707 --> 02:04:56.947
<v Juan Martinez>Okay.</v>

02:04:58.227 --> 02:05:00.307
<v Val Levitan>The Indian and Pakistanis.</v>

02:05:03.267 --> 02:05:07.747
<v Val Levitan>That free stuff, that big value should be should have an enormous effect.</v>

02:05:12.227 --> 02:05:13.427
<v Michael Gottlieb>Because they all love a deal.</v>

02:05:16.587 --> 02:05:18.627
<v Val Levitan>And they squeeze the living daylights out of me.</v>

02:05:21.187 --> 02:05:26.067
<v Val Levitan>And there is not, there's nothing more in joyful than squeezing.</v>

02:05:27.587 --> 02:05:29.907
<v Val Levitan>The living daylights out of JVL.</v>

02:05:35.467 --> 02:05:39.667
<v Val Levitan>And so then in 2027, 28.</v>

02:05:40.627 --> 02:05:42.147
<v Val Levitan>I should and should use.</v>

02:05:43.267 --> 02:05:48.947
<v Val Levitan>in the transactional equipment should be something more expensive that they want.</v>

02:05:50.067 --> 02:05:52.227
<v Val Levitan>that we discount or package together.</v>

02:05:54.427 --> 02:05:57.387
<v Val Levitan>And so I need to get to that 18, $19,000.</v>

02:05:59.267 --> 02:05:59.907
<v Val Levitan>Level.</v>

02:06:06.947 --> 02:06:08.467
<v Val Levitan>So that's the strategy.</v>

02:06:15.267 --> 02:06:15.827
<v Juan Martinez>Stir.</v>

02:06:16.467 --> 02:06:18.867
<v Val Levitan>But you nailed, you nailed the screen.</v>

02:06:19.947 --> 02:06:22.947
<v Val Levitan>I would like to go to, let's call it 14 game.</v>

02:06:24.707 --> 02:06:25.107
<v Val Levitan>Um...</v>

02:06:28.067 --> 02:06:28.867
<v Val Levitan>Interface.</v>

02:06:30.067 --> 02:06:32.947
<v Val Levitan>and the large format advertising.</v>

02:06:35.827 --> 02:06:38.307
<v Val Levitan>That's that's gonna that's gonna be nice.</v>

02:06:41.667 --> 02:06:49.507
<v Val Levitan>And let's replace the VDAC. Let's borrow the design idea from Aristocrat.</v>

02:06:50.627 --> 02:06:55.107
<v Val Levitan>I hope we're not making a mistake because I just love VDEC. I think it's...</v>

02:06:57.907 --> 02:07:03.027
<v Val Levitan>Beautiful, but I've learned to understand that whatever I love is not necessarily good.</v>

02:07:04.987 --> 02:07:15.907
<v Michael Gottlieb>Well, the one thing I would say is we have, there's lots of work that Lena and I have to do with both Nebraska and South Dakota right now. So</v>

02:07:16.947 --> 02:07:31.027
<v Michael Gottlieb>it might help to just park these issues for a few weeks and let it have a little oxygen, get some further feedback. Because I mean, we, yeah, I don't want it, I don't, we don't have to make a decision on this this very second. Okay.</v>

02:07:23.987 --> 02:07:25.187
<v Val Levitan>Yeah, yeah, yeah, yeah.</v>

02:07:28.707 --> 02:07:31.587
<v Val Levitan>No, no, no, no, yeah, yeah, I agree.</v>

02:07:32.427 --> 02:07:38.147
<v Val Levitan>But one decision I would make, I would move away from showing dollars on the buttons to credits.</v>

02:07:39.027 --> 02:07:42.467
<v Val Levitan>I recommend for you to do it even in this Giorgi release.</v>

02:07:42.627 --> 02:07:58.787
<v Efim Podvoiski>We cannot, we cannot, we cannot do it like this, because unfortunately the mass is done in this in such a way that there are different denominations in some games, not one sense elimination, so it's not the greatest are not there.</v>

02:08:04.787 --> 02:08:07.267
<v Val Levitan>Is it a matter of taking one game out?</v>

02:08:10.307 --> 02:08:13.427
<v Efim Podvoiski>I would say, to say, I'm not sure.</v>

02:08:14.707 --> 02:08:15.507
<v Efim Podvoiski>Exactly.</v>

02:08:16.227 --> 02:08:19.747
<v Val Levitan>Maybe it's worth it. Maybe it's worth taking two games out.</v>

02:08:16.387 --> 02:08:18.467
<v Efim Podvoiski>I have to check my best.</v>

02:08:20.587 --> 02:08:22.627
<v Efim Podvoiski>Three games, three games is half of.</v>

02:08:20.627 --> 02:08:25.027
<v Juan Martinez>Yeah, but what happens if they're the top two games? We've got to be careful there.</v>

02:08:24.547 --> 02:08:26.387
<v Efim Podvoiski>Crazy Spins is a top game.</v>

02:08:27.587 --> 02:08:29.187
<v Juan Martinez>Don't touch crazy spins.</v>

02:08:27.907 --> 02:08:31.907
<v Efim Podvoiski>Basically, whatever, whatever, yeah.</v>

02:08:28.067 --> 02:08:30.307
<v Michael Gottlieb>Rodeo spins. Rodeo spins.</v>

02:08:31.387 --> 02:08:33.747
<v Michael Gottlieb>our number one performer by a substantial margin.</v>

02:08:36.147 --> 02:08:51.267
<v Michael Gottlieb>I would not suggest making that change, Val. I think what you've put forth are some interesting theories. I think there's definitely potentially some foundation to the theories. But I think that's a pretty substantial change without more data.</v>

02:08:50.467 --> 02:08:50.947
<v Val Levitan>Okay.</v>

02:08:52.067 --> 02:09:08.147
<v Efim Podvoiski>I understand people cannot count in two cent and two and five cents 50 credits is not 200 is not $2.50 that I understand, but 600 and dollar on one cent I think it's.</v>

02:08:53.827 --> 02:08:55.267
<v Val Levitan>Fair enough, fair enough.</v>

02:09:09.987 --> 02:09:12.787
<v Efim Podvoiski>How will you tell that you should be not to understand?</v>

02:09:14.707 --> 02:09:17.587
<v Juan Martinez>Well, I've met some really dumb people in the casinos.</v>

02:09:14.867 --> 02:09:16.627
<v Michael Gottlieb>Okay, we're good at team, we put the, we're done.</v>

02:09:15.987 --> 02:09:18.667
<v Val Levitan>You'll be, you'll be, you'll be surprised.</v>

02:09:18.867 --> 02:09:19.267
<v Juan Martinez>Yeah.</v>

02:09:18.947 --> 02:09:22.787
<v Efim Podvoiski>Yeah, I, I, you probably have to be if you play this machines here, but...</v>

02:09:23.347 --> 02:09:36.307
<v Val Levitan>And you know what, I can tell you there is another element. There is one thing betting $6, which you're not really a millionaire. It's another thing betting 600 things on it.</v>

02:09:37.427 --> 02:09:41.667
<v Val Levitan>Like 600, you're almost a millionaire, and $6 you're an idiot.</v>

02:09:45.027 --> 02:09:49.907
<v Val Levitan>Like, like if you're already spending, spend 600 / 6.</v>

02:09:53.467 --> 02:09:59.827
<v Efim Podvoiski>Hmm, interesting. Yeah, yeah, I understand. I kind of understand. Unfortunately, unfortunately, it was never...</v>

02:09:57.587 --> 02:10:00.627
<v Juan Martinez>Don't forget you're on your 4th, you're on your 4th beer.</v>

02:09:59.427 --> 02:10:07.987
<v Val Levitan>Like, like, like 600, like 600, like, you're ******* betting, like, ah, 600, well, 6.</v>

02:10:17.427 --> 02:10:19.827
<v Val Levitan>I don't know, these are my theories, so I don't know.</v>

02:10:24.227 --> 02:10:25.747
<v Val Levitan>Not really sure that it's true.</v>

02:10:32.787 --> 02:10:33.987
<v Val Levitan>Okay, what else?</v>

02:10:35.667 --> 02:10:36.947
<v Michael Gottlieb>I think that covers it.</v>

02:10:38.387 --> 02:10:55.827
<v Lena Zhukova>So I have a question. Next, because Nebraska design stage is done, so next product for concept and design is G27 Dakota, right? Not vertical as we previously saw. Okay.</v>

02:10:51.907 --> 02:10:52.547
<v Val Levitan>Yes.</v>

02:10:53.827 --> 02:10:54.187
<v Val Levitan>Inna.</v>

02:10:56.667 --> 02:10:59.587
<v Michael Gottlieb>Yeah, South Dakota D2703.</v>

02:11:01.907 --> 02:11:06.107
<v Val Levitan>And you're staying with D27 in Nebraska.</v>

02:11:06.627 --> 02:11:07.187
<v Lena Zhukova>Yes.</v>

02:11:07.347 --> 02:11:07.747
<v Michael Gottlieb>Yes.</v>

02:11:07.587 --> 02:11:08.867
<v Val Levitan>Yes, yes, yes.</v>

02:11:09.987 --> 02:11:16.307
<v Val Levitan>And View 43, we're going to continue View 43, version 456 in Georgia.</v>

02:11:18.627 --> 02:11:27.707
<v Lena Zhukova>And another question, we discussed that this vertical South Dakota, we are going to move to Nova.</v>

02:11:27.027 --> 02:11:28.787
<v Val Levitan>Yes, yes.</v>

02:11:30.147 --> 02:11:31.827
<v Val Levitan>Much better than I expected.</v>

02:11:33.187 --> 02:11:34.707
<v Michael Gottlieb>So that's the next release then.</v>

02:11:35.267 --> 02:11:40.947
<v Lena Zhukova>So, get 27 South Dakota, we move into Nova, OK.</v>

02:11:35.587 --> 02:11:36.067
<v Val Levitan>Yeah.</v>

02:11:41.027 --> 02:11:47.987
<v Val Levitan>Yes, yes. But anything that we're moving into Nova starting 1st of October.</v>

02:11:42.387 --> 02:11:43.627
<v Lena Zhukova>It's important.</v>

02:11:50.467 --> 02:12:04.547
<v Juan Martinez>But just from a compliance standpoint, do we want to deal with GLI and Nova this early? Or should Eclipse get Nova first to help us troubleshoot anything?</v>

02:12:07.187 --> 02:12:11.187
<v Val Levitan>Okay, I understand where you're coming from. I was there myself.</v>

02:12:12.787 --> 02:12:16.627
<v Val Levitan>Let me tell you what I think. I think that...</v>

02:12:17.387 --> 02:12:19.907
<v Val Levitan>Eclipse doesn't test anything.</v>

02:12:20.987 --> 02:12:22.787
<v Val Levitan>Eclipse only tests us.</v>

02:12:24.707 --> 02:12:28.787
<v Val Levitan>And so it's quite pointless to rely on Eclipse.</v>

02:12:30.067 --> 02:12:30.787
<v Val Levitan>Fredy.</v>

02:12:31.987 --> 02:12:36.587
<v Val Levitan>if they're not really digging, if they're not taking a shovel and digging anything.</v>

02:12:37.507 --> 02:12:45.907
<v Val Levitan>They're not traversing in any depth through anything that we're doing. They're testing SAS. So it's nothing.</v>

02:12:47.427 --> 02:12:52.147
<v Val Levitan>And I feel quite comfortable. First of all, I feel cool. I'm going to give you...</v>

02:12:52.987 --> 02:12:54.147
<v Val Levitan>An incredible.</v>

02:12:55.907 --> 02:12:57.187
<v Val Levitan>development environment.</v>

02:12:59.827 --> 02:13:01.187
<v Val Levitan>Anton.</v>

02:13:03.387 --> 02:13:07.267
<v Val Levitan>I'm going to set up an incredible testing.</v>

02:13:11.627 --> 02:13:13.827
<v Val Levitan>ecosystem around this.</v>

02:13:15.827 --> 02:13:24.307
<v Val Levitan>And even if we make an error in anything, it will be much easier for me to find it, to fix it permanently.</v>

02:13:26.947 --> 02:13:30.467
<v Val Levitan>So, hands down, we're ready.</v>

02:13:36.067 --> 02:13:40.307
<v Val Levitan>It's a good, it's going to be a good piece of technology.</v>

02:13:42.387 --> 02:13:48.867
<v Lena Zhukova>And I would like to confirm one more time, we are not going to move to 4K resolution.</v>

02:13:49.187 --> 02:13:49.707
<v Val Levitan>No.</v>

02:13:50.067 --> 02:13:52.307
<v Lena Zhukova>Okay, it's very important.</v>

02:13:53.027 --> 02:13:57.627
<v Val Levitan>No, we're not moving. There's absolutely zero reason right now to move to 4K.</v>

02:13:57.507 --> 02:13:58.467
<v Lena Zhukova>Okay, perfect.</v>

02:13:59.667 --> 02:14:01.107
<v Val Levitan>There's 0 benefit.</v>

02:14:01.867 --> 02:14:02.027
<v Lena Zhukova>Mm.</v>

02:14:05.107 --> 02:14:17.267
<v Michael Gottlieb>Okay, well, some of the titles in South Dakota, D2703 are best performing titles from previous releases, Lena, so we can start by converting those to Nova.</v>

02:14:18.307 --> 02:14:19.667
<v Michael Gottlieb>And use those as our test bed.</v>

02:14:20.067 --> 02:14:25.427
<v Lena Zhukova>Yeah, but it's going to be like after Nebraska, so like, yeah, developers, yeah.</v>

02:14:23.507 --> 02:14:25.907
<v Michael Gottlieb>Oh yes, of course. Right. It's just...</v>

02:14:23.667 --> 02:14:24.467
<v Efim Podvoiski>Good afternoon, Bosik.</v>

02:14:25.187 --> 02:14:31.427
<v Val Levitan>So, we've we've we've tested automatic conversion from Rage to Nova.</v>

02:14:32.147 --> 02:14:33.267
<v Michael Gottlieb>Have you tested Keno?</v>

02:14:32.547 --> 02:14:33.027
<v Val Levitan>We.</v>

02:14:32.707 --> 02:14:33.267
<v Efim Podvoiski>From Laura.</v>

02:14:35.347 --> 02:14:39.507
<v Val Levitan>We tested keynote, to be honest with you, no, we've tested two games.</v>

02:14:39.587 --> 02:14:39.907
<v Michael Gottlieb>Right.</v>

02:14:40.547 --> 02:14:54.387
<v Val Levitan>one to vertical and one to from dual screen to dual screen. And in both cases, it went very smoothly. I think Keynote will be easier, to be honest with you.</v>

02:14:55.347 --> 02:14:58.547
<v Val Levitan>But this is my own professional opinion.</v>

02:14:55.587 --> 02:14:55.987
<v Michael Gottlieb>Great.</v>

02:15:02.947 --> 02:15:15.427
<v Val Levitan>We'll see. I don't know. So starting 1st of October, tentatively, we're planning for a conversion of South Dakota VLT from RAGE to...</v>

02:15:16.547 --> 02:15:17.427
<v Val Levitan>Nova.</v>

02:15:18.067 --> 02:15:33.827
<v Lena Zhukova>Yeah, I like developer will work on Nebraska in October, so we will start a little bit later. For now, I will work on all like all design screens for South Dakota real key, and once we finish with Nebraska, we will move to.</v>

02:15:32.547 --> 02:15:32.947
<v Val Levitan>I...</v>

02:15:34.467 --> 02:15:38.787
<v Val Levitan>Are you changing visual design for Nova?</v>

02:15:40.387 --> 02:15:41.507
<v Lena Zhukova>Some games.</v>

02:15:40.627 --> 02:15:45.667
<v Val Levitan>Because we can, because we can take the same design and convert it in a matter of hours.</v>

02:15:46.067 --> 02:16:00.947
<v Lena Zhukova>Some games will be changed and the second screen is going to be changed. Yeah, I will, yeah, I need to collect and to start to work on this product, like we also need artists and all artists will be working on Nebraska, so...</v>

02:16:00.027 --> 02:16:02.547
<v Val Levitan>I hear you. I hear you. I hear you.</v>

02:16:04.267 --> 02:16:24.827
<v Lena Zhukova>It's better to allocate all team because it's a new, very important release. And let's finish Nebraska and then all together we will work on this conversion and creating some new content like for variance pop for example.</v>

02:16:04.547 --> 02:16:05.107
<v Val Levitan>Okarak.</v>

02:16:24.907 --> 02:16:28.067
<v Lena Zhukova>So, just some new games we are designing for some of the code.</v>

02:16:29.667 --> 02:16:41.747
<v Val Levitan>Okay, and I want to, in the final statement, to make a point that we have a repository which is called Knowledge Base in GitHub.</v>

02:16:42.627 --> 02:16:49.827
<v Val Levitan>Under Knowledge Base, there is a folder called Standards. This is where all standards go.</v>

02:16:52.067 --> 02:17:04.707
<v Val Levitan>And this repository is open to everyone, so when you use a clot to do any function, please point your clot to the standards repository.</v>

02:17:04.707 --> 02:17:05.667
<v Lena Zhukova>Uh-huh.</v>

02:17:06.627 --> 02:17:09.987
<v Val Levitan>Let him refer to it. Let it refer to it.</v>

02:17:11.187 --> 02:17:13.587
<v Val Levitan>And if you want to read manually, you're welcome to.</v>

02:17:14.747 --> 02:17:29.107
<v Val Levitan>It's under knowledge-based standards. If you don't have access, then you should, because it's open to everybody. And it includes the taxonomy, it includes the filing naming convention.</v>

02:17:30.387 --> 02:17:36.547
<v Val Levitan>whatever standards you're working with. And by the way, when you write standards, write...</v>

02:17:39.187 --> 02:17:43.347
<v Val Levitan>Like, to to a to a narrow point, don't make it a broad standard.</v>

02:17:45.507 --> 02:17:51.627
<v Val Levitan>So keep on adding narrow standards, narrow points. Granular. Yeah, thank you very much. I appreciate it.</v>

02:17:48.067 --> 02:17:48.707
<v Michael Gottlieb>Granular.</v>

02:17:52.467 --> 02:18:02.787
<v Lena Zhukova>Yeah, we we actually have this kind of documents for, uh, only like now it's no, we we just need to move it, uh, yeah, in in proper, uh, repository.</v>

02:18:04.067 --> 02:18:04.707
<v Lena Zhukova>On.</v>

02:18:04.227 --> 02:18:15.827
<v Val Levitan>Okay, and we're moving, as we switch to Nova, we will probably move away completely, but we're steadily moving away from Confluence.</v>

02:18:17.507 --> 02:18:25.667
<v Lena Zhukova>Yes, but if we will continue to release Giorgi before, for example, we will still work with Ridge, right?</v>

02:18:27.267 --> 02:18:27.587
<v Efim Podvoiski>Hi.</v>

02:18:29.427 --> 02:18:31.507
<v Val Levitan>Why? Yeah, I also don't understand why.</v>

02:18:32.467 --> 02:18:33.907
<v Lena Zhukova>I don't know, I'm asking you.</v>

02:18:34.707 --> 02:18:35.187
<v Val Levitan>No.</v>

02:18:37.027 --> 02:18:48.867
<v Val Levitan>No, my understanding that South, South, no, no, my, hold on, hold on one second. My understanding that South Dakota VLT is the last rage.</v>

02:18:38.627 --> 02:18:40.307
<v Efim Podvoiski>But wait, wait, wait, but...</v>

02:18:50.387 --> 02:18:51.547
<v Val Levitan>In Nebraska, sorry.</v>

02:18:52.867 --> 02:18:57.427
<v Val Levitan>Nebraska is the last stage, the last release for OnRage.</v>

02:18:58.067 --> 02:19:00.547
<v Lena Zhukova>Okay, so we...</v>

02:19:01.747 --> 02:19:08.227
<v Lena Zhukova>Forty-three, #4, and are going to be in Nova.</v>

02:19:08.467 --> 02:19:12.227
<v Michael Gottlieb>Correct. Everything is basically everything is Nova from here on out.</v>

02:19:08.707 --> 02:19:10.427
<v Val Levitan>Yes, yes, correct.</v>

02:19:10.707 --> 02:19:30.467
<v Lena Zhukova>Yeah. So like by August of next year, we only can make one release. I think probably let's do the C because we will do Nebraska up to New Year's and we will do this South Dakota VLT.</v>

02:19:32.147 --> 02:19:41.107
<v Val Levitan>No, no, no, no, no, no, South Dakota VLT. The next next South Dakota VLT is is a novel.</v>

02:19:32.307 --> 02:19:33.027
<v Lena Zhukova>In the.</v>

02:19:38.867 --> 02:19:39.427
<v Lena Zhukova>Yes.</v>

02:19:41.267 --> 02:19:56.387
<v Lena Zhukova>Yes, yes, start in January. Yeah, start in January, South Dakota will be Noah and we can do up to August, we can do another Georgia release and probably we want to do curve, right? We want to do something new to present it on the show.</v>

02:19:41.747 --> 02:19:43.347
<v Michael Gottlieb>Yes, but it's next year.</v>

02:19:53.427 --> 02:20:00.627
<v Michael Gottlieb>Yes, we're introducing C43. Yes, C43 Nova will be introduced at the Georgia show. It'll be developed in Nova.</v>

02:20:01.107 --> 02:20:01.707
<v Lena Zhukova>Okay.</v>

02:20:01.427 --> 02:20:03.587
<v Val Levitan>Yes, yes, yes, yes, yes.</v>

02:20:03.027 --> 02:20:05.267
<v Lena Zhukova>Great. Okay, that sounds like a plan.</v>

02:20:08.467 --> 02:20:14.947
<v Val Levitan>Okay. Thank you very much. Have a great weekend. Expect my call on Monday early.</v>

02:20:12.627 --> 02:20:13.347
<v Efim Podvoiski>Thank you.</v>

02:20:15.507 --> 02:20:19.107
<v Efim Podvoiski>We have, we have a long weekend, right? Everybody.</v>

02:20:17.587 --> 02:20:20.947
<v Lena Zhukova>Yeah, everything, yeah, it's in US.</v>

02:20:17.747 --> 02:20:19.667
<v Michael Gottlieb>He's stra, he's strashing you.</v>

02:20:20.627 --> 02:20:24.707
<v Val Levitan>No, no, no labor. Labor is when you're at the computer laboring.</v>

02:20:24.627 --> 02:20:24.947
<v Juan Martinez>Yeah.</v>

02:20:26.547 --> 02:20:27.427
<v Val Levitan>All right, bye.</v>

02:20:26.787 --> 02:20:28.547
<v Michael Gottlieb>Talking to you is a vacation.</v>

02:20:28.987 --> 02:20:29.427
<v Juan Martinez>Yeah.</v>

02:20:29.507 --> 02:20:39.027
<v Val Levitan>Talking to me is a labor. I know, don't worry about it. I can read your facial expression, I know. Okay, have a good weekend. Bye-bye. Goodbye.</v>

02:20:31.627 --> 02:20:33.187
<v Michael Gottlieb>No, I said it's a vacation.</v>

02:20:31.827 --> 02:20:32.227
<v Juan Martinez>Yeah.</v>

02:20:37.587 --> 02:20:39.267
<v Juan Martinez>All right. Thanks, everybody. Bye.</v>

02:20:38.387 --> 02:20:38.867
<v Michael Gottlieb>Bye.</v>

