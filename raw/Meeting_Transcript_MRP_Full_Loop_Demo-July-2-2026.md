**MRP - Full Loop Demo-20260702\_094757-Meeting Recording**

July 2, 2026, 1:47PM

47m 45s

**  
Nathan Carver** started transcription

**  
Nathan Carver** 0:03  
Um...  
The.  
I had the five, just five points laid out of...  
what we're going to, what I need to do next. And so I can quickly run through what we have now, but really to get unblocked and finish off the rest of the items in the backlog is just to review those next steps. And.  
Those are around the order efficiency.  
which is the...  
MLQ awareness and the price breaking.  
And then we have the vendor and item master rights.  
And...  
And then the last two is the the locks up inventory check and the PO release.  
So these are things I'm going to move forward with. I kind of have a recommended approach, but I want to make sure this is aligning with  
what we need to do going forward.

**  
Val Levitan** 1:13  
I don't think they understood a word you said.

**  
Nathan Carver** 1:13  
Seven.  
Okay.  
So, let's...  
And.

**  
Val Levitan** 1:21  
Can you can you can you simplify? Can you primitive your your speaking?

**  
Nathan Carver** 1:26  
Yeah, so that's...

**  
Val Levitan** 1:27  
Just use short sentences, a little bit louder, punctuation, like frequent stops. It doesn't register with what you're saying.

**  
Nathan Carver** 1:34  
You.  
Okay.  
So, the next step is...  
Order efficiency.  
So, we have...  
the option of the price break and small order bundling. So this basically comes down to.  
Um...  
The default approach would be keep this to the buyers. So whoever is running the bomb, putting together the order is going to use their judgment.  
and the agent will go along with that judgment. This has to do with.  
price breaks in your ordering, in your minimum value thresholds. And it's in the, so if you open the e-mail invite, I have those five.  
five steps that basically I just, you know, thumbs up, thumbs down, or this is how, this is how we think of this. So that's it. That's all I need to get.  
To start, that's all I need to start moving into the next set of features.  
Okay, so let's look at what we have.  
So far.  
No, make this bigger.  
So, asking it to compare building 250, 500, and 750.  
Of a particular part.  
And you can ask it to show us where we're short and do this, you know, short and side by side. So it's, it now has the ability to...  
look at multiple builds and give you a sense of where the data is.  
where all the shorts are.  
And actually, this is more of a build, planning the build as opposed to just getting a short count and creating an order.  
So, let's see.  
Hold on, I think I have the wrong cloth session started.  
Let me.  
Let me verify this real quick.  
Yeah.  
All right.  
All right, here we go.  
All right, now it has its tooling.  
So asking it to compare the three build quantities for an item, it's going to go and pull these side by side using what is called its scenario tool. So it has tooling now to build out these scenarios that you might need.  
Okay, so in this scenario for this part, it's laying out the three quantities that we asked for, 250, 500, 750.  
It's showing us.  
Of each one, how many parts short we are of the 46?  
And then how many of the parts are covered?  
And then it's breaking these down.  
into part numbers using what's in MSBC.  
showing how many are on hand and how many are actually on order at this time. So this is using one of the development MSPC servers that we created. So it's not, I'm not running it on production yet. So this is going to be stale.  
if you've been updating production.

**  
Lev Rudky** 5:54  
Yeah.  
Can you?

**  
Nathan Carver** 5:55  
So, this is, go ahead.

**  
Mikhail Perelman** 5:55  
The.

**  
Lev Rudky** 5:58  
Can you scroll back, scroll up, give me a few steps back? So, I want to build...  
Three quantities.  
Of the same part number.  
Correct.

**  
Nathan Carver** 6:15  
Correct. That's what this is doing. That's right.

**  
Lev Rudky** 6:18  
Okay.  
No.  
So, if I understand correctly...

**  
Nathan Carver** 6:30  
Yeah.  
Yeah.

**  
Lev Rudky** 6:34  
Uh, let's say the first line for 250.  
I am 21 parts short.

**  
Nathan Carver** 6:46  
Correct.

**  
Lev Rudky** 6:46  
Mm.  
Okay, so...  
If I want to build 500.

**  
Nathan Carver** 6:56  
Yeah.

**  
Lev Rudky** 6:58  
And I am 14 short.

**  
Nathan Carver** 7:00  
No.

**  
Lev Rudky** 7:01  
Is it additional 14?

**  
Nathan Carver** 7:02  
Yeah.

**  
Mikhail Perelman** 7:04  
No, it's 14 covered, 32 short.

**  
Lev Rudky** 7:09  
Yeah, okay, 14 Carver. Okay, makes sense. Okay.

**  
Nathan Carver** 7:11  
No.

**  
Lev Rudky** 7:14  
But sure, yeah, OK, OK, go down.

**  
Nathan Carver** 7:17  
Yeah.

**  
Lev Rudky** 7:28  
Okay.  
Hey.  
So...  
Three.  
Write columns.  
They basically address.  
Shortages.  
for individual bills.

**  
Nathan Carver** 7:49  
What?  
Yes.  
Yes.

**  
Lev Rudky** 7:55  
Okay.  
Okay.

