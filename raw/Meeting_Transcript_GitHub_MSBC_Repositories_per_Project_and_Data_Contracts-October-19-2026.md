# Raw Transcript — GitHub-MSBC integration and supplier migration – Val, Genadi, Nathan
**Date:** October 19, 2026, 5:02 PM – 5:36 PM Eastern (Segment 1 of 2)
**Summary note:** [[Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026]]
---
WEBVTT

00:00:12.679 --> 00:00:13.399
<v Genadi Peari>Hello there.</v>

00:00:15.319 --> 00:00:15.919
<v Val Levitan>Hello!</v>

00:00:16.999 --> 00:00:17.559
<v Genadi Peari>Rovo.</v>

00:00:18.559 --> 00:00:19.559
<v Val Levitan>Hello, Genadi.</v>

00:00:26.799 --> 00:00:27.439
<v Nathan Carver>Hello.</v>

00:00:28.559 --> 00:00:29.279
<v Val Levitan>Hello.</v>

00:00:31.639 --> 00:00:32.279
<v Genadi Peari>Anything.</v>

00:00:34.639 --> 00:00:39.599
<v Val Levitan>I am looking for an alignment on the subjects.</v>

00:00:40.719 --> 00:00:42.959
<v Val Levitan>Of Github, Microsoft.</v>

00:00:45.039 --> 00:00:46.319
<v Val Levitan>Business Central.</v>

00:00:48.399 --> 00:00:49.519
<v Val Levitan>functionality.</v>

00:00:51.839 --> 00:00:53.919
<v Val Levitan>I have outlined.</v>

00:00:56.399 --> 00:00:58.719
<v Val Levitan>My views on the architecture.</v>

00:01:00.159 --> 00:01:08.639
<v Val Levitan>I'm pretty firm on it, but I understand that number one, I'm not an engineer. Number 2, I admit I don't have any experience in it.</v>

00:01:09.999 --> 00:01:14.719
<v Val Levitan>And so I'd like to hear reservations, issues.</v>

00:01:17.359 --> 00:01:20.399
<v Val Levitan>I am trying to bring the three of us together on this.</v>

00:01:19.839 --> 00:01:19.959
<v Nathan Carver>Yeah.</v>

00:01:21.759 --> 00:01:25.759
<v Val Levitan>It is relatively pointless for me to repeat again.</v>

00:01:26.519 --> 00:01:32.799
<v Val Levitan>what my thoughts are. I can do it, but I think we didn't come here to listen.</v>

00:01:34.479 --> 00:01:41.759
<v Val Levitan>to listen to me talk about it again. But I need an alignment and I need...</v>

00:01:43.199 --> 00:01:50.959
<v Val Levitan>To move forward, and I need to achieve results, and we are functioning in a relatively tight space.</v>

00:01:51.919 --> 00:01:55.679
<v Val Levitan>Honestly speaking, we have about 45 days left in this year.</v>

00:01:57.679 --> 00:02:00.959
<v Val Levitan>And so, a lot of work to be done.</v>

00:02:02.039 --> 00:02:12.319
<v Val Levitan>Especially, we're being pressured right now because Michael will be leaving, and Mary is not able to.</v>

00:02:14.639 --> 00:02:16.319
<v Val Levitan>Pick up from where Michael.</v>

00:02:19.839 --> 00:02:23.119
<v Val Levitan>How Michael worked? Michael worked on his own.</v>

00:02:26.479 --> 00:02:27.599
<v Val Levitan>30 year.</v>

00:02:30.719 --> 00:02:31.759
<v Val Levitan>framework.</v>

00:02:32.639 --> 00:02:42.399
<v Val Levitan>This is how he thought, this is how he made decisions. There were certain reports that he were relying on. Mary cannot work off of the same format.</v>

00:02:44.559 --> 00:02:47.359
<v Val Levitan>I don't have time to bring somebody else on board.</v>

00:02:48.479 --> 00:02:54.399
<v Val Levitan>We need purchasing, and I cannot allow Genadi spend time on purchasing.</v>

00:02:55.599 --> 00:02:59.439
<v Val Levitan>But I do believe that the system, the architecture of the system that I...</v>

00:03:02.239 --> 00:03:02.799
<v Val Levitan>Ohh.</v>

00:03:03.679 --> 00:03:06.079
<v Val Levitan>Presented to you, it should work for Mery.</v>

00:03:12.799 --> 00:03:13.319
<v Nathan Carver>And.</v>

00:03:15.599 --> 00:03:17.039
<v Nathan Carver>Yes, I agree.</v>

00:03:17.399 --> 00:03:36.199
<v Genadi Peari>There are a few things that need to be done in parallel, I think. This is how I see it. The one of the subjects that more related to myself is to organize all the data about the products and</v>

00:03:37.559 --> 00:03:44.519
<v Genadi Peari>components in the Github. And this I need just to be, I'm ready to.</v>

00:03:45.639 --> 00:03:54.599
<v Genadi Peari>finalize and everything I just need to again to confirm the structure of the repositories because</v>

00:03:55.479 --> 00:03:58.039
<v Genadi Peari>We have rules now in the Github.</v>

00:03:59.119 --> 00:04:17.999
<v Genadi Peari>And if we follow these rules or other rules, I need Nathan to confirm how do we build, how do we do tags, how we do this, organize the read me files. So all the information will be available right away to the, to pull it.</v>

00:04:18.119 --> 00:04:27.159
<v Genadi Peari>Right, so you want, you will not have any issues. We need detailed discussion how you see all the structure.</v>

