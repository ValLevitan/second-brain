**Game_Development-20260227_140542-Meeting Recording**

27 February 2026, 07:05pm

1h 14m 15s

**\
Val Levitan** started transcription

**\
Michael Gottlieb** 0:04\
Lena, you\'ve been you\'ve been working on the in game symbol recently, correct?

**\
Lena Zhukova** 0:08\
Yes, yes, I I hope like next week if you have time we we can start to review because I have already like a lot of material for you to discuss.

**\
Michael Gottlieb** 0:17\
Wonderful. OK, of course, of course. So we will move forward on evaluating GC361 next week and then following on from that is GC.\
360 Have you started on GC360 at all or not yet?

**\
Lena Zhukova** 0:37\
On on on bonus, not yet.

**\
Michael Gottlieb** 0:39\
OK, just making sure because it\'s currently says to do under GC 350 Twin Bison. I am continuing to work on GC356 which is the abstract. I\'m making good progress.

**\
Efim Podvoiski** 0:53\
Then.

**\
Michael Gottlieb** 0:54\
The primary focus has been getting the symbol hierarchy sorted because they\'re animals.

**\
Val Levitan** 1:04\
And can you open can can you open GC350?\
Thank you.\
I apologize for interruption.

**\
Michael Gottlieb** 1:20\
No, no, all good. All good. Outstanding. Yeah, I I will admit because my eyes do better with dark mode, so I actually look at it on my own monitor on a separate screen.

**\
Val Levitan** 1:30\
I I I figured. I figured, yeah.

**\
Michael Gottlieb** 1:32\
Yeah, yeah, yeah. So making good progress with the abstract on twin bison. The main focus is in getting the symbol hierarchy correct for the different animal.\
And one of the ideas I want to play with Lena is that when we go into free spins, there are such things as white bison. So I want to play with having the main game bison be the brown, but then when we have the locking until a line win.

**\
Efim Podvoiski** 2:02\
Mm-hmm.

**\
Lena Zhukova** 2:07\
Huh.

**\
Michael Gottlieb** 2:12\
Bison symbol in free spins. I\'d like to try that as a white bison to make it special and unique and magical, if you will. So we\'ll have a look at that.

**\
Lena Zhukova** 2:22\
And.

**\
Michael Gottlieb** 2:27\
Following through from that GC364, I will move on from Twin Bison to GC366, which is going to be the abstract for Lion\'s Riches. We\'ve already.\
Briefly discussed it and we have a sense of what we\'re going to do, primarily a revision to the pay table which has already been discussed.

**\
Lena Zhukova** 2:56\
And it would be nice to to create compart under 364 lines which is update following C GC366 abstract. Why I\'m telling it now because I I I\'m going to send this.

**\
Michael Gottlieb** 2:57\
Moving mhm.

**\
Lena Zhukova** 3:16\
Transcript of this meeting to Clayton. We are going to have our consultant. We are going to have meeting on Tuesday and we will try his updated MCP. If following this transcript, it can automatically create this issue.\
She.

**\
Val Levitan** 3:39\
Issue or or the art actually?

**\
Michael Gottlieb** 3:45\
The issue in JIRA, we all, yeah, yeah.

**\
Lena Zhukova** 3:46\
But the issue is like why Clayton is working on this MCP which is managing Jira\'s issues.

**\
Val Levitan** 3:57\
The the issue is absolutely not a problem to create in Jira from a transcript.

**\
Lena Zhukova** 4:01\
And not this images.

**\
Val Levitan** 4:05\
Oh, you mean attaching the image to it? So my point is the image. So how do you so you need to generate the compart image prior to that?\
Prior to that.\
And then lace that image somewhere in a.\
In, I don\'t know, repository and then pull from that repository and attach it to Jira task, right?

**\
Michael Gottlieb** 4:35\
Yeah, I think what we\'re specifically saying though is we need that functionality. The actual comp art for Lion\'s Riches doesn\'t need to be created before the comp art JIRA task is created. The the comp art task is created 1st and then on the completion of the task the asset is added. But I believe what Lena is saying is right now Clayton is.\
Still working on the functionality in his MCP to allow us to attach graphical images to JIRA items. Is that correct?

**\
Lena Zhukova** 5:02\
And yeah, and also following because we tried to to using like one of our like transcript from prior meetings to create issues in different spaces like 1 issue should be in concept, one issue should be in design and one some issue should be in production.\
And it fails so it failed. So now like we will try like following this transcript to create for example we will create issue. This one is going to be in concept space and like maybe some issue like other issue is going to be in design and then we will attach one site.\
We have for now we will experiment with some general image, but we will create a situation when issue is created and then we ask through Claude to attach image to this issue.

**\
Michael Gottlieb** 6:02\
OK, going down underneath IP866, there are new items that have been added, specifically GC367 which is going to be the second software release for the Nebraska.\
Market from the design side, there are three elements that the REQ is requesting be modified or changed GC 369, which is a modification to the primary.\
Skill game. It is important to note that this does not replace the current power meter primary skill game. This is in addition to and the software should be adjustable that the player, excuse me, that the operator can either.\
Enable the power meter primary skill game or the two box primary skill game.\
GC370 is a UI button update and the UI button update is specifically being requested because we have identified that the touch here to pattern match button is still both too low.\
Large and too easy to read. Normally that is counterintuitive, but we have specific reasons based upon what we are seeing with our competitors product to do this.\
We are going to significantly reduce the border around the text of the buttons so it blends in with the background. Excuse me, we are going to reduce the font size of the text even further, and the text color is going to be changed from white to a darker color font that is going.\
To further blend into the background to draw even less attention. Moving on to GC372.\
The REQ requests that we evaluate the potential schedule implications of changing the first six Nebraska titles over to adopt the Liquid Glass UI. There are.\
Two components to this. One is the generation of the comp art and the 2nd is that Lena will evaluate the schedule implications of making this modification. We need the comp art either way because inevitably we are going to move to liquid glass to be.\
Claire, Lena, we\'re requesting that you take one game and do a liquid glass treatment to it for the Nebraska market. Not all six of them. We can look at one game and evaluate it and then please let us know when you think you would be able to evaluate the schedule implication.\
Of making this change. Once we have this information, we will Juan will evaluate and review and make a determination if he wants to move forward with adopting the Liquid Glass UA UI for the second Nebraska release or if he wants to delay it.\
A subsequent Nebraska release. Juan, is there anything further you\'d like to add?

**\
Juan Martinez** 9:44\
No, I mean you you covered it. We spoke earlier Val and I and we we believe that the liquid glass effect could take 30 to 40 days to get finalized. So if we can the engineers have committed to their portion of these adjustments and.\
Timely fashion. So based on Lena\'s exercise, I do believe that liquid glass should stay at the bottom in terms of priority, but that we will most likely submit the other changes to the test lab, get the product out and then revisit liquid glass at a later time.

**\
Michael Gottlieb** 10:24\
OK. And then go ahead.

**\
Lena Zhukova** 10:25\
Uh.\
Descriptions to compart stories GC374GC376 and GC378 should be added.\
According to abstracts again, I\'m saying that because I I I would like to test if MCP can do it for me like automatically and talking about schedule for now like our priority where is it falling like finish South Dakota and.\
Immediately start to work on Georgia because I I saw Georgia is very urgent if we will wage Nebraska liquid glass project and so because as far as I understand the skill games changes are small but liquid glass project for Nebraska games bigger.\
It\'s yeah, it\'s about like 2 months maybe like to change everything in the game and add home screen, new home screen to Nebraska games. So it will delay Georgia. So I need to understand priorities.

