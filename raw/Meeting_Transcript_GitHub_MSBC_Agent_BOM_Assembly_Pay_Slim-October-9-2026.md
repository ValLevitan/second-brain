# Raw Transcript — GitHub-MSBC
**Date:** October 9, 2026, 11:37 AM – 12:33 PM Eastern
**Summary note:** [[Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026]]
---
WEBVTT

00:00:04.426 --> 00:00:05.306
<v Nathan Carver>All right, so...</v>

00:00:06.666 --> 00:00:08.106
<v Nathan Carver>Okay, can you see the...</v>

00:00:08.986 --> 00:00:09.546
<v Nathan Carver>Yeah, hun.</v>

00:00:10.186 --> 00:00:10.506
<v Genadi Peari>Yeah.</v>

00:00:11.226 --> 00:00:13.266
<v Nathan Carver>Okay, so I shared the...</v>

00:00:15.226 --> 00:00:15.386
<v Nathan Carver>Mm.</v>

00:00:18.906 --> 00:00:22.906
<v Nathan Carver>This is the PR that I created and this has basically an overview.</v>

00:00:24.186 --> 00:00:24.826
<v Nathan Carver>Of.</v>

00:00:27.186 --> 00:00:34.826
<v Nathan Carver>of just the exploratory work that I did. And its purpose is to, if we have a defined structure.</v>

00:00:35.986 --> 00:00:43.146
<v Nathan Carver>Can an agent take that structure, put together a BOM inside Msbc?</v>

00:00:44.586 --> 00:00:45.306
<v Nathan Carver>So...</v>

00:00:46.906 --> 00:00:47.866
<v Nathan Carver>What this?</v>

00:00:50.106 --> 00:00:58.426
<v Nathan Carver>Script did is it took using our dev instance of Msbc, it took an existing.</v>

00:01:01.386 --> 00:01:04.026
<v Nathan Carver>Bom out of Msbc here.</v>

00:01:07.146 --> 00:01:15.146
<v Nathan Carver>and reversed decompile that and broke it down into structures inside the repository.</v>

00:01:16.586 --> 00:01:16.826
<v Nathan Carver>Um...</v>

00:01:18.466 --> 00:01:19.066
<v Val Levitan>Which of you?</v>

00:01:18.506 --> 00:01:24.746
<v Nathan Carver>So before creating any repositories.</v>

00:01:22.346 --> 00:01:22.746
<v Val Levitan>See what?</v>

00:01:25.706 --> 00:01:26.106
<v Nathan Carver>Oops.</v>

00:01:30.586 --> 00:01:41.626
<v Nathan Carver>I just created folders that represent what those repositories would look like in the future. But so that's what these are. Right now they're just folders, but</v>

00:01:42.826 --> 00:01:48.826
<v Nathan Carver>The vision is they would be separate repos. They could have their own tag and versioning.</v>

00:01:49.946 --> 00:01:52.506
<v Nathan Carver>And so it takes these parts.</v>

00:01:54.346 --> 00:01:57.346
<v Nathan Carver>Or, yeah, these are all parts, and...</v>

00:01:58.586 --> 00:02:05.866
<v Nathan Carver>Reverse uses a script to pull them out of Msbc and creates these file structures and</v>

00:02:09.386 --> 00:02:16.826
<v Nathan Carver>So inside each of these repos, it would have just an overview of how these, how the contents, how the parts in the repo are structured.</v>

00:02:19.466 --> 00:02:26.026
<v Nathan Carver>And it's going to have this parts CSV. That's just a general description of the part. And then inside.</v>

00:02:27.706 --> 00:02:33.386
<v Nathan Carver>These contracts, so this is an example of a structured contract.</v>

00:02:34.186 --> 00:02:42.346
<v Nathan Carver>for the part and its purpose is to define the, essentially the interface.</v>

00:02:43.506 --> 00:02:49.706
<v Nathan Carver>what it provides, what it accepts. And so this structure is...</v>

00:02:50.666 --> 00:03:05.466
<v Nathan Carver>The idea is this structure can be used by an agent to assimilate parts, know and understand understand which ones you know can fit together, which which ones are compatible to make choices that way.</v>

00:03:06.746 --> 00:03:11.306
<v Nathan Carver>And so each one of these repos, so all of these here on the left would be broken down into.</v>

00:03:12.506 --> 00:03:16.426
<v Nathan Carver>These repositories different one.</v>

00:03:18.506 --> 00:03:19.546
<v Nathan Carver>Part labels.</v>

00:03:24.906 --> 00:03:27.306
<v Nathan Carver>So who's my guy? Yeah, so this guy here.</v>

00:03:28.666 --> 00:03:30.986
<v Nathan Carver>Just gonna use the label, as you can see, it's much simpler.</v>

00:03:33.706 --> 00:03:41.626
<v Nathan Carver>So it has, again, the inputs, the outputs, and then notes are metadata for the agent to review and get an understanding.</v>

00:03:44.826 --> 00:03:49.706
<v Nathan Carver>So that's what it pulls out of, pulled all of this out of Msbc.</v>

00:03:50.986 --> 00:03:56.746
<v Nathan Carver>So then the goal was to, okay, now that it has these parts.</v>

00:03:57.946 --> 00:04:00.826
<v Nathan Carver>Can it reassemble that bomb?</v>

00:04:02.026 --> 00:04:03.226
<v Nathan Carver>With instructions.</v>

00:04:04.426 --> 00:04:05.146
<v Nathan Carver>And...</v>

00:04:06.666 --> 00:04:07.426
<v Nathan Carver>So, the...</v>

00:04:11.786 --> 00:04:12.706
<v Nathan Carver>Let's see the...</v>

00:04:19.026 --> 00:04:33.226
<v Nathan Carver>So here in the, this is the standard. So this is where the agent's going to get its instructions and understanding of how this works. And then, so in the experiment was, it pulls this BOM.</v>

00:04:34.106 --> 00:04:36.586
<v Nathan Carver>Here, and then it creates a new one.</v>

00:04:38.826 --> 00:04:50.426
<v Nathan Carver>using a new agent, it gives it instructions to create a new BOM in Msbc. So the agent pulls the parts and then feeds those through a script that creates this at Msbc.</v>

00:04:53.306 --> 00:04:58.106
<v Nathan Carver>So, we pull this guy up. This is the new BOM, and the goal was...</v>

00:04:59.466 --> 00:05:01.146
<v Nathan Carver>Right, how close can we get?</v>

00:05:02.826 --> 00:05:06.506
<v Nathan Carver>and to recreating this.</v>

00:05:08.426 --> 00:05:10.306
<v Nathan Carver>Let's see, this is the original, right?</v>

00:05:12.986 --> 00:05:13.466
<v Nathan Carver>Yes.</v>

00:05:14.626 --> 00:05:34.346
<v Nathan Carver>So this is what the age using the script. So the script is able to take the information and reassemble it. So in this case, there's outlier parts that we're going to have to settle on. But for the most part, it's able to do this if it has the proper structure.</v>

00:05:37.146 --> 00:05:46.746
<v Nathan Carver>So the and then I had to do this same same exercise for these other other bombs.</v>

00:05:49.546 --> 00:05:50.986
<v Nathan Carver>It also creates this.</v>

00:05:49.866 --> 00:05:50.106
<v Genadi Peari>Yeah.</v>