**  
Nathan Carver** 8:00  
Yeah.

**  
Lev Rudky** 8:00  
So, uh...  
Ah.

**  
Nathan Carver** 8:05  
Mm.

**  
Lev Rudky** 8:07  
So, can you put...  
A query for...  
Consolidated.  
Shortages.

**  
Nathan Carver** 8:16  
Yeah.  
Yes, what is the query?

**  
Lev Rudky** 8:23  
So, let's say...

**  
Nathan Carver** 8:25  
Tse.

**  
Lev Rudky** 8:26  
I need, I need the total quantity of what was it, the 1500, right? So, what would be the shortage for the?  
For uh, all those three.

**  
Nathan Carver** 8:39  
I.  
Yeah.  
Oh, a total?

**  
Lev Rudky** 8:43  
Yeah.

**  
Nathan Carver** 8:49  
Yeah.  
And so.

**  
Lev Rudky** 9:04  
Yeah.  
Tse.  
Tse.  
Roll up a little bit.

**  
Nathan Carver** 9:49  
Yes.

**  
Lev Rudky** 9:50  
Stop, stop here.

**  
Nathan Carver** 9:50  
Okay.

**  
Lev Rudky** 10:16  
Okay, keep going.  
Yeah.

**  
Nathan Carver** 10:26  
I.

**  
Lev Rudky** 10:32  
Okay.

**  
Nathan Carver** 10:33  
Thank you.

**  
Lev Rudky** 10:35  
This is fine.

**  
Nathan Carver** 10:46  
So then it's giving you some, it will make observations on the data and give feedback on that. And then it's also generally going to follow up with a question if you'd like to. So for this, do you want to group this by vendor or price it out for a consolidated PO run?

**  
Lev Rudky** 11:07  
By vendor.

**  
Nathan Carver** 11:08  
Yeah, so we can just say group by vendor.  
Okay, so it groups them up. Oh, sorry.

**  
Mikhail Perelman** 12:02  
OKI want.

**  
Nathan Carver** 12:10  
Okay.

**  
Lev Rudky** 12:38  
Yeah.

**  
Nathan Carver** 12:39  
The.

**  
Lev Rudky** 12:42  
Those.  
Brunch.  
that you type.

**  
Nathan Carver** 12:48  
Mhm.

**  
Lev Rudky** 12:51  
Some of them.  
All of them, basically, they define the views.

**  
Nathan Carver** 12:58  
Yes.

**  
Lev Rudky** 13:00  
Chen.  
those views be stored somewhere as to not repeat them. For example, I want one view, I want to see.

**  
Nathan Carver** 13:03  
Yes.  
Yeah.  
No.  
Tse.

**  
Lev Rudky** 13:17  
Part number.  
Demand.  
Quantity on hand.  
Quantity on POS.  
Total to order as an example, something is it possible to generate something like that?

**  
Nathan Carver** 13:35  
Yeah.  
Yeah, so you can do create a report of.  
Um...  
So what was it? Just a simple example.

**  
Lev Rudky** 13:47  
Well, it's a part number.

**  
Nathan Carver** 13:48  
Yeah.

**  
Lev Rudky** 13:51  
Render.

**  
Nathan Carver** 13:52  
I.

**  
Lev Rudky** 13:54  
Going to on hand.  
Quantity on pure.  
And compose net demand.  
Yeah.

**  
Nathan Carver** 14:10  
Not demand, OK.

**  
Lev Rudky** 14:11  
Yeah.  
Every month, replace it with quantity to order.

**  
Nathan Carver** 14:21  
Oh, net demand and this is quantity to order. Same thing.

**  
Lev Rudky** 14:25  
Yeah.  
Uhh.

**  
Mikhail Perelman** 14:29  
No.

**  
Lev Rudky** 14:29  
Going to go and quantity to to order, yeah.

**  
Val Levitan** 14:32  
OK.

**  
Nathan Carver** 14:34  
Okay.  
Yeah, so we can just ask it for a report.  
And.  
And it'll do that.  
Let's see, it's asking.

**  
Lev Rudky** 16:03  
Okay.

**  
Mikhail Perelman** 16:07  
So, you show it in Excel file.

**  
Nathan Carver** 16:10  
No.

**  
Lev Rudky** 16:10  
Tse 3, similar.  
Yeah.

**  
Nathan Carver** 16:15  
Yeah, it's just a CSV, so you can look at it. It's you can look at it as a spreadsheet, the report that it generates.

**  
Lev Rudky** 16:24  
Okay.  
Now.  
The.  
Is it possible to save to save the prompt, whatever you typed on the command line there?

**  
Nathan Carver** 16:32  
The.  
Bing.  
Mm.

**  
Lev Rudky** 16:41  
And so...  
Those will be repeating themselves.

**  
Val Levitan** 16:47  
I save, I save prompts in the prompt directory.  
So prompts that I reuse from time to time, I save in the directory, but I don't do it efficiently. A better way.

**  
Nathan Carver** 16:56  
Yeah.  
Okay.  
Yeah.

**  
Val Levitan** 17:05  
A better way for prompting.