**\
Juan Martinez** 11:38\
So I mean we we have a hard date for Georgia to to have this product viewable by the 2nd week of August at the annual gaming show. So working back from let\'s just say August 10th, we you know that means it has to be.\
close to approved by Eclipse. I mean, we could certainly show a demo, but really end of March, early April is when we would want Georgia done. I don\'t think that date has changed any in terms of priority. Val, I\'ll let you.

**\
Lena Zhukova** 12:12\
Georgia done by middle of April. It\'s absolutely impossible.

**\
Michael Gottlieb** 12:13\
No, no.

**\
Juan Martinez** 12:16\
I\'m sorry, end of April, end of April.

**\
Lena Zhukova** 12:18\
No, no, the end of February with South Dakota. Are you talking about South Dakota or Georgia?

**\
Michael Gottlieb** 12:19\
Even still, no.

**\
Juan Martinez** 12:24\
No, no, no. I\'m talking about Georgia.

**\
Lena Zhukova** 12:26\
No, it\'s absolutely impossible. We we even we even prolong South Dakota days because we lost one of our developer for for more than a month.

**\
Val Levitan** 12:39\
Sorry, Juan, why do you need Georgia by the end of April?

**\
Juan Martinez** 12:43\
Just to submit it, have time to submit it to the lab and have it ready to go for August.

**\
Val Levitan** 12:52\
The lab usually needs 30 days.

**\
Juan Martinez** 12:55\
After 30 to 45 days, we\'re doing some significant changes here.\
What? What? What is the tentative date? Can we jump back to Georgia real quick?

**\
Val Levitan** 13:08\
I think, I I think with realistically speaking it should be middle of May or 1st of June.

**\
Lena Zhukova** 13:14\
June. Yeah, that\'s my. My guess is June.

**\
Juan Martinez** 13:18\
That works.

**\
Val Levitan** 13:19\
But I also but I also suggest to completely.\
Disregard GC372 at this stage and not even go in that direction.\
Because we we are going to get stuck in the mud here.

**\
Lena Zhukova** 13:39\
I agree. I\'m totally.

**\
Val Levitan** 13:43\
And and there\'s hardly any benefits.\
Of doing that, it will actually create a more complicated situation with Texas.

**\
Juan Martinez** 14:01\
In what sense, Val?

**\
Val Levitan** 14:04\
You don\'t want your.\
Call it liquid glass right now in Texas. You don\'t need it.\
You really don\'t want to fork the development.\
If you can, if you can help it.

**\
Juan Martinez** 14:22\
Right, right. I I agree with not splitting the the software into a Nebraska and the Texas version, but I\'m just trying to get get ahead of the curve right now. Liquid glass is is visually stunning and just what we\'ve seen.

**\
Val Levitan** 14:25\
Mm.

**\
Juan Martinez** 14:38\
On paper. And I think that, you know, light and wonder now arriving in Nebraska, you know, I think we\'re going to, we\'re going to see what happened in Georgia happened in Nebraska once the bigger guys start showing up. But we do have time. It\'s not a priority right now.\
So I I would agree that we can archive it, but I still think that we\'re gonna have this conversation 8-9 months down the road if the numbers are not there.

**\
Lena Zhukova** 15:05\
We we can revisit it. We sure can revisit it after Georgia. Yeah, in summer. We can revisit it in summer, yeah.

**\
Michael Gottlieb** 15:09\
Of course.

**\
Juan Martinez** 15:11\
I agree. I agree. I just don\'t want it to be pushed off to the side. I still think that.

**\
Lena Zhukova** 15:16\
No, no, let\'s let\'s just postpone it. Yeah, just postpone.

**\
Val Levitan** 15:19\
But let me let me now I I\'d like to spend some times understanding the length of time and the and the load and who is it going to be assigned to for GC369 and 370.

**\
Michael Gottlieb** 15:19\
Yeah.

**\
Val Levitan** 15:38\
So let\'s let\'s just put GC372 right now in in the backlog.\
Right.\
Now let\'s, uh, refocus on, uh, the previous two tasks and uh.\
Let\'s try to understand, please, what is really.\
Let\'s let\'s try to detail it. What is needed?\
Just just talk me through what is really required.

**\
Michael Gottlieb** 16:21\
Well, for for, you know, Lena can speak to it further, but GC370 is no big deal. That\'s practically nothing. That\'s a couple of days for her to modify the button. We\'ll go back and forth, confirm we like the button. That\'s nothing. We\'ll knock that one out. GC369, the primary skill game update, I mean two weeks.\
Makes it the most, Lena, for our part of it.

**\
Lena Zhukova** 16:42\
Yeah, yeah, I don\'t think that\'s more than two weeks. Yeah, I knew because we everything was just created and just I just started to read like abstracts and understand it because it\'s very fresh. But I don\'t think I I see it as a minor minor.

**\
Michael Gottlieb** 16:45\
Yeah.

**\
Lena Zhukova** 17:00\
Projects.

**\
Michael Gottlieb** 17:01\
Yeah, I mean, we literally, she literally go ahead.

**\
Val Levitan** 17:01\
Yeah, can I see it?\
And I think what\'s missing here is we, I think it\'s actually if we don\'t put the following task in, then we\'re going to create a scope gap in here. But I think what we want to do here.\
I\'m assuming we\'re following light and wonders design direction. We want to have Georgia type of nudge in here, right?

**\
Michael Gottlieb** 17:28\
No, no, it\'s not a nudge. It\'s a it\'s a the current. So to be very, very clear, to be very clear.

**\
Lena Zhukova** 17:29\
Yeah.

**\
Val Levitan** 17:29\
No.\
It\'s a class. It\'s a Class 3.\
It\'s a class 3 type of layout, yeah.

**\
Juan Martinez** 17:41\
Not at all.

**\
Michael Gottlieb** 17:42\
No, no, that\'s not the topic. The topic of discussion for GC369. And let me start with background. There\'s a primary skill game and a secondary skill game for Nebraska. The current primary skill game is what we refer to as a power meter, or a meter moves back and forth. You press the button and you get a percentage of your win.\
The REQ that Juan generated requests that we add a variant of the primary skill game that will consist of an overlay with two boxes and text.\
Above the two boxes, the text is going to read. To access win, choose the larger coin. On the left there\'s a box with a very, very small dull gold coin, and on the right there\'s going to be a huge large shiny coin with a gold tracer around the box if the player.

**\
Efim Podvoiski** 18:36\
OK.

**\
Michael Gottlieb** 18:38\
Presses the left box, they win nothing. If the player presses the right box, they win 100% of the win. So that is not it is a little work, but it\'s not a heavy lift. It\'s actually more work on the part of the engineers and the enable disable functionality for the menus. And then I\'ve got to rewrite the help screens.

**\
Val Levitan** 18:58\
And and this is following the design direction from Light and Wonder.

**\
Michael Gottlieb** 19:03\
That is correct, yes. This is inspired by the approach that they\'re that the approach that they are taking.

**\
Val Levitan** 19:03\
That\'s correct.\
And why do you want to keep our our power meter in and have light and wonders direction optional?

**\
Juan Martinez** 19:16\
S.\
So obviously we\'re we want to default to the new look, the light and wonder look as we\'ll call it. However, from a regulatory perspective, Val, if Nebraska, if Texas, if anyone said.\
Hey guys, this is not what you submitted. Then we are 100% dead in the water. If we had to retract the software, it\'s not like we can. We could go back to our existing, but who would want it based on performance numbers? So the on and off switch lets us have that.\
Safety net of if the regulator ever came back and said, oh, this is not what we approved or this doesn\'t comply, you know, for all I know, Vanilla might be challenging the light and wonder implementation. Unbeknownst to us, this just buys us the safety net of not having to pull our games off the floor.\
From a regulatory perspective.

