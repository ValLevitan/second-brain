**Aaron + Val-20251120_083250-Meeting Recording**

20 November 2025, 01:32pm

31m 36s

**Aaron Bockelie** 0:03  
So we're gonna try here in just a second here and load the right.

**Pavel Frolov** 0:08  
Uh, but what? What was the version that you are actually, uh, try to run on the board? It was 6.6.

**Aaron Bockelie** 0:15  
So the mainline, the mainline version of Linux was 6/2 or six. I can't remember exactly. I'm using build, I'm using build root as the distro for it.

**Pavel Frolov** 0:23  
61 probably.  
Actually, it's it's OK. It's OK. Any.

**Aaron Bockelie** 0:29  
So.  
The issue is well what I what's happening is is I'm fighting the the DTB that I so I'm I extracted the DTB from the other from the board that was given to me and then decompiled that.  
I also pulled the images out of there. They have a bunch of images for different things inside of that board, so I just sort of bin walked it all and pulled it all apart. But what I'm gonna do now is I'm gonna use the rock chips got a 6.6 PSP.  
Kernel. So I'm gonna use that one right now. It's it's still building right now. This takes time.

**Pavel Frolov** 1:05  
Mhm.  
Actually I just wrote you that for the second board, actually we have DTSI. Yes, yes, we have two files and they are not just taken from the board, but original.

**Aaron Bockelie** 1:19  
That that's the other one, right?  
Yeah.

**Pavel Frolov** 1:29  
Original files. It's it. It should simplify actually.

**Aaron Bockelie** 1:29  
OK.  
Sure, I I will try that one next. Which board should we be focusing on this the the one I'm working on now or the OR or this one?

**Pavel Frolov** 1:34  
Uh.  
Any any boards that better suits to our needs. I mean is the simplest way to to get sources and to build system for them.

**Aaron Bockelie** 1:52  
Yeah.  
OK, yeah, well, what we'll see here in a minute is, well, you can see right now the computer's pretty busy. It's running all the cores building right now still, but.  
Once we're done here, I will put it on this SD card. So the the trick, all I'm doing is I'm I actually soft bricked it when I was messing around with it. I loaded the wrong Uboot into the thing and then broke it.  
Oops sorry. And then had to unbrick that by catching Uboot ahead of time and then putting it in. Anyway I broke some stuff so I put so I'm actually compiling Uboot as well from sources and.  
Building a special U boot image too. That way we have control of the whole boot chain.

**Pavel Frolov** 2:48  
Definitely that's why I said that it will not be ready to to release solution because actually we do not know exactly what the DTS and DTB file to use and.  
At some some state you will break your board and need to understand how to unbreak it and continue continue assigning the yes.

**Aaron Bockelie** 3:07  
Yeah.  
Yep, well, I already, I already traveled that journey yesterday. So yeah, so I've got a functional U boot builder for this too.  
So it's still still building. You can see here this is kind of the last boot scroll from from booting up and anyway. So what I was saying is is that I the process is.  
Write an SD image of it. It's bootable. Pop that into the thing. Catch it in Uboot. Switch the bootloader to use the XP4 load in in Uboot to switch it over to boot off the SD temporarily.  
Cuz I have already configured it. That way you can then load it on there. Basically you could just in Uboot mode. You can switch between booting off of the SD card or the internal EMMC and then I have a little script that on the built that I wrote that is included with the builder that then runs the setup.  
It copies everything onto the EMC. It wipes the EMC and copies everything onto it, and then on a next reboot it even sets the little device boot script in there, so it'll just read it and start. So it's pretty straightforward. I could probably.  
Streamline the rest of it so it's just like a single script. You run into the watch for the device on Uboot, catch it.  
Wipe, you know, do all the bits and pieces, but I just want to. I really just want to try to get the DTB to load correctly with the Ethernet and all the other other services on it.

**Genadi Peari** 4:52  
I'm sorry, after you Aaron, after you boot from SD card, do we do automatically rewrite the boot on the EMMC or we expect to user to press some confirmation?

**Pavel Frolov** 5:07  
It easily can be automatic.

