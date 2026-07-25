**Game_Development-20260219_140155-Meeting Recording**

19 February 2026, 07:01pm

46m 34s

**Juan Martinez** started transcription

**Michael Gottlieb** 0:05  
Ridiculous. Not inches. Feet like feet like, yeah.

**Val Levitan** 0:08  
Yeah, yeah, yeah.  
I would get up in the morning. I had to. I I couldn't see my car. I mean, my car was parked outside. It was like fully covered with snow.

**Michael Gottlieb** 0:20  
Then the snow plow comes down the street and pushes even more snow into the driveway. So if you ever wanted to get out, you can't.

**Val Levitan** 0:27  
No, yeah, it was not crazy.

**Michael Gottlieb** 0:32  
Not a possibility. OK, OK, Lena, go ahead and share JIRA and we can get started.  
OK, starting with underneath IP535GC3.

**Val Levitan** 0:53  
Lena, would you, would you increase the font a little bit, please?  
Yeah, a little more, please.  
Thank you. Hmm

**Michael Gottlieb** 1:11  
And here I just thought it was my eyes. Yes. So under GC351, the new PIC 33 level progressive for Georgia, Efim and I made a change this week. We made a change in the triggering mechanism.

**Val Levitan** 1:13  
Mhm.

**Michael Gottlieb** 1:30  
And the reasoning behind it was twofold. One is that the frequency of this particular bonus hitting is a little bit further out than we thought. Would you say Efim him one in 10,000?

**Efim Podvoiski** 1:43  
Yeah, it's, yeah, about right. For $4.00, $1.00 bit, it's.

**Michael Gottlieb** 1:45  
Right, one in 10.  
Exactly. Yeah. So, so I wanted at one in 10,000 to run an anticipation on that doesn't really make a lot of sense. And then secondly, after the meetings with our customers this week, my other thought process, which I think makes sense, one, you'll have to let me know what you.

**Efim Podvoiski** 1:50  
The.

**Michael Gottlieb** 2:08  
Do think is that using the same tracker triggering mechanism we had for the Peach progressive is a better approach because the in the theory if we do have a JVL player base and it seems like perhaps we do.

**Val Levitan** 2:08  
OK.

**Michael Gottlieb** 2:24  
We want the familiarity with our new with our new software for these for these titles. So even though the progressive is being totally reworked and redesigned, the triggering mechanism is going to be the same. So for the player who has played previous JVL games.  
As part of the Peach series, they will find familiarity, right? Familiarity makes you it's easier to track. And what that means is specifically for five real games, the trigger will be 3 coins on reel three, right? Which is to say a nudge to three coins on reel 3.  
For three real games, it will be one coin on reel 3, which you have to nudge to, and then we'll do it the same way for rodeo spins won't change either, and there that trigger is on the 4th reel, the coin on the 4th reel.  
So that's the approach that we're taking there, which is different than what we were with the original direction that we were going. But I think that makes the most sense. I think familiarity is is valuable at at this juncture, right, with people who've played JVL product before and you know it's a lot of the.  
Rule of medicine and game design is like do no harm and we kind of analyzed it and like what's the upside versus the downside. And the downside is a player could get confused or frustrated that the game doesn't behave like it used to behave. And the upside is, oh, look at us, we're being clever, right? And that's not our job to be clever. Our job is to make the player feel comfortable and warm and.  
Cozy and have that familiarity. So yeah, that's that's where we're at with that. And Lena, you're going to start working on the the coin and the visuals at some point, right?

**Lena Zhukova** 4:12  
Yeah, yeah, I start. I started already. I I'm in progress. Yeah. So I'm, I'm working on.

**Val Levitan** 4:17  
And.  
And what's the frequency of progressive now like you said?

**Michael Gottlieb** 4:23  
One in 10,000 to trigger the bonus.

**Efim Podvoiski** 4:26  
Any kind of progressive it's it's it's the it. I want to say that in this case we finally would have to introduce some flexibility and I think I will introduce because it's.

**Val Levitan** 4:26  
Mm.

**Efim Podvoiski** 4:41  
Predetermined outcome. I can play with it and I can dynamically change the frequency of the progressive. So we will have some freedom in setting base levels and RTP allocated to the progressive which will dictate.  
The frequency on each progressive level. So while we will have this flexibility, we'll have to decide what are our expected values, at least in terms of RCP for total.  
Total RCP for all three levels because it's based on this. I will prepare the the remaining RCP for the game. Is it 3% or is it 5%? It's a difference, it's.  
So we have to have some understanding and based on this decide how do we prepare the RTP for the games, but this is.

**Lena Zhukova** 5:33  
What?

**Michael Gottlieb** 5:43  
Juan, Juan, I I'm going to interrupt you for a moment, Efim. Juan, do we have a sense of what our competitors, what percentage our competitors are feeding the meter with? Is it 1 percent, 2% for progressives, 2%? You're muted, Juan. You're muted one.

