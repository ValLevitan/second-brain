# Raw Transcript — Call with Nathan Carver (ad-hoc Teams call, no calendar invite)
**Date:** October 5, 2026, 1:58 PM – 2:33 PM Eastern
**Summary note:** [[Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026]]
---
WEBVTT

00:00:03.518 --> 00:00:05.518
<v Val Levitan>How I think?</v>

00:00:07.918 --> 00:00:10.078
<v Val Levitan>The electro mechanical.</v>

00:00:15.278 --> 00:00:19.198
<v Val Levitan>the administrational part of the electromechanical.</v>

00:00:24.558 --> 00:00:26.318
<v Val Levitan>Bill of material should work.</v>

00:00:27.598 --> 00:00:28.158
<v Nathan Carver>Okay.</v>

00:00:29.038 --> 00:00:33.038
<v Val Levitan>So I'm just going to discuss with you the architectural side of it.</v>

00:00:33.918 --> 00:00:35.598
<v Val Levitan>And so...</v>

00:00:36.798 --> 00:00:45.358
<v Val Levitan>It's actually nearly one-to-one how we are attempting to build our development pipeline.</v>

00:00:47.758 --> 00:00:52.198
<v Val Levitan>So, the premise of the development pipeline is that...</v>

00:00:47.838 --> 00:00:48.598
<v Nathan Carver>Correct. Yeah.</v>

00:00:53.558 --> 00:01:01.998
<v Val Levitan>A project name in Jira is equal to 1 to 1 is equal to a repo code repo.</v>

00:01:04.158 --> 00:01:09.518
<v Val Levitan>Code repo in itself is has zero trust state.</v>

00:01:11.198 --> 00:01:14.518
<v Val Levitan>It contains pros.</v>

00:01:16.238 --> 00:01:18.598
<v Val Levitan>It contains ADRs.</v>

00:01:19.678 --> 00:01:21.838
<v Val Levitan>Along with the code, obviously.</v>

00:01:22.398 --> 00:01:22.878
<v Nathan Carver>Mhm.</v>

00:01:23.038 --> 00:01:24.558
<v Val Levitan>And it contains...</v>

00:01:25.598 --> 00:01:28.078
<v Val Levitan>Uh, data contracts.</v>

00:01:31.278 --> 00:01:32.078
<v Nathan Carver>Okay, yep.</v>

00:01:36.558 --> 00:01:37.278
<v Val Levitan>So...</v>

00:01:39.758 --> 00:01:51.678
<v Val Levitan>In my view, and please correct me if I'm wrong, I'm obviously not a specialist in this thing, but in my view, the electromechanical thing could be arranged exactly the same way.</v>

00:01:55.278 --> 00:02:00.798
<v Val Levitan>In GitHub, we can start from a flat list of all the parts.</v>

00:02:01.758 --> 00:02:02.318
<v Nathan Carver>Mhm.</v>

00:02:02.718 --> 00:02:06.318
<v Val Levitan>Across, we can have our JIRA project.</v>

00:02:08.078 --> 00:02:09.598
<v Val Levitan>You call to a repo?</v>

00:02:11.838 --> 00:02:15.118
<v Val Levitan>Inside of the repo, we could have...</v>

00:02:16.198 --> 00:02:20.878
<v Val Levitan>the pros and which is essential, data contracts.</v>

00:02:18.398 --> 00:02:18.518
<v Nathan Carver>Yeah.</v>

00:02:22.238 --> 00:02:28.798
<v Val Levitan>Data contracts is a description of what a certain sub-assembly does and how it works.</v>

00:02:29.918 --> 00:02:33.918
<v Val Levitan>But from a from an output perspective, because of zero trust.</v>

00:02:35.358 --> 00:02:43.358
<v Val Levitan>So it doesn't expect to hear from anybody else. It only tells the world, broadcast the world, how it works.</v>

00:02:44.718 --> 00:02:45.598
<v Nathan Carver>Okay, yep.</v>

00:02:50.478 --> 00:02:58.318
<v Val Levitan>By describing how it works, I think that Claude is smart enough.</v>

00:02:59.118 --> 00:03:00.318
<v Val Levitan>to assemble.</v>

00:03:01.198 --> 00:03:08.958
<v Val Levitan>either a bill of material for a complete machine, or a bill of material for a sub-assembly, or...</v>

00:03:09.998 --> 00:03:16.718
<v Val Levitan>And it could do it probably on the fly or through some sort of GitHub actions.</v>

00:03:19.678 --> 00:03:27.678
<v Val Levitan>where the final ISO image, you know, I'm pretending that this is a</v>

00:03:29.278 --> 00:03:41.438
<v Val Levitan>Code developers code, so obviously there's no ISO image here, but something similar to ISO image that we built through.</v>

00:03:31.398 --> 00:03:31.918
<v Nathan Carver>Mhm.</v>

00:03:43.278 --> 00:03:46.878
<v Val Levitan>GitHub action and we post it on Azure.</v>

00:03:49.438 --> 00:04:00.398
<v Val Levitan>Cloud as an ISO image. To me, it's the same as the bill of material, final bill of material in MSBC.</v>

