# Raw Transcript — AI-logic for assembling BOM
**Date:** November 16, 2026, 4:40 PM – 5:02 PM Eastern
**Summary note:** [[Meeting_Notes_Nathan_Unguided_BOM_Spike_from_Data_Contracts-November-16-2026]]
---
WEBVTT

00:00:03.795 --> 00:00:05.075
<v Val Levitan>I'm doing well, and you?</v>

00:00:06.115 --> 00:00:07.075
<v Nathan Carver>Doing pretty good.</v>

00:00:09.555 --> 00:00:10.275
<v Val Levitan>So...</v>

00:00:09.635 --> 00:00:10.195
<v Nathan Carver>We are.</v>

00:00:11.875 --> 00:00:12.275
<v Nathan Carver>Go ahead.</v>

00:00:13.235 --> 00:00:14.995
<v Val Levitan>There's an echo behind you.</v>

00:00:16.275 --> 00:00:20.835
<v Nathan Carver>Yeah, I might temporarily on my laptop speakers, so I don't know how bad it is.</v>

00:00:23.475 --> 00:00:25.475
<v Val Levitan>Well, as long as there is no, I'm fine.</v>

00:00:28.795 --> 00:00:28.995
<v Nathan Carver>Sorry.</v>

00:00:37.715 --> 00:00:40.275
<v Nathan Carver>I'm in the process if I can improve it.</v>

00:00:44.955 --> 00:00:45.675
<v Nathan Carver>Let's see here.</v>

00:00:52.675 --> 00:00:54.115
<v Nathan Carver>Alright, how's that?</v>

00:00:55.715 --> 00:00:57.475
<v Val Levitan>Yeah, I think it's good.</v>

00:00:58.555 --> 00:00:59.395
<v Nathan Carver>It's good, OK.</v>

00:00:58.675 --> 00:00:59.635
<v Val Levitan>One second, please.</v>

00:01:25.235 --> 00:01:26.275
<v Val Levitan>Okay, so.</v>

00:01:31.075 --> 00:01:32.595
<v Val Levitan>I just spoke to Genadi.</v>

00:01:33.195 --> 00:01:33.635
<v Nathan Carver>Yeah.</v>

00:01:35.395 --> 00:01:36.035
<v Val Levitan>And.</v>

00:01:41.715 --> 00:01:42.835
<v Val Levitan>I'm having</v>

00:01:49.155 --> 00:01:49.715
<v Val Levitan>Seconds.</v>

00:02:09.315 --> 00:02:09.715
<v Val Levitan>And.</v>

00:02:11.635 --> 00:02:13.875
<v Val Levitan>I'm trying to understand. Center.</v>

00:02:15.435 --> 00:02:18.275
<v Val Levitan>Whether you manage to.</v>

00:02:20.835 --> 00:02:23.395
<v Val Levitan>Figure out a logic.</v>

00:02:25.475 --> 00:02:34.835
<v Val Levitan>how we can assemble a bill of material from data sheets, from data contracts.</v>

00:02:38.355 --> 00:02:41.395
<v Nathan Carver>So we have logic to do that.</v>

00:02:42.675 --> 00:02:47.235
<v Nathan Carver>My what I'm working on now, or will be starting on, is...</v>

00:02:48.675 --> 00:02:51.235
<v Nathan Carver>the structure of the bomb in GitHub.</v>

00:02:52.275 --> 00:02:52.995
<v Nathan Carver>And then...</v>

00:02:54.355 --> 00:02:57.715
<v Nathan Carver>Running that process on contracts to.</v>

00:02:59.075 --> 00:02:59.755
<v Nathan Carver>And.</v>

00:03:00.755 --> 00:03:02.675
<v Nathan Carver>Generator structure or I?</v>

00:03:05.075 --> 00:03:14.035
<v Nathan Carver>However we get to that structure, we need to have it in GitHub, and then we have the capability to synchronize that up to MSPC.</v>

