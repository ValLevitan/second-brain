# Raw Transcript — MRP and Sales Watch Demo
**Date:** July 14, 2026, 1:03 PM Eastern (1 h 4 m 57 s)
**Summary note:** [[Meeting_Notes_MRP_and_Sales_Watch_Demo-July-14-2026]]
---
**MRP and Sales Watch Demo-20260714\_090334-Meeting Recording**

July 14, 2026, 1:03PM

1h 4m 57s

**  
Val Levitan** started transcription

**  
Nathan Carver** 0:24  
Okay, hear me okay?

**  
Val Levitan** 0:27  
Was he okay?

**  
Nathan Carver** 0:30  
Alright.

**  
Val Levitan** 0:31  
What browser did you switch to?

**  
Nathan Carver** 0:33  
I switched to Edge for Linux.  
Let's try this.

**  
Val Levitan** 0:41  
You wanna be on edge?  
this morning.  
Oh yes, great.

**  
Nathan Carver** 0:50  
All right, you see Claude.

**  
Val Levitan** 0:52  
I see, Claude, yes, Mr. Claude.

**  
Lev Rudky** 0:53  
You.

**  
Nathan Carver** 0:53  
Okay, good.  
All right, so Edge is...  
Firefox, for some reason, has an issue.

**  
Val Levitan** 1:00  
Okay.

**  
Mikhail Perelman** 1:01  
Much.

**  
Nathan Carver** 1:06  
Okay, so let's dive in here. So I got the feedback Lev that you sent me and I made a short list of.  
A short list of changes I'll make to align with that. There's just a few things like adding line numbers, the units of measure.  
The unit cost, and then...  
The top-level part number.  
On.  
So I'll get on that. I don't think that's too much work. It shouldn't be done. It should be done pretty quickly. But we'll dive into what we have here. So what I've done is...  
I've added a lot of coding support to run calculations, so the agent is doing less work. It's more or less just orchestrating.  
We'll do just quickly do this one, since this will be a short.  
See.  
What's the invoice times?  
Ohh, and...  
So we're getting much better response now because a lot of the...  
Ideally, the agent's doing no calculations at all, unless there's an edge case the user asks for.  
O.  
From what I can verify myself so far, the accuracy seems to be precise. I think we're getting all the right totals. If anything is off, it's going to most likely be  
Making sure that the tool is using MSB configurations correctly.  
So, we're able to quickly run sales numbers.

**  
Mikhail Perelman** 3:22  
But.

**  
Nathan Carver** 3:25  
We can ask it to compare.

**  
Val Levitan** 3:31  
Yeah.

**  
Nathan Carver** 3:35  
Compared with the previous.

**  
Val Levitan** 3:36  
Yeah.

**  
Nathan Carver** 4:01  
Of course, it's giving us some options. We can also go back further.  
So that's it. So for the sales watch Val, I think using it the way you need it and then making sure that it's.  
performing as expected or as needed and able to replace whatever your current mechanism is.  
Let's see here.  
Okay, and then I want to dive into.  
Planning, I just got some.  
Statements here and students.  
Now we can dive into the items and vendors and the purchase orders.  
So, we'll ask it to do something that it's...  
It may or may not be able to do depending on how MSBC is set up. So the nice thing is, as you're asking these questions, it'll...  
It'll inform you of its limitations or limitations based on data.  
So that we can use this as a mechanism to clean up or our, I guess, refine what we keep in MSBC for better results.

**  
Val Levitan** 5:55  
Let's focus on...  
MRP, Manufacturer Requirement Planning.

**  
Nathan Carver** 6:02  
Okay.

**  
Val Levitan** 6:03  
Sales, you know, I can I can review it with you later.

**  
Nathan Carver** 6:08  
Okay, sounds good.  
It's still going.

**  
Val Levitan** 6:40  
Yeah.

**  
Nathan Carver** 7:03  
I'll break this and go into MRP. I'm going to pull an example here.  
Okay, let's go into what we did before.  
I'm gonna copy this part number.  
Um, let's see, so...  
Let's see, we can just do this command.  
So you can just type text order 500 of this part, or you can use these commands. The agent will use the commands behind the scenes.  
Even if you don't use them, it'll infer what you mean.  
but these forward slash commands will be more precise.

**  
Val Levitan** 8:26  
I'm not sure it hit home with Michael and Lev. Can you allow them to ask questions?

**  
Nathan Carver** 8:34  
Yes, absolutely.

**  
Lev Rudky** 8:34  
Yeah.  
Yeah.  
Can you?  
Can you pull data just from one journal, MRP dash flex?

