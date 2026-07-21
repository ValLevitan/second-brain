**Transcript**

10 September 2025, 12:42pm

**Aaron Bockelie** 0:03  
There to make the connection, but I think there's enough relevancy to kind of skim over a portion of it to just this is our two drink maximum on our philosophizing that we're gonna do here. Let me share my screen to do this.

**Val Levitan** 0:17  
OK

**Aaron Bockelie** 0:20  
Just a minute.

**Val Levitan** stopped transcription

**Aaron Bockelie** 0:29  
Well, you know you're in the new office and bringing a thermos.

**Val Levitan** 0:33  
I'm uh, I'm in a coworker space.

**Aaron Bockelie** 0:38  
Yeah.

**Val Levitan** 0:39  
Which, you know, it's not my preferred.

**Aaron Bockelie** 0:41  
Not your space, yeah.  
OK.  
O.  
I'm going to cherry ick specific bits out of this document because I think they're relevant and I will use it to describe my thinking.  
O I've been considering this thing. I wish this text was bigger. Let me see if I can make it bigger for you.  
OK, O, remember how I've talked about?  
Sandwiching before you know how I like food analogies.

**Val Levitan** 1:23  
Hmm.

**Aaron Bockelie** 1:24  
So basically the idea of doing any of these work, like writing a specification or writing a feature or even creating a product description or even just any kind of unit of work.  
Essentially has three phases, curation, analysis and decision.  
OK.  
O As an example, in agile software development, backlog refinement is curation, development is analysis, and acceptance or deployment is your decision.  
In strategic planning, the market assessment is the curation, the scenario modeling is the analysis, and a strategic choice is your decision.

**Val Levitan** 2:06  
OK.

**Aaron Bockelie** 2:14  
So does that, does that sort of connect the dots a little bit with you? OK.

**Val Levitan** 2:17  
Yeah, it resonate.

**Aaron Bockelie** 2:21  
So I go into a lot of discussion about how you can define all this and whatever.  
What I want to talk about specifically.  
Is this problem right here? And this has nothing to do necessarily with AI, it's actually just an intelligence problem.  
Is that?  
There is a dimension to this.  
That I call variety. So for lack of a better term, variety is a way to describe the experience of the thing that is the the the amount of experience that the thing doing that stage has.  
So for example, when you just asked me to help you with your tools there to fix them, you lacked sufficient variety to understand what's going on, however.  
If we shift the view a little bit, I lack the sufficient variety to understand what you're solving, right? Like you're doing something with meetings and whatever and finance and all sorts of other things, and it's beyond me. Remember the one time when you were bringing up different money streams and I was like M1M2? I don't know.  
Oh.  
I didn't know that I lacked sufficient variety to to be able to to get it. So what this means is, is that when we when we do the analysis, oops, when we do the analysis, the analysis is always.  
Narrower in variety than the curation or the decision. It doesn't mean that it's Dumber. It doesn't mean that it's not as smart. It means that the scope of understanding for the from.  
The perspective of the person doing the curation and the decision necessitates that this is narrower. So to put this in tangible reality, who's the principle architect for the back end stuff again?  
OK, so you asked Dima Chudinov, Dima.  
By January, I need a payment system that can do this thing.  
We'll just paraphrase the whole deal and he goes OK.  
And the real and the real problem occurs is that you are in the curation phase of curating this problem. You know everything from financial to market validation to partners to.  
All this other stuff, a very wide set of of variety is going into this request.  
And then from your perspective, it's a straightforward, narrower thing to ask to do the analysis. And then when he eventually presents it back to you, you have to then consider all of the bits that came from the analysis into and work it back into your worldview, which is a wide.

**Val Levitan** 5:32  
OK.

**Aaron Bockelie** 5:34  
Wide variety again. Now from Dima's perspective, your ask also requires these analysis. So if we were to look at this, it starts to look like this instead.  
So we have these various sequentials that are going on. Ignore that it says AI analysis for a minute. Just understand that it's analysis.  
So what this means now is that in order to develop a set of artifacts, what they might be everything from code to specifications to requirements needs these little sandwiches to be created essentially.

**Val Levitan** 6:03  
Yes.

