# Raw Transcript — AI-logic for assembling BOM-continued-November-18
**Date:** November 18, 2026, 4:36 PM – 4:54 PM Eastern
**Summary note:** [[Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026]]
---
WEBVTT

00:00:04.721 --> 00:00:07.481
<v Nathan Carver>What I want to do, let's see here, share screen.</v>

00:00:14.441 --> 00:00:19.721
<v Nathan Carver>So using multiple agents to assemble this bomb and...</v>

00:00:21.241 --> 00:00:23.881
<v Nathan Carver>Val, I try to get as close to what we had discussed.</v>

00:00:26.201 --> 00:00:31.801
<v Nathan Carver>And had ran at several simulations, having one agent just be the.</v>

00:00:34.521 --> 00:00:35.481
<v Nathan Carver>Just a non.</v>

00:00:36.441 --> 00:00:40.281
<v Nathan Carver>a non-expert asking to build something. And...</v>

00:00:42.561 --> 00:00:51.801
<v Nathan Carver>We ended up with that question-answer routine between the assembler agent and the user agent.</v>

00:00:53.641 --> 00:01:04.361
<v Nathan Carver>So the idea is don't give it any technical direction on what to build, but tell it what interfaces you need for the sub-assembly that we're building.</v>

00:01:04.321 --> 00:01:09.961
<v Val Levitan>And the and the and the interfaces were taken from the data contracts.</v>

00:01:10.681 --> 00:01:12.201
<v Nathan Carver>Correct, so in this case...</v>

00:01:12.761 --> 00:01:21.721
<v Val Levitan>And you have, and you have two agents: one is the assembly agent, one is the client agent who emulates, I don't know, Genadi.</v>

00:01:13.281 --> 00:01:13.481
<v Nathan Carver>Big.</v>

00:01:23.241 --> 00:01:27.961
<v Nathan Carver>Correct, yep, and so it there's there was three agents.</v>

00:01:29.041 --> 00:01:37.321
<v Nathan Carver>Three different, 3 scoped agents. So there's an auditor and an assembler and a spec writer.</v>

00:01:38.521 --> 00:01:39.801
<v Nathan Carver>Um, so...</v>

00:01:39.641 --> 00:01:52.521
<v Val Levitan>That could be a fourth agent that says, I couldn't find this data sheet, but I'm buying it from company ABC in China. Ask them to send you the data sheet.</v>

00:01:54.281 --> 00:01:58.281
<v Nathan Carver>Correct. Yeah, and it could automate, right, and just automate that message.</v>

00:02:00.001 --> 00:02:01.241
<v Nathan Carver>An agent that handles that.</v>

00:02:01.721 --> 00:02:15.321
<v Val Levitan>So I read through everything that you sent me. I actually read every single sentence. I mean, I mean, to me, it's black and white. It's clear. I'm ecstatic about.</v>

00:02:07.241 --> 00:02:08.121
<v Nathan Carver>Okay, good.</v>

00:02:16.761 --> 00:02:23.001
<v Val Levitan>the result. Am I being too optimistic?</v>

00:02:24.561 --> 00:02:33.241
<v Nathan Carver>No, I don't think so. I think the result was very positive because it assembled some. It asked, the one thing I liked was it was asking good questions.</v>

00:02:34.361 --> 00:02:36.481
<v Val Levitan>Yeah, and and and COO.</v>

00:02:34.521 --> 00:02:39.481
<v Nathan Carver>or at least it went through several iterations of questions to get to where it needed to go.</v>

00:02:40.281 --> 00:02:46.521
<v Val Levitan>Exactly. And the questions that it was asking was because there wasn't enough information to begin with.</v>

00:02:47.321 --> 00:02:47.641
<v Nathan Carver>Right.</v>

00:02:48.841 --> 00:02:59.321
<v Val Levitan>I mean, if we had a better information, there would be no questions. It would just go out and build. But I like the fact that it's asking questions and not just stupid the building.</v>

00:03:00.441 --> 00:03:00.921
<v Nathan Carver>Yes.</v>

00:03:01.081 --> 00:03:03.921
<v Val Levitan>Some, some nonsense, and if we...</v>

00:03:03.321 --> 00:03:04.121
<v Genadi Peari>Define the.</v>

00:03:05.721 --> 00:03:06.121
<v Val Levitan>Yeah.</v>

00:03:06.441 --> 00:03:13.161
<v Genadi Peari>The funny thing is the partially, I mean, more than half of the answers, they are in the product requirements.</v>

