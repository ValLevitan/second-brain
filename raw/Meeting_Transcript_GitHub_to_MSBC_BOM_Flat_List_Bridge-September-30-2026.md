# Raw Transcript — GitHub_to_MSBC_BOM_Integration
**Date:** September 30, 2026, 10:00 AM – 10:51 AM Eastern
**Summary note:** [[Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026]]
---
WEBVTT

00:00:03.250 --> 00:00:04.090
<v Lev Rudky>Good morning.</v>

00:00:05.610 --> 00:00:06.970
<v Val Levitan>Okay, so.</v>

00:00:09.450 --> 00:00:24.810
<v Val Levitan>Unless you guys have any questions or concerns, let me set out the objective of the meeting. What we would like to do is to figure out a way by which Genadi could</v>

00:00:26.010 --> 00:00:27.370
<v Val Levitan>Continuously.</v>

00:00:29.210 --> 00:00:31.770
<v Val Levitan>on a reoccurring basis all the time.</v>

00:00:32.890 --> 00:00:44.330
<v Val Levitan>Update various drawings as he needs to. I mean, no pressure if he doesn't have to, then he doesn't have to, and when a new drawing.</v>

00:00:45.530 --> 00:00:51.690
<v Val Levitan>or suppliers spec or anything that has to do with supplier.</v>

00:00:53.130 --> 00:00:54.090
<v Val Levitan>Changes.</v>

00:00:56.490 --> 00:01:05.610
<v Val Levitan>And that supplier or Genadi is drawing or mechanical design or hardware design or engineering design of any sort.</v>

00:01:07.050 --> 00:01:10.970
<v Val Levitan>Is part of a bill of material.</v>

00:01:11.930 --> 00:01:16.010
<v Val Levitan>that will further be incorporated in production.</v>

00:01:18.570 --> 00:01:25.690
<v Val Levitan>That gets updated. There is a new revision created all the time. Github is very good at creating revisions.</v>

00:01:27.610 --> 00:01:30.970
<v Val Levitan>that replacement or part or component.</v>

00:01:32.090 --> 00:01:35.690
<v Val Levitan>Or a design drawing.</v>

00:01:39.530 --> 00:01:40.330
<v Val Levitan>Yes.</v>

00:01:42.010 --> 00:01:42.730
<v Val Levitan>Updated.</v>

00:01:44.570 --> 00:01:50.090
<v Val Levitan>as part of the bill of material in the manufacturing and the respective.</v>

00:01:51.530 --> 00:01:52.650
<v Val Levitan>Information.</v>

00:01:54.170 --> 00:01:57.690
<v Val Levitan>Costs, bill of materials are updated.</v>

00:01:58.850 --> 00:02:00.410
<v Val Levitan>In Msbc.</v>

00:02:04.090 --> 00:02:06.090
<v Val Levitan>This is where we want to arrive.</v>

00:02:09.370 --> 00:02:12.170
<v Val Levitan>The supplier.</v>

00:02:14.450 --> 00:02:15.450
<v Val Levitan>Information.</v>

00:02:18.810 --> 00:02:26.490
<v Val Levitan>financial information, banking information, address, contact information for the supplier, active supplier.</v>

00:02:27.650 --> 00:02:32.570
<v Val Levitan>He is located and updated inside of the Msbc.</v>

00:02:33.930 --> 00:02:35.610
<v Val Levitan>The engineering.</v>

00:02:36.730 --> 00:02:37.770
<v Val Levitan>Files.</v>

00:02:38.890 --> 00:02:41.930
<v Val Levitan>Drawings, specs, live.</v>

00:02:43.290 --> 00:02:45.610
<v Val Levitan>And update it in Github.</v>

00:02:48.410 --> 00:02:56.890
<v Val Levitan>There is a clear separation between engineering territory and administrative territory.</v>

00:03:01.690 --> 00:03:04.010
<v Val Levitan>Engineers are never allowed.</v>

00:03:04.970 --> 00:03:08.570
<v Val Levitan>To change anything in Msbc.</v>

00:03:09.530 --> 00:03:15.210
<v Val Levitan>The administrator is never allowed to change anything in Github.</v>

00:03:45.290 --> 00:03:48.090
<v Genadi Peari>And should we command this?</v>

00:03:48.330 --> 00:03:55.130
<v Val Levitan>Yes, of course. And I appreciate the fact that this is maybe a new concept for us right now.</v>

00:03:57.690 --> 00:03:58.970
<v Val Levitan>And.</v>

00:04:00.170 --> 00:04:04.970
<v Val Levitan>All of us may have concerns or questions. Let's work through the concerns.</v>

00:04:06.250 --> 00:04:12.410
<v Val Levitan>instead of rejections. I don't want to be a therapist.</v>

00:04:14.890 --> 00:04:20.490
<v Val Levitan>I don't want to play a role of a therapist that convinces why one thing is better than the other.</v>

00:04:22.690 --> 00:04:26.210
<v Val Levitan>I'm just saying that's how we are setting up our business.</v>

00:04:27.450 --> 00:04:28.330
<v Val Levitan>To function.</v>

00:04:29.690 --> 00:04:31.530
<v Val Levitan>And let's work through.</v>

00:04:32.610 --> 00:04:33.530
<v Val Levitan>Concerns.</v>

00:04:35.050 --> 00:04:50.890
<v Val Levitan>one by one, and let's find solutions to the concerns. Instead of for me trying to say, well, but this is how the trend is. This is how we're going to do it. Let's do it. Let's conquer it. None of that.</v>

00:04:51.690 --> 00:04:55.530
<v Val Levitan>Just let's address a concern and see how we can address it.</v>

00:04:57.050 --> 00:05:07.610
<v Val Levitan>Sorry, let's identify a concern. I meant to say identify a concern and let's find a solution for it. Sorry, Genadi, go ahead.</v>

00:04:57.250 --> 00:04:58.090
<v Genadi Peari>OK, about.</v>

00:05:08.010 --> 00:05:22.970
<v Genadi Peari>For my perspective, I fully support first part of your description when we keep all the engineering information in Github, including...</v>

00:05:24.330 --> 00:05:36.090
<v Genadi Peari>Parts, specifications, drawings, designs of the printed circuit boards, mechanical designs, all description, everything.</v>

00:05:37.530 --> 00:05:48.090
<v Genadi Peari>No questions. I think everybody and I think Nathan also understand how can organize this with supportive files and.</v>

00:05:49.130 --> 00:05:50.410
<v Genadi Peari>Dogs and everything.</v>

00:05:52.970 --> 00:06:07.290
<v Genadi Peari>About the second part of the bill of material, I cannot comprehend how it's possible, in what format we can keep all the bill of materials in Github, in what...</v>