**Aaron Bockelie** 5:08  
I mean, it doesn't matter. It could be done either way. It could be monitored. I mean this is.

**Genadi Peari** 5:11  
This is my question, Pavel, because I I think it's.  
Do you do you actually want to make it automatically?

**Pavel Frolov** 5:22  
Yes, I think.

**Aaron Bockelie** 5:22  
If you want, I'll send you. I'll I'll spec out a giant red button you can push.  
So basically what is going on is I have uh.  
Well, I can unplug it probably here. Actually, I'll just set my camera down.  
So I have.  
FPDI serial right there.  
And I just oops, I don't know why it zoomed in like that. Sorry. And then right here is the debug port on on the board and debug port is just.  
Debug port is just serial console. That's how it's set up. So I would imagine all I would have to do is just watch the serial port. You run a run a program on the computer watching for it, plug in serial.

**Pavel Frolov** 6:16  
Yeah, yeah, I'm.

**Aaron Bockelie** 6:27  
Turn it on, give 12 volts power, it'll catch it, inject it into, you know, fix the Uboot mode with the SD card and then just run it. I mean, you could do all you could sequence it however you want is the point is what I'm getting at.

**Pavel Frolov** 6:37  
Uh.  
Actually in my understanding originally RK chips support some booting order and SD card is order number one and EMMC or NAND or something else order number 2 and number.

**Aaron Bockelie** 6:54  
Yes.  
So I changed the boot order, so I actually switched the boot order around on permanently on the board for me.

**Pavel Frolov** 7:06  
Usually it's it done through the.  
Mechanical operation.

**Aaron Bockelie** 7:14  
Well, because I have my I have my own U boot. I loaded the tools to change it so I it doesn't matter.

**Pavel Frolov** 7:18  
Oh, it's so it's still it's it's still different boot order. It still supports different boot order. If you change it something in your boot, you already post this code into EMMC.  
And it's still continue button from MMC.

**Aaron Bockelie** 7:36  
Yeah.  
It will, so I have to catch it and force it to boot off of the SD card every time.

**Pavel Frolov** 7:50  
So using the you boot environment variable, you are just switching the steps three or step two of boot mode from EMMC to SD.  
But originally it's still taken for as SPL mode from the EMC.

**Aaron Bockelie** 8:05  
Yes, and what I'm saying is.  
It'll yes, it'll it'll always boot off the MMC. And what I'm saying is, is that I could build a little supervisor script that could just be run on a computer that is connected over serial and looks for the Uboot messages and just.

**Pavel Frolov** 8:15  
Oh.  
Uh.

**Aaron Bockelie** 8:27  
Stops it, halts it and injects it and turns it in and and manipulates you boot live. There's that's that's that's only if we're looking for something to make it an automatic installation process and things like that.  
Just I don't know because I'm assuming you want to be able to make it as simple as possible for these boards to be flashed.

**Pavel Frolov** 8:49  
I still think that it's possible without this procedure just to make specially organized image that can be written on SD card that boots from SD card directly all all the steps.

**Aaron Bockelie** 9:00  
Well.  
Yeah, we could do that too. I just I always I always like to have at least with these embedded things with the rock chip or with Beagle Board and the other ones that I played with. I I prefer to have a bootable EMMC image of some kind on the boards if you.  
If you drop the SD card off into the crack of the floor, it'll still be usable.  
So, but it's up to you guys. I mean, however, OK, so hang on, let me see. I got.  
Oh, I got a I've got a missing bin image. Hang on, let me do an incremental build.  
Getting there.  
So in order to go fast, I just share with what I'm working on and sort of steer it back and forth. So I just sometimes have to share.  
All right, so I gotta run a clean build again. Womp womp.  
Um.  
Oh, I can show you what happens right now. You can see I'm just going to put power onto it. You can see right here.  
So we're getting boot.

**Pavel Frolov** 10:23  
Yeah, yeah, I saw was the same, yeah.

**Aaron Bockelie** 10:25  
And then and then right here is I'm interrupting, but notice the model number. This is not that board, so I've built our own Uboot on another device style, but it's compatible enough.

**Pavel Frolov** 10:38  
OK.