**  
Nathan Carver** 8:49  
Yes.  
So.  
What was the journal?

**  
Lev Rudky** 9:02  
MRP Flex.

**  
Val Levitan** 9:06  
P.P. as in P. as in Paul.

**  
Lev Rudky** 9:06  
Spence.

**  
Nathan Carver** 9:10  
Oh, MRP just flex.

**  
Lev Rudky** 9:13  
Excel.

**  
Nathan Carver** 9:16  
Okay.  
Yeah.

**  
Val Levitan** 10:53  
Should change the language on stale PO.

**  
Nathan Carver** 10:59  
Okay, where's...

**  
Val Levitan** 11:00  
Well, false is not descriptive, the last column.

**  
Nathan Carver** 11:03  
Oh, got it.  
Okay.  
This should be a yes or no.  
Indicator.

**  
Val Levitan** 11:14  
Oh, I don't know how Lev wants it, but it should be in his language.

**  
Nathan Carver** 11:19  
Okay.

**  
Lev Rudky** 11:20  
Haze.  
War.  
Suck.

**  
Val Levitan** 11:25  
What does tail? What does tail PO mean? I I don't understand the definition of it.

**  
Lev Rudky** 11:28  
And.  
It's like aged that were created a long time ago.  
Potentially redundant.

**  
Val Levitan** 11:45  
Okay, so what, what, how do you want to express it? Yes or no? Or do you want a different language? Like more than, more than number of days?

**  
Lev Rudky** 11:56  
Michael, do we need it at all?

**  
Mikhail Perelman** 11:59  
You're talking about stay still.

**  
Val Levitan** 12:00  
I need it. I want to see it.

**  
Mikhail Perelman** 12:04  
Stale Pure.

**  
Lev Rudky** 12:04  
You do OK.  
Okay, so...

**  
Val Levitan** 12:07  
Stale PO, yes. How do you want to describe it? More than the number of days?

**  
Lev Rudky** 12:14  
Yeah.  
Oh, oh, let's say over 180 days or something like that.

**  
Mikhail Perelman** 12:29  
No.

**  
Lev Rudky** 12:31  
No.

**  
Mikhail Perelman** 12:32  
No.  
So, so maximum that we have is a four-month delivery, so 120 days.

**  
Val Levitan** 12:44  
Okay, no, but that's not like 120, 120 days could be a, there could be a reason for it. But 180 days, that's already a stale deal.

**  
Mikhail Perelman** 12:44  
120 days.  
Well...

**  
Val Levitan** 13:05  
Okay, let's just say yes or no. That's good.

**  
Mikhail Perelman** 13:07  
Could be, yes, some could be could be other versions as well, for example, if we place several orders split in time for several months.

**  
Nathan Carver** 13:14  
Rudky.

**  
Val Levitan** 13:19  
That's a good point.

**  
Mikhail Perelman** 13:20  
Yeah, so we have...  
Would do it will be indicated with still pure.

**  
Val Levitan** 13:28  
But again, we don't want such POs, right? We want POs that are current.

**  
Lev Rudky** 13:29  
It's.

**  
Val Levitan** 13:34  
So we want to see it, but we want to see over 180 days. So the rule is over 180 days, stay LPO, yes.

**  
Mikhail Perelman** 13:36  
Yeah.  
Okay.

**  
Nathan Carver** 13:48  
All right, that sounds good.

**  
Mikhail Perelman** 13:49  
Not gonna hurt.

**  
Nathan Carver** 13:54  
Okay.  
From this point, Lev and Mikhail, how would you like to, anything you want to start diving into?

**  
Lev Rudky** 14:04  
Can you go up?

**  
Nathan Carver** 14:05  
Yeah.

**  
Lev Rudky** 14:07  
Stop here.  
OK, you will have to incorporate the columns that that I mailed you and the.

**  
Nathan Carver** 14:21  
Correct.

**  
Lev Rudky** 14:23  
So, basically...

**  
Mikhail Perelman** 14:27  
OK.

**  
Lev Rudky** 14:28  
The main point there is that...  
This output.  
Is.  
will be for some time working process because the quantities will have to be reviewed and adjusted.

**  
Mikhail Perelman** 14:47  
Yeah.

**  
Lev Rudky** 14:52  
And the review?  
Ha.  
The real output will be, let's say, in the range of, let's say, 400 lines, so...  
To review it.  
will take some time and to adjust quantities will take some time. So we will need an option.  
to save work in process.

**  
Nathan Carver** 15:27  
Okay.

**  
Lev Rudky** 15:29  
K.  
No.  
That, that's the main point.