00:05:52.266 --> 00:05:52.666
<v Nathan Carver>Go ahead.</v>

00:05:52.506 --> 00:05:59.866
<v Genadi Peari>But what is it structure you mean? What do you mean by structure? What the rules?</v>

00:06:00.986 --> 00:06:02.906
<v Genadi Peari>You feed him to make.</v>

00:06:01.626 --> 00:06:02.106
<v Nathan Carver>Mhm.</v>

00:06:03.906 --> 00:06:07.666
<v Genadi Peari>What is the structure? Why parts are missing? I don't understand.</v>

00:06:10.026 --> 00:06:11.946
<v Nathan Carver>So I think those.</v>

00:06:12.946 --> 00:06:13.706
<v Nathan Carver>Forget which.</v>

00:06:18.746 --> 00:06:20.506
<v Nathan Carver>So let me pull up the structure first.</v>

00:06:19.946 --> 00:06:24.026
<v Genadi Peari>What his logics when he assembled the new BOM?</v>

00:06:24.986 --> 00:06:27.386
<v Nathan Carver>Sure, yep, so it it has.</v>

00:06:25.786 --> 00:06:35.066
<v Genadi Peari>He didn't, he didn't save anything from existing, right? He he made new logics how to assemble.</v>

00:06:35.386 --> 00:06:40.746
<v Nathan Carver>So, it has to make choices based on what are my inputs and my what, what right now, what is.</v>

00:06:40.106 --> 00:06:42.106
<v Genadi Peari>Oh, based on the contracts you mean?</v>

00:06:42.266 --> 00:06:47.026
<v Nathan Carver>Correct. So what part, what part satisfies this contract?</v>

00:06:49.466 --> 00:06:53.546
<v Nathan Carver>And that's how it's able to RIS. I'm trying to find one that is.</v>

00:06:55.466 --> 00:07:03.546
<v Genadi Peari>Yeah, I mean, if a PC board has four holes, so it needs to find the four screws, right? This is the logic.</v>

00:07:04.266 --> 00:07:06.186
<v Nathan Carver>Correct. That's the idea.</v>

00:07:10.106 --> 00:07:19.306
<v Genadi Peari>So basically, it might not never be perfect, right? It will be 90% correct.</v>

00:07:20.506 --> 00:07:33.146
<v Genadi Peari>I mean, we ideal case never be 100%, so we basically need to keep the reference solid reference, which are which is adjusted manually.</v>

00:07:21.706 --> 00:07:22.746
<v Nathan Carver>Yeah, yes.</v>

00:07:24.906 --> 00:07:25.706
<v Nathan Carver>It couldn't.</v>

00:07:34.306 --> 00:07:40.746
<v Nathan Carver>Correct. And what it's supposed to do is it creates this trace report. And again, this is all.</v>

00:07:41.706 --> 00:07:42.986
<v Nathan Carver>Just, um...</v>

00:07:44.266 --> 00:07:50.986
<v Nathan Carver>Testing the waters, what can we do with this? So, the idea is it would run this process and would create this report, and this is...</v>

00:07:52.106 --> 00:08:01.546
<v Nathan Carver>and everything that is put in there, and it may have whatever we need. This can have, these are the reasoning, this is what I found, this is what I didn't find. These are parts I rejected.</v>

00:08:02.626 --> 00:08:04.906
<v Nathan Carver>But it's going to have to have some level of guidelines.</v>

00:08:06.066 --> 00:08:15.466
<v Nathan Carver>Because we can do this all day, but what we really need at the output side is how do we verify, and I don't know the answer to this yet, but how do we verify the output?</v>

00:08:16.746 --> 00:08:17.146
<v Genadi Peari>No.</v>

00:08:16.746 --> 00:08:20.506
<v Nathan Carver>in a way that doesn't take you more time than what you're doing now, right? And</v>

00:08:20.426 --> 00:08:22.106
<v Genadi Peari>I it definitely will.</v>

00:08:26.586 --> 00:08:31.546
<v Genadi Peari>Because the building bill of material is not a time-consuming part.</v>

00:08:33.786 --> 00:08:34.426
<v Genadi Peari>You just...</v>

00:08:35.546 --> 00:08:43.146
<v Genadi Peari>Do the design like months or half a year, and then whatever you did, you build the bill of material once.</v>

00:08:36.906 --> 00:08:37.026
<v Nathan Carver>Yeah.</v>

00:08:44.666 --> 00:08:47.546
<v Genadi Peari>And then just maintain it like.</v>

00:08:48.346 --> 00:08:53.946
<v Nathan Carver>So, what is the, like, what is the most time-consuming and challenging piece of that?</v>

00:08:48.746 --> 00:08:49.146
<v Genadi Peari>Ai.</v>

00:08:56.506 --> 00:08:57.466
<v Genadi Peari>I don't see.</v>

00:08:58.346 --> 00:09:01.106
<v Genadi Peari>Building bill of materials that they can see me.</v>

00:09:02.266 --> 00:09:04.906
<v Genadi Peari>Well, I don't want to argue as well, so...</v>

00:09:06.026 --> 00:09:08.426
<v Genadi Peari>He thinks it's a time-consuming.</v>

00:09:07.946 --> 00:09:08.066
<v Nathan Carver>Yeah.</v>

00:09:10.106 --> 00:09:15.386
<v Genadi Peari>It's really not. The idea is not probably to save time. The idea is...</v>

00:09:12.986 --> 00:09:13.106
<v Nathan Carver>Okay.</v>

00:09:17.906 --> 00:09:18.826
<v Genadi Peari>Tools.</v>

00:09:20.746 --> 00:09:23.426
<v Genadi Peari>Make, keep the revisions.</v>

00:09:24.666 --> 00:09:25.626
<v Genadi Peari>Oh.</v>

00:09:26.986 --> 00:09:29.626
<v Genadi Peari>Make suggestions, I don't know.</v>

00:09:32.186 --> 00:09:33.466
<v Genadi Peari>Make improvements.</v>

00:09:35.866 --> 00:09:42.266
<v Genadi Peari>Second opinion, I, but Nathan, it's really hard for me to, I, I...</v>

00:09:46.026 --> 00:09:47.946
<v Genadi Peari>Let's say he built something.</v>

00:09:49.146 --> 00:09:58.266
<v Genadi Peari>So the idea is what? To take this and then to adjust it to reality? I mean, maybe...</v>

00:09:59.066 --> 00:09:59.546
<v Genadi Peari>Because.</v>

00:10:01.306 --> 00:10:05.226
<v Genadi Peari>Because not only that, right? You took one level bill of material.</v>

00:10:07.746 --> 00:10:12.186
<v Nathan Carver>Um, uh, two, yeah, yep.</v>

00:10:08.426 --> 00:10:09.386
<v Genadi Peari>A few levels.</v>

00:10:10.666 --> 00:10:11.546
<v Genadi Peari>Two levels.</v>

00:10:13.786 --> 00:10:20.586
<v Genadi Peari>And he did it 2 levels as well? No, 139, the one you show is the one level.</v>

00:10:24.266 --> 00:10:27.066
<v Genadi Peari>No, these are one level bill of materials.</v>

00:10:26.186 --> 00:10:30.906
<v Nathan Carver>These are all one level, or no, this one it claimed was 2 levels, but...</v>

00:10:32.586 --> 00:10:33.306
<v Nathan Carver>It could be wrong.</v>