**Aaron Bockelie** 10:40  
What I had to do is suppress ADAC. Basically the pin GPIO pins from the board to this carrier board. It was detecting a keyboard press, but not it was actually it was stuck in a loop, so I had to do some stuff.  
To disable the ADAC that was pretending to be press a key. So now let me let me just actually I don't have the SD card ready yet so I'll just boot. I'll boot off the latest image here so.

**Pavel Frolov** 11:10  
OK.  
Actually on on on this board I can stop running you you boot in automatic way just pressing control plus C not just any any press but control C.

**Aaron Bockelie** 11:26  
Yeah.  
Uh.  
The original image that I had with this did do that.  
O.  
So you can see here.  
And then the issue right now I've got is.  
The network interface is not mapping the DTB to the devices right now, so I'm working on that. That's why I'm building the kernel off of rock chip kernel instead of the just mainline Linux kernel.  
But rock chips is 6.6, that's they've got a kernel 6.6, which is pretty new and I think that's worthwhile to try.  
Anyway, we're just watching paint dry right now while the kernels compiled.  
Um.  
Let's see what other interesting things did I encounter? This board somebody was using as a, or at least it had.  
A game game platform, game console platform on it. It was kind of funny. There was a directory for like video game emulator on it, so someone was testing that or something maybe.

**Genadi Peari** 13:18  
So how important for us to specify which exactly platform we'll be using? Because we need to get some quotations to see which one is more suitable like price wise and harnesses and.  
Hitting.  
They're more or less similar, I mean.

**Aaron Bockelie** 13:39  
Pretty similar. One's a little bigger than the other.

**Genadi Peari** 13:41  
No, no. In terms of support, in terms of work you do after we change or is it like it will be pretty much the same, right?  
No.

**Aaron Bockelie** 13:56  
I don't know this this port has a bunch of Baidu links to download all the support for it, but I don't have a Baidu account to go download things. I mean, that's not that hard. I just have to go figure that out, but.  
There's a lot of Chinese support for this board. I just don't know if that's something you want to look into.

**Genadi Peari** 14:22  
So, so it's it's better for us to concentrate on one model.  
It's better sooner. It's better, eh?

**Aaron Bockelie** 14:30  
Yeah.

**Genadi Peari** 14:34  
They'll get the.  
Closer look to get quotations and.

**Aaron Bockelie** 14:50  
All the core is turning red.  
Oh, they were turning red.  
On.

**Pavel Frolov** 15:03  
Anyway, Aaron, just to to your knowledge, we just filled the form official request for the SDK from Rockchip. So I think actually we will get practically the same system.

**Aaron Bockelie** 15:04  
Yeah.

**Pavel Frolov** 15:21  
But from original rock ship I I I assume that we we we can get the.

**Aaron Bockelie** 15:27  
Well, to be fair.  
This is where I'm pulling the the sources.

**Pavel Frolov** 15:41  
Since you posted it last time.

**Aaron Bockelie** 15:44  
This is where I'm pulling sources from right now. Here's 6/1, here's 66. This is Rock Chip Linux. This is their official real so.

**Pavel Frolov** 15:54  
Yeah, yeah, everything, everything you boot and file system Linux actually already available for us, but external external scripts.

**Aaron Bockelie** 16:07  
Mhm.

**Pavel Frolov** 16:10  
I I think, I think they will provide us special files including some some some documents so.

**Aaron Bockelie** 16:18  
Sure.  
Obviously that makes it easier, yeah.

**Pavel Frolov** 16:24  
Yeah.

**Genadi Peari** 16:26  
Is the boot from USB flash drive also available or?

**Pavel Frolov** 16:34  
I don't think so. Actually it will be done as Aaron explained before. It can be done through the you boot environment variable to set load this file from USB and boot.

**Genadi Peari** 16:41  
Mhm.

**Pavel Frolov** 16:50  
In this approach it it, but it it will not be a full boot process. It will be partly from EMMC and partly from.

**Genadi Peari** 16:59  
Mhm.

**Pavel Frolov** 17:01  
USB highly likely 99%.

**Genadi Peari** 17:02  
OK, so instead OK.  
OK, no problem. Let's stay with TF card for the full update and for JVL application we create a partition rate for.