**\
Val Levitan** 20:18\
I understand the argument. The only thing that seems incoherent for me is when you said.\
The erformance factor.\
I mean by by having our option number one, which is the power meter, assuming that that option is enabled again, it is fair to assume that the performance would go down.\
So.

**\
Juan Martinez** 20:49\
Yeah, but we\'re we\'re saying you\'re saying don\'t bother, we\'re gonna pull our games off completely if if we ran into a regulatory hurdle.\
Versus hey operator, please roll back while we fixed it.

**\
Val Levitan** 21:00\
No, that\'s not. No, that\'s not.\
No, that\'s not what I\'m saying. I\'m just saying that if we roll back to power meter, we should expect our performance to go down.

**\
Juan Martinez** 21:12\
100%.\
I don\'t want us to roll back. I\'m just saying if we don\'t have the option, it\'s the games coming completely off the floor or being turned off by order of the regulator or by the intralot system. It\'s the lesser of two evils. We can make 50 bucks a day or we can make zero a day because the games have been completely removed.

**\
Val Levitan** 21:39\
Is this an option that\'s set up by RIS or by an operator?

**\
Juan Martinez** 21:46\
I would, I would suggest we have the operator. We defaulted through RIS, but you should be able to flip the switch at an operator given the the distance these these places are from our office and from each other. We\'re talking about hundreds of miles apart, so we would want the customer to be able to do it themselves.

**\
Val Levitan** 22:14\
So if there is a legislative challenge, what would happen to Light and Wonder? Will they shut down their machines?

**\
Juan Martinez** 22:23\
They probably, I I don\'t know how Nebraska works, but I would say that they\'ll give us and anyone some time to comply with an alternate solution. I mean, I have my theory that since light and wonder also controls the state lottery.\
They\'re probably going to get a very small slap on the hands, if any. This is a very hypothetical scenario. It\'s just that, you know, light and wonder could probably whip up a game and prioritize GLI\'s resources and get something out.\
Quickly, probably faster than us because of their their submission power. That\'s my fear.

**\
Val Levitan** 23:07\
I don\'t. I I I gonna share.

**\
Juan Martinez** 23:08\
You know, right now we only have nine games, so it\'s easy to say remove them.

**\
Val Levitan** 23:12\
I don\'t share the same fear for some reason.\
I share a fear of wrong setting if there is an option.

**\
Juan Martinez** 23:25\
Oh, in that case, nobody touches our machine like they do others because most of the settings cannot be changed. We can we can hard code it to make it via an RIS, but that gets us back to the operator always needs to rely on us.\
To make what should be a basic game change, I I hear what you\'re saying about, but you know that they\'re shooting themselves in the foot. This is not a 711 employee making the change. They don\'t even have keys to the machines. This would be the actual operator sending a technician.

**\
Val Levitan** 23:54\
No, no, no. My no. My suggestion is not to have that option.

**\
Juan Martinez** 24:03\
Not roll back, not have the remove the power meter completely.

**\
Val Levitan** 24:09\
Yes, I\'m assuming that the power meter interface has failed us in the field and it doesn\'t work for whatever reason.

**\
Juan Martinez** 24:29\
Mhm.

**\
Val Levitan** 24:30\
I I think supporting 2 variations as we process in revisions of software supporting 2 interfaces is just unnecessary and taxing.\
And and I genuinely don\'t see a regular challenging light and wonder.

**\
Juan Martinez** 24:58\
In other jurisdictions, yes, I I agree with you. In Nebraska, that is a very far-fetched. It just leaves us no safety net.

**\
Val Levitan** 24:58\
And if and if they do.\
Well, I don\'t know if we need safety net because we sell these machines, we don\'t operate them.

**\
Juan Martinez** 25:17\
Yeah, right. Right now these are, we\'re talking about 9 games on trial and preliminary conversations is they\'re not converting to sales. So even when we\'ve re-released the software, they\'re probably gonna ask for another trial.

**\
Val Levitan** 25:32\
I\'m probably not making a point. Maybe I\'m not saying it correctly. These nine trial\
Machines, they are irrelevant for this conversation. At some point we have to convert them into sales, and when we convert them into sales, the assumption is that machines will be making money.

**\
Juan Martinez** 26:01\
Yes.

**\
Val Levitan** 26:02\
So I I I mean if if a regulator comes down on light and wonder within next 60 to 90 days, then I I see your argument.\
But after we converted machines into sales.\
And the regulator comes down on light and wonder and JVL and most likely says we\'re going to give you 30 days to rectify your software, then we\'re OK. I don\'t see any any issue with it.

**\
Juan Martinez** 26:36\
But you\'re saying, what are you saying if if we\'ve removed the switch to keep the power meter on or off or display the alternate version, we\'re just going to resubmit our old software or have to reintroduce the power meter into Nebraska 2 software?\
I\'m just trying to minimize efforts for all of us in the future because we\'re not, we\'re not adding the power meter, the power meter\'s there. We\'re just adding this new bonus.\
So.

**\
Val Levitan** 27:08\
It\'s there. It\'s there. Yes, it\'s there as an initial solution. It has not worked out for us. We\'re moving away from it. We\'re introducing something else.\
To support two different interfaces is not a good idea.

**\
Juan Martinez** 27:25\
Yeah.\
It\'s it\'s not a hill for me.

**\
Val Levitan** 27:29\
And I don\'t and and I and I don\'t see any benefit in it. Like I I see zero benefit. Like I I\'m trying to understand what the benefit is and I don\'t understand it.

**\
Juan Martinez** 27:44\
It\'s not a hill to die on now, so I I I\'m not gonna lose any sleep over it. No big deal. We can proceed with just the one solution.

**\
Val Levitan** 27:54\
My, my father, my father used to say that the only hill to die on is the the health. If your health suffers, then it\'s the hill to die on. So I mean, definitely, definitely we\'re not killing each other over this.\
I\'m just saying that a decision needs to be made and I would like it to be a clever decision in mutual agreement if it\'s possible.\
Again, I\'m going to repeat, repeat what I said. Maintaining 2 interfaces is not really a good idea if we we\'re now assuming that, OK, light and wonder is making two or three times more money than us.\
Because of how the game feels to the player, how it appeals to the player. We\'re assuming this, right? And we\'re assuming that our interface is less appealing. That\'s an assumption.\
If this assumption is correct and we\'re saying that the coin type of interface is faster and more appealing to the player, then and we\'re going with the coin interface, we\'re saying what will happen if at some point we\'re talking about a couple of years from now.\
A regulator comes in and says this is not legal, we\'re not accepting it and you need to change it. First of all, we\'re we\'re saying that the chance of this is slim to none.\
And we\'re saying that during the next couple of years, there will be a number of other game revisions and software updates.\
And so we will have X amount of machines in locations. We would probably be given 30 to 60 days to comply. We would rush with a new agreed interface after speaking to a regulator.\
Produce a new software, approve it and release it to our operators.\
The only risk that I see is if regulator comes down with the next 60 to 90 days while we\'re still testing 9 machines or 12 machines or 20 machines. But it\'s not. I mean, it\'s.\
It\'s it\'s not really a quantity to be worried about or.\
And and at that point, yeah, I see the risk, but in the next.\
306090 days I don\'t see anything happening.

**\
Juan Martinez** 30:36\
I mostly agree with you. I just want to. I just want to get a vote here. Does everyone understand my statement regarding an added level of security from a regulatory perspective?

**\
Michael Gottlieb** 30:52\
Yes, I recognize the fact that what Light and Wonder is doing is, in my opinion, not.

**\
Efim Podvoiski** 30:53\
Yes.

**\
Michael Gottlieb** 31:02\
Correct. And I was extraordinarily surprised that it got approved. It it was it. It is egregiously incorrect.