00:04:28.319 --> 00:04:30.279
<v Genadi Peari>So we can organize the repositories.</v>

00:04:32.279 --> 00:04:32.639
<v Nathan Carver>Okay.</v>

00:04:32.919 --> 00:04:35.439
<v Genadi Peari>Of course, we can maybe reshuffle in the...</v>

00:04:34.079 --> 00:04:39.519
<v Val Levitan>The repositories, the repositories, we have a standard how to organize them.</v>

00:04:39.799 --> 00:04:49.159
<v Genadi Peari>Yeah, it's in the Github right now. But not only that, how he access the data, right? The tags, how the organization of the tags works.</v>

00:04:50.159 --> 00:04:50.879
<v Val Levitan>Of what?</v>

00:04:50.359 --> 00:04:51.319
<v Genadi Peari>And the rip.</v>

00:04:52.759 --> 00:04:59.159
<v Genadi Peari>How you access each component? Through what? Through the part number, where it's stored, how it's stored.</v>

00:04:53.279 --> 00:04:53.839
<v Val Levitan>Of the.</v>

00:04:55.759 --> 00:04:56.079
<v Nathan Carver>Okay.</v>

00:05:00.999 --> 00:05:10.319
<v Nathan Carver>Okay, okay. So for me, you need for me that structure so you can start adding the information to Github.</v>

00:05:10.479 --> 00:05:10.879
<v Val Levitan>Okay.</v>

00:05:10.759 --> 00:05:17.159
<v Genadi Peari>I already doing this, but we need to review if everything is good, if it's acceptable for you.</v>

00:05:15.439 --> 00:05:16.639
<v Val Levitan>Hold on, which?</v>

00:05:18.159 --> 00:05:31.839
<v Val Levitan>I don't understand which structure, I apologize. The structure of Github repository per vendor is not structured, it's freestyled.</v>

00:05:33.439 --> 00:05:38.399
<v Val Levitan>You put as much information into that repository as possible.</v>

00:05:39.999 --> 00:05:40.639
<v Val Levitan>Pro.</v>

00:05:41.919 --> 00:05:42.639
<v Val Levitan>Ohh.</v>

00:05:44.399 --> 00:05:48.479
<v Val Levitan>per category. By category I mean per project.</v>

00:05:53.039 --> 00:05:55.199
<v Val Levitan>So, let's say all of the monitors.</v>

00:05:58.079 --> 00:05:58.559
<v Val Levitan>Uh...</v>

00:05:59.759 --> 00:06:01.439
<v Val Levitan>are in the same repository.</v>

00:06:05.519 --> 00:06:14.559
<v Val Levitan>Correct me if I'm wrong, that's how I see it. I do not envision a structure, because the moment you start defining structure,</v>

00:06:15.759 --> 00:06:22.079
<v Val Levitan>Within the repository, meaning tables, that's what you're saying? Tables? I don't see it.</v>

00:06:23.359 --> 00:06:26.479
<v Val Levitan>I see, I I see a lot of data sheets.</v>

00:06:28.479 --> 00:06:33.839
<v Val Levitan>Drawings from supplier, data sheets and drawings from suppliers.</v>

00:06:34.959 --> 00:06:36.239
<v Val Levitan>Various suppliers.</v>

00:06:42.119 --> 00:06:51.879
<v Genadi Peari>So, you create repository for each category, it might be like a few, I mean, 30, 40 repositories.</v>

00:06:50.559 --> 00:06:56.799
<v Val Levitan>I sent, I sent, I sent the table, I sent the table, there was a table, I sent the table that listed.</v>

00:06:58.159 --> 00:06:59.679
<v Val Levitan>Every single Project.</v>

00:07:00.799 --> 00:07:02.879
<v Val Levitan>Come on, we're starting again from this.</v>

00:07:07.039 --> 00:07:08.839
<v Nathan Carver>Hold on, let me just find your e-mail then.</v>

00:07:10.759 --> 00:07:11.079
<v Genadi Peari>Um...</v>

00:07:12.359 --> 00:07:16.919
<v Genadi Peari>All right, now is the rules in the Github a bit different.</v>

00:07:18.119 --> 00:07:19.559
<v Genadi Peari>So, we need to change them.</v>

00:07:22.399 --> 00:07:26.719
<v Val Levitan>Well, maybe I don't understand rules, I just, I don't understand how they're different.</v>

00:07:27.959 --> 00:07:33.719
<v Genadi Peari>Ohh, we have a hard repository standard, and and and this says exactly how.</v>

00:07:32.959 --> 00:07:39.679
<v Val Levitan>We don't have hardware repository standard. We have repository standard. There's no hardware repository standard.</v>

00:07:46.519 --> 00:07:50.279
<v Genadi Peari>I just read what it is in Github.</v>

00:08:03.519 --> 00:08:04.559
<v Nathan Carver>OK, so.</v>

00:08:07.439 --> 00:08:09.039
<v Nathan Carver>From, and I'm still getting.</v>

00:08:08.079 --> 00:08:18.319
<v Val Levitan>Repository is a collection of either technical joins or technical documentation or data sheets.</v>

00:08:21.639 --> 00:08:23.599
<v Val Levitan>Each repository is...</v>

00:08:25.199 --> 00:08:28.399
<v Val Levitan>Equal to a Project.</v>

00:08:38.879 --> 00:08:39.439
<v Nathan Carver>Okay.</v>

00:09:00.639 --> 00:09:05.679
<v Nathan Carver>Forgive me, I'm still getting caught up from last week and I intend to...</v>