00:10:37.786 --> 00:10:41.866
<v Nathan Carver>Okay, so it says because of this part here.</v>

00:10:43.626 --> 00:10:44.586
<v Genadi Peari>Ohh, this.</v>

00:10:47.466 --> 00:11:10.186
<v Genadi Peari>This one might be two levels, but it just for convenience treating of the procurement. It's not physical level that we needed, but this level done like assembly and the PC board. And so we have changed the revision, so we automatically will spread it.</v>

00:10:50.746 --> 00:10:50.866
<v Nathan Carver>The.</v>

00:11:00.266 --> 00:11:00.466
<v Nathan Carver>Yeah.</v>

00:11:10.506 --> 00:11:13.466
<v Genadi Peari>To all the products, that's why the level is created.</v>

00:11:15.386 --> 00:11:15.946
<v Nathan Carver>Okay.</v>

00:11:17.226 --> 00:11:17.946
<v Genadi Peari>But...</v>

00:11:18.946 --> 00:11:22.666
<v Genadi Peari>What if we do 3 levels of the bill of material?</v>

00:11:23.306 --> 00:11:25.066
<v Nathan Carver>Yeah, we would have to.</v>

00:11:25.786 --> 00:11:44.266
<v Genadi Peari>And that levels based not only on the contracts we have, it's also based on the how production is working in the how they assemble the machine, what is conveniently for them to do sub-assemblies, right?</v>

00:11:45.226 --> 00:11:58.266
<v Genadi Peari>if it's convenient to put more parts in one assembly. Because the logics between myself, the AI, and the production might be three different logics.</v>

00:12:01.026 --> 00:12:01.706
<v Nathan Carver>Understood.</v>

00:12:02.186 --> 00:12:04.906
<v Genadi Peari>So, it's also the point that...</v>

00:12:05.066 --> 00:12:05.386
<v Nathan Carver>Coo.</v>

00:12:06.026 --> 00:12:12.666
<v Genadi Peari>So my point is, there's whatever he will do, it never will be 100% solid.</v>

00:12:09.466 --> 00:12:09.546
<v Nathan Carver>It.</v>

00:12:13.026 --> 00:12:13.146
<v Nathan Carver>Bep.</v>

00:12:15.106 --> 00:12:21.946
<v Genadi Peari>source, right? It's always we need to keep in mind that might be need small adjustment.</v>

00:12:16.346 --> 00:12:16.386
<v Nathan Carver>I.</v>

00:12:22.746 --> 00:12:23.306
<v Nathan Carver>Correct.</v>

00:12:24.306 --> 00:12:25.866
<v Genadi Peari>Okay, this is we agree, right?</v>

00:12:24.666 --> 00:12:30.106
<v Nathan Carver>Yeah, I think complex structures, the agent is not going to produce something.</v>

00:12:31.066 --> 00:12:36.266
<v Nathan Carver>that you would look at and it's just perfect. Like I don't see that happening anytime soon for sure.</v>

00:12:36.586 --> 00:12:38.746
<v Genadi Peari>Yeah, the second point.</v>

00:12:39.946 --> 00:12:40.506
<v Genadi Peari>Sorry.</v>

00:12:42.026 --> 00:12:43.306
<v Nathan Carver>Yeah, so that's why I'm saying.</v>

00:12:44.586 --> 00:12:47.866
<v Nathan Carver>There has to be some, the efficiency has to be kind.</v>

00:12:49.146 --> 00:12:55.146
<v Nathan Carver>Can we maintain the files, version them, and then build the BOM?</v>

00:12:56.306 --> 00:13:00.186
<v Nathan Carver>what can be automated, and then how can that automation be verified.</v>

00:13:01.466 --> 00:13:06.546
<v Nathan Carver>And what are the, it's going to have constraints. It's going to have inputs and outputs and.</v>

00:13:07.546 --> 00:13:12.906
<v Nathan Carver>But there has to be a verification step, and 'cause we can't trust, we trust.</v>

00:13:10.666 --> 00:13:29.626
<v Genadi Peari>Then, all right, so look at the next stage. Once we build the bill of material, right, this bill of material will be deployed for procurement, for production everywhere. So procurement will take this bill of material,</v>

00:13:27.386 --> 00:13:27.626
<v Nathan Carver>Cool.</v>

00:13:29.786 --> 00:13:43.066
<v Genadi Peari>And, based on the instances of the parts, we will need to place in orders. This can be fully automated. I don't see any problem with this, right? But...</v>

00:13:39.226 --> 00:13:39.466
<v Nathan Carver>Yeah.</v>

00:13:44.586 --> 00:13:58.346
<v Genadi Peari>In this, eventually what? It will create some report probably, right? For this product, we need hundreds of, I mean, I want to order 100 pieces of this product. And we have the bill of material, solid bill of material.</v>

00:13:47.706 --> 00:13:48.026
<v Nathan Carver>No.</v>

00:13:59.306 --> 00:14:13.146
<v Genadi Peari>Then the procurement or agent can go, oh, this part, it has two instances. So Val wants to order 200, I mean hundreds, so we need to place an order to send RFQ for 200 parts to procure.</v>

00:14:07.786 --> 00:14:07.946
<v Nathan Carver>Yeah.</v>

00:14:14.106 --> 00:14:35.146
<v Genadi Peari>Right, and this will be a report which needs to be updated daily, which shows I need this amount of part I have in the stock, this amount of part, and I need to order this, and the delete time is a month.</v>

00:14:31.346 --> 00:14:31.626
<v Nathan Carver>Please.</v>

00:14:35.386 --> 00:14:43.066
<v Genadi Peari>and it will be here on December 1st. All this information needed for the agent.</v>

00:14:44.346 --> 00:14:46.106
<v Genadi Peari>For CO agent.</v>

00:14:47.386 --> 00:14:48.746
<v Genadi Peari>To fully operate.</v>

00:14:50.186 --> 00:15:04.826
<v Genadi Peari>So for this portion, it's very easy to automate. But the point is the source of everything is the bill of material, which has not been fluctuated.</v>

00:15:01.466 --> 00:15:01.586
<v Nathan Carver>Okay.</v>

00:15:08.426 --> 00:15:10.026
<v Nathan Carver>Okay, yep.</v>

00:15:15.946 --> 00:15:24.906
<v Nathan Carver>I see. So the source, the bill of material is not just, there's a downstream source, it's a source for all this downstream work.</v>

00:15:26.106 --> 00:15:31.306
<v Nathan Carver>that you see that as a good candidate for automation.</v>

00:15:34.346 --> 00:15:48.986
<v Nathan Carver>So ordering the parts and understanding what, looking at what's being ordered, reviewing the bill of material, and then recognizing all the quantities that are short, what needs to be ordered, and then being able to automate that downstream.</v>

00:15:50.146 --> 00:15:50.906
<v Nathan Carver>Prose.</v>

00:15:51.146 --> 00:15:53.466
<v Genadi Peari>The next step, yeah, definitely. We have to.</v>

00:15:56.906 --> 00:15:57.386
<v Nathan Carver>Okay.</v>

00:16:01.066 --> 00:16:04.826
<v Nathan Carver>So is there, as far as like having...</v>

00:16:06.266 --> 00:16:08.026
<v Nathan Carver>These hardware conventions.</v>

00:16:10.666 --> 00:16:13.026
<v Nathan Carver>Something like this, and...</v>

