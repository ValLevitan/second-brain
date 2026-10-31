# Raw Transcript — Alignment - First Generated Contracts
**Date:** October 29, 2026, 2:02 PM – 2:28 PM Eastern
**Summary note:** [[Meeting_Notes_Hardware_Parts_Data_Contract_Generation_and_Persona_Repo-October-29-2026]]
---
WEBVTT

00:00:03.398 --> 00:00:06.838
<v Genadi Peari>You did the all the read me changes.</v>

00:00:08.038 --> 00:00:13.318
<v Nathan Carver>Yes, they look, yeah, they look good, so Igor.</v>

00:00:14.318 --> 00:00:14.998
<v Val Levitan>Hi, guys.</v>

00:00:17.158 --> 00:00:17.718
<v Genadi Peari>Hello.</v>

00:00:17.558 --> 00:00:17.718
<v Nathan Carver>Um...</v>

00:00:24.838 --> 00:00:30.918
<v Nathan Carver>OK, so I will, so I can show the contract generation work I did.</v>

00:00:32.638 --> 00:00:38.838
<v Val Levitan>Let's just, can you just explain the principles by which, what do you, what do you call contract?</v>

00:00:32.798 --> 00:00:32.918
<v Nathan Carver>Um...</v>

00:00:39.478 --> 00:00:42.358
<v Nathan Carver>Okay, let's do that.</v>

00:00:42.358 --> 00:00:44.998
<v Val Levitan>I just need to understand the general logic first.</v>

00:00:45.718 --> 00:00:52.358
<v Nathan Carver>Yep, so that we're still honestly still settling on terminology, but...</v>

00:00:53.438 --> 00:01:00.198
<v Nathan Carver>We have referred to a couple different, so there's source files, which are.</v>

00:01:01.638 --> 00:01:05.238
<v Nathan Carver>In this case, this compressed file that has...</v>

00:01:06.278 --> 00:01:09.798
<v Nathan Carver>diagrams, images, whatever it is that the vendor would give us.</v>

00:01:10.758 --> 00:01:12.918
<v Nathan Carver>To describe the component.</v>

00:01:13.958 --> 00:01:32.838
<v Val Levitan>Okay, so we get from a vendor, whatever he sends to us, data sheets, technical drawings, specifications, connector diagrams, PIN diagrams, whatever it is, we collect it, we put it into Github.</v>

00:01:33.638 --> 00:01:39.958
<v Val Levitan>And then we say what? Generate a contract or generate what?</v>

00:01:36.118 --> 00:01:36.598
<v Nathan Carver>Okay.</v>

00:01:37.558 --> 00:01:37.758
<v Nathan Carver>Yeah.</v>

00:01:40.358 --> 00:01:42.918
<v Nathan Carver>So the next human thing is to create this.</v>

00:01:43.998 --> 00:01:49.718
<v Nathan Carver>Simple item YAML file here, and all this is, let me enlarge it.</v>

00:01:52.038 --> 00:01:52.838
<v Nathan Carver>Is.</v>

00:01:55.558 --> 00:02:03.478
<v Nathan Carver>the item card, like the high level data for the item card in Msbc, but it also identifies, go ahead.</v>

00:02:00.598 --> 00:02:12.598
<v Val Levitan>But hold on a sec. You're pointing to an item number which says cabinet. That by itself, it's already an assembly. That's not a part.</v>

00:02:13.478 --> 00:02:14.678
<v Val Levitan>That's an assembly.</v>

00:02:14.918 --> 00:02:16.918
<v Genadi Peari>It's a part cabinet.</v>

00:02:16.438 --> 00:02:25.478
<v Val Levitan>Or it's a part, it's a main door, sorry, it's main door for Flex Pay, but that's this is something that you designed yourself.</v>

00:02:26.998 --> 00:02:27.478
<v Genadi Peari>This.</v>

00:02:27.958 --> 00:02:38.838
<v Val Levitan>That's not a vendor. Okay, got it. So it came out from SolidWorks. That's your drawings. You designed it. You put it in Github.</v>

00:02:40.198 --> 00:02:44.918
<v Val Levitan>And you did all the specifications yourself. We're not talking about third party now.</v>

