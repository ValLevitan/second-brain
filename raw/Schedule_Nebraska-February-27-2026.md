**Schedule changes for Nebraska release-20260227_080239-Meeting Recording**

27 February 2026, 01:02pm

49m 5s

**Val Levitan** started transcription

**Val Levitan** 0:05  
We're waiting for Paula, right?

**Juan Martinez** 0:07  
And he just got up.

**Val Levitan** 0:08  
Mm.

**Pavel Frolov** 0:12  
Yeah.

**Val Levitan** 0:14  
Hi Pavel, how are you?

**Pavel Frolov** 0:15  
Good morning. Yeah, everything is fine.

**Val Levitan** 0:16  
Mhm.

**Pavel Frolov** 0:19  
Shpak.

**Irina Shishko** 0:19  
Yeah.

**Val Levitan** 0:20  
Okay.

**Pavel Frolov** 0:21  
Just, just first run.  
Of FlexPay with two monitors.

**Irina Shishko** 0:26  
Yeah.  
Thanks.

**Val Levitan** 0:28  
Doesn't look like, it doesn't doesn't look like flex POS, it looks like flex flex ruins, flex garbage.

**Pavel Frolov** 0:28  
Flex boss, flex boss.

**Juan Martinez** 0:33  
Ohh.

**Irina Shishko** 0:36  
Ohh.

**Juan Martinez** 0:36  
Yeah.  
Mm.

**Irina Shishko** 0:41  
No.

**Val Levitan** 0:42  
Congratulations.

**Irina Shishko** 0:44  
I'm still is that what?

**Pavel Frolov** 0:44  
Hmm.

**Val Levitan** 0:46  
I know, I know, I know, bunch of pieces. Yeah, okay. So as always, we need to interrupt our priorities and shift this particular issue to the forefront. I apologise for that. I hate to do it. But and

**Pavel Frolov** 0:46  
Mm.

**Val Levitan** 1:04  
And I think...  
We did a wonderful job in planning and scheduling without causing much emergencies, but this one is really urgent for us. So back to Nebraska.

**Pavel Frolov** 1:06  
Okay.  
Yes.

**Val Levitan** 1:17  
And.  
We are going to be redesigning the way our games work.  
And from what I read in a bunch of emails, it will look very much similar to a Giorgi release with some additions, right?  
One, maybe you could brief everybody in.

**Pavel Frolov** 1:42  
Yeah.

**Juan Martinez** 1:42  
Yeah, sure. So, you know, we made an observation that obviously this was our first Nebraska skill game. There were limited competitors in the market. All of a sudden, light and wonder appeared. And they're using a different tactic.  
The regulator was somewhat strict with us on holding us to the letter of the law of how skill works in Nebraska. We now clearly see by light and wonder that there is flexibility there. So we want to adjust our skill method in Georgia to  
increased speed for the player and to reduce their ability to enter the secondary memory skill by, you know, I don't want to say hiding it, but by making it a little more difficult to see, similar to what Light and Wonder has done.

**Val Levitan** 2:22  
Be.

**Pavel Frolov** 2:26  
Ohh.

**Juan Martinez** 2:42  
So on top of that, we're recommending that we use the liquid glass display concept that if you've looked at the recent Georgia vertical project we're working on, as well as South Dakota, we're going to introduce a new look to the home screen, the buttons, the introduction of a banner that clearly displays  
the types of games in different categories. So that'll be done. If need be, I could share a screen image of that. You guys let me know. I'm not sure how much you've seen of it or not. So just give me one second here.

**Pavel Frolov** 3:06  
It is.  
The.  
Yes.

**Juan Martinez** 3:43  
Yeah, so if you can see my screen, this liquid glass effect, similar to an iPhone, is the name of the concept. You know, we're adding these banners to categorise each game type to make it easier for the player to find it. And then the traditional peach style games here at the top. So

**Pavel Frolov** 3:50  
Shh.

**Juan Martinez** 4:06  
Obviously, we'll head in this direction for Nebraska. We're not ready to introduce what you see down here yet, but so we're just going to make modifications to what you see here in the top portion.

**Pavel Frolov** 4:07  
It's.  
Is.

**Juan Martinez** 4:19  
In addition to these graphical changes, we currently have 3 requisitions associated with Nebraska, Rec 998, which is the introduction of the audit ticket, which is similar in concept

**Pavel Frolov** 4:25  
20.

**Val Levitan** 4:26  
Okay.

**Juan Martinez** 4:39  
Pavel Irina, we've already briefly discussed this one. You know, a slight modification of what we're already doing in South Dakota, but this was a note from the operator that the way they balance their books with the locations involves an audit ticket and that audit tickets are standard in markets like Nebraska and Texas. So

**Pavel Frolov** 4:52  
Yeah.

**Juan Martinez** 5:01  
We're going to comply not just for Nebraska, but for Texas software as well. And I owe Pavel, Pavel, you've already sent me some comments from Igor as well on audit ticket. So Val, do we need to dig into the actual requirements on this call? How did you want to proceed?

**Pavel Frolov** 5:04  
Sex.

**Val Levitan** 5:21  
Yes, I would like to do dig into requirements and.

**Juan Martinez** 5:25  
Okay.