**Efim Podvoiski** 5:55  
The percent.

**Juan Martinez** 6:00  
Yeah, we saw that from the aristocrat screenshots. They're anywhere from .8% to 1 1/2%. That's just aristocrat. But I I think the the our goal here, the better player experience would be more frequent.  
Smaller hits than a one off larger hit, you know that.

**Michael Gottlieb** 6:22  
Right. And we'll force that for sure. Yes, Efim.

**Juan Martinez** 6:25  
Yeah.

**Efim Podvoiski** 6:25  
In this particular case, unlike usually I am, I am talking about the RTP for progressive for base level, not for increment. I think I'm not sure whether Juan was talking about increment or.

**Michael Gottlieb** 6:43  
Increment. He's talking about increment.

**Juan Martinez** 6:43  
Increment, increment.

**Val Levitan** 6:44  
2.

**Efim Podvoiski** 6:44  
Increment. Increment is increment. Increment is fed in the system and it dictates what the actual progressive win will be compared to the base level. It doesn't affect the frequency of the progressive, so.  
They still have to decide what's base portions of progressive. It's and usually it's like a little bit bigger than increment. So if you're talking 1 1/2% increment, this probably will make sense to make it to 2 1/2, say percent.  
I think we cannot. We would like to go farther, but it's robbing the base game and bonuses. So I think we I think.

**Michael Gottlieb** 7:24  
Right.

**Juan Martinez** 7:25  
Yeah, we don't. We don't want to go farther.

**Efim Podvoiski** 7:29  
Yeah, so, so we will decide Juan, Juan and Michael and me will decide what's our target like say 2%, 3% and based on this we will, I will define the RTP for the games.  
There's a.

**Michael Gottlieb** 7:46  
Right. OK. Could you, could you, when you get a chance, provide Juan and I with the parameters for the fiery ice progressive as a starting point of comparison? Because I think that that's working for us.

**Efim Podvoiski** 7:56  
Yes, I do.

**Michael Gottlieb** 7:59  
Thank you. I appreciate that.

**Val Levitan** 8:00  
So sorry, I need to go back. I didn't get a chance to ask my question. So what is the frequency of wind? You said one in 10,000 and I was gonna ask, is it 10,000 spins or 10,000 coins or?  
11 so.

**Michael Gottlieb** 8:16  
At a dollar bet, it's 10,000 spins. It's 10,000 spins. He's he's using a dollar at a dollar bet. At a dollar bet.

**Val Levitan** 8:20  
At a dollar at a dollar bag.

**Efim Podvoiski** 8:20  
It's $10,000.  
Yeah, but if you well, technically, OK.  
More precise answer is dollars, because the the biggest beds, the more frequent is the less smaller.

**Val Levitan** 8:29  
OK, so OK, so dot.

**Michael Gottlieb** 8:31  
Right.

**Val Levitan** 8:33  
I I I understand. I understand. So if it's $10,000, how often will somebody here to progress statistically?  
Every 10 days.

**Efim Podvoiski** 8:46  
I think on location we have a handle. Typical handle is 1 from 1 to 2000 so.

**Val Levitan** 8:54  
1000 typical is 1000 on an average, right?

**Efim Podvoiski** 8:56  
I think it's, I think it's bigger because our our hold is more than $100 and our RTP is more than 90%. So it's yeah.

**Val Levitan** 8:59  
A little bit, a little bit, maybe 1200.  
Right, right. A little bit more.

**Michael Gottlieb** 9:07  
But in the, but in slower locations, it's going to be lower. I mean, it's an average, right? So we're not worried about the location that's doing 2000 handle pulls a day. We're worried about the one that's doing 500.

**Efim Podvoiski** 9:09  
Yeah, yeah, yeah, yeah, yeah.

9:10  
Right.

**Val Levitan** 9:14  
No.

**Efim Podvoiski** 9:15  
Yes, please.

**Val Levitan** 9:16  
So.

**Efim Podvoiski** 9:17  
OK, so.

**Val Levitan** 9:18  
So roughly, roughly 10 to 15 days, yeah.

**Efim Podvoiski** 9:22  
Yes, but it's the smallest level. It's for the smallest level. Most of the events are on the smallest level, obviously.

**Val Levitan** 9:24  
Is that?  
Right. Is it?  
Sorry.

**Efim Podvoiski** 9:33  
Obviously, most of the progressive events will be the smallest level of the progressive one, of course, yeah.

**Michael Gottlieb** 9:39  
Of the three levels, in most instances, you're going to win the smallest value, which is typical.

**Val Levitan** 9:44  
Right, right. So is when progressive hits once every 1015 days, is that is that good or bad? I'm trying to understand what does competition have?

**Efim Podvoiski** 10:00  
They don't know.

**Juan Martinez** 10:01  
Well, we don't know, but we know from Felipe's test play that he certainly reported more frequent winnings when he played the IGT aristocrat machines. So the expectation is constant celebration.