00:02:46.118 --> 00:02:51.478
<v Nathan Carver>Correct. In this instance, it's a Jvl. Jvl is the vendor, and we can look at it that way.</v>

00:02:50.998 --> 00:02:53.318
<v Val Levitan>Okay, okay, okay, fair enough.</v>

00:02:54.038 --> 00:02:54.438
<v Nathan Carver>Yeah.</v>

00:02:54.278 --> 00:02:55.318
<v Genadi Peari>Same logics.</v>

00:02:58.118 --> 00:02:58.758
<v Nathan Carver>And.</v>

00:02:59.998 --> 00:03:01.158
<v Nathan Carver>So those are the two.</v>

00:03:02.278 --> 00:03:10.758
<v Nathan Carver>human stood, a new part, this would be the two human steps. Add all of your resource, your source files to the folder.</v>

00:03:11.718 --> 00:03:13.398
<v Nathan Carver>Create the item YAML file.</v>

00:03:14.558 --> 00:03:19.318
<v Nathan Carver>And then we can run the agent to generate the contract file.</v>

00:03:20.398 --> 00:03:24.278
<v Nathan Carver>And the agent will evaluate the source files, and...</v>

00:03:26.118 --> 00:03:30.118
<v Nathan Carver>This is the contract file that it can use to in the next.</v>

00:03:31.278 --> 00:03:37.078
<v Nathan Carver>Further downstream, build the BOM using this as a component within it.</v>

00:03:37.958 --> 00:03:55.678
<v Val Levitan>And how do you prompt, like, what do you say to the agent? So the agent has a source of truth. So you point it to Github and then it has, I guess, a persona. You define a persona, what it can do, I assume.</v>

00:03:55.878 --> 00:04:01.638
<v Nathan Carver>Correct. So it has instructions out here for...</v>

00:04:03.158 --> 00:04:17.158
<v Nathan Carver>This repository is self-instructing on how to read it, on how to find the information. And this is what allows the agent to build out the contract. So for example,</v>

00:04:16.678 --> 00:04:17.238
<v Val Levitan>Okay.</v>

00:04:19.478 --> 00:04:25.518
<v Nathan Carver>So you can even use agents to, you know, add the source files and create the YAML, the item YAML.</v>

00:04:26.518 --> 00:04:29.878
<v Nathan Carver>because the agent also has the instructions on how to use the folders.</v>

00:04:31.518 --> 00:04:32.998
<v Nathan Carver>where the source files go.</v>

00:04:34.758 --> 00:04:38.358
<v Nathan Carver>And then maintaining the README file for these.</v>

00:04:39.958 --> 00:04:41.798
<v Nathan Carver>Writing the AMOT file, and then...</v>

00:04:42.838 --> 00:04:49.638
<v Nathan Carver>There's the human interaction is going to be, is all of this looking correct?</v>

00:04:50.478 --> 00:04:55.318
<v Nathan Carver>And then once it is, the agent can then be asked, we can then go on to generating the contract.</v>

00:04:56.878 --> 00:05:08.038
<v Nathan Carver>But that gets all of our, once our source is structured and consistent within that structure, generating contracts will be consistent.</v>

00:05:10.838 --> 00:05:13.798
<v Val Levitan>So, Genadi, do you understand this?</v>

00:05:14.118 --> 00:05:14.238
<v Nathan Carver>Yes.</v>

00:05:14.118 --> 00:05:29.078
<v Genadi Peari>Of course. We spent actually three days for generating the right structure because it was an inconsistency every time. And I think we just yesterday came to the understanding, full understanding, right, Nathan?</v>

00:05:29.398 --> 00:05:30.598
<v Nathan Carver>Yeah, I agree.</v>

00:05:32.518 --> 00:05:45.078
<v Val Levitan>So, so Genadi and and Nathan, I guess correct me if I'm wrong, but conversely, I'm explaining in my own words how I understand things will be.</v>

00:05:46.198 --> 00:05:49.198
<v Val Levitan>So, an agent, in effect, is a persona.</v>

00:05:50.918 --> 00:05:52.038
<v Val Levitan>And.</v>

00:05:53.198 --> 00:05:57.078
<v Val Levitan>This persona, we give this persona just like to a human.</v>

00:05:57.678 --> 00:05:58.198
<v Nathan Carver>Mhm.</v>