**Val Levitan** 5:27  
This conversation is recorded, so we're generating a transcript. I think all of us are becoming much more...  
Comfortable with...  
Moving from recorded transcript to...  
writing out requirements, pushing those requirements into Jira directly.

**Juan Martinez** 5:49  
Sure.

**Val Levitan** 5:53  
Likewise, I think, I'm not sure about Juan, but Pavel I think is quite comfortable with describing JIRA tasks through transcripts and pushing them into JIRA right away. So the more details we can describe on the call.  
with using proper taxonomy in whatever language, English or Russian.  
Have a productive solid transcript generated from it.

**Pavel Frolov** 6:26  
Okay.

**Val Levitan** 6:30  
The easier it is then for everybody to uh...

**Pavel Frolov** 6:32  
I.

**Val Levitan** 6:34  
deal with bureaucracies associated with time spent on maintaining and managing JIRA and schedules, etc.

**Juan Martinez** 6:45  
Absolutely.

**Val Levitan** 6:45  
especially when generating tasks, descriptions, etc.

**Pavel Frolov** 6:47  
I.  
Mm.

**Irina Shishko** 6:51  
K.

**Juan Martinez** 6:52  
Okay, agreed. So like I said, so right now the  
Preliminary 3 engineering related requirements are requirement 998, which has to do with the introduction of an audit ticket, requirement 1007, which has to do with the whole dollar and rounding  
of a cash out ticket. And the newly introduced one, requirement 1010, has to do with the overall graphical changes to the Nebraska software and the skill component of it. So I'm going to share my screen and we'll start with requisition 998.

**Irina Shishko** 7:44  
Mm.

**Juan Martinez** 7:44  
This one should be straightforward. As I said, the customer has requested that we produce an audit ticket for their ability to reconcile on a weekly, bi-weekly basis with the location. Unlike the South Dakota audit ticket,

**Pavel Frolov** 7:48  
Shpak.  
That is.

**Juan Martinez** 8:03  
This ticket does not auto print every time you open a door. This ticket is to be produced manually by going through the setup menu, locating the audit ticket, and hitting print. And likewise,

**Pavel Frolov** 8:16  
D.

**Juan Martinez** 8:22  
the ability to clear the period meters, which Irina confirmed, it's already there. So we just need to figure out where the audit ticket button will appear and that we don't do anything automatic because if the ticket doesn't print,

**Pavel Frolov** 8:26  
The.

**Juan Martinez** 8:42  
The customer needs to resolve the printer problem, add paper. We want it to be fully manual so that they can actually produce a working ticket. We've already discussed the required fields. MG Oil made a point that, hey, since we already use your audit ticket for South Dakota,

**Pavel Frolov** 8:51  
Please.  
Shpak.

**Juan Martinez** 9:03  
no real need to change the fields since they're comfortable with the South Dakota one. So the fields are in requisition 998. I do believe you've had a chance to review all them. So I do believe this one is self-explanatory. And I just owe you some language clarification, Pavel, that you asked for, and I'll do that today. So

**Pavel Frolov** 9:16  
The.  
Okay.

**Juan Martinez** 9:27  
Any questions on the Nebraska audit ticket?

**Pavel Frolov** 9:31  
Rich.  
Mm.

**Irina Shishko** 9:38  
First.

**Pavel Frolov** 9:45  
Oh, so Irina is asking, uh, when's the attendant, uh, Torrance Key?

**Juan Martinez** 9:52  
Mhm.

**Pavel Frolov** 9:53  
Actually, right now, we assume that we will show some floating screen that will say, do you want to print an audit ticket with button yes?  
Is it okay or logic need to be changed to something else to go to some menu and select print?

**Juan Martinez** 10:18  
Well, I guess that's a question for you. I assumed it was going to go to an existing menu only because I believe that would be less work for you. But if this pop-up screen, the only problem though is the flow, you know, when you turn a key, you're normally clearing a jackpot, you're already accessing the service menu.

**Pavel Frolov** 10:29  
But.  
Yeah.  
Yeah.

**Juan Martinez** 10:41  
How do this, how does this pop up not block?  
A hand-paid clearing or access to the regular service menu.

**Pavel Frolov** 10:51  
Oh, I think this is not a problem because when you need to clear jackpot, it actually relates to the game.  
But after you clear and turn in the key, you will enter a screen, a setup screen related to attendant.

**Juan Martinez** 11:08  
Mhm.  
Right.

**Pavel Frolov** 11:11  
And it will be a separate pop-up message. And it actually looks different than the game pop-up messages.

**Irina Shishko** 11:19  
Mm-hmm.

**Juan Martinez** 11:21  
Okay. Yeah, that sounds like that's a clear message. I guess before we commit too far along the process, could we get a mock-up from Igor and Figma of what this could look like?

**Pavel Frolov** 11:26  
****.  
Igor no no with us more.

**Juan Martinez** 11:39  
Ohh, okay.  
Okay.

**Irina Shishko** 11:41  
Set up.

**Pavel Frolov** 11:44  
Ira will take a screenshot from the...

**Juan Martinez** 11:48  
Okay.

**Pavel Frolov** 11:48  
Good.

**Juan Martinez** 11:50  
Print.