**  
Lev Rudky** 17:06  
Yeah.

**  
Val Levitan** 17:08  
is to have an agent that does it for you, an autonomous agent. If it's the same type of prompting, what we can create is a repetitive autonomous agent that repeats the same thing over and over.

**  
Nathan Carver** 17:09  
Right.  
Yes.

**  
Val Levitan** 17:27  
Let's say on a daily basis, Michael could come to his office and say, and the agent for 9 A.m. will give you the shortages.  
You could do another agent for, let's say, weekly reports.  
approach with an agent is much better because an agent is repetitive.

**  
Nathan Carver** 17:49  
Yeah, that's right, and it's...

**  
Val Levitan** 17:50  
But, but, but you, but you, but you could, but you could save a prompt. Many times I save prompts myself.

**  
Mikhail Perelman** 17:50  
There are several, there are several reports.

**  
Lev Rudky** 18:00  
Yeah, so there will be a set of repetitive.

**  
Val Levitan** 18:07  
So you could definitely save a prompt if you want, but whatever repetitive work, I would prefer to allocate it to an agent.

**  
Lev Rudky** 18:07  
Give us my.

**  
Nathan Carver** 18:10  
No.  
Correct. And if you know that repetitive work, basically all you have to do is just...  
put it in a text document for me, just step one, step two, step three. This is what I do every day. And then...  
Um...  
We would create a skill. It's just a basically as it's kind of like saving a set of instructions for the agent.  
And you just tell the agent, you know, run daily report, whatever you call it, and it will repeat that same process every day. Every time you just type a simple command, it'll repeat all those steps that you, whatever it is your normal workflow is.  
So that's where this is going to bear, where it has the agent or the tool that we're building has two sides to it. It has the software side, which is  
Procedural steps programmed in.  
how to pull data from MSBC, how GDL specifically classifies data in MSBC. And then it has the skill instruction side, which is what we're talking about now. This is how we work, this is how we flow, and this is  
our daily processes. So those two combined will create these agents that can efficiently go and do this stuff for you very quickly.  
Yes.

**  
Lev Rudky** 19:59  
Yeah.

**  
Nathan Carver** 20:02  
So if you have examples of that, share them with me and I can put together.  
The skill, and it would be simply you just...  
typing a simple command and it goes and does all those steps.

**  
Lev Rudky** 20:21  
Okay, so for the time being, we can stick with the current one. It will be refined later on, but for practicing, for practicing.

**  
Nathan Carver** 20:23  
A

**  
Mikhail Perelman** 20:29  
Well...  
Yeah.

**  
Lev Rudky** 20:34  
So, good.

**  
Mikhail Perelman** 20:34  
Okay, Nathan.

**  
Nathan Carver** 20:36  
Mm.

**  
Mikhail Perelman** 20:37  
Ohh, let me start from the beginning.

**  
Nathan Carver** 20:40  
Okay.

**  
Mikhail Perelman** 20:40  
We, let's say, choose product.

**  
Nathan Carver** 20:44  
Yeah.

**  
Mikhail Perelman** 20:45  
Choose what kind of assembly.

**  
Nathan Carver** 20:46  
Yeah.

**  
Mikhail Perelman** 20:49  
Assembly, what kind of assembly this product consists of?

**  
Nathan Carver** 20:51  
Yes.

**  
Mikhail Perelman** 20:56  
We should enter them, enter them into the system with quantities.

**  
Nathan Carver** 20:57  
You.  
Yeah.  
Yes.

**  
Mikhail Perelman** 21:06  
That is how we should receive a report for how many.  
And then we have to consolidate.

**  
Nathan Carver** 21:12  
Okay.

**  
Mikhail Perelman** 21:15  
consolidate if there are some parts that are going into the system into one assembly and another assembly. It has to be consolidated. How we can do this?

**  
Val Levitan** 21:17  
No, this is that.

**  
Nathan Carver** 21:19  
Yes.  
Yeah.

**  
Val Levitan** 21:28  
This is probably an incorrect approach. This is the approach of...  
This is the approach that you used with limited tools previously.

**  
Nathan Carver** 21:37  
Yeah.

**  
Val Levitan** 21:42  
You used to that approach, but it's illogical. It has no logic. It's the wrong logic. That logic applied only because you had limitation in the tools.

**  
Nathan Carver** 21:45  
Good.

**  
Mikhail Perelman** 21:56  
Okay.  
Anyway.

**  
Nathan Carver** 21:59  
Thanks.

**  
Mikhail Perelman** 22:00  
We should have consolidated part numbers. We should know how many of them and what we need, how many we need.

**  
Nathan Carver** 22:08  
Correct.

**  
Val Levitan** 22:09  
Correct.

**  
Mikhail Perelman** 22:09  
Everything else is everything close is clear, so first.  
how we enter it into the system.  
What need what need to be done to enter that into the system to receive this report?

**  
Nathan Carver** 22:22  
Okay.

**  
Val Levitan** 22:26  
I don't understand the question. What's the question?

**  
Mikhail Perelman** 22:29  
The question is, input, how we do input?

**  
Nathan Carver** 22:31  
Yeah.

