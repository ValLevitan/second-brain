---
tags:
  - Mother-Goose-Board
  - data-transfer
  - security
  - technical
  - juan
  - hardware
---

# Transcript
**July 7, 2025, 6:46PM**  
Juan Martinez started transcription

## Meeting Discussion: Mother Goose Board Replacement Solution

### Overview
**Jim** (0:03): It's the barrier you set up for a gift card collect. It goes ahead and sends that data to an FTP site and then you can peruse it. And well, let me tell you what we're currently doing 100%. They break that. They break that barrier. It prints a normal Mother Goose voucher that says gift card voucher.

(0:15): Sure.

**Jim** (0:23): And gives you a QR code. You can then go to the kiosk and boop your QR code and get your gift card.

**Juan Martinez** (0:32): OK.

**Jim** (0:32): And all it's doing is sending that collect data to A to an FTP site that the a company we were already working with. But it it doesn't have to be them. I mean it's the same data, but they then their server grabs that data packet. And waits for them to collect or to scan the QR code. So obviously we can send that data anywhere you want.

**Juan Martinez** (0:55): OK. Sure, sure, sure. Um, Nathan, at the highest level, I believe that that would satisfy. What we're looking to do, correct?

### Technical Details

**Nathan Carver** (1:11): Correct. So this board adapts the Mother Goose to send the print, the ticket through FTP to a server and the company or whoever we would JBL in this case would just monitor that server for new. For new files and then pull them.

**Jim** (1:31): Yep.

**Nathan Carver** (1:33): And that would be the same ticket information as as if it was printed out.

**Jim** (1:38): Yes.

**Nathan Carver** (1:39): OK.

**Jim** (1:40): The way we're currently doing it is it generates a UUID for that collect. That's the only thing that's in the QR code is that UUID. The file that gets updated to the FTP server is that UUID number dot GC for gift code. It can be obviously that's just the file name. But you see a new gift card file show up. Boom. You know there's a guy holding a ticket.

**Nathan Carver** (2:04): I see. So the UU to the file is just the UUID number with some suffix.

**Jim** (2:12): Yeah, with the in this case currently has the location, name or number, the value of the collect, you know, just the data that would be on a normal ticket is inside that gift card file. It's right now it's just in UTF 8 ASCII you know.

### Security Considerations

**Nathan Carver** (2:28): Yeah, yeah, yeah. OK, got it.

**Jim** (2:30): Yeah. And I can send you an example of what the file looks like. And if you want it modified because you know the guy we were doing it with, they just accepted it first pass. It's like you sure you don't want anything added subtracted or whatever, you know, but yeah.

**Juan Martinez** (2:32): OK.

**Nathan Carver** (2:34): Yeah, that'd be perfect.

**Juan Martinez** (2:35): Yeah, that. Sure.

**Nathan Carver** (2:47): How are they validating for security purposes? How do they challenge the the file to be, you know, not not corrupted or fraudulent?

**Jim** (3:01): I guess they're doing it because of the way that, well, it's a secured FTD site and then yeah, we're just not, we're going in through a secure link and then I don't know what they're doing after that.

**Nathan Carver** (3:07): OK.

**Jim** (3:18): So.

**Nathan Carver** (3:18): OK, so you just OK from the Mother Goose sign, you just have a secured FTP site, you push the file and then it's black box from there.

**Jim** (3:25): Yeah, and we can do other. We can do other things too. It can be encrypted if it needs to be.

**Nathan Carver** (3:33): OK.

**Jim** (3:33): I mean, this is just how we shot it to them.

### Pricing and Hardware Details

**Juan Martinez** (3:37): And Jim, this piece of hardware, this board, would you be able to share that with me and pricing and anything like that?

**Jim** (3:45): Sure.

**Juan Martinez** (3:48): Um.

**Jim** (3:49): 455, Yeah. So what? 466, Yeah. So 466 bucks, whatever she just said.

**Juan Martinez** (3:52): There. OK.

**Nathan Carver** (3:57): OK, nice.

**Jim** (4:01): So yeah, we can send you a sample.

**Nathan Carver** (4:05): Yeah, that'd be great. OK. Yeah, Juan, if it has the same information as ticket, then that answers that question. Then it's just a matter of if we need to work out some way to, like we said, encrypt it, make it a little harder to crack, intercept, send a fraudulent message. That kind of thing.

### Installation Details

**Juan Martinez** (4:28): Sure, sure. And Jim, this board typically sits near or inside of the gaming machines or one of the bases or closer to the printer?

**Jim** (4:40): It's it literally replaces the Mother Goose.

**Juan Martinez** (4:43): OK.

**Nathan Carver** (4:45): Hmm.

**Jim** (4:46): And we made it to fit the exact same footprint of the old board. So if they want, they can just buy the board and slap it in the old case. So as far as the operator is concerned, they don't see anything different.