**Pavel Frolov** 11:51  
Gina will provide some screenshots from implemented screens to show how it looks like.

**Juan Martinez** 11:52  
Okay.  
Okay.  
understood. So any questions on the audit ticket?  
Okay.

**Pavel Frolov** 12:09  
No, no.

**Juan Martinez** 12:10  
OK, OK, so next we're going to...

**Val Levitan** 12:13  
If there are no questions going back to the previous ticket, REQ998, I would like to move it.

**Pavel Frolov** 12:14  
Shpak.

**Val Levitan** 12:27  
Um...

**Pavel Frolov** 12:29  
Draft.

**Val Levitan** 12:31  
Yeah.

**Pavel Frolov** 12:32  
Oh, okay, Dan.

**Val Levitan** 12:33  
Yeah.

**Irina Shishko** 12:33  
Mm, mm, come.

**Juan Martinez** 12:35  
OK.

**Irina Shishko** 12:36  
That.

**Juan Martinez** 12:36  
Done.

**Val Levitan** 12:38  
So from I think it's approved. What's the next date after draft? I forgot.

**Juan Martinez** 12:46  
A request review.

**Pavel Frolov** 12:47  
Ohh.  
Yeah.

**Val Levitan** 12:49  
Well, yeah, so we're reviewed.

**Juan Martinez** 12:52  
Yes.

**Val Levitan** 12:54  
So, what's the what's the state after that?

**Irina Shishko** 12:55  
Published, but only yes never published.

**Pavel Frolov** 12:58  
And the next will be published.

**Val Levitan** 13:05  
Yeah, let's shift it to the next stage, please, after.

**Pavel Frolov** 13:08  
Done.  
Just update your screen.

**Juan Martinez** 13:17  
And it is now published.

**Irina Shishko** 13:19  
Mhm.

**Pavel Frolov** 13:19  
Yeah.

**Juan Martinez** 13:21  
Nope.

**Val Levitan** 13:42  
the leadership on this and just consume Irina and Pavel for 15 minutes. Be on the clock. Doesn't matter if you have time or not. Don't overburden anybody. Just literally do 3 tickets.

**Juan Martinez** 13:44  
Sure.

**Pavel Frolov** 13:48  
Yes.

**Juan Martinez** 14:01  
Okay, understood. Also, I'm watching the edits that Dmitri is making in the system, auto modifying the acceptance criteria tag, and I'm seeing some duplicates. So I was going to go back and start with what he's done, at least to my...

**Pavel Frolov** 14:19  
He.

**Juan Martinez** 14:20  
tickets, he's created a duplicate acceptance text. So I was just going to delete those duplicates within the body of that. So just an FYI, whatever he's doing in certain instances is creating a duplicate, the acceptance criteria, and then the acceptance criteria inserted twice.

**Pavel Frolov** 14:35  
Yeah.

**Juan Martinez** 14:39  
So it's just taking up extra room in the description field.

**Val Levitan** 14:44  
Oh, okay, because he...

**Juan Martinez** 14:45  
I'll send you a sample.

**Irina Shishko** 14:46  
But.

**Val Levitan** 14:47  
because he is doing it automatically.

**Juan Martinez** 14:50  
I guess, yeah, yeah.

**Val Levitan** 14:52  
Yeah, he doesn't read every single description, but what he's trying to, what we need to do is to get rid of a separated acceptance criteria and move the acceptance criteria under the description field. So if those, if some, if some description fields already had.

**Pavel Frolov** 15:03  
Hmm.  
Ohh.

**Irina Shishko** 15:08  
Mhm.

**Pavel Frolov** 15:09  
Good.

**Val Levitan** 15:11  
The acceptance criteria in it, then it will be duplicated, but...

**Juan Martinez** 15:16  
Yeah, and mine did, and that's what I'm seeing, so yeah.

**Val Levitan** 15:19  
I wouldn't be so worried about it because eventually these tasks are going to get closed. The extra custom field acceptance criteria will disappear. And moving forward it will be OK and the and an MCP.  
will pick up on the duplication of acceptance criteria. But by the way, we could clean it up through an MCP, so don't worry about it.

**Juan Martinez** 15:40  
OK.

**Pavel Frolov** 15:44  
Yeah.

**Juan Martinez** 15:45  
Okay.

**Val Levitan** 15:46  
Don't waste your time on it. But do please, please groom the requirements issue type.

**Juan Martinez** 15:59  
Absolutely.

**Pavel Frolov** 16:00  
Mhm.

**Juan Martinez** 16:01  
All right, so closing requisition 998 has been moved to publish.

**Pavel Frolov** 16:05  
Hmm.

**Val Levitan** 16:06  
It's not requisition, it's requirements.

**Juan Martinez** 16:08  
Oh, I'm sorry, requirement. You're right. Requirement 998 has been moved to publish. Our next requirement is 1007. And again, this was a customer request. The customers prefer not to redeem a Tito ticket.  
that has fractional change or coins on it. These locations have a kiosk that just dispenses cash and they do not want to deal with coins. So we certainly understand that. So this is a request from the customer and this will apply to both Nebraska and Texas.

**Irina Shishko** 16:34  
Mm.

**Pavel Frolov** 16:43  
Mm.