**  
Val Levitan** 22:34  
Input we do by the number of products we want to manufacture.

**  
Nathan Carver** 22:34  
Tse.

**  
Mikhail Perelman** 22:39  
Where?

**  
Nathan Carver** 22:40  
Yeah.

**  
Mikhail Perelman** 22:41  
Where are we keeping the list of this product?

**  
Nathan Carver** 22:45  
Yeah.  
MSBC.

**  
Val Levitan** 22:47  
Why do we, why do we need a list of the product? Why don't we know the product? You want, you want to pull up, pull down menu of all the products.

**  
Nathan Carver** 22:50  
Right.

**  
Mikhail Perelman** 22:57  
I don't want to enter my area.

**  
Val Levitan** 23:00  
No problems, no problem.

**  
Mikhail Perelman** 23:00  
The product, it's already in the system. I just need to put 100 pieces to 100 or whatever.

**  
Nathan Carver** 23:01  
Yeah.

**  
Val Levitan** 23:05  
No problems, we could, we could say, no problems, we could say, pull down the list of all products.

**  
Nathan Carver** 23:07  
Right.

**  
Val Levitan** 23:11  
And it will give you the list of products.

**  
Nathan Carver** 23:13  
Yeah.  
So we can ask or give it a command to go retrieve the list of products.  
OK.  
Okay, so what I found was there's 250 item response and that's going to be large. So now it's optimizing its...  
it's searched. So now it's going to start caching things to a local text file. So the tool will have the ability to make these decisions if you start asking for large.  
You know, large chunks of data.

**  
Mikhail Perelman** 24:16  
No, this is not a list of product.

**  
Nathan Carver** 24:17  
The.

**  
Mikhail Perelman** 24:19  
I am interested in.

**  
Nathan Carver** 24:21  
Yeah.

**  
Val Levitan** 24:21  
You're interested in, you're interested in.

**  
Mikhail Perelman** 24:22  
I need part, I need part numbers, I need part numbers.  
Assembly part numbers that make.

**  
Nathan Carver** 24:31  
Okay.

**  
Mikhail Perelman** 24:34  
Flex or some other product.

**  
Nathan Carver** 24:35  
Tse.  
Okay, so...

**  
Mikhail Perelman** 24:38  
What part? What is the list part numbers? Top level assemblies.

**  
Nathan Carver** 24:44  
Top level assembly.

**  
Mikhail Perelman** 24:47  
Well...

**  
Lev Rudky** 24:49  
He needs to purchase level items.

**  
Mikhail Perelman** 24:57  
Not.

**  
Nathan Carver** 24:57  
Ohh.

**  
Mikhail Perelman** 24:58  
Not purchase Lev.  
The final list of assemblers.

**  
Lev Rudky** 25:07  
What do you call?

**  
Mikhail Perelman** 25:07  
We have, we have file, we have a file right now.

**  
Nathan Carver** 25:08  
I.

**  
Mikhail Perelman** 25:14  
We on a first plate sample summary, we have a list of all assemblies that could be ordered. Some of them goes for effort, some of them go for flex, some of them go for flex pay and so on.

**  
Nathan Carver** 25:19  
Play.  
Yes.

**  
Mikhail Perelman** 25:30  
My business is to click on this part number, put quantity next to it, and then system provide me list of all the components with how many we kept in stock, how many, how many we need.

**  
Nathan Carver** 25:37  
Mm.  
Yeah.  
Yeah.  
Yeah.

**  
Mikhail Perelman** 25:52  
Short, let's say.

**  
Lev Rudky** 25:53  
Okay, Nathan, what he was talking about, we have a list of...  
Forecasted items, if you will, right? Let's say 20 line items.

**  
Nathan Carver** 26:05  
Mhm.

**  
Mikhail Perelman** 26:09  
It's not 20, it's probably 50-60, but...

**  
Lev Rudky** 26:09  
Yeah.  
Does it matter?

**  
Mikhail Perelman** 26:16  
No, no, no.

**  
Lev Rudky** 26:16  
Whatever. So there is a list of forecasted items. Those could be.

**  
Nathan Carver** 26:18  
Oh.  
Tse.

**  
Lev Rudky** 26:26  
Either finished goods or high-level assembly, or whatever it might be, so...

**  
Nathan Carver** 26:27  
Yes.  
Yeah.  
No.

**  
Lev Rudky** 26:33  
This is the input.  
As an output, he wants to have a list.

**  
Nathan Carver** 26:41  
Please.

**  
Lev Rudky** 26:42  
Of consolidated, consolidated.  
Purchase items.

**  
Nathan Carver** 26:47  
The.

**  
Lev Rudky** 26:48  
Beautiful.

**  
Nathan Carver** 26:52  
Okay, that would, you need to know all the parts you have to purchase to create those.

**  
Lev Rudky** 26:57  
Yeah.

**  
Mikhail Perelman** 26:58  
But...

**  
Nathan Carver** 26:58  
Assemblies.

**  
Lev Rudky** 27:01  
Yes.

**  
Mikhail Perelman** 27:01  
Begin.

**  
Nathan Carver** 27:02  
You.

