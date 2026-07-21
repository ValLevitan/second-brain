**Transcript**

9 September 2025, 12:20pm

**Val Levitan** started transcription

**Will Jones** 0:03  
OK, so my thoughts Val, First off that when?  
When?  
When the problem that's being posed or the what I guess the business problem that we're trying to solve with the terms with the managing the transactions, I think that one that pops out to me and just from my experience previously it tells me this is that there's.  
Lot of points of failure in the system and then we have to explore those to ensure we have a concrete solution end to end so that we don't, as I said before, either have the potential to lose money or double funds. I've seen both happen with systems in the past, so I know that it's possible to do it with best.

0:47  
Oh.

**Will Jones** 0:50  
Intentions and just miss a nuanced point, especially when we're talking about legacy devices and having to utilize those serial based protocols, some of which are not actually. You have to watch out for the gotcha points, let's call it. Some of them, their protocols are not sufficient to entirely.  
For transactions. So you have to not assume anything along the way. So I think that that's probably what jumps out at me as saying, hey, we've got to spend some time looking at this in detail. So the developers who are developing understand the nuances, understand the potential gotchas.  
Because that if that doesn't work well, we have not only a major problem, but I think we also have a product that is going to be really not, it's not going to be supported in the field. You know when you when you start getting that first bad transaction, you get a really difficult time pushing more of it. So, so that's that's the starter.  
I guess. And that's just in the back of my head. Your question's a greater one. Hey, let's talk about how we can evolve from where we are to a different architecture and then be able to take on these challenges more effectively in the future. Exactly. Yeah. So.  
In that the discussions that we had pin, you know or say I'm pinning this this to the requirement that sorry, I'm trying to remember the the gift card issuer's name again. I don't have it in front of me. What's that?

**Val Levitan** 2:18  
Income. Income.

**Will Jones** 2:19  
Income, yes. So income requiring us to be a cloud to cloud or I should say B to B in the back end architecture is the place that I think is the the the focus right now or is the is the first need.  
To solve. So in doing that, we're gonna have to move if we're gonna be hosting in Azure. From what I've heard, that's what I was told is the most likely cloud service. If we're gonna be hosting in Azure and the team hasn't created cloud services before, there's not a barrier to.  
Entry, but there's definitely a learning that's going to have to occur, and there's going to be this functionality that is not the actual functionality of the product, but functionality of justice getting to the point where we can develop and host in the cloud.  
So, so there's a little bit more work there than than probably is perceived right now, but maybe I'm wrong in order just to to solve that problem. Then this other picture of seeing, you know, realizing an architecture that is going to be more extensible, do the different.  
Things for HHR versus Georgia versus the markets that you have in in I believe South Dakota, you know finding that is is more I think looking at the existing CMS or the functions that the existing CMS provides.  
And identifying which are the most, what are the pain points and let's talk about those in terms of the priority or what's the effect on the business and really start to see how we could deal with those pain points and realize a new architecture at the same time, so.

**Val Levitan** 3:56  
OK.

**Will Jones** 4:13  
Meaning that each one of the services that may not be sufficient for our needs in the future but was in our past and it's got some kind of, you know, it's got something that's causing our development team or our business to not function fully.  
Then we'll take those, identify what we can do better on that, and try to realize it in the new architecture system. In other words, taking onesies out of this older paradigm and moving it over and using something which you know, being able to do it in such a way so it's seamless.  
To the the devices that are that we're supporting all the slots and other things on the floor. So that that's where I think you know I I have a say a blueprint if that's the way to call it. I have a an experience of dealing with legacy systems.  
And migrating them over to newer architectures that match the needs of the future, and doing it in such a way that it can be done piece by piece. Not so that we have a better, more perfect solution, but that we have a realistic journey.  
To get there, meaning that we we discover what's the biggest problem, we solve that problem, we move over into the newer system and hopefully that means our business can, you know, can thrive and do that more quickly in the future. And it's no longer a problem. We don't have to look to that. We in fact we actually usually anchor to that.  
And then you find the next one, you keep moving it over that way. So, so I know I've I've used more of just very broad terms, but specifically with the CMS Val there, you know in the discussions, minimal discussions that we've had and I've explored what it does.  
It does have a function that that works, you know, works well enough for what you know things we need to do, except it needs to be expanded maybe to do more with this specific problem in Georgia with the operators and what operator control is versus what.  
JBL can actually see and control. So there's some area there that we probably have the potential to start working on, you know, moving towards if it's a cloud based architecture, but moving towards what we envision in the future.  
But I don't think that it's likely that we're going to uproot everything that is all you know this to with Georgia and put it into a cloud system in a short order. It seems to me like that would be.  
Less advantageous for the Business School of this, which is definitely getting there 1st and being the one to attack the problem, be in the right place at the right time. So yeah, so that that's my bigger picture thoughts First off.  
There's some nuances in here. Identify them, make sure the team's equipped to solve them, because if we don't solve them, I see major, you know, really disruption in our our relationship with the customers, disruption not being able to successfully roll it out quickly.