**Juan Martinez** 16:49  
Rounding. I'm asking that we introduce a rounding feature. The customer says that the players are okay with the fractional change remaining on the machine. So we can each target that through allowing the last risk bet anyway.  
But we need to create a feature where we allow through an enable or disable option, the removal of anything less than a dollar on a Tito ticket. Example, if the cash out is $15.25, when you press cash out,  
The 25 cents should stay on the credit meter, and the Tito ticket should come out only for $15. So we're looking to leave anything less than $1 on the machine's credit meter, and only the whole dollar amount comes out on the Tito ticket.  
And again, obviously, this should be an on and off switch where we turn rounding off if needed, or we turn it back on if the location does support coins in their kiosk.

**Pavel Frolov** 18:03  
Hmm.

**Juan Martinez** 18:05  
Any questions on this requirement?

**Irina Shishko** 18:06  
No.  
But.

**Pavel Frolov** 18:10  
Yes, yes.  
Just to confirm, we do not round anything, but we left all the money less than $1.00 on the machine.

**Juan Martinez** 18:30  
That is correct.

**Pavel Frolov** 18:32  
Is this?

**Juan Martinez** 18:34  
That is correct.

**Pavel Frolov** 18:35  
And after cash out, after cash out, then so if some money less than $1.00 left on machine, it will automatically trigger the last bet risk.

**Val Levitan** 18:37  
Yeah.

**Pavel Frolov** 18:54  
Shishko.

**Juan Martinez** 18:56  
Yes, yes, and...

**Irina Shishko** 18:57  
Ah, yes, you were you earlier?

**Pavel Frolov** 19:01  
If the player won.

**Irina Shishko** 19:03  
So, I was probably...

**Pavel Frolov** 19:04  
This bonus, it will be a spin, and he can continue playing on this machine.

**Juan Martinez** 19:10  
That is correct. That's the proper behavior, yes.

**Irina Shishko** 19:13  
Oh.  
Mmh.

**Pavel Frolov** 19:17  
G.

**Val Levitan** 19:18  
Maybe, maybe, maybe this behaviour should be fully described in this RQ.

**Juan Martinez** 19:19  
Have.  
Yes.  
I will modify it, and...

**Irina Shishko** 19:30  
Mhm.

**Juan Martinez** 19:31  
Add that behavior.

**Irina Shishko** 19:33  
Les Desmarais.

**Juan Martinez** 19:37  
I mean, it's partially in here, but I will.

**Pavel Frolov** 19:38  
The.

**Irina Shishko** 19:38  
Oh.

**Juan Martinez** 19:43  
I mean, it's partly described Val, so you tell me if I need to add more detail to.

**Val Levitan** 19:53  
Actually, you need to find a...  
compromise with Irina, if she understands it, then we're good.  
Because she'll have to test it.

**Juan Martinez** 20:06  
Alright, so, Irina, yeah, out.

**Val Levitan** 20:07  
So, Irina, do you, Irina, Irina, do you want to want to?

**Irina Shishko** 20:09  
Okay.

**Val Levitan** 20:14  
Update the requirement, the description, or add acceptance criteria to it.  
Yeah, she would like you to describe the operation, including the risk feature.

**Juan Martinez** 20:32  
Okay.

**Irina Shishko** 20:37  
No, yes.

**Val Levitan** 20:37  
Okay.

**Pavel Frolov** 20:37  
Just.

**Val Levitan** 20:46  
Yes, if we use AFT, then we will pay the entire amount, including the fractional pay.

**Juan Martinez** 20:57  
Yeah, correct. I mean, currently there is no AFT going on in Nebraska or Texas, but yes, that is correct behavior. I'll include that.

**Val Levitan** 21:11  
The one you are to update the behavior.

**Juan Martinez** 21:11  
Right.

**Val Levitan** 21:17  
for what is it, number 10-07?

**Juan Martinez** 21:19  
One 1007.

**Val Levitan** 21:22  
Yes.  
Can you move it to review, please?

**Juan Martinez** 21:29  
And I edit it if after it's moved to review. Like I just want to make sure I'm not locked out from editing the.

**Val Levitan** 21:34  
Well, it's in.  
Sure, sure, sure, but I think in review it's not locked out, but yeah, that's fine, of course.

**Juan Martinez** 21:44  
Okay.

**Val Levitan** 21:46  
Moving on.

**Juan Martinez** 21:48  
So the next requirement related to Nebraska is requirement 1010. And this is a high level requirement that focuses on our observations and behaviours of how our nudge works. So

**Irina Shishko** 21:56  
Okay.

**Juan Martinez** 22:09  
The bulk of this is going to be on the graphical team requirement to remove the current power metre that we show, as well as to modify our very crystal clear message here where we tell the player to touch the pattern match. So the graphics team is going to remove the border.  
They're going to reduce the size of the font, and they're going to make the font colour darker to sort of blend into the background to make it less obvious for the player. And that's what the competition is doing. And within  
The acceptance criteria here, I listed the other requirements we've already reviewed, because this goes in as part of the entire package.

**Pavel Frolov** 22:53  
Cris.  
I.  
East.