00:06:08.490 --> 00:06:15.130
<v Genadi Peari>in what format and how we can manage it in the Github with all the structures that we have.</v>

00:06:16.490 --> 00:06:22.090
<v Genadi Peari>Uh, it is the models and how it's even how, how in what?</v>

00:06:24.650 --> 00:06:28.410
<v Genadi Peari>This is, for me, it's completely uncertain.</v>

00:06:29.530 --> 00:06:29.770
<v Genadi Peari>Ai.</v>

00:06:31.450 --> 00:06:38.170
<v Genadi Peari>How do we duplicate the structure in the Github, similar to what it should be?</v>

00:06:42.450 --> 00:06:47.770
<v Val Levitan>To duplicate, meaning we already have something we want to duplicate.</v>

00:06:46.090 --> 00:06:47.370
<v Genadi Peari>Recover.</v>

00:06:48.890 --> 00:06:55.210
<v Genadi Peari>We have structures of build bill of material like we did in the vision and the Msbc.</v>

00:06:54.810 --> 00:07:12.730
<v Val Levitan>Yes, I understand. Navision was designed 50 years ago, got obsolete 30 years ago, and was taken offline 20 years ago, and now practically dead. So whatever methodology Navision used, we kind of inherited and trained our minds to use Navision</v>

00:07:13.370 --> 00:07:18.730
<v Val Levitan>But that has antiquated itself and has gone out of circulation.</v>

00:07:18.570 --> 00:07:19.210
<v Genadi Peari>Ai.</v>

00:07:20.090 --> 00:07:21.450
<v Genadi Peari>I mentioned the vision.</v>

00:07:20.250 --> 00:07:38.890
<v Val Levitan>The Excel path was used previously as a tool in the absence of any other tools. So let's not say, how do I take my Excel and do something else?</v>

00:07:39.690 --> 00:07:41.930
<v Val Levitan>Let's just define an issue.</v>

00:07:42.970 --> 00:07:47.290
<v Val Levitan>of what information needs to be transferred into.</v>

00:07:48.410 --> 00:07:53.370
<v Val Levitan>Msbc and then find the way the effective way of how to transfer.</v>

00:07:54.890 --> 00:08:04.810
<v Val Levitan>So what capabilities do we need? We need a capability of transferring the final most updated information.</v>

00:08:08.170 --> 00:08:10.010
<v Val Levitan>Into Msbc.</v>

00:08:11.010 --> 00:08:18.330
<v Val Levitan>that forms a bill of material for a sub-assembly or assembly.</v>

00:08:20.170 --> 00:08:20.810
<v Genadi Peari>Everything.</v>

00:08:23.930 --> 00:08:28.090
<v Genadi Peari>Fill of materials includes sub-assemblies, assemblies, modules.</v>

00:08:24.410 --> 00:08:25.850
<v Val Levitan>Well, I just, I just know.</v>

00:08:27.050 --> 00:08:28.250
<v Val Levitan>I justified.</v>

00:08:29.410 --> 00:08:33.850
<v Val Levitan>Yes, sir, I understand, so I just, I just verbalize the capability.</v>

00:08:39.210 --> 00:08:51.610
<v Genadi Peari>This is one point how to move it. First, how to keep it, how to keep it in the Github, in what format? This is my first question.</v>

00:08:45.530 --> 00:08:46.730
<v Val Levitan>Been there for nothing.</v>

00:08:52.810 --> 00:08:53.610
<v Genadi Peari>How, how?</v>

00:08:55.290 --> 00:08:56.250
<v Val Levitan>So, we need...</v>

00:08:55.290 --> 00:08:57.690
<v Genadi Peari>How, how, what tools do we have for this?</v>

00:08:58.490 --> 00:09:04.170
<v Val Levitan>We need the capability should probably sound like this.</v>

00:09:07.930 --> 00:09:08.650
<v Val Levitan>On.</v>

00:09:14.490 --> 00:09:22.010
<v Val Levitan>We're capable of assembling a raw bill of material or raw list of materials.</v>

00:09:15.050 --> 00:09:15.290
<v Nathan Carver>Good.</v>

00:09:23.290 --> 00:09:24.090
<v Val Levitan>AR.</v>

00:09:26.570 --> 00:09:27.610
<v Genadi Peari>Structurized.</v>

00:09:26.810 --> 00:09:27.370
<v Val Levitan>Tour.</v>

00:09:29.770 --> 00:09:32.130
<v Val Levitan>Well, I'm not sure that it needs to be structurized.</v>

00:09:35.610 --> 00:09:37.370
<v Val Levitan>We just need a list of some sort.</v>

00:09:38.090 --> 00:09:41.770
<v Genadi Peari>I cannot maintain lists, how we need the structure.</v>

00:09:41.610 --> 00:09:46.490
<v Val Levitan>I'm not, I'm not sure that we need to maintain this. I think it has to be a flood.</v>

00:09:44.650 --> 00:09:46.090
<v Genadi Peari>But, but if you don't...</v>

00:09:48.010 --> 00:09:56.570
<v Genadi Peari>But if it's flat, how you can move it? If it's flat, how you will be able to transfer it to Msbc?</v>

00:09:48.250 --> 00:09:49.930
<v Val Levitan>Go ahead. Don't do it.</v>

00:09:57.530 --> 00:10:00.730
<v Genadi Peari>You need the socket somehow, which is...</v>

00:10:01.690 --> 00:10:06.890
<v Val Levitan>That's a different capability. We have to then be able to transfer.</v>

00:10:08.570 --> 00:10:11.530
<v Val Levitan>A flat list to Msbc.</v>

00:10:16.010 --> 00:10:17.810
<v Nathan Carver>Yeah, these are similar to a...</v>

00:10:18.810 --> 00:10:19.770
<v Nathan Carver>Build script.</v>

00:10:21.210 --> 00:10:24.570
<v Nathan Carver>your whatever structure is needed to maintain.</v>

00:10:25.850 --> 00:10:30.730
<v Nathan Carver>That within Github and then have a build that translates that into.</v>

00:10:32.330 --> 00:10:35.770
<v Nathan Carver>a data structure that can be pushed to Msbc.</v>

00:10:37.050 --> 00:10:49.530
<v Nathan Carver>So there may be a middle step that is automated, translating what Genadi is seeing and managing into something that the application can sync back and forth with Msbc.</v>

00:10:50.250 --> 00:11:09.410
<v Val Levitan>But Genadi, Genadi maintains, in reality, maintains a flat list. Genadi says there is 550 nominations that will go into assembling one machine. Some of it will be two each, some will</v>

