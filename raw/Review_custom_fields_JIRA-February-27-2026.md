**Review_custom_fields_JIRA-20260227_090556-Meeting Recording**

27 February 2026, 02:05pm

26m 40s

**Val Levitan** started transcription

**Dmitri Kovalchuk** 0:03  
5 custom fields 17 from this is system managed fields and also we have 25.  
This is some information.

**Aaron Bockelie** 0:19  
Right.

**Dmitri Kovalchuk** 0:20  
This feels a user.  
In the last six months.

**Aaron Bockelie** 0:30  
Oh.

**Val Levitan** 0:30  
The 25, the 25, right?

**Dmitri Kovalchuk** 0:33  
Yeah, 25.

**Val Levitan** 0:34  
The the the 25 fields have been used in the last six months.

**Dmitri Kovalchuk** 0:38  
Yes.

**Val Levitan** 0:39  
Yes, but they have been used, but I doubt that they have been used productively.

**Dmitri Kovalchuk** 0:50  
We can delete from this.  
List this fields because we will move, we will delete this field.

**Aaron Bockelie** 1:00  
Right.  
So there is.  
We're sitting.

**Val Levitan** 1:05  
So it will be 20.  
Yes.

**Dmitri Kovalchuk** 1:10  
24.

**Val Levitan** 1:12  
24 OK.

**Dmitri Kovalchuk** 1:14  
Resolves this.

**Aaron Bockelie** 1:14  
We're sitting on top of a lot of desires and wishes from previous years here. Things like approvers, for example, is something that Lana uses in her workflow or.  
Um.  
I think that we need to check to see.

**Dmitri Kovalchuk** 1:35  
Yeah, let's check.  
Mm.  
I I have a problem with this field. I don't know why it's not show me.  
Correct.  
Information another.

**Val Levitan** 1:59  
Maybe the maybe the spelling?

**Dmitri Kovalchuk** 2:03  
And.  
I.

**Val Levitan** 2:04  
Is it plural approvers?

**Dmitri Kovalchuk** 2:07  
Yeah, let me check.  
Rules.

**Aaron Bockelie** 2:22  
Approvers.

**Val Levitan** 2:22  
No approvals, approvals, yeah.

**Dmitri Kovalchuk** 2:25  
Yeah, yeah, it's it's my.

**Aaron Bockelie** 2:32  
I don't think that's the right one. Approvers.  
No, that's still spelled wrong. Approvers the second one.  
So see how its date last used was February 26th, 2023 as well.

**Val Levitan** 2:46  
2nd.

**Aaron Bockelie** 2:53  
I don't. I don't think we need to be in the query field. We can just look at fields view.

**Dmitri Kovalchuk** 3:00  
OK.

**Aaron Bockelie** 3:03  
Just go to the last browser tab and let's just look there.  
Just look at at the last browser tab, please. Don't. We don't need to even search on stuff. Just yeah, let's just look there for a minute.

**Dmitri Kovalchuk** 3:21  
This.

**Aaron Bockelie** 3:24  
So we can see that it's custom field.  
3.

**Dmitri Kovalchuk** 3:30  
I understand.

**Aaron Bockelie** 3:32  
This field was created by JIRA and basically what we're having to fight now we have to fight that some of these custom fields are created by JIRA themselves out-of-the-box. When you start a JIRA instance, these custom fields unroll themselves.

**Dmitri Kovalchuk** 3:47  
Yeah, when we select some template, create some fields for this template.

**Aaron Bockelie** 3:53  
Right. And so we can continue to trim things down, but this is kind of like going into an electrical cabinet and flipping wires that you think aren't probably used. It's not the right way to do this.  
We need to have a design or a plan for what we want to do and then adjust the electrical box to fit that.  
So what I want us to talk about here, I go back to your report inside of V code is you have a list of fields and what they were used for, right?  
So we need to come up with a bit of a refresh on the intentions of what we want JIRA to look like. Let's just say that the long-term plan is to not have JIRA at all two years from now.  
What is JIRA going to look like a year from now? What is JIRA going to look like 6 months from now?  
Because if we think that we're going to pick two years, let's I'm going to just use two years in 2028.  
March 1st, 2028, JVL will not be on JIRA anymore. Let's just say that for a minute. We're not actually doing it, but let's use a starting point. This means that we need to slowly wind down the use of JIRA by the time we get to that point and we can use a progression.  
Of slowly weaning people from the capabilities of Europe right now.  
It doesn't mean we need to throw it all away either, but what we should be asking ourselves is what are the essential parts of JIRA that we actually want to keep at this point. So for instance, I see cabinet type, progressive family.  
Reporter information reviewed by producer and so forth, right? Some of these are like reviewed by director and reviewed by producer are are informational fields that direct a workflow, right?