**\
Juan Martinez** 31:09\
OK.

**\
Michael Gottlieb** 31:15\
And it is frustrating and disappointing that we went through so much time, effort and energy to do our primary skill gain based upon something that was more that is skill. It is literally, truly skill to replace it with something that is.

**\
Val Levitan** 31:28\
Yep.

**\
Michael Gottlieb** 31:32\
Not. I don\'t know how they\'re getting away with it, but I do recognize your point that if somebody in one of the states, such as Nebraska, sobers up and takes a hard look at it, it could be problematic. That being said, I also agree with you that if the lights, for example, Light and Wonder\'s in bed with the Georgia Lottery.\
They sorry, Nebraska Lottery, Nebraska Lottery. They\'ll find a way to to get away with it and get through with it. I don\'t know how they got away with this in the 1st place. The ultimate question Juan is do all the rules apply equally to all of us? And you know once the genie is out of the bottle which is taking place here if if something does have to.

**\
Juan Martinez** 31:52\
Nebraska Lottery.

**\
Efim Podvoiski** 32:04\
Oh.\
Text.

**\
Michael Gottlieb** 32:11\
Get pulled back. Is everybody given adequate time to to accommodate? Now the other element that I\'ll identify is that the Panella games are dead last and they use a skill meter that we drew inspiration from. Ours looks different, but it behaves in extraordinarily similar fashion. So I do have to wonder.

**\
Juan Martinez** 32:25\
Right.

**\
Michael Gottlieb** 32:30\
Especially given that we\'ve seen some pretty darn good numbers out of out of South Dakota with a game like Lion\'s Riches, that you know, why is the game performing so poorly? We all know that players don\'t know who the manufacturer is, but they do have a sense of oh.\
This has got that crappy skill meter thing I don\'t like and then vanilla gets lumped in with JVL. So I think that that if that premise has any legitimacy to it, then our skill meter is a distinct, our our power meter is a distinct negative for JVL.\
Because it may be getting lumped in with Vanilla\'s skill meter, which is, and those games are crap.

**\
Juan Martinez** 33:14\
Yeah. No, that that is 100% fair statement. So, so Val, yeah, I I think we we all agree that we can certainly move forward without the power meter. So I will adjust the requirement.\
To remove the condition of having an on and off switch for the existing power meter primary skill.

**\
Michael Gottlieb** 33:37\
Right. And yeah, so that is a modification to REQ 1010.

**\
Juan Martinez** 33:43\
Yep.

**\
Val Levitan** 33:45\
OK, I would also like to suggest that this is not a second release of software.\
It it\'s it\'s I I I mean again, I really love how you said this is not a hill to die on, but just for clarity, this is a rework of a skill feature.\
We I I would, I would consider software releases when it, I mean establish itself in the market. But what we\'re doing, we\'re scrapping this now and we\'re saying we\'re reworking the skill feature. So I suggest renaming for clarity renaming GC369.\
Nine as uh.\
Uh, coin skill feature.\
Or something similar.

**\
Michael Gottlieb** 34:39\
OK, well to be fair, it is a subsequent software release. Normally what you would do is bump a Rev. So could you would you want to call it 1.1 perhaps?

**\
Val Levitan** 34:49\
No, no, no, no. I\'m I\'m not actually fighting against release one or release two. I\'m just saying that it\'s a rework of a skill feature and and I think and and I just want to be fair.\
The fact that we feel that.\
Light and Wonder broke all the legislative norms.\
It\'s our interpretation.\
But light and wonders interpretation that they didn\'t. So because I don\'t want to be a legislator, and actually it\'s dangerous for us to become a legislator, even for ourselves, we shouldn\'t be talking like this.\
And and especially because this thing might be challenged, we should say our initial interpretation was too conservative and we\'re drawing our.\
New sentiment from the market leader and adopting that their interpretation is acceptable to a legislator and following the leader in that respect. So and therefore instead of saying that we are designing a second revision.\
I would like to and I insist on this.\
And that\'s important for me. I would like to say that we are introducing a different skill feature and you\'re welcome to call it Coin, Shmoyin, Cohen, Moyal, whatever you want to call it.

**\
Michael Gottlieb** 36:24\
May I simply refer to it as update primary skill game update?

**\
Val Levitan** 36:29\
No, I need it to be a a new skill feature.

**\
Michael Gottlieb** 36:29\
OK.

**\
Val Levitan** 36:37\
And a new skill feature adapted from a market leader as a result of our recognition that that market leader is most likely right.\
In in their interpretation of the skill feature.\
And I think that sort of legislative attitude at JVL is very important.

**\
Michael Gottlieb** 37:02\
OK, it is now a primary skill feature.

**\
Val Levitan** 37:02\
Because the.\
Yes, because because I do not want to be later, I don\'t want standing in court, God forbid.\
Saying that.

**\
Juan Martinez** 37:20\
You froze there, Val.

**\
Val Levitan** 37:23\
I did. It must be my Internet. What? What did I lose, you know?

**\
Michael Gottlieb** 37:24\
Yeah.\
You don\'t want to be in court.

**\
Efim Podvoiski** 37:29\
Standing to.

**\
Val Levitan** 37:31\
I don\'t want to be in court stating that we broke a legislative, you know, regulatory.\
Um, definition of skill.\
OK. Can you hear me?

**\
Michael Gottlieb** 37:49\
Absolutely. GC369 is now a primary skill feature.

**\
Juan Martinez** 37:50\
Yep.

**\
Efim Podvoiski** 37:50\
Yes.

**\
Val Levitan** 37:56\
Yes, yes, thank you very much. Do you wanna Nate, do you wanna name it as coin instead of power meter?

**\
Michael Gottlieb** 37:57\
Done.\
Uh, yeah, I\'ll um, I think I want to call it dual box.

**\
Val Levitan** 38:10\
Sure.\
Whatever name you\'re going to give it, this is great and your abstract will reflect.\
Accordingly, right?

**\
Michael Gottlieb** 38:20\
Yes.

**\
Val Levitan** 38:21\
OK, cool. So the decision is to remove the power meter.\
Rimary skill feature and replace it with a box to box selector rimary skill feature.\
And can somebody estimate how long it will take?\
And the way I suggest to estimate it is by moving the power bar on the right.

**\
Michael Gottlieb** 39:00\
To be fair, Lena literally saw the abstract this morning. I wrote the abstract last night. That\'s how quickly we\'re moving. So I would respectfully suggest that you have the opportunity to confer with the engineers.

**\
Val Levitan** 39:11\
Absolutely.

**\
Lena Zhukova** 39:11\
I.

**\
Val Levitan** 39:13\
Of which engineers that this is, this is only, this is only design stage. This is concept stage right now.

**\
Lena Zhukova** 39:23\
But.

**\
Michael Gottlieb** 39:24\
Yeah, I think we, yeah, I think we set a couple weeks. I believe we set a couple weeks for this for this phase to do the design part of it.

**\
Val Levitan** 39:29\
Couple.\
OK, so abstract what? Let\'s say a week and compart design is another week after that.

**\
Lena Zhukova** 39:39\
And that was completely, yeah.

**\
Michael Gottlieb** 39:39\
I\'ve already put, yeah, I\'ve already put the date in. The abstract already has dates in it. I\'m ahead of you, Val.

**\
Val Levitan** 39:46\
Well, OK.

**\
Michael Gottlieb** 39:46\
I\'ve had a lot of coffee.

**\
Val Levitan** 39:49\
That\'s I\'m accepting this, but Lena is is sharing her screen and I\'m referring to to Lena\'s screen.

**\
Michael Gottlieb** 39:57\
Yeah, the date my I\'ve already put in dates for the abstract and she needs to put in dates for the comp art. I I think we should be able to knock it out in two weeks.