**  
Nathan Carver** 15:36  
Okay, so this will take, you'll take time to build this, so you need a way to save.

**  
Lev Rudky** 15:36  
Yeah, I know.

**  
Nathan Carver** 15:44  
Save your progress so when you come back.

**  
Lev Rudky** 15:48  
Yeah.

**  
Nathan Carver** 15:48  
You can continue with that. With that, is it you're working on a purchase order or you're working on an item?  
Or could it, could it be both? Like, what is that?

**  
Lev Rudky** 15:59  
He.  
Peari.  
Yeah.

**  
Nathan Carver** 16:04  
Okay.

**  
Lev Rudky** 16:04  
It, it could, yeah.

**  
Nathan Carver** 16:07  
It could be both, okay.

**  
Lev Rudky** 16:08  
Mhm.

**  
Mikhail Perelman** 16:09  
Nathan.

**  
Nathan Carver** 16:11  
Yes.

**  
Mikhail Perelman** 16:12  
There is column on order and column order quantity.  
On order, what does it mean?

**  
Nathan Carver** 16:22  
So this would be if it's on a purchase order.

**  
Mikhail Perelman** 16:27  
Let's see, that's just order number or what?

**  
Nathan Carver** 16:27  
Um...  
Yeah, we need to, let me.  
So, the order quantity.

**  
Mikhail Perelman** 16:37  
What the quantity? OK, it's clear, clear.

**  
Nathan Carver** 16:39  
is matching our shortage. I'm not, I need to look, let me look into this.  
Oh, if there's, I think what it's, I need to, I'm gonna, I need to go verify this, but I think what it's doing is it's taking your.  
So you have a net shortage of 64. If you already had, let's say, 30 on order, your order quantity would only be the difference of what's on order and what the shortage. So it would be 34. So if this was an on order already of 30, then you would say 34.

**  
Mikhail Perelman** 17:12  
Okay.  
Okay, so...  
On order, it's a...  
Like, suggestion, what is it?  
What is our shortage? Let's say that is that what you mean on order?

**  
Nathan Carver** 17:45  
Okay.

**  
Mikhail Perelman** 17:46  
Because we have, we have a column net shortage. OK, it's clear.

**  
Nathan Carver** 17:51  
Mhm.

**  
Mikhail Perelman** 17:52  
Now, what is on order?

**  
Nathan Carver** 17:56  
Okay, so this needs better definition. So what do you what do you want to see like these are?  
columns that we use based on MSPC, but we can.

**  
Mikhail Perelman** 18:06  
Ohh.

**  
Nathan Carver** 18:11  
rename them and give them better, more meaning to how you use them.

**  
Val Levitan** 18:16  
No, but hold one second. Hold on a second.  
I don't want to rename columns here. If we rename columns, they have to be the same in MSBC and here.  
So this simply reads the column.

**  
Nathan Carver** 18:41  
Let me see.

**  
Val Levitan** 18:41  
In other words, I do not want the names to be different.

**  
Nathan Carver** 19:05  
Let's make sure we know where.  
Okay.  
Yeah, so that's what it's pulling, so on order in this in this table.  
is the sum of all outstanding quantities across open purchase orders.  
And then the quantity would be what it's recommending.  
That you still need to buy to to.  
cover any shortages.

**  
Mikhail Perelman** 20:03  
Okay, so order quantity, it's a general recommendation.

**  
Nathan Carver** 20:11  
Correct. So this is the, yeah, this is, so it's deriving this in the calculation.

**  
Mikhail Perelman** 20:19  
Val.  
Demand minus stock.  
Minus.  
Okay.  
Okay.  
So, and I understand.  
You might minus self minor that or no of the figure. Okay.  
So in case that we do have something on order, but it's not enough to cover demand. That is what they recommend to buy.  
Exit.  
I see.

**  
Lev Rudky** 21:00  
Hmm.

**  
Nathan Carver** 21:03  
So those two column names, they don't come directly from MSPC. They're just.  
On order is just the open purchase orders that is.  
Concept in MSPC open the order quantity is what we're.  
deriving. So we can renaming this here wouldn't conflict with anything in MSPC. And then we can obviously name that a little bit. But if these are fine, then we can leave them as is.

**  
Lev Rudky** 21:38  
No.  
No.

**  
Mikhail Perelman** 21:44  
Okay.

**  
Lev Rudky** 21:44  
Do you know, do you know which field it pulls for?  
Quantity on order.

**  
Nathan Carver** 21:56  
Yes, it should be looking at the line items. Let's verify it's going to look at the line items for on.

**  
Lev Rudky** 21:56  
Yeah.