00:16:15.426 --> 00:16:18.106
<v Nathan Carver>Where we maintain a file that defines.</v>

00:16:19.226 --> 00:16:21.306
<v Nathan Carver>This type of...</v>

00:16:22.826 --> 00:16:23.386
<v Genadi Peari>Yeah.</v>

00:16:22.906 --> 00:16:25.306
<v Nathan Carver>Input structure with contract structure.</v>

00:16:28.106 --> 00:16:28.666
<v Genadi Peari>Okay.</v>

00:16:29.546 --> 00:16:30.826
<v Nathan Carver>Is that something that...</v>

00:16:32.026 --> 00:16:40.506
<v Nathan Carver>Do you see it's having just in what you're doing now, does this have a value and is this going to be something that we can use and maintain and version?</v>

00:16:43.226 --> 00:16:43.786
<v Nathan Carver>On.</v>

00:16:45.066 --> 00:16:56.106
<v Nathan Carver>Like, I don't, so I don't understand the whole flow, but I can start, I can, if you say this, this part here can be automated, I can look in that, right? And I can, I can help with scripting wherever I know.</v>

00:16:57.786 --> 00:17:06.986
<v Nathan Carver>And I don't fully understand all of Val's vision, but I know the automation and the agenda part is important.</v>

00:17:12.146 --> 00:17:12.746
<v Genadi Peari>Bom.</v>

00:17:14.266 --> 00:17:18.266
<v Genadi Peari>I thought you, I, I, I don't have an answer.</v>

00:17:19.146 --> 00:17:19.546
<v Nathan Carver>Okay.</v>

00:17:19.546 --> 00:17:25.466
<v Genadi Peari>Um, because uh, I also don't see the whole the whole picture, like...</v>

00:17:26.666 --> 00:17:33.786
<v Genadi Peari>I understand the idea of having the repositories and the contracts, it makes sense, but...</v>

00:17:36.426 --> 00:17:40.106
<v Genadi Peari>But I, I don't see the whole, how it...</v>

00:17:37.306 --> 00:17:37.546
<v Nathan Carver>Yes.</v>

00:17:44.106 --> 00:17:53.786
<v Genadi Peari>Due to the limitation that you just mentioned that we will have, we never have 100% of solid buildup of the final BOM.</v>

00:17:46.266 --> 00:17:46.386
<v Nathan Carver>Play.</v>

00:17:47.906 --> 00:17:48.186
<v Nathan Carver>No.</v>

00:17:55.226 --> 00:17:56.426
<v Genadi Peari>How do we?</v>

00:17:59.466 --> 00:18:06.026
<v Nathan Carver>It's a it's a trust trust and verify, like we always we have to verify what it creates, so.</v>

00:18:07.986 --> 00:18:11.866
<v Nathan Carver>What that verification step looks like, is it just...</v>

00:18:12.986 --> 00:18:17.466
<v Nathan Carver>someone going and reviewing the entire BOM. Is there another way that we can verify?</v>

00:18:18.746 --> 00:18:21.866
<v Nathan Carver>what the agent is assembling.</v>

00:18:23.026 --> 00:18:35.786
<v Nathan Carver>And it's just a decision. Like the agent makes the decision looking at all the parts, these parts put together. I can choose these parts. I can document why I chose each part.</v>

00:18:36.986 --> 00:18:39.146
<v Nathan Carver>The script then takes over and pushes.</v>

00:18:38.666 --> 00:18:48.986
<v Genadi Peari>Nathan, can you, can you while while send a message that can you hear all the want hear all the limitations?</v>

00:18:50.826 --> 00:18:53.866
<v Nathan Carver>Oh, limitations. So, um...</v>

00:18:57.226 --> 00:19:01.866
<v Nathan Carver>I think it's the limitation I see is.</v>

00:19:03.026 --> 00:19:09.946
<v Nathan Carver>or I should say, it's really a verification step. And that is the agent can make these decisions.</v>

00:19:11.146 --> 00:19:13.946
<v Nathan Carver>But we need some way to verify.</v>

00:19:15.986 --> 00:19:18.826
<v Nathan Carver>what the agent is doing. Now, the script.</v>

00:19:19.786 --> 00:19:26.426
<v Nathan Carver>Once the agent has made a decision, it can run this through a script. And the script, what it will do.</v>

00:19:27.706 --> 00:19:31.146
<v Nathan Carver>is look at each of these parts, all these parts in here.</v>

00:19:32.266 --> 00:19:37.066
<v Nathan Carver>And if their interfaces don't line up, the script can flag.</v>

00:19:38.146 --> 00:19:56.426
<v Nathan Carver>problems and give it back to the agent to resolve. So I don't think it's going to be a one-time loop. I think the agent will put together the BOM, run it through the script for verification, take that feedback and cycle on it. So I think.</v>

00:19:57.666 --> 00:20:04.666
<v Nathan Carver>What it's going to come down to is, at the final output, how do we verify that what we're getting?</v>

00:20:05.866 --> 00:20:12.426
<v Nathan Carver>is acceptable and there may be for the first few we run.</v>

00:20:12.906 --> 00:20:13.146
<v Nathan Carver>Um...</v>

00:20:15.866 --> 00:20:19.946
<v Nathan Carver>Correct. So you could also add an audit agent that.</v>

00:20:21.626 --> 00:20:26.106
<v Nathan Carver>reviews it. We could take a different model even, right? We could have</v>

00:20:27.626 --> 00:20:44.746
<v Nathan Carver>Claude build it and Grok or Astra audits it, right? Just take a totally different model to audit. The script automation, the script audit will be the most consistent because it's going to be very strict on using the inputs and the outputs.</v>

00:21:17.466 --> 00:21:19.466
<v Genadi Peari>I think all these AR.</v>

00:21:20.746 --> 00:21:22.186
<v Genadi Peari>Realistically, right now.</v>

00:21:24.906 --> 00:21:27.546
<v Genadi Peari>All this word that Val mentioned right now.</v>

00:21:30.946 --> 00:21:31.466
<v Nathan Carver>Okay.</v>

00:21:32.106 --> 00:21:38.266
<v Genadi Peari>This, we need to, I don't see any reason why we don't, we won't have it tomorrow.</v>

00:21:36.826 --> 00:21:37.066
<v Nathan Carver>Yeah.</v>

00:21:44.266 --> 00:21:46.906
<v Nathan Carver>Yeah, I agree. I think this is all reasonable.</v>

00:21:47.546 --> 00:21:48.106
<v Genadi Peari>Yes.</v>

00:21:48.266 --> 00:21:48.506
<v Nathan Carver>Yeah.</v>

00:21:51.466 --> 00:21:56.586
<v Nathan Carver>And this is these actions are only working with the existing BOM, so they're not.</v>

00:21:57.786 --> 00:22:02.506
<v Nathan Carver>This is just taking an existing BOM and using current inventory in.</v>

00:22:04.186 --> 00:22:08.746
<v Nathan Carver>BC and the list of suppliers in BC and being able to automate that.</v>

00:22:10.106 --> 00:22:18.986
<v Genadi Peari>This is very important that Val is texting now. These are real things which takes a lot of mistakes and efforts.</v>

00:22:21.626 --> 00:22:25.306
<v Genadi Peari>These 5 that Val just texted are very important.</v>

00:22:25.706 --> 00:22:26.106
<v Nathan Carver>Okay.</v>