**Juan Martinez** 23:04  
The graphical team replacing the power metre primary skill, we're going to go with a 50-50 type of display where the customer merely has to choose which icon contains more coins or more money. So it's a straight 50-50 versus our power meter,

**Pavel Frolov** 23:11  
Two.

**Juan Martinez** 23:26  
which requires physical dexterity to try to land on 100%. So this will speed up gameplay, no doubt. I don't necessarily know if there's any engineering work behind selecting of two icons on screen or not, but that's what we'll do.

**Pavel Frolov** 23:40  
Yeah.

**Juan Martinez** 23:45  
Let me also pull that up.  
Yeah, I'll add it here. And I've linked all the other requirements under this one, just so you have it.

**Pavel Frolov** 24:15  
Yeah.

**Juan Martinez** 24:16  
Val, one of the questions I had was, today, Nebraska, Texas software are identical. Most of these changes also make sense for Texas.

**Val Levitan** 24:28  
Yeah, Val.  
Yeah, but not the game changes, right?

**Juan Martinez** 24:36  
Well, that's a question for you. Do we really want to create two different branches here or do we, everything that applies here will eventually go into Texas?  
The audit ticket, you know, I think that makes sense. The rounding, the fact that we can turn that on and off, makes sense to keep if operators don't have coins in their locations. And the liquid glass is just a better visual presentation  
So, you know, otherwise we have to keep 2 development streams to keep Texas looking more like traditional peach and less liquid glass, yet we still have to keep the name Nebraska in it as we previously agreed we were not going to call anything Texas.

**Val Levitan** 25:29  
Well...

**Pavel Frolov** 25:31  
The.

**Val Levitan** 25:32  
First of all, I have a...  
I have a question. Are you sure that liquid glass interface will be ready in a reasonable time? Because we need Nebraska out in locations within weeks.  
So if the liquid glass implementation is only coming in 30 days from now, I don't want to wait for it.

**Pavel Frolov** 25:52  
I.

**Juan Martinez** 26:01  
I don't know, because it's not exactly game by game. So we're going to do 2 submissions for Nebraska, one now and one later.

**Val Levitan** 26:12  
I would not even do submission right now for Nebraska.

**Pavel Frolov** 26:14  
Yeah.

**Juan Martinez** 26:16  
No, we have to. We have to. We have to use Eclipse or GLI. That's definitely a requirement. We just don't have to represent it to the attorneys. We just get the approval and go right to the customer.

**Irina Shishko** 26:21  
Ohh.  
A little.  
Is it?

**Juan Martinez** 26:28  
But we still have to go to the lab.  
Yeah, Nebraska is a GLI or eclipse jurisdiction.  
Yes.  
We used Eclipse last time.

**Val Levitan** 26:43  
But, but is it, but is it a requirement to have a lab prior to testing in locations?

**Juan Martinez** 26:54  
Oh yeah, I mean, we need to, the lab sends every approval letter to the Nebraska Department of Revenue.

**Val Levitan** 26:57  
Hello.  
Cool.

**Juan Martinez** 27:03  
At the same time, it comes to us, so...

**Val Levitan** 27:06  
But we already have our approval and we operate legitimately. Do we need to submit a checksum or can we just upgrade the game in location?

**Juan Martinez** 27:19  
So remember, Nebraska uses Intralot, so there's some marriage between our CRC or MD5 Shaw value against Intralot that enables the machine to connect. Pavel, I believe that's what we do in Georgia. You can't just turn on the game

**Irina Shishko** 27:30  
Suppose.

**Juan Martinez** 27:38  
There's some sort of data mismatch if it's not registered with Intralot.

**Pavel Frolov** 27:42  
Yeah, exactly. A new version with new numbers will definitely been seen by the lottery.

**Val Levitan** 27:44  
But is...

**Irina Shishko** 27:46  
Yeah.

**Val Levitan** 27:51  
Is the interlock already operational?

**Juan Martinez** 27:55  
Yep, they've been operational since July of last year.  
And, and all the installations we did in January, we certainly connected to Intralot.

**Irina Shishko** 28:08  
Suppose.

**Val Levitan** 28:19  
Okay, it still doesn't change anything.  
if it doesn't seem like liquid glass is imminently ready.  
I think we're talking about...  
in excess of 30 days plus.

**Juan Martinez** 28:37  
Okay. Well, we'll fine-tune that on our development call later today.

**Val Levitan** 28:39  
Soap.  
I'm just suggesting that...  
These 3 REQs.  
plus game modification, I assume, could probably be done much faster. But if you get stuck with liquid glass implementation, that may take a couple of months.

**Juan Martinez** 29:05  
Sure.  
Read.  
Okay.

**Irina Shishko** 29:26  
Кратно доллару или нет включать выключать, если я правильно это.  
Поняла, есть такое.

**Pavel Frolov** 29:33  
Хуан.  
Куды прессы чек то реклама цен о seven?

**Juan Martinez** 29:41  
Значит свой 4.

**Pavel Frolov** 29:42  
А я я свеч.

**Val Levitan** 29:44  
Ясно.

**Pavel Frolov** 29:47  
А. с Ириной за скин из этих Чили реквиемам то хэвен option ту ту ту мейк он оф.  
А фазы с фича.  
Хех fraction.  
Замещением.