00:03:14.361 --> 00:03:16.041
<v Val Levitan>Yes, yes.</v>

00:03:19.961 --> 00:03:30.681
<v Val Levitan>So, Nathan, just for Genadi maybe, and for me maybe, just to inhale this a little bit fuller, you gave</v>

00:03:29.241 --> 00:03:29.721
<v Nathan Carver>Mhm.</v>

00:03:33.081 --> 00:03:40.841
<v Val Levitan>The prompt was, here is the design purpose. This is what we're designing.</v>

00:03:41.921 --> 00:03:42.361
<v Val Levitan>Wyk.</v>

00:03:43.641 --> 00:03:44.361
<v Nathan Carver>Correct.</v>

00:03:44.841 --> 00:03:49.321
<v Val Levitan>This is where this is where the data contracts are.</v>

00:03:45.161 --> 00:03:45.881
<v Nathan Carver>Yeah, this.</v>

00:03:51.081 --> 00:03:55.001
<v Val Levitan>And I want you to build a sub-assembly for me, which is a power supply.</v>

00:03:56.441 --> 00:03:57.001
<v Nathan Carver>Correct.</v>

00:03:59.401 --> 00:04:14.601
<v Val Levitan>and it had a flat list of parts. You didn't tell the agent that this part goes here, the other part goes here. The agent only had data contracts and says, okay, how do I figure out where everything goes?</v>

00:04:16.041 --> 00:04:16.681
<v Nathan Carver>That's right.</v>

00:04:18.681 --> 00:04:20.841
<v Val Levitan>So, Genadi, this is fantastic.</v>

00:04:18.921 --> 00:04:19.241
<v Nathan Carver>Yeah.</v>

00:04:24.201 --> 00:04:28.761
<v Nathan Carver>So, from Genadi perspective, this would be the starting sentence.</v>

00:04:24.361 --> 00:04:24.681
<v Genadi Peari>Up.</v>

00:04:30.601 --> 00:04:32.041
<v Nathan Carver>And then, from here...</v>

00:04:33.241 --> 00:04:34.601
<v Nathan Carver>It moves into these.</v>

00:04:35.961 --> 00:04:47.081
<v Nathan Carver>questions. So the assembler coming back and asking these questions. And then we simulated answers for this, but that's what it would look like.</v>

00:04:38.481 --> 00:04:38.841
<v Val Levitan>Van.</v>

00:04:48.841 --> 00:04:57.241
<v Val Levitan>But Genadi would say, you know what, go get the data sheet or call the supplier or e-mail the supplier.</v>

00:05:03.161 --> 00:05:04.681
<v Val Levitan>Because the goal is...</v>

00:05:05.721 --> 00:05:10.761
<v Val Levitan>To have assembled, clean, pure.</v>

00:05:11.641 --> 00:05:25.001
<v Val Levitan>flat library of data sheets, either from JVL as the source or from whoever a third party supplier is as a source. And everything lays flat.</v>

00:05:28.241 --> 00:05:31.481
<v Val Levitan>Without a hint of where everything goes.</v>

00:05:32.641 --> 00:05:36.281
<v Val Levitan>And then the agent says, ohh, I need to assemble.</v>

00:05:37.561 --> 00:05:38.281
<v Val Levitan>The.</v>

00:05:39.561 --> 00:05:40.761
<v Val Levitan>You know, flex.</v>

00:05:41.561 --> 00:05:45.721
<v Val Levitan>Pay slim. This is how it looks like.</v>

00:05:47.401 --> 00:05:51.721
<v Val Levitan>I'm going to assemble a power supply for it. Let me start working on it.</v>

00:05:53.001 --> 00:05:56.201
<v Val Levitan>I don't know certain answers. Let me ask Genadi.</v>

00:05:57.401 --> 00:06:07.641
<v Val Levitan>Genadi doesn't say connect this to this. Genadi simply adds to the description. The description is saved once forever.</v>

00:06:09.561 --> 00:06:09.961
<v Val Levitan>Ohh.</v>

00:06:11.401 --> 00:06:17.561
<v Val Levitan>We could actually back into requirements and acceptance criteria from here.</v>

00:06:19.161 --> 00:06:20.841
<v Nathan Carver>Yes, yeah, I think so.</v>

00:06:25.281 --> 00:06:26.441
<v Val Levitan>This is just incredible.</v>