**Aaron Bockelie** 6:18  
And.  
You have to be able to define them in a way that allows them to understand the problem with less variety than the original request, because if you ask them to consider the whole, they can't.  
I can't. You can never have.  
The ask have just ask somebody to to get into more variety than than what the originating question is. I'm going to stop screen share for a minute to not have it be distracting.  
O.  
Essentially what this means is, is that whenever you request something of somebody, you have to ensure that your request at least contains the set of their experiences and then.  
They can then consider it.  
So what happens when you ask something of somebody that they don't know about? They have to go learn, right? They have to go into the environment and go read something and figure it out. And I like to think about it this way. You know how when you read something?  
New that you haven't seen before and you're either confused by it or like, I don't get it. And then you kind of read it again and then sometimes you just sort of walk away and stare at the ceiling and you're like, oh, I get it now. It kind of just happens.  
And other times you read it and you immediately understand it after you've read it or or experienced it. And then you can work that into your worldview. There is there's like this gap that occurs for learning. So when you go from I don't know it to what I know it.  
The closer you can, the smaller the jump, the easier it is to learn a new thing.  
When you learn new things, you are increasing your variety, that width of that this way. So when Dima reads the requirements that he didn't know about before, he is increasing his variety.  
To be able to better understand your ask because you understand inherently all this other stuff that's going on.  
So now the process. I'm going to get out of this this sort of hypothetical here and just talk about it in reality, like tangible stuff here.  
If you have to define the outcome of our POS system has to be functional in the market by January. The very first things you need to do is not write specifications, but instead write requirements.  
The ointer cells shall do this. It shall do that. It shall do this other thing.  
And you could also say.  
We like you could be thinking about it in your variety terms. I'm going to have 50,000 customers in the Georgia market potentially be using this thing. So one of the one of the conveniences you're offering for requirement is you're basically saying.  
This shall track up to 50,000 players on release day, and it shall have this many can capable of sustaining this many concurrent transactions because you need to be able to define the performance envelope of it.  
So I don't know what those numbers are. Maybe it's.  
100 concurrent transactions, let's just say there's 100 players immediately and simultaneously trying to cash in a ticket or something like that. And that sets a concurrency target, which is you are not asking like what technical platform it is. You're not saying it's SQL.  
Or some other thing or whatever, because that's outside of your variety. Your variety is understanding that the market has to support this many people, has to do this kind of thing for the transaction, and so forth.  
By setting these requirements up, it's it's closing out the sandwich. You you then close out that decision layer in the bottom and say I have decided these things are what I want and then when Dima looks at your output, he begins a new curation process of reading the.  
Requirements and going in order to sustain this many transactions per per second or simultaneous transactions, I need this kind of back end or that kind of back end. And remember the diagram the other day I showed you about executive kind of doesn't worry about the architecture and the and the.  
Other people need to have empathy for understanding, but not knowing why that needs to. That needs to come into play now as sort of a separation of of duty a little bit. So Dima.  
Can't just say that's impossible. We can't do that. He needs to instead sit back and experience the sort of the pain of of having to think through something and learn it.  
And that's kind of where I'm going to get to the other iece of this here.  
Let me find it here.  
O.  
I'm just gonna it's it's literally fancy words for learn some **** and have some patience.  
But it's I'm going to call it in this in this phrase, building variety, building variety, like expanding or building variety through cognitive friction.  
And I call this roductive doubt.  
I have productive doubt. It's like it's like constructive criticism, right? Criticism on its own can be can be destructive. Doubt on its own can be unproductive. But if you do it right.

**Val Levitan** 12:54  
Yeah.

**Aaron Bockelie** 13:00  
You can have roductive doubt by questioning why something is.  
O An example of roductive doubt is a code review.  
An example of productive doubt is a demonstration of what you've done.  
So basically it's.  
I think that you've done the right thing, but let's actually go through it and see what it does. Kind of thing like the the the proof is in the eating of the pudding, right?  
That's roductive doubt, so.  
Without productive doubt, no code reviews means no exposure to better practice, no variety checkpoints, no skill development if it's frictionless. With productive doubt, you can have effortful processing, which means to really.  
Think things through and understand it and deeply learn the subject at hand. Or if you're going to force a peer review, a peer review forces you to have to consider somebody else's opinion and therefore you're growing variety.  
And you begin to understand the world view of what's going on.  
So in the sense of defining requirements, Dimitri can't just.  
Unquestionably accept these requirements. You can't just look at it and go, OK, I'll make it work. That kind of culture will fail.  
There has to be some sort of not a not a challenging to drop the requirement, but a challenge to challenge the requirement to to.  
Ask why does this requirement exist and where does it come from? And depending on how well you've defined your requirement, a well defined requirement will actually have all of that proof in it. This requirement exists because of these reasons.  
And so the 1st order questions in productive doubt are already answered just by reading the requirement.