**Aaron Bockelie** 17:19  
So I'd imagine you could you could decide to write a chain of basically chain chain boot things going on here where?

**Genadi Peari** 17:19  
Well, great.

**Aaron Bockelie** 17:30  
I think you had written in your in your requirements to if if an SD card is present then find the script and run an update. That seems pretty.  
Retty easy to do.

**Pavel Frolov** 17:44  
Just just on on big device and write some initial image.

**Aaron Bockelie** 17:51  
Yeah, cuz that's ultimately what I'm doing. I'm just copying my images over. It's however you want the convenience to act, right? Like I'm always, I'm always of the opinion. Put the SD card in there, turn it on one time.

**Pavel Frolov** 17:56  
Mhm.

**Aaron Bockelie** 18:09  
And then it'll what it would do is it would just check the SD card every time it boots and if everything's up to date and then it's up to date and it doesn't copy any files or anything like that. But if you take it out after it's done its update.  
It still works just fine.  
It's just I always feel like SD cards are a source of failure in both their, you know, if they're unplugged or not connected or if the card fails or whatever kind of thing versus the onboard EMC. But I know you also want to have more storage probably for files.  
All other thing.  
Do what you do.  
The building.  
Sorry, I had to do a full kernel build it.  
Boring watching it, but.  
OK.

**Val Levitan** 19:19  
OK, friends, if Aaron answered all of your questions, then I think the the meeting, the purpose of this meeting is completed and I.

**Pavel Frolov** 19:32  
Probably the last just one one last last question. Aaron, I saw your actions, GitHub actions and seems I I can reproduce it but.  
What? How can I get binaries from there? Are you starting scripts to to make release or it?

**Aaron Bockelie** 19:55  
Oh well.  
Yeah, look in here.  
Build kernel, build remote, build SD image, build you boot, build root, which is what we're running right now. And so we can run local release or release and local release just create publishes the images in this repo here.

**Pavel Frolov** 20:06  
Uh huh.  
Mhm.

**Aaron Bockelie** 20:22  
Release pushes them up to GitHub with your credentials to your repo, so you wouldn't be able to run release on mine. You'd have to clone it and fix it and adjust the grip for the right.

**Pavel Frolov** 20:34  
Oh OK and and and then and then question how to organize this build system on local computer, not on GitHub. So you you're using some.  
Voter container.

**Aaron Bockelie** 20:49  
So I yeah, so so I use a um.  
Second here.  
So this is the buildroot builder.

**Pavel Frolov** 21:06  
Mhm.

**Aaron Bockelie** 21:07  
And I'm grabbing the build root version of course, and then I use a Docker container. I'm using the Ubuntu 2204 Docker container to build this, which is essentially the same container that GitHub uses and this way.

**Pavel Frolov** 21:15  
Uh huh.  
Mhm.

**Aaron Bockelie** 21:24  
It doesn't matter what OS I'm running host wise, I just use I build inside the container.

**Pavel Frolov** 21:32  
OK, probably in my case I will also try to use this approach something to install docker.

**Aaron Bockelie** 21:32  
So.  
Right here you can see what I'm doing is I'm pulling the user ID, my user identity. So when the container doesn't run as well, it writes the files not as root, but as my identity for convenience because otherwise they end up as root and owned.  
And basically it's.  
Checks the dependencies, initiates the container, starts running the build and it's building here.

**Pavel Frolov** 22:08  
Mhm.

**Aaron Bockelie** 22:09  
And then what can happen is, is after I have these build images done, I can push them up to GitHub into. That way I can basically treat it as a local runner essentially. But I wanted to make sure that we had a remote runner that ran entirely on GitHub as well. It just takes.

**Pavel Frolov** 22:20  
Mm-hmm.

**Aaron Bockelie** 22:29  
It's a it takes like an hour or two to to build. It takes a long time.

**Pavel Frolov** 22:34  
Yeah, but OK, I understand that in any case we will need to modify build infrastructure to take all the sources, not from the white.

**Aaron Bockelie** 22:44  
Mhm.

