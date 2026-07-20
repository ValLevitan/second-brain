---
tags:
  - weekly-review
  - ATM-contract
  - architecture-documentation
  - pavel
  - juan
  - val
  - flex-pos
  - github
---

# Flex-POS Iteration Review

## Meeting Participants
- Nathan Carver
- Pavel Frolov
- Juan Martinez
- Val Levitan

## Meeting Transcript

**Nathan Carver** (00:00:09): Right. Well, I think we can, we can get started.

**Pavel Frolov** (00:00:14): Yeah.

**Nathan Carver** (00:00:20): It's.

**Juan Martinez** (00:00:24): I think I gave Pavel my cold through the through the teams.

Thank you.

**Val Levitan** (00:00:29): Called virtual virtual environment.

**Juan Martinez** (00:00:32): Yeah.

**Nathan Carver** (00:00:33): Mm-hmm.

**Val Levitan** (00:00:36): Telepathy.

**Nathan Carver** (00:00:36): All right.

**Nathan Carver** (00:00:38): So this meeting is the weekly review meeting where we're just going to talk about what we've accomplished for the week and start prepping for next week since we don't necessarily have dev work to go through and demo.

**Nathan Carver** (00:00:54): We'll just go around and we can just talk about what we've done and summarize it and we'll just touch on next week and any other questions we might have or concerns to get next week started, so.

**Nathan Carver** (00:01:09): Juan, do you want to kick us off?

**Juan Martinez** (00:01:11): Sure. So one of the action items from our last call was to collect an assortment of ATM kiosk service agreements and master agreements. So I've collected those from three of the larger manufacturers in the casino business.

**Juan Martinez** (00:01:29): You know, tons of legal language in there, so I still need to go through it, but it's all been posted into Confluence and I I did share that link. So I'll be cleaning it up over the weekend a little bit more, but I would say, you know, go ahead and take a look at it if you want. Otherwise, wait till Monday for me to clean. It up a bit more. The second request was to get an ATM contract for Georgia. So I spoke to Felipe and he did have a master who agreed to send that to him today. So as soon as we get that, I will post it in Teams as well as add it to Confluence.

**Juan Martinez** (00:02:10): Oh.

**Juan Martinez** (00:02:12): Following up with RKS Valve, we we certainly understand the priority of of intercepting the serial. So Nathan and I have a call this afternoon with Jim at RKS. He apologized for not being responsive.

**Juan Martinez** (00:02:28): He's been very busy, so he is will also have a quote for the four sets of Mother Goose and accessory parts for us today, hopefully in time for our call. And then Felipe will coordinate with him to get those items and we will ship that hardware directly to Toronto.

**Juan Martinez** (00:02:47): So.

**Juan Martinez** (00:02:50): Oh.

**Juan Martinez** (00:02:51): That's all I have for now.

**Nathan Carver** (00:02:54): OK.

**Nathan Carver** (00:02:55): I can follow up with that. So same thing. I'm to connect with Jim and so I'll start that conversation today. We also have the meeting with with John and today and initially that was for going through.

**Nathan Carver** (00:03:14): Um.

**Nathan Carver** (00:03:16): The fraud cases that have happened, that income has experienced, but I think we're also adding a little more context to the conversation today. Juan, since the meeting with Jim was cancelled earlier this week.

**Juan Martinez** (00:03:28): Yeah.

**Nathan Carver** (00:03:28): OK, and I've started. I've added two architecture documents to the Flex POS repository. One is architectural overview which has architecture context information, several context diagrams.

**Nathan Carver** (00:03:46): Just using C4 model that gives us different levels of granularity. I'll just do models levels essentially one through 3 and there's and if there's any more detail at a level 4 engineering team can add that in.

**Nathan Carver** (00:04:02): They choose.

**Val Levitan** (00:04:03): Yes, what is the C4 model? I'm not familiar with it.