00:22:26.746 --> 00:22:31.546
<v Genadi Peari>And this, this like a lot of saving might might bring to the company.</v>

00:22:33.226 --> 00:22:36.506
<v Nathan Carver>Okay, okay, and this is downstream, I think, from...</v>

00:22:40.066 --> 00:22:44.426
<v Nathan Carver>What we're looking at here is really assembling a BOM, not necessarily...</v>

00:22:46.346 --> 00:22:50.426
<v Nathan Carver>All of this that Val is mentioning is downstream from this, so...</v>

00:22:51.946 --> 00:22:54.666
<v Nathan Carver>Right, working on an existing bill of material.</v>

00:22:59.906 --> 00:23:04.586
<v Genadi Peari>And the last one I remember I mentioned you in the conversation.</v>

00:23:16.346 --> 00:23:17.346
<v Genadi Peari>Absolutely.</v>

00:23:16.986 --> 00:23:17.106
<v Nathan Carver>Yeah.</v>

00:23:37.306 --> 00:23:41.386
<v Nathan Carver>So he wants, okay, so Github and Msbc have to be in sync.</v>

00:23:58.026 --> 00:24:01.466
<v Genadi Peari>Nathan, I think this is your stage.</v>

00:24:01.706 --> 00:24:01.786
<v Nathan Carver>Ach.</v>

00:24:04.826 --> 00:24:06.746
<v Nathan Carver>Yes, thinking on this.</v>

00:24:55.786 --> 00:24:56.426
<v Nathan Carver>Okay.</v>

00:25:01.066 --> 00:25:02.986
<v Nathan Carver>So the BOM has to exist in Github.</v>

00:25:08.106 --> 00:25:09.786
<v Nathan Carver>The BOM exists in Github.</v>

00:25:12.266 --> 00:25:16.026
<v Nathan Carver>And the parts, contracts, they all exist in Github.</v>

00:25:17.146 --> 00:25:18.506
<v Nathan Carver>So, the agent has...</v>

00:25:19.666 --> 00:25:30.906
<v Nathan Carver>This, the AI CO has access to those repos. Is the reason they have to exist there because they can be versioned? Is there what?</v>

00:25:33.306 --> 00:25:43.386
<v Nathan Carver>because they can access the BOM in Msbc, but Msbc doesn't have all the information that Github can have. So the CO needs more information than...</v>

00:25:44.986 --> 00:25:46.826
<v Nathan Carver>Msbc provides.</v>

00:25:56.906 --> 00:25:57.306
<v Val Levitan>Let me.</v>

00:25:58.346 --> 00:25:59.306
<v Nathan Carver>Maybe you get busted.</v>

00:26:05.306 --> 00:26:05.786
<v Val Levitan>You hear me?</v>

00:26:06.666 --> 00:26:07.106
<v Nathan Carver>Yeah.</v>

00:26:08.186 --> 00:26:10.426
<v Nathan Carver>Yes, it's choppy.</v>

00:26:13.546 --> 00:26:14.506
<v Val Levitan>The help.</v>

00:26:44.986 --> 00:27:03.946
<v Genadi Peari>So, so it like, like Github, Github provides the bill of material, you export it into Msbc and then look it there, and if there is a change, it exports another bill of material, new revision.</v>

00:26:45.626 --> 00:26:45.746
<v Nathan Carver>Yeah.</v>

00:26:47.226 --> 00:26:47.386
<v Nathan Carver>Yes.</v>

00:26:51.026 --> 00:26:51.146
<v Nathan Carver>Yeah.</v>

00:26:54.746 --> 00:26:54.826
<v Nathan Carver>Ach.</v>

00:27:06.226 --> 00:27:09.146
<v Genadi Peari>Because, where, where, where the comes the human?</v>

00:27:12.026 --> 00:27:14.106
<v Genadi Peari>Verification, where do you lock it?</v>

00:27:15.026 --> 00:27:15.466
<v Nathan Carver>Correct.</v>

00:27:16.106 --> 00:27:25.626
<v Genadi Peari>Because all these five actions, they actually, the placing orders, connecting the suppliers, this all comes from Msbc.</v>

00:27:17.266 --> 00:27:17.386
<v Nathan Carver>Play.</v>

00:27:20.906 --> 00:27:21.066
<v Nathan Carver>Pay.</v>

00:27:27.146 --> 00:27:34.666
<v Nathan Carver>Correct. Yeah, so I'm waiting. I think Val Val is typing. I'm wondering what is the piece of data that is in Github?</v>

00:27:35.626 --> 00:27:38.986
<v Nathan Carver>That's not an Msbc that's helping the agent succeed.</v>

00:27:41.546 --> 00:27:42.746
<v Genadi Peari>Order information.</v>

00:27:44.826 --> 00:27:46.266
<v Genadi Peari>All engineering sources.</v>

00:27:46.826 --> 00:27:47.226
<v Nathan Carver>Right.</v>

00:27:47.626 --> 00:27:53.866
<v Genadi Peari>These are in the Github, but the connection is by part number, right?</v>

00:27:55.866 --> 00:27:56.426
<v Nathan Carver>Okay.</v>

00:28:01.146 --> 00:28:04.026
<v Genadi Peari>It's very easy to pull it from the Github.</v>

00:28:06.346 --> 00:28:07.866
<v Genadi Peari>By part number and revision.</v>

00:28:10.186 --> 00:28:10.826
<v Genadi Peari>Each port.</v>

00:28:12.426 --> 00:28:12.906
<v Nathan Carver>Okay.</v>

00:28:14.426 --> 00:28:15.546
<v Genadi Peari>It's already there.</v>

00:28:14.506 --> 00:28:14.986
<v Nathan Carver>Let's see.</v>

00:28:17.546 --> 00:28:20.266
<v Genadi Peari>Maybe you need to shuffle it in the repository.</v>

00:28:25.306 --> 00:28:28.186
<v Nathan Carver>Okay, still waiting for Val still typing.</v>

00:29:21.706 --> 00:29:25.586
<v Nathan Carver>So I guess what I'm looking for, the more I understand.</v>

00:29:26.506 --> 00:29:29.066
<v Nathan Carver>The need of this AI CO.</v>

00:29:32.666 --> 00:29:33.466
<v Nathan Carver>Yes.</v>

00:29:36.026 --> 00:29:37.946
<v Nathan Carver>The workflow may not be.</v>

00:29:39.706 --> 00:29:45.066
<v Nathan Carver>The workflow may be different to provide this, maybe even simpler to provide the same value, so...</v>

00:29:45.946 --> 00:29:47.106
<v Nathan Carver>I can understand.</v>

00:29:50.466 --> 00:29:54.506
<v Nathan Carver>If I can understand the core need, because the conflict I hear is...</v>

00:29:56.986 --> 00:29:59.626
<v Nathan Carver>It's not really saving us a lot of time.</v>

00:30:01.946 --> 00:30:07.946
<v Nathan Carver>But we still need the information. So is there a different way we can provide that information?</v>

00:30:09.146 --> 00:30:09.786
<v Nathan Carver>In Github.</v>

00:30:11.026 --> 00:30:15.466
<v Nathan Carver>Because we've already shown that we can take a BOM in Msbc and put it in Github.</v>

00:30:17.026 --> 00:30:18.826
<v Nathan Carver>and create all the structure from that.</v>