**Val Levitan** 15:18  
I, I, I think, I think we're far away from 2 drinks.

**Aaron Bockelie** 15:23  
OK, so let me get back to then the rest of this then.

**Val Levitan** 15:29  
I I think that let me rephrase the question because maybe my question was too washed out.

**Aaron Bockelie** 15:36  
OK.

**Val Levitan** 15:37  
Or too broad.  
Do we feel comfortable that if I push somewhat of a of an old fashioned?  
Style development. Go get it done. Here's the set of MV PS or something that I need for January. Do we feel comfortable that we will not fall off the wagon on the transformational path from the transformational path?

**Aaron Bockelie** 16:08  
I think that you'll be able to succeed in working in a new system of tools, which is probably acceptable enough, but you're going to kick the hand down the road when it comes to architectural excellence.

**Val Levitan** 16:19  
OK, so I agree with that. There will be no architectural excellence, but will I get completely derailed if I say we need it urgently, we need it for January, forget all the development.  
Uh, hygiene. Just go get it done.

**Aaron Bockelie** 16:39  
I'm of the opinion I I I work really well in this sort of way. Change one thing and one thing could be a big one thing and in this case change one thing is get out of SVN and work and get.

**Val Levitan** 16:55  
OK, so for that to happen I need to finish this taxonomy excel.

**Aaron Bockelie** 17:03  
Correct.

**Val Levitan** 17:05  
OK, they have a new version now. Can we log in into this new meeting?

**Aaron Bockelie** 17:08  
OK.  
Yeah, sure.

**Val Levitan** 17:13  
And and get and get that done. Let's let's hope that we can get this done today so they could create new repositories after these new repositories are created. OK, so we're now working git. What else do I need?  
To.  
Things that I cannot live without. I would say that I need initial broad strokes, the highest level of what the back end architecture will look like five years from now or three years from now, just a broad.  
Spectrum diagram and then a list of services that will be talking to this architecture and from there I could say OK, based on this overall architecture, let's focus on these MVPS.  
Let's create a detailed architecture, including these MVPS.  
Would that be sufficient enough for us? I'm trying to minimum things done in order not to screw up our attempt to do things right.

**Aaron Bockelie** 18:17  
So.  
I'm I'm gonna give you this strong advice.  
Don't call it architecture when it's at that level. It's not an architecture. What you're what you're defining when you say super high, when you say the word super high level architecture just five years in advance, high level architecture, right?  
That's not architecture. That's a goal. You're actually thinking of goals right now. My goal is to have our architecture based on X.  
And so you need to have a little bit of discussion about what that is.

**Val Levitan** 19:06  
I am not. I'm not sure that I want to call it goal. Maybe there is another word for it. Maybe it's not architecture. I understand why you're saying please don't call it architecture because architecture is.  
Something more detailed than what I'm looking for, but I actually think it is. Maybe there is another level of architecture that describes a high level of thinking, and maybe it should.

**Aaron Bockelie** 19:26  
Yeah.  
Well, you could call it architectural goal. I mean, you can turn architecture into goals, right?

**Val Levitan** 19:45  
I don't know.

**Aaron Bockelie** 19:46  
Well, you can. So in building something you could say our architectural goal is to have a lead a building lead score of at least 90.

**Val Levitan** 19:59  
OK, so we develop architectural goal, then we finalize.  
Finalize the Um.  
Uh.  
Repo taxonomy.

**Aaron Bockelie** 20:20  
Yeah, the repository taxonomy should be straightforward and easy. Architectural goals exist regardless of where the repos are at.

**Val Levitan** 20:31  
OK, then we develop. What would I call the?  
MVP architecture for POS deployment.

**Aaron Bockelie** 20:46  
I would call it the architecture minimum. You could call it minimum architecture.  
Minimum viable architecture. MVP stands for minimum viable product, so you could describe minimum viable architecture as a as an outcome. You have to be very careful that that does not becoming become the true architecture of things though.  
So one of the holy grails of architecture and software is to have scalable architecture, right?

**Val Levitan** 21:24  
Well, I actually like saying scalable architecture because when we discuss as you, you know, as I like to call it highest level architecture or architectural goals.

**Aaron Bockelie** 21:39  
Yeah.

**Val Levitan** 21:40  
Maybe it's part of the scalability.

**Aaron Bockelie** 21:43  
Right. And but you then. But then you can't stop at just saying it. You have to define what scaling means.