**Nathan Carver** (00:04:07): So the C4 model is just an architectural diagram approach and it looks to separate architecture diagrams into 4 tiers and just to give to create a consistent contextual awareness between diagrams. So you can look at the high level.

**Nathan Carver** (00:04:27): Level system look at maybe the you know how these higher level components interact and then you dive into individual components to see their architectural structures.

**Juan Martinez** (00:04:39): Is this for a free tool, Nathan, or or not?

**Nathan Carver** (00:04:43): So the the tool we're using is Mermaid. That's free. That's and GitHub will render that for us. The I'm gonna drop a link to the C4 model.

**Juan Martinez** (00:04:48): OK.

**Nathan Carver** (00:04:53): It's just a it's just a paradigm for doing diagrams.

**Val Levitan** (00:04:55): Yeah.

**Val Levitan** (00:04:56): It's a standard. It's It's an engineering standard, yeah.

**Nathan Carver** (00:04:59): In craft.

**Val Levitan** (00:05:04): I never heard of it, so I I wouldn't know.

**Nathan Carver** (00:05:09): Um, yeah, I like it. It just helps keep things consistent. Um.

**Nathan Carver** (00:05:16): It's a very.

**Val Levitan** (00:05:16): Let's start. Let's start. If if this committee is OK with it, I prefer drifting away from Confluence as much as possible into our GitHub. Eventually, eventually we will switch completely from GitHub and.

**Nathan Carver** (00:05:29): OK.

**Val Levitan** (00:05:35): Possibly even from Jira. My goal is to move away from Jira, from Atlassian and Microsoft as much as possible,

**Pavel Frolov** (00:05:42): It.

**Val Levitan** (00:05:43): but right now use it for your comfort. But if you guys feel comfortable, start shifting priority to GitHub. It's just a.

**Val Levitan** (00:05:54): Overall, a better environment for us.

**Nathan Carver** (00:05:54): OK.

**Nathan Carver** (00:05:59): Yes, sounds good. I'll definitely put all the architecture stuff in there and then as Juan and I collaborate. Juan, if you have access to GitHub or if we want to use a different repo, we can we can sort all that out, but we'll collaborate in Confluence and then move things into GitHub.

**Juan Martinez** (00:06:15): Sure.

**Nathan Carver** (00:06:17): Let's see. So I'll I also have sequence diagrams out there. So both of these, the architectural view and the sequence diagrams, I'll start updating with our more concrete decisions from this week.

**Nathan Carver** (00:06:34): And that's OK. That's it for me.

**Val Levitan** (00:06:37): I have a question if if we will make a final decision to use outside sources for banking, should I call them applications?

**Pavel Frolov** (00:06:52): I.

**Val Levitan** (00:06:52): I guess transactional banking applications, how will it influence our architectural diagram and how each I guess block communicates with with each other?

**Nathan Carver** (00:07:08): Um.

**Val Levitan** (00:07:08): Is there a dramatic change in this or or not?

**Nathan Carver** (00:07:12): Yeah. So in the diagrams it will look very similar to how we interact with Incomm. It should be. My guess is the the service will be a few API calls that we make and just to initiate the transactions with the with the software.

**Nathan Carver** (00:07:31): Or module or the the software service?

**Nathan Carver** (00:07:35): So in diagram wise, it'll look very similar and I'll start adding those in just conceptually what I think it's gonna look like for the engineering team. It should be a handful of API calls to manage within the workflow. Pavel can weigh in on that what he he thinks it might look like, but that's.

**Nathan Carver** (00:07:53): That's my assumption.

**Val Levitan** (00:07:55): OK. Also, sorry, Padal, did I interrupt you? I apologize. Go ahead.

**Pavel Frolov** (00:08:00): Just one one sentence. Last time we we just agreed on we will need just to add one more step on our cloud servers that communicates to income to perform final transaction requests.

**Pavel Frolov** (00:08:20): Request before this transaction request to make additional API API call to third party get answer from them that everything is OK. We already taking this money to our account and then proceed with income final activation card.