**Juan Martinez** 30:07  
Айгуль целый ящик был на убрал белок, лишен это сам пойдем.  
И пауэр.  
Чего ещё в направился пакистанской колледж? Вот хапчоне.  
Хочешь раунды?

**Pavel Frolov** 30:29  
Угу.

**Juan Martinez** 30:32  
Так так так факел ковролин долго общин павильонов.

**Irina Shishko** 30:32  
Паш.  
А ваш муж это перевести? Я не уловила да или нет?

**Pavel Frolov** 30:42  
Угу.  
Ой, Ну что лучше иметь это в виде опции, потому что? А вдруг какие то локейшн сны у них у киоска есть возможность выдавать монеты и тогда, чтобы не возникло вопрос у игроков и локейшн.

**Irina Shishko** 30:50  
Ну.  
Всё ну.  
Ну тогда нужно и это добавить сюда.

**Pavel Frolov** 31:06  
Окей, Ренессанс соус из point ниптб тритон indirection ф з с рекламист то хеф параметр.  
Свечи он.

**Juan Martinez** 31:16  
И.  
Кто там уже?

**Irina Shishko** 31:46  
И я так понимаю, мы это на машине разрешаем включать свой ключ.

**Pavel Frolov** 31:51  
Да.

**Val Levitan** 31:56  
Павел совет, что нибудь?

**Pavel Frolov** 31:56  
Всё Лукас.  
Но всё как.  
Ну.

**Juan Martinez** 32:22  
Done.

**Pavel Frolov** 32:23  
Then.

**Irina Shishko** 32:25  
Mhm.

**Pavel Frolov** 32:26  
Okay.  
You.

**Juan Martinez** 32:28  
Do you believe that the on or off switch is going to add significant time to the requirement?

**Irina Shishko** 32:28  
So.  
There was.  
Make sure I sent you.

**Pavel Frolov** 32:35  
No, no, not exactly. So just to clarify, I think we will need for Nebraska and for TXS to make this option on by default, but allows location to change it at any time when they want it.

**Irina Shishko** 32:36  
Show me some chicken.  
She would.  
And, actually.  
Cris.

**Juan Martinez** 32:54  
That's correct. Not hard-coded via RIS. They can manually adjust it. Yep.

**Pavel Frolov** 32:55  
Mm.

**Irina Shishko** 32:55  
I'm here.

**Pavel Frolov** 32:56  
Yeah.

**Irina Shishko** 33:00  
No.

**Juan Martinez** 33:02  
Right.  
Okay.  
This one is in draft. Do we does it? Do we leave it in draft?

**Irina Shishko** 33:07  
Yeah.  
Thanks.  
Yeah.  
Mhm.  
I trusted nothing.

**Pavel Frolov** 33:15  
I think if everything is clear, we can proceed to...

**Irina Shishko** 33:18  
Okay.

**Pavel Frolov** 33:21  
Uh, the next steps.

**Irina Shishko** 33:22  
You should of course play against the army.

**Pavel Frolov** 33:25  
If no, any any.

**Irina Shishko** 33:26  
Aaya Ferrari Ski, Chudzinau.  
Yeah.  
If she sees Moyota.

**Pavel Frolov** 33:38  
Ah, OK, yeah, before before to proceed, need to add a risk feature.  
Cheers.

**Juan Martinez** 33:47  
Need to add what?  
Oh yeah, yeah, yeah, yes, the description on the rest bed. Yep, yep, you're right. We'll come back to that one then.

**Pavel Frolov** 33:49  
Uh.

**Juan Martinez** 33:57  
So back to requirement 1010. I don't even know if you guys have had a chance to really read it yet since I did this the other day, but this is just the master requirement overseeing the other two requirements and then the graphical changes for the design team.

**Pavel Frolov** 34:01  
The.

**Irina Shishko** 34:08  
This.  
No.  
Thank you.

**Pavel Frolov** 34:17  
Mhm.

**Irina Shishko** 34:17  
That.  
If you.

**Juan Martinez** 34:23  
Val, we're going to review this also, I'm assuming, during our development call later today. Do you want me to leave this? Do you want me to move it to draught and then we make any adjustments based on our call?

**Irina Shishko** 34:23  
Subit.  
You're welcome.

**Pavel Frolov** 34:32  
It.

**Irina Shishko** 34:33  
On this.

**Val Levitan** 34:38  
I'm not too particular about it. It's not a big deal for me what state it is. I just want to move states forward eventually on all of them. So whether you do it right now or later today, it doesn't matter to me.

**Irina Shishko** 34:45  
And this is the.  
We should go.

**Juan Martinez** 34:49  
Inna.

**Irina Shishko** 34:51  
The.

**Juan Martinez** 34:52  
Okay.  
I just did it.

**Irina Shishko** 34:55  
Shpak.  
Questions.

**Juan Martinez** 34:58  
And really those are the three requirements governing the Nebraska changes.

**Irina Shishko** 35:03  
The.  
I am so in Spanish.

**Juan Martinez** 35:05  
Any questions?

**Pavel Frolov** 35:08  
No.

**Juan Martinez** 35:13  
Val, any questions from you?