**Val Levitan** 7:19  
Yes.

**Will Jones** 7:28  
If we don't identify those and then for the greater good, I don't think I have an answer to say this piece needs to be the first one that we do in the new architecture, but working with.  
You know, working with the team in Minsk, I suppose, you know Pavel and his crew, then we can identify what are the bigger pain points and see what we might be able to do first in that respect. But obviously the as I mentioned before the the B2B with income hosting it in Azure.  
or whichever cloud environment we need to put it into is going to be you know a new experience for everyone, I believe, and something that's going to take a little bit of time to do it right.

**Val Levitan** 8:17  
So in in my view, one of the issues that I'm personally having is finding an alignment between the executive branch and the developers.

**Will Jones** 8:23  
Mm.  
Hmm.

**Val Levitan** 8:31  
And.  
The only way I understand how to get this alignment is on the executive branch, and this is where I put you in particularly. So I look at you as an executive. I'm saying, OK, can you develop a set of?  
Or name physically name the the initiative or set of initiatives, split them into products and for each product develop a set of capabilities.  
And if this is then done.  
On the executive side, then we can have productive conversation of which capability in particularly we want to implement first.  
If we understand that, we can then develop a set of features for each of those capabilities that correspond to a particular use case.

**Will Jones** 9:31  
Mhm.

**Val Levitan** 9:33  
And then we could say, OK, great, let's start with feature 17 and 9.  
Start implementing them because that will enable us to get capability #1 going in the market for this particular product. That's the only.

**Will Jones** 9:50  
Mm-hmm.

**Val Levitan** 9:55  
Way I can see us getting aligned between the entire chain of people that are involved in this particular process.

**Will Jones** 9:58  
OK.  
And when you say alignment, let me make sure I understand more specifically what alignment is. Is alignment more the direction of we're choosing to do things on the legacy platform time and time again?  
I'm going to just use this term say because it's the easiest and yet I want to be able to start migrating or moving towards what the future vision is, no?

**Val Levitan** 10:31  
I I am not discussing a solution.

**Will Jones** 10:34  
OK, got it.

**Val Levitan** 10:36  
So this is before it gets to engineers and they say, well, OK, if you want this capability enabled by January 1st, the only engineering solution I could give you is to stick with what we have.  
Have we slightly change this and this and this and roll it out in this form. I cannot give you anything else.

**Will Jones** 11:05  
Is is in that is sorry, I didn't get if that's acceptable alignment or if that's OK, OK.

**Val Levitan** 11:10  
Yeah.  
I I I cannot dictate engineering solutions.

**Will Jones** 11:15  
Exactly. I was. I was wondering if you were. I mean then the the answer if if if that wasn't acceptable, the answer is is coming back to agreeing upon what the objective is, which is probably something watered down or different, which might actually then achieve whatever that expectation is, but I don't suggest.  
Just that the expectation of a solution is not the where to start with engineering. It's definitely the expectation of the feature, the expectation of what it's going to do, not how it's going to do it exactly.

**Val Levitan** 11:48  
Correct. Exactly. You nailed it. What it's going to do, not not how it's going to do it. How it's going to do it can only come after we understand what it needs to do at what time.