00:05:58.678 --> 00:06:06.198
<v Val Levitan>its source of truth and we say, hey, agent, persona agent, this is your source of truth.</v>

00:06:07.398 --> 00:06:26.838
<v Val Levitan>Then we define a personality to it. You act like this. That's how you behave. That's what you look at. And then we tell this persona we want from you to use your logic, use the knowledge base here, use the logic.</v>

00:06:27.078 --> 00:06:27.638
<v Val Levitan>Off.</v>

00:06:28.838 --> 00:06:31.238
<v Val Levitan>Creating a bill of material.</v>

00:06:32.358 --> 00:06:32.838
<v Nathan Carver>Correct.</v>

00:06:32.598 --> 00:06:51.158
<v Val Levitan>So, and do we have only one agent or do we have multiple personalities? Because we want the agent to learn from the mistakes. And in order for the agent to learn from the mistakes, the way I understand that, I'm not teaching you, I'm simply talking out my own.</v>

00:06:51.278 --> 00:06:54.998
<v Val Levitan>understanding in order for this agent.</v>

00:06:56.038 --> 00:06:56.998
<v Val Levitan>To uh...</v>

00:06:58.198 --> 00:07:04.198
<v Val Levitan>act a certain way, we wanted to learn from the mistakes. So we need to have an auditor of some sort.</v>

00:07:05.718 --> 00:07:06.278
<v Nathan Carver>Correct.</v>

00:07:06.678 --> 00:07:18.838
<v Val Levitan>We need another agent who says, who looks at the truth and says, hey, dude, you're screwing up here. You made a mistake. It doesn't work this way. I want you to learn from this process.</v>

00:07:21.718 --> 00:07:24.358
<v Nathan Carver>So, correct. So we have to have.</v>

00:07:25.798 --> 00:07:37.238
<v Nathan Carver>There has to be verification of the output, and that is we can use another agent to verify the work. And there's also, you know, human review when they're</v>

00:07:39.118 --> 00:07:45.878
<v Nathan Carver>Whenever the humans are interacting with the final output, they may see problems. And that also has to go back into...</v>

00:07:44.038 --> 00:07:44.158
<v Val Levitan>Yeah.</v>

00:07:47.158 --> 00:08:01.638
<v Nathan Carver>the agent for correcting the problem. In our, in this structure, the way that our learning would be refining the instructions and the scripts that do the work.</v>

00:08:02.918 --> 00:08:09.398
<v Nathan Carver>So that's what we can tune. That would effectively be the learning process for our agents.</v>

00:08:12.078 --> 00:08:12.278
<v Nathan Carver>Um...</v>

00:08:13.558 --> 00:08:18.758
<v Nathan Carver>And so part of that learning process here is what we were going through is...</v>

00:08:22.438 --> 00:08:24.278
<v Nathan Carver>Taking a stab at how these.</v>

00:08:25.838 --> 00:08:38.998
<v Nathan Carver>how these folders are going to play out and realizing that they're not all the same. Not every folder we have at the root component level is going to fall into the same structural pattern.</v>

00:08:40.278 --> 00:08:52.518
<v Nathan Carver>So part of that learning has just been restructuring these folders to follow a better pattern so that we can, I'm just going through here, you can see how we've</v>

00:08:54.358 --> 00:08:58.918
<v Nathan Carver>restructured the path. I think from what the standard kind of laid out a default pattern.</v>

00:09:00.198 --> 00:09:07.798
<v Nathan Carver>And we're iterating on that pattern and coming up with a with one that makes sense for each group of components that we have.</v>

00:09:08.998 --> 00:09:14.198
<v Nathan Carver>So that's part of our learning too. That's the human interaction and then us going back and refining.</v>

00:09:15.158 --> 00:09:17.078
<v Nathan Carver>the structure of the project.</v>

00:09:18.758 --> 00:09:24.198
<v Nathan Carver>So then, now that I've shown that I can generate contracts, the next thing is to...</v>

00:09:25.638 --> 00:09:32.758
<v Nathan Carver>make sure the instructions can regenerate that contract with different agents, they regenerate the same contract consistently.</v>

00:09:33.838 --> 00:09:35.638
<v Nathan Carver>If we're consistent, then...</v>