00:04:03.278 --> 00:04:03.838
<v Nathan Carver>Yes.</v>

00:04:03.278 --> 00:04:05.998
<v Val Levitan>So, so this is kind of a...</v>

00:04:07.198 --> 00:04:11.278
<v Val Levitan>hazy image of what I think might work.</v>

00:04:12.798 --> 00:04:13.838
<v Val Levitan>But, of course.</v>

00:04:14.958 --> 00:04:16.838
<v Val Levitan>I don't have clarity on everything.</v>

00:04:20.838 --> 00:04:21.358
<v Nathan Carver>Correct.</v>

00:04:24.558 --> 00:04:32.238
<v Nathan Carver>So I agree. I think MSBC has a specific structure for their bill of material.</v>

00:04:33.358 --> 00:04:38.558
<v Nathan Carver>And so for us to programmatically build that should be.</v>

00:04:39.358 --> 00:04:41.438
<v Nathan Carver>Once we know the structure, once we know the input.</v>

00:04:43.198 --> 00:04:49.038
<v Nathan Carver>We wouldn't even need an agent, I don't think, to build it for us. We should be able to programmatically build it.</v>

00:04:50.398 --> 00:04:55.038
<v Nathan Carver>But what we need in the GitHub side in our repo.</v>

00:04:56.078 --> 00:04:57.278
<v Nathan Carver>Is that saying?</v>

00:04:58.358 --> 00:05:10.958
<v Nathan Carver>It doesn't have to be the same structure as BC, but it has to be an organized structure of data files that are just text because people edit them.</v>

00:05:12.158 --> 00:05:16.798
<v Nathan Carver>So it's essentially code that doesn't compile at that point. It has all the same.</v>

00:05:17.758 --> 00:05:22.878
<v Nathan Carver>Principles applied to it as source code would have. It is source code in that sense.</v>

00:05:24.638 --> 00:05:28.158
<v Nathan Carver>But it not not code that is compiled into an application.</v>

00:05:28.958 --> 00:05:33.758
<v Nathan Carver>So it gets compiled into a VC bomb.</v>

00:05:29.838 --> 00:05:31.358
<v Val Levitan>But, but, but I think...</v>

00:05:34.318 --> 00:05:41.198
<v Val Levitan>Correct, but I think the way it should be assembled is specifically through...</v>

00:05:43.598 --> 00:06:00.398
<v Val Levitan>data contracts. There should be a description of how things come together. Because if we do it once in the form of a dot MD file, it stays there forever. I mean, we always know that power comes from a power supply.</v>

00:05:46.958 --> 00:05:47.358
<v Nathan Carver>Yes.</v>

00:06:01.038 --> 00:06:01.438
<v Nathan Carver>Yeah.</v>

00:06:02.238 --> 00:06:09.518
<v Val Levitan>And we know that a power supply is connected to a PC board with a harness. Like I mean...</v>

00:06:10.478 --> 00:06:10.958
<v Nathan Carver>Right.</v>

00:06:11.358 --> 00:06:21.358
<v Val Levitan>And the monitor is connected to a PC board, and that's connected either to HDMI or to some other connector.</v>

00:06:21.758 --> 00:06:24.718
<v Nathan Carver>Right, and those interfaces I'll operate on.</v>

00:06:22.718 --> 00:06:26.318
<v Val Levitan>But there is, there is logic how everything works.</v>

00:06:28.078 --> 00:06:30.718
<v Val Levitan>That logic to me is data contract.</v>

00:06:32.238 --> 00:06:46.478
<v Val Levitan>And if the board is held by 4 screws, then it's understood. But then the spec takes over and says, well, the threat for this particular screw is, you know, blah, blah, blah.</v>

00:06:45.998 --> 00:06:47.438
<v Nathan Carver>Yeah, right.</v>

00:06:48.558 --> 00:06:53.758
<v Val Levitan>And that is already part of the spec that comes from a supplier.</v>

00:06:55.918 --> 00:07:05.678
<v Nathan Carver>Yeah, and I suspect every board, even down to the position of the screws, is following an industry standard specification so they can fit.</v>

00:07:07.278 --> 00:07:07.918
<v Val Levitan>Well.</v>

00:07:07.278 --> 00:07:09.278
<v Nathan Carver>So, it can attach itself, right?</v>

00:07:09.438 --> 00:07:18.478
<v Val Levitan>Yeah, I mean, I mean, how can Genadi spec a screw where a start is spec for, I don't know, for...</v>

00:07:20.078 --> 00:07:21.118
<v Val Levitan>Some other screw.</v>

00:07:20.238 --> 00:07:20.398
<v Nathan Carver>Mm.</v>

00:07:21.918 --> 00:07:22.238
<v Nathan Carver>Right.</v>

00:07:22.398 --> 00:07:24.398
<v Val Levitan>It just can't happen, right?</v>

00:07:25.838 --> 00:07:26.398
<v Nathan Carver>Correct.</v>

00:07:26.798 --> 00:07:39.678
<v Val Levitan>And if we're saying that this monitor needs to plug in into this interface, which is HDMI, well, you just can't provide a, you know, a different connector and a harness.</v>