**\
Val Levitan** 40:01\
Yeah.\
OK, fantastic. We spoke to Pavel today. He feels that he will schedule everything by Thursday and will deliver his part within two weeks.\
So we\'re quite engineers are quite aligned with the design team. So that\'s that\'s wonderful.\
So then one, I think it should be your undertaking to set the clips or give them a call. Tell them that we\'re redesigning the primary skill feature to follow light and wonders interpretation.

**\
Juan Martinez** 40:47\
Well, I\'m not gonna mention Light and Wonder though to Eclipse, because Light and Wonder normally uses GLI, which is also approved for Nebraska. So I have no idea of Eclipse. I could discreetly ask, but I have no. I doubt they used Eclipse.

**\
Val Levitan** 40:48\
M.\
You\'re absolutely correct. Let me let me rephrase it. Please advise Eclipse that we will be submitting.\
This new release I have an agreement with Eclipse where they charge us 20% premium.\
On labor and they can do it within 10 days.\
And so I\'m willing to pay 20% premium.\
For 10 days approval.\
But but what they asked me to is to give them as much advance notice as possible before the submission. So let\'s schedule the submission for March.\
16th.

**\
Lena Zhukova** 42:04\
Oh, I think it\'s too soon. So it\'s only two weeks. I we I I need.

**\
Efim Podvoiski** 42:04\
But.

**\
Val Levitan** 42:05\
Why?\
Yeah, fair. Fair enough. Fair enough. You\'re right. You\'re right. 23rd.

**\
Lena Zhukova** 42:13\
Yeah, that sounds good.

**\
Val Levitan** 42:16\
Yeah, if you.

**\
Michael Gottlieb** 42:17\
The same.

**\
Efim Podvoiski** 42:18\
I have two questions. One is Juan, we overlooked adding any statistics on how this features primary and secondary are used. Do we want to put it in this release or we don\'t have time for it?\
Hope you don\'t care.

**\
Juan Martinez** 42:38\
I guess. Can it be done in two weeks?

**\
Val Levitan** 42:39\
Sorry, sorry, I didn\'t. I didn\'t understand. Say it again, please.

**\
Efim Podvoiski** 42:41\
I.\
We don\'t have any statistics on this skill features. We don\'t know how much players are losing because they\'re missing this power meter or in this case if they missed my mistake on this picture choosing.\
And we don\'t know how often players are using this secondary feature, this Simon Says game. I think never, but.\
Kind of interesting to know, but I I think it\'s it\'s nice to have, but not necessary. But just my opinion, but one is entitled.

**\
Juan Martinez** 43:20\
Yeah, I no, I I I I don\'t think it\'s necessary.

**\
Val Levitan** 43:22\
Does does light.\
Does Light and Wonder have Simon Says game?

**\
Efim Podvoiski** 43:30\
Yes, I do.

**\
Juan Martinez** 43:30\
Yes, they they use.

**\
Michael Gottlieb** 43:31\
Yes, that\'s the secondary skill game.

**\
Juan Martinez** 43:34\
They use an actual prize symbol.

**\
Val Levitan** 43:35\
And the.\
And is it?

**\
Juan Martinez** 43:38\
Like a bag.

**\
Val Levitan** 43:40\
Is it as prominently displayed as ours or less prominently more hidden?

**\
Michael Gottlieb** 43:47\
The button, the button that triggers it is more hidden, which is why we already have a a JIRA item to reduce the font and the prominence of the button.

**\
Juan Martinez** 43:50\
Yes.

**\
Val Levitan** 44:00\
So that\'s the can we rename it to the secondary skill feature then?\
Button.

**\
Michael Gottlieb** 44:08\
OK, it it actually isn\'t the secondary skill feature, it\'s the trigger. But yeah, I\'ll.

**\
Val Levitan** 44:15\
OK. You understand. Yeah. Thank you.

**\
Efim Podvoiski** 44:18\
And another small.

**\
Val Levitan** 44:19\
And we have and we haven\'t. Sorry, I\'m interrupting. Go ahead.

**\
Efim Podvoiski** 44:23\
Another small question when I Michael says that on the bigger coin is always on the right. Is it?\
It it may be on the left.

**\
Juan Martinez** 44:36\
It needs to randomly toggle. I don\'t know the frequency, but in the last video from Dennis you can see that in the Green Machine game the money bag did move to the left after X amount of plays versus being on the right.

**\
Efim Podvoiski** 44:38\
Yeah.\
I wouldn\'t. Yeah. In this case I wouldn\'t. I wouldn\'t try to have any patterns that it\'s always on the right because people will learn it\'s always on the right automatically click on the right, lose their money and be upset. So it it would better if we.

**\
Juan Martinez** 44:51\
So the.

**\
Efim Podvoiski** 45:09\
We we can is alternate everyone or every time or be prepared around them.

**\
Val Levitan** 45:10\
Understood.

**\
Michael Gottlieb** 45:16\
It should be random.

**\
Efim Podvoiski** 45:18\
Should be random. Yeah, I guess it should be random.

**\
Michael Gottlieb** 45:25\
OK, how updated?

**\
Val Levitan** 45:29\
I would like to delete.\
GC372. It doesn\'t need to be under backlog.\
I can delete it for you. I can bot delete it.

**\
Lena Zhukova** 45:50\
Yeah, OK.

**\
Juan Martinez** 46:05\
Sorry, which which GC did we delete? Remove?

**\
Lena Zhukova** 46:11\
Liquid glass.

**\
Juan Martinez** 46:12\
OK, OK.

**\
Val Levitan** 46:17\
OK, so great, this is scheduled now.\
The submission is on 23rd.\
Time is clear. Understood.\
The rest of the schedule hasn\'t moved, right? We did not impact any any of the other products, am I correct? Especially those that are in production now.

**\
Lena Zhukova** 46:44\
Not yet, because we\'re only working on concert.

**\
Michael Gottlieb** 46:45\
Not yet.

**\
Val Levitan** 46:49\
But sorry, my hold on, my apologies.\
We didn\'t. We didn\'t plan it correctly.\
We planned the.\
Can you move that screen away?

**\
Lena Zhukova** 47:04\
I just wanted to show Michael. It\'s probably it\'s unsaved changes.

**\
Michael Gottlieb** 47:10\
Yeah, go ahead and save it. Go ahead and highlight it and save it.

**\
Lena Zhukova** 47:12\
Can I drink for you?

**\
Efim Podvoiski** 47:12\
A second.

**\
Lena Zhukova** 47:19\
OK.

**\
Efim Podvoiski** 47:20\
Oh.

**\
Val Levitan** 47:21\
It it seems like we incorrectly scheduled this for two weeks.\
The game concept and this needs to be a production done.\
Right.

**\
Michael Gottlieb** 47:39\
Well, the first step is the concept phase.

**\
Val Levitan** 47:42\
Yeah, but I\'m just saying that it\'s not two weeks then. The concept is not two weeks, right?

**\
Michael Gottlieb** 47:47\
Yes, it is.

**\
Val Levitan** 47:51\
I\'m afraid that\'s true mistake him.

**\
Michael Gottlieb** 47:53\
OK. How long would you like it to take?

**\
Val Levitan** 47:57\
Thumbs up should probably in this particular case.\
We should probably be done on Wednesday.\
And then we should move it into production, right? And then?

**\
Michael Gottlieb** 48:11\
It moves into the design hase next.

**\
Val Levitan** 48:15\
Sorry. Then design space, probably couple of days in production, couple of days. So it will be ready on the 23rd. Sorry, sorry, yeah, a couple of weeks.