**Dmitri Kovalchuk** 5:55  
It's your field, I said.

**Aaron Bockelie** 6:01  
The question is, is, is that workflow still used? Does Lena and Michael still use that process?  
If yes, then we need to define that process just roughly saying these fields are used here.

**Val Levitan** 6:16  
All we need to do is a stage reviewed by whom it was reviewed. That's not important because our company is not huge. We don't have multiple departments. So it was reviewed. Great, move on.

**Aaron Bockelie** 6:26  
Right.  
So the the question is, is are they are they using that workflow casually? Do they ask for the big official thing and are using it informally? That's a common pattern that people do is they ask for some important big thing.  
And then they don't really use it and we need to see if that is still the case.  
Um, we have a lot of.

**Val Levitan** 6:56  
We have, we have, we have decision making here. We have a power of decision making and even if they use something, the other question should be asked what is the?  
I don't know how to call it use factor.  
From from that feature, I mean, how much does it give us? What does it bring? How much money does it put in our pockets?

**Aaron Bockelie** 7:24  
Right.

**Val Levitan** 7:25  
Sometimes, as you always say, less is more.

**Aaron Bockelie** 7:30  
So do we see how they're oh.

**Val Levitan** 7:30  
I'd rather.  
Yeah, I'd rather consume 20% of the features, but 80% of the time.

**Aaron Bockelie** 7:38  
Right.  
So I see like these game mechanic framework and sector and things. We set those up to be able to allow the pipeline for determining what requirements were applied to what jurisdictions and all this other stuff.  
But my real question is, is that we actually actually use it or is it just sitting there never configured for the majority of the requirements that we set up?

**Val Levitan** 8:05  
Well, we're actually using it inside of the requirements, but we don't generate any reports from it.

**Aaron Bockelie** 8:14  
Right.

**Val Levitan** 8:16  
So yeah, there is an extra load on those who writes a requirement to think about where it might go, but in actuality it's not a useful feature because even if we put it in the requirements, it doesn't find its way anywhere in the web past the requirement.  
And and I actually the way the requirements is used is not used to the fullest degree. So I'd rather focus on using the requirement to the fullest degree rather than having more features in the requirements that are not used.

**Aaron Bockelie** 8:50  
Yeah. So that turns it into, yeah.

**Val Levitan** 8:52  
So there might be a sorry for it, for I keep on jumping in, but there might be initial questions. Well, we had it. We spend all this energy on it. It's there. How come we don't have it anymore?

**Aaron Bockelie** 8:55  
It's fine.

**Val Levitan** 9:09  
And you know, I could brush it off and say, you know what, we have so many things that we're not using. Here's another few things that we're not going to be using.  
And sometimes, you know, I like your analogy. It's like going into electrical box and start clipping wires. You know what? Normally it's probably the wrong thing if you do a surgery on a human, but if you want to isolate what works, what doesn't work.  
Maybe shutting down the power to a block somewhere is not a bad thing. See if we survive.  
And these requirements will remain there for the next 60 days. So if we cannot live without it, we could always bring it back.

**Aaron Bockelie** 9:56  
Yeah.  
So I guess the the thing that we want to make sure that we're doing is.  
Are we going to deactivate or delete these fields in a way that doesn't break the existing workflow or searching for things? So I know that there's some filters that are feeding up the dashboards.  
That use these fields, right?

**Val Levitan** 10:24  
There are there are three dashboards being used right now. I took a survey on it.

**Aaron Bockelie** 10:32  
So then what we might want to do then is look at those dashboards.  
See what the because what what we want to ultimately do Dmitri is we want to we want to configure based on intentions and use, not some technical focus on it. So if we say.  
Look at those dashboards and we look at what filters are attached to them. Then we know exactly what queries we're going to use. Then everything else that's not in those queries is subject for deletion.  
As an example.  
We need to make essentially A deletion matrix of what we're going to delete and what we're going to keep.  
Because in this custom fields list I see the fields, but I don't see what's marked for deletion.

**Val Levitan** 11:25  
Come back, can I suggest what to delete here and tell tell me if you cannot live with it with with my views here. Let me just tell you what I want to delete.  
Would that work for you, Aaron?