**Val Levitan** (00:08:42): OK.

**Val Levitan** (00:08:46): Will there be any functions?

**Val Levitan** (00:08:52): That, well, I should rephrase this. How do you envision management reports?

**Val Levitan** (00:09:01): I have been very.

**Val Levitan** (00:09:07): I have been enjoying very much the MCP approach to things that.

**Val Levitan** (00:09:19): Allows for.

**Val Levitan** (00:09:21): Free you.

**Val Levitan** (00:09:24): Querying instead of rigid.

**Val Levitan** (00:09:31): Uh, reporting.

**Nathan Carver** (00:09:35): So we could.

**Val Levitan** (00:09:36): I I.

**Val Levitan** (00:09:38): Yeah, I I I don't. I don't know how to.

**Val Levitan** (00:09:43): Go about this.

**Nathan Carver** (00:09:44): So if we wanted to use MCP with Claude for example, we could generate reports that are just CSV files. That should make it very easy for Claude to to allow querying of data.

**Pavel Frolov** (00:10:06): Yes.

**Nathan Carver** (00:10:06): Right contextual amount of data for us to actually be able to generate reports off both system and through MCP.

**Val Levitan** (00:10:14): So from an architectural standpoint of view, I assume that everything will go into some sort of a cube will get formed, saved in.

**Val Levitan** (00:10:25): CSV file maybe, I don't know some sort of file and allow.

**Val Levitan** (00:10:33): Claude or client MCP?

**Nathan Carver** (00:10:38): Yeah, off the cuff, not knowing what Pavel's team has now, but you would log those transactions. For example, could be logged to a database table, they could be logged to a file, and then we would have a system workflow that takes that database.

**Nathan Carver** (00:10:56): The data from the database and exports it into a CSV that could be consumed by an AI tool. So there we we would just we would ideally have an automated pipeline that just spits that CSV out at the end. So how we store it in the system can be.

**Nathan Carver** (00:11:13): Is flexible.

**Val Levitan** (00:11:15): That will allow us to move away from Widget, Excel or Tableau.

**Nathan Carver** (00:11:20): Uh, correct.

**Val Levitan** (00:11:23): That's that's fantastic. That's really fantastic.

**Nathan Carver** (00:11:24): Yeah, I don't. Again, I don't want to speak with Pablo.

**Pavel Frolov** (00:11:25): OK.

**Nathan Carver** (00:11:27): I'm just kind of going off the cuff here, so I.

**Pavel Frolov** (00:11:32): Oh, actually we have never used the MCP approach before before our conversation, but I think this is quite the easiest.

**Pavel Frolov** (00:11:45): Project here to try it because we will have a simple data, linear data I would say that we need to to check data that we recorded on in our

**Nathan Carver** (00:11:56): Mhm.

**Pavel Frolov** (00:11:59): database, probably data from third party.

**Pavel Frolov** (00:12:04): Or data from income. We need just to to compare line by line

**Nathan Carver** (00:12:08): Mhm.

**Pavel Frolov** (00:12:13): or probably to find data with close values and so on.

**Pavel Frolov** (00:12:22): It find inconsistencies.

**Val Levitan** (00:12:26): Well, no, I'm not. I'm not only referring to inconsistencies, which is, by the way, is a separate question. I'm referring just to a normal data query. I'd like to move away from structured presentation of data.

**Val Levitan** (00:12:43): The reason I don't like structure presentation of data because if you happen to have a smart guy in your company or a girl in your company, they tend to. If they freestyling, they tend to find interesting angles.

**Val Levitan** (00:12:59): And I don't want to extinguish that.

**Val Levitan** (00:13:03): Gift in somebody. I think it's a looking at data is quite a gift.

**Val Levitan** (00:13:10): People see data in different lights, but if it's presented in rigid format and this is how people must.

**Val Levitan** (00:13:21): Digest data. It's not really inducive for having a talent in the company, and I prefer having a talent, so I prefer to relax the data presentation format.