**  
Mikhail Perelman** 27:03  
It should be for particular product line. For example, product line for flex. We have that many for flex, let's say 27 inches, that many for flex, 43 inches.

**  
Nathan Carver** 27:04  
Be.  
Yeah.  
Yeah.  
Yeah.

**  
Mikhail Perelman** 27:23  
That is.

**  
Nathan Carver** 27:24  
Yeah.  
And.  
So, we can do that. The those types of that type of metadata will have to be an MSPC identifying.  
how these are associated.

**  
Lev Rudky** 27:43  
Yeah.

**  
Nathan Carver** 27:44  
But asking this question.  
Give me the list of.  
Top-level assemblies, right? It can see that, so it can go.  
find all of them in MSVC and give you a list. So if you know the assemblies you want.  
to build, then you would tell it, I need these specific assemblies.

**  
Val Levitan** 28:16  
Sorry, Nathan, may I ask you to stop sharing and start sharing again? I'm sorry to...

**  
Nathan Carver** 28:17  
Yeah.  
Yeah, let me do that.

**  
Val Levitan** 28:23  
Yeah.  
Start sharing now. Do you use a hardware accelerator?

**  
Nathan Carver** 28:31  
Go.  
Yeah.  
Do I have a hardware accelerator?

**  
Val Levitan** 28:39  
Yeah.

**  
Nathan Carver** 28:41  
Let me look.  
Is that, so I guess the short answer is yes.

**  
Val Levitan** 29:09  
Can you, can you?

**  
Nathan Carver** 29:10  
But is that a Teams specific setting or another setting?

**  
Val Levitan** 29:14  
No, it's the general setting.

**  
Nathan Carver** 29:18  
Oh, for the system.

**  
Val Levitan** 29:20  
For the system.

**  
Nathan Carver** 29:25  
Yes, is it suggesting turn that off?

**  
Val Levitan** 29:28  
Yeah, turn it off, please.

**  
Nathan Carver** 29:34  
Let's see here.

**  
Val Levitan** 29:38  
And then stop and start again.

**  
Nathan Carver** 30:02  
Okay.

**  
Val Levitan** 30:12  
Yes.

**  
Nathan Carver** 30:28  
All right, trying to figure out how to do that.  
Let me put, let me put.  
Make the clients.  
It's just the black screen on your side, right, Val?

**  
Val Levitan** 31:22  
No, I see why it's green.

**  
Nathan Carver** 31:23  
Yeah.  
You see what?

**  
Val Levitan** 31:27  
Widescreen.

**  
Nathan Carver** 31:28  
Okay.  
All right.  
All right, so within MSBC.  
We do have these.  
Right, it can identify these top level assemblies. So if we were to...  
And.  
Give it two of these.  
Is that the direction you're going? It's like, I need to build just whatever, however many of these, so I need to build.

**  
Lev Rudky** 32:25  
Correct, I need.

**  
Nathan Carver** 32:26  
Okay.

**  
Lev Rudky** 32:28  
I'll have, I'll have a list in B.C.

**  
Nathan Carver** 32:29  
The.  
Tse.

**  
Lev Rudky** 32:35  
I'll have a dedicated place which will be equivalent to forecast.

**  
Nathan Carver** 32:38  
Yes.  
Yeah.

**  
Lev Rudky** 32:43  
And I'll have there a list of items I need to build.

**  
Nathan Carver** 32:45  
Tse.

**  
Lev Rudky** 32:51  
And this will be a list of items with quantities, then this will be an input.

**  
Nathan Carver** 32:51  
Okay.  
B.

**  
Lev Rudky** 33:01  
Right, so don't have to type it in, it all will be stored in BC.

**  
Nathan Carver** 33:05  
One.

**  
Lev Rudky** 33:09  
And maintained by Michael.  
When Mikhail, right? So, and this...

**  
Nathan Carver** 33:15  
Yes.

**  
Mikhail Perelman** 33:17  
No, first of all, first of all, we have engineering file.  
where all major assemblies for each product line are listed.

**  
Nathan Carver** 33:28  
Mm.

**  
Lev Rudky** 33:30  
It should be.

**  
Mikhail Perelman** 33:30  
When addition is a file that we have, all this assemblies were transferred to summary table, and that is where I can choose how many of which.

**  
Lev Rudky** 33:33  
You see, you shouldn't be using.

**  
Nathan Carver** 33:41  
Yeah.  
Yeah.

**  
Lev Rudky** 33:43  
Because he.

**  
Mikhail Perelman** 33:43  
This doesn't count years, so if yeah.

**  
Lev Rudky** 33:46  
Tse.

**  
Nathan Carver** 33:48  
Yeah.

**  
Lev Rudky** 33:49  
Your terminology is confusing for others.

**  
Nathan Carver** 33:51  
Yeah.

**  
Lev Rudky** 33:54  
Right? So, basically, you, if you have you have a forecast that you need to satisfy, you need to order, you need to build this much for this part number, this much for this part number of this part number, correct? You need to build.

**  
Nathan Carver** 33:54  
Yes.  
This.  
It's the same.  
But...  
Yeah.