**Will Jones** 11:55  
Exactly, yeah.  
Yeah.  
Yes, yeah, yeah, understood. And there obviously can be that time pressure and that's that's that's necessary honestly.

**Val Levitan** 12:10  
And so.  
And and so first of all I had my question was few fold #1 is.

**Will Jones** 12:18  
Hmm.

**Val Levitan** 12:22  
Can we do it?

**Will Jones** 12:24  
Yeah.

**Val Levitan** 12:24  
In a in a, you know large, you know the large question, can we do it #2 how do we get aligned?

**Will Jones** 12:30  
Yeah.

**Val Levitan** 12:40  
And so it.

**Will Jones** 12:40  
And I I where do you feel the alignment is not you know where where the alignment is truly broken and that you need more you know alignment on that. Is it the expectation of what we're trying to achieve by by the given date is that is that where you feel the.  
Alignment is mostly, you know, broken.

**Val Levitan** 12:59  
I'm not saying that it's broken. I'm saying that it probably exists in everybody's mind in its own shape and form. And so I'm just saying let's take everybody's perception of an alignment and let's actually expose it in visual.

**Will Jones** 13:08  
OK.

**Val Levitan** 13:19  
Presentation where we say here's the list of products that we're gonna roll out in the next two years, including HHR. This is the overall block diagram of architecture, how things will work.

**Will Jones** 13:29  
Mhm.

**Val Levitan** 13:35  
Five years from now.  
And this is what's needed today for this initiative, for this product, let's say initiative is transactional operations, product is POS point of sales.  
Date is January 1st. Capability will be, I don't know, nothing comes to mind, but let's say except or or to be able to convert player issue card or player winnings and onto a card.

**Will Jones** 13:59  
Yeah.  
But.  
Yeah, issue a card or something, yeah.  
Yeah.

**Val Levitan** 14:12  
That's the capability. It will consist of 50 features that we can think of, maybe more, but here's the three features that's required right now for January 1st. So implementing these particular three or five features or 10.

**Will Jones** 14:14  
Mm-hmm.

**Val Levitan** 14:29  
For this particular capability for this particular product, which is the OS for this particular initiative, which is transactional equipment.  
We will engage our current CMS architecture, this this particular tech stock with these particular, I don't know, capabilities or features or.  
4.

**Will Jones** 14:57  
Hmm.

**Val Levitan** 14:57  
Yeah. So that today, that chain doesn't exist. Yeah, I mean, it exists maybe in everybody's mind, but I'm afraid that everybody's mind is slightly different and this is what I'm seeking an alignment for.

**Will Jones** 15:05  
Mhm.  
OK. In that in the conversations, obviously Pavel being an integral part of the conversations or the meetings that have already occurred on this, you know on this functionality for Georgia, that obviously is.  
You know, him hearing and that he has a perspective on what he's hearing versus anybody else who's on the meetings. But is it is then taking the discussions that have occurred, the ones that I probably haven't been part of too, is it taking those discussions and being able to visually see them, whether it's in words or pictures?  
What expectations are and having each, you know, each not responsible, but each person who who plays a part in that, have them, you know, sign up or sign off on that picture is that.  
That the kind of expectations you have for how you know how alignment occurs or is there a different kind of view of you know of that alignment?

**Val Levitan** 16:14  
Well, look, I don't know. Alignment could probably be achieved on multiple levels. Maybe it's a set of conversations, maybe it's a set of documents, maybe it's a set of presentations, maybe it's a mixture of all three or a few. I don't know.

**Will Jones** 16:21  
Yeah.

**Val Levitan** 16:32  
It depends. I would like to see everybody eyes.

**Will Jones** 16:33  
Mm.

**Val Levitan** 16:41  
Beaming with comprehension and.  
Um.  
Either questions or agreement. Like I have not seen this physically played out in a group, so I honestly don't know what level of comprehension everybody is at. I'll give you an example.

**Will Jones** 17:03  
OK.  
Yeah, I was gonna ask that.

**Val Levitan** 17:06  
Of my of my of my personal recent evolution in one of the meetings so.  
When we validate a card, sorry, when we when we validate a transaction through income.  
And we allow winnings to be deposited on the credit card, on the debit card.