00:11:09.650 --> 00:11:11.450
<v Val Levitan>Require 50 each.</v>

00:11:12.330 --> 00:11:16.890
<v Val Levitan>But a flat list is 550 nominations.</v>

00:11:20.210 --> 00:11:24.010
<v Val Levitan>And, in reality, Gennady, that's all that Genadi does.</v>

00:11:20.410 --> 00:11:20.810
<v Nathan Carver>Okay.</v>

00:11:25.610 --> 00:11:36.810
<v Val Levitan>Then step #2 that Genadi does, he says, I need 50 of this, I need five of that, I need one of this and three of that.</v>

00:11:38.930 --> 00:11:43.130
<v Val Levitan>And then the third thing that Genadi does, he develops.</v>

00:11:46.890 --> 00:11:48.970
<v Val Levitan>The process by which...</v>

00:11:50.490 --> 00:11:58.410
<v Val Levitan>the process and priority by which all of the flat list comes together.</v>

00:12:00.650 --> 00:12:01.770
<v Val Levitan>So, three things.</v>

00:12:02.650 --> 00:12:04.250
<v Genadi Peari>Not only, no.</v>

00:12:04.490 --> 00:12:07.050
<v Val Levitan>Okay, maybe I'm missing something, so...</v>

00:12:05.850 --> 00:12:09.050
<v Genadi Peari>It's very, yes, but it's very important what you're missing.</v>

00:12:08.890 --> 00:12:10.850
<v Val Levitan>I'm not saying that it's not important.</v>

00:12:11.690 --> 00:12:13.770
<v Genadi Peari>It's very important because...</v>

00:12:12.370 --> 00:12:16.170
<v Val Levitan>Alright, I am not saying, I am not saying that it's not important.</v>

00:12:15.850 --> 00:12:18.090
<v Genadi Peari>Because when you would transfer.</v>

00:12:17.050 --> 00:12:20.650
<v Val Levitan>I'm just saying that maybe, maybe I don't remember. That's it.</v>

00:12:20.650 --> 00:12:29.210
<v Genadi Peari>I just saying the flight list is not good for Navision for Msbc because when they do production.</v>

00:12:27.530 --> 00:12:32.170
<v Val Levitan>I'm not, I'm not, I'm not say, I'm not saying that it's good for Msbc.</v>

00:12:32.890 --> 00:12:51.130
<v Genadi Peari>I am almost done. When they do production orders, for example, they assemble partially machine, okay, they might be assembling, for example, monitor assembly. It has to be this assembly in the Msbc. Then we take this</v>

00:12:52.010 --> 00:12:56.570
<v Genadi Peari>Cell, we combine another cell, another cell, so you have to be assemblies.</v>

00:12:55.930 --> 00:13:03.050
<v Val Levitan>In, in, in Msbc, in M, in, in Msbc, but we're here.</v>

00:12:57.930 --> 00:12:59.050
<v Genadi Peari>Yes, yes.</v>

00:13:04.570 --> 00:13:16.970
<v Val Levitan>We're still in Github. The step between Github and Msbc is that step that could form it in the shape and the form that we want.</v>

00:13:18.570 --> 00:13:25.930
<v Val Levitan>But let's stay in Github for now. Let's understand that in Github, it is all flood information.</v>

00:13:26.970 --> 00:13:29.930
<v Val Levitan>It's just a big list that's a flood information.</v>

00:13:31.530 --> 00:13:37.050
<v Val Levitan>It gets grouped, compiled in inside of Msbc.</v>

00:13:37.770 --> 00:13:45.050
<v Val Levitan>But that grouping, the step, could be a step of automation. It doesn't have to be a manual step.</v>

00:13:56.810 --> 00:14:02.010
<v Genadi Peari>If you keep all the database of the flat list in Github.</v>

00:14:03.410 --> 00:14:20.570
<v Genadi Peari>Perfect. No argue. But why you need to keep in Github? You take two of these and three of these. You can keep it in Msbc. You keep all the revision, all the history in Github. But why to pool in can be the...</v>

00:14:17.850 --> 00:14:24.370
<v Val Levitan>I am, I am, I am, I am, I am saying the same thing, except I'm saying...</v>

00:14:25.290 --> 00:14:28.810
<v Val Levitan>I'm saying that it does not have to be a manual process.</v>

00:14:40.010 --> 00:14:54.890
<v Genadi Peari>Okay, let's say tomorrow we need South Dakota, we need to supply cable for light and wonder. I need to create the part number. I have a new number. What is automatically?</v>

00:14:53.770 --> 00:15:05.130
<v Val Levitan>Part number part number needs to be created based on a standard that is developed. You the Claude reads the standard.</v>

00:15:06.570 --> 00:15:17.450
<v Val Levitan>And it gives an automatic part number that is then transferred into Msbc only for the first time. When that part is created, it's done.</v>

00:15:15.050 --> 00:15:15.770
<v Genadi Peari>Perfect.</v>

00:15:17.690 --> 00:15:22.090
<v Genadi Peari>I can create it in Github. It's perfect. Or Msbc, it doesn't matter.</v>

00:15:20.890 --> 00:15:38.170
<v Val Levitan>But it's a different procedure. We have a standard of creating parts, part numbers. That is written in Github, in the knowledge base, in the repo that is called standards.</v>

00:15:39.530 --> 00:15:40.250
<v Val Levitan>So.</v>

00:15:41.210 --> 00:15:45.290
<v Val Levitan>Claude looks at the standards and gives it a part number.</v>

00:15:46.330 --> 00:15:47.690
<v Genadi Peari>OK, good.</v>

00:15:48.650 --> 00:15:57.050
<v Genadi Peari>No, no questions. Then we need, I need to populate it in three different products.</v>

00:15:56.410 --> 00:16:00.970
<v Val Levitan>You don't need, you don't need to populate it. Claude can populate it.</v>

00:16:02.010 --> 00:16:04.570
<v Genadi Peari>So, Claude can populate it, but...</v>

00:16:19.210 --> 00:16:21.530
<v Val Levitan>I want to go from design.</v>

00:16:23.650 --> 00:16:24.810
<v Val Levitan>Do the automation.</v>

00:16:29.290 --> 00:16:38.090
<v Val Levitan>During the design, you already know which component goes where. You actually have in your drawings, you have a placement of where everything is.</v>

00:16:42.090 --> 00:16:44.130
<v Genadi Peari>So, we keep three different...</v>

00:16:46.090 --> 00:16:53.210
<v Genadi Peari>So, so what exactly Claude will do? How how it will populate this this wire to three-part to three different products?</v>

00:16:49.770 --> 00:16:55.850
<v Val Levitan>Hopefully, hopefully, hope I don't, I don't, I don't know. Hopefully everything.</v>