**Val Levitan** 10:12  
Mhm.

**Michael Gottlieb** 10:17  
We're talking specifically about the progressives, though.

**Juan Martinez** 10:20  
Yeah, no, yeah, he obviously I couldn't get him to hit a progressive yet. We we don't have any data.

**Michael Gottlieb** 10:21  
How frequently the progressives had.

**Efim Podvoiski** 10:25  
So he he he personally hit many progressives.

**Juan Martinez** 10:28  
No, no, no, that's he. I'm talking about the overall game wins. There's no way he could just come in and hit a progressive, nor could we set up a progressive win.

**Efim Podvoiski** 10:35  
Yes, yes, yes, that's what I was. That was was surprised.

**Michael Gottlieb** 10:40  
Which is why I was going to look at the math for fiery ice as being representative of of hit frequency. We may need to adjust it, you know, based on a lower volume theory that you're not going to get as many handle pulls per per day. And keep in mind it is scripted and it's forced.  
So if we if we wanted to.

**Val Levitan** 11:00  
And why? Why is? Why do you look at? I mean, you lost me. I mean, you said it so kind of categorically, concretely that, you know it. I almost feel like I I should know it, but I don't know it. So why fiery ice was so?  
Incredible about it.

**Michael Gottlieb** 11:20  
I I think it's progressive hit frequency is representative of the current games in the market, of what a typical behavior of a Class 3 game is.

**Efim Podvoiski** 11:32  
But despite it.

**Val Levitan** 11:32  
But but but what is it? What is fiery ice? What's the frequency of progressive here?

**Michael Gottlieb** 11:38  
Well, that's what I asked him to look up. He was going to to look that up and provide the information.

**Efim Podvoiski** 11:41  
Yeah, but uh, if you if you are talking about the actual progressives, not this fake ones.  
Of minor.  
And the meaning the frequency is much, much lower because the progressives are much bigger.

**Michael Gottlieb** 11:58  
Right. Well, we would have to, we would have to correspondingly adjust for for the for the frequency. If fiery ice is at 100 and we're doing 50, then we would be able to do twice as often as whatever the fiery ice hit frequency number is, right, as we usually do with this stuff.

**Efim Podvoiski** 12:15  
Yeah. So, yeah, so you initially said look on RCP something to rate and I said to me that makes it so a total sense that we like I believe it's 2 1/2 and 1%, but I will double check. So it's to see and 1/2% in total.  
I believe, but we'll double check. I'll double check.

**Michael Gottlieb** 12:34  
Right of of RTP.

**Efim Podvoiski** 12:35  
Of RTP for the best levels, yes.

**Michael Gottlieb** 12:38  
Right.  
Did you get that, Val, or do you want me to explain it again?

**Val Levitan** 12:44  
Yeah, please explain.

**Michael Gottlieb** 12:46  
OK. So just quite simply, there is an allocation of RTP that we give to the player and fiery ice we think is about, well, he'll confirm, but it's about 2 1/2 to 3%, which is typical.  
So if we have that same 2 1/2, 3% of total RTP, if 2 1/2 to 3% is allocated to the progressive that that's a hit frequency that should start, that should get us in the range of where we want to be.

**Val Levitan** 13:20  
But my understanding that the allocation of the total RTP.  
To progressive in Georgia is much smaller, about half of it.  
So machines are maybe I'm talking about different RTP or maybe I'm not understanding the subject, but my understanding that the setup that we all agreed for Georgia is 92%.  
That's the base RTP and then and then approximately 1 1/2% to a progressive.

**Michael Gottlieb** 13:52  
Right.  
Right. That's that's feeding the meter though. That's what the meter is fed with. That's what's going in, not not what's coming out. Those can be two different percentages.

**Juan Martinez** 13:57  
No, no.  
OK.

**Val Levitan** 14:07  
But in but in the but in the fine.

**Juan Martinez** 14:07  
And the just to clarify, the Peach Progressive is .8%, Diamond Link is 1%. So we're we're not anywhere near 1.5%. The majority of the product out there is only getting .8% via the Peach Progressive.

**Val Levitan** 14:24  
OK, so even less. So even less, right? You're saying you're saying even less than 1 1/2.

**Michael Gottlieb** 14:25  
Yeah, but.  
But the.

**Juan Martinez** 14:27  
Yes, increments.  
Correct.

**Michael Gottlieb** 14:31  
Right, but but you can't count that because the Peach progressive is not in most instances even a progressive. It tends to be a credit value that is substantially less than the progressive. So the the win that the player is going to experience is significantly less with Peach. Therefore it can hit more frequently.  
Now that we're moving to a bonus where you're guaranteed a progressive, even the lowest level progressive is going to be like maybe the highest value of that fixed credit value that you're going to get. I mean, occasionally you would win the Peach progressive, but in most instances you would win a fixed value, a fixed.  
Credit value.  
Thus, we'd want to allocate more to feed the progressive. Does that make sense, Efim?