**Will Jones** 17:36  
Mm-hmm.

**Val Levitan** 17:37  
This moment player walks away with money.  
The this money exists right now in the form of a cash sitting in the machine belonging to an operator sitting in a location. The location owner will overnight take possession of cash.  
So that's his cash. He's not in a loss.

**Will Jones** 18:06  
Mhm.

**Val Levitan** 18:06  
JVL now is in a position where we don't have this cash.

**Will Jones** 18:14  
Yes.

**Val Levitan** 18:14  
But our money is already obligated to income. We we we encumbered this amount and we owe it to income. We hold it in reserve.

**Will Jones** 18:19  
Yes.  
Mhm.

**Val Levitan** 18:29  
In our bank to be swiped the following day through an ACH, the money will be gone, but we physically don't have the money.

**Will Jones** 18:37  
Yes, yeah.

**Val Levitan** 18:39  
So it is extremely dangerous situation for JVL. I don't know what happened to my camera.

**Will Jones** 18:43  
Mm-hmm.  
OK, I can still hear you just fine.

**Val Levitan** 18:48  
One second.  
Yeah.  
Oh, is it a gesticulation?

**Will Jones** 18:56  
I don't know. It's good for me.

**Val Levitan** 18:59  
Oh, OK, yeah. So you see me there.

**Will Jones** 19:02  
Yes, Yep.

**Val Levitan** 19:04  
So as I was saying, this amount has been already encumbered.

**Will Jones** 19:07  
Yeah, there's certainly a risk.  
Mhm.

**Val Levitan** 19:13  
But it's not in our bank yet. So I was having negotiations with the banks that we deal with to figure out the solution of how we could immediately ACH the money from.

**Will Jones** 19:14  
Yeah, absolutely.

**Val Levitan** 19:32  
The location to our account that night that end of day.

**Will Jones** 19:35  
Mhm.  
Yeah.

**Val Levitan** 19:41  
End of day I consider to be 3:00 AM.  
Or 4:00 AM, doesn't matter. So at 4:00 AM I need to send a signal.

**Will Jones** 19:50  
Mm.  
Um.

**Val Levitan** 19:54  
To all of the locations to swipe their accounts and to bring money into my account.

**Will Jones** 20:00  
Mhm.

**Val Levitan** 20:02  
And I was having difficulty negotiating these things with the bank, disagreement with with my banks.

**Will Jones** 20:09  
Yeah, OK.

**Val Levitan** 20:11  
In one of the meetings, recent meetings a week ago, Nathan presented me with the solution that there are specialized companies in the business that all they do is the ACH transfers between accounts.  
That's that's that's their business, that's their nature of business. So it's not the banks that really handle this transactions, it's this electronic fintech companies.

**Will Jones** 20:31  
Mhm.  
Mhm.

**Val Levitan** 20:43  
That specialize in a CH in these amounts and literally they specialize in moving trillions of dollars back and forth and they do it extremely efficiently.  
And the whole process is very efficient. I didn't know that, but that I'm saying that the light bulb came up and I'm saying, wow, this must be a part of our solution. We should immediately start working in contracting these companies or finding a company that we can contract.  
To carry these transactions for us. This has not been part of our architecture.

**Will Jones** 21:21  
Mm-hmm.  
OK, Yep.

**Val Levitan** 21:26  
So that's a discovery that I made for myself on the executive level.

**Will Jones** 21:31  
Mhm.

**Val Levitan** 21:32  
I wonder if such discoveries exist for the developers. Well, we are not going to use this tech stock, but the other tech stock. I I don't know if this conversation even take place.

**Will Jones** 21:46  
Mhm.

**Val Levitan** 21:46  
We have to stimulate these conversations. The only way we can stimulate these conversations is when we define the capability of a product.  
And slit the capability into a set of features.  
And that has not happened yet.

**Will Jones** 22:04  
Yeah. And I think that that so Val, where I would go at with that is that you know in in this.