**Nathan Carver** (00:13:37): Yeah, we can create a workflow that just transforms the data we have or takes the data we have, exports it and something easily consumed by the AICCSV comes to mind.

**Nathan Carver** (00:13:51): And I think what Pablo was touching on is we can also use it. We get the data from income, get the data from the banking software system and get that into similar simple data format. We can now use MCP to.

**Nathan Carver** (00:14:09): Actually compare those three things and start looking for discrepancies for us.

**Val Levitan** (00:14:17): A couple of other things that came to me overnight. Let me just fire them out. There are a few first of all.

**Val Levitan** (00:14:28): All of our hardware.

**Val Levitan** (00:14:31): Obviously will will need must have passport.

**Pavel Frolov** (00:14:34): Thank you.

**Val Levitan** (00:14:38): Lease and RIS capabilities.

**Val Levitan** (00:14:47): If Nathan is not familiar with any of these or some of them, we can elaborate later, but let's digest what I'm saying first.

**Juan Martinez** (00:14:56): OK.

**Val Levitan** (00:14:58): The second thing that came to mind is because I'm hyper.

**Val Levitan** (00:15:04): Focused right now on fraud, we may need to, may want to, may benefit from knowing exactly where.

**Val Levitan** (00:15:16): Where our hotspots are. By hotspots I mean either Uber active locations or Uber active set of transaction in a given period of time or something unusual. And where exactly is it located?

**Val Levitan** (00:15:34): The reason that it's so relevant because in the street business, what is extremely important is that a fraud starts somewhere geographically.

**Pavel Frolov** (00:15:56): Thank you.

**Val Levitan** (00:15:44): It usually spreads very quickly all around geographically. It doesn't just migrate 100 miles away.

**Val Levitan** (00:15:53): It goes within a walking distance, so if we detect a fraud somewhere at an address ABC, we should immediately shut down most of the operation in the surrounding areas.

**Val Levitan** (00:16:09): Should we know the a a precise geographic location of the equipment and how complicated would it be?

**Nathan Carver** (00:16:21): OK.

**Val Levitan** (00:16:21): Um.

**Val Levitan** (00:16:22): I mean that.

**Val Levitan** (00:16:25): If if there is a red alert, we should and and then brings me to the next subject. What if there is a red alert and what is the immediate automated action list that should kind of be engraved in our.

**Val Levitan** (00:16:43): Architecture. What do we do?

**Juan Martinez** (00:16:47): Sure.

**Val Levitan** (00:16:47): Can we can we shut? Can we shut off the equipment?

**Nathan Carver** (00:16:48): OK, just.

**Pavel Frolov** (00:16:49): Good.

**Val Levitan** (00:16:51): Can we shut off the location?

**Val Levitan** (00:16:55): Can we send a group of assassin?

**Juan Martinez** (00:16:58): Mm.

**Val Levitan** (00:17:00): To eliminate the undesired objects, the session is session is recorded,

**Nathan Carver** (00:17:03): I think we.

**Val Levitan** (00:17:04): so I'll make sure that it's treated as a joke. This was a joke.

**Nathan Carver** (00:17:09): We should keep the option on the table though, right?

**Pavel Frolov** (00:17:10): So.

**Pavel Frolov** (00:17:11): 3.

**Juan Martinez** (00:17:12): Yeah.

**Val Levitan** (00:17:13): Alright.

**Juan Martinez** (00:17:13): No more. No more John Wick movies for Val.

**Val Levitan** (00:17:16): Yeah, exactly. Exactly.

**Nathan Carver** (00:17:20): Right.

**Pavel Frolov** (00:17:23): Mhm.

**Nathan Carver** (00:17:24): OK.

**Val Levitan** (00:17:25): So yeah, these these are the things that I wake up with. I I love the business. I love the direction where we're going. It's a it's a powerful, great business.

**Val Levitan** (00:17:35): But we should be very careful. It's a different level of risk now.

**Juan Martinez** (00:17:38): Sure.