00:16:56.010 --> 00:16:57.410
<v Genadi Peari>Okay, so even...</v>

00:16:56.850 --> 00:17:00.810
<v Val Levitan>What I'm saying, when I'm hold on a second, what I'm saying, I don't know.</v>

00:17:01.770 --> 00:17:16.170
<v Val Levitan>That means, as I sit here right now, before Nathan had a chance to experiment with it, we don't know right now, but it's not, it's not.</v>

00:17:19.410 --> 00:17:32.730
<v Val Levitan>spaceship science. This is just a little bit of tinkering here and there. The point is that I'm making that the source of truth here is your drawings, your design.</v>

00:17:33.770 --> 00:17:37.610
<v Val Levitan>From there, I want to automate, I want to make it us.</v>

00:17:38.810 --> 00:17:41.130
<v Val Levitan>As automated as possible.</v>

00:17:42.810 --> 00:17:45.610
<v Val Levitan>I want to remove all this labor from you.</v>

00:17:48.170 --> 00:17:56.170
<v Val Levitan>So you're doing your design, every single piece of flame goes inside of that design.</v>

00:17:57.250 --> 00:18:03.290
<v Val Levitan>And whatever isn't, you still know where it goes because you pre-drilled the holes.</v>

00:18:05.930 --> 00:18:13.130
<v Val Levitan>You know every single thing. You can't even put a screw inside of the machine without having a hole for it.</v>

00:18:14.250 --> 00:18:30.730
<v Val Levitan>We don't have self-tapping screws. There is no room for imagination for an assembly worker to put things anywhere except in the exact predetermined location that you assign during the time that you make the drawing.</v>

00:18:33.930 --> 00:18:37.050
<v Val Levitan>There is 0 room for imagination.</v>

00:18:38.570 --> 00:18:42.250
<v Val Levitan>For each individual screw, for each individual bracket.</v>

00:18:44.570 --> 00:18:58.490
<v Val Levitan>The PC board that we are not even designing, you know the dimension for it, and you have this dimension, you've measured it, you know exactly how it's going to be fastened, you provide the posts for it.</v>

00:18:59.850 --> 00:19:04.650
<v Val Levitan>You know exactly if it's self-topping, what the diameter is.</v>

00:19:07.970 --> 00:19:13.770
<v Val Levitan>That's the source of truth. I don't want to create another source of truth. I already have one source of truth.</v>

00:19:48.570 --> 00:19:53.450
<v Genadi Peari>I just raised the question, I and I said I don't know how we do it.</v>

00:19:54.410 --> 00:20:13.010
<v Genadi Peari>And I'm not against. You want to automate it? It's very good. The question is still there. How do we transfer structurized bill of material from flat, some flat to in Github to Msbc? And what is the rule?</v>

00:19:56.850 --> 00:19:57.690
<v Val Levitan>I respect it.</v>

00:19:58.730 --> 00:20:00.490
<v Val Levitan>I I RIS.</v>

00:20:13.250 --> 00:20:19.970
<v Genadi Peari>To keep this the structurized bill of materials, and so...</v>

00:20:17.890 --> 00:20:21.970
<v Val Levitan>I agree. I agree with this question. Let's discuss it.</v>

00:20:21.170 --> 00:20:27.330
<v Genadi Peari>Because, and this is a question I think to Nathan, what do we, how do we do it simple?</v>

00:20:29.250 --> 00:20:34.850
<v Genadi Peari>Keep in mind, when you we do need to keep the the the the sub-assembly center and Msbc.</v>

00:20:29.690 --> 00:20:30.610
<v Val Levitan>I would like...</v>

00:20:37.730 --> 00:20:44.690
<v Val Levitan>I would like us to go through the source. The source is your design.</v>

00:20:47.170 --> 00:21:00.930
<v Val Levitan>So the file that you're generating in SolidWorks, that file knows everything. Let's agree on one thing. No, no, no. Okay, okay, okay, so tell me.</v>

00:20:55.090 --> 00:20:58.290
<v Genadi Peari>No, not, not at all, not at all.</v>

00:21:00.770 --> 00:21:06.850
<v Genadi Peari>The SolidWorks is just a tool to create mechanical parts. It just shape and the drawings.</v>

00:21:04.930 --> 00:21:25.090
<v Val Levitan>Okay, how do you, okay, when you create, let's say a PC board is not designed by us, it's designed by somebody else. Can you put a PC board somewhere else? Can you shift the PC board by 1 millimeter to the left or to the right?</v>

00:21:29.330 --> 00:21:32.050
<v Val Levitan>Let's say I want to put it on top of the machine.</v>

00:21:33.570 --> 00:21:35.650
<v Val Levitan>I just wanted to be there. Can I do it?</v>

00:21:41.490 --> 00:21:45.810
<v Val Levitan>The answer is no. I don't know why you keep quiet. I have no idea why I...</v>

00:21:42.130 --> 00:21:47.450
<v Genadi Peari>I'm not, I'm not, I'm not, I'm not following your.</v>

00:21:48.450 --> 00:21:52.370
<v Val Levitan>I don't know why you don't follow me. I have no idea why you don't follow me.</v>

00:21:48.530 --> 00:21:49.130
<v Genadi Peari>So it's.</v>

00:21:52.370 --> 00:22:14.370
<v Genadi Peari>No, take another example. Well, we have 10 types of locks. We put a lock in the door. We have different locks. We have keys alike, we have with come, without come, the seven eights, the five sixteenths, 10 types of locks. We don't keep this information in SolidWorks, right? We keep this information in database.</v>

00:22:14.610 --> 00:22:15.570
<v Genadi Peari>Of the parts.</v>

00:22:16.130 --> 00:22:17.970
<v Val Levitan>Yes, so?</v>

00:22:17.810 --> 00:22:21.610
<v Genadi Peari>So it nothing to do with the SolidWorks, so we need to...</v>

00:22:20.450 --> 00:22:23.810
<v Val Levitan>Yes, but yes, but before we...</v>

00:22:25.490 --> 00:22:26.050
<v Val Levitan>Wyk.</v>

00:22:27.570 --> 00:22:30.210
<v Val Levitan>Fine, let's deal with logs first.</v>

00:22:31.730 --> 00:22:39.570
<v Val Levitan>OKOK, so we have we have an item number which is called a lock.</v>

00:22:41.090 --> 00:22:43.650
<v Val Levitan>There are how many different logs?</v>

00:22:44.730 --> 00:22:45.890
<v Genadi Peari>Let's say 10 looks.</v>

00:22:46.530 --> 00:22:48.090
<v Val Levitan>I know, but are they all different?</v>