**Val Levitan** 22:08  
I don't know actually if I I don't know if I complicated the matter or answered your question, and maybe I deviated from the subject a little bit. But anyways, we are here now.

**Will Jones** 22:17  
No, I was looking for examples and and certainly you know what where you what stimulates this conversation is important to understand. So what I would say is that all development work is going to have a set of risks and obviously that's what I believe.  
You know, the manager, the the director, the person who's more organizing the teams for it needs to be very good at, you know, being able to identify those risks, keep them in vision and mitigate them. Of course, in any this risk that you talk about is less technical. I mean, though it has a technical solution, it's less technical and it's.  
Much more just an accounting one, a big problem that the liability is on JBL's hands to be able to pay income for the card that they just issues issued and we're having to trust the actual operators.  
To make that transfer into an account, you know, into something that JVL can use to pay off, you know, the the, you know, income for issuing this, you know, this actual financial instrument, this card that's being walked away with.  
So yeah, completely understand that being a particular one that if the team doesn't understand that the consequences of it or the the risk there that they're not, they're under emphasizing the, you know, what has to be done. I don't know how much of that is a developer making.  
You know implementing and or just the the the network that we have in terms of moving the monies into the right account but certainly understood that it's you know it's it's a it's a significant piece of the puzzle and we better have both a report say what a you know an operator is is.  
Due to pay by that 4:00 AM and also some kind of check to verify that it was paid immediately so that every day we know exactly what liabilities didn't get met and then we're able to, you know, quickly work on that.

**Val Levitan** 24:26  
So the moment there is a requirement to move money at 3:00 AM.  
That means the generation of reporting and availability of those reconciliation reports obviously creates a technological challenge that needs to be resolved.

**Will Jones** 24:46  
Mhm.  
Mm-hmm.

**Val Levitan** 24:49  
And that's what you are highlighting. You're saying, well, now that we have a requirement to move money at 3:00 AM for the previous date, then what are my technological challenges for reporting reconciliation if there is, I don't know, third party application?  
That is running at the same time, how stable it should be, etc. So there will be a set of engineering questions that will be addressed based on the requirement and based on certain capability.

**Will Jones** 25:15  
Mhm.  
Yeah. And I wonder some of that, you know, as I said, some of that system is going to be outside of the CMS. It's just moving money through accounts. Being able to access that data in a timely fashion may not be.

**Val Levitan** 25:25  
Or set of requirements.

**Will Jones** 25:40  
You know, may take some effort to make sure that we can get accurate reconciled, you know, transactional information that isn't just on our side, but the is the perspective of that ACH or perspective of the income or whatnot.  
For the transactions that have occurred.

**Val Levitan** 25:59  
So then to fine tune on my question or the the subject of this conversation, how do we now reach the alignment that I'm looking for or that transparency, not even an alignment. Let's first talk about transparency.

**Will Jones** 26:03  
Hmm.

**Val Levitan** 26:16  
I guess having all the requirements properly listed and documented and develop a set of capabilities from it.

**Will Jones** 26:17  
Mhm.  
Mhm.  
Mhm.  
Yeah, I think that, um.  
There's in in this solution, there's known.  
You know, known entities that are going to play a part. First off, there's the legacy machine or the machine that's actually where the funds start. Second off, if I go way over to the other side, there's income where the funds end in that way, where they issue the card from it.  
Then there's of course midpoints where it goes through. I think that the that for my own purposes of just understanding each one of those entities.  
Is in, you know, is imperative to be able to identify the, you know, the functional requirements that are going to be asked of the system. So obviously we know that if it starts at a legacy machine, we're going to have to account or do some kind of accounting.  
Against the machine via SASS meters or some other to say how much was the credit meter? What was the transaction off? Maybe know about, you know, all the transactions that led up to it too, but we'll have something there to be able to validate that when they said they cashed out 100 bucks that we can tell that it truly cashed out 100 bucks.  
And then of course, income receives the, you know, the amount of funds that get issued to it when it's going to, you know, pay out the the card. So again, on that side, we're going to be able to understand what's gone in, what the expectations are and reconcile that.  
So understanding all the pieces in the movement is I think critical and then taking that information and being able to, you know, state it.  
I don't know with the Minsk people, it's yeah, visually that's that transaction is is extremely interesting to see. So I would say for the problem that we're looking at right now about the first part I would take it is to make sure that we understand all the pieces the you know this all the moving parts.  
Understand the risks in, you know, in the information we need to get out of them and have a visual of it and then adapt that into something that is a more call it well defined structure definition of what needs to occur.  
With the expectation then that the you know the Pavel or the developers that are working for Pavel would be able to to visually see and read the definition, probably translated to you know to Russian.  
And and really understand what the responsibility of each component is.  
Yeah. Then I would, I would see that as quote alignment with the, you know, what needs to occur. And then of course the how is going to be defined more on basis of what we're hoping to achieve with the architectural evolution that's being proposed.