00:09:06.639 --> 00:09:09.999
<v Nathan Carver>Break down our conversation from when we left, but we have.</v>

00:09:11.039 --> 00:09:11.839
<v Nathan Carver>The spike.</v>

00:09:12.919 --> 00:09:16.399
<v Nathan Carver>That we did, and the idea was to organize.</v>

00:09:18.319 --> 00:09:28.799
<v Nathan Carver>components, however we structure that into various repositories and then pull those. So I think what I'm hearing is Genadi is asking like.</v>

00:09:23.079 --> 00:09:25.079
<v Val Levitan>Correct, correct, correct.</v>

00:09:29.879 --> 00:09:37.919
<v Nathan Carver>What are those? Do we need to create them? And then within there, there's a specific file structure that has to be followed.</v>

00:09:39.519 --> 00:09:43.599
<v Nathan Carver>Or at least agreed upon, and that still is.</v>

00:09:44.719 --> 00:09:49.679
<v Nathan Carver>We need to form that, because once that file structure is agreed upon, then...</v>

00:09:49.679 --> 00:09:59.799
<v Val Levitan>But what file, what file structure? We talked about that repository is a collection of information for each particular.</v>

00:09:58.439 --> 00:09:58.879
<v Nathan Carver>Correct.</v>

00:10:00.199 --> 00:10:00.919
<v Val Levitan>Ohh.</v>

00:10:02.919 --> 00:10:10.119
<v Val Levitan>project. A project, for example, the best, the easiest way to talk about, let's say monitors or touch screens.</v>

00:10:04.199 --> 00:10:04.519
<v Nathan Carver>Yeah.</v>

00:10:10.839 --> 00:10:11.159
<v Nathan Carver>Right.</v>

00:10:11.279 --> 00:10:15.879
<v Val Levitan>So touch screen is a project of its own, its repository of its own.</v>

00:10:17.159 --> 00:10:38.559
<v Val Levitan>Monitors is a project of its own in Jira, repository of its own in Github. So all monitors, every single monitor, we don't produce any of the monitors. We buy them. And we identify one, two, 5 suppliers of the monitors. And these suppliers could have various sizes of monitors, various</v>

00:10:40.359 --> 00:10:54.119
<v Val Levitan>technical specification. For each of those monitors, we have now, we have, otherwise we cannot build a machine, we have complete data sheet, and we have drawings for it.</v>

00:10:55.159 --> 00:11:05.239
<v Val Levitan>Either drawings supplied by the supplier or drawings that Genadi was forced to produce, because maybe a supplier didn't produce the specific drawings.</v>

00:11:06.439 --> 00:11:26.639
<v Val Levitan>So anything that Genadi gets from a supplier or produces for a particular subject needs to be put in that repository. So repository is not organized. It's a collection of various things. It's an informational, it's a collection gathering thing.</v>

00:11:27.839 --> 00:11:35.879
<v Val Levitan>Just like code, you don't you don't know what what code developer will write. It's a it's a collection of.</v>

00:11:37.319 --> 00:11:38.279
<v Val Levitan>A bunch of...</v>

00:11:39.959 --> 00:11:41.079
<v Val Levitan>Java.</v>

00:11:42.679 --> 00:11:46.599
<v Val Levitan>you know, blubber as far as I'm concerned. To me, it's meaningless.</v>

00:11:48.679 --> 00:12:03.079
<v Val Levitan>There is no structure to it, but what the repository does have, and if I understand it correctly, it could work here as well. The developers repository has the Prose and it has data contracts.</v>

00:12:05.959 --> 00:12:10.039
<v Val Levitan>which is similarly to what I'm suggesting implementing here.</v>

00:12:12.199 --> 00:12:14.839
<v Val Levitan>Prose and data contract.</v>

00:12:16.039 --> 00:12:17.479
<v Val Levitan>Will allow.</v>

00:12:19.719 --> 00:12:20.519
<v Val Levitan>Ohh.</v>

00:12:24.519 --> 00:12:25.079
<v Val Levitan>Um...</v>

00:12:26.159 --> 00:12:31.959
<v Val Levitan>Nathan to create, number one, bill of material.</v>

00:12:33.839 --> 00:12:38.439
<v Val Levitan>which I understand will be created by Github actions.</v>

00:12:42.199 --> 00:12:49.839
<v Val Levitan>And it will allow us to create various assortment of bill of materials because we now have data contracts.</v>

00:12:53.479 --> 00:12:54.039
<v Nathan Carver>Correct.</v>

00:12:53.799 --> 00:12:59.799
<v Val Levitan>That's my assumption. I am assuming things. I have never done it before.</v>

00:13:00.599 --> 00:13:17.639
<v Val Levitan>But to me, it makes sense. I do not envision, I cannot understand, structure of a repository, a table. And I know that Genadi likes to think of tables, but let's discuss it again. We are...</v>

00:13:19.959 --> 00:13:30.439
<v Val Levitan>subcontracting, we're pushing the logic of whatever logic substance we need onto an AI.</v>

00:13:33.239 --> 00:13:39.719
<v Val Levitan>So the harness, the logical harness of how everything comes together will come from an AI.</v>

00:13:43.039 --> 00:13:49.159
<v Val Levitan>But how does AI know what we need? It knows it through data contract and through Prose.</v>

00:13:50.639 --> 00:14:01.079
<v Val Levitan>which resides in each individual repository. That's how it works right now. Today, it works right now with the developers of code.</v>

00:14:02.279 --> 00:14:03.799
<v Val Levitan>Code is a bunch of.</v>

00:14:05.079 --> 00:14:06.199
<v Val Levitan>Unpredictable.</v>

