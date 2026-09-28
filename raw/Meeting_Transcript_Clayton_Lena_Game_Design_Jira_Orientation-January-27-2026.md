# Raw Transcript — Clayton Chancey / Lena Zhukova — game design workflow and Jira automation orientation
**Date:** January 27, 2026, 9:58 AM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026]]
---
00:00:27 Speaker 1
Okay.
00:00:57 Speaker 2
Your name says Axel Smith.
00:00:59 Val
Yeah, it's my Gmail account.
00:01:02 Speaker 1
Uh okay. Gotcha.
00:01:10 Speaker 2
I, just saw your email that you sent a few hours ago regarding the IP things with how to create the DNS zone. Look, for uh think you'd have in the LACM. And from that map, we're very happy to help you out with that as well. If you need anything else, just let me know and I'll be happy to help out. Thank you very much for your time today and have a great day bye- bye.
00:01:28 Val
Look at the enrollment process and see if there is something wrong with it.
00:02:20 Speaker 2
And we're waiting for Lena, correct?
00:02:23 Val
Yeah, correct. She is a little bit punctual. Okay. Usually she's on the minute.
00:02:32 Speaker 2
Okay. Let me just make uh, let me just make sure that my meeting allows others who are not well. I did not invite to join. Yeah, it should.
00:03:00 Val
I'm just keeping my Teams open in case she can't log in. But she's.
00:03:40 Speaker 1
Thank you.
00:05:37 Val
I'll be having difficulty logging in. Can I send you uh can I ask you to invite her?
00:05:47 Speaker 2
Can you what, sorry?
00:05:48 Val
Can I ask you to invite her directly?
00:05:51 Speaker 2
Yeah, of course. Uh, let me just get. Believe you included her email. Um, yeah, I've got her email here. Oh, it seems okay here she is.
00:06:13 Speaker 2
Hello. Hello. How are you? Good, good. How are you? I'm doing well. Nice to meet you. I'm Clayton.
00:06:22 Speaker 4
Nice to meet you, my name's Lena. Nice to meet you too.
00:06:26 Speaker 2
All right, awesome. Um, I have some sort of questions and and thoughts I wanted to run through with Val. Did you want to say anything or.
00:06:43 Val
So Lena is a director of game design. She reports directly to. The game producer. And then she has um. A team of designers that are located mainly in Europe, Portugal, Poland.
00:07:14 Val
And the is located in uh, Toronto. And so. Let.
00:07:26 Speaker 1
Me share the screen. Do.
00:07:41 Val
You guys see the screen? Yes.
00:07:47 Speaker 2
Yeah, this is your uh Jira roadmap.
00:07:49 Val
This is our Jira roadmap, And Lena's work is broken into uh I guess game design is broken into three segments.: game concept, uh game design, and game production. So Lena's work starts from being present at game design, but this is mainly, The work that involves the product manager and the producer.
00:08:24 Speaker 2
Okay, so Juan is the PM and Michael is a producer. Correct.
00:08:34 Val
And so they discuss different concepts, and Lena is present here. Does she contribute? Very very insignificant I should say Lena.
00:08:46 Speaker 4
Correct me if I'm wrong.
00:09:16 Val
Then game design further grows in this stage. And this is where Lena starts developing home park. And this is below the stage, is where Lena is mainly running the show and she is pushing the production. So this is the conveyor belt.
00:09:49 Val
We, the way we layer our Jira is we have an initiative, then it's split into a product, and on the product we have features and stories. Feature is what signifies a feature branch in GitHub. Okay.
00:10:18 Val
A feature branch implies an artifact, a deliverable artifact that must be deposited in GitHub. This is a rule; this must happen. And if a feature does not produce an artifact, then it's probably not a feature and probably not properly defined.
00:10:51 Speaker 4
I May make a little correction here. As this process is applicable for production of only games in our like for our like only game engine,
00:11:12 Val
Yeah, let me explain this. Let me explain right now, the company as Lena tried to explain the company is. Shifting paradigm, Our Jira and Confluence was a was treated for ten years, was treated as a central notepad repository. For not to forget to do things. Yeah, and about five years ago we deleted.
00:11:48 Val
80,000 tasks. We reduced our workforce by half. And we got rid of our CTO and CFO. Today Jira is a productive place, but it's not working to my satisfaction.
00:12:20 Val
It is quite bureaucratic. It's a process that sucks life out of us. And it's not really productive source of information. If we lost Jira today, the company would not go down.
00:12:53 Val
The decision, the decision.
00:12:54 Speaker 2
Can I ask just a question about the state of Jira and Confluence today? Would you say that I understand it's labor intensive? There is probably a lot of data entry maintaining roadmaps, creating artifacts and tickets. I understand it's it's a painful process. One question is: Is it accurate today or is this is it still inaccurate?
00:13:21 Speaker 4
Not bad. We are trying to keep it up to date and accurate. We are trying our best there.
00:13:29 Val
Not bad, not bad. I find that Confluence is more polluted and more unproductive because it's just everything. Yeah. And I don't know really. Anyways, we made a decision to move away from Confluence into GitHub. And we look to put all our artifacts into GitHub. It's a decision; it's not we're not discussing it anymore. I mean, we're there. Let me just say this : that we have a legacy product, which is our framework this.
00:14:22 Val
Framework is called Rage Studio. And Rage Studio comes from the fact that we used to have a department, the entire department, that was developing and maintaining an engine, a graphic engine that also wedged itself Into development ecosystem, and eventually we just like it happens all the time, we couldn't compete with the industry; the industry surpassed us. And we made a decision to and we also entered a online market, online game market which at that time was.
00:15:20 Val
Based on HTML architecture. And so the decision was made just to put our entire framework under HTML. And then still the judgment is out there, not judging whether we made the right move or not, But at that time, we had a business architect consultant working with us, and he heavily embraced it. And. I wasn't smart enough to counterbalance this, but and I really don't understand how it works. But we took a Unix sorry, Not Unix Unity Unity engine unity development ecosystem, and we created our own translator that would take Unity.
00:16:20 Val
Graphics or Unity development and distill it to 2D Pixie engine. And Pixie engine was chosen because it was free. And I mean we need free because we use multiple copies of it. And we attempted to negotiate with Unity, Unity was too bulky, too heavy, uh too expensive.
00:16:51 Val
Negotiated deal. So the architectural decision was to have this middleware, I don't know how to call it, Middle app or something that would allow us to design in Unity and then take it and siphon all of it into a Pixie ecosystem under HTML. Framework environment. Okay, so we we put tremendous effort in it, and I hear that it's working. And I hear that we're happy maybe or maybe I don't hear enough. The judgment is still out there. I don't know whether we.
00:17:48 Val
In the right place or not, But what Lena was trying to say is that while we were within the Rage Studio framework, we were also on other antiquated ecosystems like an SVN and Jenkins.
00:18:12 Val
And So that legacy setup is still.
00:18:19 Val
With us, And Lena, unfortunately has to spend herself on parallel working between Rage Studio and Omni. So when I inaccurately stated that our development were are that our artifacts need to find its way on GitHub, Lena correctly.
00:18:49 Val
Corrected me by saying that this is our future plan for omni ecosystem. And. So right now, we're going through very uncomfortable transition of getting that ecosystem as our prime development methodology, which is not. And, the reason it is not because our industry has a bureaucratic process of approvals. Of technical approvals we have in our ecosystem and our business, there is a lab, technical lab that wedged itself between the regulator and the manufacturers. And so that process requires approval. So we're just hitting this part right now. But what you need to.
00:19:48 Val
Assume is that we will be moving into GitHub, moving away from SVN, moving away from Jenkins. I don't know how much effort you want to put on Rage Studio. We have massive amount of work going in right now in Rage Studio and Lena's prime bureaucratic swamp is on Rage Studio.
00:20:19 Val
So, This is a little bit of a difficulty that I also when I when I hired you, I didn't think through this. And you know Leona's bringing it to our attention. So yeah um. The the the, I'm still gonna make this point. As as management we're suffering from uh we want efficiency. But we're burdening our people with bureaucracy. And we're saying that you guys are not efficient, but in the back of my mind, I understand that there's a bureaucratic swamp in here that is just tremendously uncomfortable. And Lena, for example, I have a feeling that Lena is spending somewhere between 20 to 40 % of her productive time on bureaucracy.
00:21:19 Val
And I don't know whether it's twenty or forty. I don't know where it's closer to. I am going to let Yanami to comment on this, but yeah, I mean, this is something that we're dealing with today. I think that concludes everything that I needed to say. Yeah, any questions.
00:21:45 Speaker 2
From my side? I guess just to understand. Transition or the bureaucracy from Rage to Omni. What do you what do you think that transition looks like? Are, you just closing out Rage projects and getting them through to the regulation process and anything new starts with Omni, and when the old backlog is done, then it's done? Or is there some other additional requirement there?
00:22:15 Val
Not that simple.
00:22:18 Val
I mean, we have markets, and markets move at certain pace. And markets have certain demand. And for example, market in South Dakota requires a certain game development, but we have Rage Studio product in there. And we cannot forget the market. So very uncomfortably, we're just making a very minimum that the market can tolerate. We also understand that.
00:22:48 Val
We need to shift gears, and we need to get into Omni. So we schedule scheduling submission to the lab for Omni in March. We anticipate that we'll get through the lab by June, so by the end of the year, we'd like to accumulate more product in Omni because Omni will Deploy along with the new ecosystem for development, along with new framework, along with new it has an internal database. You know Citi on the side. So that is that part is new, but in addition to it, it will be sitting on on the new hardware.
00:23:45 Val
So we're migrating from uh AMD V ten hundred processor into uh FP seven processor. Okay. And as we migrating into more powerful, processor, more efficient framework, more efficient internal database. We're now saying well graphic designers, we want more bells and whistles. We want more rounds. We want more entertainment.
00:24:16 Val
More transitions, more particle effects, et cetera, et cetera. So approximately when I would say ideally, I would like to have at least three more games by the end of the year in an approved omni framework with new F P seven hardware placed in locations.
00:24:48 Val
How realistic is it? I mean, It's a tall order because the designers are also busy with giving us products in Rage Studio in the markets that we must maintain, otherwise we're not going to have cash to survive. Yeah, so those are real challenges. Again, I just want maybe if when I noticed, I'm just going to repeat. Rage Studio sits on SVM and Jenkins. Yeah. And that's uh and and some of the uh applications, Graphical applications that the department is using cannot be used in the modern settings anymore. Because, for example, 3D Max does not have the upgraded version that Rage Studio supports, and we don't have development team.
00:25:47 Val
To bring Rage Studio uh on the level to support 3 D Max. Am I correct, Elena?
00:25:54 Speaker 4
Oh yeah, Rage Studio is based on 3 ds Max11, which is not supported already by Autodesk. So, we use a very old version of 3 ds Max, but we don't have a team to work on Rage and to adopt to newest versions of 3 ds Max. So, there's also like there are some risks that we are working on unsupported software. And uh.
00:26:18 Speaker 4
It's the healthy.
00:26:21 Val
So we, I mean, we're very motivated move off of storage studio. Very motivated. It's just that it's a swamp that we are having difficulty getting out of.
00:26:35 Speaker 2
Right. Okay. I noticed on the roadmap, it seemed like the dates that were scheduled in those date columns, it looked like it was about five months.
00:26:51 Speaker 2
Is that accurate, Darian?
00:26:55 Val
I mean, it's accurate, but it's not entirely true. There are three baskets: concept, design, and production. They all were circular and they all loaded differently. So what it shows you is that conceptually, we have five months of concepts that we're. Estimating, uh, if you look at the design stage, we only have a month of work maybe less. And, if you look at production and we're going to be busy for another four to six months. This is just a workload per basket.
00:27:43 Speaker 4
Okay, I see it.
00:27:45 Val
But they but they're cumulative and we can put uh we can put each, Of the products, or each of the artifacts, or each of the results per basket on a shelf. I see. And take it when we're ready. Right. Ideally, I wouldn't have so many things in design, but again we're not in monochromatic um.
00:28:21 Val
Instance, we are we're addressing multiple things in parallel. Yeah,
00:28:32 Speaker 4
Okay. Also, Like to mention that there are typical different cycles for products, which we are starting to design from scratch. Like complex games with several bonuses, for example. So yeah, it can be like five months.
00:28:53 Speaker 4
But, we have a lot of products when we are adapting like our existing products to different markets. And this is a different cycle. And it also can vary because adaptation can be complex and can be easy. You can use the same theme, for example, and the symbols of the game, but Mars is different. We are adding different bonus if it was horizontal for example or horizontal as. And of.
00:29:43 Speaker 2
All the people working in all of these things, in the concept work, the design work, the production work are all of these people, In Jira, managing their work in Jira, Or are there developers? And there are like kind of scrum masters or product managers doing Jira? Is it everything?
00:30:03 Speaker 4
Yeah, I have like two people who are helping me a lot, like project manager, like art managers. They are also they're not full time art managers, so they, uh they are game artists by themselves, but they help in.
00:30:24 Val
Just To be clear, when Lena says" managers," in her world, managers that means they manage Jira. But they're not managers; they're lead, the senior design people that are helping Lena enter tasks. But they lack managerialresponsibilities. And they lack managerial talent, and they don't like to be managers. They just, they really. They're not managers. So, it is a way for the managers to get a little bit of a breathing room from bureaucratic tasks, but it's really it's not done properly and it's like.
00:31:20 Val
Getting the teeth out.
00:31:21 Speaker 2
Okay. That I'll just be I I don't want to you know bullshit anybody here. Um, I would be very interested to see exactly what those people do and what their inputs and outputs look like in Jira, And if we could just kind of double click on, what is the work that those roles do, uh that might be an interesting place too.
00:31:50 Val
I'm Going to take this opportunity just to tell you another weakness that we know, I understand it. Just like you saw the defined stages in game concept, game design and game production, they're almost like their own silos. But, they are united by common knowledge of Lena and the product manager and the producer. So we have another set of silos that fall under core technology, hardware. All of that is managed outside of Lena, produce the producer and the product manager. They're managed by.
00:32:45 Val
Entirely different set of people. In addition to it, There is a uh uh there is aum uh QA department that is also its own silo. Uh which you know hardly communicating, so that is all of it disjointed higher.
00:33:10 Speaker 2
Hello, hi Adam, can you hear me okay? Yeah yeah we got Jeff I'll uh, I'll send you the transcript of the previous thirty two minutes. Okay, so there are so what you're saying though, correct me if I'm wrong, Is there are other silos where there may be similar inefficiencies, not just limited to Lena's lane and area that are related to other other contributors to these.
00:33:47 Val
Oh, For sure. But, what I was actually trying to say is that aside from them being their own silos between themselves, they're disjointed and they're not run by the same person. So I am trying to fill those shoes by being vertically responsible for everything.
00:34:14 Val
The problem with this is that I'm not properly educated. I'm not an engineer. I'm not a designer, and I have very limited time. I mean, I'm running multiple businesses and responsible for all executive decisions, so. And I'm not the most knowledgeable person on this.
00:34:42 Val
And I am learning Jira, the new tool. So that is also an issue, of course. But with all these problems, with all these problems on a daily basis, I personally feel better and better and better about it. And I am more versed, and it's easier for me to run the company, and it's easier for me to run the meetings now. Jira is a unification tool for all of us. It brings us together, it opens up the questions. And you asked a very good question: Does it show truth? It does. Is it an ideal that is everything absolutely truthful? Are all the dates absolutely were held to every day? No, but it's not bad.
00:35:41 Val
Not, not really. Not bad at all, right?
00:35:45 Speaker 4
Yes. We are trying to keep it very hard for us to take away from them. We have put a lot of effort here.
00:35:56 Speaker 2
So, if you were to say like what's you have these managers who work for you who help you? And get stories that sort of decomp.
00:36:10 Speaker 2
You have these buckets of concept, design, production through which work flows in an agile manner. What is the most difficult part of like what makes that process of managing that work in Jira painful? Is it the act of decomposing tasks or things that are very broad into smaller pieces?
00:36:40 Speaker 4
Communication. Yes, you need to answer a lot of issues. For concept and design, we are managing these two spaces like me, VP product owner and game producer. So we are taking all issues there. And for game production it's me and art managers. And for each game we have a list of deliverables.
00:37:15 Speaker 4
For different type of games, we have like the different milestones. So, each milestone we treat as a feature. So and inside each feature we need to create a list of stories inside. So and we're trying to keep our stories not more than two days. It's not always two days but it's about this. So there is a lot of stories also under each feature.
00:37:45 Speaker 4
So, That's basically the main problem.: is the amount of issues you need to enter, and you need to do description. So go each story and each feature. That's basically.
00:38:02 Val
I could tell you that I'm very much involved in doing the same thing that Lianna does, but on the core side. The developers and I've adopted a very and I'm pushing them to adopt the same thing. I've adopted this form of, I call it automation, where I do not try to write things. I sit in a meeting with them and I make people talk things out. And i squeeze information, i'm recording it, and i'm squeezing information out of the developers: explain it to me, explain it to me break it down break it down.
00:38:44 Val
And then I take this transcript, I put it into Claude. Yeah. And you know, with a few prompts, within 15 minutes it opens up a bunch of tasks for me, a bunch of features. So my problem is when I do it personally, I am not an engineer, and if I made an error or not an error if I wasn't exact or if I missed the technical side of it, it creates a lot of shit which I don't want but.
00:39:14 Val
If I was an engineer and I read and I understood what I was saying, then it would be a clean thing. So, I don't know. i have not had this discussion with Lena. I don't know if she adopted a similar tactic or not. I know for a fact that she has not used Claude Desktop, so she has not had an MCP connected to Jira, so obviously she has not used that sort of automation. But am assuming she's probably using Chat G P T in, In doing something like this, but then manually entering all the tasks. So not not entering tasks manual and just telling Claude, okay, I mean you you've broken it down for me here. It's all clear now go ahead and do the Jira manual entry. That shaves off a couple of hours right there.
00:40:09 Speaker 4
Yeah, I did not use Claude to get for the task because with AI get code and output. A couple of days ago, uh, if I use spline for this, uh, and yeah. And I found that it it helped a little bit, but you need to check. First of all he is asking you so many questions on the way.
00:40:30 Speaker 2
Yeah. Correct correct correct.
00:40:31 Speaker 4
Correct automatically both in the right way. Uh, so you need to again, you need to answer all the time. And then you again, you need to uh recheck everything, because sometimes uh it's sometimes okay. And again, you need to check because sometimes he's just out of the way. He's trying to fix our help because he thinks it's better to say that, but we are saying it because.
00:41:14 Speaker 4
There are some regulations on our market,
00:41:17 Val
But hold on a second. We also are not good prompters,
00:41:23 Speaker 4
Yes, that's true.
00:41:27 Val
And most of us, most of the companies English is a second language. And the further we depart from being the prime language yet. We're using English as ourtyping tool as the entry tool, the more we depart from the proper prompting. So we need to understand this. And I'm encouraging us to use our mother tongue for prompting instead of trying to use broken English for prompting. But the problem is that those that don't live in North America, they want to perfect their English. So, they kind of using this as a platform for conversation just to improve their English, but their prompting is suffering.
00:42:15 Speaker 5
I would also add that the story told with Klein and things like that is technology and the other tools and platforms that we're using right now has significantly changed. Notably, way better in different ways,
00:42:36 Val
And has been progressing on a monthly basis. I am sorry for interruption, but I am noticing this.
00:42:42 Speaker 5
So essentially, you're going on information that's about nine months old, maybe ten months old. And the amount of change that's happened in ten months is considerable. So I think there's, you know, that's another thing that we're trying to catch up on. Yeah.
00:42:56 Speaker 4
Yeah, but it depends if you try to use quotes or yeah. But, of course, like mostly because we are artists, mostly we are using chat GPT for creating. Uh uh creating uh, like some art reference. Some uh images for combat for building like concepts of the game that that and in this area, I see that the whole AI tools are progressing a lot. I think it's a good idea to use those tools and try creating images.
00:43:29 Val
Aaron's suggestion uh for the designers to depart from chat GPT and.
00:43:42 Val
Graphics based application AI tools.
00:43:45 Speaker 4
What kind of?
00:43:49 Speaker 2
Yeah, so let me just say for another of my clients, I just built something which I think is. Uh I don't think it has a license on it yet. I can put an MIT license on it, fork it and use it for here that will serve our.
00:44:13 Speaker 2
Which is, I was given charge to create a backlog for their AI practice, like this massive backlog for an entire year, decomposing along a certain hierarchy of work. This hierarchy was not exactly standard. When you get down to the epic level and below, it's kind of standard Jira, But several levels above are unique, and they had rules and ideas and a philosophy that's not just like standard Agile. And. So I say that because the default way of managing things in Jira didn't exactly apply. There was some nuance, some context, and so I can't use like out-of-the-box AI tools. I can't really use Robo very well for that. I wanted to use Claude, And I as one person who also is running a business and has like eight different clients, was responsible for creating an entire year backlog.
00:45:11 Speaker 2
And generating slides and selling it to a board and all of these things, budgeting, opex, capex, all of this bureaucracy to translate a vision that I have. And so I instead of doing all that work manually, I just created a custom MCP tool, which is sort of based on some of the Atlassian MCPs that they've created and even some that Aaron and I have created together. But I started from scratch from first principles, because I know how to create an MCP. And more importantly, I know how I want to manage my projects. And I don't necessarily want to write to Claude, Look up all of the fixed versions and find the fixed versions, which are based on our quarterly date. And look at all the issues, which are tagged to our fixed versions and organize them by X. That is not how I think. That's how Jira thinks. I want to say, Are there any incomplete tasks.
00:46:11 Speaker 2
For upcoming releases, and I want it to just know this. And so, the way that I designed the MCP tool was very opinionated. So, Each little tool call that the MCP can make has within it five or six or ten or twenty API calls, and also prompts and resources, which are embedded in the MCP tool that hard code prompts to say when the user refers to a release. So you should look up the fixed version field. When the user talks about such and such a concept, this actually refers to a custom labeling scheme which is only found here, here, and here but not over here. And, all of this is just embedded so that anyone who's familiar with this way of working can just use this MCP tool and ask a simple question and also create it. So I spent maybe ten hours getting this MCP created, and everyone was sort of quite.
00:47:09 Speaker 2
Hey, I don't see any tickets, Clayton. Are you making tickets in Jira? And I was building a tool. And then when the tool was finished, I copy pasted a transcript from a meeting, uh like a conversation that was a two hour long conversation into Claude. And with one shot, it created three hundred and forty tickets in Jira with organization, the hierarchy, the epics, the features everything. And then I have to go check and edit a few things, but it saved. Sixty hours, probably. So, in my mind, this might be something interesting to try. I have a technical foundation for that; like I have code. But, the crucial piece is not the MCP server, because we can stand up an MCP server from the time that we started this call until now—it ' s been forty - seven minutes.—so the MCP server could have been created by now. What we need is very specific.
00:48:10 Speaker 2
Regarding how you guys are working in Jira. And that I think I just saw that Dima emailed me with access, so I can get in and poke around. And then I think I would like to try to just create something. And I think we're meeting again uh not tomorrow but the day after. Let me come to that meeting with whatever I created, and let's try asking it, some read only questions. And and then and then maybe Lena, if you're able to join that call, you can look at the answers, Me as an expert, does that feel right or does that feel wrong? And how does it feel wrong? And, this becomes a feedback loop to improve the tool until you're able to take it and do the same. And then we continuously improve it. I think this could be a very fast way to show value, and you could get to the point, I hope within one week or two weeks, even where this tool actually does seventy five percent of.
00:49:10 Speaker 2
Managers, your scrum masters are actually doing.
00:49:15 Val
That. That's a great direction. I really like it.
00:49:18 Speaker 2
Okay, and I think it's very comfortable for me as well. Aaron and I have done. These sort of this is a very comfortable motion custom MCP server with custom opinions behind it. So, let me just quickly look at the email.
00:49:33 Speaker 5
That I don't think i'd like to make sure we can kind of coordinate on is that in the last session? For this call, I am helping the developer engineering team with their version of tier M C P as well. And we can coordinate sort of. I think what we need is more focused elastic M C P servers for different ways of thinking. So, like when you are talking about the management hierarchy, I'll be talking about sort of the developer blend hierarchy and things of that nature. And, we can coordinate a kind of a couple of them depending on the major role that we're looking at because it's not a one size fits all solution.
00:50:09 Speaker 5
Tools to be able to get that context correctly.
00:50:11 Speaker 2
Yes, yeah, yeah. You know, And uh, this is a little bit of inside baseball, but Aaron I'm almost wondering if the like TypeScript directory and a tool search capability would be useful here. I don't know if you could create folder one MCP server JVL MCP server with different roles baked in or something where whoever the user is.
00:50:34 Speaker 5
Maybe with I've done a pattern like that before. It's just to get. It's difficult to pass the.
00:50:40 Speaker 2
Yeah, I mean it's fine to keep them separate too, but in my mind I am like, I mean, that's a way to create this semantic ontology of all the things that people need to do. And sort of it's almost like creating job descriptions now tasks, and it's a familiar organizational hierarchy approach. Maybe,
00:50:59 Speaker 5
We can spend some time in our design session on it little bit kind of talk about yeah.
00:51:05 Speaker 2
Well at the very least I am going to i just have access.
00:51:09 Speaker 2
To GitHub and Outlook, I am going to email them back and just make sure I can get access to the Elastique piece as well. And then if I can get in and explore a little bit, then in the design space particularly, then I'll be able to start working on some.
00:51:28 Speaker 5
So like something some of the things Leonard you may not even be seeing it like it's not surfacing or obvious, is that when the tool calls run for the MCP server. They could be really inefficient right now, right? Like, you could be getting tons of extra text context and making the model dumber than it's supposed to be for how things are working. I was watching Yevgeny do some work, and one call of the official ElastiNMT server consumed a quarter of his context as one of his tools. This is the worst, and so this is something that can be optimized for what's going on.
00:52:12 Speaker 2
Well, it sounds uh it sounds like we have a direction. And then Lena, I want to confirm as well. Would, you be able to join uh the next meeting, which is the same time, not tomorrow, but the day after tomorrow?
00:52:26 Speaker 4
It's going to be yes. And and.
00:52:31 Val
Can weum when you get access to our tools, can we start using Microsoft?
00:52:37 Speaker 2
Yes. Yeah, I'll uh I have a task already set up for my, Login. I need to get my Outlook set up. I'll kind of do the onboarding process today or tomorrow morning at the latest, and then I'll do some of these meetings.
00:52:55 Val
Okay, so we have our marching orders. You have direct line with Elena. You're open to chat with her at your leisure all you want, and vice versa, Elena. My main objective is to make, Your life personally easier to unload the bureaucracy on automation. Aaron has a good speech on bureaucracy if you have a want to hear it, but he calls it "good bureaucracy." It's necessary. I, you know, I hate bureaucracy, But I adopted his preaching. So so let's let's put this good bureaucracy to uh.
00:53:41 Val
And Clayton has a good article on this. He calls it" augmented knowledge work." Augmented knowledge work, yeah. So let's put good bureaucracy in the hands of augmented knowledge tools.
00:53:58 Speaker 2
Yeah, yeah. Awesome, thank you guys. This is very helpful content.
00:54:03 Val
We'll see you all next time.
00:54:04 Speaker 2
I've been transcribing this as well, so this is all in this recursive self- improving meta loop.
00:54:12 Speaker 2
Also going into a clog project that I have with all of the context from our conversations and is being used to help me populate backlog tasks on my Jira board to help you populate tasks on your Jira board. So there's a, and I'm maybe in our next meeting I can show you that as well. So, it's just see it's going to be a very different way of working because I do a different thing than what you do, but the concept of just offloading as much of the manual uh, Generation to an engine that does that very well. But to your point, Lena, I think it's a very I think that despite how good these tools are getting, I think you are very right to say, well, I've used it before, and it felt like now there's a lot of extra judgment work needed. Yes, it can type faster than I can. Yes, it can generate more. But the judgment I feel there might be more work in judgment.
00:55:11 Speaker 2
Just typing and I think that is still almost always going to be a necessary tradeoff. So the the goal of all of this is how do we bake the judgment work into the tool? So that you are doing the judgment work once or very limited. And then so that you can trust the generation. And I mean, that's that's the trick with all of this. I think that's what we're trying to do here.
00:55:34 Val
Yeah, I'm, just going to pat myself on the shoulder because I never get any compliments in the. Company. I just want to let you know that Clayton is really hired because of you for you. Okay? Cool. Thank you, guys. Awesome. All right, thank you, guys so much. See on Thursday by the day after tomorrow Aaron, Everybody's, complimenting, your your previous seminar.
00:56:03 Speaker 5
Good good I'm, glad they, uh, they picked it up.
00:56:09 Speaker 5
See you guys.