**  
Nathan Carver** 22:03  
Open Purchase Orders.

**  
Lev Rudky** 22:41  
Yeah, this looks fine.  
Yeah.  
So, it takes into account.  
Whatever was already received from a specific line.  
Can you?  
Can you show?  
What it pulled?  
From the journal.  
From the what?  
Requirements from the journal, whatever I entered there, because the list of shortages.  
Looks to me.  
A little bit too short.

**  
Nathan Carver** 23:45  
Okay.  
In general.

**  
Lev Rudky** 26:02  
I think there is some.  
Inconsistency there.

**  
Nathan Carver** 26:09  
Okay.

**  
Val Levitan** 26:18  
Is there a mathematical inconsistency or what is it?

**  
Lev Rudky** 26:22  
It's no, the input inconsistency file.

**  
Val Levitan** 26:22  
But.

**  
Lev Rudky** 26:31  
Let me.  
Let me cheque the journal, maybe something is changed a second.  
Yeah.  
Yes.  
K.  
Cody.  
I am.  
Nathan, are you in live environment or in test environment in the?

**  
Nathan Carver** 27:23  
Yeah.  
This is in live right now.

**  
Lev Rudky** 27:38  
OK, I'm sending you one of the lines that I have. I put in the chat. One of the lines in the input journal.  
And, uh...  
Can you?  
Try to receive this value.

**  
Nathan Carver** 28:00  
Okay, got it.

**  
Lev Rudky** 28:00  
In the club.

**  
Nathan Carver** 28:02  
So, you mean to pull the journal for that for that item?

**  
Lev Rudky** 28:05  
Yeah.  
Mm.  
I'd say.  
This list.  
Appears to be too short.  
Mhm.  
So, it's 5 items.  
Because...  
Theoretically, it's possible, but...  
I need to dig deeper.  
Sweet.  
Okay, once.  
OK, once you are dressed.  
This issue for Poland.  
All lines, regardless of shortages, it will it will be more visible than I.

**  
Nathan Carver** 30:10  
Mhm.

**  
Lev Rudky** 30:16  
everything. Right now, I just can tell that it looks to me the list of shortages looks to me to short. Let's say, just a second, can we do some output? I'll put a higher number in the journal. Let's see what maybe then the list will be longer.

**  
Nathan Carver** 30:28  
Mhm.  
What is it that you're looking for more?

**  
Lev Rudky** 30:42  
I look for more shortages. I'm looking for more shortages. I put 500.

**  
Nathan Carver** 30:46  
Okay.  
Okay.

**  
Lev Rudky** 30:51  
OK, I did now try to pull it.  
Yeah.  
Is it calculating now?

**  
Nathan Carver** 31:51  
No, what is it that you need me to? Sorry.

**  
Lev Rudky** 31:52  
Thank you.  
I changed the quantities in the input table, right? So I put some, yeah, so I expect a much longer list.

**  
Nathan Carver** 31:59  
Oh, okay, good. I will let it know.  
The quantities.  
Okay, says nothing's changed. Let me...

**  
Mikhail Perelman** 33:50  
7am.

**  
Lev Rudky** 33:50  
Mmh.  
Yeah, so basically, does it show here anyway? What kind of...  
What can it show what was the input for this output?

**  
Nathan Carver** 34:08  
And...  
Yeah, it's saying it doesn't see any change. Does this look correct? The location.

**  
Lev Rudky** 34:26  
Location, let me confirm it.  
Yeah.  
Asian.

**  
Nathan Carver** 35:26  
Yeah.  
Okay.

**  
Lev Rudky** 36:30  
I need.  
How many units it received for this part number, CM08?

**  
Nathan Carver** 36:49  
Yeah.

**  
Lev Rudky** 36:50  
How many units for this build?

**  
Nathan Carver** 37:02  
Yeah.

**  
Lev Rudky** 37:30  
Please.  
Yes.  
It doesn't show, does it?

**  
Nathan Carver** 37:47  
No, what is it? So it says it has 10 units.  
There's Kern on hand.  
So the build quantity is 10 units. You have a current on hand of finished assembly of 21 units.

**  
Lev Rudky** 38:08  
Journal bill quantity 10 units. I put, I put, I put.

**  
Mikhail Perelman** 38:15  
Yeah, sorry, guys. Journal built quantity 10 units.  
current on hand of the finished assembly.  
How it shows a finished assembly?

**  
Lev Rudky** 38:30  
Let's put it aside for a moment because she's selling something. No, but I put on the line there 500 units, right? Not so, maybe I should, I will refresh it.

**  
Mikhail Perelman** 38:35  
Yeah, OK.