**Juan Martinez** (4:57): OK.

**Jim** (4:59): Try to keep it as simple as possible for the guys in the field.

### QR Code and Data Management

**Juan Martinez** (5:02): Sure, sure. And this this QR code. So one one of our thoughts on on making sure that there is no fraud going on is the QR code contains the full amount of that ticket, right? They don't have any ability to do a partial pay or do they or that's up to Kia.

**Jim** (5:20): The QR code has the QR code has no data in it other than it's the QR code that you attach to the file that's been uploaded. There's no value in it. It's just literally the Q. It's just the UUID number is the QR code.

**Nathan Carver** (5:35): OK, so the the board is giving it a unique ID and sending it and OK and then the board doesn't retain any data at that point. It's once it's sent, it's gone or is there OK?

**Jim** (5:40): Yep. Yep. I mean, it can't keep backups, but I'm currently as soon as it gets a valid upload, I delete it from the local server.

**Nathan Carver** (5:55): OK.

**Juan Martinez** (5:57): And this is a a per machine board in order to maintain that unique ID, right? This isn't one per location, correct?

**Jim** (6:04): It's one per location. You're literally just replacing the master controller, Yep.

**Juan Martinez** (6:06): 01. OK.

**Jim** (6:11): Still have to have the Yeah, yeah, it has to have a Mother Goose system in there. Yeah, yeah. So I mean, just it it drops in and replaces the current controller is what it does.

### Alternative Solutions

**Juan Martinez** (6:20): Course. Sure. OK.

**Nathan Carver** (6:29): OK, that makes sense.

**Juan Martinez** (6:31): If if for whatever reason we did not want to go this board route and we wanted to sniff that RS485 connection to the printer, but.

**Nathan Carver** (6:32): Yes.

**Juan Martinez** (6:44): Do that with your support. Like how? How? How do you envision that happen?

**Jim** (6:47): Oh yeah. Unfortunately, the protocol's kind of been glued together over 25 years of add-ons. So I I'm suffering from the Intel problem. I have to maintain backwards compatibility with all that old junk. So it's kind of a.

**Juan Martinez** (6:56): Yeah. Sure.

**Jim** (7:03): It's kind of a hodgepodge of multi packets for bookkeeping and single packets for this, but it's yeah, it's it's pretty straightforward.

**Juan Martinez** (7:12): OK.

**Nathan Carver** (7:15): OK. Is that something the engineer is just reverse engineering that or is there information we can that that is available that we can use to understand the signal?

**Jim** (7:28): Oh yeah, I mean, I just documented.

**Nathan Carver** (7:32): OK. Perfect.

### Printer Protocol

**Juan Martinez** (7:35): For these printers, is there more than one printer in the field, or does that even in any way impact that protocol going to the printer?

**Jim** (7:47): It just, yeah, the printer's just the the output device. We just use an Escape POS printer. But as far as everything that goes on the RS485 is completely different than what gets massaged out of it.

**Juan Martinez** (8:01): OK.

**Jim** (8:01): Yeah, it's just there's no, there's no pulses or anything. It's just RS45 data packets. It's a fixed packet size protocol. So you know, had I had I known then what I known, I know now I would would have done several things differently, but.

**Nathan Carver** (8:16): Yeah, right.

**Juan Martinez** (8:17): Sure.

**Jim** (8:19): Yeah, it started out as one guy saying, hey, I'd really like it to print collects behind the counter. OK, so we set it. I just, oh, we can just set a fixed packet size and rock'n'roll. Then it was, oh, can we print bookkeeping? Can we do remote crediting? Can we do? Yeah. So it's just. It just grew like a monster from there, but yeah.

**Nathan Carver** (8:37): That's how it goes. Yep, that's how it goes. Um.

**Jim** (8:44): But there's, yeah, I kind of broke the mold on some of the newer units where there's there's other packets in there. But it's for as far as covering the main, the main things like well, all the collects, the collect is just a literally a single packet that has how much it was. So that's pretty simple to grab.

### Machine Compatibility

**Juan Martinez** (9:03): Sure. And Jim, quick question, I'm other than seeing it and helping our Georgia office, I'm not, I haven't actually, you know worked with the Mother Goose is, is the device specific to machine manufacturers or is this new board just a direct drop in for any? Any kind of previous master board in there.

**Jim** (9:27): Well, unfortunately, yeah, unfortunately back in the old days or the only way to talk to a machine was via the the hard meters. There was no, you know, and now I don't, I don't think you guys support it, but now we we have a USB interface that you can target.

**Juan Martinez** (9:36): Yes.

**Jim** (9:43): Which is a hell of a lot better than the pulse interface, because it's instead of waiting for the pulses, you get an instant collect and instant data. Yeah, and it's fully galvanically isolated too, which is a big plus.