00:07:40.478 --> 00:07:41.358
<v Nathan Carver>Correct, yeah.</v>

00:07:41.998 --> 00:07:46.798
<v Val Levitan>So, to me, to me, the way I understand it, these are data contracts.</v>

00:07:49.838 --> 00:07:51.518
<v Nathan Carver>Yeah, I agree.</v>

00:07:50.958 --> 00:07:59.198
<v Val Levitan>Call them whatever, call them whatever you want, maybe call them specification, call them whatever it is, but to me, it's just data contracts.</v>

00:08:00.478 --> 00:08:05.598
<v Val Levitan>This is how I work. It's A declaration of what I'm capable of doing.</v>

00:08:07.198 --> 00:08:09.358
<v Nathan Carver>Correct. Yeah, I agree.</v>

00:08:10.718 --> 00:08:24.158
<v Nathan Carver>I think there's terminology gaps between Genadi's world and GitHub and BC, but it's all the same. It's interfacing with each other, components, how they interface together.</v>

00:08:25.118 --> 00:08:33.518
<v Val Levitan>But what I what I don't want, I basically want to hand over the logic to AI.</v>

00:08:35.038 --> 00:08:35.438
<v Nathan Carver>Okay.</v>

00:08:35.358 --> 00:08:54.638
<v Val Levitan>and I want the source of truth to be flat, linear. And if you yank one card out of that linear list and replace it with another card, but assuming that it has compatible data contract, then it should work.</v>

00:08:54.878 --> 00:09:03.518
<v Val Levitan>But if the data contract changes, then it should say, that's fine, I'll pay this replacement. But please change the four screws and change the harness.</v>

00:08:55.118 --> 00:08:55.598
<v Nathan Carver>Correct.</v>

00:09:05.718 --> 00:09:24.478
<v Val Levitan>So it creates immediate conflict. So the logic of it, I don't want Genadi to be burdened with the logic because his design time is 30% of the time. 70% of the time is building the assembly manual, the, you know.</v>

00:09:05.918 --> 00:09:06.318
<v Nathan Carver>Got it.</v>

00:09:25.438 --> 00:09:35.278
<v Val Levitan>bill of material, descriptions, et cetera, et cetera, filing names. But instead of doing that, we'll have a...</v>

00:09:36.398 --> 00:09:42.558
<v Val Levitan>Naming Standards Convention will have filing naming conventions.</v>

00:09:43.198 --> 00:09:43.838
<v Nathan Carver>Mm-hmm.</v>

00:09:44.158 --> 00:09:59.278
<v Val Levitan>And so Claude goes and looks at it and say, okay, well, these are the standards. I can only name the file a certain way with the hyphens in between and four alphanumeric spaces here and three alphanumeric spaces here.</v>

00:10:00.598 --> 00:10:12.398
<v Val Levitan>And these are my revisions and these are my suppliers. And it doesn't need to know the financial aspect of these suppliers because the financial aspect is the administrational side of it.</v>

00:10:13.838 --> 00:10:14.878
<v Nathan Carver>Yeah, it makes sense.</v>

00:10:18.798 --> 00:10:28.478
<v Nathan Carver>It makes sense to me. Like, I don't see why that wouldn't work. With the proper conventions in place, you should be able to do that.</v>

00:10:30.558 --> 00:10:31.038
<v Val Levitan>Okay.</v>

00:10:32.278 --> 00:10:45.118
<v Val Levitan>Let's take flex, pay, slim, and let's reverse engineering out of that bill of material. Let's just grab this bill of material, let's flatten it.</v>

00:10:45.918 --> 00:10:46.318
<v Nathan Carver>Okay.</v>

00:10:47.318 --> 00:10:59.838
<v Val Levitan>put it in GitHub, and then let's reverse out of it, going into projects. Then when we broke it down into projects, we'll create repos.</v>

00:11:00.238 --> 00:11:00.718
<v Nathan Carver>Mhm.</v>

00:11:01.278 --> 00:11:03.998
<v Val Levitan>We'll create data contracts in those repos.</v>

00:11:05.478 --> 00:11:05.918
<v Nathan Carver>Okay.</v>

00:11:07.358 --> 00:11:10.558
<v Val Levitan>And then we'll create the logic of how these.</v>

00:11:12.318 --> 00:11:19.358
<v Val Levitan>Let's call it compiling, you know, the code compiling. Let's put it.</v>

00:11:21.278 --> 00:11:22.478
<v Val Levitan>On AI.</v>

00:11:25.118 --> 00:11:30.238
<v Val Levitan>to formalize the bill of material, to get into the bill of material.</v>

00:11:32.958 --> 00:11:33.438
<v Nathan Carver>Okay.</v>

00:11:33.678 --> 00:11:34.318
<v Val Levitan>Based.</v>

00:11:35.478 --> 00:11:49.598
<v Val Levitan>based on data contract. So my point is, when we troubleshoot and we say, okay, well, something is wrong. We came up with the wrong bill of material. We came up with the wrong bill of material because our data contracts are flawed.</v>

00:11:50.798 --> 00:11:59.118
<v Val Levitan>Let's go back into data contract, because the source of truth now is the actual data contract. That means it's not properly defined.</v>