00:09:36.838 --> 00:09:38.918
<v Nathan Carver>We can find 2 mistakes as they come up.</v>

00:09:43.478 --> 00:09:47.718
<v Nathan Carver>So that's, in a nutshell, that's our progress we've made.</v>

00:09:49.398 --> 00:09:59.478
<v Nathan Carver>Nothing surprises me that we can generate these contracts and build a BOM. I think the good part here is that the structure is better. The contract we produced is better than</v>

00:10:00.758 --> 00:10:08.438
<v Nathan Carver>The previous spike that I that I had done, now that that Genadi has his his structure in place, so...</v>

00:10:10.358 --> 00:10:17.318
<v Nathan Carver>That's in a nutshell, that's where we are right now. So the next step is to, Genadi has his structure in there. I'm going to merge in my.</v>

00:10:18.478 --> 00:10:21.958
<v Nathan Carver>contract generation stuff with his new structure.</v>

00:10:23.198 --> 00:10:27.478
<v Nathan Carver>And we're just going to continue to refine it as the next step.</v>

00:10:29.318 --> 00:10:38.438
<v Nathan Carver>So I think we're close to regenerating a BOM. And then the final step, obviously, is pushing. This is going to be syncing this information with Msbc.</v>

00:10:40.838 --> 00:10:46.758
<v Val Levitan>So, Msbc will say, okay, here is the...</v>

00:10:48.118 --> 00:10:52.438
<v Val Levitan>Set of stand-alone parts were they manufactured by us, or...</v>

00:10:53.478 --> 00:10:55.398
<v Val Levitan>supplied by a third party.</v>

00:10:56.758 --> 00:11:00.758
<v Val Levitan>Here's all the technical specification that is required.</v>

00:11:01.718 --> 00:11:04.918
<v Val Levitan>And, obviously, because it lives in Github, it...</v>

00:11:03.718 --> 00:11:03.798
<v Nathan Carver>Pay.</v>

00:11:06.198 --> 00:11:06.838
<v Val Levitan>Ohh.</v>

00:11:08.638 --> 00:11:10.598
<v Val Levitan>When it's reiterated.</v>

00:11:11.798 --> 00:11:16.198
<v Val Levitan>The new part is substituted easily, so we have version controls.</v>

00:11:21.398 --> 00:11:25.238
<v Val Levitan>So it pushes that technical information into.</v>

00:11:26.518 --> 00:11:28.038
<v Val Levitan>Msbc, but.</v>

00:11:29.878 --> 00:11:33.078
<v Val Levitan>It needs a second push for the same vendor.</v>

00:11:35.638 --> 00:11:38.358
<v Val Levitan>Of all the administrational data.</v>

00:11:41.518 --> 00:11:44.838
<v Val Levitan>which is not a Github related. We don't want it in Github.</v>

00:11:46.358 --> 00:11:46.678
<v Nathan Carver>Ahh.</v>

00:11:48.038 --> 00:11:48.518
<v Nathan Carver>Okay.</v>

00:11:53.398 --> 00:11:59.558
<v Nathan Carver>Do you know where you want to put that currently or where is it stored? Or is it only an Msbc now at the moment?</v>

00:12:00.998 --> 00:12:01.718
<v Val Levitan>So...</v>

00:12:00.998 --> 00:12:02.918
<v Genadi Peari>At the at the moment, yes.</v>

00:12:03.638 --> 00:12:11.318
<v Val Levitan>So right now it's in Msbc. I don't know whether we should change it or not, but today it lives in Msbc.</v>

00:12:12.518 --> 00:12:12.998
<v Nathan Carver>Okay.</v>

00:12:13.558 --> 00:12:19.638
<v Val Levitan>And that's accessible by the administrational way of the company, not by engineering.</v>

00:12:21.958 --> 00:12:24.278
<v Val Levitan>And, and not by procurement people.</v>

00:12:25.478 --> 00:12:25.958
<v Nathan Carver>Okay.</v>

00:12:32.038 --> 00:12:33.718
<v Val Levitan>And we want to have a division.</v>

00:12:35.238 --> 00:12:36.998
<v Val Levitan>Of of power.</v>

00:12:41.478 --> 00:12:42.838
<v Nathan Carver>Okay, so it's...</v>