**Val Levitan** 21:51  
Explain that.

**Aaron Bockelie** 21:52  
You can't just say it's scalable. You have to do you have to describe the dimensions in which you're scaling into.

**Val Levitan** 22:02  
Well, yes, but I cannot.  
I don't think any of us, and I spoke already to Will and to Nathan and to Pavel. None of us see the architecture that it will evolve in to its fullest degree. We all there are many moving blocks.  
And we just can't put everything together. It takes us time. But if I stop everything and say put the architecture together so it scales to what it will migrate to two or five years from now, then everything will stop and we will get paralyzed. We won't be able to do anything. That's why.  
I am calling it high level architecture.

**Aaron Bockelie** 22:47  
Have you considered hiring a payment systems architect?

**Val Levitan** 22:52  
Well, because it's not a payment system architect I need, I need to have a payment system architect. I need to have a back end cater to transactional architecture, to HHR and to the conventional slot machines because everything will eventually talk to the back end.  
And.  
And I understand we don't want to call it back end anymore. We want to call it orchestration and.  
Forgot the name of it.  
Platform but.

**Aaron Bockelie** 23:32  
Right.

**Val Levitan** 23:35  
In my mind, that's simple back end. So there will be some sort of back end and the HHR products and the transactional products and the conventional slot machines, they will all talk to that back end and there will be a set of services that talk.  
Back to these products.

**Aaron Bockelie** 23:56  
Right.

**Val Levitan** 23:57  
They're all will be.  
Writing on a.  
On on this back end architecture or will become a part of this back end architecture. But none of us, even if we sit in the room, all of us together, none of us can see how it will be two years from now.  
We can, we can only say, well, the HHR will need these, these, these blocks, the transactional. Right now we see that it needs these blocks or these services or this set of tools.

**Aaron Bockelie** 24:18  
O.  
I would be taking a customer oriented perspective on what the architecture is going to look like. Here's an example. Will will prepaid Visa debit cards be used in the Georgia market for payment of of games or services?  
Like this is kind of a question.

**Val Levitan** 24:54  
Well, it doesn't matter what will be used. We know that we will be talking to a cloud service provided by income for a validation of cards.

**Aaron Bockelie** 25:03  
OK.  
So you have a validation service that probably will remain relatively static for a long time. So then that is a method that your architecture will use for the next five years. So that's a that's a point. You can stick a pin on the map, right?

**Val Levitan** 25:11  
Yeah.  
So.  
Right. Yeah. And so.

**Aaron Bockelie** 25:25  
You just need to start doing that.

**Val Levitan** 25:25  
Yeah. And we already and we already know that and we were factoring the same.

**Aaron Bockelie** 25:30  
OK, so I think that you actually do have a lot of the ability to define what it's going to look like, but you got to commit to it.

**Val Levitan** 25:38  
Correct. But I cannot. I can. I can define to a relative degree to a relative comfort. I can define transactional part of it. I can fully define the HHR part of it and I can define to a very high degree the.

**Aaron Bockelie** 25:49  
Right.

**Val Levitan** 25:58  
Regular slot machine architecture. But what I don't have time right now is to think through all the integrational modules and to say this is the overall architecture. This is how the whole thing is going to work. This is how the back office, sorry, the back end will look like.

**Aaron Bockelie** 26:00  
Yeah.

**Val Levitan** 26:20  
It just it it just needs time. And if I if I take my engineers and devote them to that, then they will not be rolling out the POS system. Instead, I could say, well, there are known blocks without which we can absolutely not.

**Aaron Bockelie** 26:23  
Right.

**Val Levitan** 26:38  
Exist and this is this part of cloud architecture that needs to talk to a third party validation system without.

**Aaron Bockelie** 26:47  
The way I the way I'm feeling, it's it's based on a feeling just by kind of knowing what I've seen of the code is that you have a big monolithic systems architecture for the back end of everything right now. It's a big Java monolith and you're basically going to ask them to add another.

**Val Levitan** 27:00  
Yes.  
I will not. I will. I will not. I will not. And you need to stop thinking about it and you need to stop talking about it because it's tiring. I understand that I have the old system that was designed 30 years ago.

**Aaron Bockelie** 27:05  
Wrinkle to that, to that monolith, and then you kind of go with it.

**Val Levitan** 27:24  
This is something that in existence right now, it's a monolithic system. We're all quite aware that it needs to get chopped up, redesigned into services. We all talk about it. We all understand this.  
So we need to stop going back to that monolithic system. What the intent is, is to take the tribal knowledge and to take the know how.