00:11:59.998 --> 00:12:00.558
<v Nathan Carver>Correct.</v>

00:12:04.318 --> 00:12:04.718
<v Nathan Carver>Okay.</v>

00:12:07.118 --> 00:12:08.158
<v Nathan Carver>That makes sense to me.</v>

00:12:14.718 --> 00:12:19.518
<v Nathan Carver>OK, so we take the flex slim.</v>

00:12:20.878 --> 00:12:22.238
<v Nathan Carver>And reverse engineer.</v>

00:12:21.358 --> 00:12:23.678
<v Val Levitan>But flex pay flex pay slim.</v>

00:12:24.078 --> 00:12:25.038
<v Nathan Carver>Let's pay slim.</v>

00:12:26.078 --> 00:12:26.638
<v Val Levitan>Mhm.</v>

00:12:26.398 --> 00:12:31.198
<v Nathan Carver>Reverse that, reverse engineer that into this flat file.</v>

00:12:32.078 --> 00:12:33.678
<v Nathan Carver>structure in GitHub.</v>

00:12:34.398 --> 00:12:38.078
<v Val Levitan>You need, you need three things: you need flat file.</v>

00:12:39.438 --> 00:12:52.238
<v Val Levitan>You need project, you need to break down things into project. Projects to me is, for example, peripheral devices, that's a project. Monitors is a project.</v>

00:12:53.118 --> 00:12:53.758
<v Nathan Carver>I gotcha.</v>

00:12:54.438 --> 00:12:55.918
<v Val Levitan>Excuse me, please. I'm sorry.</v>

00:12:57.598 --> 00:12:58.078
<v Val Levitan>Hello?</v>

00:14:30.798 --> 00:14:31.518
<v Val Levitan>I'm sorry.</v>

00:14:32.718 --> 00:14:33.638
<v Nathan Carver>Alright, no problem.</v>

00:14:35.198 --> 00:14:40.238
<v Nathan Carver>OK, so project breakdown projects are monitors, peripheral devices.</v>

00:14:41.358 --> 00:14:43.798
<v Nathan Carver>So these independent components, they can be added.</v>

00:14:43.518 --> 00:14:54.318
<v Val Levitan>For yeah, yeah, PC boards, all of the PC boards, metal cabinet or cabinet, I should say, or enclosures, maybe enclosures.</v>

00:14:55.918 --> 00:14:56.318
<v Nathan Carver>Okay.</v>

00:14:56.718 --> 00:15:04.478
<v Val Levitan>Or maybe we should say not enclosures, maybe we should say sheet metal. And then we should say plastics.</v>

00:15:06.878 --> 00:15:07.358
<v Nathan Carver>Got it.</v>

00:15:09.598 --> 00:15:10.078
<v Nathan Carver>Okay.</v>

00:15:09.878 --> 00:15:16.638
<v Val Levitan>I think, I think actually Genadi has in his part numbers, I think he has categories.</v>

00:15:17.798 --> 00:15:27.278
<v Val Levitan>So it almost feels like those categories are the projects. For example, harnesses, it's his category, but to me it's a project.</v>

00:15:29.198 --> 00:15:29.958
<v Val Levitan>In Giorgi.</v>

00:15:33.678 --> 00:15:34.318
<v Nathan Carver>I.</v>

00:15:33.678 --> 00:15:37.518
<v Val Levitan>Because he's got he's got a bunch of harnesses that he has to design.</v>

00:15:39.278 --> 00:15:41.598
<v Nathan Carver>So, it's a project of harnesses.</v>

00:15:42.638 --> 00:15:43.438
<v Val Levitan>That's right.</v>

00:15:43.678 --> 00:15:46.398
<v Nathan Carver>So the project will encapsulate the related.</v>

00:15:47.758 --> 00:15:48.478
<v Nathan Carver>Components.</v>

00:15:50.078 --> 00:15:51.038
<v Nathan Carver>Or categories.</v>

00:15:50.158 --> 00:15:51.198
<v Val Levitan>So that will.</v>

00:15:51.998 --> 00:15:56.878
<v Val Levitan>So I'm just curious. I'm thinking out loud. Hold on, just bear with me.</v>

00:15:57.958 --> 00:16:03.678
<v Val Levitan>And actually, maybe you should help me think it through, because we want projects to be.</v>

00:16:06.078 --> 00:16:12.158
<v Val Levitan>repos and because we want repos to have data contracts.</v>

00:16:14.038 --> 00:16:15.358
<v Val Levitan>What should?</v>

00:16:16.718 --> 00:16:18.478
<v Val Levitan>Be treated as a project.</v>

00:16:22.718 --> 00:16:25.038
<v Nathan Carver>So, like, with these...</v>

00:16:26.558 --> 00:16:28.398
<v Nathan Carver>So taking the categories.</v>

00:16:32.638 --> 00:16:42.398
<v Nathan Carver>So I don't know how many items would be in a category, probably, I mean, dozens to hundreds. It could be all varied range.</v>

00:16:46.078 --> 00:16:53.838
<v Nathan Carver>So you wouldn't, I don't think you want a lot of repos. I think you want to limit the number of repos just for management's sake.</v>