**Pavel Frolov** 22:51  
World Wide Web, but from from our local either storage or GitHub or mirror.

**Aaron Bockelie** 23:01  
Yeah, oh, right at the end.

**Pavel Frolov** 23:02  
So we we need to clone kernel, need to clone your boot, need to clone scripts or even binaries related to file system, yeah.

**Aaron Bockelie** 23:15  
Right, right. You will need to control all those sources, but I I think that's pretty easy to identify those in the build script so you can keep copies and maintain them.

**Pavel Frolov** 23:24  
Yeah, OK, too. Thank you.

**Val Levitan** 23:28  
OK, so I invite uh.  
Genadi and Pavel to communicate. I I formed. I formed the chat. Please communicate in this chat. Aaron, I know that you don't like to look at any emails or teams messages, but would you please?

**Aaron Bockelie** 23:51  
I will keep an eye on it.

**Val Levitan** 23:51  
For the next two days.  
OK, please do. Yeah, at least for today and tomorrow maybe, because I really would like Pavel to take a firm grip as time is of extreme sensitivity to us and Genadi.

**Aaron Bockelie** 23:58  
Yes.

**Val Levitan** 24:10  
Can you please order more samples, especially for Pavel Tuminsk?

**Genadi Peari** 24:16  
I believe at this point, if Aaron goes so fast, we need to finalize which supplier we go with. We will get the most convenient and cheaper version. I believe they're all the same.

**Aaron Bockelie** 24:33  
I haven't pushed these to the remote repo, but I've structured this repo in a way to allow us to investigate multiple boards with the same build system. So I've got DT BS for this board and its own thing, and then I'm going to explore the other one. That way Genadi, you can choose.

**Genadi Peari** 24:33  
****.

**Pavel Frolov** 24:45  
I saw.

**Genadi Peari** 24:50  
Yeah, the blue, the blue one. Yeah, check the one, this one. So we'll do quick check. We'll order more boards of the final version and we need to prepare set of harnesses and displays for Aaron, I understand.

**Aaron Bockelie** 24:51  
You know, you have the most the blue one. Yeah, yeah.

**Genadi Peari** 25:08  
Is it?

**Pavel Frolov** 25:09  
Oh.

**Aaron Bockelie** 25:12  
Is there a preference if if I run into persistent DTB issues with this board to make it build cleanly, is there a preference for this board I'm working on now, the smaller one or the bigger one that's blue?

**Genadi Peari** 25:13  
Do you?

**Pavel Frolov** 25:27  
Yeah, actually as I as I have already said for this blue board we we have original file so.

**Genadi Peari** 25:34  
Yeah, they they gave. They gave us a DTB DTS.

**Aaron Bockelie** 25:37  
Right.

**Pavel Frolov** 25:39  
Highly, fairly like it will be easier.

**Aaron Bockelie** 25:40  
But which one is cheaper overall? I guess is the what? Which one is the better long term one to figure out?  
Is it the blue one?

**Genadi Peari** 25:47  
OK, you can blue one is probably.  
Preferable.

**Aaron Bockelie** 25:53  
OK OK so I will like let's I'm just really just want to try to get Ethernet and the DTB working that I pulled out of this back on to it and if if I continue to have problems I will stop and I'll switch to using the blue one and then Pavel if you could share those those DTBS with.

**Pavel Frolov** 26:13  
Yeah, yeah, I I just try to find it. Oh, probably, probably not. It was taken from your e-mail. Probably you can.

**Aaron Bockelie** 26:13  
Me.  
Yeah.

**Genadi Peari** 26:21  
Yeah, yeah, I have it. I have it. I'll send it to you.

**Aaron Bockelie** 26:22  
And the other thing is, is that if I have a working image on it, I can always decompile the DTB. That's not a huge problem. That's how I did this one.

**Pavel Frolov** 26:32  
Yeah, it will not be exactly the same as original because original consists some include files, include lines that actually depends from your boot code.

**Aaron Bockelie** 26:47  
Yes.  
Right.

**Genadi Peari** 26:52  
Sorry guys, so.