00:22:48.770 --> 00:22:49.410
<v Genadi Peari>Yes.</v>

00:22:49.810 --> 00:22:55.810
<v Val Levitan>How many different locks? Each lock is different, each single one is different, different size.</v>

00:22:52.930 --> 00:22:53.410
<v Genadi Peari>Yes.</v>

00:22:57.170 --> 00:22:58.290
<v Val Levitan>Different part number.</v>

00:22:58.770 --> 00:23:10.690
<v Genadi Peari>can be keys, key like tubular lock or flat key, tubular key, flat key, different types of cams, different types of locks.</v>

00:23:09.890 --> 00:23:20.450
<v Val Levitan>You cannot, you cannot, there is zero chance, negative chance that you can improvise on anything.</v>

00:23:21.530 --> 00:23:36.850
<v Val Levitan>You have assembly drawings. You define exactly what part number goes where. Nobody in the company can fart without you telling them which corner to go for farting.</v>

00:23:39.570 --> 00:23:45.730
<v Val Levitan>You can only fart in the left side of the hole. That's the instructions where to fart.</v>

00:23:51.250 --> 00:23:52.610
<v Val Levitan>There is no mystery.</v>

00:23:54.050 --> 00:24:03.170
<v Val Levitan>You tell him where to buy, what lock, flat key, tubular key, 5 eighths, 7 ninths, it makes no difference.</v>

00:24:20.770 --> 00:24:44.050
<v Val Levitan>Nobody in manufacturing can assemble, nobody can put a lock inside of the machine without you telling them which lock, which key goes where. You specify the hole, you specify the lock, and you tell Michael which lock he orders, and you tell Elizabeth which lock goes where.</v>

00:24:44.850 --> 00:24:49.650
<v Genadi Peari>Yes, correct log needs to be Msbc. That's it. Yeah, this is the statement.</v>

00:24:50.730 --> 00:24:59.010
<v Val Levitan>The lock, the lock gets into Msbc because this is a purchase part. It has revisions.</v>

00:25:03.010 --> 00:25:08.530
<v Val Levitan>We don't have to use flat key lock. We could substitute with the tubular lock.</v>

00:25:09.890 --> 00:25:13.090
<v Val Levitan>So a bill of material could have various revisions.</v>

00:25:21.090 --> 00:25:21.650
<v Genadi Peari>Oh.</v>

00:25:26.130 --> 00:25:36.130
<v Genadi Peari>The part number definition of the part number is if it is interchangeable, it can have different sources. Yes, tubular or flat. If it's allowed, allowed.</v>

00:25:30.530 --> 00:25:32.050
<v Val Levitan>The part number.</v>

00:25:37.970 --> 00:25:43.170
<v Val Levitan>It's not allowed by itself. You spec it inside.</v>

00:25:43.650 --> 00:25:45.490
<v Genadi Peari>Yeah, we not argue about this.</v>

00:25:44.290 --> 00:25:52.850
<v Val Levitan>The size, the angle, the curvature of the tongue, the length of the tongue, everything has a drawing.</v>

00:25:54.370 --> 00:26:04.610
<v Val Levitan>either supplied by a supplier and you approve that drawing and you put it in the file, or alternatively you design and create a tool for it.</v>

00:26:05.730 --> 00:26:11.450
<v Val Levitan>and create a spec for it. Nothing gets improvised in the machine.</v>

00:27:15.970 --> 00:27:29.650
<v Genadi Peari>So I understood. Well, I don't understand what we are. Yes, we have database. Let's say this database in the Github. We have 10 part numbers in Github for different logs.</v>

00:27:30.850 --> 00:27:38.450
<v Genadi Peari>This is, I think, this is doable. I mean, this is basically what we have today. It just will be kept in the Github.</v>

00:27:39.450 --> 00:27:41.530
<v Genadi Peari>What's the next step? Yeah, what's...</v>

00:27:39.570 --> 00:27:40.130
<v Val Levitan>Github.</v>

00:27:41.170 --> 00:28:00.850
<v Val Levitan>Github has a flat list. We need to agree that Github has a list, one flat list of everything either designed by you that comes out from SolidWorks or comes out from a supplier which you spec, which you approved, which a supplier must.</v>

00:27:59.330 --> 00:27:59.810
<v Genadi Peari>Coo.</v>

00:28:00.890 --> 00:28:02.690
<v Val Levitan>Provide the drawing for.</v>

00:28:02.210 --> 00:28:06.210
<v Genadi Peari>Yes, yes, includes in the revision. Yes.</v>

00:28:03.850 --> 00:28:17.490
<v Val Levitan>So, that's what, yes, and if there are revision, then it gets substituted into revision and pick it up the flat list with continuous revisions with continuous.</v>

00:28:18.690 --> 00:28:33.010
<v Val Levitan>changes needs to be kept in Github. So we know now Github, whether it's supplied by you, supplied by a third party, designed by you, is kept, a flat list is kept in Github.</v>

00:28:34.210 --> 00:28:34.770
<v Genadi Peari>Great.</v>

00:28:35.650 --> 00:28:49.410
<v Val Levitan>We now know that financial information, data, money transfer, anything that has to do with a particular vendor that you have personally selected and approved.</v>

00:28:51.570 --> 00:28:52.210
<v Genadi Peari>Understood.</v>

00:28:53.570 --> 00:28:55.890
<v Val Levitan>Is kept in Msbc.</v>

00:28:57.570 --> 00:29:05.170
<v Val Levitan>And all the financial information to this particular or to these vendors are isolated.</v>

00:29:06.530 --> 00:29:27.570
<v Val Levitan>You never know that financial information. You have no effect on that financial information. Just like administration has no effect on what drawings are included in there. There is a clear separation, clear border, non-penetrable border,</v>

00:29:27.690 --> 00:29:47.570
<v Val Levitan>between engineering and administration, and they're located under the key and lock. Nobody has right to go in either side. We need a transcriber. We need a tool that looks after the revisions all the time, flat revisions,</v>

00:29:47.610 --> 00:29:55.490
<v Val Levitan>Whatever you substitute, whatever you said changes, and it's constant. It could be hourly, it could be by minute, I don't know what it is.</v>

00:29:56.610 --> 00:30:08.050
<v Val Levitan>And then it imports that in the form that is required by Msbc to structure a functioning bill of material.</v>

00:30:11.090 --> 00:30:14.770
<v Val Levitan>And what we're discussing here is that exact tool.</v>

00:30:15.850 --> 00:30:27.650
<v Val Levitan>So the location for these, for the flood list is identified. If it's 1000 locations, it doesn't matter. You could scan all these 1000 locations.</v>