00:16:55.038 --> 00:16:58.878
<v Nathan Carver>human just for cognitive ability to manage all the repos.</v>

00:17:00.718 --> 00:17:01.118
<v Nathan Carver>Um...</v>

00:17:02.478 --> 00:17:04.878
<v Nathan Carver>You could have a mono repo with.</v>

00:17:06.878 --> 00:17:11.278
<v Nathan Carver>various projects inside it, rather than one project per repo.</v>

00:17:13.358 --> 00:17:17.358
<v Val Levitan>No, if we have one monorepo, then JIRA doesn't work.</v>

00:17:18.358 --> 00:17:24.878
<v Val Levitan>because we want certain capabilities within a project. Project is described by capabilities.</v>

00:17:26.078 --> 00:17:27.358
<v Nathan Carver>Okay, okay.</v>

00:17:27.358 --> 00:17:33.358
<v Val Levitan>So, so harnesses, for example, are good to discuss under one project.</v>

00:17:35.678 --> 00:17:36.158
<v Nathan Carver>Okay.</v>

00:17:36.798 --> 00:17:39.438
<v Val Levitan>because they'll have a bunch of capabilities under it.</v>

00:17:42.238 --> 00:17:42.718
<v Nathan Carver>Okay.</v>

00:17:43.918 --> 00:17:45.118
<v Nathan Carver>That makes sense to me.</v>

00:17:46.318 --> 00:17:47.038
<v Nathan Carver>Um...</v>

00:17:52.478 --> 00:17:56.638
<v Nathan Carver>So then you would, okay, so each of these projects has.</v>

00:17:57.998 --> 00:17:59.118
<v Nathan Carver>A number of...</v>

00:18:00.318 --> 00:18:06.878
<v Nathan Carver>Components that could be added to the bill of material, right? One or more to a to a bill of material.</v>

00:18:10.158 --> 00:18:21.598
<v Nathan Carver>So each project inside it would have its own. It's almost like, is there a project level definition of what these components are? And then each component has a more fine grain detail of its interface.</v>

00:18:24.398 --> 00:18:33.678
<v Nathan Carver>Like, there's a project level definition for harness, for example, and then each harness in that project has a more granular interface definition.</v>

00:18:36.478 --> 00:18:38.078
<v Val Levitan>Sorry, one second, please. Hold on.</v>

00:21:39.358 --> 00:21:44.318
<v Val Levitan>I'm back again. Sorry about it. My lawyer on the line I had to pick up.</v>

00:21:45.238 --> 00:21:45.358
<v Nathan Carver>Yeah.</v>

00:21:48.638 --> 00:21:52.478
<v Val Levitan>Okay, so yes, we need we need some</v>

00:21:48.798 --> 00:21:48.838
<v Nathan Carver>Uhh...</v>

00:21:55.438 --> 00:21:56.798
<v Val Levitan>We need to think it through.</v>

00:22:00.878 --> 00:22:04.398
<v Val Levitan>I think I think the pivotal subject here is to.</v>

00:22:05.598 --> 00:22:07.598
<v Val Levitan>to be able to relay.</v>

00:22:08.758 --> 00:22:16.198
<v Val Levitan>project to repo and to ensure that repo could be described by data contract.</v>

00:22:09.758 --> 00:22:09.918
<v Nathan Carver>Mm.</v>

00:22:11.518 --> 00:22:11.638
<v Nathan Carver>Yes.</v>

00:22:19.438 --> 00:22:27.438
<v Nathan Carver>Right, because if the agent's going to assemble something, a bomb, it has a starting point, right? I'm assuming.</v>

00:22:28.518 --> 00:22:33.438
<v Nathan Carver>and I need to build this. So I need a harness, I need a monitor, I need...</v>

00:22:34.638 --> 00:22:37.838
<v Nathan Carver>So, it has to know when it when it needs a monitor.</v>

00:22:38.998 --> 00:22:46.878
<v Nathan Carver>where to go to get that. And so if there's a repo, a monitor repo that has a very brief.</v>

00:22:47.758 --> 00:22:52.398
<v Nathan Carver>These are display devices with a connector of X, Y, or Z.</v>

00:22:53.838 --> 00:22:54.158
<v Nathan Carver>Um...</v>

00:22:54.798 --> 00:23:14.878
<v Val Levitan>And the beauty about it is then when we build the linear chart of everything that goes inside, not chart, list, just flat list, flat linear list where everything is, then your display devices go by sizes, connectors, resolution,</v>

00:23:16.638 --> 00:23:23.278
<v Val Levitan>You know, whatever about the spec, but it's all within the provider's spec.</v>

00:23:23.918 --> 00:23:24.478
<v Nathan Carver>Correct.</v>

00:23:24.158 --> 00:23:25.918
<v Val Levitan>It's all in there.</v>

00:23:28.958 --> 00:23:30.678
<v Nathan Carver>Correct, so we could shoot.</v>

00:23:29.878 --> 00:23:33.438
<v Val Levitan>Which is which needs to be part of data contract.</v>