00:12:43.798 --> 00:12:46.678
<v Nathan Carver>As far as using this tool, this is something that...</v>

00:12:48.358 --> 00:12:54.278
<v Nathan Carver>Individuals will use the agent with on their local machine and have it.</v>

00:12:55.438 --> 00:12:58.998
<v Nathan Carver>Let's say Genadi, for example, adds a new item.</v>

00:13:00.838 --> 00:13:06.118
<v Nathan Carver>puts the source files into the folder structure, then asks the agent to generate the document.</v>

00:13:03.798 --> 00:13:05.798
<v Val Levitan>Well, well, what?</v>

00:13:06.598 --> 00:13:10.038
<v Val Levitan>I, I don't, I don't know whether it's used on the local machine.</v>

00:13:11.638 --> 00:13:12.038
<v Nathan Carver>Okay.</v>

00:13:12.758 --> 00:13:15.318
<v Val Levitan>Why do you say it's used on the lock-in machine?</v>

00:13:18.598 --> 00:13:27.798
<v Nathan Carver>That's my question. I'm asking, what is your vision? Is that what you're envisioning? Or is there another cloud tool that we're going to be using?</v>

00:13:30.198 --> 00:13:35.558
<v Nathan Carver>Because I know Jvl is using Claude locally extensively, but I don't know what cloud.</v>

00:13:38.438 --> 00:13:46.038
<v Nathan Carver>Agent tools you have, you might have running. I don't know if you're using Claude in the cloud or Copilot or Rock, for example.</v>

00:13:45.878 --> 00:13:52.038
<v Val Levitan>Well, no, I mean we use Claude Code. Yes, Claude Code is a local.</v>

00:13:53.798 --> 00:13:55.918
<v Val Levitan>Bound? Yes, I understand that.</v>

00:13:56.918 --> 00:13:57.318
<v Nathan Carver>Right.</v>

00:13:57.478 --> 00:14:06.918
<v Val Levitan>But although it lives locally, the reference, the source of truth is the Github.</v>

00:14:07.718 --> 00:14:08.358
<v Nathan Carver>Correct.</v>

00:14:09.158 --> 00:14:10.038
<v Val Levitan>So...</v>

00:14:09.438 --> 00:14:14.518
<v Nathan Carver>So it's just a local instance, but they all use the same set of instructions, same source of truth.</v>

00:14:14.038 --> 00:14:32.358
<v Val Levitan>Yeah, so I mean, we could use Grok or we could use any cloud services pointed to the same Github repository and ask an outside agent to do exactly the same work as the local.</v>

00:14:32.598 --> 00:14:34.038
<v Val Levitan>Claude code would do.</v>

00:14:36.518 --> 00:14:36.998
<v Nathan Carver>Correct.</v>

00:14:36.678 --> 00:14:43.158
<v Val Levitan>So I don't, I don't, I don't see why we need to be married to, you know.</v>

00:14:44.598 --> 00:14:46.278
<v Val Levitan>Just to a single.</v>

00:14:47.398 --> 00:14:48.278
<v Val Levitan>Ai model.</v>

00:14:50.598 --> 00:14:52.278
<v Nathan Carver>No, no, we're not.</v>

00:14:54.198 --> 00:14:55.478
<v Nathan Carver>We're not, in fact.</v>

00:14:55.238 --> 00:15:03.078
<v Val Levitan>So, where do these, where does the persona live? Because we have a persona.</v>

00:14:56.918 --> 00:14:58.358
<v Nathan Carver>This is set up here.</v>

00:15:04.278 --> 00:15:06.438
<v Val Levitan>We have repository for personas.</v>

00:15:07.718 --> 00:15:11.398
<v Nathan Carver>Oh, okay. I didn't know that. So right now...</v>

00:15:13.958 --> 00:15:17.478
<v Nathan Carver>This is it. This file here defines.</v>

00:15:20.278 --> 00:15:21.958
<v Nathan Carver>what this agent needs to do.</v>

00:15:23.158 --> 00:15:26.998
<v Nathan Carver>And so this needs to be refined, but if we have...</v>

00:15:28.198 --> 00:15:30.278
<v Nathan Carver>If you have a persona repo, then...</v>

00:15:31.318 --> 00:15:35.238
<v Nathan Carver>It needs to know about that. So these instructions need to be updated so it knows.</v>