**Val Levitan** 29:28  
Still wait.  
So where do you see your role in in this?

**Will Jones** 29:43  
Where do I see my role in this? How do I help facilitate the the understanding?

**Val Levitan** 29:54  
From a technical perspective, I see initially your role in defining in in helping us define all of the requirements for the entire system.

**Will Jones** 29:56  
M.  
Hmm.

**Val Levitan** 30:07  
And a set of caabilities.

**Will Jones** 30:12  
I yeah, so definitely you know doing what facilitating the same thing that that I did before in terms of writing requirements and hopefully identifying the user stories that that come out of those requirements.  
Those requirements I I I don't have a problem with the use case. I I prefer user stories because I really feel that they they focus on the the what and less on the how. And I I'm not saying a user use case can't be written well, but I feel like the.  
The user story has more personality and it tells you more about what the what the perspective of the actual user is. So you know that you're achieving what the user needs and less what functionally or what just what has been somebody's.  
Interpretation of what the user needs. So anyway, yeah, I feel like I could definitely help with that again as far as trying to, you know, trying to.  
Help learning. I guess I'm trying to say coaching mentoring is is a is a word that I could come up but help the learning process of going from definition to action. I can certainly you know be a facilitator of that with Pavel and just.  
You know help guide him on on areas of of that. I don't know if that's what you're you're you're interested in in me mentoring in terms of Pavel side or or just being a facilitator of the information.  
But I can definitely be a conduit of that.

**Val Levitan** 32:02  
Well, first of all, on my my personal comment, and I'm not an expert of any sort, I I I am just really a novice trying to.

**Will Jones** 32:08  
Hmm.

**Val Levitan** 32:16  
Take a grip of the the.  
New style of development. So let me comment my views on use cases versus user stories. In my view, use cases is more of a front end.

**Will Jones** 32:22  
Hmm.

**Val Levitan** 32:36  
Um.  
Action where we describe how a product is used, a product on a product level. In my view, use cases are more related to feature level.  
So this is closer to user story as it applies to an implementation or development of a particular feature.  
If if you feel if if it's enjoyable for you and you feel comfortable right writing user use cases.  
Sorry, user stories, which applies more on the development side of things. That is definitely fantastic.  
Because use cases could be covered by somebody like one.

**Will Jones** 33:36  
I would actually I, you know, maybe this is just a a perspective that is not justified in that way, but I would I would say use cases in my maybe opinion are actually more functional.  
And more from it's like the perspective of the developer way back when, when use cases were thought up by Booch and whoever else it was, you know, they they said great developers are just going out and coding, but they don't actually produce what what's necessary or what needs to be, you know, needs to be done for the.  
The user. So I'm going to go out and try to get closer to that by saying here's a use case, this is how my system's going to be used, and here's another use case. This is how my system's going to use. If I detail all the use cases, I should be able to sum that up into a system that provides all the different value that it's supposed to.  
But I think it was from the perspective of the developer or from the engineering perspective how to define that less from say the end user perspective how you can define what what they need. So that's where I think user stories and you know the agile development process.  
Came into the picture where somebody said, you know what, this was really a developer driven perspective and use case and how you structure them and how you collect as many as you can. And instead I just want to write a story that describes what my user is going to do, what they do with every day. Tell me what they they sit down at work and.  
They needed to do and hopefully make it so that it's defined encompasses an actual singular action that they're going to do. So it was easier to write it from, you know, in language. It was easier to write it from the perspective of the user who was providing some kind of value to a business.  
This and say as a dot dot dot I want to dot dot dot. So my perspective Val is actually the use case or sorry, the user story is more valuable to the end user, meaning that if that actually defines what the true end users.  
Is going to do and we are able to achieve that. We can go through and say that through the acceptance criteria that we've achieved what they needed. We've provided a better solution than if we went from quote the developer's perspective and try to go through each function and define how the functions need to to work.