00:14:08.439 --> 00:14:11.799
<v Val Levitan>Not structured things, lines.</v>

00:14:15.479 --> 00:14:19.079
<v Val Levitan>But it's defined through Prose and data contracts.</v>

00:14:21.479 --> 00:14:22.679
<v Val Levitan>Github Action.</v>

00:14:26.999 --> 00:14:29.959
<v Val Levitan>Collects all of it into a release.</v>

00:14:32.359 --> 00:14:35.079
<v Val Levitan>So, a release to me is a bill of material.</v>

00:14:36.119 --> 00:14:37.239
<v Val Levitan>That's the end result.</v>

00:14:41.319 --> 00:14:58.599
<v Genadi Peari>So when you're saying repository equals project, it means all the harnesses for all different products in the same repository and all the metal, whatever it is, for all the products in the same repository.</v>

00:14:51.639 --> 00:14:53.119
<v Val Levitan>Yes, because the project.</v>

00:14:59.159 --> 00:14:59.719
<v Val Levitan>Yes.</v>

00:15:00.039 --> 00:15:03.639
<v Genadi Peari>So, we need to create like a lot of repositories, first of all.</v>

00:15:04.359 --> 00:15:05.159
<v Val Levitan>Thirteen.</v>

00:15:06.599 --> 00:15:08.519
<v Genadi Peari>Sorry, was it the...</v>

00:15:07.639 --> 00:15:07.799
<v Nathan Carver>Yeah.</v>

00:15:08.999 --> 00:15:12.759
<v Val Levitan>13, 13 repositories, I created a table.</v>

00:15:10.119 --> 00:15:10.679
<v Genadi Peari>This.</v>

00:15:13.159 --> 00:15:16.759
<v Genadi Peari>This table you sent by e-mail or because I was...</v>

00:15:17.959 --> 00:15:20.599
<v Genadi Peari>How did you send it to us? Sorry, I'm...</v>

00:15:21.719 --> 00:15:24.359
<v Genadi Peari>I'm, I'm, I know you posted it.</v>

00:15:25.399 --> 00:15:26.679
<v Genadi Peari>And somehow I cannot.</v>

00:15:27.879 --> 00:15:30.759
<v Genadi Peari>I spent, I was looking for it today.</v>

00:15:35.719 --> 00:15:36.199
<v Genadi Peari>Ohh.</v>

00:15:42.999 --> 00:15:43.159
<v Nathan Carver>Yeah.</v>

00:15:43.079 --> 00:15:46.759
<v Genadi Peari>So, Nathan, we go with these repositories, but...</v>

00:15:49.639 --> 00:15:56.199
<v Genadi Peari>But I need to to understand if you need anything else to find the to to when when you do.</v>

00:15:57.399 --> 00:16:02.679
<v Genadi Peari>Pull parts from Github to Msbc - how, how based on what?</v>

00:15:58.479 --> 00:15:58.679
<v Nathan Carver>What?</v>

00:16:03.879 --> 00:16:05.719
<v Genadi Peari>Um, talk, right?</v>

00:16:07.159 --> 00:16:14.199
<v Nathan Carver>Correct, so each reach repository will have contracts in defining, so.</v>

00:16:11.639 --> 00:16:12.039
<v Genadi Peari>Okay.</v>

00:16:15.399 --> 00:16:18.839
<v Nathan Carver>Within that repository, it will have a specific.</v>

00:16:19.919 --> 00:16:27.279
<v Nathan Carver>File structure for placing those contracts, and that's what we need to agree on, and then that way the...</v>

00:16:23.799 --> 00:16:24.199
<v Genadi Peari>Okay.</v>

00:16:29.159 --> 00:16:34.599
<v Nathan Carver>The scripts and the agent can read from that file structure of each repo.</v>

00:16:36.199 --> 00:16:37.799
<v Genadi Peari>Okay, so...</v>

00:16:36.359 --> 00:16:36.759
<v Nathan Carver>Ohh.</v>

00:16:37.079 --> 00:16:43.639
<v Val Levitan>And you can, it seems like Genadi, I cannot explain it, but I know that it works.</v>

00:16:44.839 --> 00:16:51.959
<v Val Levitan>Genadi seems to want to get to the bottom of it. Can you, Nathan, perhaps go into deeper...</v>

00:16:55.879 --> 00:17:14.599
<v Val Levitan>Description of what, how, what, what is the data contract? How are you going to write your Github auctions? Because you probably understand that, but can you explain it to Genadi and vicariously to me as well, because I kind of heard about it.</v>

00:17:15.159 --> 00:17:19.399
<v Val Levitan>I can use the, I can talk about it, but I cannot explain it.</v>

00:17:21.559 --> 00:17:28.119
<v Genadi Peari>So I'll start doing this and actually show one example so we can run all the...</v>

00:17:22.039 --> 00:17:22.239
<v Nathan Carver>No.</v>

00:17:30.039 --> 00:17:31.319
<v Genadi Peari>You can do it tomorrow.</v>

00:17:30.279 --> 00:17:37.079
<v Val Levitan>To me, I can explain to you, to me, data contract is a description of what...</v>

00:17:38.199 --> 00:17:39.239
<v Val Levitan>A particular.</v>

00:17:41.079 --> 00:17:48.599
<v Val Levitan>Let's say monitor can output what, sorry, not output, what it can offer.</v>

00:17:43.399 --> 00:17:43.559
<v Nathan Carver>Blue.</v>

00:17:50.199 --> 00:17:53.959
<v Val Levitan>to the machine, to the entire product, what it can offer.</v>