00:06:26.601 --> 00:06:27.081
<v Genadi Peari>Ohh.</v>

00:06:28.281 --> 00:06:36.121
<v Genadi Peari>You didn't even tell him that we need that much power for this product? How he...</v>

00:06:36.961 --> 00:06:45.401
<v Genadi Peari>What was his guess? I mean, well, he picked the best available, most powerful.</v>

00:06:39.961 --> 00:06:40.361
<v Nathan Carver>Um...</v>

00:06:45.961 --> 00:06:48.681
<v Nathan Carver>So the closest thing we got to that power question was...</v>

00:06:49.241 --> 00:06:49.801
<v Genadi Peari>Whoa.</v>

00:06:49.881 --> 00:06:52.201
<v Nathan Carver>120 volts, 60 hertz, right? That was...</v>

00:06:52.761 --> 00:06:53.641
<v Genadi Peari>Unbelievable.</v>

00:06:55.641 --> 00:06:59.081
<v Nathan Carver>Yeah, and so this is what it came back with.</v>

00:06:59.881 --> 00:07:02.241
<v Genadi Peari>Or to comprehend from the enemy.</v>

00:07:03.281 --> 00:07:09.241
<v Nathan Carver>And then it identified, it identified contracts that it needs that are still missing.</v>

00:07:03.481 --> 00:07:03.881
<v Genadi Peari>Val.</v>

00:07:10.961 --> 00:07:12.601
<v Nathan Carver>And then the auditors.</v>

00:07:13.801 --> 00:07:16.441
<v Nathan Carver>Even the auditor agents came back.</v>

00:07:17.961 --> 00:07:18.201
<v Nathan Carver>Um...</v>

00:07:19.401 --> 00:07:20.361
<v Nathan Carver>with findings.</v>

00:07:22.281 --> 00:07:23.241
<v Nathan Carver>And so...</v>

00:07:24.281 --> 00:07:25.961
<v Nathan Carver>It, it was able to iterate.</v>

00:07:27.561 --> 00:07:35.161
<v Nathan Carver>with the auditors. And then it could identify things it needs to close the gaps to get.</v>

00:07:37.801 --> 00:07:41.081
<v Nathan Carver>All the contracts that it would that it would need to make the assembly.</v>

00:07:43.961 --> 00:07:45.881
<v Nathan Carver>So, I think it was, it was...</v>

00:07:48.121 --> 00:07:50.921
<v Nathan Carver>I think the results were very, very good. I mean...</v>

00:07:56.121 --> 00:07:57.161
<v Nathan Carver>Let's see here.</v>

00:07:59.401 --> 00:08:00.521
<v Nathan Carver>Yeah, so...</v>

00:08:04.361 --> 00:08:09.401
<v Nathan Carver>And it's a collection of instructions. So if we want to open these up.</v>

00:08:12.121 --> 00:08:15.161
<v Nathan Carver>This is essentially the, it's kind of small, but.</v>

00:08:18.761 --> 00:08:25.881
<v Nathan Carver>This is the limited information we really gave the assembler. Now it does live in, it has access to all the files.</v>

00:08:30.201 --> 00:08:51.041
<v Nathan Carver>But this is the direction it's given. It's given all the structures and what folders to look in. So with that information, it was able to run. And then the auditor here, pretty much the same thing. So each one has their own specific role. And as you said, Val, we can add as many.</v>

00:08:51.801 --> 00:08:53.921
<v Nathan Carver>different prompts for different agents that we need.</v>

00:08:56.281 --> 00:09:03.561
<v Val Levitan>Okay, so I love it. I'm like, love it is an understatement. I am.</v>

00:09:04.121 --> 00:09:04.601
<v Nathan Carver>Good.</v>

00:09:05.081 --> 00:09:09.801
<v Val Levitan>Tickled pink, you understand? I have jitters, I have jitters.</v>

00:09:07.721 --> 00:09:08.041
<v Nathan Carver>Yeah.</v>

00:09:10.281 --> 00:09:10.841
<v Nathan Carver>All right.</v>

00:09:11.641 --> 00:09:15.081
<v Val Levitan>So, let's quickly build on it.</v>

00:09:16.041 --> 00:09:18.441
<v Val Levitan>I suggest that we...</v>

00:09:20.121 --> 00:09:22.441
<v Val Levitan>Identify who the supplier is.</v>

00:09:24.521 --> 00:09:24.921
<v Nathan Carver>Okay.</v>