**  
Nathan Carver** 38:51  
Oh, you updated that item.

**  
Lev Rudky** 38:53  
Yeah, I updated this line item and I changed the demand for 500 units. So this will definitely produce lots of shortages. So  
I would like...  
To see.  
Those shorties.  
So, I refreshed the thing there, maybe now it...  
Ohh.  
Yeah, can can you run it again?

**  
Nathan Carver** 39:39  
Yes.  
You got.  
Sorry, looking.  
Okay, now it sees the 500.

**  
Lev Rudky** 41:32  
Okay, now can you produce a list of shortages?  
Oh, this looks much better.

**  
Mikhail Perelman** 42:08  
Okay.  
Do we produce the list of shortages only, or the whole list of parts that required for this product?

**  
Lev Rudky** 42:10  
Nobody.

**  
Mikhail Perelman** 42:19  
Because I need the whole list.

**  
Lev Rudky** 42:21  
Yeah, I, I sent, I sent the, I sent this requirements just not implemented yet.

**  
Nathan Carver** 42:28  
So you want the full list?

**  
Mikhail Perelman** 42:30  
Full list, yeah.

**  
Lev Rudky** 42:31  
He.  
Just a second, go back. Okay, let's finish.  
The.

**  
Nathan Carver** 43:02  
Actually, let me make sure.

**  
Lev Rudky** 43:13  
So, you asked it to write into a CSV file, right?

**  
Nathan Carver** 43:18  
Correct.

**  
Mikhail Perelman** 43:36  
Ohh.

**  
Nathan Carver** 43:37  
Let's see here, this is too small.  
Sam, Sam, Sam.  
Why is it on this?  
Actually, there we go.  
So that's 100 and.  
179 parts.

**  
Lev Rudky** 44:20  
Yeah, it's on the boat.  
You go tonight.  
So, the right order, I don't know exactly how many are there.  
So, just a second, let me cheque all things there. Okay, so...  
On hand, on our day, yeah.  
Yay.  
King.  
Can you?  
OK.  
Can you go back to this CSV file?

**  
Mikhail Perelman** 44:55  
Go on.

**  
Nathan Carver** 45:00  
Yeah.

**  
Lev Rudky** 45:01  
Okay, put the philtre on top there.

**  
Mikhail Perelman** 45:01  
K.

**  
Nathan Carver** 45:09  
Um...  
Hold on.

**  
Lev Rudky** 45:13  
It's data, menu item data.

**  
Nathan Carver** 45:18  
There we go. Thank you.

**  
Lev Rudky** 45:21  
And now philtre stuff that starts part now that begins with L.

**  
Nathan Carver** 45:30  
With L.

**  
Lev Rudky** 45:31  
Yeah.

**  
Nathan Carver** 45:39  
And.

**  
Lev Rudky** 45:39  
It's OK.  
Yeah.

**  
Nathan Carver** 45:44  
What is the command for starts with?

**  
Lev Rudky** 45:47  
It's, I don't see the menu items there, but it should be custom philtres and begins with hell.

**  
Nathan Carver** 45:58  
And.

**  
Lev Rudky** 45:59  
Maybe it's different from Oxford CSV. OK, but OK, that doesn't matter. Close this field for me.

**  
Nathan Carver** 46:02  
Yeah, it's going to be a little different.  
We can sort by, we can sort by L though.

**  
Lev Rudky** 46:11  
Okay.  
So it's not so here.  
Top.  
On the four labels.  
Michael, does it look reasonable to only four?  
Payables on the base unit.

**  
Mikhail Perelman** 46:39  
OK, so there is some questions, but yeah, it's OK out of this.

**  
Lev Rudky** 46:41  
What?  
It's reasonable, yeah.

**  
Mikhail Perelman** 46:48  
Out of these labels, we have to know this, but...  
I fifty-one 20, we don't buy at all.  
515508 at the end, we don't buy at all. And line 140, we don't buy at all.

**  
Lev Rudky** 47:13  
Okay, this is not an issue for Nathan, right? It's an issue, we have to remove it from bill of materials, right?

**  
Mikhail Perelman** 47:15  
Okay.  
And I'm just saying, whoops.  
What are you looking for?

**  
Lev Rudky** 47:27  
No, I, I just, I just knew that we don't have.

**  
Mikhail Perelman** 47:32  
OK, now.  
Nathan.

**  
Nathan Carver** 47:37  
Mm-hmm.

**  
Mikhail Perelman** 47:39  
Can you go on to the top top row?  
Okay, so...  
What do we need some some changes?  
For example, on order.  
On order, and the next column is...