**\
Lena Zhukova** 48:21\
No, production is not a couple of days.\
Mhm.

**\
Val Levitan** 48:31\
Right, because it\'s 2027th now. So then Monday is.\
Monday is the second, right? So concept should be probably be ready by the 4th.\
And then my suggestion is for design stage to be ready by the 10th.\
11th.\
And then production is already on the 23rd.\
Sorry, we need the testing.\
So it needs to be ready on probably 19th.

**\
Efim Podvoiski** 49:16\
Hmm.

**\
Val Levitan** 49:17\
Gives a we gives the 20th and 23rd will submit it.\
The testing isn\'t too much there.

**\
Michael Gottlieb** 49:32\
Anna, do you want to put those dates in there or do you disagree with them?

**\
Val Levitan** 49:33\
Right.

**\
Lena Zhukova** 49:36\
I I first I need to work on concept. It\'s it\'s very hard for me. I need to read abstract carefully. I I need to start to work on concepts and I I can estimate more like correctly how much we will need in production I I think.\
We will be done by like estimating and like everything together. I think we will be done by end of March, but.

**\
Efim Podvoiski** 50:04\
It\'s not. It\'s not end of March, man. It\'s not end of March.

**\
Lena Zhukova** 50:08\
But first of all, set to March 31, 31st.

**\
Juan Martinez** 50:14\
They said the 23rd, the 23rd, 23rd.

**\
Efim Podvoiski** 50:15\
No.

**\
Lena Zhukova** 50:15\
Submission. Submission.

**\
Efim Podvoiski** 50:18\
When you search.

**\
Lena Zhukova** 50:19\
And shut down, OK.

**\
Val Levitan** 50:26\
Well, we know for sure that the concept doesn\'t need to be two weeks. Right now we\'re assigned two weeks to.

**\
Lena Zhukova** 50:33\
Sure, yeah. So for for this one, we can do it faster, especially if we will remove everything else\'s like.

**\
Val Levitan** 50:42\
OK.

**\
Juan Martinez** 50:46\
And uh.

**\
Val Levitan** 50:46\
OK, so so let\'s can we assign?\
The concept stage. Can we? Let\'s assign the 4th as the end of the concept stage. Can you please move the?\
Bars.

**\
Juan Martinez** 51:07\
Yeah.

**\
Val Levitan** 51:07\
Don\'t put the hard date. You gotta you gotta move the you cannot put a hard date.

**\
Michael Gottlieb** 51:10\
The bars.

**\
Val Levitan** 51:15\
You\'re going to move the bars.

**\
Juan Martinez** 51:20\
Removing it from the 6th to the 4th.

**\
Michael Gottlieb** 51:26\
Yeah, so that means Lena stops working on what she\'s working on and works on the overlay for the two boxes with the coin.

**\
Efim Podvoiski** 51:36\
I guess that\'s why you asked for two weeks, because you didn\'t want to drop everything abruptly.

**\
Val Levitan** 51:44\
I don\'t think it will be able to. OK, so let\'s so we\'re great here.

**\
Efim Podvoiski** 51:45\
Right.

**\
Lena Zhukova** 51:46\
Yes.

**\
Val Levitan** 51:53\
No, but you\'re just move the compart will be done at the same time, right?

**\
Lena Zhukova** 51:59\
No, I start on Monday and uh, let\'s assume that I will finish on Wednesday.\
If like, yeah, it\'s going to something.

**\
Val Levitan** 52:05\
OK.\
OK.\
OK, great. Thank you. So now let\'s.

**\
Michael Gottlieb** 52:16\
Right. And and to to be clear, for the record, so there is no confusion, Juan, this is exactly what you want. There is no more information coming. There is no more market research. There\'s no more data associated with this.

**\
Juan Martinez** 52:32\
No.

**\
Michael Gottlieb** 52:32\
OK, just making sure.

**\
Juan Martinez** 52:41\
That will come, Michael, when once we have games deployed and we\'re collecting individual gameplay data to then address the the real Nebraska 2 software release.

**\
Michael Gottlieb** 52:56\
OK, and I have already updated the abstract to indicate that the presentation of the coin boxes are random.

**\
Juan Martinez** 53:05\
OK. And I\'ve already updated Rec 1010 with that statement as well as the removal of the support for the power meter.\
Peter.

**\
Michael Gottlieb** 53:36\
OK. And just to confirm, Val, you want this sense of urgency, this is the number one priority right now then?

**\
Val Levitan** 53:43\
Yes. And I would like to explain to everybody why I choose to make it #1 priority because in the small company like JBL, cash is important.\
And this is holding U our sales.\
We cannot sell. We cannot turn this project into cash.

**\
Lena Zhukova** 54:02\
OK, so we will stop everything and we will focus on just then we can probably like finish it first.

**\
Val Levitan** 54:09\
And.\
And I\'m and I\'m very open with you. I want you to understand why I\'m doing certain things and in in the hopes that that I will not force you, but make you my but align you rather than force it.\
How do you like my choice of English? My choice of words?

**\
Juan Martinez** 54:33\
Very smooth.

**\
Val Levitan** 54:34\
Yeah, I could be a politician.

**\
Michael Gottlieb** 54:35\
Oh, both things. Both things can be true. We can be forced and aligned. It\'s perfectly fine. There\'s nothing wrong with being forced is we just you\'re you\'re what you\'re doing is explaining the why, which is always intelligent, thoughtful people perform better when they understand the why.

**\
Val Levitan** 54:55\
You can definitely be a politician.

**\
Juan Martinez** 54:58\
Mhm.

**\
Michael Gottlieb** 54:59\
You\'re killing me.

**\
Efim Podvoiski** 55:03\
This is not a compliment, right?

**\
Val Levitan** 55:04\
You kill what?

**\
Michael Gottlieb** 55:05\
Of course not.

**\
Val Levitan** 55:06\
You can. You can. You can run for Congress.

**\
Lena Zhukova** 55:09\
We\'ll get back.

**\
Juan Martinez** 55:10\
At least he didn\'t call you Trump, Michael.

**\
Michael Gottlieb** 55:13\
Hi. OK, Lena, let\'s carry on.

**\
Val Levitan** 55:18\
Hold on, hold on. Let me let me just delete that task one second.\
So 373 is gone now, right?\
Yeah.

**\
Juan Martinez** 56:05\
Yeah, 372 was.

**\
Lena Zhukova** 56:07\
It\'s a one time.

**\
Val Levitan** 56:09\
OK, so game design now, right? Let\'s start planning game design. Do we need do we need NAD two in the game design stage? Obviously, yes. Yeah.

**\
Lena Zhukova** 56:15\
Yeah.\
Not yet, but first we need to finish concert. I locate the game design issues next week.

**\
Val Levitan** 56:25\
I know.\
OK. I just, I was hoping to plan it, but OK, that\'s fine. That\'s fine. I can, I can live with it.

**\
Michael Gottlieb** 56:39\
The the REQ. The REQ was generated yesterday. I wrote the abstracts. I stayed up late last night to get all of that done. This is for us to stay on track. And then Lena looked at it this morning for the first time.

**\
Val Levitan** 56:40\
Um.\
Yes, yes, yes, yes. I have full appreciation that you guys moved fast and I I thank you for that.

**\
Lena Zhukova** 56:59\
In the design stage for now, we have one issue in IP887. It\'s IP 1018 Dragon face update. We are doing like almost like full update of everything.

**\
Val Levitan** 57:00\
Um.

**\
Lena Zhukova** 57:19\
This game except symbols art, so it takes a little bit longer than other games in this set to create.\
Full design assets and I have like a lot done and I hope like on Tuesday and again if if you are going to switch now like completely to this in Nebraska maybe I need to problem because I I still need something to finish.\
So due date is Tuesday.\
Should I prolong it? Because I will switch to Nebraska. I\'m I\'m not sure.