**  
Mikhail Perelman** 34:12  
What is what is that number?

**  
Lev Rudky** 34:13  
Ten, 10 foot.

**  
Nathan Carver** 34:15  
Yeah.

**  
Lev Rudky** 34:17  
But number it is an item in Business Central.

**  
Mikhail Perelman** 34:23  
Yes. Okay, so this is a purchase part number.

**  
Nathan Carver** 34:26  
Yeah.

**  
Mikhail Perelman** 34:28  
You're talking about purchase part number or high-level assembly part number.

**  
Nathan Carver** 34:30  
Oops.

**  
Lev Rudky** 34:34  
Both of them, both of them are part numbers.

**  
Mikhail Perelman** 34:34  
What with the?  
Bosik.

**  
Lev Rudky** 34:38  
Most of them are part numbers, right? So you have a table, the same like you had in the past, only it will be stored in Business Central. This is forecast, right? You specify, you create the lines that you need to

**  
Nathan Carver** 34:45  
Yes.  
Yeah.  
Yes.

**  
Lev Rudky** 34:57  
Build, and you put the quantities, how many you need to build this.

**  
Mikhail Perelman** 35:01  
What, what does it mean? Create July?

**  
Nathan Carver** 35:03  
Yes.

**  
Lev Rudky** 35:05  
You go to a table, I will tell you to which. I'll find it. Let's say, for argument's sake, you need to build 10 flexes.

**  
Nathan Carver** 35:08  
Tse.  
Yeah.  
Yeah.

**  
Lev Rudky** 35:16  
Single configuration.

**  
Nathan Carver** 35:18  
me.

**  
Lev Rudky** 35:19  
Okay, so you select part number for this flags.

**  
Nathan Carver** 35:20  
Yeah.  
No.

**  
Lev Rudky** 35:25  
Can you put 10? Or if you want, you select the module it consists of and select quantity, whatever, whether it's finished product, assembly, sub-assembly, each one of them has a part number.

**  
Nathan Carver** 35:26  
Oh.  
Yeah.  
Yeah.

**  
Lev Rudky** 35:43  
We agree on that, right?

**  
Mikhail Perelman** 35:47  
OK.

**  
Lev Rudky** 35:49  
Yes, so it exactly like you operated before, but it will be operated out of Business Central.

**  
Nathan Carver** 35:53  
Okay.  
Yeah.

**  
Lev Rudky** 35:57  
Right.

**  
Mikhail Perelman** 35:58  
That's fine. My question is...  
Where we have a list of is this top level assemblies as as we have an engineering file where I can go through this list and just put numbers for the particular.

**  
Nathan Carver** 36:05  
Yeah.  
Yes.  
Yes.  
Yeah.  
Yeah.  
Yes.  
Okay.

**  
Lev Rudky** 36:23  
I, I...

**  
Mikhail Perelman** 36:23  
A particular assembly.

**  
Lev Rudky** 36:25  
I will show you. It's not engineering file, it's a list of our numbers, a list of part numbers in Business Central.

**  
Mikhail Perelman** 36:27  
Okay.

**  
Nathan Carver** 36:29  
Yeah.  
Right.

**  
Mikhail Perelman** 36:38  
That's right.

**  
Nathan Carver** 36:40  
Right.

**  
Lev Rudky** 36:40  
Yes, so.

**  
Mikhail Perelman** 36:40  
But it comes is at least comes from engineering file; this is a basic.

**  
Nathan Carver** 36:44  
Bing.

**  
Lev Rudky** 36:45  
It comes from what Genadi entered into the system.

**  
Nathan Carver** 36:47  
No.

**  
Mikhail Perelman** 36:51  
Yeah.

**  
Lev Rudky** 36:51  
Right, where it came from for this exercise is irrelevant, right? So, so we have a list of items.

**  
Nathan Carver** 36:51  
Yeah.  
What?  
The.

**  
Lev Rudky** 37:02  
List of all possible items in Business Central.

**  
Nathan Carver** 37:04  
Yes.

**  
Val Levitan** 37:05  
Nathan.

**  
Nathan Carver** 37:06  
Good.

**  
Val Levitan** 37:07  
Nathan.

**  
Nathan Carver** 37:08  
Yeah.

**  
Val Levitan** 37:10  
We're good.

**  
Nathan Carver** 37:10  
Good, good.

**  
Val Levitan** 37:11  
We're good.  
Thank you, buddy.

**  
Nathan Carver** 37:13  
Alright, I found it. I found it.

**  
Val Levitan** 37:16  
Thank you, buddy.

**  
Nathan Carver** 37:17  
You're welcome.

**  
Lev Rudky** 37:23  
So.

**  
Nathan Carver** 37:24  
Cool.

**  
Lev Rudky** 37:25  
So, the input is no.

**  
Nathan Carver** 37:26  
Yeah.

**  
Val Levitan** 37:27  
Lova, you're absolutely on the right track. You got it. You're absolutely 100% correct. You got it. Now, now, now we're talking the same language.

**  
Nathan Carver** 37:31  
No.  
Scism.

**  
Lev Rudky** 37:40  
OK, so what I was talking about is it relates to inputs.