**Val Levitan** 35:18  
I guess.  
What, after the requirements written, how do we link them to features?  
What's the process? Because right now we really, I really don't understand the process.  
I'm struggling with it.

**Pavel Frolov** 35:40  
Actually, if the requirement exists and even if it's published, it doesn't mean that somebody takes this into the work.  
So at some moment, we might make some discussion with you or with Lena or with Juan or somebody else who saying that we need this urgently or we need it until this date. And we either create a feature.

**Irina Shishko** 36:06  
Yeah.  
I.

**Pavel Frolov** 36:08  
related to this requirement and schedule stories under these features and start developing.

**Irina Shishko** 36:09  
That was much, Yasha.

**Val Levitan** 36:11  
Go, go.

**Irina Shishko** 36:14  
Thank you.

**Pavel Frolov** 36:17  
Hmm.

**Val Levitan** 36:17  
No, but my question is different. I don't understand.  
The.  
Culture, I don't understand the culture of.  
Generating feature, knowing requirements.  
Let's say we know a bunch of requirements. How does how do features depend on the requirements? I don't understand how it all fits together.

**Pavel Frolov** 36:51  
So, so mhm.

**Val Levitan** 36:51  
To me, it's like 22 separate, 2 parallel inventories.

**Pavel Frolov** 36:59  
Yes, exactly, but they can be referred to each other by this linked work item field. You can see.

**Irina Shishko** 37:08  
Okay.

**Val Levitan** 37:09  
But what's the process of, let's say we created features and we say, okay, for this particular feature, we're going to link these requirements. Who does it?

**Pavel Frolov** 37:10  
Yeah.  
In many cases, me.  
In some cases.

**Val Levitan** 37:27  
But do you actually do you actually do it? You actually do it? Because I think...

**Pavel Frolov** 37:31  
You can see.

**Val Levitan** 37:34  
I believe a lot of our requirements are written and they're well written, but they're not attached.

**Pavel Frolov** 37:41  
Yes, it could be, but for this particular case, you can see it actually referred to the requirement to feature.  
Hmm.

**Val Levitan** 37:54  
Where, well, I see the feature in here.

**Juan Martinez** 37:56  
Yeah, right here.

**Val Levitan** 37:58  
But who linked it? Who actually did it now?

**Pavel Frolov** 38:01  
Me.

**Val Levitan** 38:03  
or you already linked it as we were going along.

**Pavel Frolov** 38:05  
Yes.  
Yes.

**Val Levitan** 38:11  
Okay, I don't understand.

**Pavel Frolov** 38:13  
Highly likely, highly likely, if we have a well-written requirement and using code, we can say, take a look on this requirement and please create a feature for me under this IP, for example. And it will

**Val Levitan** 38:22  
Yeah, I was.

**Pavel Frolov** 38:33  
Quite good to create a new feature in this case.

**Val Levitan** 38:36  
No.  
I'm just saying that what's missing in this is probably...  
a set of architectural decisions.

**Pavel Frolov** 38:45  
Yeah.  
Sure.

**Val Levitan** 38:52  
I just don't see how it links.  
And I do agree that Claude would probably do a good job by linking it, but without the...

**Pavel Frolov** 39:03  
This.

**Val Levitan** 39:06  
a bunch of engineering decisions.

**Juan Martinez** 39:14  
And it just sounds like there's nothing automatic. It's still fully manual.

**Irina Shishko** 39:14  
Mmh.

**Val Levitan** 39:20  
We can definitely automate this process, but I think we are missing a layer of specifications and...

**Pavel Frolov** 39:21  
I.

**Val Levitan** 39:29  
Like an engineering layer.  
But then, anyways, okay, alright.  
This is something that I need to research on how to do.  
But I do believe that it from a bureaucratic perspective, it could, we need to hand it over to Claude.

**Pavel Frolov** 39:57  
Yeah, I agree.

**Val Levitan** 39:59  
Okay, so next step is to create a set of new features.  
for these requirements.

**Irina Shishko** 40:06  
Oh.

**Val Levitan** 40:08  
But we already have features for this.

**Pavel Frolov** 40:20  
So for first two requirements, we will just need some stories related to something that we discussed previously, some minor changes. But for 10-10 requirements, a feature need to be created, I assume by Lena.  
Shpak.

**Irina Shishko** 40:40  
Mhm.

**Pavel Frolov** 40:41  
And, and make a link, probably she already created, but need to make a link to this requirement.

**Juan Martinez** 40:50  
Now, 1010 was literally barely 24 hours old. Michael did already create something in the game concept, and I don't know if that helps towards the feature, but he did open a new game concept surrounding this requirement.

**Pavel Frolov** 40:56  
Done.

**Irina Shishko** 41:14  
Liquid glass.

**Pavel Frolov** 41:20  
Ohh.

**Val Levitan** 41:22  
It depends on where liquid glass is at in terms of development right now. My hunch tells me that probably yes, but let's leave it to our meeting today. Later today, we have a games meeting and we will have a better idea of  
how feasible it is to incorporate liquid blast in it.

**Pavel Frolov** 41:47  
Yeah. Yeah.

**Juan Martinez** 41:56  
Durst.  
Any other questions?

**Pavel Frolov** 42:13  
No.  
I.