00:23:33.838 --> 00:23:43.598
<v Nathan Carver>Right. So it could choose a display based on whatever the definition of the product need is, and that could be size of the display, touchscreen, anything like that.</v>

00:23:44.238 --> 00:23:51.678
<v Val Levitan>Yes, yes. So you have, let's say, you have 27 inch display and you have a 43 inch display.</v>

00:23:45.358 --> 00:23:46.638
<v Nathan Carver>So, alright.</v>

00:23:53.518 --> 00:24:03.518
<v Val Levitan>But the machine that you're building is vertical, 43-inch screen machine. Well, you're not going to put a 27-inch screen in there.</v>

00:24:04.238 --> 00:24:05.278
<v Nathan Carver>Right, exactly.</v>

00:24:06.558 --> 00:24:10.798
<v Nathan Carver>So it would know its limitations and it can scan the repo for the appropriate.</v>

00:24:11.998 --> 00:24:14.718
<v Nathan Carver>are compatible specs.</v>

00:24:16.998 --> 00:24:17.358
<v Nathan Carver>Okay.</v>

00:24:17.998 --> 00:24:20.238
<v Val Levitan>And if it build the wrong machine.</v>

00:24:21.038 --> 00:24:25.118
<v Val Levitan>We go back to the data contract and the spec.</v>

00:24:26.238 --> 00:24:38.638
<v Val Levitan>If the spec is correct, then the data contract is not properly defined. And if data contract is properly defined and we have conflicting spec, maybe we should pay attention to it before the production starts.</v>

00:24:39.598 --> 00:24:55.678
<v Val Levitan>And if we happen to have two models of the same spec, well, I mean, are they identical? Are they interchangeable? Could we then say, take this or that, which is fine? You know, great for substitution.</v>

00:24:56.838 --> 00:25:03.758
<v Val Levitan>What does the data contract say? Would the data contract say you could take this or this or this, whatever you have in stock?</v>

00:25:05.598 --> 00:25:10.318
<v Val Levitan>But then maybe the mechanical constraints, maybe this one is thicker, thinner.</v>

00:25:11.678 --> 00:25:12.238
<v Val Levitan>You know?</v>

00:25:12.958 --> 00:25:13.358
<v Nathan Carver>Yeah.</v>

00:25:13.998 --> 00:25:15.198
<v Val Levitan>Different geometry.</v>

00:25:16.158 --> 00:25:18.078
<v Nathan Carver>So I think the repos would have...</v>

00:25:19.038 --> 00:25:27.518
<v Nathan Carver>So each repo would have like an overall spec describing what it has. And then not only that, but then.</v>

00:25:28.678 --> 00:25:34.478
<v Nathan Carver>The repo would also describe how to search for those things in its within its container.</v>

00:25:35.398 --> 00:25:38.078
<v Nathan Carver>So then each repo can optimize.</v>

00:25:38.958 --> 00:25:44.478
<v Nathan Carver>for how to search and find components within that repo.</v>

00:25:45.918 --> 00:25:51.438
<v Nathan Carver>So then that pushes you towards likewise, like components end up in the same repo.</v>

00:25:54.478 --> 00:26:01.038
<v Val Levitan>Well, that's why I'm saying displays is 1 repo. Harnesses is another repo.</v>

00:25:56.318 --> 00:25:56.718
<v Nathan Carver>Yeah.</v>

00:25:58.798 --> 00:25:59.398
<v Nathan Carver>Exactly.</v>

00:26:01.598 --> 00:26:14.478
<v Nathan Carver>So you would, yeah, and then the repos would describe, this is the optimized way to search for display specs. And then the harness repo would have different instructions for searching. That basically, I think what that gives us is</v>

00:26:15.758 --> 00:26:20.958
<v Nathan Carver>The repos can instruct the agent how best to search their data for compatible devices.</v>

00:26:22.918 --> 00:26:27.358
<v Nathan Carver>I think that's the advantage of a container repo like that too.</v>

00:26:28.558 --> 00:26:36.078
<v Nathan Carver>So I don't know how many you need. Maybe you don't need that many. I don't know the variation of the hardware, but</v>

00:26:35.518 --> 00:26:42.238
<v Val Levitan>But I don't feel, I don't feel that there is a huge issue with having more repos, like, so what?</v>

00:26:41.998 --> 00:26:42.398
<v Nathan Carver>No.</v>

00:26:43.478 --> 00:26:47.318
<v Nathan Carver>No, if the agents are managing them or searching through them, they'll know where to go.</v>

00:26:45.678 --> 00:26:47.118
<v Val Levitan>Yeah, yeah.</v>

00:26:48.158 --> 00:26:48.558
<v Val Levitan>Yeah.</v>

00:26:50.958 --> 00:26:57.358
<v Val Levitan>But the decision, the hinging decisions here, I think what we're making is that</v>

00:26:51.838 --> 00:26:51.998
<v Nathan Carver>No.</v>

00:26:58.638 --> 00:27:07.678
<v Val Levitan>We have a project which is equal to a repo. A repo has all the information that it needs, plus data contract, plus the pros.</v>

00:27:09.478 --> 00:27:09.958
<v Nathan Carver>Mhm.</v>