**  
Nathan Carver** 37:41  
In.  
Okay.

**  
Lev Rudky** 37:48  
For analysis.

**  
Nathan Carver** 37:50  
Yeah.

**  
Lev Rudky** 37:51  
Now, regarding the output.  
So, regarding the output...  
We need.

**  
Nathan Carver** 38:03  
The.

**  
Lev Rudky** 38:05  
To.  
Store repetitive prompts.

**  
Nathan Carver** 38:07  
Yeah.  
Yeah.

**  
Lev Rudky** 38:12  
Somehow.  
And, ideally...

**  
Nathan Carver** 38:17  
Yeah.

**  
Lev Rudky** 38:17  
Those.

**  
Nathan Carver** 38:18  
Yes.

**  
Lev Rudky** 38:19  
could be called upon on demand. I mean, not like scheduled or anything else. The, the, I'm not sure about.

**  
Nathan Carver** 38:20  
Okay.  
Mmh.

**  
Lev Rudky** 38:34  
Yes, I think it shouldn't be an issue, right?  
Should call up on her.  
Pre-existing prompt.

**  
Nathan Carver** 38:41  
Yeah.

**  
Lev Rudky** 38:45  
On demand, right?

**  
Nathan Carver** 38:46  
Yes.

**  
Lev Rudky** 38:47  
So prompt 5 or prompt whatever description attached to it and to display the output according to this prompt.

**  
Nathan Carver** 38:56  
Cris.  
No.

**  
Lev Rudky** 39:05  
That's.

**  
Nathan Carver** 39:05  
Yes, if you have prompts, we can.  
We can do that, so...  
On.  
Whenever.  
Whatever like simple code prompt you want to give it, we can give those, we can create those skills for the agent.  
Right, and it would have that. You can see that I have my own custom prompts that I put in here.  
around JIRA.  
I have a local screenshot, but we can create these prompts for this tool. So they're just very small keywords. And then when you're in Claude, you would just do the forward slash and it's going to show you.  
All the prompts that it has, and you will see.  
So maybe we do, you know, MSPC.  
Right now we can see that the JVL specific.  
skills that are in here.  
So...  
what we have so far, and these may not be terms that you use, right, but we have these skills that are defined, start planning, run, accountability, review, and the tracking. So some of these are.  
And...  
You know, the names are more generic, you know, function-oriented, but we can we can give these more, you know, just human names to match what it is that you do.

**  
Lev Rudky** 40:32  
Yeah.  
So...  
Ahh.  
I will both.

**  
Nathan Carver** 40:42  
Great.

**  
Lev Rudky** 40:43  
Thank you.

**  
Nathan Carver** 40:45  
No.

**  
Lev Rudky** 40:46  
I'll discuss at some points with Mikhail. I will send you.

**  
Nathan Carver** 40:50  
The.

**  
Lev Rudky** 40:54  
The.  
So, I'll send you where the inputs.

**  
Nathan Carver** 40:58  
Yeah.  
You.

**  
Lev Rudky** 41:00  
Will be Stuart.

**  
Nathan Carver** 41:02  
Yes.

**  
Lev Rudky** 41:03  
in Business Central.

**  
Nathan Carver** 41:05  
Yes.

**  
Lev Rudky** 41:06  
And.

**  
Nathan Carver** 41:07  
I.

**  
Lev Rudky** 41:08  
Example.  
Column headers for the sum of the outputs.

**  
Nathan Carver** 41:13  
Yes.  
Yeah.

**  
Lev Rudky** 41:17  
So, basically, we'll create a few prompts.  
that will produce the necessary output and will be repeatable. That's the point. The final output should be such that the end user can easily operate on it.  
Right. So it basically boils down to.  
List of columns.  
That should be on the output.  
Am I?

**  
Nathan Carver** 41:59  
Okay, yeah, that would be perfect.

**  
Lev Rudky** 42:05  
So, uh...  
Yeah.  
Always the the.

**  
Nathan Carver** 42:12  
Yes.

**  
Lev Rudky** 42:15  
Data completeness or data?

**  
Nathan Carver** 42:19  
Yeah.

**  
Lev Rudky** 42:20  
Clean this is a...

**  
Nathan Carver** 42:21  
Yeah.

**  
Lev Rudky** 42:23  
Stand-alone topic right, it will.  
Take some time to sort it out, but...

**  
Nathan Carver** 42:30  
Yeah.

**  
Lev Rudky** 42:33  
Functionality should not be affected by it.

**  
Nathan Carver** 42:38  
Correct. Yes, we can still use it and it'll just get better as the data gets cleaned up.

**  
Lev Rudky** 42:47  
Yes, so.

**  
Nathan Carver** 42:48  
No.

**  
Lev Rudky** 42:49  
So, basically, I said my piece.

**  
Nathan Carver** 42:52  
Yeah.  
Okay.

**  
Val Levitan** 42:57  
So when can you provide this information?

**  
Lev Rudky** 43:01  
Yeah, so they...

**  
Nathan Carver** 43:03  
Yeah.

**  
Lev Rudky** 43:07  
Okay, the data source, today is what, Friday.