00:03:15.075 --> 00:03:34.115
<v Val Levitan>No, but I'm not worried about getting data from GitHub to MSPC. I'm not worried about putting data into GitHub. I'm not worried about it. Let's say we have data sheets in GitHub and we have a list of all parts that would flat list of.</v>

00:03:21.395 --> 00:03:21.875
<v Nathan Carver>Mhm.</v>

00:03:34.155 --> 00:03:37.955
<v Val Levitan>Parts that will comprise.</v>

00:03:40.275 --> 00:03:41.555
<v Val Levitan>Of the bill of material.</v>

00:03:42.195 --> 00:03:42.515
<v Nathan Carver>Yup.</v>

00:03:42.435 --> 00:03:51.155
<v Val Levitan>But how do you, how does, let's say, one bracket knows that it needs to fit into another bracket and...</v>

00:03:52.035 --> 00:03:55.555
<v Val Levitan>Mount a PC board on top of these two brackets.</v>

00:03:56.515 --> 00:03:58.195
<v Val Levitan>What's the logic behind that?</v>

00:03:58.995 --> 00:04:08.915
<v Val Levitan>How would how would AI know that using these data contracts, because these parts are manufactured a certain way?</v>

00:04:10.435 --> 00:04:21.955
<v Val Levitan>How would it know that from these three parts you assemble an enclosure with the PC board inside of it? Without telling this, without explicitly telling it,</v>

00:04:23.395 --> 00:04:25.235
<v Val Levitan>of what goes where.</v>

00:04:27.155 --> 00:04:35.315
<v Nathan Carver>Right. So the idea is, for example, to put a board into a housing or a case.</v>

00:04:37.315 --> 00:04:40.355
<v Nathan Carver>To attach it, you know, whatever 4 screws.</v>

00:04:41.475 --> 00:04:50.115
<v Nathan Carver>Those that that becomes the interface, so the contracts have to indicate that a specific screw is needed.</v>

00:04:51.395 --> 00:04:53.075
<v Nathan Carver>To mount the board.</v>

00:04:53.795 --> 00:05:13.955
<v Val Levitan>Well, you actually don't need the specific screw to mount the board, because if there are studs and they have a certain metric thread and you have screw of the same dimension, which is the height, it needs to match the height of the stud, it needs to have the metric thread.</v>

00:04:54.195 --> 00:04:54.835
<v Nathan Carver>And then...</v>

00:05:02.995 --> 00:05:03.515
<v Nathan Carver>Correct.</v>

00:05:12.035 --> 00:05:12.515
<v Nathan Carver>That's it.</v>

00:05:14.355 --> 00:05:16.355
<v Val Levitan>Then, the other screw will not fit.</v>

00:05:17.795 --> 00:05:31.315
<v Nathan Carver>Correct. So you have to have, so the screws, so for example, in the screws, we've identified their size and their dimensions and what they're going to fit. So the board's going to have to identify, this is what I take.</v>

00:05:32.675 --> 00:05:46.115
<v Nathan Carver>And then when it comes to mounting a board, I'm assuming most boards are going to be generic, but they're going to have to fit whatever the mounting standard is that that case is using.</v>

00:05:45.635 --> 00:05:47.155
<v Val Levitan>Yes, yes.</v>

00:05:47.875 --> 00:05:49.075
<v Nathan Carver>Yep, so.</v>

00:05:48.355 --> 00:05:48.915
<v Val Levitan>Yes.</v>

00:05:50.595 --> 00:05:52.435
<v Nathan Carver>Ideally, those are all just...</v>

00:05:54.515 --> 00:06:00.435
<v Nathan Carver>Those are all identical characteristics, so the contract has to have enough characteristics.</v>

00:06:01.555 --> 00:06:07.795
<v Nathan Carver>for the agent to put those things together to say, okay, these are the screws I need. These are, this is.</v>

00:06:08.675 --> 00:06:12.595
<v Nathan Carver>We have those screws, so I'm going to put those into the assembly.</v>