**Aaron Bockelie** 27:42  
OK, so so the other half.

**Val Levitan** 27:53  
Of how that system is designed, split it into services and then yank couple of services and design a new cloud service that could run the MVPS.  
For the POS.

**Aaron Bockelie** 28:14  
So.  
You can use the existing stuff that you've built. You can't really use the code from it. What you can use from it is the purpose of it and its intentions. OK.

**Val Levitan** 28:26  
No.  
Radar.

**Aaron Bockelie** 28:34  
In order to be able to make something new, I I just know from watching team sizes, unless they're extremely competent and do this all the time, asking a very small team to build from scratch a.  
Microservices serverless architecture for payment systems in only four months, five months, four months is probably not going to very well succeed unless you're copying from another pattern or inheriting another design pattern that you can then just.  
Basically adopt as yours.  
So that will force an architect a set of architectural decisions, because in order to move at that speed, you can't produce it from first principles in that amount of time.  
You have to basically take somebody else's understanding of the design pattern that's validated and known, adopted it as yours, and then iterate on it from there.  
O if you're looking for a minimum viable system for justice the O aspect of it.  
Perhaps that is actually the the then the goal. And So what you do is before cart before the horse thing going on here a little bit, which is don't doubt before you've validated your doubt in this case, so.  
Instead now you can set up the remembering the division of of of concerns. As the executive you will say we cannot use our legacy system for this. It must be serverless architecture that is cloud based first.  
It cannot use big monolithic SQL databases to do this work, and it must be understandable by other people. And that's where people like Nathan could come in and sort of define that more clearly with you, not as a technical advocate, but as a.  
Sort of business, technical business architect or advisor kind of perspective. Once these requirements are defined this way, then you can go, OK, Dima, this is the set of requirements and goals that I'm looking for for the payment system in January.

**Val Levitan** 30:55  
Yes.

**Aaron Bockelie** 30:59  
What are your? I need you to review and understand them and provide to us your initial assessment as to how you think this is going to go together. And he's going to go, OK, let me go work on it. I'll get back to you in a week.  
And then you're going to listen to these, his feedback as to what he's going to say and then the constructive doubt.

**Val Levitan** 31:23  
OK.

**Aaron Bockelie** 31:25  
That you can then introduce in this review of his work. That's that sandwich thing I was talking about, allows you to constructively doubt what he's saying. If he if he tells you, well, actually we're going to use our existing architecture, it's perfectly fine.

**Val Levitan** 31:34  
But.

**Aaron Bockelie** 31:41  
Then you can say and how does that fulfill my desire for serverless architecture on cloud platforms? And he should be able to explain it and he might have a very clever way that he's pivoted into it, so but if he doesn't.  
Then it's a matter of OK, this won't work. You need to go understand this requirement better because he didn't understand you when you asked the requirements and you go and iterate on that. So maybe it's not a week, maybe it's three days. You give him a couple days to consider it.  
And this the cycle has to go on several times. These sandwiches that you're consuming over time basically, and eventually you're going to get to the point to where both sides have negotiated the conversation and and requirements to the point of acceptance.  
And while you're doing that, you're mindful of the amount of work that you're actually placing out in front of you because you're like, holy crap, this is going to take like 14 months to get to this point. Not even acceptable. We can't even because our one of our requirements is delivery of MVP by January.  
So what you might end up doing is inadvertently forcing the engineering iron triangle of fast, cheap, good, pick two, right? And if you end up with asking for something in too too soon of a time, it's going to be.  
Fast and cheap.

**Val Levitan** 33:08  
So remember this conversation? Let's stop.

**Aaron Bockelie** 33:12  
Sure.

**Val Levitan** 33:13  
We made a point. Remember where we are because this is the course we need to adapt now.

**Aaron Bockelie** 33:20  
Yep.

**Val Levitan** 33:22  
And so we will refocus and we will just use minimum.

**Aaron Bockelie** 33:29  
Minimum viable roduct.

**Val Levitan** 33:31  
Well, no minimum structural changes that we implemented in our development cycle to get there and we will forego all other initiatives, disciplines, practices that we want to implement that we will not.  
Cause any slowdown. OK, let's let's have a 14 minutes break and then essential invite for the git repo meeting.

**Aaron Bockelie** 33:53  
Yeah.

**Val Levitan** stopped transcription