00:30:29.730 --> 00:30:36.850
<v Val Levitan>We also know exactly how a bill of material must look. We know what the final result is.</v>

00:30:41.330 --> 00:30:46.690
<v Val Levitan>Now, let's discuss the tool. I don't know how to make that porting.</v>

00:30:47.850 --> 00:30:49.410
<v Val Levitan>This is where it may be.</v>

00:30:50.370 --> 00:31:09.570
<v Val Levitan>Nathan needs to cast his opinion. This is the standard that he wants the flat pieces in, because, and he, there should probably, I assume, there should, and this is an assumption, there should probably be a standard how a bill of material is formed. Maybe, I don't know.</v>

00:31:19.890 --> 00:31:21.970
<v Val Levitan>Maybe the word should be given to Nathan now.</v>

00:31:22.290 --> 00:31:22.450
<v Nathan Carver>Yeah.</v>

00:31:32.850 --> 00:31:33.490
<v Nathan Carver>Sam.</v>

00:31:34.730 --> 00:31:39.010
<v Nathan Carver>I think experimenting with what we what can be done.</v>

00:31:44.010 --> 00:31:51.250
<v Nathan Carver>What it would need is this examples or actual actual BOM structures that you're using now.</v>

00:31:52.490 --> 00:31:56.130
<v Nathan Carver>What does flat versions look like, and then...</v>

00:31:57.290 --> 00:32:05.650
<v Nathan Carver>what, and then we look at the structure within Msbc and determine what are the median steps that we have to take.</v>

00:32:06.530 --> 00:32:12.210
<v Nathan Carver>to convert that automatically, not having someone go in and enter it into Msbc.</v>

00:32:15.490 --> 00:32:18.610
<v Nathan Carver>So what that would force out is...</v>

00:32:19.650 --> 00:32:25.010
<v Nathan Carver>of our current process of building the BOM structure and files.</v>

00:32:26.130 --> 00:32:32.690
<v Nathan Carver>Is it a convention that's followed across every file? What kind of one-off cases might there be?</v>

00:32:34.170 --> 00:32:34.290
<v Nathan Carver>Um...</v>

00:32:35.410 --> 00:32:48.690
<v Nathan Carver>And so the more structured it is, the more it's following a convention or a standard for how those files are written, the easier it will be for an automated process to read them and build them into something.</v>

00:32:53.490 --> 00:33:11.130
<v Nathan Carver>So that would be my recommendation is look at what we have, try to create some examples, and we can use, we have development Msbc instances that we can use and actually start building something out in just to get an example.</v>

00:33:15.290 --> 00:33:29.490
<v Nathan Carver>But that tells us where we are. And then ideally, your workflow doesn't change much. The only thing I could see it enforcing is changing the file structure a bit. But</v>

00:33:30.850 --> 00:33:41.330
<v Nathan Carver>Or not so much changing the files, but just ensuring that everything is built consistently. So the reader, so whatever tool that's creating this conversion, this build.</v>

00:33:42.930 --> 00:33:46.290
<v Nathan Carver>to put into Business Central can read consistent data.</v>

00:33:48.210 --> 00:34:06.930
<v Nathan Carver>And it can have multiple sources, like if it has files, if it has like a database of things. As long as we identify those sources and they're structured and consistent, then we should be able to develop process automated system that can read those and build them into something for.</v>

00:34:07.170 --> 00:34:07.970
<v Nathan Carver>Business Central.</v>

00:34:11.570 --> 00:34:18.530
<v Genadi Peari>Yeah, I'm sorry, it's really hard to understand what you're saying for me because you're saying...</v>

00:34:19.570 --> 00:34:34.050
<v Genadi Peari>But what rule you will apply for converting, for transferring information to Msbc? If each bill of material is different, how you can create the rule? Each product is different.</v>

00:34:34.690 --> 00:34:36.210
<v Nathan Carver>Each product is different.</v>

00:34:35.970 --> 00:34:45.650
<v Genadi Peari>You need to keep the rule in Msbc then to pull the rule and then do the transfer. You cannot do it the other way around. I'm not saying what we're saying.</v>

00:34:46.370 --> 00:34:51.330
<v Nathan Carver>So there's a, let me make sure I understand.</v>

00:34:47.490 --> 00:34:48.850
<v Genadi Peari>I'm not following.</v>

00:34:53.090 --> 00:34:54.130
<v Nathan Carver>The rule.</v>

00:34:55.250 --> 00:35:04.250
<v Nathan Carver>And each product is different, so each BOM is different because it has a different structure of components, correct?</v>

00:34:55.450 --> 00:34:57.810
<v Genadi Peari>You need the rules to do this conversion, right?</v>

00:35:03.650 --> 00:35:08.610
<v Genadi Peari>Exactly, so how, how, how is can be automated if each bloom is different?</v>

00:35:09.250 --> 00:35:16.530
<v Nathan Carver>So building the BOM is not, that's something you do, right? And you'll keep doing that. You'll decide what goes into that.</v>

00:35:16.930 --> 00:35:33.970
<v Genadi Peari>Yeah, it's very simple to do it. Just put the new instances in the Msbc. Do we have such a, can we create such a tool in the Github similar to that? Then you will be transferred easily.</v>

00:35:34.930 --> 00:35:39.890
<v Genadi Peari>You need two structures to be similar, right? Then it's easy to synchronize.</v>

00:35:40.210 --> 00:35:43.010
<v Nathan Carver>Correct, correct. Each structure on both sides.</v>

00:35:40.690 --> 00:35:45.170
<v Genadi Peari>This is in my, like, this is what I see. I'm not sure what are you saying.</v>

00:35:46.690 --> 00:35:50.770
<v Nathan Carver>So, to have engineer, so the end, if the end goal is...</v>

00:35:52.770 --> 00:35:56.250
<v Nathan Carver>Engineers are not going to go into Msbc and enter this information.</v>

00:35:57.410 --> 00:36:03.650
<v Nathan Carver>So then we do need some way to structure a BOM outside of Msbc so it can be.</v>

00:36:05.250 --> 00:36:06.530
<v Nathan Carver>Programmatically added.</v>

00:36:09.490 --> 00:36:09.970
<v Genadi Peari>I.</v>

00:36:11.090 --> 00:36:16.130
<v Genadi Peari>Okay, I do not understand this, but if you find a way how to...</v>

00:36:17.330 --> 00:36:23.250
<v Genadi Peari>I, I really don't see the advantage here, but...</v>

00:36:24.290 --> 00:36:25.410
<v Genadi Peari>Maybe I don't understand.</v>