00:06:12.075 --> 00:06:29.635
<v Val Levitan>No, I understand, but for some reason you're not answering my question. Let me rephrase it differently. Are you or Genadi creating a specific scenario guiding the process of assembling a bill of material, or are you just letting</v>

00:06:29.875 --> 00:06:40.915
<v Val Levitan>AI loose, say, hey, AI, figure out the logic, how the whole thing comes together based on the data contracts that we have.</v>

00:06:42.035 --> 00:06:55.075
<v Val Levitan>And if it assembles it, then great. If it doesn't assemble, it stumbles it. You're not giving it the logic, but you say, I'm missing something in the data contract.</v>

00:06:57.075 --> 00:07:04.355
<v Nathan Carver>Correct. So, no, the idea is that there is a procedure, a function of some kind that can...</v>

00:07:05.875 --> 00:07:09.915
<v Nathan Carver>match up and align contracts. The agent would be used to...</v>

00:07:11.475 --> 00:07:20.675
<v Nathan Carver>First edge case searching and things like that, but we shouldn't need the agent to identify compatible parts. The contract files.</v>

00:07:21.875 --> 00:07:27.715
<v Nathan Carver>So, the trek that we're where we are right now is...</v>

00:07:28.675 --> 00:07:35.395
<v Nathan Carver>What's the starting point? What defines what goes into an assembly or a bomb?</v>

00:07:36.675 --> 00:07:37.555
<v Nathan Carver>And then.</v>

00:07:38.595 --> 00:07:56.035
<v Nathan Carver>we can, so if Genadi is just choosing a part, I need this part in an assembly, then the functions should be to identify all the other contractual components that are needed or that match that part that he wants to add into an assembly, for example.</v>

00:07:57.475 --> 00:08:05.715
<v Nathan Carver>The agent can do the same thing, but it shouldn't have to make those decisions because that's just a repeatable logic that we want to build in.</v>

00:08:08.555 --> 00:08:19.715
<v Nathan Carver>So where the agent would come in is, you know, aided searching and guidance in finding different things, but contractually, these things should fit together programmatically.</v>

00:08:22.355 --> 00:08:28.115
<v Nathan Carver>So the question is, I think, Genadi and I are in a state of, okay, what's our conceptual starting point?</v>

00:08:29.595 --> 00:08:37.875
<v Nathan Carver>What does this flat structure look like for the assembly or an actual bomb that points to all these contracts?</v>

00:08:38.835 --> 00:08:52.995
<v Val Levitan>Nathan, I'm sorry, I'm being very difficult today, but I'm struggling in understanding. I'm struggling understanding you. It might be me, or it might be that</v>

00:08:54.515 --> 00:08:59.315
<v Val Levitan>Maybe you're not explaining yourself correctly, so...</v>

00:08:58.595 --> 00:08:59.235
<v Nathan Carver>OK, sure.</v>

00:09:00.515 --> 00:09:01.395
<v Val Levitan>So, the...</v>

00:09:03.675 --> 00:09:07.475
<v Val Levitan>Let's go down to the prompt. What are you telling the agent?</v>

00:09:08.915 --> 00:09:20.275
<v Val Levitan>Because what I'm trying to avoid, what I'm sorry, what I want to make absolutely 100% sure that I am not or Genadi is not guiding the agent.</v>

00:09:21.475 --> 00:09:40.835
<v Val Levitan>On how to assemble it or create some sort of a template, how to assemble it. I'm trying to avoid any sort of template. I would like to leave. The agent or group of agents free, absolutely free without any instructions how to assemble a machine.</v>

00:09:41.475 --> 00:09:43.715
<v Val Levitan>Only based on data contracts.</v>

00:09:45.475 --> 00:10:00.915
<v Val Levitan>The only guiding principle for an agent or group of agents must be a description of what it is, a verbal description. This is a machine, you know, you know, roughly what it does functionally.</v>

00:10:01.875 --> 00:10:07.715
<v Val Levitan>And the rest should be left up to a group of agents to read the contracts.</v>