**Aaron Bockelie** 11:39  
Yeah, I'm kind of leaning on Dimitri to drive this. I don't want to be the decider. I'm the advisor here.

**Dmitri Kovalchuk** 11:46  
I think we use well delete all fields that we think we need. We don't need. These fields contain some information.

**Val Levitan** 11:57  
Let me let let me go through this. Let bring bring this into. Can you export it into Excel?  
I will get much more out of a smooth, smoothly working MCP rather than multiple fields. OK, share, share, share the same thing in Excel please.

**Dmitri Kovalchuk** 13:09  
I sent a file in chat, but.

**Val Levitan** 13:12  
You did. Please open the Excel now.

**Aaron Bockelie** 13:17  
But.

**Val Levitan** 13:23  
Thank you, Sir.

**Dmitri Kovalchuk** 13:33  
I think we can delete this.

**Val Levitan** 13:36  
I I I don't see it. Can you can you put the whole screen like you need to widen the columns?

**Dmitri Kovalchuk** 13:43  
Uh, OK.

**Val Levitan** 13:46  
Yes, yes, yes.  
OK, so yeah, great.  
Remove #4.  
No, no, sorry. Uh, OK, so remove #2.

**Dmitri Kovalchuk** 14:24  
And we'll show this like this.

**Val Levitan** 14:30  
I can't read it.  
I can't. I can't read the the the red background.

**Dmitri Kovalchuk** 14:37  
Oh, sorry.

**Val Levitan** 14:42  
Yes, you should just strike, strike out, strike it out. OK, works. That's fine. That's fine.  
Uh #4.  
#9.  
Hold on, hold on, hold on, hold on.  
OK, so you see 11.  
And eight is almost the same.  
So I prefer to use the legislative framework.

**Dmitri Kovalchuk** 15:44  
OK, and we can mark this.

**Val Levitan** 15:46  
Yeah, you can, yeah.  
Uh, move down a little bit.  
Um.  
13.  
Move down, please.  
Move down more, please.  
13 and 14 are the same, so remove both.  
Sorry, sorry. Hold on. There was something about progressive above there. Can you move up?

**Dmitri Kovalchuk** 16:51  
Progressive mechanic and.

**Val Levitan** 17:03  
Don't need it. Could now. Could never really use progress. Yeah, remove 14.

**Dmitri Kovalchuk** 17:16  
We use reporter information fields in our.  
And Jura Service Management.

**Val Levitan** 17:26  
OK.

**Dmitri Kovalchuk** 17:30  
And this one too, yeah.

**Val Levitan** 17:30  
And #17.  
Yeah, #17 please.

**Dmitri Kovalchuk** 17:38  
Uh.

**Val Levitan** 17:39  
17.

**Dmitri Kovalchuk** 17:42  
This.

**Val Levitan** 17:43  
Yes.  
#18  
#19  
#21  
Move down please.  
November 23.

**Dmitri Kovalchuk** 18:25  
This field create by me for count how much OK.

**Val Levitan** 18:25  
Tony.  
Yes, yes, yes, yes, yes, yes. I know, I know. Don't need it.

**Dmitri Kovalchuk** 18:35  
OK.

**Val Levitan** 18:35  
24 and 25.

**Dmitri Kovalchuk** 18:38  
No.  
I think this is not our field. This is not Jira service desk field I think.  
16.

**Val Levitan** 19:03  
Maybe.  
Maybe I I don't know what requirement type is.

**Aaron Bockelie** 19:10  
It's just part of the requirement system, requirement fields.

**Val Levitan** 19:17  
Meaning which requirement? Is it legislative or?

**Aaron Bockelie** 19:22  
Yeah, let's see how it says cascading list.

**Val Levitan** 19:26  
Yeah.  
OK, so I would leave everything in black right now and remove everything in red.

**Dmitri Kovalchuk** 19:37  
Right now or I can do it later.

**Val Levitan** 19:40  
No, no, of course. Later, of course.

**Aaron Bockelie** 19:40  
I think.  
Yeah, you need to also, before you delete this, verify that what you're doing here isn't going to adversely affect things.

**Dmitri Kovalchuk** 19:42  
OK.

**Aaron Bockelie** 19:51  
So requirements categorization label may be problematic. Be very careful about what you're deleting.

**Val Levitan** 19:59  
Which? Which one? Which one? What number?

**Aaron Bockelie** 20:01  
I can't see it. It's scrolled the wrong way. Scroll up.

20:07  
Up.