00:17:57.239 --> 00:18:00.199
<v Val Levitan>I might be wrong on this. I'm making **** up.</v>

00:18:00.839 --> 00:18:03.559
<v Nathan Carver>Yeah, so the spike we did.</v>

00:18:05.319 --> 00:18:06.599
<v Val Levitan>We don't see your screen.</v>

00:18:05.759 --> 00:18:05.959
<v Nathan Carver>Um...</v>

00:18:07.399 --> 00:18:08.759
<v Nathan Carver>Oh, alright, hold on.</v>

00:18:13.399 --> 00:18:14.439
<v Val Levitan>Yeah, see it now.</v>

00:18:15.559 --> 00:18:16.119
<v Nathan Carver>Is that?</v>

00:18:16.519 --> 00:18:17.079
<v Val Levitan>Yes.</v>

00:18:17.719 --> 00:18:18.199
<v Nathan Carver>Okay.</v>

00:18:19.799 --> 00:18:20.439
<v Nathan Carver>So...</v>

00:18:20.039 --> 00:18:22.039
<v Val Levitan>Can you increase the font a little bit, please?</v>

00:18:22.439 --> 00:18:22.759
<v Nathan Carver>Yep.</v>

00:18:25.479 --> 00:18:32.279
<v Nathan Carver>Now, these aren't individual repos, it's just using folders to simulate that. But these would be...</v>

00:18:25.799 --> 00:18:26.359
<v Val Levitan>Thank you.</v>

00:18:34.119 --> 00:18:39.399
<v Nathan Carver>These represent what the repositories may look like. Now, if you set a table and you have the exact one.</v>

00:18:38.759 --> 00:18:42.839
<v Val Levitan>Well, no, this is, but, but hold on, this is exactly what my table is.</v>

00:18:43.239 --> 00:18:44.119
<v Nathan Carver>Yeah, okay.</v>

00:18:45.079 --> 00:18:50.279
<v Val Levitan>So sheet metal, power supply, plastics, peripheral, money devices.</v>

00:18:45.519 --> 00:18:45.719
<v Nathan Carver>Is.</v>

00:18:51.959 --> 00:18:54.599
<v Val Levitan>Labels, harnesses, display, yeah.</v>

00:18:55.479 --> 00:18:55.879
<v Nathan Carver>Okay.</v>

00:18:56.999 --> 00:18:58.359
<v Nathan Carver>So, um...</v>

00:18:59.519 --> 00:19:03.319
<v Nathan Carver>And I think what I'm hearing from Genadi is, okay, where do I?</v>

00:19:02.919 --> 00:19:09.479
<v Val Levitan>But I'm sorry, but hold on a second. Right now, those are individual files. You need to make them into repositories.</v>

00:19:09.799 --> 00:19:11.399
<v Nathan Carver>Correct. Correct.</v>

00:19:10.759 --> 00:19:23.399
<v Val Levitan>So you need to split those into repositories. So each repository will have a readme file. It will have a Prose, a folder for Prose. It will have a folder for...</v>

00:19:14.119 --> 00:19:14.599
<v Nathan Carver>Correct.</v>

00:19:26.439 --> 00:19:28.519
<v Val Levitan>Data contract, am I correct or not?</v>

00:19:29.159 --> 00:19:33.559
<v Nathan Carver>Yes, and that's what this is showing. So if you go look at this inside, this is what...</v>

00:19:34.919 --> 00:19:37.559
<v Nathan Carver>An example of what that might look like, so...</v>

00:19:36.919 --> 00:19:39.799
<v Val Levitan>One, one second, one second, Nathan. Hold on.</v>

00:19:41.039 --> 00:19:44.119
<v Val Levitan>Genadi, I don't want you to get lost. So did you understand?</v>

00:19:44.919 --> 00:19:45.799
<v Genadi Peari>Yes, of course.</v>

00:19:46.279 --> 00:20:05.439
<v Val Levitan>So what what Nathan showed you is an incorrect collection, incorrect collection of folders within one repository. But what Nathan is saying that he will now take it each folder and treat it as individual repository.</v>

00:19:58.679 --> 00:19:59.239
<v Genadi Peari>Understand.</v>

00:20:05.839 --> 00:20:07.439
<v Genadi Peari>Yeah, this too.</v>

00:20:07.439 --> 00:20:16.479
<v Val Levitan>You understood that each repository he now he now shows you that each repository will have an ADR, it will have a contract.</v>

00:20:08.399 --> 00:20:08.959
<v Genadi Peari>Of course.</v>

00:20:18.239 --> 00:20:19.999
<v Val Levitan>But let's get into contracts now.</v>

00:20:22.719 --> 00:20:23.839
<v Nathan Carver>Okay, so.</v>

00:20:25.919 --> 00:20:30.959
<v Nathan Carver>If you go in that folder is the collection of YAML files.</v>

00:20:32.319 --> 00:20:33.839
<v Nathan Carver>And each one of these.</v>

00:20:35.519 --> 00:20:41.599
<v Nathan Carver>Will defined that component, right? The contract, this one's kind of small. Let's see if we can find a bigger one, but...</v>

00:20:44.559 --> 00:20:45.119
<v Nathan Carver>And.</v>

00:20:46.079 --> 00:20:47.999
<v Nathan Carver>So, this, this is the general idea.</v>

00:20:51.839 --> 00:21:11.759
<v Val Levitan>So, but you see, you see it's written in.md file. And imagine that general intelligence is increasing rapidly and becoming smarter and smarter. But right now it's pretty smart. It's pretty logical. It's pretty smart. And if it reads a.md file,</v>