00:10:08.915 --> 00:10:14.195
<v Val Levitan>Without any guidance, to assemble all the flat parts into subassemblies.</v>

00:10:15.635 --> 00:10:24.275
<v Val Levitan>That's what I'm trying to achieve. And I'm hoping that neither you nor Genadi is helping the agent.</v>

00:10:17.875 --> 00:10:18.435
<v Nathan Carver>Correct.</v>

00:10:25.475 --> 00:10:26.355
<v Val Levitan>In doing so.</v>

00:10:28.315 --> 00:10:29.075
<v Nathan Carver>Correct.</v>

00:10:28.355 --> 00:10:33.155
<v Val Levitan>Enhances my question: Are you or are you not?</v>

00:10:33.715 --> 00:10:53.195
<v Nathan Carver>No. So let me give you an example of a prompt. So the first thing we've successfully done is I prompted the agent to review the design materials and write the contracts for that part. And the agent can go through and write contracts without any</v>

00:10:54.755 --> 00:11:03.715
<v Nathan Carver>It knows what a contract looks like, it knows the guidelines of a contract, and it can review all the materials and write a contract for each part.</v>

00:11:05.075 --> 00:11:07.395
<v Nathan Carver>So, the piece that we're at now is...</v>

00:11:08.355 --> 00:11:14.675
<v Nathan Carver>We're going to tell the agent, build me a bomb for whatever.</v>

00:11:16.915 --> 00:11:21.155
<v Nathan Carver>And then the agent can use the contracts to go build it.</v>

00:11:23.355 --> 00:11:33.515
<v Nathan Carver>And so all is what we need is what is that starting point? That's what we're trying to figure out is what is that prompt? Where am I starting with the agent?</v>

00:11:34.635 --> 00:11:40.195
<v Nathan Carver>so that it has enough information to go assemble a bomb.</v>

00:11:41.475 --> 00:11:44.435
<v Val Levitan>You are starting from a...</v>

00:11:46.835 --> 00:11:54.435
<v Val Levitan>from a description of what it is, what the product is. That's all I want to give the agent.</v>

00:11:54.835 --> 00:11:55.315
<v Nathan Carver>Okay.</v>

00:11:55.795 --> 00:12:20.195
<v Val Levitan>So I want to give the agent an idea that this is an ATM machine or this is a gaming machine. And let the agent do the same. Because what I'm trying to do is to create an environment where everything around this concept is easy to substitute or easy to go to the vendor and say, these are my mounting dimensions. This is what I'm looking for. This is</v>

00:12:20.355 --> 00:12:32.355
<v Val Levitan>replacement, this is the spec, this is how it functions. If I can have the agent to sync for itself, then everything, all other functionality will click for me.</v>

00:12:33.075 --> 00:12:35.075
<v Nathan Carver>OK, so.</v>

00:12:36.115 --> 00:12:44.355
<v Val Levitan>And I need and I need a group of agents. I need an agent that writes the spec. I need an auditor. I need an assembler.</v>

00:12:46.995 --> 00:12:48.435
<v Nathan Carver>Understood. Okay.</v>

00:12:48.275 --> 00:13:06.595
<v Val Levitan>And I need and I need a looping learning process. Oh, I made a mistake here. Oh, Genadi corrected me. Oh, but that's because of missing spec or missing data sheet. So.</v>

00:13:06.835 --> 00:13:25.315
<v Val Levitan>It's not that I was wrong, it was the data sheet that was missing. Get me the ******* data sheet. I don't have the data sheet. So go to the supplier, get me the data sheet. Oh, that data sheet that I got from the supplier, that's a BS data sheet. That's a ********. The supplier sent me the wrong sheet.</v>

00:13:13.915 --> 00:13:14.195
<v Nathan Carver>Mm.</v>

00:13:26.515 --> 00:13:28.195
<v Val Levitan>So that's what I'm after.</v>

00:13:26.995 --> 00:13:27.475
<v Nathan Carver>Okay.</v>