00:15:36.358 --> 00:15:36.918
<v Nathan Carver>About that.</v>

00:15:36.438 --> 00:15:44.358
<v Val Levitan>Yes, yes, so we have a persona repo, and if you get together with Andrei Bosik.</v>

00:15:40.598 --> 00:15:41.078
<v Nathan Carver>Okay.</v>

00:15:47.078 --> 00:15:48.518
<v Val Levitan>Then he'll.</v>

00:15:49.678 --> 00:16:01.238
<v Val Levitan>tell you what it is. For example, he is working on AI Project Manager, right? And so that persona is alive in a, you know.</v>

00:16:02.518 --> 00:16:06.118
<v Val Levitan>In a persona file, we have a CO.</v>

00:16:07.078 --> 00:16:10.838
<v Val Levitan>And you know, there is a persona there. We have a Cfo.</v>

00:16:12.278 --> 00:16:17.438
<v Val Levitan>So, all of the persona lives in a persona files repository.</v>

00:16:18.918 --> 00:16:19.878
<v Nathan Carver>Okay, got it.</v>

00:16:25.518 --> 00:16:27.238
<v Nathan Carver>OK, that makes sense to me.</v>

00:16:30.998 --> 00:16:33.478
<v Nathan Carver>All right, so some of the next steps then.</v>

00:16:34.758 --> 00:16:44.598
<v Nathan Carver>refine these instructions, repeat the generate, be able to generate A consistent contract from the same source files.</v>

00:16:45.638 --> 00:16:52.598
<v Nathan Carver>and incorporate the personas instructions from Andre's from Andre's work.</v>

00:16:54.678 --> 00:16:56.598
<v Val Levitan>So I see many, many...</v>

00:16:54.798 --> 00:16:57.318
<v Nathan Carver>And then you find what the transformer will be.</v>

00:16:58.198 --> 00:17:00.998
<v Val Levitan>My apologies, I interrupted. Can you say it again?</v>

00:17:01.878 --> 00:17:12.918
<v Nathan Carver>I think, and we may still have to define what this persona is. We have instructions so far, and some will stay in here and then some will get moved into the persona repo, I'm assuming.</v>

00:17:14.998 --> 00:17:18.758
<v Val Levitan>Right. Yes, it needs to move to a persona, Req.</v>

00:17:19.718 --> 00:17:20.198
<v Nathan Carver>Okay.</v>

00:17:21.638 --> 00:17:29.958
<v Val Levitan>So I see a number of applications building on top of it. Well, not applications, but functions or.</v>

00:17:33.718 --> 00:17:42.918
<v Val Levitan>Yeah, I guess applications to how we apply this knowledge. So, for example, we have a sub-assembly that houses a...</v>

00:17:47.838 --> 00:17:49.238
<v Val Levitan>I don't know, a monitor.</v>

00:17:50.118 --> 00:17:51.078
<v Val Levitan>For the sake of...</v>

00:17:53.478 --> 00:18:00.678
<v Val Levitan>sake of conversation. And we want a replacement monitor that mounts in the same dimensions.</v>

00:17:55.238 --> 00:17:55.878
<v Nathan Carver>Mhm.</v>

00:18:04.278 --> 00:18:05.958
<v Val Levitan>So, we can...</v>

00:18:08.278 --> 00:18:09.878
<v Val Levitan>Send RFQ.</v>

00:18:11.318 --> 00:18:14.598
<v Val Levitan>to a potential list of monitor suppliers.</v>

00:18:15.798 --> 00:18:19.718
<v Val Levitan>And we can ask the agent to yank.</v>

00:18:22.438 --> 00:18:23.798
<v Val Levitan>the dimensions.</v>

00:18:24.878 --> 00:18:29.158
<v Val Levitan>out of the Github and include it in with our rq.</v>

00:18:27.438 --> 00:18:27.558
<v Nathan Carver>Yeah.</v>

00:18:33.238 --> 00:18:33.718
<v Nathan Carver>Okay.</v>

00:18:34.118 --> 00:18:37.398
<v Val Levitan>together with all other data sheets for the monitor.</v>