**Juan Martinez** (9:57): Sure.

**Nathan Carver** (9:58): Yeah. Okay.

**Juan Martinez** (9:59): Yeah, but so in our solution, go ahead.

**Jim** (10:03): Novamatic and. Oh, I can't think of the guy in Columbus that we just visited. There's like 3 or 4 manufacturers that target the USB machine, the USB board now.

**Juan Martinez** (10:15): OK, aristocrat, light and wonder.

**Jim** (10:18): Light and wonder opted not to. There's they're using. We do have isolated pulse boards where the net Rs 45 is isolated and that's what I recommend everybody grab here in Georgia, especially with lightning like we have here in Georgia, yeah.

**Nathan Carver** (10:24): OK.

**Juan Martinez** (10:37): Yeah.

**Jim** (10:38): But yeah, a lot of them are still sticking with the meters. I don't know why. Well, it might be because then they got to rewrite their software to talk to the device, so. It's a it's almost the same protocol as an ID 003 dollar bill acceptor. I tried to make it as simple something that they'd be familiar with already. Yeah, yeah, but it worked very.

**Juan Martinez** (10:49): Understood. OK. Sure, sure. That's the one we use as well.

**Jim** (11:04): And it was. It was originally intended to target guys that have multi games like the the fish tables because one board can handle up to it can emulate 8 seats. So if you've got an 8 player fish table, you can emulate all 88 player stations with a single board.

**Nathan Carver** (11:06): Nice.

**Jim** (11:24): Board saves them from having to buy a board from every station.

**Juan Martinez** (11:27): Oh, sure, sure.

**Jim** (11:28): Yeah, and that's what Janka Labs used it for.

**Juan Martinez** (11:32): Sure.

**Jim** (11:33): But yeah, so yeah, we can. Whatever we want to do, we can. We'll work with you.

### Wrap-up

**Juan Martinez** (11:39): Excellent then. All right. So I think Nathan, we we'll regroup on our side and then Jim, I'll, I'll get back to you with some some other questions and and how we get our hands on this so we can start playing around with it here in our Georgia office.

**Nathan Carver** (11:41): Alright.

**Jim** (11:51): OK.

**Juan Martinez** (11:54): Excellent. Nathan, did you have anything else?

**Jim** (11:54): You got it.

**Nathan Carver** (11:54): Alright. No, that's it. I think that's good for us to start digesting and going through.

**Jim** (12:03): OK.

**Juan Martinez** (12:03): Perfect. All right, Jim, thank you. I appreciate it and we'll follow up with you shortly. Great. Thanks.

**Jim** (12:05): All right. You're welcome. Have a good day. All right. Goodbye.

**Nathan Carver** (12:07): Thanks, Jim. Bye.

## Post-Meeting Discussion

**Juan Martinez** (12:10): Do you want to stay on for a SEC?

**Nathan Carver** (12:12): Yeah.

**Juan Martinez** (12:13): Yeah. And I I threw out there going both scenarios because knowing Val, you know, he may say, oh, I don't want to pay $466 per machine or per location, but that that's actually a reasonable price and then that cost may fall on the master that we partner with as a requirement. Saying, hey, in order to install our Flex POS or pay network, you need to switch to this more advanced Mother Goose replacement board.

**Nathan Carver** (12:46): Yeah. And if if we don't want to go that route immediately, we could still support. Ideally we could support both if if it sounds like he'll send, Jim will send us documentation on the print signal. So that will greatly increase our speed at digesting that.

**Juan Martinez** (12:55): Oh, absolutely. Yes.

**Nathan Carver** (13:04): The FTP server, if it's a secured server, you know SFTP, then that's more secure than a physical printer cable.

**Juan Martinez** (13:04): Yeah, yeah. Oh, 100%. I I I my eyes lit up when I heard that. I'm like, Oh yes, way better than serial wires being intercepted.

**Nathan Carver** (13:16): Yeah. Yes. So then it's, you know, the only, the only way they could hack that signal is to somehow get the credentials off that board. They would have to physically get at that board I would think to get the credentials, so.

**Juan Martinez** (13:34): Right. Yeah, yeah. And and just so we don't overthink it, all of this happens today. So if they're scamming, they're already scamming today. You know, it's the master's responsibility to say, no, wait a minute, my machine reports say we only paid out $100 yesterday. Why did you issue $200 in gift cards? It's just that now we're in the middle and we're on the hook with MasterCard for that money. So, but operationally it it it's a there's no more. Well, there will actually be more security in our route than there is today. But um.

**Nathan Carver** (14:20): Yes, yeah. So it's definitely more secure than the physical cable, but and I'm glad Jim will work with us, I think to create some encryption or whatever we need. But we do, we do need to add some, yeah, fraud detection in that file, some way to say this file doesn't look authentic.