00:09:24.921 --> 00:09:37.401
<v Val Levitan>and the information that is missing. So don't, the assembler doesn't go to Genadi. Let's just, Genadi is the last, is the last person that I want to take the attention from.</v>

00:09:40.121 --> 00:09:40.601
<v Nathan Carver>Okay.</v>

00:09:40.201 --> 00:09:45.801
<v Val Levitan>Who is the supplier? Who is the supplier? What's the contact information for the supplier?</v>

00:09:47.241 --> 00:09:53.641
<v Val Levitan>What are you looking from the supplier? Send a message to the supplier. Chase the supplier.</v>

00:09:54.601 --> 00:09:57.561
<v Val Levitan>Get the information, go back.</v>

00:09:58.641 --> 00:09:59.401
<v Val Levitan>Assemble.</v>

00:10:00.281 --> 00:10:02.761
<v Val Levitan>Identify what el what else is missing.</v>

00:10:04.201 --> 00:10:06.681
<v Val Levitan>And the certain looping motion.</v>

00:10:08.041 --> 00:10:08.601
<v Nathan Carver>Mhm.</v>

00:10:08.281 --> 00:10:16.281
<v Val Levitan>and update flat list, update data contracts. Data contracts have to be learning, it's a...</v>

00:10:17.641 --> 00:10:25.321
<v Val Levitan>The whole point about data contract is not to say what the data contract is. It needs to be self-defined.</v>

00:10:29.561 --> 00:10:31.241
<v Nathan Carver>Correct. Yep. Okay.</v>

00:10:30.761 --> 00:10:35.321
<v Val Levitan>Data conscience is a looping learning mechanism.</v>

00:10:37.801 --> 00:10:53.401
<v Val Levitan>Who is the supplier? What am I missing? Go get the information, put the information into data contract, update that data contract, go through the assembly loop again, assemble, assemble the component.</v>

00:10:54.601 --> 00:10:57.721
<v Val Levitan>Update, update the.</v>

00:11:00.041 --> 00:11:02.041
<v Val Levitan>inventory of whatever was missing.</v>

00:11:04.521 --> 00:11:05.001
<v Nathan Carver>Okay.</v>

00:11:07.001 --> 00:11:19.321
<v Val Levitan>So obviously, obviously, if supplier is not known, or certain information about a supplier is not known, get it from Genadi. But it will only take once.</v>

00:11:07.801 --> 00:11:08.121
<v Nathan Carver>All right.</v>

00:11:20.521 --> 00:11:21.001
<v Nathan Carver>Right.</v>

00:11:23.801 --> 00:11:39.641
<v Val Levitan>Then we're going to do the same thing for new suppliers. Let's say we're sourcing something, then sourcing data cannot be put into the flat list without the supplier information that we're looking for.</v>

00:11:41.841 --> 00:11:56.121
<v Val Levitan>And that's it. And we basically have a loop. We have a loop that alive, evolving, constantly evolving loop, where on one side we're looking for supplier, we're verifying the fit.</v>

00:11:57.161 --> 00:12:06.041
<v Val Levitan>Based on the data contracts, we're updating data contracts. We're checking the price with the supplier. We're saying change this supplier to this supplier.</v>

00:12:07.721 --> 00:12:10.921
<v Val Levitan>It is, it is incredible. I am blown away.</v>

00:12:10.041 --> 00:12:10.521
<v Nathan Carver>Mhm.</v>

00:12:13.961 --> 00:12:14.281
<v Nathan Carver>COO.</v>

00:12:14.241 --> 00:12:24.681
<v Val Levitan>I always felt that we had something, but right now this experiment shows me, oh my God, it's not only that I have something. Now I can see the actual loop because I see the question that it asks.</v>

00:12:25.561 --> 00:12:25.961
<v Nathan Carver>Yeah.</v>

00:12:27.401 --> 00:12:29.561
<v Nathan Carver>Yeah, I see that. Okay.</v>

00:12:32.841 --> 00:12:41.961
<v Nathan Carver>All right, I'm gonna start, I'm gonna, I'll take this transcript and I'll put together the focus for the next iteration and then</v>

00:12:43.481 --> 00:12:52.921
<v Val Levitan>I need a short, short next spike. Let's continue working on this assembly, sub-assembly.</v>

00:12:54.281 --> 00:13:06.761
<v Val Levitan>Let's make it learning and let's contact suppliers. Let's create an e-mail. Let's send out a message of what we need, what data sheet we need. Let's get the data sheet or chase the data sheet.</v>