**Efim Podvoiski** 15:21  
Yes, and don't forget that we are speaking about two different things was increment and the and the and the base level TPR are totally disconnected. It's two different things it.

**Michael Gottlieb** 15:26  
Right.

**Juan Martinez** 15:35  
We need that worksheet in front of us so we could just see it that that's the document that Michael asked for. You know, I I think we're just going in circles here till we have that sheet in front of us.

**Efim Podvoiski** 15:47  
What kind of city I can?  
I can show you. I can share the screen and show you the document that I have sent to you that it's allows to see what what would be the frequency and the frequency of.

**Val Levitan** 16:04  
Before, yeah, that's fine. Pull up the sheet. But before you switch the screen, why are we talking about progressive right now when we're discussing the schedule? I'm. I'm completely lost. I have to. I have to.

**Efim Podvoiski** 16:15  
Sorry, because I I I distracted everybody mentioning this.

**Val Levitan** 16:21  
OK, So what?

**Efim Podvoiski** 16:21  
So probably so do.

**Juan Martinez** 16:25  
Well, one of the game concepts includes A progressive that that's an entire feature that is being added.

**Efim Podvoiski** 16:25  
Do you want them?

**Michael Gottlieb** 16:31  
Right, but Val Val's directive is he wants to go through the schedule 1st and the and then discuss discrete issues later. So does it make more sense for us to just carry on with the schedule Val and then come back to this topic?

**Juan Martinez** 16:35  
OK.  
OK.

**Val Levitan** 16:42  
Yeah, but OK. But can we start for the sake of I I'm totally not aligned. I I just don't. I just don't know where everybody's at. So can we pretend that this meeting never happened and start all over again? I'm confused. I don't know what we're discussing.

**Michael Gottlieb** 16:58  
OK, so underneath IP535 there is GC351, which is the pick three, three level progressive for Georgia. The decision that a theme and I made this week is that we're going to keep the same triggering.  
Mechanism that we had for the Peach progressive and use that same triggering mechanism for the Peach 3 three level progressive for Georgia.

**Val Levitan** 17:28  
But that's you're discussing in particularly feature GC359, which is a visual presentation concept of a progressive, right?

**Michael Gottlieb** 17:38  
Not necessarily. It was. It was just the global. It was the 351, which is the global. I mean technically would be GC361, which is the in game symbol.

**Val Levitan** 17:52  
OK.

**Michael Gottlieb** 17:53  
But it's a characteristic, a behavioral characteristic of the of the in-game symbol. So in any case, we're going to use the same behavioral characteristics for triggering the new match 3 three-level progressive for Georgia that we used for the Peach progressive.  
Yes.

**Val Levitan** 18:20  
531, which is the umbrella value stream game concept. It's the highest level, right? When you discuss, when you discuss, when you make a statement, we decided to use three coins concept.

**Michael Gottlieb** 18:25  
Yes.  
Yes.

**Val Levitan** 18:39  
So the decision has been made. My question is within the game concept, when the decision is made, is the task done?

**Michael Gottlieb** 18:39  
Yes.  
Yes.  
Yes, and you don't see it here because the done tasks no longer show up here anymore, right?

**Val Levitan** 18:56  
No, no, I see. I see it because it shows in progress.

**Michael Gottlieb** 18:59  
No, you don't see it because there was an abstract on here that contained the information that you're describing.  
And this got closed.

**Val Levitan** 19:09  
I see. So what I'm.

**Michael Gottlieb** 19:10  
If you look specific, go ahead.

**Val Levitan** 19:13  
So what am I looking at if we go back to the general? Yeah.

**Michael Gottlieb** 19:19  
What what you're looking at is the are the next tasks that are required in order to move forward with this particular feature, which is to say what the in game symbol for the jackpot coin is going to look like, what the bonus transition.  
Is is going to consist of and the visual presentation concept of what the match three pick three screen is going to look like.

**Val Levitan** 19:48  
OK. And so who who is involved in that, Lena?

**Michael Gottlieb** 19:53  
Yes.

**Val Levitan** 19:55  
OK, so Lena is part of the conceptual design, and when you decided to do coins, now you're asking Lena to present you with conceptual designs.

**Michael Gottlieb** 20:00  
Oh, yes.  
Yes.

**Val Levitan** 20:11  
And this is what GC 361 and 360 is about.

**Michael Gottlieb** 20:16  
Yes.

**Val Levitan** 20:18  
OK. So that will be finished February 20th.  
More or less.

**Michael Gottlieb** 20:27  
No.

**Juan Martinez** 20:31  
The start date and due dates are flipped here.

**Lena Zhukova** 20:35  
Yeah, March 6 bonus is going to finish March 6th. I didn't even start bonus, yeah.

**Val Levitan** 20:37  
Oh, oh, oh, oh, I'm sorry. I'm sorry. Would you mind changing the order then start date 1st and from left to right?  
Yeah. Thank you.  
Got you. OK. OK. OK. March 6th. Got it. OK. Thank you.