**  
Nathan Carver** 43:09  
Yes.

**  
Lev Rudky** 43:14  
I'll provide the, I'll provide it.

**  
Val Levitan** 43:19  
Today is Thursday.

**  
Lev Rudky** 43:20  
Today is Thursday, a holiday Thursday.  
I aim for tomorrow.

**  
Val Levitan** 43:28  
Okay, so let's assume that tomorrow night you'll provide it.

**  
Nathan Carver** 43:28  
Okay.

**  
Lev Rudky** 43:33  
Fair enough.

**  
Nathan Carver** 43:35  
So it's a holiday weekend here. So I am not going to get back to it until Monday morning anyway. So just.

**  
Val Levitan** 43:36  
Van.

**  
Lev Rudky** 43:39  
Yeah.

**  
Val Levitan** 43:44  
So Monday morning it is. And then starting Monday morning, Nathan, what will be your plan or what are we trying to achieve for that week?

**  
Nathan Carver** 43:46  
Yeah.

**  
Val Levitan** 43:55  
Can we roughly lay it out or schedule it at least in verbally so we understand what to expect?

**  
Nathan Carver** 43:56  
And.  
Yeah, that's.

**  
Val Levitan** 44:04  
Let's say we have a meeting next Thursday.

**  
Nathan Carver** 44:08  
Yeah, let's do that here.

**  
Lev Rudky** 44:10  
You.

**  
Val Levitan** 44:10  
What would be expected deliverables?

**  
Nathan Carver** 44:14  
Let me see here.  
All right, so I've been waiting, so let me...  
restructure this. So Lev, when you send me that, I'm going to add a task here.  
for implementing those.  
The yeah, are you seeing the browser?

**  
Val Levitan** 44:32  
Are you sharing your screen?

**  
Lev Rudky** 44:36  
Yeah, yeah, I can see.

**  
Val Levitan** 44:37  
No, I'm not. I'm not seeing anything.

**  
Nathan Carver** 44:39  
All right, let me try.  
We try it different.  
Okay.  
Curious, let me try this.  
Anything?

**  
Val Levitan** 45:04  
One second.  
No.

**  
Nathan Carver** 45:08  
Interesting.  
When I try to share a browser view with you, it doesn't work. Or when I share the console view, it works. Okay, I think there's something. I found the settings on my side. I will play that. What I'm looking at is just the Jira board, the company portfolio.

**  
Val Levitan** 45:27  
Ah, okay. Let me open that on my side.

**  
Nathan Carver** 45:28  
In the.  
Yeah.  
That's all I'm looking at.

**  
Val Levitan** 45:31  
Okay, yeah, so looking at the Giorgi board, yeah.

**  
Nathan Carver** 45:33  
Two.  
So, one, so 941, I'm gonna pick that up on Monday, 946.  
is vendor and item master record rights. This, we may just decide we want to defer this. This may not be needed for now. I don't know if it's important. This is basically giving the tool the ability to keep your item records and your vendor records updated in MSPC.

**  
Val Levitan** 46:01  
You're talking about 964?

**  
Nathan Carver** 46:04  
Correct, 964.

**  
Val Levitan** 46:06  
Ah, I see deferred. Okay, so let's put it in.  
and backlog them.

**  
Nathan Carver** 46:14  
Okay.

**  
Val Levitan** 46:15  
So all three items. Do you want me to move it or will you move it?

**  
Nathan Carver** 46:17  
Yep.  
You can go ahead and move them to backlog, that's fine.

**  
Val Levitan** 46:24  
Doing it now.

**  
Nathan Carver** 46:26  
So then I will get to work on 941 is where I will.  
add in the story for this implementing what Lev shares with me and I'll start that on Monday. My goal.

**  
Val Levitan** 46:39  
Which one, Sergey? Which one?

**  
Nathan Carver** 46:41  
941. I'll add a new story under 941 to implement what Lev will share on Monday morning.

**  
Val Levitan** 46:45  
Uh-huh.

**  
Nathan Carver** 46:49  
And then...

**  
Val Levitan** 46:50  
But 94941 has five more stories.

**  
Nathan Carver** 46:55  
Correct. So these are what those items I shared in the calendar invite.  
I just want to review those things and say...  
Yes, this is the right direction. And that's all I want before I start implementing these under 941.

**  
Val Levitan** 47:18  
So basically you will be working under DTP 941, but you will rearrange the stories to fit the agenda.

**  
Nathan Carver** 47:21  
Yeah.  
But.  
Correct.

**  
Val Levitan** 47:27  
Okay, got it clear.

**  
Nathan Carver** 47:32  
Yeah.

**  
Val Levitan** 47:33  
Thank you, everyone.

**  
Mikhail Perelman** 47:36  
Thank you.

**  
Lev Rudky** 47:36  
Tse.

**  
Val Levitan** 47:37  
Bye-bye.

**  
Lev Rudky** 47:38  
Bye.

**  
Nathan Carver** 47:38  
All right. Thanks, Val.

**  
Mikhail Perelman** 47:38  
Val.

**  
Nathan Carver** stopped transcription
