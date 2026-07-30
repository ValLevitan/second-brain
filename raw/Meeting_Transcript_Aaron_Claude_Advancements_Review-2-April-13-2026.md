**Claude_advancement_review_implimentation-20260413_085429-Meeting Recording**

13 April 2026, 12:54pm

6m 2s

**\
Aaron Bockelie** 0:03\
I\'ve been away is a really great example of\...\
reverse engineering hardware. So I know that, you know, JVL probably has more of a\...\
procure and get the data sheets and specs and stuff for things.\
But also.\
I have a repo that I want to, I\'ll just share the screen and I\'ll send you the path to.\
Let me find the right browser window. There we go.\
So you can see the page, the GitHub page.

**\
Val Levitan** 0:43\
Yeah.

**\
Aaron Bockelie** 0:44\
Okay, so I bought these new headphones.\
I mean, their Bose QuietComfort Ultra 2s, their \$500 noise cancel active noise canceling headphones, right?

**\
Val Levitan** 0:58\
Yeah.

**\
Aaron Bockelie** 0:59\
The problem is, is the app for them sucks. It\'s got to be on a phone. I can\'t really use them on Linux. And I mean, I can connect to them, but I can\'t control them. There is no binary or program or whatever to be able to make them work. And Bose does not publish anything related to how to\
interact with these things. And so what happened was I was able to build a software library. This is just the library. There\'s two pieces to it, a library and an application. This is literally the application that the Attend tool helped write much faster.\
is that it can completely control the headphones with all of the parts by, essentially, I collaborated with it by doing packet captures, Bluetooth packet sniffing of the communication protocol between the devices, between the headphones and the cell phone app.\
the app on my phone.\
By playing with different settings, like the win block setting, or changing the equalizer settings for the audio, or playing with the treble, or toggling multi-connections and stuff like that.\
We were able to understand the communication protocol that the headphones used to talk to the app, which is not published and private, like nobody, Bose does not disclose any of this.\
And we were able to reverse engineer this into an actual C library that can be included with any application, so C, and just because I wanted it to be available for people, it\'s written in the equivalent thing is written in Python and Rust.\
So in Rust, we have the device library too. We can see how we have every single device, all of these headphones, and all of these Bose devices.\
The second half of the engineering effort was to take the, to let Claude find the app on my phone, download it from the phone, disassemble the app that I downloaded from the Google Play Store.\
look for all of the information of the strings, including the internal code names of the devices and all of the different categories, and build this library up from that. And so now what happens is that when we\'re all done,\
We have.

**\
Val Levitan** 3:34\
Yeah.

**\
Aaron Bockelie** 3:35\
An actual application.\
See right here the tray menu picture. So here\'s the picture of the thing configuring it and controlling it. Here is noise cancellation, the equalizer, and all of the internal management. This manages the profiles on the headphones themselves.\
Why am I telling you, a hardware manufacturer, about how to do this?\
It\'s because\...\
This is an excellent way to get your own set of specs and spec sheets that fit your hardware, what you want to build, and possibly unlocks a cheaper route to hardware specification or hardware use for your products in the future.\
That you don\'t have to go through the custom procurement pipeline for stuff. In many cases, you can just use this to integrate the code and the libraries and acquire them much, much faster than you would be if you had just gotten the standard stuff from a vendor, because most of the time the drivers and the software.\
for stack and everything from the vendor are terrible. And this is a great way to write exactly what you want instead.

**\
Val Levitan** 4:49\
Understood. Thank you.

**\
Aaron Bockelie** 4:51\
So, that\'s kind of the other example, and that\'s also out there available on the on my profile for looking at as well.

**\
Val Levitan** 4:58\
Thank you. That\'s helpful.

**\
Aaron Bockelie** 5:01\
Oh.\
Those are kind of the two.\
Big things that were done, I guess, that I could that I would describe.\
Yeah.\
The the.

**\
Val Levitan** 5:13\
Everything, everything is extremely interesting, and it just takes me a little time to reflect on it and lean back and reflect and just wrap things around my mind.

**\
Aaron Bockelie** 5:23\
Yeah.\
Yeah, of course. It\'s just, it moves really fast, you know? And I think it\'s just only moving faster, which is why\...\
I kind of needed to get ahead of the curve a bit with the attend tool because it\'s getting to the point where I can\'t wrap my mind around all of it all the time.\
And for me\...\
Well, in the document, in the documentation for a 10, let me, I\'m gonna switch back to that for just a minute. I don\'t know if you wanna change your recording around or what.

**\
Val Levitan** 5:58\
I do.

**\
Aaron Bockelie** 5:59\
Um\...

**\
Val Levitan** stopped transcription