**Michael Gottlieb** 21:05  
Horse.

**Val Levitan** 21:05  
All clear, all clear on 351.

**Michael Gottlieb** 21:10  
Very good. OK. So then moving on to GC350, I am continuing to move for.

**Val Levitan** 21:20  
But that's that should be moved in progress, right, Lena?

**Michael Gottlieb** 21:26  
Yeah, 'cause I'm working on the abstract, that's correct.

**Efim Podvoiski** 21:27  
Is it?

**Val Levitan** 21:32  
OK. Thank you.

**Michael Gottlieb** 21:33  
Yeah. So I'm, I'm starting to cook on that and have a sense of what we want to do with it. Have I have been discussing with the theme basically how we're going to do it. We've got a plan.  
This is on track and then once we once we get that complete that will then roll into Lena doing the concept art.

**Val Levitan** 22:03  
So will twin bison have a progressive?

**Michael Gottlieb** 22:08  
Yes.

**Val Levitan** 22:09  
Will it have the same progressive as pick 3?

**Michael Gottlieb** 22:10  
Oh.  
Yes, the Pick 3 three level progressive progressive is applicable to all of the lines and ways games in Georgia Vertical to release.

**Val Levitan** 22:26  
So when we talk about GC351, it has to do with the particular design of a progressive that will go in all of the games.

**Michael Gottlieb** 22:38  
Yes, in all of the lines and ways games, not Jackpot, Rush or Fiery Ice, but the lines and ways games for Jackpot, excuse me, for Georgia Vertical 2.

**Val Levitan** 22:49  
Thought when bison will inherit the same progressive.

**Michael Gottlieb** 22:53  
Correct. All of them will have it. This progressive replaces the Remember how the Peach progressive was applicable to all of those lines and ways games? We are replacing the Peach progressive with this progressive.

**Val Levitan** 23:05  
And you'll you'll call it pick 3 progressive.

**Michael Gottlieb** 23:08  
Match. Yeah, pick three or match three. I haven't decided yet, but yeah.

**Val Levitan** 23:10  
Gotcha.  
OK. So if I look at Twin Bison, the estimated completion day is March 16th and if I look at pick three, just the progressive portion, it will come 10 days prior to that which is March 6th. That's that's the orientation more or less.

**Michael Gottlieb** 23:32  
Correct.

**Val Levitan** 23:34  
OK, got it. I I have no questions. We can move on to Lyon's riches unless anybody else has questions, but I I seem to be a stickler on the schedule.

**Michael Gottlieb** 23:45  
No, it's great. Nope, not a problem. OK, so GC364, we are going to do a based upon the positive feedback. Well, two things based upon the performance of Lion's Riches in South Dakota, which is our number one game and the fact that it is our number two game in Georgia behind crazy.  
Spins, which is a different type of game. Anyway, we are going to do a update to Lion's Riches. It's going to be for vertical for the vertical release with some some updated backgrounds, some some sharpened art.  
And the other big thing that Juan and I have discussed is the desire for a revised execution of the pay table such that the pay table does not take over the entire half of the screen. It's going to take over a percentage of space.  
Base above the real bundle, but most importantly that will give us a large canvas that will allow us to get a lion up there with the eyes looking at the player and I think that that is the correct approach to take. We will also have a message banner.  
On top of the real bundle to help communicate the messaging that is potentially lost by revising the pay table layout. So this is going to be a game of Tetris that Lena and I are going to have to play.  
To design how the screen should be laid out, it is more challenging than.

**Val Levitan** 25:22  
Can you can you open the subtasks for QC 364?

**Michael Gottlieb** 25:30  
Yeah, right now it's just the abstract.

**Val Levitan** 25:30  
So where, where? So where, where is all of this that you're talking about?

**Michael Gottlieb** 25:35  
I'm just getting started with it now. I just put it in yesterday.

**Lena Zhukova** 25:37  
I I didn't. Yeah, I didn't have to create yet my my features there. Yeah, I do.

**Michael Gottlieb** 25:40  
Right.

**Val Levitan** 25:45  
OK, I've got it. Sorry for, sorry for interruption. If you don't mind, would you please start discussing GC364 again as a refresher, please. I'm sorry.

**Michael Gottlieb** 26:03  
OK, so GC364 is a updated vertical version of Lion's Riches. We are doing this game because it is our number one performer in South Dakota.  
And it is our #2 performer in Georgia behind Crazy Spins, which is a completely different type of game. So Lions Riches is our top performing 5 reel in Georgia and.  
Lena and I are going to redesign the layout specifically.  
Changing the pay table design. The current pay table design takes over the entire top half of the screen and we are going to simplify that and create.  
A small portion in the middle of the screen with pay table information. A line of text that will cycle as you spin above the real bundle that will say things like you know, 3 whatever symbol triggers free spins.  
Three coin stacks trigger match 3 progressive, so we will communicate the instructions to the game.  
That way this will allow us a large canvas of real estate on the top of the screen to put a very large lion, which we believe will be a very impactful presentation and a.  
More current look versus just having the pay table on the top of the screen.