00:20:52.479 --> 00:20:52.879
<v Nathan Carver>Yeah.</v>

00:21:11.919 --> 00:21:18.159
<v Val Levitan>it will understand that it's still, it knows that there is a process, it needs to be painted.</v>

00:21:23.039 --> 00:21:25.759
<v Nathan Carver>Correct. So this is the target.</v>

00:21:24.159 --> 00:21:32.959
<v Val Levitan>It has, look, look, it has, it has thickness. I mean, I mean, I'm reading through width. It's fully defined.</v>

00:21:33.999 --> 00:21:37.839
<v Val Levitan>That's a data contract. That's factual.</v>

00:21:39.039 --> 00:21:45.039
<v Val Levitan>So, if you put this part together with another part, and if it doesn't fit, it's not going to assemble it.</v>

00:21:50.799 --> 00:22:05.959
<v Val Levitan>And if and and the beautiful checkpoint is that if at the end it doesn't assemble, you need to find the issue with data contract, because somewhere data contract is off. What we are after is the proper data contract.</v>

00:22:11.679 --> 00:22:20.799
<v Nathan Carver>So, Genadi, you should have access to this is just on a on a branch right now, like I haven't merged this, this was just the example.</v>

00:22:21.039 --> 00:22:24.479
<v Genadi Peari>Ohh, 'cause I looking for it, I don't see it. OK.</v>

00:22:21.919 --> 00:22:22.159
<v Nathan Carver>With.</v>

00:22:24.879 --> 00:22:26.799
<v Nathan Carver>Let me, let me share it.</v>

00:22:28.079 --> 00:22:28.799
<v Nathan Carver>In this chat.</v>

00:22:32.639 --> 00:22:45.119
<v Nathan Carver>Okay, so that second link drops you at the folders that represent these repositories. And then inside each folder is</v>

00:22:46.399 --> 00:22:52.239
<v Nathan Carver>the conceptual structure of that repository and where the contracts live.</v>

00:22:53.639 --> 00:22:53.759
<v Nathan Carver>Um...</v>

00:22:55.759 --> 00:22:56.479
<v Nathan Carver>So...</v>

00:22:57.559 --> 00:23:04.239
<v Nathan Carver>If this is enough to get us going, the next step is we send this list and have these repos created for us.</v>

00:23:07.439 --> 00:23:13.919
<v Nathan Carver>To whoever, whoever can do that, I will, I can send the list or and ask for it to be recreated.</v>

00:23:17.759 --> 00:23:23.759
<v Nathan Carver>But this, the idea is this gives us an our starting point and.</v>

00:23:24.959 --> 00:23:42.119
<v Nathan Carver>I think we'll tweak it as we go, as we find changes or improvements we need to make. But I think overall, this is going to follow the contract. And then it doesn't have a Prose folder yet, but that can be added in as we go. It does have the contracts folder.</v>

00:23:41.119 --> 00:23:56.639
<v Val Levitan>Can I get Genadi get Genadi and and this is also an explanation to Genadi, but also my question to Nathan. Do I understand it correctly that we do not physically by hand write data contract?</v>

00:23:59.519 --> 00:24:01.279
<v Nathan Carver>Correct, we generate.</v>

00:23:59.759 --> 00:24:05.279
<v Val Levitan>Data contract, data contract is taken from data sheets and drawings.</v>

00:24:05.639 --> 00:24:06.159
<v Nathan Carver>Correct.</v>

00:24:06.639 --> 00:24:12.399
<v Val Levitan>And Claude is smart enough to describe it by properly reading.</v>

00:24:14.479 --> 00:24:17.679
<v Val Levitan>all these files. That's why we need the files.</v>

00:24:19.079 --> 00:24:20.399
<v Nathan Carver>Correct, so then.</v>

00:24:20.439 --> 00:24:22.479
<v Val Levitan>In order to create data contracts.</v>

00:24:23.439 --> 00:24:39.759
<v Nathan Carver>So then I'm envisioning what each of these would have is a data sheet or whatever those files are, data sheets, a folder for those that the agent can go review and then following</v>

00:24:26.839 --> 00:24:27.039
<v Val Levitan>The.</v>

00:24:41.039 --> 00:24:41.239
<v Nathan Carver>The.</v>

00:24:43.439 --> 00:24:54.319
<v Nathan Carver>There's no ADR here, but following the contract for that repository and how it should assemble them, you can use data sheets to build out these contract files and maintain them.</v>

00:24:57.519 --> 00:24:58.079
<v Nathan Carver>So.</v>

00:24:59.839 --> 00:25:14.159
<v Nathan Carver>So, Genadi, you have these data sheets and other resource files for these components. There should be a, we'll have to create a folder in each of these repos to house that information. And then</v>

00:25:17.759 --> 00:25:32.559
<v Nathan Carver>I haven't seen them, so I'm just kind of guessing how we would go about this. But essentially, this allows each repository to have its own unique instructions for its own problems that those data sheets may be solving. And then the agent can from that can build contract files.</v>

00:25:33.359 --> 00:25:44.319
<v Genadi Peari>Yes, this makes sense. Now it makes sense. Can you go back just for a second for the list of all the repositories?</v>

00:25:35.959 --> 00:25:36.239
<v Nathan Carver>Okay.</v>

00:25:46.519 --> 00:25:54.239
<v Genadi Peari>Just because we might need to adjust it, because I don't understand hardware manufacturing. What does it mean? For example.</v>