00:27:10.558 --> 00:27:15.198
<v Val Levitan>And the agents are the logical.</v>

00:27:16.318 --> 00:27:18.158
<v Val Levitan>Uh, executors.</v>

00:27:19.758 --> 00:27:35.118
<v Val Levitan>And they could execute in whichever, whatever you want to execute, but the execution comes from the agents. A human doesn't touch anything. A human only describes in words what is it that the human wants.</v>

00:27:38.078 --> 00:27:48.158
<v Val Levitan>And then it could push this information in whatever format, either to MSBC or maybe production files or maybe request for proposal.</v>

00:27:49.318 --> 00:27:50.398
<v Val Levitan>Whatever it is.</v>

00:27:51.758 --> 00:27:52.158
<v Nathan Carver>Okay.</v>

00:27:55.278 --> 00:28:01.278
<v Nathan Carver>OK, so from this flex play slim reverse reversal of engineering.</v>

00:28:03.598 --> 00:28:06.558
<v Nathan Carver>It should give us start to give us the idea of what that breakdown is.</v>

00:28:06.918 --> 00:28:23.758
<v Val Levitan>Yes, yes, that's our spike. I mean, if you say that it's too big for a spike, maybe we can take Flexport, which is also a good complete device, but with less items in it.</v>

00:28:11.038 --> 00:28:11.358
<v Nathan Carver>Yeah.</v>

00:28:24.398 --> 00:28:24.878
<v Nathan Carver>OK.</v>

00:28:26.038 --> 00:28:28.958
<v Nathan Carver>No, I think we can start with Flex Play Slim, and then...</v>

00:28:30.118 --> 00:28:33.118
<v Nathan Carver>We'll spike it out and see where we what we get, and then...</v>

00:28:35.038 --> 00:28:40.158
<v Nathan Carver>Take a second product, spike it out maybe independently and see how they align and what we came up with.</v>

00:28:42.558 --> 00:28:42.638
<v Nathan Carver>Um...</v>

00:28:45.518 --> 00:28:45.838
<v Nathan Carver>Okay.</v>

00:28:45.838 --> 00:28:53.838
<v Val Levitan>So, so the second product, if you want a smaller format, then take a flex port.</v>

00:28:51.678 --> 00:28:51.838
<v Nathan Carver>Mm.</v>

00:28:53.198 --> 00:28:53.318
<v Nathan Carver>Yeah.</v>

00:28:56.078 --> 00:29:08.638
<v Val Levitan>That's a smaller, much smaller items, much less items, but it also has it has plastics, it has sheet metal fabrication, it has screen, it has touch screen, it has hardware, it has connectors.</v>

00:29:09.358 --> 00:29:09.758
<v Nathan Carver>Okay.</v>

00:29:13.438 --> 00:29:16.798
<v Nathan Carver>Okay. And these all live right now.</v>

00:29:18.158 --> 00:29:21.278
<v Nathan Carver>In a repo, right? In the hardware manufacturing repo.</v>

00:29:21.598 --> 00:29:26.558
<v Val Levitan>Yeah, but I'm not sure that we need to pay attention to what exists today.</v>

00:29:28.158 --> 00:29:28.638
<v Nathan Carver>Okay.</v>

00:29:29.998 --> 00:29:30.958
<v Nathan Carver>So, what should be like?</v>

00:29:30.158 --> 00:29:39.038
<v Val Levitan>I, I would cut, I would kind of run a just just a freehand spike just to see where we'll end on this.</v>

00:29:40.198 --> 00:29:46.438
<v Val Levitan>I don't want to be bound to what's created, because I'm not sure that it will give us the right picture.</v>

00:29:48.558 --> 00:29:54.798
<v Nathan Carver>I see. So what would be like the source to use to reverse engineer? Is it?</v>

00:29:56.758 --> 00:30:02.398
<v Nathan Carver>Um, the design manual of the of the system itself, or like, what is a source that?</v>

00:30:03.038 --> 00:30:22.038
<v Val Levitan>We want to be, we want to, we want to reverse from the existing bill of material. So this is our point of reversal. We want to go into MSBC and grab that bill of material and flatten it out. And then pretend</v>

00:30:03.758 --> 00:30:05.678
<v Nathan Carver>We can look at everything.</v>

00:30:22.198 --> 00:30:25.518
<v Val Levitan>Pretend that this was not our starting point.</v>

00:30:27.318 --> 00:30:34.998
<v Val Levitan>And then whatever we do, however we choreograph everything, we need to end up with the bill of material.</v>

00:30:36.198 --> 00:30:36.758
<v Nathan Carver>Okay.</v>

00:30:36.198 --> 00:30:38.518
<v Val Levitan>But using using the agents.</v>

00:30:41.078 --> 00:30:45.438
<v Val Levitan>That's the entire spike. That's what we want to achieve.</v>

00:30:41.238 --> 00:30:41.718
<v Nathan Carver>Scott.</v>

00:30:46.278 --> 00:31:04.998
<v Val Levitan>So the moment you started with the bill of material and extracted the initial information, forget that we have that bill of material. It like never happened. Then you build the entire infrastructure, the architecture, then you push through the agents. You push</v>