**Val Levitan** 27:58  
Clear for me.

**Lena Zhukova** 27:59  
For now, for now, we are planning to do it only for line switches other.

**Val Levitan** 28:06  
It's too bad. It's oh, I was gonna say it's too bad if it's only for lion's reaches, but because you're saying for twin bison, I compliment you on this. That's that's a great, great thing.

**Michael Gottlieb** 28:07  
And twin bison.

**Lena Zhukova** 28:08  
And and it by sounds, yeah, for only for two new games.

**Val Levitan** 28:23  
Yeah, I I mean, I really like it. I I like both subjects, both, both topics.  
Topics.  
It's how many, how many lines is twin bisons? Sorry, how many reels and lines is twin bison and lines riches?

**Michael Gottlieb** 28:41  
Twin Bison is a three by three. It's a single line game and then when you go into free spins it will have a second reel bundle above it and it'll be 55 lines on the base reel bundle and an additional 5 lines on the second reel bundle above. So you'll have.

**Val Levitan** 28:50  
OK.  
Oh.

29:01  
Yeah.

**Michael Gottlieb** 29:01  
Have one line in play during base game and 10 lines in play during during free spins. And Efim, what is Lions Lions Riches? I don't have it right in front of me. Yeah, it's a five by three, but I mean how many is it a 20? How many lines is it?

**Efim Podvoiski** 29:12  
5 by 3, 5 by 3.

**Lena Zhukova** 29:13  
Wi-Fi screen.

**Efim Podvoiski** 29:17  
Georgia was 25 lines, so.

**Michael Gottlieb** 29:21  
Yeah, 25, right.

**Lena Zhukova** 29:21  
Thank you.

**Michael Gottlieb** 29:24  
Yeah, we do different lines depending upon territory. So yeah, so it's a 2525 line, 5 by 3.

**Val Levitan** 29:33  
And and just just uh.  
I I think I know the answer, but just to be clear, we have flexible RTP per button, right?

**Michael Gottlieb** 29:47  
We have had that in the past, but I believe that's one of the challenges that we identified with game performance in Georgia because we had our lowest bet level set at 88%. So my understanding from Juan is we're going to go back to the kind of the 92 across the board, correct Juan?

**Juan Martinez** 30:02  
But but we will still, we will still maintain that feature. We're just not going to go down to 88.

**Val Levitan** 30:03  
No, we.

**Michael Gottlieb** 30:07  
Oh, yeah.

**Val Levitan** 30:10  
That was my question. So we're maintaining, we're maintaining that requirement, right? And and is it only for the lower bed buttons or all of the bed buttons?

**Michael Gottlieb** 30:10  
Correct.

**Juan Martinez** 30:11  
Yes.  
That's correct.  
All the bed buttons are adjustable.

**Val Levitan** 30:26  
Individually.

**Juan Martinez** 30:28  
Yes.

**Val Levitan** 30:29  
And that's a requirement.

**Juan Martinez** 30:32  
It's been for a while, yes. Even before the new nudge, this was already an available option.

**Val Levitan** 30:45  
And will it have that?  
Small progressive. How do we call it? I forgot.

**Michael Gottlieb** 30:52  
The match 3 progressive.  
Oh, the fast and swift cache. No, no, we're not messing with that.

**Val Levitan** 30:55  
No, no.

**Juan Martinez** 30:55  
The swift.  
Oh.

**Val Levitan** 30:58  
No, no.

**Juan Martinez** 31:06  
Yeah, we we we shouldn't have swift cache because we know we have a limitation as to how many different progressives we can even run on the box.

**Efim Podvoiski** 31:14  
Right.  
And it's replaced with the lowest level of the main progressive.

**Michael Gottlieb** 31:20  
Correct.

**Juan Martinez** 31:21  
Yep. And I think Val froze there.

**Val Levitan** 31:25  
Yeah, I'm back. Sorry. Not we're moving away from all of for all the games. We're moving away from that progressive from swift bonus.

**Juan Martinez** 31:26  
OK.

**Michael Gottlieb** 31:33  
Correct. Yes, correct.

**Val Levitan** 31:36  
Including Nebraska.

**Juan Martinez** 31:40  
Now Nebraska will keep the golden Husk progressive that it has.

**Michael Gottlieb** 31:44  
But not Swift Bonus. We're not messing around, right? Yeah, Swift Bonus is kind of deprecated with everything else that we're doing.

**Juan Martinez** 31:46  
That's it.

**Val Levitan** 31:52  
OK, understood. And why? Why? Why are we doing? Why? Why are we deprecating?  
Uh, Swift bonus.