00:30:24.106 --> 00:30:34.666
<v Nathan Carver>So if it changes the flow of information, but we end up with the same version BOM in Github.</v>

00:30:37.706 --> 00:30:39.786
<v Nathan Carver>That the CO can use.</v>

00:30:42.586 --> 00:30:45.066
<v Nathan Carver>that the CO can use as its source of truth.</v>

00:31:10.986 --> 00:31:14.586
<v Nathan Carver>Is there a new message? Oh, there they are. I see them. Okay, they're coming through.</v>

00:31:16.906 --> 00:31:18.026
<v Nathan Carver>Okay, here we go.</v>

00:31:22.506 --> 00:31:24.106
<v Nathan Carver>Engineering source of truth.</v>

00:31:26.746 --> 00:31:27.386
<v Nathan Carver>Correct.</v>

00:31:40.906 --> 00:31:43.866
<v Nathan Carver>Okay, so Val doesn't want Msbc as a starting point.</v>

00:31:52.106 --> 00:31:52.546
<v Nathan Carver>Okay.</v>

00:31:55.826 --> 00:31:56.906
<v Nathan Carver>So from here.</v>

00:31:59.706 --> 00:32:00.906
<v Nathan Carver>The structure.</v>

00:32:03.466 --> 00:32:05.146
<v Nathan Carver>That I experimented with.</v>

00:32:06.266 --> 00:32:06.826
<v Nathan Carver>And.</v>

00:32:09.986 --> 00:32:10.586
<v Nathan Carver>Let's see.</v>

00:32:13.066 --> 00:32:14.186
<v Nathan Carver>The Pcie I have it.</v>

00:32:15.546 --> 00:32:23.786
<v Nathan Carver>Automatic net was with scripting is I took the e-mail Val sent yesterday afternoon.</v>

00:32:25.626 --> 00:32:25.786
<v Nathan Carver>Um...</v>

00:32:27.146 --> 00:32:32.906
<v Nathan Carver>and just started creating a concept of the highest assembly point, so the actual product.</v>

00:32:33.946 --> 00:32:36.346
<v Nathan Carver>And then that would be...</v>

00:32:37.226 --> 00:32:55.786
<v Nathan Carver>This would also end up with its own structure inside the main hardware manufacturing repo. And then from this, this would be the main product that goes into Msbc. And then obviously the BOM, however, Msbc structures that BOM under this.</v>

00:32:57.066 --> 00:32:58.986
<v Nathan Carver>if this is the highest assembly point.</v>

00:33:05.546 --> 00:33:06.986
<v Nathan Carver>So, from this...</v>

00:33:08.106 --> 00:33:12.026
<v Nathan Carver>Here, we can take, we can do the scripting, so we...</v>

00:33:15.226 --> 00:33:16.506
<v Nathan Carver>We can take.</v>

00:33:17.906 --> 00:33:23.466
<v Nathan Carver>something that has an interface, that has a contractual agreement like these parts that I showed here.</v>

00:33:24.746 --> 00:33:30.266
<v Nathan Carver>And we can use the agent in combination with a script to generate.</v>

00:33:32.186 --> 00:33:33.786
<v Nathan Carver>A BOM, and then also...</v>

00:33:36.826 --> 00:33:40.986
<v Nathan Carver>do some scripted validation to ensure that all the interfaces are correct.</v>

00:33:42.826 --> 00:33:49.626
<v Nathan Carver>So at the end of that stream would be the, there's a stage of human, human review and human approval, whatever it produces.</v>

00:33:52.346 --> 00:33:52.666
<v Nathan Carver>Um...</v>

00:33:54.306 --> 00:34:06.746
<v Nathan Carver>And then there may also be, how do we keep the agent instructions for doing it? And that would be, human would review the instructions and update the instructions as needed to improve output.</v>

00:34:09.146 --> 00:34:09.466
<v Nathan Carver>Um...</v>

00:34:11.866 --> 00:34:18.826
<v Nathan Carver>But I think we still need to work, if we need to work out that workflow, like, like again, I'm not as I'm not familiar with that, so I don't know.</v>

00:34:20.026 --> 00:34:33.866
<v Nathan Carver>Everything that you're doing, Genadi, and how that would work, but as far as the scripting goes, we can we can create a structure and create this flow that Val wants of pushing things into Msbc.</v>

00:34:50.266 --> 00:34:52.106
<v Nathan Carver>So, from here, I think...</v>

00:34:55.386 --> 00:35:11.266
<v Nathan Carver>For me to understand what this would have to do in more detail is I would need the real world examples of this is how it, this is how we're doing it now, and this is how we can measure success of the</v>

00:35:12.706 --> 00:35:27.866
<v Nathan Carver>of an automated piece. Because I know you've explained it to me, but it's because I'm so new to this, it's still, I'm still trying to understand, get my head wrapped around everything. And I know there's complexities here. I miss it.</v>

00:35:27.226 --> 00:35:30.106
<v Genadi Peari>Can you take a flat structure, flat?</v>

00:35:31.866 --> 00:35:34.786
<v Genadi Peari>Parts for one or even for this product.</v>

00:35:35.786 --> 00:35:51.026
<v Genadi Peari>and try to build a bill of material without having the structure in front of, without giving him the structure, the existing structure, to see what they were coming up with.</v>

00:35:39.346 --> 00:35:39.466
<v Nathan Carver>Yeah.</v>

00:35:41.626 --> 00:35:41.786
<v Nathan Carver>Yeah.</v>

00:35:52.186 --> 00:35:53.226
<v Nathan Carver>So, create like...</v>

00:35:54.986 --> 00:35:58.986
<v Genadi Peari>For example, I mean, this is the, this is the real world.</v>

00:35:56.106 --> 00:35:57.386
<v Nathan Carver>Yep, so rather than...</v>

00:35:59.786 --> 00:36:00.266
<v Nathan Carver>Okay.</v>

00:36:01.866 --> 00:36:07.466
<v Nathan Carver>So if you just point me where that input data is, and I can start working on that.</v>

00:36:09.146 --> 00:36:17.386
<v Nathan Carver>And basically to take that input and turn it into this contract and then push that up.</v>

00:36:21.626 --> 00:36:23.466
<v Nathan Carver>Into Msbc.</v>

00:36:27.546 --> 00:36:38.186
<v Nathan Carver>So with the scripts involved, I mean, if the scripts, we have the scripts and we have data structures, these data contracts, GAMOA files here.</v>

00:36:41.066 --> 00:36:59.866
<v Nathan Carver>Using an agent would just speed up the process, but we wouldn't have to because the scripts don't need an agent to validate the BOM and they don't need an agent to push this up to Msbc. The agent is just there to, you know, automate some, speed up some decision processes. But</v>

00:37:01.866 --> 00:37:06.666
<v Nathan Carver>There's no reason I, there's no reason a person couldn't just build all this in Github.</v>

00:37:08.426 --> 00:37:09.706
<v Nathan Carver>Then it comes down to...</v>

00:37:11.026 --> 00:37:22.346
<v Nathan Carver>What saves us time? Like, what's important for the agent to do? What saves us time, and what does the person need to do? But the source would all stay in Github and get pushed up to Msbc regardless of.</v>

00:37:23.626 --> 00:37:24.666
<v Nathan Carver>Who does that work?</v>

00:37:35.786 --> 00:37:37.386
<v Nathan Carver>We want to use agents.</v>