**Nathan Carver** (00:17:38): Yes.

**Juan Martinez** (00:17:41): And from my past experience, I would say these should be structured

**Pavel Frolov** (00:17:43): OK.

**Juan Martinez** (00:17:46): standard alert formats that can go even to a distribution group Val where if one location normally processes 10 cash outs and all of a sudden they've done 100, you know an alert can.

**Juan Martinez** (00:18:01): Go out and and those are the types of things that you know we we could distribute. My my only fear, Pavel in in the design architecture, what happens if if these issues happen and you're asleep 7 hours ahead of us. So we need to think about how we could.

**Juan Martinez** (00:18:20): do some sort of controlled shutdown from the US as well.

**Juan Martinez** (00:18:27): Or with the help of income or something like that.

**Val Levitan** (00:18:30): Well, and this brings me then to I thought it was an obvious subject, at least for Pavel I have been talking about.

**Val Levitan** (00:18:39): Um.

**Val Levitan** (00:18:41): What do you call it? Black Swan events. It it would never occur to me five years

**Juan Martinez** (00:18:44): Hmm.

**Val Levitan** (00:18:51): ago that Belarus would be a a black swap.

**Val Levitan** (00:18:57): Black Swan, but it is now and so I don't want to keep any servers. The our our servers or our infrastructure should be geographically independent.

**Val Levitan** (00:19:13): Pavel and I already spoke about it many times, but just bringing it in in this.

**Val Levitan** (00:19:21): Forum here specifically. Just want to make it very clear that part of our architecture is.

**Val Levitan** (00:19:31): Servers are geographically independent. Access to servers should be geographically independent.

**Nathan Carver** (00:19:41): OK.

**Val Levitan** (00:19:42): We at some point will have to build redundancies.

**Nathan Carver** (00:19:49): Mhm.

**Val Levitan** (00:19:49): So that that means.

**Val Levitan** (00:19:53): The the architecture must be scalable.

**Nathan Carver** (00:20:03): OK.

**Nathan Carver** (00:20:06): Yes.

**Val Levitan** (00:20:07): Make sure that we understand it.

**Juan Martinez** (00:20:07): Sure.

**Juan Martinez** (00:20:09): So.

**Nathan Carver** (00:20:11): OK.

**Nathan Carver** (00:20:18): All right, that's all I had. Pavel, any summaries or updates you want to share?

**Pavel Frolov** (00:20:26): Actually no. Any updates from me? Just to inform you, I started to to discuss this architecture approaches, not directly architecture but approaches different devices.

**Pavel Frolov** (00:20:43): Limitations with our key developer.

**Pavel Frolov** (00:20:48): And try to understand possible.

**Pavel Frolov** (00:20:53): Um.

**Pavel Frolov** (00:20:55): Possible configuration sets able to install to the location, how it could be organised, how it could communicate to money transactions here to our control server. We started the discussions.

**Nathan Carver** (00:21:17): OK.

**Val Levitan** (00:21:18): That's very good, very good.

**Nathan Carver** (00:21:19): Perfect.

**Juan Martinez** (00:21:21): And and just to Val, based on your third party topic raised yesterday, I did reach out to John and Alan at Incom to try to get contact information for RWJ, Lunix and YN Low. So he responded late with oh, what's going on? What is your agenda?

**Juan Martinez** (00:21:41): So I explained it to John. So hopefully we'll have that answer maybe during our 10:00 call with them.

**Nathan Carver** (00:21:53): All right. OK, value last last one. Anything else you want to add?

**Val Levitan** (00:22:01): No, just to remind you that I'm on vacation next week. I will not be available, will not be participated in the meetings, but my knowledge, personal knowledge base system that I built around my recordings.

**Val Levitan** (00:22:17): Is working fantastically well for me. I'm very happy with it.

**Pavel Frolov** (00:22:22): Yes.

**Val Levitan** (00:22:23): All I'm asking you to please continue having meetings, record them and send me a unobstructed full recording in WVTT file.