00:13:29.235 --> 00:13:30.995
<v Nathan Carver>Understood. Okay.</v>

00:13:30.395 --> 00:13:45.395
<v Val Levitan>And I can only achieve it, in my opinion, I can only achieve it if I have free thinking learning agent or group of agents, as well as the auditing agents. I am missing this data sheet. Let me chase it. Let me chase the supplier.</v>

00:13:48.035 --> 00:13:55.635
<v Nathan Carver>Okay, so the starting point is a description of what I want to build, and the agent is going to go assemble that.</v>

00:13:56.755 --> 00:14:01.315
<v Nathan Carver>And then the workflow is going to be, this is what I've assembled, but this is.</v>

00:14:02.755 --> 00:14:22.435
<v Nathan Carver>This is what I think you want to build, and here is what I think the agent is going to come back with is, here are three different alternatives to what I think you need to build. So then the human interaction comes in and says, yes, I want this, or giving the agent direction more, refining what it is that they want.</v>

00:14:23.075 --> 00:14:34.915
<v Val Levitan>Or the human says, no, you built, this doesn't fit. Or, you know, this doesn't go together. And the agent says, yeah, but you supplied me this data sheet.</v>

00:14:35.915 --> 00:14:37.515
<v Val Levitan>or this data contract.</v>

00:14:38.355 --> 00:14:40.275
<v Val Levitan>I built it based on the...</v>

00:14:41.555 --> 00:14:50.035
<v Val Levitan>raw material that you provided. And then Genadi says, oh, ****, I supplied the wrong bill of material. That's why it doesn't fit.</v>

00:14:50.595 --> 00:14:51.155
<v Nathan Carver>Yeah, yeah.</v>

00:14:51.235 --> 00:14:54.675
<v Val Levitan>It sure, the agent, the agents, plural.</v>

00:14:55.595 --> 00:15:11.475
<v Val Levitan>should not be able to assemble a product if they are presented with the wrong data contract. And data contract, the exit is the data contract, but the entry point is the data sheet.</v>

00:15:03.555 --> 00:15:04.115
<v Nathan Carver>Correct.</v>

00:15:12.435 --> 00:15:18.635
<v Nathan Carver>So your output in this is a new bill of material, essentially. Okay.</v>

00:15:17.395 --> 00:15:21.875
<v Val Levitan>Yes, yes, yes, unguided, unguided.</v>

00:15:22.035 --> 00:15:24.515
<v Nathan Carver>Unguided assembly of a bill. OK.</v>

00:15:25.635 --> 00:15:28.915
<v Val Levitan>Yes, I know that right now you're cheating and you're dumping.</v>

00:15:30.275 --> 00:15:49.235
<v Val Levitan>bill of material from MSBC, you're creating a flat list. I understand this, I understand that you're cheating, but pretend that we don't have a bill of material in the MSBC. This product never existed. We're creating something else. We're creating that has, we're creating something that's never been built by JBL yet.</v>

00:15:49.715 --> 00:15:52.435
<v Val Levitan>How do we start? We start from...</v>

00:15:53.595 --> 00:15:57.795
<v Val Levitan>Speaking each part separately, and then Genadi goes through.</v>

00:16:00.115 --> 00:16:19.835
<v Val Levitan>3D design trying to fit, make sure that everything is fit correctly. Well, I don't need any of it. I could just say, look, suppliers, I'm building this. This is a 3D vision of it, supply me all the data sheet that goes in here. And 5 suppliers give me some data sheets that</v>

00:16:20.435 --> 00:16:29.155
<v Val Levitan>Don't match together. I could put an agent on it and say, hey dudes, you gave me some crap, you gave me ****.</v>

00:16:30.915 --> 00:16:31.715
<v Nathan Carver>Okay, that makes sense.</v>

00:16:31.075 --> 00:16:50.875
<v Val Levitan>It doesn't match. And your power supply cannot handle this power. And the monitor is, you know, doesn't have whatever I'm looking for. I want to do it within minutes through an agent. I don't want Genadi to sit with, you know, 3D vision and viewing and</v>