00:37:47.226 --> 00:37:48.746
<v Nathan Carver>agents to assemble the bomb.</v>

00:39:21.546 --> 00:39:22.426
<v Nathan Carver>Okay, so...</v>

00:39:24.826 --> 00:39:32.746
<v Nathan Carver>Let's do that, Genadi. Let's, I'll take the source that you have and use that as the starting point and build.</v>

00:39:34.586 --> 00:39:36.706
<v Nathan Carver>Doing here what Val is laying out.</v>

00:39:42.706 --> 00:39:47.626
<v Genadi Peari>How do we visualize the BOM for approval with Excel?</v>

00:39:49.866 --> 00:39:53.466
<v Genadi Peari>Agent build what physically? The Excel file?</v>

00:39:56.156 --> 00:40:04.156
<v Nathan Carver>I will figure that, I'll figure that out. What do we need? What can be, what kind of data file can a human actually review?</v>

00:40:06.586 --> 00:40:07.386
<v Nathan Carver>efficiently.</v>

00:40:10.386 --> 00:40:15.146
<v Nathan Carver>And maybe it spits out a CSV, right, that Excel can open and use.</v>

00:40:16.186 --> 00:40:17.786
<v Nathan Carver>and a human can review that way.</v>

00:40:20.386 --> 00:40:23.786
<v Nathan Carver>Because the data files will be big, so we'll have to, I'll have to figure that out.</v>

00:40:25.146 --> 00:40:39.386
<v Genadi Peari>We need to figure out a few things then. Sometimes we create identical, very similar bill of materials for different jurisdictions. And the difference might be one item.</v>

00:40:28.746 --> 00:40:28.866
<v Nathan Carver>One.</v>

00:40:31.306 --> 00:40:31.506
<v Nathan Carver>Yeah.</v>

00:40:40.906 --> 00:40:41.546
<v Nathan Carver>I see.</v>

00:40:42.986 --> 00:40:43.546
<v Genadi Peari>So.</v>

00:40:45.786 --> 00:40:50.026
<v Genadi Peari>Or are we going to build a new one? Or the difference might be...</v>

00:40:50.426 --> 00:40:50.666
<v Nathan Carver>Pay.</v>

00:40:51.146 --> 00:40:55.626
<v Genadi Peari>Information which human somebody told.</v>

00:40:57.066 --> 00:41:00.346
<v Genadi Peari>Can information come from sales?</v>

00:41:02.106 --> 00:41:03.466
<v Genadi Peari>Right, for example.</v>

00:41:04.346 --> 00:41:06.586
<v Genadi Peari>For this customer, I want to provide.</v>

00:41:07.546 --> 00:41:08.266
<v Genadi Peari>Whatever.</v>

00:41:09.866 --> 00:41:17.946
<v Nathan Carver>Does that end up as separate? So if you had a bill of material and then for a specific...</v>

00:41:10.746 --> 00:41:11.306
<v Genadi Peari>This is.</v>

00:41:19.306 --> 00:41:21.466
<v Nathan Carver>district or division you had.</v>

00:41:22.666 --> 00:41:27.466
<v Nathan Carver>a part that's different. Is that a whole new bill of material in Msbc? Or is there like...</v>

00:41:26.906 --> 00:41:30.426
<v Genadi Peari>Yes, yes, because it's a different customer. He needs to...</v>

00:41:31.746 --> 00:41:41.706
<v Genadi Peari>when the production order has to see this, the difference, even if it's one small cable which has to be provided.</v>

00:41:31.946 --> 00:41:32.346
<v Nathan Carver>Okay.</v>

00:41:42.866 --> 00:41:43.306
<v Nathan Carver>Okay.</v>

00:41:43.146 --> 00:41:49.226
<v Genadi Peari>And this is not necessarily engineering information, might come from the sales, the difference.</v>

00:41:49.866 --> 00:41:50.826
<v Nathan Carver>Okay, understood.</v>

00:41:53.786 --> 00:42:04.346
<v Nathan Carver>So yeah, if we were mirroring Msbc and Github and we had that as a source of truth. So in Github, there would be that same bill of material for each one.</v>

00:42:05.466 --> 00:42:11.306
<v Nathan Carver>So the question is, how does the humans review that? And as you were saying, it's only one part difference.</v>

00:42:13.386 --> 00:42:13.946
<v Nathan Carver>And.</v>

00:42:16.226 --> 00:42:21.546
<v Nathan Carver>I think the review in that could just kind of come down to what tools do we use to do that job.</v>

00:42:22.426 --> 00:42:22.986
<v Genadi Peari>Yes.</v>

00:42:26.186 --> 00:42:26.666
<v Nathan Carver>Okay.</v>

00:42:37.866 --> 00:42:39.226
<v Nathan Carver>Okay, we have the quality.</v>

00:42:40.666 --> 00:42:41.066
<v Nathan Carver>Okay.</v>

00:42:44.346 --> 00:42:57.066
<v Nathan Carver>So, that's good to know. So, Genadi, that the source, what product we want to assemble first, and if it has a variable.</v>

00:42:55.386 --> 00:43:03.306
<v Genadi Peari>Ohh, let's do the let's the current do the current one, the the the pay slim, uh, and the...</v>

00:43:04.106 --> 00:43:05.186
<v Nathan Carver>Hey, slim, okay.</v>

00:43:05.386 --> 00:43:06.026
<v Genadi Peari>It's a.</v>

00:43:08.346 --> 00:43:11.146
<v Genadi Peari>I'll show you in Github, it's...</v>

00:43:13.026 --> 00:43:15.226
<v Genadi Peari>Um, I'll send the link.</v>

00:43:16.746 --> 00:43:18.426
<v Nathan Carver>Okay, perfect.</v>

00:43:17.786 --> 00:43:18.266
<v Genadi Peari>Ohh.</v>

00:43:20.666 --> 00:43:36.426
<v Genadi Peari>Because this is the product we go into deploy soon and we actually need all this before that Val mentioned, we will need it. Send it quotations and getting parts and everything.</v>

00:43:39.226 --> 00:43:40.826
<v Nathan Carver>Okay, perfect.</v>

00:44:07.466 --> 00:44:07.626
<v Nathan Carver>Yeah.</v>

00:44:11.306 --> 00:44:11.546
<v Nathan Carver>Okay.</v>

00:44:25.626 --> 00:44:40.106
<v Genadi Peari>So just for your understanding, this is final product, right? In this product, if we get, for example, different printer, the part number will be different, definitely, because it has a...</v>

00:44:41.186 --> 00:45:01.226
<v Genadi Peari>It's not just a revision, it's a different model. If you open this product, you will see like 5 different modules, one of them the kit for the money devices, one for the printer, and so on and so forth. So these items, these final part numbers might be...</v>

00:45:01.786 --> 00:45:09.466
<v Genadi Peari>Six, 7, 10, at least, depending on the parts which come in inside.</v>

00:45:10.506 --> 00:45:11.066
<v Nathan Carver>I see.</v>

00:45:10.546 --> 00:45:15.786
<v Genadi Peari>If we change something, we have to change the top bill of part number.</v>

00:45:12.106 --> 00:45:12.266
<v Nathan Carver>Yeah.</v>

00:45:17.626 --> 00:45:18.106
<v Nathan Carver>Okay.</v>

00:45:17.626 --> 00:45:19.706
<v Genadi Peari>It might go to different customers.</v>