00:36:27.490 --> 00:36:35.890
<v Nathan Carver>So we could run experiments with what we have. So take an existing BOM and Msbc.</v>

00:36:33.330 --> 00:36:33.810
<v Genadi Peari>Sure.</v>

00:36:37.490 --> 00:36:44.850
<v Nathan Carver>trace it back to all of its items and come up with a way, okay, what would this BOM look like in Github?</v>

00:36:46.530 --> 00:36:47.050
<v Nathan Carver>And.</v>

00:36:46.610 --> 00:36:49.810
<v Genadi Peari>And how conveniently maintain it in the Github?</v>

00:36:50.850 --> 00:36:54.610
<v Nathan Carver>Right. So how do we make it maintainable?</v>

00:36:57.930 --> 00:36:59.810
<v Nathan Carver>And not just add complexity.</v>

00:37:08.290 --> 00:37:09.330
<v Genadi Peari>I would go with...</v>

00:37:11.410 --> 00:37:17.090
<v Genadi Peari>Few iterations. We'll start with the database to keep in Github.</v>

00:37:18.370 --> 00:37:25.010
<v Genadi Peari>And then, next step would be to deal with all the bill of materials, because...</v>

00:37:30.130 --> 00:37:36.050
<v Genadi Peari>Maybe I don't see it, but for me to keep bill of material in the in the Msbc, it's very...</v>

00:37:37.650 --> 00:37:39.570
<v Genadi Peari>This is how it should be, but...</v>

00:37:41.010 --> 00:37:42.450
<v Genadi Peari>And it's easy to maintain.</v>

00:37:43.570 --> 00:37:50.530
<v Nathan Carver>So start with just maintaining items and updating those first before going into bill of materials.</v>

00:37:43.810 --> 00:37:44.530
<v Genadi Peari>Three.</v>

00:37:58.690 --> 00:38:07.650
<v Nathan Carver>So I can do that. I can experiment in phases and figure out what we can and can't do, what it might look like.</v>

00:38:09.330 --> 00:38:11.170
<v Nathan Carver>to maintain that in Github.</v>

00:38:12.690 --> 00:38:14.290
<v Lev Rudky>Just keep in mind.</v>

00:38:15.570 --> 00:38:18.610
<v Lev Rudky>Outside what we discussed right now.</v>

00:38:20.050 --> 00:38:23.490
<v Lev Rudky>If the source of a new part number.</v>

00:38:24.690 --> 00:38:25.930
<v Lev Rudky>He is in Github.</v>

00:38:28.290 --> 00:38:35.330
<v Lev Rudky>And it automatically gets created in BC afterwards.</v>

00:38:37.090 --> 00:38:45.890
<v Lev Rudky>So you need to populate there more than engineering parameters in order to create a part number.</v>

00:38:46.930 --> 00:39:00.210
<v Lev Rudky>in BC. It's all kinds of BC classifications associated with the part number, which has nothing to do with engineering. It's various posting groups, things like that, dimensions.</v>

00:39:00.450 --> 00:39:01.650
<v Genadi Peari>Serialized.</v>

00:39:02.850 --> 00:39:05.770
<v Nathan Carver>So that's accounting, entering that information.</v>

00:39:02.930 --> 00:39:03.410
<v Lev Rudky>Jira.</v>

00:39:06.650 --> 00:39:08.290
<v Lev Rudky>So, basically, they will do.</v>

00:39:09.370 --> 00:39:12.130
<v Lev Rudky>Two sources of input.</v>

00:39:13.410 --> 00:39:16.970
<v Lev Rudky>for a specific new part number.</v>

00:39:20.610 --> 00:39:23.690
<v Lev Rudky>One, one by engineers.</v>

00:39:24.850 --> 00:39:27.370
<v Lev Rudky>In London for somebody else, correct?</v>

00:39:30.690 --> 00:39:32.930
<v Genadi Peari>Well, you unmuted, you muted.</v>

00:39:35.250 --> 00:39:37.170
<v Val Levitan>Nothing changes, it's still the same.</v>

00:39:38.290 --> 00:39:43.170
<v Val Levitan>Today, we require two or three people participating in.</v>

00:39:45.250 --> 00:39:46.930
<v Val Levitan>Creating a proper.</v>

00:39:48.930 --> 00:39:50.370
<v Val Levitan>Part number in BC.</v>

00:39:56.210 --> 00:39:59.010
<v Val Levitan>Except we do it part by part manually.</v>

00:40:07.410 --> 00:40:13.010
<v Val Levitan>We need to we need to create highly confidential banking information.</v>

00:40:18.650 --> 00:40:19.570
<v Val Levitan>For a vendor.</v>

00:40:22.210 --> 00:40:26.610
<v Val Levitan>Less confidential, general information, the address.</v>

00:40:27.690 --> 00:40:31.330
<v Val Levitan>Contact names, phone numbers for a vendor.</v>

00:40:34.930 --> 00:40:37.810
<v Val Levitan>Terms, payment terms.</v>

00:40:35.410 --> 00:40:35.730
<v Lev Rudky>Me.</v>

00:40:37.090 --> 00:40:37.330
<v Lev Rudky>No.</v>

00:40:38.530 --> 00:40:48.050
<v Lev Rudky>Not talking about vendors or manufacturers, so talking strictly about part number as a stand-alone entity.</v>

00:40:53.410 --> 00:40:54.690
<v Val Levitan>Explain that.</v>

00:40:56.290 --> 00:40:57.330
<v Val Levitan>Not understandable.</v>

00:40:56.370 --> 00:41:02.850
<v Lev Rudky>One part when OK right now when Genadi creates a part numbers.</v>

00:41:03.930 --> 00:41:19.970
<v Lev Rudky>part number, a new part number in Msbc, he enters additional information that is not strictly engineering information. Things like Dimensions.</v>

00:41:23.810 --> 00:41:27.330
<v Lev Rudky>Type of inventory in simple language.</v>

00:41:28.770 --> 00:41:41.250
<v Lev Rudky>And there are more. When there is a separate animal, but non-engineering information associated with item.</v>

00:41:42.850 --> 00:41:43.570
<v Lev Rudky>And.</v>

00:41:44.930 --> 00:41:46.690
<v Lev Rudky>For example, if we...</v>

00:41:48.450 --> 00:41:57.570
<v Lev Rudky>Maybe it's a bad example. If there is, for example, a new unit of measure for some part, it has to be initialized.</v>

00:41:58.610 --> 00:42:02.610
<v Lev Rudky>in the system and has to be accommodated during transfer as well.</v>

00:42:03.650 --> 00:42:14.530
<v Lev Rudky>But it's probably a good idea to experiment with to see how this concept works, because there are...</v>