**  
Lev Rudky** 48:06  
I sent an e-mail. Michael, listen.

**  
Mikhail Perelman** 48:07  
Demand.  
Okay, you change it.

**  
Lev Rudky** 48:12  
First, read the e-mail that I sent this morning, right? I asked to, I asked, I asked to have some columns and I specified the order of columns, right? It's there, like if you start at the beginning.

**  
Mikhail Perelman** 48:17  
No, I didn't.  
Mhm.  
Yeah, okay.  
Mmh.

**  
Lev Rudky** 48:32  
The main points are there, like bullet points.

**  
Mikhail Perelman** 48:38  
Mhm.  
Okay, so at the end, you transfer.  
This table from your tool to Excel.

**  
Lev Rudky** 48:53  
This is, in this specific case, it is a CSV file. It's similar to Excel, but it doesn't have all the features of the Excel.

**  
Nathan Carver** 48:56  
Yeah.

**  
Mikhail Perelman** 48:58  
Yeah, because...  
Okay.  
And.  
Okay, I just...  
That type of file, I'm okay with that.  
We need to add several columns.  
Is that file?  
Like...  
Your number.

**  
Lev Rudky** 49:31  
This is the PO part and payment part will be kind of phase two. We get this piece stabilised because this will allow you to.

**  
Mikhail Perelman** 49:37  
Mhm.  
Okay.  
Okay.  
UK.

**  
Lev Rudky** 49:47  
Operate, right? When we go to the invoice and payments and stuff, this will be next, next, next piece, but...

**  
Mikhail Perelman** 49:52  
Mm.  
Let me think.  
Yeah, Nathan, one more thing.

**  
Nathan Carver** 50:02  
Yeah.  
Yeah.

**  
Mikhail Perelman** 50:04  
How can I see on that file?  
What assemblies are used and in what quantities?

**  
Lev Rudky** 50:11  
This is top-level item; I didn't put it there yet.

**  
Mikhail Perelman** 50:16  
Okay, but...  
Yeah.

**  
Lev Rudky** 50:22  
But just let this piece run smoothly, and then like...

**  
Mikhail Perelman** 50:24  
Okay.  
Okay, okay, so we're not there yet.

**  
Nathan Carver** 50:32  
Okay.

**  
Lev Rudky** 50:32  
We're not there yet, yeah.  
But it, but...  
So far it looks fine. Now, if he is, so once you added the, I specified there, we need a  
adjusted, we need an extra column for adjusted values, right, to be put. So this is when Michael starts working on this file.

**  
Mikhail Perelman** 51:04  
Ohh.  
Okay.

**  
Lev Rudky** 51:11  
This is from me? Where does it come from? Okay, the question is, whatever...

**  
Mikhail Perelman** 51:18  
Bing.

**  
Lev Rudky** 51:21  
But.

**  
Mikhail Perelman** 51:23  
Okay. All right.

**  
Lev Rudky** 51:25  
Let's try it again. Whatever is in this file.  
Can be uploaded back, right?

**  
Nathan Carver** 51:35  
If you want to make changes and upload back.

**  
Lev Rudky** 51:37  
Yes.  
Yes.

**  
Nathan Carver** 51:41  
And OK.  
So, let's just take one.  
And so what would you change here that you want to go back?

**  
Lev Rudky** 51:52  
Well, I said I put another column called named adjusted quantity.

**  
Nathan Carver** 51:57  
Mm.  
Okay.

**  
Lev Rudky** 52:03  
So, it's going to be, it's there in my e-mail when you say adjusted quantity and it populated default values are the same like in adjacent column, right? Those.

**  
Nathan Carver** 52:05  
Yeah.  
Okay.

**  
Mikhail Perelman** 52:16  
Yeah, what, what is it adjusted quantity? What?

**  
Lev Rudky** 52:19  
It means that you look at it and you say, I want to order another quantity, not the one that is suggested.

**  
Mikhail Perelman** 52:24  
Okay, so it's for purchaser to play with.

**  
Nathan Carver** 52:27  
I Singh.

**  
Lev Rudky** 52:30  
Yeah, you work with it, top line it says 350, right? You decide to do 500, yeah? So he works on, yeah, so he works on this, then...

**  
Mikhail Perelman** 52:33  
Mmh.  
Yeah, okay, okay, yeah.

**  
Nathan Carver** 52:39  
The way it would be like this, OK.

**  
Lev Rudky** 52:47  
He saves this file and continues working tomorrow, the following day, right? When he's done, he wants to upload it.  
It's like ready for...

**  
Mikhail Perelman** 52:59  
Ohh.