**Val Levitan** (00:22:35): And I can, uh, consume that.

**Val Levitan** (00:22:39): I I can. I can catch up with everything that you're doing.

**Nathan Carver** (00:22:43): OK, perfect.

**Val Levitan** (00:22:47): I strongly recommend if anybody wants to build their own knowledge base to use Obsidian.

**Nathan Carver** (00:22:54): Yeah, I'm using Obsidian and Claude to do this. Yep.

**Val Levitan** (00:22:59): You're using desktop cloud.

**Nathan Carver** (00:23:02): Um uh, cloud code.

**Val Levitan** (00:23:05): Yeah, yeah, cloud code. I also use cloud code,

**Nathan Carver** (00:23:08): Yep.

**Val Levitan** (00:23:11): but I suggest for you to use cloud desktop. It's it's it.

**Nathan Carver** (00:23:17): I have used desktop on Windows and then I use cloud code on Linux so.

**Val Levitan** (00:23:25): I I use both, but cloud code is nice. Cloud Cloud Desktop is nice.

**Nathan Carver** (00:23:26): Uh huh.

**Nathan Carver** (00:23:33): OK, you're preferring that one. OK, cool.

**Val Levitan** (00:23:36): No, not necessarily. I mean, I'm preferring that because I don't want. I'm afraid that, you know, I'll say something stupid.

**Nathan Carver** (00:23:46): Oh.

**Val Levitan** (00:23:46): I'm not an engineer and cloud. Cloud code has too much power. It will go and make changes and I.

**Val Levitan** (00:23:53): I I don't want to encounter that or install,

**Nathan Carver** (00:23:54): Oh yeah, that's true. It will do that.

**Val Levitan** (00:23:57): install or uninstall some files and it's just going to be a nightmare for me.

**Nathan Carver** (00:23:59): OK, that's good.

**Val Levitan** (00:24:04): So I prefer cloud desktop.

**Nathan Carver** (00:24:07): OK, that's fair. Yeah, that makes sense.

**Val Levitan** (00:24:08): You you you you give a stupid person too much power. You're asking well.

**Juan Martinez** (00:24:09): Yeah, yeah.

**Nathan Carver** (00:24:13): Mhm.

**Nathan Carver** (00:24:15): OK.

**Val Levitan** (00:24:16): So yeah, but please don't slow down. Don't slow down. Have your meetings while I'm away. It's. I mean, we're we're full, full force. Just Juan and Pavel just.

**Val Levitan** (00:24:32): For your information, I'm in touch with Will. We will be starting HHR, Omni HHR as of August 7th and the reason August 7th and not first is because Alex Deradke.

**Val Levitan** (00:24:51): Is on vacation.

**Val Levitan** (00:24:53): And I didn't want to cut his vacation short, so.

**Val Levitan** (00:24:58): Will is asking if he should prepare himself for something. I would recommend strongly next week for Pavel, Juan and Will just to have a.

**Val Levitan** (00:25:15): Meeting of the minds.

**Juan Martinez** (00:25:17): Sure.

**Val Levitan** (00:25:18): With Will, just to make sure that comes August 7th, we are ready and it's not that the first time on August 7th, which is getting together, scratching our minds and saying where do we go from here?

**Val Levitan** (00:25:33): I mean, it takes people a little bit of inertia,

**Juan Martinez** (00:25:33): Sure.

**Val Levitan** (00:25:37): a little bit of, you know, planning and scheduling, personal time, personal ideas, personal mind space just to get things going. And Pavel, for you personally, when you start thinking about your sprints or how you want to ride.

**Val Levitan** (00:25:53): Especially the HHR, you need to set your mind to reoccurring meetings. How are your people will be consumed?

**Val Levitan** (00:26:06): You need to bring Anton Liskevich a little bit faster in the loop because he needs to. He's building automated test framework for Omni. So how will it encompass the HHR product? I don't know.