00:18:40.678 --> 00:18:58.838
<v Genadi Peari>We'll need to be able to expand these descriptions as per to study how to expand it. For example, monitor at the beginning is dimension, then it's brightness, then we have the interface, the LEDs, that amount of</v>

00:19:00.118 --> 00:19:02.758
<v Genadi Peari>LED backlight and so on and so on.</v>

00:19:04.038 --> 00:19:12.518
<v Val Levitan>Well, all of it needs to be contained in the in the data sheet, no, in the data sheet that we initially put into Github.</v>

00:19:06.998 --> 00:19:07.798
<v Genadi Peari>In the contract.</v>

00:19:14.918 --> 00:19:16.398
<v Val Levitan>Before the data contract.</v>

00:19:16.918 --> 00:19:17.478
<v Genadi Peari>Yes.</v>

00:19:20.518 --> 00:19:40.118
<v Val Levitan>I don't know, screws are the same way. I mean, if we make a thread a certain, you know, metric or imperial dimension, the certain depth, the certain radius, the thread, et cetera, we should be able to quickly get this information.</v>

00:19:43.718 --> 00:19:53.718
<v Val Levitan>And if we don't have this information, we should not be able to form a complete bomb. It should collapse. That's our checkpoint.</v>

00:20:06.358 --> 00:20:19.878
<v Genadi Peari>I'm sorry, to complete the structure, I need to be able to pull all the hundreds of parts into the Github from Msbc. I don't have an access.</v>

00:20:20.958 --> 00:20:23.318
<v Genadi Peari>Because I, manually, I cannot do this.</v>

00:20:21.318 --> 00:20:21.878
<v Val Levitan>You will help.</v>

00:20:23.478 --> 00:20:26.438
<v Nathan Carver>He needs a he needs an ID, a client ID.</v>

00:20:27.958 --> 00:20:30.678
<v Nathan Carver>and to access Msbc.</v>

00:20:32.038 --> 00:20:33.078
<v Val Levitan>Oh, I'm sorry.</v>

00:20:34.278 --> 00:20:34.598
<v Val Levitan>What?</v>

00:21:06.038 --> 00:21:09.478
<v Val Levitan>Uh, Nathan, uh, tell me what what he needs: ID.</v>

00:21:12.118 --> 00:21:17.718
<v Nathan Carver>So yeah, the client ID so he can use, so he can access Msbc.</v>

00:21:18.998 --> 00:21:21.198
<v Nathan Carver>And do you want to use the same Msbc?</v>

00:21:19.518 --> 00:21:22.278
<v Val Levitan>Client, client ID, and what else?</v>

00:21:23.398 --> 00:21:32.038
<v Nathan Carver>Oh, that's it. He needs a client ID for Msbc. So it's the same thing we did for the MCP server.</v>

00:21:49.958 --> 00:21:50.118
<v Nathan Carver>Yeah.</v>

00:22:00.918 --> 00:22:05.078
<v Val Levitan>Okay, what's our next milestone and when can we attend to it?</v>

00:22:07.638 --> 00:22:09.958
<v Nathan Carver>So, the next milestone is...</v>

00:22:11.518 --> 00:22:16.278
<v Nathan Carver>Let's see, I want to reach out to Andrei and hook into the persona repo.</v>

00:22:17.638 --> 00:22:21.238
<v Nathan Carver>refine the instructions, generate consistent contracts.</v>

00:22:23.158 --> 00:22:26.478
<v Nathan Carver>I think that's kind of that's on my side, and I think...</v>

00:22:27.798 --> 00:22:36.198
<v Nathan Carver>for Genadi is just getting access to Msbc so he can finish the folder structure and getting all the source files in there.</v>

00:22:40.278 --> 00:22:43.638
<v Nathan Carver>And I think Andrei may have to provide that client ID.</v>

00:22:44.278 --> 00:22:57.958
<v Genadi Peari>We agreed on the part on the not on the assembly which you wanted to try to generate. First of all, I need to accomplish all this assembly, this all the structure.</v>

00:22:56.198 --> 00:22:56.358
<v Nathan Carver>Yes.</v>

00:22:59.558 --> 00:23:02.358
<v Genadi Peari>And it's about like 100 files.</v>

00:23:03.798 --> 00:23:09.478
<v Genadi Peari>Because Claude said you says it it was a small one that we picked previously.</v>