**  
Lev Rudky** 53:02  
For purchase orders.

**  
Mikhail Perelman** 53:03  
There is, there is a point.  
Um...  
Tomorrow, situation in BC is changed, let's say.  
Some stuff gone, some stuff pretty sick.  
How can I update this file so the changes will be reflected in this part?

**  
Lev Rudky** 53:31  
I said they're gonna tell anymore.

**  
Nathan Carver** 53:34  
Okay, so you the workflow is you've created this file and you're making your adjustments.  
Then information in MSBC changes. So you want to update your file with those changes.

**  
Val Levitan** 53:46  
I.

**  
Lev Rudky** 53:49  
Felipe.

**  
Mikhail Perelman** 53:53  
Yeah, some simple way, yeah.

**  
Nathan Carver** 53:55  
Okay.

**  
Mikhail Perelman** 53:58  
So demand is not changed, just information.

**  
Nathan Carver** 54:00  
Mhm.

**  
Mikhail Perelman** 54:04  
Some items are gone, some items are received, so...  
Need to be updated.

**  
Nathan Carver** 54:11  
Okay.  
And the things that would change would be...  
And.  
So, you already have on hand and on order, so the new information would most likely be other orders have been placed, so...  
Do you wanna update?

**  
Mikhail Perelman** 54:31  
Yeah, for example, we have 320 on order. By the way, they already received or should be received today.

**  
Nathan Carver** 54:36  
Mm.

**  
Mikhail Perelman** 54:41  
and need to be accepted into the system, received into the system. So they're going from column on order to the column on hand. And I have received.

**  
Nathan Carver** 54:55  
Okay.  
And.  
So yes, we can, so it can do that. Let's see.

**  
Mikhail Perelman** 55:04  
Yeah, so just update, update file.

**  
Lev Rudky** 55:05  
This, this.  
To discuss it, because if you do that...  
Exactly.  
Call Jay.  
Will there be?  
Will retain the same values, right?  
So, uh, basically...  
Whatever you did previous day.  
Well, may not be correct.  
Right.

**  
Mikhail Perelman** 55:56  
Not exactly if.  
If, okay, if we just receive some stuff, it transfers from on order to on hand. That's one thing. Now, if we ship something, let's say we ship big order and a lot of parts are gone,

**  
Lev Rudky** 56:07  
Yeah.  
The man, the man.

**  
Mikhail Perelman** 56:18  
So this adjusted quantity needs to be revised.

**  
Lev Rudky** 56:29  
Okay.  
Okay, but...  
Nathan.

**  
Nathan Carver** 56:36  
Yes.

**  
Lev Rudky** 56:36  
Uh, it does doable, like...  
Once he finished working on it, it goes back. It forms the whatever, the torch sorted.

**  
Nathan Carver** 56:50  
Yes, this is.  
Yes, that's doable.

**  
Lev Rudky** 56:56  
Okay.

**  
Nathan Carver** 56:58  
So I think.  
I can, I'll incorporate the columns you have, and then we have this adjusted quantity, which...  
Any numbers you enter here, I think if it defaults to blank, and then...

**  
Lev Rudky** 57:15  
No, when I when I wrote you the specs, I put default value the same as in F, but now I'm now I'm rethinking it.

**  
Nathan Carver** 57:22  
As...  
Okay.  
So either way, I think from a systems perspective, the adjusted quantity would be...  
would when you create the file would be blank because we haven't entered any different quantities. So then once you come in and say, no, I'm going to put.

**  
Lev Rudky** 57:44  
Okay.  
Because originally I thought to put the default value same like net demand zone, so you modify only whatever you need and whatever you don't need, you keep assist because the list is fairly long. This is this list is for a measure assembly.

**  
Nathan Carver** 57:50  
Um...

**  
Lev Rudky** 58:09  
but only one assembly. It's 200 lines almost. If you put together the whole device, it will double the number of lines, you know, or close to it. So, okay, Michael, it will be your call, how you want it.

**  
Nathan Carver** 58:09  
Correct.

**  
Lev Rudky** 58:30  
whether you want this column populated with the same value as in column F, or you want it empty in the...

**  
Nathan Carver** 58:31  
Yeah.

**  
Mikhail Perelman** 58:41  
It should be, yeah, it should be empty. I just need to play with this.

**  
Lev Rudky** 58:41  
Very much.  
Yeah.

**  
Nathan Carver** 58:45  
Yeah.

**  
Lev Rudky** 58:46  
Okay.  
Okay.  
Now, Nathan, you wrote about...  
What do you call rail guard, like some limits on?  
number of items. I didn't exactly get this point. Like you want what to avoid some kind of endless loop while traversing the bill of materials or.