00:13:07.721 --> 00:13:18.681
<v Val Levitan>update the data contract until we totally, finally, without any sort of human involvement, assemble the sub-assembly.</v>

00:13:20.121 --> 00:13:20.521
<v Nathan Carver>Okay.</v>

00:13:22.361 --> 00:13:27.081
<v Val Levitan>So, erase, erase all the, erase all the answers that you gave it.</v>

00:13:27.961 --> 00:13:43.201
<v Val Levitan>If you gave any answers, if you gave any hints, erase it. The only source, the only source that it could get new information, identify who the supplier is, go to the supplier, get the data, update your data contract, reassemble.</v>

00:13:30.601 --> 00:13:31.401
<v Nathan Carver>Correct, yeah.</v>

00:13:32.481 --> 00:13:32.761
<v Nathan Carver>Yeah.</v>

00:13:44.521 --> 00:13:45.001
<v Nathan Carver>Okay.</v>

00:13:46.801 --> 00:13:47.961
<v Nathan Carver>Yeah, we can do that.</v>

00:13:48.921 --> 00:13:51.161
<v Val Levitan>Erase all the answers you gave it.</v>

00:13:54.841 --> 00:13:55.561
<v Nathan Carver>And.</v>

00:13:56.641 --> 00:13:57.001
<v Nathan Carver>Okay.</v>

00:13:57.481 --> 00:14:00.321
<v Val Levitan>If you gave any answer, if you said use this.</v>

00:13:59.641 --> 00:14:05.801
<v Nathan Carver>No, it's even this runs in a sandbox, so every run is blank. It doesn't have any.</v>

00:14:06.921 --> 00:14:14.121
<v Nathan Carver>Persisting decisions or any any any persistent prompts or or information just the build this.</v>

00:14:15.481 --> 00:14:16.601
<v Nathan Carver>Um, so...</v>

00:14:15.881 --> 00:14:24.721
<v Val Levitan>So the only thing that you will be giving, the only information that you will be feeding it, is the information, let's say, about the supplier. If you don't know, we're together.</v>

00:14:23.921 --> 00:14:24.521
<v Nathan Carver>Mhm.</v>

00:14:26.361 --> 00:14:27.481
<v Nathan Carver>Correct, okay.</v>

00:14:29.401 --> 00:14:44.041
<v Val Levitan>Now, in the future, when we have a solid data contract and it's fully assembled and we're not missing anything, we're now saying, okay, we have our data contract. This is the part. Let's go out in the market.</v>

00:14:45.641 --> 00:14:51.481
<v Val Levitan>and look for a new supplier. So we say, okay, here's the data contract. This is the data sheet.</v>

00:14:52.521 --> 00:14:54.681
<v Val Levitan>Who can supply this part for me?</v>

00:14:57.401 --> 00:14:57.881
<v Nathan Carver>Okay.</v>

00:14:59.161 --> 00:14:59.721
<v Nathan Carver>I see.</v>

00:15:03.801 --> 00:15:04.281
<v Nathan Carver>All right.</v>

00:15:05.481 --> 00:15:14.441
<v Nathan Carver>Let's do, let's try to do another two or three day spike with some, yeah, let me see what I can get.</v>

00:15:10.441 --> 00:15:11.161
<v Val Levitan>Friday.</v>

00:15:15.521 --> 00:15:16.361
<v Nathan Carver>Friday.</v>

00:15:17.081 --> 00:15:19.281
<v Val Levitan>Let's try to get Friday at 4:00.</v>

00:15:20.761 --> 00:15:21.161
<v Nathan Carver>Okay.</v>

00:15:22.201 --> 00:15:30.041
<v Val Levitan>I will book the meeting. It took us, it took us 15 minutes or half an hour or so. Genadi, do you have any questions?</v>

00:15:23.961 --> 00:15:25.161
<v Nathan Carver>Okay, that sounds good.</v>

00:15:27.001 --> 00:15:27.401
<v Nathan Carver>Yep.</v>

00:15:31.721 --> 00:15:34.761
<v Genadi Peari>No, it's incredible.</v>

00:15:35.641 --> 00:15:36.281
<v Genadi Peari>Citing.</v>

00:15:38.481 --> 00:15:38.881
<v Genadi Peari>No.</v>

00:15:41.161 --> 00:15:41.321
<v Nathan Carver>Um...</v>

00:15:43.961 --> 00:15:44.601
<v Nathan Carver>Okay.</v>