00:23:12.638 --> 00:23:14.198
<v Nathan Carver>Correct, yeah, which was a small one.</v>

00:23:17.038 --> 00:23:20.638
<v Val Levitan>I want to point the CO persona.</v>

00:23:21.958 --> 00:23:23.958
<v Val Levitan>to the same repository.</v>

00:23:27.958 --> 00:23:30.118
<v Val Levitan>I have a I CO.</v>

00:23:31.278 --> 00:23:35.158
<v Val Levitan>whose responsibility is to look after purchasing and manufacturing.</v>

00:23:43.718 --> 00:23:47.878
<v Val Levitan>Can you send me the link to the repo that you're working in?</v>

00:23:48.758 --> 00:23:49.478
<v Nathan Carver>Yes.</v>

00:24:06.758 --> 00:24:06.998
<v Val Levitan>Bep.</v>

00:24:08.198 --> 00:24:09.798
<v Val Levitan>Got it. Thank you very much.</v>

00:24:11.478 --> 00:24:17.558
<v Val Levitan>That's it for me, guys. I just need to know when can we re-attend to the next step.</v>

00:24:18.758 --> 00:24:19.878
<v Val Levitan>How much time do you need?</v>

00:24:21.238 --> 00:24:23.078
<v Val Levitan>Can we do it on Monday afternoon?</v>

00:24:29.958 --> 00:24:30.838
<v Nathan Carver>Look at my schedule.</v>

00:24:36.118 --> 00:24:43.798
<v Val Levitan>Genadi, how much more do you need to, how much more information do you need to put into the repos?</v>

00:24:46.038 --> 00:24:46.838
<v Val Levitan>A lot, a lot.</v>

00:24:47.478 --> 00:24:55.958
<v Genadi Peari>Yeah, it's two things. The all I need to accomplish all the...</v>

00:24:56.918 --> 00:25:00.998
<v Genadi Peari>Jvl vendor parts ever since we completed.</v>

00:24:59.598 --> 00:25:00.238
<v Val Levitan>Mmh.</v>

00:25:02.158 --> 00:25:14.438
<v Genadi Peari>And once I get the client ID, I can pull the Msbc standard parts in the Github. So I need these two steps. The both are.</v>

00:25:15.718 --> 00:25:20.358
<v Genadi Peari>Probably the second is easier, soon I'll know how to do it.</v>

00:25:21.718 --> 00:25:24.278
<v Genadi Peari>Nathan, will you help me how to?</v>

00:25:24.118 --> 00:25:24.438
<v Nathan Carver>Yeah.</v>

00:25:25.798 --> 00:25:30.918
<v Genadi Peari>Because we need carefully category by category to pull all this information.</v>

00:25:27.238 --> 00:25:27.398
<v Nathan Carver>Yeah.</v>

00:25:34.998 --> 00:25:36.438
<v Nathan Carver>Yeah, I can help with that.</v>

00:25:40.038 --> 00:25:40.758
<v Genadi Peari>Bom.</v>

00:25:41.398 --> 00:25:45.958
<v Val Levitan>Okay, so then let's do it on Wednesday, Wednesday afternoon.</v>

00:25:49.478 --> 00:25:49.958
<v Nathan Carver>Okay.</v>

00:25:50.758 --> 00:25:51.478
<v Val Levitan>Is that OK?</v>

00:25:52.278 --> 00:25:53.558
<v Nathan Carver>Yeah, yeah.</v>

00:25:52.998 --> 00:26:01.638
<v Val Levitan>I'll set up a meeting for 2 P.m. Eastern Time on Wednesday. I'll book it for half an hour. We should have enough time.</v>

00:26:04.198 --> 00:26:05.838
<v Nathan Carver>Okay, that works.</v>

00:26:05.238 --> 00:26:06.438
<v Val Levitan>Thank you very much, guys.</v>

00:26:07.558 --> 00:26:08.038
<v Genadi Peari>Thank you.</v>

00:26:08.438 --> 00:26:09.878
<v Nathan Carver>All right. Thanks, all.</v>

00:26:08.678 --> 00:26:08.918
<v Val Levitan>Bye.</v>

00:26:11.398 --> 00:26:12.038
<v Genadi Peari>Nathan.</v>