00:16:51.235 --> 00:16:52.355
<v Val Levitan>This is, this is.</v>

00:16:54.755 --> 00:16:55.875
<v Val Levitan>I can't handle this.</v>

00:16:55.155 --> 00:16:56.875
<v Nathan Carver>Okay, that makes sense.</v>

00:16:58.115 --> 00:17:01.395
<v Val Levitan>I'm going to repeat myself again because I want to hammer it home.</v>

00:17:02.675 --> 00:17:18.435
<v Val Levitan>These agents have to be unguided. They cannot go there with predetermined view of Genadi, how the bill of material needs to be assembled. And that's the whole thing. This is where I'm pushing you.</v>

00:17:20.355 --> 00:17:30.355
<v Nathan Carver>Got it. So the only thing the agents will know is what a bill of material would look like, but not what the component or assembly would be.</v>

00:17:30.755 --> 00:17:34.355
<v Val Levitan>A description, general description, I want to make an ATM machine.</v>

00:17:34.355 --> 00:17:34.835
<v Nathan Carver>Got it.</v>

00:17:35.555 --> 00:17:55.235
<v Val Levitan>And any agent right now know what's an ATM machine is. Okay, well, it has a touch screen, it has a TV, it has a bill acceptor, it has this, it has door, doors open, access, sliding mechanism, yes. Today, and especially as the agents become more clever,</v>

00:17:36.275 --> 00:17:36.435
<v Nathan Carver>Van.</v>

00:17:47.795 --> 00:17:48.115
<v Nathan Carver>Yeah.</v>

00:17:55.795 --> 00:17:58.275
<v Val Levitan>In half a year, this should not be a problem at all.</v>

00:17:59.355 --> 00:18:13.235
<v Val Levitan>But as long as we do not guide the agent, we do not give it a system, assemble it based on this, or do this, nothing of that nature. The only guiding principle, this is an ATM machine.</v>

00:18:14.035 --> 00:18:20.675
<v Val Levitan>You're assembling an ATM machine. You're not assembling a garbage compactor.</v>

00:18:22.595 --> 00:18:23.355
<v Nathan Carver>Understood.</v>

00:18:25.555 --> 00:18:41.555
<v Nathan Carver>Okay, now that helps. That helps clarify your vision of the input and the output. And that answers a question that I was bouncing around with Genadi. So I understand my starting point and I can start building towards that.</v>

00:18:45.155 --> 00:18:47.155
<v Val Levitan>I'd like to have a spike.</v>

00:18:48.755 --> 00:18:53.075
<v Val Levitan>Let's assemble A sub-assembly of any sort, whatever is easy to assemble.</v>

00:18:54.315 --> 00:19:01.395
<v Val Levitan>Let's have a spike. I want Genadi to see because Genadi, when I tell him this vision, he looks at me like...</v>

00:19:04.675 --> 00:19:19.395
<v Val Levitan>He thinks in old fashion, he thinks, I don't understand. If you don't give it a path, if you don't give it a subset, or if you don't give it a structure, how will it do it?</v>

00:19:08.275 --> 00:19:08.995
<v Nathan Carver>Yeah, I get it.</v>

00:19:20.435 --> 00:19:23.875
<v Val Levitan>Valid question, but I've seen it done in development.</v>

00:19:25.395 --> 00:19:28.275
<v Val Levitan>Developers don't guide agents anymore.</v>

00:19:30.035 --> 00:19:34.435
<v Nathan Carver>Right, yes, yeah, that's nice.</v>

00:19:32.835 --> 00:19:41.075
<v Val Levitan>And the code is, and the code is being written, and not only the code is being written, you can even do end-to-end testing right now.</v>

00:19:42.195 --> 00:19:43.635
<v Nathan Carver>Yeah, yeah.</v>

00:19:44.675 --> 00:19:45.235
<v Nathan Carver>Okay.</v>