**Michael Gottlieb** 32:02  
Because there's only so much RTP to go around and it really goes back to the conversation we were having earlier that if you have limited RTP, it's just one more progressive that you have to feed and the presentation level of it is very, very minimal.  
Compared to what we're doing with this big match 3 progressive with the jackpot towers and jackpot rush, we there there's not there had not been as much salesmanship going on with Swift Bonus and it just it was an add-on. It was something, it was a quickie add-on that we did that served us at the time. But right now we've got these other progressives.  
That superseded, I guess would be the correct phrase.

**Juan Martinez** 32:44  
Yeah, and and trying to to fit a swift bonus icon on the main screen just sort of limits what you can do, Val. And having it on the V deck, it loses some of its impact if it's not, you know, front facing.

**Efim Podvoiski** 32:45  
OK.

**Michael Gottlieb** 32:59  
Right.

**Val Levitan** 33:02  
OK, I have no more questions on the concept.

**Michael Gottlieb** 33:09  
OK, very good.

**Val Levitan** 33:09  
We can, we can collapse that.

**Michael Gottlieb** 33:15  
OK, Lena, do you want to pick up on game designs and I'll jump in as needed?

**Lena Zhukova** 33:20  
With game design we continue to work on IP887 South Dakota VLT2 IP 1017 Wild Code updates for South Dakota is in progress. Almost done.  
Next is going to be IP 1018 Uh Dragon face updates. Uh uh.  
And I think this is it for now for design. This is Dragon Pace will be the last game for South Dakota. We will need to do some updates.  
For con parts.

**Michael Gottlieb** 34:10  
And this was, this was the topic of conversation to remind everybody that we're we're going back to Royals. This was a game that had, you know, kind of funky gems, very detailed gems, and it's a game where we're going to go back to Royals.

**Lena Zhukova** 34:27  
Yes, and the.

**Val Levitan** 34:27  
I thought. I thought the conversation about Royals was focused on Georgia instead of South Dakota, South.

**Michael Gottlieb** 34:35  
South Dakota inherited South Dakota inherited that approach for the low paying symbols from Georgia because we were trying to get those games done really fast.

**Juan Martinez** 34:47  
Yeah, but in South Dakota never had that restriction. So we're definitely OK to to go in that direction.

**Val Levitan** 34:47  
OK.  
OK, so I understood why South Dakota, but the principal.  
Change, of course, on the Royals has to do with the.  
Previous assumption of the, you know, perceived restrictions in Georgia.

**Michael Gottlieb** 35:13  
Correct. The perceived directive that there were restrictions, yes.

**Juan Martinez** 35:13  
Right.

**Lena Zhukova** 35:16  
Now in in Georgia and South Dakota, we are going to use letters for Royals and we are going to use our updated version of Royals, which is cleaner and more like modern book.  
Even for games for South Dakota, even for games which had letter Royals before, we are going to update.

**Val Levitan** 35:43  
And you guys are OK introducing Oriental style game in South Dakota?

**Michael Gottlieb** 35:51  
Yeah, I I think so. I think having one is is not a.

**Juan Martinez** 35:51  
Yeah.

**Lena Zhukova** 35:53  
Yeah.

**Juan Martinez** 35:58  
Yep, there's there's plenty of Asian games on the other guys boxes.

**Val Levitan** 36:04  
OK, I don't have any more. Go ahead.

**Lena Zhukova** 36:05  
And it's this game about mhm.  
It's game about dragon and I think like everybody likes dragon, so dragon so.

**Val Levitan** 36:15  
I don't have any more questions on game design.  
Unless you guys have questions. I mean, when I say I don't have, I welcome the floor to everybody else.

**Lena Zhukova** 36:26  
Yeah, so this when we finish with South Dakota design, then I will focus on concepts for this new games for Georgia and then when we finish concepts they will they will go to design level.  
To buy some sand and new lines.

**Val Levitan** 36:47  
Yeah, that will be, yeah, that will be exactly.  
OK.

**Lena Zhukova** 36:56  
OK, so in game production we're also focusing on IP459 South Dakota Realty. We are actively working on Black Hill Skinner game, Cool Cat Kino.  
Liquid Glass style home screen La Rosa game and we started on rodeo spins and line switches updates in production.  
Um.  
We finish actually all what which what we discussed like last on the last meeting for IP975 Florida market for IP877 Kaya Ochi only game.  
We finished all art features. There were only one features which left last week. It was attraction video and now it's done.  
I am not closing the IP 877 because I think there are like other like from which is there which you don't see.  
For now we see only art issues, but all art issues are done for this game.

**Val Levitan** 38:35  
Sorry, I I need to park Florida market Florida only for a second.  
I need to go up to start the quarter.  
So.  
Jackpot rush.  
Is all done, am I correct?  
For South Dakota.

**Lena Zhukova** 39:06  
Yeah, we are not too inch of a trash for now for South Dakota. We we marked it down because we decided not to release it for SDVLT 2.

**Val Levitan** 39:20  
But OK, should we not put it in in backlog or we will never do it? Should we are private?