00:25:53.999 --> 00:26:04.479
<v Val Levitan>It, it, it means that it means the hardware that that you design and we manufacture specifically for ourselves.</v>

00:26:04.559 --> 00:26:14.399
<v Genadi Peari>Yes, but we already have this hardware sheet metal, hardware part sheet metal, Plastics, harnesses, so basically nothing left in there.</v>

00:26:15.199 --> 00:26:19.519
<v Val Levitan>Yes, because it's possible that the names are also incorrect. That's fine.</v>

00:26:18.719 --> 00:26:29.439
<v Genadi Peari>Yeah, yeah, yeah, we need to, yeah, review the names again, but yeah, understood. So, Nathan, you will, who is opening the repositories, yourself or Andrei?</v>

00:26:30.079 --> 00:26:30.799
<v Val Levitan>Andrei.</v>

00:26:30.959 --> 00:26:41.279
<v Genadi Peari>Andrei, OK, so we need to ask them to open 15 about 15 repositories, and and we will...</v>

00:26:39.519 --> 00:26:54.239
<v Val Levitan>Correct, and correct, and it's important, it's important we cannot neglect this. Dima at the same time opens projects. You have to have projects in order to have a repository.</v>

00:27:01.039 --> 00:27:01.439
<v Nathan Carver>Okay.</v>

00:27:03.839 --> 00:27:10.679
<v Nathan Carver>So is this, I guess, then, Genadi, Val, on your side, is this...</v>

00:27:11.679 --> 00:27:15.679
<v Nathan Carver>The final list or the list we start with, or do you want to change any of it?</v>

00:27:11.999 --> 00:27:35.079
<v Val Levitan>It's very close. It's good enough to start with. And as we get to the end of it, we will probably see what's missing or what is too much. If it's too much, we will delete it. And if it's missing, then we'll add it. But if we see that in one of the repositories, for example, there is only one item,</v>

00:27:35.759 --> 00:27:43.439
<v Val Levitan>Maybe we will move it to some other repository and rename it or combine it. I mean, we can maneuver it slightly.</v>

00:27:44.399 --> 00:27:45.439
<v Nathan Carver>Yes, okay.</v>

00:27:46.879 --> 00:27:50.319
<v Val Levitan>But overall, this is not a bad first list.</v>

00:27:52.639 --> 00:27:53.199
<v Nathan Carver>Okay.</v>

00:27:53.039 --> 00:27:55.119
<v Genadi Peari>I think, I think the one you...</v>

00:27:55.999 --> 00:27:58.159
<v Genadi Peari>You sent us was better, but...</v>

00:27:59.079 --> 00:28:03.039
<v Val Levitan>Well, let's find that. I mean, it's either an e-mail or Teams.</v>

00:28:04.959 --> 00:28:06.879
<v Nathan Carver>Yeah, I was looking for it as well.</v>

00:28:08.719 --> 00:28:14.079
<v Genadi Peari>Okay, this is more or less clear how to, what to do.</v>

00:28:14.719 --> 00:28:24.079
<v Val Levitan>But let's review it again, Genadi. I just want to make sure that you and I, we understand each other. Again, please understand, I've never done it before.</v>

00:28:25.119 --> 00:28:25.599
<v Nathan Carver>Mhm.</v>

00:28:25.439 --> 00:28:26.879
<v Val Levitan>I'm only leaning.</v>

00:28:27.839 --> 00:28:36.799
<v Val Levitan>on what has been done in the development side of it, in the programming side of it. And there it works. I know that it works.</v>

00:28:42.359 --> 00:28:42.879
<v Val Levitan>So.</v>

00:28:44.479 --> 00:28:48.799
<v Val Levitan>Each repository you will have a dump.</v>

00:28:49.759 --> 00:28:53.439
<v Val Levitan>of data, sorted data, when I'm saying a dump.</v>

00:28:54.319 --> 00:29:03.679
<v Val Levitan>dump because you already have it, but it will be a properly selected set of items that you vetted and you approved.</v>

00:29:05.359 --> 00:29:09.199
<v Val Levitan>In your personal computer, personal emails, you get a lot of...</v>

00:29:10.319 --> 00:29:20.719
<v Val Levitan>things sent to you, but what you put into Github is approved items. This is what you selected and you say, yeah, Jvl is going with this.</v>

00:29:23.679 --> 00:29:39.999
<v Val Levitan>I approve this monitor or these monitors, I approve these drawings, I approve these data sheets. And you have to put them into appropriate repositories. Displays with displays, harnesses with harnesses.</v>

00:29:41.919 --> 00:29:44.399
<v Val Levitan>Money devices with money devices.</v>

00:29:45.359 --> 00:29:47.199
<v Val Levitan>Plastics with Plastics.</v>

00:29:48.879 --> 00:29:52.479
<v Val Levitan>And then there you have to have data sheet drawings.</v>

00:29:54.519 --> 00:29:59.519
<v Val Levitan>Whatever, if you need whatever information you need for yourself.</v>

00:30:01.439 --> 00:30:06.639
<v Val Levitan>To put the machine together by hand, like you do it by hand.</v>

00:30:07.919 --> 00:30:10.799
<v Val Levitan>You have to have everything in the repositories.</v>

00:30:11.959 --> 00:30:16.319
<v Val Levitan>From there, I assume Nathan will trigger.</v>

00:30:17.759 --> 00:30:24.879
<v Val Levitan>an agent who's going to look at everything you have in the repository. I assume, Nathan correct me if I'm wrong.</v>

00:30:25.199 --> 00:30:25.679
<v Nathan Carver>Mhm.</v>