00:19:47.715 --> 00:20:06.755
<v Val Levitan>But Genadi has a binary mechanical vision of things. And unless I show it, look, look, the only thing that it knows how that this is a power supply. It doesn't know anything else. It just knows that it's a power supply. But it will assemble a power supply. I'm going to give it flat parts.</v>

00:20:06.795 --> 00:20:19.515
<v Val Levitan>and it will assemble it into an enclosure with a power supply. We'll put boards and filter and the receptacle and it will do everything the way it needs to be done and it will create a power supply that will be a sub-assembly.</v>

00:20:21.715 --> 00:20:25.075
<v Nathan Carver>Okay. All right. That makes sense.</v>

00:20:27.955 --> 00:20:40.675
<v Val Levitan>So the agent will know that this is an ATM machine, it has a power supply, it has a monitor block, it has something else, it has something else, it has doors open for service.</v>

00:20:28.995 --> 00:20:29.635
<v Nathan Carver>I will.</v>

00:20:35.195 --> 00:20:35.475
<v Nathan Carver>Yeah.</v>

00:20:42.995 --> 00:20:52.755
<v Nathan Carver>Okay, so what I'm going to do is spike out a workflow where we can ask the agent for something simple, the ATM, whatever simple thing that we want to build.</v>

00:20:53.795 --> 00:20:59.475
<v Nathan Carver>And I envision the agent asking some clarifying questions and then moving forward.</v>

00:21:00.355 --> 00:21:01.395
<v Nathan Carver>Would be pretty much it.</v>

00:21:00.675 --> 00:21:08.435
<v Val Levitan>Yes, yes, and what I want to make sure that we only fall on, do I have the right data sheet?</v>

00:21:09.555 --> 00:21:10.035
<v Nathan Carver>Correct.</v>

00:21:10.995 --> 00:21:11.435
<v Nathan Carver>Okay.</v>

00:21:11.795 --> 00:21:16.035
<v Val Levitan>Because that's the source of actual knowledge, the correct data sheet.</v>

00:21:17.195 --> 00:21:22.035
<v Val Levitan>Because then I can work with the supplier. I could say, this is the data sheet, this one, this one.</v>

00:21:23.235 --> 00:21:26.915
<v Val Levitan>And you sent me the wrong part; you know I'm not, I'm not paying for it.</v>

00:21:28.195 --> 00:21:29.315
<v Nathan Carver>Yeah, gotcha.</v>

00:21:31.155 --> 00:21:31.635
<v Nathan Carver>OK.</v>

00:21:33.955 --> 00:21:35.075
<v Val Levitan>Thank you very much.</v>

00:21:34.355 --> 00:21:35.955
<v Nathan Carver>All right, they're working on that.</v>

00:21:36.435 --> 00:21:39.475
<v Val Levitan>So, when, when can I have a first first view?</v>

00:21:40.435 --> 00:21:43.715
<v Nathan Carver>Let's shoot for Wednesday.</v>

00:21:44.955 --> 00:21:49.315
<v Nathan Carver>I'm going to shoot for Wednesday, and if not Thursday, but I'd like to have it Wednesday.</v>

00:21:45.155 --> 00:21:46.595
<v Val Levitan>Okay, can you hear that?</v>

00:21:51.395 --> 00:21:54.595
<v Val Levitan>Alright, will you send me a note when you're ready?</v>

00:21:54.915 --> 00:21:56.675
<v Nathan Carver>Yeah, I'll send you a note for sure.</v>

00:21:57.235 --> 00:22:01.315
<v Val Levitan>I don't want to book a meeting if you're not ready, but just send if you're getting.</v>

00:21:59.555 --> 00:22:04.115
<v Nathan Carver>Okay, yeah, I'll get it booked. Yeah, I'll get it booked.</v>

00:22:04.435 --> 00:22:05.315
<v Val Levitan>Thank you, bye bye.</v>

00:22:05.315 --> 00:22:06.515
<v Nathan Carver>All right, thanks, Val.</v>