**Juan Martinez** 39:28  
Remember, we we committed to doing the vertical for South Dakota, so I can see this going on the vertical and mimic what we're doing for Georgia.

**Val Levitan** 39:39  
I I know, but it's hanging in our schedule.  
So my assumption, we should probably archive it and then pull it from archive when we decide to do something with it.

**Juan Martinez** 39:53  
OK.

39:54  
Makes sense.

**Val Levitan** 40:09  
Kindly save it please. Thank you.  
OK, cool. OK, hold on, hold on.  
Hold on.  
You cannot have something in backlog if there is a schedule against it. So can you please put Dragon Pace and wild code? Yeah. Thank you. OK. Thank you.

**Juan Martinez** 40:44  
Oh.

**Val Levitan** 40:46  
So is that a true production? This is like, this is what we're looking for, right? So right now actively in production.  
Sorry for now, can we go back to down to Kaya Ocho for Omni?  
So there's no schedule for it. So it we we need to put a stop at it because it's becoming extremely aggravating. No schedule cannot be in progress.

**Lena Zhukova** 41:21  
Well, I think under this IP there are from issues which you don't see now. I I am not sure that only artists are using this IP. That's why I don't want to close it.

**Val Levitan** 41:37  
Sorry, can you explain this please?

**Lena Zhukova** 41:40  
Uh.

**Val Levitan** 41:42  
What? What did you say, Efim?

**Lena Zhukova** 41:47  
Uh, OK.

**Val Levitan** 41:48  
I just. I just didn't. I just didn't hear you. Can can you please repeat?

**Lena Zhukova** 41:53  
I for now I don't see like any like there were like one from issue which Biratko closed. So maybe we can we can close it. I I I just know I'm not sure like they like developers they have.  
Their own IP for where where the link their issues. I'm not sure if no like I I see only our issues here so then then we can we can close.

**Val Levitan** 42:29  
You're saying you're saying that there might be something in a framework, right?

**Lena Zhukova** 42:35  
Yeah, but now I see like, uh, Alexander closed his issue here.  
I I'm sure he he still has some open issue on, but maybe they're using different IP.

**Efim Podvoiski** 42:51  
Yes.

**Val Levitan** 42:52  
And that's why you keep it in progress. But but I don't understand if it's in progress, how even if they have open issues, why doesn't it show the schedule?

**Lena Zhukova** 42:55  
Yes.

**Val Levitan** 43:06  
What could be the problem?  
OK. I need to think about it. OK. Can you please go back to the to the plans?

**Lena Zhukova** 43:20  
Maybe, maybe you're right. Maybe they're they're keeping all the issue here like and I don't, I don't know where it's like from issues here. So that's why we don't see them under this IP and if all artistic features are done, we we should close it.  
And probably I can close the track one.  
I I think you're right.

**Val Levitan** 43:48  
Uh, I.  
I I don't know. I need to think it through.

**Lena Zhukova** 43:52  
Yeah, let's, let's, let's think about this PFL.

**Val Levitan** 43:55  
OK.

**Efim Podvoiski** 43:55  
It's definitely not released, right?

**Lena Zhukova** 43:58  
Yes.

**Val Levitan** 43:59  
Right. Well, well, yes. But I mean, our schedule stops. The the stops in the schedule may also be incorrectly named. I mean, we might be using wrong taxonomy. So you're right, it's not released, but.  
As far as roduction, maybe it's done and maybe we shouldn't release it in roduction. Maybe we should release it somewhere else.  
But that's fine. That's not a conversation for this meeting. Can you please collapse the Kayocho?  
OK. So let's go back to. Uh huh. Thank you.  
Can you?  
Can you open IP 986 please?  
Mhm.  
OK, I see. Understood.  
OK, you can collapse.  
OK. Uh, anybody has anything to add on the production side?

**Efim Podvoiski** 45:31  
And do you know what was the conclusion of this about the fact that we only have one programmer for this project?

**Val Levitan** 45:41  
We're gonna have a one month extension in the schedule.

**Lena Zhukova** 45:41  
Like.

**Efim Podvoiski** 45:45  
Mhm.

**Val Levitan** 45:47  
But I think it will be less than one month.

**Efim Podvoiski** 45:51  
Maybe.

**Lena Zhukova** 45:55  
So yeah, if Juan is OK with this extension, so that's this is good. Yeah, because Pavel Pavel updated me today that the Igor cannot work while while he's in military camp. So we thought probably he can do it like after hours, like in the evening, but.

**Efim Podvoiski** 46:10  
Mhm.

**Lena Zhukova** 46:14  
Today, if I have updated me that it's impossible.

**Val Levitan** 46:16  
OK, OK. OK. Anybody has any more questions?

**Juan Martinez** 46:23  
Nope.

**Val Levitan** 46:23  
OK, we're done with the schedule.

**Michael Gottlieb** 46:26  
Yes.

**Val Levitan** 46:28  
Perfect.

**Val Levitan** stopped transcription