**Aaron Bockelie** 26:55  
OK, there we go. So now I got the build complete. So now let me just, I'll just show you the rest of the process here. So what I do is I have a build SD image tool. I'm going to specify SDB which is the device for that. I'm going to wipe the SD card.  
So now we're writing down the boot image onto the SD card.  
So now.  
Take it out of there.  
Let's turn off the board for a minute.  
But the D card in the board ower it U.  
Catch you boot, switch it to boot off of the SD card. So here let me.  
Just switched it over so I'm going to switch it to the load the image off the MMC. You can see that it loaded that.  
We're going to load the DTB.  
E.  
I'm going to set the boot arg. I'm going to kick off the boot.  
Now we're booting off the the SD card, hopefully.  
Maybe not. No, it's dead. So this is what I was saying. Oh, no, it's going. It's going. OK, good, good, good. Just took a while. This is looking a lot better, actually.  
OK.  
So now we have that. Let's just.  
Uh, still not seeing addressing. Anyway, I'll show you the rest of now. So now what do we do?

**Val Levitan** 28:37  
Aaron, Aaron, Aaron, Aaron, Aaron. I'm sorry to pinpong you from meeting to meeting, but because of time difference between Minsk and and you, I only have an.

**Genadi Peari** 28:40  
But.

**Aaron Bockelie** 28:42  
Yeah.  
Yep.

**Val Levitan** 28:53  
Narrow window to catch some of the employees and so this particular person that I need to put online with you is available only for the next half an hour. So can can you can you let this thing run and I will book another meeting for us.

**Aaron Bockelie** 28:57  
OK.  
Yep.  
OK.

**Genadi Peari** 29:06  
Yep.

**Val Levitan** 29:13  
In exactly half an hour I will send an invite, but in the meantime, can you switch? You have a you have a other invite right now for a different meeting. So jump over and then I'll send another invite. Gentlemen, can we revisit this in half an hour?

**Aaron Bockelie** 29:17  
Yeah.  
Sure, I'll jump over to that.

**Val Levitan** 29:32  
Yes, thank you very much. I appreciate it.

**Aaron Bockelie** 29:33  
Yeah, it I actually will wrap up right here. You can see right here 10 more seconds unmounting.  
O Now we're unmounting the original file system.  
This one's a little slower because the kernel's bigger.

**Genadi Peari** 29:53  
So I don't need to ask Chinese anymore to prepare image with SD bootable.

**Aaron Bockelie** 29:58  
No. So now I'm gonna pull. I just pulled the power. I pulled the SD card. I'm just gonna power it up and let it auto boot now and now it's booting off of the image.

**Genadi Peari** 30:00  
Mhm.

**Aaron Bockelie** 30:11  
That we just blocked.

**Genadi Peari** 30:17  
Oh.

**Aaron Bockelie** 30:19  
Done.

**Pavel Frolov** 30:21  
Yeah, perfect.

**Aaron Bockelie** 30:25  
And here we are.  
So that's.

**Pavel Frolov** 30:28  
Your name, Your name, Dasha.

**Aaron Bockelie** 30:31  
Oh, yeah. All right.

**Pavel Frolov** 30:36  
Oh, that's a good.

**Aaron Bockelie** 30:37  
Yeah. All right. Let's jump over to the other meeting.

**Genadi Peari** 30:39  
Whoa.  
So I don't ask anything, any anything from Chinese, right? We do everything by ourselves.

**Aaron Bockelie** 30:46  
Eventually is no Chinese involvement. We just build our own stuff from sources. That's cool.

**Genadi Peari** 30:50  
So we get any any image and that's it. Just for any Ubuntu you you do you you do Ubuntu not dead, right?

**Aaron Bockelie** 30:54  
Yeah, we'll have to fix it. That's why I'm yeah.

**Pavel Frolov** 30:55  
Yes.

**Aaron Bockelie** 31:01  
Whatever we want.

**Pavel Frolov** 31:02  
It doesn't matter. For us, it doesn't matter. You would. Oh, you. Yeah. Thank you. Bye.

**Aaron Bockelie** 31:05  
Yep. All right. I gotta go, guys. Bye.

**Genadi Peari** 31:05  
OK.  
Thank you.

**Val Levitan** stopped transcription