00:15:46.041 --> 00:15:55.801
<v Nathan Carver>So I will, so Genadi, I'll have, I may just have some of these parts, just we need the supplier things that we do have.</v>

00:15:57.241 --> 00:15:57.961
<v Nathan Carver>put out there.</v>

00:15:58.441 --> 00:16:02.041
<v Val Levitan>Genadi, can you make sure that you have supplier information in the file there?</v>

00:16:02.801 --> 00:16:04.201
<v Genadi Peari>Yeah, I'll do.</v>

00:16:03.721 --> 00:16:11.001
<v Val Levitan>Not the data, don't give any data, just the supplier information. I actually like the fact that some data is missing.</v>

00:16:07.961 --> 00:16:08.601
<v Genadi Peari>Understood.</v>

00:16:12.601 --> 00:16:17.481
<v Nathan Carver>Okay, so we won't we won't hydrate all of it then. We'll leave some of that out so we can.</v>

00:16:18.441 --> 00:16:19.481
<v Nathan Carver>We can test with.</v>

00:16:21.801 --> 00:16:25.401
<v Nathan Carver>building the agent that's going to go get that information for us. Okay.</v>

00:16:25.241 --> 00:16:40.841
<v Val Levitan>And the agent should say, Mr. Supplier, I am one of your clients. We've been supplying us this thing. I'm missing data. I don't have this data sheet. I'm missing this and this information. Can you please supply it as soon as possible? That's it.</v>

00:16:41.481 --> 00:16:42.041
<v Nathan Carver>Okay.</v>

00:16:41.721 --> 00:16:57.161
<v Val Levitan>inhale the data, update the data contract, and go through the cycle. Can you assemble it now? Now you have the data, your data contracts have been updated. Can you assemble it now? No. What are you missing now?</v>

00:16:58.521 --> 00:16:59.641
<v Val Levitan>Let's go get that.</v>

00:16:58.521 --> 00:17:00.681
<v Nathan Carver>Yeah, OK.</v>

00:17:05.641 --> 00:17:15.321
<v Genadi Peari>There are two cases available, two options available. When there is generic part, which goes by description, then you go to any supplier in the world.</v>

00:17:16.601 --> 00:17:27.721
<v Genadi Peari>And the second case is when there is a dedicated part number, and then you this brand you can buy purchase from any supplier in the world, so two types of...</v>

00:17:28.121 --> 00:17:45.881
<v Val Levitan>I know, but we're not trying to purchase. All we're trying to do is to go to the exact supplier that we had already chosen that you built into your bill of material. You already know who you're using. So we're going back to that supplier, that exact supplier. We're saying, hey,</v>

00:17:46.121 --> 00:17:55.721
<v Val Levitan>We're buying it from you, but we're missing data sheets. We need data sheets. We're missing, let's say, opening holes. We're missing...</v>

00:17:57.161 --> 00:18:01.161
<v Val Levitan>You know, fastening parameters of some sort were missing.</v>

00:18:02.841 --> 00:18:06.441
<v Val Levitan>connectors, whatever we're missing. I don't know what we're missing.</v>

00:18:07.561 --> 00:18:09.881
<v Val Levitan>All we're trying to do is to build.</v>

00:18:12.361 --> 00:18:18.081
<v Val Levitan>The proper data contract, so we can assemble a sub-assembly.</v>

00:18:23.961 --> 00:18:24.761
<v Genadi Peari>Yes, clear.</v>

00:18:25.481 --> 00:18:33.001
<v Val Levitan>I'm going to send you a transcript of this meeting and we'll see you at 4 o'clock on Friday. Thank you very much. Excited.</v>

00:18:32.561 --> 00:18:37.641
<v Genadi Peari>Well, well, can I get your attention for a few minutes, literally a few minutes?</v>

00:18:32.681 --> 00:18:33.201
<v Nathan Carver>Alright.</v>

00:18:37.001 --> 00:18:40.201
<v Val Levitan>Yes, I'll call you. I'll call you on a separate call within 5 minutes.</v>

00:18:38.321 --> 00:18:38.601
<v Nathan Carver>But...</v>

00:18:39.641 --> 00:18:40.761
<v Genadi Peari>Thank you, thank you.</v>

00:18:40.841 --> 00:18:41.721
<v Nathan Carver>OK, thanks all.</v>

00:18:41.001 --> 00:18:41.561
<v Val Levitan>Thank you.</v>