**\
Val Levitan** 58:05\
Should you extend it? Yes, you should. Yes, you should extend it.

**\
Lena Zhukova** 58:07\
Now.\
I should extend it probably until the end of just next week.

**\
Val Levitan** 58:15\
I recommend for you to extend it probably by two weeks.

**\
Lena Zhukova** 58:19\
Till Monday until Monday. Yeah, I I I think I will. I will done everything next week. I will finish this Nebraska compartment this because again I.

**\
Efim Podvoiski** 58:21\
Hi.

**\
Val Levitan** 58:35\
The game design, the game design stage contains only one open item and so my suggestion is to put it on to park it, put it in the freezer for now and in the game design stage put the NAD 2.

**\
Lena Zhukova** 58:54\
Let\'s try to to do it, to experiment and do it automatically with MCP when I will work with Clayton on Tuesday.

**\
Val Levitan** 58:54\
And push that.\
No, I agree with you. On Tuesday is fine. I\'m just suggesting that when you think of how much extension.\
Time to give yourself. Then I suggest you don\'t extend it just by two days, you extend it by at least.

**\
Lena Zhukova** 59:23\
Yeah, and I sent it by one week. So I I I plan to finish at the beginning of next week. Now it\'s beginning of other week like March and.

**\
Val Levitan** 59:32\
No, because the no, because the priority in the design stage will be an AD too. So for the moment you.

**\
Lena Zhukova** 59:39\
Uh, you\'re right. You\'re right. You\'re right. You\'re right. You\'re right. I did not think about it. And and I also have two days of next week, so.

**\
Val Levitan** 59:47\
That\'s right.

**\
Lena Zhukova** 59:49\
I will. I will try to finish everything for Nebraska by three days. I I don\'t if I I if I put everything aside, everything else aside, I will do it in three days.

**\
Val Levitan** 1:00:03\
OK. All right. Um.\
Let\'s move into game roduction.

**\
Lena Zhukova** 1:00:17\
Yeah, so in the production we are working on IP 969986 Black Hills Kina, IP 985 Kukat Kina.\
IP984 liquid glass style home screen for South Dakota IP988 La Rosa games IP987 rodeo spins game.\
Started to work on IP 998 line switches and two games IP 997 Dragon Pace and IP 995 Wild Cold in to do.\
We have fresh build today. I send it to Michael. He started to review it like on Monday. He\'ll give us like feedback on La Rosa, Rodus Pins and Black Hills Kino.

**\
Michael Gottlieb** 1:01:22\
Yeah, Elena, is that gun animation the same one from Larosa Fiery Ice, or did you adjust it at all?

**\
Lena Zhukova** 1:01:29\
We didn\'t have animation for gun in fire eyes. It was just template symbol. Just we had we have template animation when we put placeholders for symbols, just static images. We have template animation just move image forwards a little bit and then backwards.

**\
Michael Gottlieb** 1:01:41\
Right.

**\
Lena Zhukova** 1:01:49\
The standard highlight.

**\
Michael Gottlieb** 1:01:51\
I think it looks good. Are you happy with it?

**\
Lena Zhukova** 1:01:54\
You mean like new anime? Because this one which we created in South Dakota, it\'s it\'s it\'s real animation because box is turning a little bit and highlight is not fake but real on the box.

**\
Michael Gottlieb** 1:01:54\
Or do you want to keep the?\
Right. That\'s what I\'m saying. I like it. I think it looks good. Are you happy with it?

**\
Lena Zhukova** 1:02:09\
Yeah, yes, I\'m happy. I said it\'s a little bit too subtle, but you\'re right, it it helps us to keep hierarchy of symbols value, right? Because it\'s not expensive symbol we we should not have like very active animation boxes open and gun is turning and.

**\
Michael Gottlieb** 1:02:21\
Right. For the, yeah.

**\
Lena Zhukova** 1:02:29\
Sign in so.

**\
Michael Gottlieb** 1:02:30\
Exactly right. For purposes of the record, Lena and I are discussing the animation of the gun symbol in La Rosa, specifically the fact that the original implementation.\
Was more significant than it should have been relative to the value of the symbol. It\'s important for all of the symbol animations to match their respective hierarchy and be in alignment with.\
All other symbols and we identified that the animation for the gun symbol in La Rosa was bigger and more prominent than the other high pay symbols, so it did not look correct. Accordingly, we.\
Modified the animation of the gun symbol in La Rosa to be more in alignment with the other symbols and it is now approved.

**\
Lena Zhukova** 1:03:37\
OK, great.

**\
Michael Gottlieb** 1:03:38\
The the also Black Hills Kino Deluxe, we are just about complete with the help screens. Everything looks good and we\'re we\'re moving forward there.

**\
Lena Zhukova** 1:03:56\
Yeah, next next the build you will see already animation of balls like falling into this. I don\'t know this big box.

**\
Michael Gottlieb** 1:04:09\
The yeah, the silo or shoot or shoot or whatever you want to call it. And Vlad, has Vlad had a chance to work on the audio for it at all?

**\
Lena Zhukova** 1:04:12\
Sorry.\
I think a lot created all sounds, but the problem is that Anton is not insert inserted it here because Anton now is working for two people, so he\'s working with eager.

**\
Michael Gottlieb** 1:04:35\
Right.

**\
Lena Zhukova** 1:04:38\
Tasks, so everything a little bit slower, but Vlad did all sounds. He created all sounds. He created all sounds.

**\
Michael Gottlieb** 1:04:40\
OK.\
OK, well, if the sounds are there, that\'s good. We yeah, the triggers just have to be there correctly. I noticed when I was playing it after all the balls fall into the chute, there\'s some like coin tinkling sound that doesn\'t even make any sense, but I\'m sure they\'ll, I\'m sure they\'ll get to it. I just wanted to check on the audio.

**\
Lena Zhukova** 1:04:50\
Mhm.\
And yeah, line switches we started to work. It\'s not in the build yet, but we started to work on line switches.

**\
Michael Gottlieb** 1:05:21\
OK, I believe that covers everything, unless there\'s anything else you want to touch on regarding the schedule.

**\
Val Levitan** 1:05:27\
No, this was a healthy review. I enjoyed it. Thank you.

**\
Michael Gottlieb** 1:05:32\
OK. And then Juan, did you want Lena to show that image that you requested?

**\
Juan Martinez** 1:05:37\
Yeah, yeah. Just because I haven\'t discussed it with Val yet, definitely.

**\
Lena Zhukova** 1:05:41\
Mhm.

**\
Juan Martinez** 1:05:43\
Yeah, Val. So per our last conversation, this is the 8 pack version that will serve as the base game. So we\'ve got 2 jackpot rushes, 2 fiery ice and four.\
Lines and ways games.

**\
Lena Zhukova** 1:06:01\
And it\'s going to be different lines and ways, but for for to I need to put lines, reach a second and to twin bison.

**\
Juan Martinez** 1:06:02\
So I\'ll do.

**\
Val Levitan** 1:06:05\
Very, very.

**\
Juan Martinez** 1:06:10\
Yes.

**\
Val Levitan** 1:06:11\
Very clean.

**\
Michael Gottlieb** 1:06:14\
Well, so that\'s a good, that\'s a good question. So to be clear, Juan, you want us to deliver 6 lines and ways games. So it\'s basically these four plus the updated lines, riches and the twin bison and then it will be operator.

**\
Val Levitan** 1:06:15\
OK.

**\
Michael Gottlieb** 1:06:33\
Enable, disable, but only a maximum of four games. Is that correct or do you only want us to do 4 games?