00:45:21.146 --> 00:45:28.026
<v Nathan Carver>So if you were to do that, or when that happens, you change the printer, that becomes a new BOM with that new configuration.</v>

00:45:29.146 --> 00:45:43.386
<v Genadi Peari>Yes, and the production, when they ship it, they see, oh, we haven't stocked these printers, we will be sending this. Oh, this customer requires the particular bill acceptor, we have to send with the particular model. So we'll keep a few.</v>

00:45:44.266 --> 00:45:47.386
<v Genadi Peari>Uh, items, uh, product, uh, product numbers.</v>

00:45:48.826 --> 00:45:50.106
<v Nathan Carver>I see, OK.</v>

00:45:52.986 --> 00:45:53.946
<v Nathan Carver>Okay, that makes sense.</v>

00:46:03.706 --> 00:46:04.346
<v Nathan Carver>Okay, Val.</v>

00:50:16.546 --> 00:50:17.306
<v Nathan Carver>Okay.</v>

00:50:19.546 --> 00:50:23.306
<v Nathan Carver>So, there's a future where a bomb is ordered, but...</v>

00:50:25.386 --> 00:50:29.306
<v Nathan Carver>The customer wants a modification that is given to.</v>

00:50:31.146 --> 00:50:33.386
<v Nathan Carver>That's fed into the agent who then...</v>

00:50:34.346 --> 00:50:38.266
<v Nathan Carver>makes that modification and automatically creates the new BOM.</v>

00:50:43.546 --> 00:50:45.706
<v Genadi Peari>Yes, Val is correct.</v>

00:50:43.626 --> 00:50:44.026
<v Nathan Carver>Okay.</v>

00:50:45.346 --> 00:50:45.546
<v Nathan Carver>What?</v>

00:50:53.386 --> 00:50:53.866
<v Nathan Carver>Okay.</v>

00:50:53.466 --> 00:51:11.786
<v Genadi Peari>I'm not saying that it's not possible, but I'm just saying there is such an option. The requirement might come from the salesperson, might come from the production, something is wrong, they need to improve it. What I'm saying just, they might be needed in some additional.</v>

00:51:02.506 --> 00:51:02.586
<v Nathan Carver>Oh.</v>

00:51:13.626 --> 00:51:14.346
<v Genadi Peari>Human.</v>

00:51:15.626 --> 00:51:15.866
<v Genadi Peari>Um...</v>

00:51:17.626 --> 00:51:18.346
<v Genadi Peari>Touch up.</v>

00:51:19.786 --> 00:51:24.266
<v Nathan Carver>Yeah, a verification, a human, yeah.</v>

00:51:21.666 --> 00:51:23.066
<v Genadi Peari>Verification, yes.</v>

00:51:27.066 --> 00:51:28.666
<v Genadi Peari>Because this might be important.</v>

00:52:11.066 --> 00:52:13.146
<v Nathan Carver>Yeah, I agree. There will be a point in time where...</v>

00:52:14.306 --> 00:52:18.186
<v Nathan Carver>we have more confidence that the agent's producing something.</v>

00:52:20.186 --> 00:52:20.826
<v Nathan Carver>Something good.</v>

00:52:41.946 --> 00:52:42.266
<v Nathan Carver>Right.</v>

00:52:43.466 --> 00:52:45.706
<v Nathan Carver>Well, and it's also maybe it's...</v>

00:52:46.666 --> 00:52:55.466
<v Nathan Carver>30 bombs away, right? Once we see this thing produce 30 consecutive bombs that need no corrections, then our confidence level is way up and it's...</v>

00:52:56.506 --> 00:52:59.226
<v Nathan Carver>May not be a new model, but better instructions are.</v>

00:53:06.746 --> 00:53:18.026
<v Genadi Peari>Nathan, please don't forget what we what Val you see in the text before the all requirements to the CO.</v>

00:53:09.946 --> 00:53:10.186
<v Nathan Carver>It.</v>

00:53:14.986 --> 00:53:15.466
<v Nathan Carver>Yes.</v>

00:53:19.626 --> 00:53:21.546
<v Genadi Peari>They need, we need to keep them in mind.</v>

00:53:22.426 --> 00:53:22.986
<v Nathan Carver>Okay.</v>

00:53:23.626 --> 00:53:24.026
<v Genadi Peari>Right.</v>

00:53:24.826 --> 00:53:25.386
<v Nathan Carver>Correct.</v>

00:53:30.666 --> 00:53:33.306
<v Nathan Carver>Okay, so I'm going to run with this.</v>

00:53:35.706 --> 00:53:40.266
<v Nathan Carver>I'll take the Flex Pay slim for Georgia and start the process of...</v>

00:53:42.026 --> 00:53:44.426
<v Nathan Carver>starting where we are now and assembling a BOM.</v>

00:53:46.506 --> 00:53:48.746
<v Nathan Carver>Running it through the through the workflow.</v>

00:53:50.066 --> 00:53:50.266
<v Nathan Carver>Um...</v>

00:53:51.266 --> 00:53:56.906
<v Nathan Carver>Look at my calendar. So I am out next week, but then that Val, you want this done.</v>

00:53:58.106 --> 00:53:59.946
<v Nathan Carver>End of month, so I will.</v>

00:54:01.146 --> 00:54:02.586
<v Nathan Carver>Jump on that when I'm back.</v>

00:54:04.266 --> 00:54:05.306
<v Nathan Carver>following week.</v>

00:54:08.266 --> 00:54:25.226
<v Genadi Peari>Nathan, I understand I need to do some work with shuffling repositories and maybe we need to discuss it because whatever you need, because I I don't know how what I I can help with this.</v>

00:54:08.826 --> 00:54:08.986
<v Nathan Carver>Yes.</v>

00:54:21.546 --> 00:54:21.786
<v Nathan Carver>Great.</v>

00:54:26.186 --> 00:54:26.746
<v Nathan Carver>Okay.</v>

00:54:26.346 --> 00:54:29.386
<v Genadi Peari>if needed, but just let me know.</v>

00:54:31.146 --> 00:54:36.266
<v Genadi Peari>If it requires more detailed discussion, please.</v>

00:54:35.786 --> 00:54:41.066
<v Nathan Carver>Okay, I will, yeah, I'll set up time for us to discuss.</v>

00:54:37.546 --> 00:54:39.066
<v Genadi Peari>I will, I will be able, OK.</v>

00:54:42.426 --> 00:54:45.626
<v Nathan Carver>As I, as I get going, as needed, so OK.</v>

00:54:47.546 --> 00:54:48.746
<v Nathan Carver>Sounds good. Thank you, Genadi.</v>

00:54:51.146 --> 00:54:55.306
<v Genadi Peari>Yeah, well understood. Must be equal to Project in Jira. Yes, we...</v>

00:54:58.106 --> 00:54:58.666
<v Nathan Carver>Yes.</v>

00:54:58.346 --> 00:54:59.626
<v Genadi Peari>It's still...</v>

00:55:01.466 --> 00:55:02.506
<v Genadi Peari>I need solid.</v>

00:55:09.146 --> 00:55:09.626
<v Nathan Carver>Okay.</v>

00:55:11.946 --> 00:55:13.866
<v Genadi Peari>OK, thank you, thank you.</v>

00:55:13.386 --> 00:55:13.986
<v Nathan Carver>Thanks, guys.</v>