**Irina Shishko** 42:33  
A Chinese, South Dakota.  
I'll talk first to the machine, Nathan.

**Val Levitan** 42:42  
Look, look, I'm just translating what Irina is saying. Liquid glass is currently a stage for implementation in South Dakota and currently being worked on.

**Juan Martinez** 42:53  
Right.

**Val Levitan** 42:53  
But if we are putting Nebraska ahead now, South Dakota will get off of critical path and get delayed.

**Juan Martinez** 43:04  
Yeah.

**Val Levitan** 43:08  
if you want the implementation of liquid glass.

**Juan Martinez** 43:12  
Yeah, I mean, I almost think I do, Val. I think that we're in, we're two operators who are the largest ones. Obviously, one of them is MG Oil, who I believe will work with us. So to your earlier question about testing the games, I believe we can certainly test it in their warehouses.  
not in the field for changes, but I also think that they will work with us when they see that, hey, we listened to your comments, we're adding a max bet change, we're giving you the audit ticket you requested. So I think that they will keep feeding us data, but that it's not a showstopper right now

**Pavel Frolov** 43:41  
I.

**Val Levitan** 43:50  
Yeah.

**Juan Martinez** 43:54  
or there isn't a pressing need to get games in 30 days because it's still going to be with the same guys that we're already doing business with the two largest ones. So that's what we just need to figure out.

**Irina Shishko** 43:55  
Things work.

**Val Levitan** 44:05  
But, Inna.  
But none of them are buying from us.

**Juan Martinez** 44:18  
Ограничивала запомнить комментарии и услуги глаз.

**Irina Shishko** 44:20  
Во сколько человек?

**Juan Martinez** 44:24  
А если оно?

**Irina Shishko** 44:27  
Там ближе.

**Val Levitan** 44:28  
140000 компьютера.  
А.  
Когда челендж этот видос сказки?  
А.  
performance levels that they're looking for. Definitely. The number one changes that will get us there are the game changers. But those game changers, from what I understand, could be implemented with minimum effort.

**Juan Martinez** 44:58  
Yes.

**Val Levitan** 45:08  
Because essentially what we're saying, we will take our Giorgi implementation.  
with an addition of some sort of a skill game like Simon Says.  
But we will make it less binding.  
Skill option or skill trigger will make the skill trigger less binding and in line with what Light and Wonders is doing, but the ad by itself.

**Juan Martinez** 45:37  
Yes.

**Val Levitan** 45:46  
And that by itself, including the changes that we discussed right now, are more or less  
I'm not going to say trivial, but...  
Easier.

**Juan Martinez** 46:01  
No, I absolutely.

**Val Levitan** 46:01  
from what I understand.  
So if we don't have to do liquid glass, these changes could probably...  
get submitted to Eclipse within.  
Let's say 2 weeks.  
But if you wait for liquid glass, that's going to be...  
I don't even know.

**Juan Martinez** 46:32  
Sure.

**Val Levitan** 46:33  
But we're definitely talking about 30, 60, maybe 90 days.  
So all this time will not be, it will not be even conceivable for us to even ask for an order.

**Pavel Frolov** 46:47  
Play.

**Juan Martinez** 46:51  
Yeah.  
No, understood.

**Val Levitan** 46:55  
So, that's the, I think, I think it's a big deal for us.

**Juan Martinez** 46:59  
Yeah.  
Three.

**Val Levitan** 47:05  
So it seems like we should be moving without liquid glass.

**Pavel Frolov** 47:14  
Mmh.

**Juan Martinez** 47:19  
Read.

**Val Levitan** 47:20  
So, so then, if this is the case...  
Then I would say that.  
You should hurry up and...  
grooming those requirements to the point where there are no more questions from Irina and Pavel.  
Releasing the requirements into work.  
Pavel should start working on creating features.

**Pavel Frolov** 47:53  
Shh.

**Val Levitan** 47:55  
linking those requirements to necessary features, and scheduling, in fact, scheduling those features into...

**Pavel Frolov** 47:58  
He.

**Val Levitan** 48:05  
The following sprint, when is your next sprint bottle?

**Irina Shishko** 48:10  
Current sprint.

**Pavel Frolov** 48:10  
Next week, Thursday.

**Val Levitan** 48:14  
OK, so it will take him to realign resources.

**Pavel Frolov** 48:17  
Oh.

**Val Levitan** 48:19  
to create a schedule until Thursday and then he can take it into work and then we complete it within that cycle.  
And hurry for the approval.  
That should be our schedule. That should be how we move forward.  
We all agree to that.

**Juan Martinez** 48:41  
Yep, that makes sense.

**Pavel Frolov** 48:42  
Yes.

**Val Levitan** 48:45  
Okay, so, okay, so that's our undertakings. That's the marching orders.  
The meeting is recorded. I'm going to place recording into the chat here for your use. Yeah.

**Pavel Frolov** 48:51  
Yeah.

**Juan Martinez** 48:59  
Perfect.

**Val Levitan** 49:01  
Okay, thank you very much, everyone.

**Pavel Frolov** 49:02  
Thank you, bye.

**Irina Shishko** 49:03  
Bye.

**Val Levitan** 49:04  
Go.

**Irina Shishko** stopped transcription