**Val Levitan** (00:26:25): know if it will have any effect on it or not. Probably very little, I assume.

**Val Levitan** (00:26:31): And speaking about automated testing, we need automated testing on transactional products.

**Val Levitan** (00:26:39): So I don't know how that framework, Anton's framework will apply to it.

**Pavel Frolov** (00:26:45): Mhm.

**Val Levitan** (00:26:46): Maybe you should start discussing this thing with him.

**Pavel Frolov** (00:26:48): OK.

**Val Levitan** (00:26:52): OK, that's it for me.

**Juan Martinez** (00:26:54): All right. Thanks, everybody.

**Nathan Carver** (00:26:56): All right.

**Val Levitan** (00:26:57): When you schedule, Nathan, when you schedule your meetings for next

**Juan Martinez** (00:26:57): Yes.

**Val Levitan** (00:27:02): week, still invite me because I want to see it in my calendar. I adjust my searches by the name.

**Nathan Carver** (00:27:09): OK.

**Nathan Carver** (00:27:11): Perfect. Yep. We'll make sure that you're still on there.

**Pavel Frolov** (00:27:15): Yeah.

**Val Levitan** (00:27:15): OK, very cool. Thank you very much. Alfia, is Pavel invited for our meeting with?

**Juan Martinez** (00:27:17): Thanks for everything.

**Juan Martinez** (00:27:24): No, he's not. I'm forwarding it to you right now, Pablo.

**Pavel Frolov** (00:27:29): OK.

**Val Levitan** (00:27:30): Do we want to consume them at this stage or not?

**Juan Martinez** (00:27:34): All right. The topic of the meeting is historical events of things not to repeat. So some of that could be design. I I don't know.

**Nathan Carver** (00:27:43): I think a lot of it will be from John's perspective, so not necessarily an engineering perspective.

**Juan Martinez** (00:27:50): Mm.

**Nathan Carver** (00:27:52): So I guess.

**Val Levitan** (00:27:52): Yeah, let's leave part a lot of it. That's just.

**Juan Martinez** (00:27:55): OK.

**Val Levitan** (00:27:56): OK. Thank you. Bye, bye.

**Pavel Frolov** (00:27:58): Right.

**Nathan Carver** (00:27:59): All right.

## Key Topics Discussed

1. **ATM Kiosk Service Agreements**: Juan collected agreements from three major casino manufacturers and posted them to Confluence
2. **Georgia ATM Contract**: Felipe is expecting to receive this today and Juan will post it once received
3. **RKS Hardware**: Meeting scheduled with Jim at RKS to get quote for Mother Goose parts; hardware will ship directly to Toronto
4. **Architecture Documentation**: Nathan added C4 model architecture documents to Flex POS repository using Mermaid diagrams
5. **Migration from Confluence**: Val expressed preference to move documentation from Confluence/Jira to GitHub
6. **Third-Party Banking Integration**: Discussion on adding API calls to third-party banking services before Incomm transactions
7. **MCP Reporting**: Plan to use MCP with Claude for flexible data querying instead of rigid reporting formats
8. **Fraud Prevention**: 
   - Need for geographic location tracking of equipment
   - Automated red alert responses
   - Ability to shut down equipment/locations quickly
9. **Infrastructure Requirements**:
   - Geographic independence of servers
   - Scalability and redundancy
   - Black Swan event preparedness
10. **HHR Project**: Starting August 7th; need preparation meetings next week with Will
11. **Automated Testing**: Need to discuss with Anton Liskevich about test framework for transactional products
12. **Val's Vacation**: Val will be away next week but wants meeting recordings in WVTT format

## Action Items

- Juan: Post Georgia ATM contract when received
- Nathan & Juan: Call with Jim at RKS today
- Nathan & Juan: Meeting with John about fraud cases
- Pavel, Juan & Will: Schedule preparation meeting for HHR project next week
- Pavel: Discuss automated testing framework with Anton Liskevich
- All: Continue recording meetings and send WVTT files to Val during his vacation