**Juan Martinez** (14:35): Absolutely. Yeah, yeah, he he has an assortment of of manuals and documents on his website. I'm gonna, I think I moved most of them to Confluence. I'm gonna verify that and then I'll send you the link cause I've I've downloaded almost all of them already either before.

**Nathan Carver** (14:39): It.

**Juan Martinez** (14:58): Or recently. So I have almost every manual that he says he's gonna send us. It is on their website and it you don't need any password or anything to get to them. So I'll I'll throw them on Confluence and send you that link.

**Nathan Carver** (15:13): OK, yeah, if we can get a sample file from him, like that would be good too. You get that shared with Paul.

**Juan Martinez** (15:17): Yeah. Absolutely.

**Nathan Carver** (15:22): Um, OK.

**Juan Martinez** (15:24): And the um uh. Say. Yeah, I'll, I'll reach out to him back to say how do we buy this board and get a sample going an entire system like that. I'm not sure why Val wanted for Mother Goose environments, but I'll figure that out and then we'll get all that going. I can say. Oh, explain to me. So the the data is uploaded to FTP. This QR code is married to a unique identifier. We need to go and fetch that unique identifier from FTP, which in that table contains that oh, this is a $10 cash out. Is that at the highest level? Is that it?

**Nathan Carver** (16:16): Yeah, so based on what he said, the file. So they assign a unique ID to that file and then they send it and then on their server they delete it. So the only record of that file is what's in the tax. So it doesn't sound like there's nothing else to go to.

**Juan Martinez** (16:33): OK.

**Nathan Carver** (16:37): Um. We would have to just one moment. OK, so we would if they hash, for example if they hash the file then as we have on our site we have to have the ability to unhash it and pull the information so or or crypted unencrypted so.

**Juan Martinez** (17:01): Mhm.

**Nathan Carver** (17:07): We'll just have to have that handshake, which is probably.

**Juan Martinez** (17:08): Sure.

**Nathan Carver** (17:13): It should be pretty simple to implement and adds just another layer of prevention to it.

**Juan Martinez** (17:20): Yeah, sure.

**Nathan Carver** (17:21): But yeah, I don't. There's no other, there's no other lookup table I think to go back to like their server's gone. So all the data's gonna be in that file. So essentially everything we see on the ticket will be in the metadata of that file.

**Juan Martinez** (17:36): Sure, what?

**Nathan Carver** (17:38): We just don't want plain text. Like I think we need to have it somehow. Yeah, somehow encrypted. So it's not just plain text going out.

**Juan Martinez** (17:47): Sure, sure. Yeah. And also he, he never mentioned the site ID. So from our perspective, yes, every Mother Goose has a unique identifier. Oh, but yeah, that's for the whole location. So that's how we know that that unique ID is for that location. I guess we just need to be mindful of that Mother Goose does fail and that that does get replaced. How do we track the unique identifier of a swap out unit versus the one? Because the master can change that without our knowledge, without our direct knowledge, I guess we would find that out. After the fact, after transactions got rejected because we were looking for a different UID.

**Nathan Carver** (18:32): Yeah, so we would, right. So we would record the UID from that site and then every new ticket that comes in, we would just compare it. That way as soon as we pick up the the ticket, we can check the ID and if it's different, we can flag it.

**Juan Martinez** (18:48): Sure.

**Nathan Carver** (18:49): Before there's any attempt to retrieve a gift card on it and then then it may be we decide is it do we contact the site immediately? Do we hold all processing or or like we can make those decisions?

**Juan Martinez** (18:59): Right. Perfect. Yep.

**Nathan Carver** (19:05): OK.

**Juan Martinez** (19:06): I'll copy you on my the gym, just you know, asking for some detail on this new Mother Goose replacement board and and anything else he wants to share with us.

**Nathan Carver** (19:18): OK. Yeah, it sounds good.

**Juan Martinez** (19:20): Perfect.

**Nathan Carver** (19:22): Well, that was it.

**Juan Martinez** (19:22): All right, Nathan, that was quick and easy. It goes the same. The other, the other company is called Omega Games and I'll have the actual contact tonight and then we'll reinitiate a call with them to see what they're. I think that they are a much smaller.

**Nathan Carver** (19:26): Yeah, all right.

**Juan Martinez** (19:42): If like 1% of the market might use a product and it might be only in, they're also a distributor slash operator or master, so they may only use it at their sites. And if we do or don't have business with them, I'll find that out tonight as well, so.

**Nathan Carver** (19:51): OK.

**Juan Martinez** (19:58): But the the 99% of the market is definitely using this this Multi Goose RKS solution.

**Nathan Carver** (20:04): OK. All right. Sounds good.

**Juan Martinez** (20:08): We appreciate it, Nathan. Thanks.

**Nathan Carver** (20:08): All right. Thanks, Mark.

Juan Martinez stopped transcription