**Val Levitan** 35:50  
It.

**Will Jones** 36:08  
I do believe that they both meet in the middle and they're really close and one's a little bit more user perspective in the the story and one's a little bit more system perspective. So that's my, you know, that's my thinking of of how.  
These two compete with each other and that's why I prefer a user story because I think it's a little closer to the user who's going to use it as opposed to a use case. However, I'm not going to say that if you wrote either one well and you took that and you really understand what you're producing and then can define a system.

**Val Levitan** 36:32  
Yes.

**Will Jones** 36:44  
That does that well. You're going to be successful either case. So I don't think you can. I I think you can be successful either way. I don't, you know, one or the other is fine. But all that said, yeah.

**Val Levitan** 36:53  
OK, we only have few. We only have few minutes left. I don't want to go over our time, so let.

**Will Jones** 36:59  
Yeah, it's splitting hairs anyways. Either way, writing a definition for what the user, you know, doing the same things it did for HHR can certainly do that for for this endeavor too. I really would like to understand.  
The the the details of that transaction end to end and if you know make sure that that the risks at each point are identified such as the risk of the operator not paying JVL in a timely manner and if that's if that's that's a that's you know a functional feature I see.  
to find that JVL needs the ability to quickly identify if a given operator did not, you know, did not settle up by that 3:00 or 4:00 AM so that it understands that there's a liability now that needs to be dealt with.

**Val Levitan** 37:51  
OK. Again, because of the time constraint that we're dealing with here, I'd like to wrap up our meeting in a couple of minutes. I I'd like to understand the following. Still, we're dealing with the overall architecture at some final point.

**Will Jones** 37:56  
Mm.  
Mhm.  
Mhm.  
Mhm.

**Val Levitan** 38:09  
Years from now of how the entire architecture will function, take into account transactional products, the HHR and the conventional CMS in the form that it is right now. How do we combine it into?  
A singular architecture that we could start with and in in your opinion, is there such singular architecture or is it an exercise of fatality trying to combine everything into one thing?  
And maybe let's not even think about how to combine everything together. Let's just address mini applications, local architecture of how it will function and then somehow tie it together in a large thing.

**Will Jones** 38:52  
Each.  
Hmm.

**Val Levitan** 39:03  
That works.

**Will Jones** 39:09  
Each. No matter how. Yeah, I'm not. I'm trying to make this not too far from what your question is. No matter how you get to that end result, you're still gonna be doing each thing individually. So you're not gonna do the whole thing all at once.  
Now having a vision for what that architecture might be in, you know, three months time or whatever, not even setting a date to it, but what the what we'd like it to fit into is a good guide for the direction that we're going with as long as it has, you know, purpose on what that architecture is, then we.  
Can conform to it as we go forward, but you're still going to do each individual piece. Is there an evolutionary architecture? Certainly. Is that evolution, you know, is that architecture at the end line known at this point? Not that I've witnessed in the conversations.  
It's just it's a concept or a idea that we like to be able to achieve. And I would say that there's, you know, the reason why we want to do that is for, well, I believe anyways would be for the business goal, for agility, for you know, being able to have maybe less cost and.  
And how we house our our services. So, so I don't think it's futile. I don't think it's not the right endeavor. I think that it's just going to be done on each individual piece file and the only one that I saw that's definitive and moving towards something different than what was done in the past.  
Is that B2B transaction and then these other pieces, I I think that there's probably a great deal of benefit in making it so that they're hosted in the cloud and not running on on-prem or not assumed to run only on on-prem servers.  
Is that's going to be beneficial. But yeah, that I I think you're you're probably wanting more of a concrete answer to say yes, that's the right direction to go. I I don't know that it's the wrong direction. I just think that it's going to be individually defined.  
By the need to get to that place right now, because there's such a, there's such a significant legacy system that weren't, you know, gonna have to do it piece by piece.