**\
Juan Martinez** 1:06:39\
No, no, we we want to submit all six and going to try what we\'re seeing on screen. 8 will be the default enabled and we would toggle more and Val\'s working on software packages where if you want 10 or if you want 12, that\'s a different price for the customer.

**\
Lena Zhukova** 1:06:41\
All six, OK.

**\
Michael Gottlieb** 1:06:58\
OK, so we\'re where we need to be then because Rodeo Spins is a three reeler with a bonus reel as is Queen of Luxor and then Crazy Colton Bayou are five reelers. And then we\'re doing a five reeler with Lion Riches and then another three reeler with Twin Bison. So you\'ll get the three and three that we.\
Agreed to and and we\'re good.

**\
Juan Martinez** 1:07:22\
Yeah, yeah.\
I just, I do want to go over with you what games, you know, expanding reels or not. I I just want to get us the most bang for our buck with the first deployment of this, so.\
Whether it\'s these actual four or not, you know, I\'ll review that with you, OK.

**\
Michael Gottlieb** 1:07:39\
It\'s the IT is these four it is I would say well I shouldn\'t say that it it it\'s yeah we can have that conversation of of of the six you know what what do you want to.\
To go with.

**\
Juan Martinez** 1:07:54\
Sure.\
And that\'ll be based on features. So yeah, we\'ll we\'ll touch on that.

**\
Lena Zhukova** 1:08:00\
But I think we definitely wanted to lose Dragon Dreams or whatever and Gypsy Spirits because it\'s cool enough by Riches and by Riches is nicer game in my opinion.

**\
Michael Gottlieb** 1:08:05\
Yes.\
Yes. And you get, yeah, it\'s not, it\'s not a literal clone. The free spins are a touch different, but you get more free spins in Bayou Riches and I think the theme is more appropriate for that market. There are people that are, um, superstitious.

**\
Val Levitan** 1:08:15\
Can I can I see the top right here?

**\
Michael Gottlieb** 1:08:31\
And gypsy spirits got a black cat in it. And you know, I I just, you know, why? Why take any risk of crippling yourself in any way, shape or form? But um.\
Yeah, I mean, the good news is that of the six, honestly, it\'s going to be kind of a hard discussion and fight to pick which four you want to go with because I think all six are unique and solid products in their own, in their own right. You know, if you\'re talking about pulling one of these out here and putting a lion, and I think you want a lion\'s riches in there because that\'s one of our top performers.

**\
Juan Martinez** 1:09:03\
Absolutely, yeah.

**\
Michael Gottlieb** 1:09:07\
I\'d probably swap out by. I would swap out bio riches for for lions riches, probably.

**\
Juan Martinez** 1:09:08\
Val, did you have a question?

**\
Michael Gottlieb** 1:09:17\
I mean, Rodeo Spins is a clone of Crazy Spins, which is one of our top, our number one performer in that market, so.\
Maybe Queen of Luxor for twin bison? Maybe.

**\
Juan Martinez** 1:09:33\
Yeah.

**\
Michael Gottlieb** 1:09:34\
I think they\'re all good games, so.

**\
Val Levitan** 1:09:35\
Can I? Can I see the topper? Can I see the topper on this machine?

**\
Lena Zhukova** 1:09:50\
Because now it\'s highlighting in fire ice link game, it shows fire ice link progressive for Jetpotrash. It will show Jetpotrash progressive and for lines and ways we will decide to what are we going to show.\
Maybe some some.

**\
Val Levitan** 1:10:05\
So you have your your your fiery ISIS 120,000 or is that just a number?

**\
Lena Zhukova** 1:10:11\
That\'s just a normal.

**\
Efim Podvoiski** 1:10:12\
Just um.

**\
Val Levitan** 1:10:14\
But.

**\
Efim Podvoiski** 1:10:15\
It\'s not.

**\
Val Levitan** 1:10:19\
I\'m I\'m just saying that the number on the topper is much less than is it?

**\
Lena Zhukova** 1:10:23\
Yeah, I know there\'s just the numbers I can and I I can put in your numbers you will give me. It\'s just a comfort. I\'m just showing how like digits are going to.

**\
Val Levitan** 1:10:32\
Gotcha.\
But the idea is that we\'re gonna show a higher number on the topper, right?

**\
Michael Gottlieb** 1:10:43\
No, the same number. Well, the same number is shown.

**\
Lena Zhukova** 1:10:45\
Stay.

**\
Val Levitan** 1:10:47\
So if it\'s 10, then it will be in both places.

**\
Michael Gottlieb** 1:10:51\
Correct.

**\
Lena Zhukova** 1:10:51\
Yes, yes, because is optional and.\
Probably for lines and ways we will show, but we will show progressive. We we have the three levels progressive, so we will show the levels of.

**\
Val Levitan** 1:10:59\
So.\
Right.\
So explain. So explain to me your idea that you.

**\
Michael Gottlieb** 1:11:07\
Absolutely.

**\
Val Levitan** 1:11:14\
Getting inspired from that other manufacturer where it it\'s reduced to tabs, the symbols, the pay tables reduced it, yeah.

**\
Juan Martinez** 1:11:22\
The the reduced pay table.

**\
Michael Gottlieb** 1:11:28\
The concept behind it is that normally the top of your vertical screen or your second screen in Georgia has been utilized for displaying the pay table, which while perfectly fine for playing the game.

**\
Val Levitan** 1:11:29\
Sidur.

**\
Michael Gottlieb** 1:11:45\
It\'s not a great come on for a distance from a distance, and it\'s not terribly compelling to look at. It is more informational than it is entertainment. So drawing from what other people are doing in the market, what we\'re going to do with Twin Bison and Lions Riches.\
Is that instead of having a pay table take up an entire section of the screen, we\'re going to have a row of pays shown for the symbols, and then we\'ll have text alternating on top of the real bundle telling you how the match 3 progressive is triggered.\
How the free spins are triggered. And then instead of a massive large pay table, we\'re going to have a massive large lion staring down the player. And then in twin bison, we\'re going to have two bisons staring down the player.

**\
Lena Zhukova** 1:12:46\
We will do it only for these two new games. Yeah, we will keep play tables for like our existing games.

**\
Michael Gottlieb** 1:12:49\
Right.

**\
Val Levitan** 1:13:02\
OK.\
I have no questions.

**\
Michael Gottlieb** 1:13:09\
OK. Thank you for your time.

**\
Lena Zhukova** 1:13:11\
Thank you.

**\
Efim Podvoiski** 1:13:11\
Sorry, sorry, sorry. I have I have one question. I I it just happens that I don\'t have in in zero. I don\'t have a dedicated IP for my mass engine.

**\
Juan Martinez** 1:13:13\
Thanks everybody.

**\
Efim Podvoiski** 1:13:27\
All this when I did something some changes in my sensions, they were linked to some game update or something. But right now I want to do a feature and I don\'t know where to put it because it\'s.\
Not into specific game and the game is not in production for yet, but we are doing this series.

**\
Val Levitan** 1:13:49\
You were not. You feel, you feel you\'re not going to decide it on this forum, OK?

**\
Efim Podvoiski** 1:13:54\
OK, so how how do I approach it?

**\
Val Levitan** 1:13:56\
Let let you and I talk. Let you and I talk about it.

**\
Efim Podvoiski** 1:14:00\
OK, OK.

**\
Val Levitan** 1:14:04\
OK. Thank you guys.

**\
Juan Martinez** 1:14:05\
everybody. Bye.

**\
Lena Zhukova** 1:14:05\
Thank you. Bye.

**\
Val Levitan** 1:14:06\
Thank you.

**\
Efim Podvoiski** 1:14:06\
Thank you. Bye.

**\
Val Levitan** stopped transcription