**  
Nathan Carver** 59:19  
Yeah, let me, let me.  
So the guards are going to be on.  
How deep we go? I know we were just talking about that. Like, we're going, this is 4 levels deep.  
So the things we want to protect against are any type of loops that could happen or

**  
Lev Rudky** 59:41  
No.

**  
Nathan Carver** 59:43  
you know, tremendously deep.  
journals, right? I don't know if we saw things that were too deep beyond what the system could handle, but those are those are the type of guards just.

**  
Lev Rudky** 59:46  
Please.  
Yeah.  
Yeah.  
You know, if you generate more than...  
couple of 1000 lines, it's probably...  
Sign for a flag, for a warning, or for a stop, but within this quantity is fine.

**  
Nathan Carver** 1:00:14  
Okay. Okay, so we're usually dealing with several 100 lines.

**  
Lev Rudky** 1:00:19  
Yeah.

**  
Nathan Carver** 1:00:21  
Okay.

**  
Lev Rudky** 1:00:21  
What?

**  
Nathan Carver** 1:00:25  
Alright, yeah, that makes sense. OK, so for next steps, I'll take the e-mail you sent, Lev.

**  
Mikhail Perelman** 1:00:31  
Yeah, sorry Nathan, one more question. The item item list, it include consolidation of all the parts from different examples.

**  
Nathan Carver** 1:00:35  
Yeah.

**  
Mikhail Perelman** 1:00:49  
It's already it's already done, or...

**  
Nathan Carver** 1:00:53  
The.

**  
Lev Rudky** 1:00:54  
Here, it is done.

**  
Nathan Carver** 1:00:55  
Go ahead.

**  
Mikhail Perelman** 1:00:56  
It's done.

**  
Lev Rudky** 1:00:59  
used to be done, yeah.  
Yeah.

**  
Mikhail Perelman** 1:01:02  
Okay, so...

**  
Lev Rudky** 1:01:03  
You mean no of lines right in this output?  
One line, one item, one line, right?

**  
Nathan Carver** 1:01:09  
Correct.  
Correct, correct. There should be no duplicates.

**  
Lev Rudky** 1:01:12  
Yes.

**  
Mikhail Perelman** 1:01:16  
So, the system system give you.  
Consolidation, okay.

**  
Lev Rudky** 1:01:24  
Yeah.

**  
Nathan Carver** 1:01:24  
Correct, yep.  
Okay, so for next steps then.  
I'm going to implement the changes you sent in the e-mail lab and then what we discussed in this meeting and then turn that around and let's meet again this week to look at that so we can iterate quickly on it.

**  
Lev Rudky** 1:01:51  
Sure.  
Yeah.  
Okay.

**  
Val Levitan** 1:02:10  
Okay, thank you, Nathan. Can you lay out your tasks in Jira based on the undertakings from this meeting?

**  
Nathan Carver** 1:02:21  
Yeah, yes, I'll do that.

**  
Val Levitan** 1:02:25  
Thank you very much.

**  
Nathan Carver** 1:02:25  
And I also, I read the e-mail you sent regarding an.  
The account set up, so I'll get to that later today, but I did see it.

**  
Val Levitan** 1:02:39  
The account set up as a priority because it takes us from alpha test, which we are in as of 15th as of tomorrow.  
For about a week.  
Uh, takes a set to a beta test.

**  
Nathan Carver** 1:02:54  
Okay.  
Okay.

**  
Val Levitan** 1:02:59  
Is it mission critical? No. But like you want to get there rather sooner than later.

**  
Nathan Carver** 1:03:09  
Okay. All right. Understood.

**  
Val Levitan** 1:03:10  
And banks, and you know banks don't move too fast, as you know.

**  
Nathan Carver** 1:03:15  
Ah, right. Okay.

**  
Val Levitan** 1:03:17  
So from the moment you tell them what to do and the moment they implement something, it's going to take a while. So if we want as part of our beta test to have that routine tested as well, you want to give them instructions as soon as possible. So you want to get to that.

**  
Nathan Carver** 1:03:34  
Okay.

**  
Val Levitan** 1:03:37  
the API as soon as you can.

**  
Nathan Carver** 1:03:42  
Okay, understood.

**  
Val Levitan** 1:03:44  
Thank you. Bye.

**  
Nathan Carver** 1:03:45  
All right. Thanks, everyone.

**  
Lev Rudky** 1:03:48  
OK, thank you, thank you, bye.

**  
Mikhail Perelman** 1:03:48  
Thank you.

**  
Val Levitan** stopped transcription