**Val Levitan** 41:30  
I I think, I think what I'm what I'm reading I guess from this conversation is that I I think what you're saying is there's no harm in addressing the immediate concerns and getting an affair going.  
And start generating money. And then maybe it's not such a big deal, even if you don't see the end result and how everything comes together. Maybe even to an extent that a certain module might be reworked.

**Will Jones** 41:56  
It's.

**Val Levitan** 42:02  
It's not such a big harm because to visualize the entire system to a perfection will either be extremely difficult or we have to overbuild quite a bit in order to achieve that.

**Will Jones** 42:14  
Yeah, that that that that was great, you know, spoken very well. So absolutely I agree with what you just said. And on top of that or is it in addition to that, I would say from this point now with the pressure of the timeline too.  
That most likely the direction, the vision for the future might not match what vision, where we'd want to be in the end. So I can see a definitive need right now. As I said, to host something in Azure is what I've been told, whether that's Azure or a different cloud service.  
That's fine, but to have a B2B connection to income to be able to make that, I would focus on that because that's going to do 2 things. One, it's going to solve an immediate business need and we're going to be able to hopefully get to this market faster than anyone else and get.  
And get good revenue from that. It's also going to give the team an experience they do not have right now. I don't believe they have the experience from talking with Pavel of setting up a DevOps pipeline that's going to be they're going to be coding on their.  
Machine, they're going to eventually hit return. This is done and submit and that's going to have to get deployed to an Azure, you know, cloud server and then that's going to be able to be the conduit between JVL and Incom.  
There's a lot of new muscles to, you know, to exercise there that they haven't done in the past. And once that's set up, I believe there'll be more realization of how we can continue to evolve, probably towards that same cloud architecture. I don't think we would go to a WS.  
If we've already gone to Azure for that, but how we can continue to leverage the ecosystem of services that are up there to create the next, I don't know, UI for an operator to log in and check their transactions or JBL to be able to go log in to be able to see exactly which operators.  
Didn't pay us here at 3:00 AM and have a, you know, a clear understanding of that every day. When we wake up and get into work at, you know, at 8:00 AM, we see that list and we can work on it, you know, work on that list.  
So from my perspective, for what you said is is true. From my perspective right now, I don't see a, you know, a compelling reason to eliminate the CMS all at once and move over. But also having a vision for what it's going to be, I believe is.  
You know, something we need to aspire to attain, but that shouldn't stop us from immediately working on the business need that we have.

**Val Levitan** 45:10  
OK, I need a little bit of time to process everything that we spoke about and with your permission I will approach you again just to regurgitate everything that we said and develop a plan on moving forward.

**Will Jones** 45:14  
Mm.  
Yep. So I think another side to it that I would say, Val, is that where I know I can help is in terms of being a conduit information both ways because that as development, you know.  
Needs to understand and eventually has, you know, perspective, their perspective on what they're trying to achieve that perspective or I should say the the, the definition of what that is, the challenges.  
Again, the risks that that that are associated with that need to be understood by the executive level too. So there's a conduit, you know, there's another information flow coming up too, which isn't always that easy to express. There's a technical definition of a problem. How do you express that?  
The business sense to say what you know, what we're trying, what we're faced with and why we're making these decisions, even if it doesn't, you know, doesn't necessarily take us in a direct path towards where we want to go. We may have challenges that we need to overcome that are going to take a couple more steps in between and not just.  
To leap forward. So it can go both ways, you know the information flow.

**Val Levitan** 46:42  
OK. Let me process everything that we said and I'll have another call with you.

**Will Jones** 46:44  
Yep.  
OK. Thanks, Val.

**Val Levitan** 46:49  
Thank you. Thank you for your time. Have a good day.

**Will Jones** 46:52  
OK, you too. Bye.

**Val Levitan** 46:53  
1.

**Val Levitan** stopped transcription