00:31:05.798 --> 00:31:17.958
<v Val Levitan>the outcome already into MSBC in the form of a bill of material, you take that bill of material which you ended up with, compare it to the bill of material that you started with.</v>

00:31:19.078 --> 00:31:19.558
<v Nathan Carver>Right.</v>

00:31:19.118 --> 00:31:25.958
<v Val Levitan>And theoretically, they should be identical, but I suspect that through the agents, you'll come up with problems, something better.</v>

00:31:27.878 --> 00:31:28.358
<v Nathan Carver>Okay.</v>

00:31:28.878 --> 00:31:35.958
<v Val Levitan>Because I think the agents will find many issues that we are closing our blind eye on.</v>

00:31:31.398 --> 00:31:31.558
<v Nathan Carver>Yeah.</v>

00:31:37.238 --> 00:31:37.638
<v Nathan Carver>Right.</v>

00:31:39.158 --> 00:31:40.758
<v Nathan Carver>Okay, that makes sense to me.</v>

00:31:43.398 --> 00:31:45.798
<v Val Levitan>Okay, I'm going to send you this transcript.</v>

00:31:47.078 --> 00:31:51.558
<v Val Levitan>So you kind of have your objectives and your undertakings from it.</v>

00:31:52.998 --> 00:31:55.958
<v Val Levitan>Break it down into a new project, into...</v>

00:31:57.318 --> 00:31:57.798
<v Val Levitan>You know.</v>

00:31:58.638 --> 00:32:10.998
<v Val Levitan>I don't know how you're going to call it, architecture of ball or alignment between GitHub and MSBC, however you want to call it. Break it down into</v>

00:32:03.798 --> 00:32:04.398
<v Nathan Carver>Okay.</v>

00:32:13.158 --> 00:32:16.518
<v Val Levitan>capabilities and just start implementing it.</v>

00:32:17.398 --> 00:32:17.878
<v Nathan Carver>Okay.</v>

00:32:19.078 --> 00:32:22.918
<v Nathan Carver>No problem. Do you want me to put this under a specific spot, Jira?</v>

00:32:24.918 --> 00:32:28.198
<v Nathan Carver>A hardware sync is what we have already, so that would work.</v>

00:32:30.678 --> 00:32:31.158
<v Nathan Carver>Okay.</v>

00:32:33.598 --> 00:32:35.798
<v Val Levitan>Where do you have it? Show me.</v>

00:32:35.318 --> 00:32:37.558
<v Nathan Carver>So we have hardware sync is.</v>

00:32:39.278 --> 00:32:39.518
<v Val Levitan>Yeah.</v>

00:32:39.878 --> 00:32:41.558
<v Nathan Carver>DTP 1083.</v>

00:32:43.238 --> 00:32:44.758
<v Val Levitan>Is it under?</v>

00:32:45.238 --> 00:32:49.238
<v Nathan Carver>IP 964, modernization and improvements.</v>

00:32:58.118 --> 00:33:00.998
<v Val Levitan>Where is it under two months or core? What's the value stream?</v>

00:33:00.998 --> 00:33:04.118
<v Nathan Carver>Oh, DevOps tools and processes.</v>

00:33:24.518 --> 00:33:25.798
<v Val Levitan>Sorry, I don't see it.</v>

00:33:28.758 --> 00:33:30.438
<v Val Levitan>Can you share your screen, please?</v>

00:33:31.078 --> 00:33:32.758
<v Nathan Carver>Yeah, let me drop a link right here.</v>

00:33:57.238 --> 00:33:57.958
<v Val Levitan>Ohh, yes.</v>

00:34:03.878 --> 00:34:05.238
<v Val Levitan>Yeah, okay, let's do it there.</v>

00:34:05.798 --> 00:34:05.958
<v Nathan Carver>Yes.</v>

00:34:11.958 --> 00:34:13.078
<v Nathan Carver>Okay, sounds good.</v>

00:34:13.238 --> 00:34:21.638
<v Val Levitan>Well, actually, actually, you could also put it under Business Central application, which is IP 965.</v>

00:34:25.478 --> 00:34:26.358
<v Nathan Carver>Oh, okay.</v>

00:34:33.158 --> 00:34:35.238
<v Val Levitan>Either case is fine with me, okay?</v>

00:34:35.878 --> 00:34:36.278
<v Nathan Carver>Okay.</v>

00:34:40.278 --> 00:34:41.318
<v Nathan Carver>All right, that sounds good.</v>

00:34:40.598 --> 00:34:46.758
<v Val Levitan>So, I'm gonna send you the transcript, and then let you percolate on it, and...</v>

00:34:48.518 --> 00:34:51.878
<v Val Levitan>You said that you're taking a week off or a couple of weeks off?</v>

00:34:52.838 --> 00:34:59.558
<v Nathan Carver>Just one week next week, so I'll try to turn some of this some of this over this week, so you have it before I go.</v>

00:34:59.398 --> 00:35:03.478
<v Val Levitan>Okay. Okay, fantastic. Thank you very much. All the best to you.</v>

00:35:04.038 --> 00:35:04.918
<v Nathan Carver>All right, thanks, Val.</v>