00:42:05.410 --> 00:42:06.370
<v Val Levitan>This is slim.</v>

00:42:16.130 --> 00:42:17.090
<v Lev Rudky>There are.</v>

00:42:19.090 --> 00:42:21.250
<v Lev Rudky>some unanswered questions there.</v>

00:42:22.770 --> 00:42:29.650
<v Lev Rudky>I understand it on high level, but in terms of getting into practical implementation.</v>

00:42:31.890 --> 00:42:33.170
<v Lev Rudky>There might be issues.</v>

00:42:41.570 --> 00:42:45.490
<v Nathan Carver>Yeah, I think this will take some experimenting and discovery.</v>

00:42:49.530 --> 00:42:49.850
<v Nathan Carver>And.</v>

00:42:54.170 --> 00:42:57.730
<v Nathan Carver>And that would be down into the items, the workflow to.</v>

00:42:58.930 --> 00:43:11.250
<v Nathan Carver>create items, sync items, how we get them into Msbc and how, because like you said, we have to map all the account codes to that item, all the other outside of engineering work.</v>

00:43:14.050 --> 00:43:26.050
<v Genadi Peari>Maybe we should check our best practices before we start the deep investigation. How people, we don't want to be first in this investigation.</v>

00:43:32.690 --> 00:43:43.250
<v Nathan Carver>Yeah, I agree with that. I think if we know, if I know especially, is build out some experiments, how are people entering this into Msbc? What are examples I can use?</v>

00:43:44.490 --> 00:43:44.690
<v Nathan Carver>Um...</v>

00:43:47.170 --> 00:43:48.530
<v Nathan Carver>to get an understanding of that.</v>

00:43:50.290 --> 00:43:56.210
<v Nathan Carver>That's exactly what we need. What's the artifact in Msbc? How do we get it in there? And then...</v>

00:43:57.410 --> 00:44:10.690
<v Nathan Carver>What will that look like in Github? And what are we doing in Github? And then once we have clarity on both ends, the input, the output, we can start to build that automated bridge between them.</v>

00:43:58.050 --> 00:43:58.450
<v Val Levitan>Ai.</v>

00:44:19.410 --> 00:44:19.810
<v Val Levitan>Wow.</v>

00:44:20.890 --> 00:44:24.970
<v Val Levitan>Okay, give me, give Mandy the.</v>

00:44:27.970 --> 00:44:36.450
<v Val Levitan>How do you get from your design tool to a bill of material, to a flat bill of material?</v>

00:44:40.610 --> 00:44:44.290
<v Genadi Peari>Design tool, it doesn't give me.</v>

00:44:45.890 --> 00:44:55.250
<v Genadi Peari>the bill of material. It gives me, it's a tool to design mechanical and PC boards mechanically.</v>

00:44:57.890 --> 00:45:08.050
<v Genadi Peari>I do not have in the SolidWorks source of all fasteners, all the tapes, locks, wires.</v>

00:45:09.490 --> 00:45:21.170
<v Genadi Peari>I have strictly mechanical make parts make, which is what we're doing by our by design, not of the shelf.</v>

00:45:22.530 --> 00:45:30.050
<v Genadi Peari>Let's say over the shelf parts we do not or we do not I do not keep it otherwise it's very heavy and like</v>

00:45:31.130 --> 00:45:33.170
<v Genadi Peari>A lot of configurations and.</v>

00:45:35.090 --> 00:45:39.010
<v Genadi Peari>I mean, then I need the twice work to do.</v>

00:45:41.090 --> 00:45:53.810
<v Genadi Peari>It's much easier for twice work. I need a powerful computer than to handle all this bulk information. It's much easier.</v>

00:45:41.210 --> 00:45:43.730
<v Val Levitan>You need what? You need what? I'm sorry.</v>

00:45:52.690 --> 00:45:53.970
<v Val Levitan>Yeah, come out, come out.</v>

00:45:54.930 --> 00:46:06.050
<v Genadi Peari>Much easier what I do, once we did the new product, I just tap in all the standard parts in the bill of material.</v>

00:46:12.090 --> 00:46:14.290
<v Val Levitan>I'm going to ask the question again.</v>

00:46:15.570 --> 00:46:17.890
<v Val Levitan>Can I, can I understand?</v>

00:46:18.930 --> 00:46:29.890
<v Val Levitan>How you arrive to a bill of material from the design from mechanical design for those parts that you design in SolidWork?</v>

00:46:27.810 --> 00:46:27.970
<v Nathan Carver>Yeah.</v>

00:46:33.890 --> 00:46:40.290
<v Genadi Peari>Whatever I have in SolidWorks, when I do a new part, I already assigned the number.</v>

00:46:41.810 --> 00:46:43.650
<v Genadi Peari>It's already have the number.</v>

00:46:45.850 --> 00:46:52.610
<v Genadi Peari>Then, when I enter it after the project is done, manually enter this number.</v>

00:46:54.850 --> 00:46:55.970
<v Genadi Peari>In Msbc.</v>

00:46:58.050 --> 00:47:03.730
<v Genadi Peari>If it's not part of the design, just under part, like, I don't know, washer.</v>

00:47:05.330 --> 00:47:13.970
<v Genadi Peari>And I know we need 6 washers. Just put in the Msbc, I add the instance. This part number multiply 6.</v>

00:47:17.170 --> 00:47:20.850
<v Genadi Peari>It's not during the design, it's during the building bill of material.</v>

00:47:23.690 --> 00:47:26.210
<v Val Levitan>I don't know, we can play this game for as long as you want.</v>

00:47:27.170 --> 00:47:28.530
<v Val Levitan>I need to understand.</v>

00:47:30.770 --> 00:47:32.530
<v Val Levitan>Or maybe you could show it to me.</v>

00:47:33.330 --> 00:47:41.730
<v Val Levitan>for those parts that you design mechanically. You know what, I actually, I want to change the format. I think this meeting is not productive.</v>

00:47:43.010 --> 00:47:43.650
<v Val Levitan>Um...</v>

00:47:44.930 --> 00:47:51.410
<v Val Levitan>I need to let Lev and Nathan go because I'm just burning their hours.</v>

00:47:52.930 --> 00:47:55.970
<v Val Levitan>And I will switch to a different meeting with Genadi.</v>

00:48:00.450 --> 00:48:01.810
<v Nathan Carver>Okay, sounds good.</v>

00:48:01.650 --> 00:48:09.250
<v Val Levitan>Thank you. Thank you, guys. I'm going to collapse this meeting. I'm going to invite Genadi to the different meeting. Thank you. Bye bye.</v>

00:48:03.170 --> 00:48:04.130
<v Lev Rudky>Thank you.</v>