**Aaron Bockelie** 20:09  
You just had it, but.  
Go down. I don't see it yet.  
Called Requirements Categorization Label.  
Wherever it's at, I didn't catch, but was on.

**Dmitri Kovalchuk** 20:25  
This one.

**Aaron Bockelie** 20:26  
Yeah.

**Val Levitan** 20:31  
OK, so let's return it.

**Aaron Bockelie** 20:34  
And you may want to look at the requirements checklist too. Here's the clue. The clue is what's the on column H You see how it has a date of last used.

**Val Levitan** 20:50  
Yes.

**Aaron Bockelie** 20:52  
So Dmitriy, you need to see this. The last use column is going to be your clue as to whether this is actively used or not.  
So if you see 15 and 16, those are last used last year, right? Very rarely and frequently.

**Dmitri Kovalchuk** 21:09  
16 views but I I don't know why it show.

**Aaron Bockelie** 21:18  
15 and 16, right?

**Dmitri Kovalchuk** 21:22  
I don't know about 16.

**Aaron Bockelie** 21:23  
No, I'm looking at the Excel column number, not the not the fields. It's not on column B.

**Dmitri Kovalchuk** 21:29  
Ah, this one, this.

**Aaron Bockelie** 21:31  
And 15 you see the dates old.

**Dmitri Kovalchuk** 21:36  
Yeah.

**Aaron Bockelie** 21:37  
So that's a higher likely this is there's no cut off, there's no yes or no in this list right now. This is just intentions. This is the way it's always been done with large migrations or Jira work is that you kind of start with the theory of operation, which is what we've done here.  
Now you need to go check to verify that it's really not going to break stuff when you clean it up.  
Uh.  
O for the ones that you want to delete. Now you need to go query them and see what issues have these fields populated.

**Val Levitan** 22:06  
Can you?  
Can you remove in column I 17 and 18 the yes, yes.

**Dmitri Kovalchuk** 22:24  
Which one this is?

**Val Levitan** 22:26  
71718 Can you remove the? Yes, Yes. Yeah. Thank you.

**Dmitri Kovalchuk** 22:28  
Uh, OK, OK, yeah.  
Yeah.

**Val Levitan** 22:45  
I'm I'm pretty happy with this list.  
Can you please generate a final list of what custom fields we're keeping?

**Dmitri Kovalchuk** 23:01  
Before I did, before I don't delete.

**Val Levitan** 23:03  
And circulate that and.

**Dmitri Kovalchuk** 23:08  
Yeah.

**Val Levitan** 23:10  
You will delete everything on Monday. I'm not. I'm not looking out. I don't need everything right now. I just need the final list.

**Aaron Bockelie** 23:20  
And you can also practice this deletion on the sandbox instance to make sure it all works correctly first.

**Val Levitan** 23:28  
You know what I need you to do? Just just just go into. Hold on, I need to achieve something. This meeting in this excel, delete the columns that are red.

**Dmitri Kovalchuk** 23:29  
Certain.  
Hm.

**Val Levitan** 23:43  
Can you do it now and then save this XLS final custom fields?  
What are you doing?

**Dmitri Kovalchuk** 24:00  
I can delete it.

**Val Levitan** 24:02  
Oh, OK, good.  
Yes, fantastic.  
Yes.  
OK, so that's that's fantastic. That's that's what I need.  
OK, please save it as final custom fields.

**Dmitri Kovalchuk** 25:39  
Later I will create a normal file for this.

**Val Levitan** 25:44  
OK, can you please place it into chat?

**Dmitri Kovalchuk** 25:52  
Is this file or normal?

**Val Levitan** 25:54  
This file, please place it into chat. We we don't know how to manipulate Excel.

**Dmitri Kovalchuk** 25:56  
OK.

**Val Levitan** 26:06  
How many fields is that? What's the count? 13.

**Dmitri Kovalchuk** 26:09  
Uh, certain.

**Val Levitan** 26:12  
So Aaron, you your MCP need to address these 13 fields.

**Aaron Bockelie** 26:16  
Sure.

**Val Levitan** 26:19  
OK. Damon, thank you very much. We're done for today.

**Aaron Bockelie** 26:20  
OK.

**Dmitri Kovalchuk** 26:24  
OK. Thank you.

**Val Levitan** 26:24  
Can you can you please then on Monday when you come to work, continue with this?

**Dmitri Kovalchuk** 26:31  
OK.

**Val Levitan** 26:33  
Aaron, let's log in into the next meeting.

**Aaron Bockelie** 26:36  
OK.

**Dmitri Kovalchuk** stopped transcription