00:30:25.839 --> 00:30:36.079
<v Val Levitan>And that agent, you will ask that agent to create a data contract for each repository. I assume there will be mistakes.</v>

00:30:37.199 --> 00:30:46.959
<v Val Levitan>I intend to catch these mistakes during the final assembly, because it should not assemble with improper data contracts.</v>

00:30:49.239 --> 00:31:00.559
<v Val Levitan>If data contracts don't match, it cannot assemble. But if data contracts match, that means the information in there is good.</v>

00:30:49.359 --> 00:30:49.919
<v Nathan Carver>Correct.</v>

00:31:01.999 --> 00:31:20.399
<v Val Levitan>If not, we have to go back and fix it. And this is what I'm saying. We're fixing it at the source. And when the source is fixed and we use intelligence, artificial intelligence, we could use it at any point of our lives. We could seek a new vendor. We could</v>

00:31:20.559 --> 00:31:28.159
<v Val Levitan>assemble new bill of material. We could check pricing.</v>

00:31:29.359 --> 00:31:32.719
<v Val Levitan>We could, I don't know, do so many things.</v>

00:31:35.039 --> 00:31:38.479
<v Val Levitan>But the information that the source has to be dead on.</v>

00:31:42.719 --> 00:31:43.199
<v Nathan Carver>Correct.</v>

00:31:44.319 --> 00:31:44.799
<v Nathan Carver>So.</v>

00:31:47.679 --> 00:31:48.399
<v Nathan Carver>Go ahead, Genadi.</v>

00:31:49.519 --> 00:31:49.919
<v Val Levitan>PIN.</v>

00:31:50.959 --> 00:32:09.999
<v Genadi Peari>No, I think we're clear. Let's do tomorrow one repository example, see exactly how the readme file works and the folders or the organization of 1 repository if possible, and then I'll start.</v>

00:32:10.959 --> 00:32:12.399
<v Genadi Peari>Push everything I have.</v>

00:32:12.879 --> 00:32:19.039
<v Val Levitan>I suggest you do 2 repositories, I suggest, or three, I suggest you do, let's say, a harness.</v>

00:32:20.399 --> 00:32:28.159
<v Val Levitan>A few displays and maybe some sheet metal, something that was assembled together with the with all of this.</v>

00:32:29.199 --> 00:32:30.639
<v Genadi Peari>Yeah, sure.</v>

00:32:33.759 --> 00:32:37.999
<v Nathan Carver>Okay, and then we make the request to create the repos.</v>

00:32:39.359 --> 00:32:39.839
<v Nathan Carver>Oh.</v>

00:32:41.119 --> 00:32:42.479
<v Genadi Peari>Three repositories, yeah.</v>

00:32:42.759 --> 00:32:44.399
<v Nathan Carver>Three repositories, okay.</v>

00:32:46.079 --> 00:32:47.279
<v Genadi Peari>You have like the.</v>

00:32:46.399 --> 00:32:49.599
<v Val Levitan>Who's gonna make, who's gonna make this request?</v>

00:32:51.199 --> 00:32:52.919
<v Val Levitan>Whose undertaking is this?</v>

00:32:54.519 --> 00:32:54.879
<v Nathan Carver>Um...</v>

00:32:56.639 --> 00:33:03.839
<v Nathan Carver>Well, I can make the request, but I think just need Genadi sign off on the on the names. That's all.</v>

00:33:03.839 --> 00:33:06.479
<v Genadi Peari>Yeah, yeah, whatever you have, it's good here.</v>

00:33:06.239 --> 00:33:06.639
<v Nathan Carver>Okay.</v>

00:33:08.159 --> 00:33:13.519
<v Val Levitan>So, let's do, let's do the second one: Display, let's do...</v>

00:33:13.839 --> 00:33:14.639
<v Genadi Peari>Third one.</v>

00:33:16.159 --> 00:33:17.679
<v Val Levitan>Okay, third one.</v>

00:33:18.799 --> 00:33:21.119
<v Val Levitan>And let's do a sheet metal.</v>

00:33:21.639 --> 00:33:21.999
<v Genadi Peari>Yeah.</v>

00:33:23.519 --> 00:33:23.919
<v Nathan Carver>Okay.</v>

00:33:25.119 --> 00:33:27.599
<v Nathan Carver>All right, so these three. Perfect.</v>

00:33:25.999 --> 00:33:26.519
<v Val Levitan>We are.</v>

00:33:29.919 --> 00:33:31.439
<v Genadi Peari>Okay, understood.</v>

00:33:31.919 --> 00:33:36.159
<v Val Levitan>And ask, ask Dmitri Kovalchuk.</v>

00:33:38.319 --> 00:33:40.719
<v Val Levitan>To create 3 projects.</v>

00:33:44.479 --> 00:33:44.959
<v Nathan Carver>Okay.</v>

00:33:50.079 --> 00:33:53.759
<v Genadi Peari>In the parallel world with the...</v>

00:33:56.799 --> 00:33:59.839
<v Genadi Peari>Mikhail Levitan part.</v>

00:34:00.719 --> 00:34:01.839
<v Genadi Peari>Organization.</v>

00:34:02.719 --> 00:34:04.719
<v Genadi Peari>We need to work on the.</v>

00:34:07.519 --> 00:34:09.119
<v Genadi Peari>Organization of the...</v>

00:34:09.599 --> 00:34:09.719
<v Nathan Carver>Yeah.</v>

00:34:11.839 --> 00:34:16.879
<v Genadi Peari>Tools for Mary, right? Mary or for the Shayee CO or whoever it is.</v>

